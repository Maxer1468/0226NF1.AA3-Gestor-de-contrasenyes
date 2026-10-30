# 0226NF1.AA3-Gestor-de-contrasenyes

## Fase 1: Anàlisi i Justificació (Document d'Informe)
#### Heu de redactar un informe que justifiqui tècnicament la decisió de la Direcció i comparin les opcions. Aquest informe ha d'incloure:

<br>
<br>

### 1. Introducció i Justificació:

**Les contrasenyes febles o reutilitzades son un gran risc per a qualsevol empresa, ja que aquests tipus de contrasenyes no tenen prou seguretat per afrontar un atac.**

Que a de tindre la teva contrasenya perque sigui forta?
Sempre procura de posar:

* Minim 12 caracters.
* Lletras majusculas i minuscules (aA).
* Caracters especials (_-*).

**La funció principal d'un gestor de contrasenyes**

Desar i xifrar totes les teves credencials en un lloc segur, protegides per una única contrasenya mestra, per no haver de memoritzar-ne cap altra i utilitzar claus úniques i robustes a cada servei.

<br>

### 2. Comparativa Tècnica: Realitzeu una taula comparativa detallada entre:

### Bitwarden (Alternativa Online / Núvol)
* Emmagatzematge i Arquitectura: Basat en el núvol.

* Model de Seguretat: Xifratge d'extrem a extrem amb AES-256 i derivació de clau mitjançant PBKDF2 o Argon2id abans de la transmissió.

* Sincronització: Automàtica, nativa i en temps real entre tots els dispositius associats al compte.

* Accés Multi-dispositiu: Excel·lent i homogeni amb aplicacions oficials per a Windows, macOS, Linux, iOS, Android i integració nativa en navegadors web.

* Portabilitat: Les dades s'emmagatzemen al servei; és possible exportar la informació en formats JSON o CSV.

* Cost / Model Freemium: Model freemium amb pla gratuït molt complet i opcions de pagament per a funcions avançades.

### KeePassXC (Alternativa Offline / Escriptori)
* Emmagatzematge i Arquitectura: Completament local. Les dades es guarden en un arxiu físic amb format KDBX.

* Model de Seguretat: Xifratge local robust de l'arxiu KDBX amb algoritmes a escollir combinats amb Argon2/PBKDF2. Cap dada surt de l'equip.

* Sincronització: Manual o gestionada per l'usuari mitjançant serveis de tercers.

* Accés Multi-dispositiu: Excel·lent en entorns d'escriptori. A dispositius mòbils depèn d'aplicacions compatibles desenvolupades per tercers.

* Portabilitat: Portabilitat absoluta. Tota la base de dades s'empaqueta en un únic arxiu KDBX fàcil de moure, copiar o desar.

* Cost / Model Open Source: 100% de codi obert, gratuït, sense subscripcions, sense publicitat i sense funcions bloquejades.

<br>

### 3. Avantatges i Inconvenients: Resumiu els principals pros i contres de cada model (online vs. offline) des del punt de vista de seguretat, usabilitat i continuïtat del negoci.

### Bitwarden (Online)
Pros: Sincronització fluida, compartició segura de credencials entre equips i gestió centralitzada amb polítiques d'auditoria.

Contres: Dependència de la xarxa/servidor i major superfície d'atac potencial per estar connectat a Internet.

### KeePassXC (Offline)
Pros: Control absolut de la base de dades, independència total de servidors externs i ideal per a entorns d'alta seguretat sense Internet.

Contres: Sincronització complexa, dificultat per compartir claus en temps real i risc de pèrdua si no es fan backups locals.

<br>

### 4. Recomanació: Concloeu l'informe escollint l'eina que considereu més adequada per al personal tècnic de l'empresa i justifiqueu la vostra elecció.

Per al personal tècnic de l'empresa es recomana més el Bitwarden, ja que ofereix un equilibri ideal entre seguretat, operativitat i usabilitat. La seva sincronització automàtica entre navegadors i eines CLI agilitza el treball diari, permet compartir credencials d'infraestructura de forma segura entre companys i ofereix auditoria centralitzada.

<br>
<br>

## Fase 2: Guia d'Ús Tècnica (Manual Operatiu)
#### Utilitzant l'eina que heu seleccionat a la Fase 1 (Bitwarden, KeePassX, o similar), heu de crear una Guia d'Ús per a l'Equip Tècnic. Aquesta guia ha de ser clara i basada en captures de pantalla i instruccions pas a pas.
La guia ha de cobrir els següents punts obligatoris:
1. Instal·lació i Configuració Inicial: Descàrrega, instal·lació i creació de la BBDD principal o compte mestre.

* Descarrega del bitwarden a Linux:

![](/img/1.png)

![](/img/2.png)

Quan tinguem l'arxius descarregat l'executem.

![](/img/3.png)

Si no tenim compte de Bitwarden hem de crear una.

![](/img/4.png)

2. Generació de Contrasenyes Segures: Explicació de com utilitzar el generador de contrasenyes de l'eina (paràmetres, longitud, caràcters especials).

Quan tenim el Bitwarden descarregat accedim a l'aplicació.

![](/img/5.png)

![](/img/6.png)

Ja que volem generar contrasenyas entrem al generador.

![](/img/7.png)

Posem els parametres per una contrasenya segura.

![](/img/8.png)

Copiem la contrasenya per aixi posarla a altres credencials nostres.

3. Exemples d'Ús i Emplenament Automàtic:
    * Com desar una credencial d'un compte de correu electrònic.

        ![](/img/9.png)

        ![](/img/10.png)

    * Com desar una credencial d'una aplicació o servei web.

        ![](/img/9.png)

        ![](/img/11.png)

    * Com fer servir l’extensió del navegador per emplenar automàticament les dades.

        ![](/img/12.png)

        Per fer servir Bitwarden has d'instalar la seva extensió al teu navegador.

        ![](/img/13.png)

        Fem la configuració de l'extensió.


4. Gestió de Còpies de Seguretat (Backup):
    * Explicació detallada de com fer una còpia de seguretat de l'arxiu de contrasenyes (KDBX en KeePass o Exportació en Bitwarden).

        <img src="/img/15.png" width="328" height="822">

        Entrem a l'opció d'exportar.

        <img src="/img/16.png" width="793.5" height="320">

        Exportació del fitxer.

        <img src="/img/17.png" width="428.5" height="560">

        Confirmació de l'exportació.

    * Recomanació de la millor pràctica per emmagatzemar aquesta còpia de seguretat de forma segura (clau USB xifrada o emmagatzematge xifrat al núvol).

        <img src="/img/14.png" width="722.5" height="336">

        L'arxiu el pots guardar a un lloc on tinguis les teves contrasenyes o a un disc dur extern.
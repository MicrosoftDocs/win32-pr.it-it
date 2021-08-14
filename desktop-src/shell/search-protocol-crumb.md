---
description: Informazioni su come usare l'argomento CRUMB nell'interfaccia utente Windows Shell per controllare l'ambito di una ricerca.
title: Argomento CRUMB (shell Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f87a2b7-7f5a-4629-b881-44bf418b2df0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b93764f8014a5d9446811ef622f7c5afc20acbc6193d938c98642afaae5392fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452877"
---
# <a name="crumb-argument-the-windows-shell"></a>Argomento CRUMB (shell Windows)

L'argomento supporta istruzioni AQS (Advanced Query Syntax) complete ed è particolarmente utile per controllare `crumb` l'ambito di una ricerca. Oltre alle istruzioni AQS, l'argomento può assumere un parametro speciale in Windows Vista e i parametri e in Windows XP, come descritto più avanti `crumb` `location` in questo `kind` `store` argomento.

In questo argomento sono incluse le sezioni seguenti:

-   [Sintassi crumb](#crumb-syntax)
    -   [Esempi generali](#general-examples)
-   [Uso di crumb con Vista (posizione)](#using-crumb-with-vista-location)
    -   [Esempi di Vista](#vista-examples)
    -   [Costanti per cartelle comuni](#constants-for-common-folders)
    -   [Informazioni sugli argomenti](#argument-information)

## <a name="crumb-syntax"></a>Sintassi crumb

La sintassi di base è la seguente:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



La <column> parte è qualsiasi proprietà nel sistema di proprietà e <value> portion è un valore valido per tale proprietà. La <label> parte è un alias facoltativo per la proprietà visualizzata come suggerimento dell'interfaccia utente.

### <a name="general-examples"></a>Esempi generali


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



## <a name="using-crumb-with-vista-location"></a>Uso di crumb con Vista (posizione)

Nel parametro crumb Windows Vista supporta AQS completo e anche la proprietà , che ha un'implementazione speciale disponibile solo `location` in Windows Vista. È possibile usare una stringa AQS o la proprietà `location` all'interno di un singolo parametro crumb, ma non entrambi. Se il parametro crumb include AQS, tutti gli altri elementi nel parametro crumb vengono ignorati.

La `location` proprietà consente di specificare un percorso in cui eseguire la ricerca. Windows Vista può ignorare l'indicizzatore e attraversare direttamente la directory se il percorso non rientra nell'ambito della ricerca per indicizzazione dell'indicizzatore. Di conseguenza, queste ricerche possono essere più lente delle ricerche che usano l'indicizzatore.

Quando si specifica una `location` proprietà, sono supportati due parametri aggiuntivi e facoltativi:



| Parametro | Valori                  | Descrizione                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inclusione | include, exclude        | Specifica se la query deve includere o escludere elementi da tale percorso. L'impostazione predefinita è "Include". Windows Vista non supporta le esclusioni senza inclusioni. (Vedere l'esempio) |
| ricorsione | ricorsivo, non ricorsivo | Specifica se la ricerca deve essere ricorsiva di tutte le sottocartelle a partire dal valore definito nel percorso:<value>. L'impostazione predefinita è "Recursive".                             |



 

Per impostare l'ambito di una ricerca usando il protocollo **search:** sono disponibili opzioni diverse a seconda della destinazione dell'ambito.

Cartella in un computer locale:

-   Usare AQS (crumb=folder:<percorso con codifica URL>)
-   Usare l'argomento location (crumb=location:<percorso con codifica URL>)

Cartella in un computer/rete remoto:

-   Usare l'argomento location (crumb=location:<percorso con codifica URL>)

Cartella a cui si accede tramite un gestore Universal Naming Convention (UNC) noto:

-   Usare AQS (crumb=store: <UNC protocol handler name> )
-   Usare l'argomento location (crumb=location:<percorso con codifica URL>)

### <a name="vista-examples"></a>Esempi di Vista


```
search:query=vacation&crumb=location:shell%3aPersonal,include,recursive&
    
search:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 
    
search:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



Nel primo esempio viene eseguita una ricerca di "vacation" a partire dal percorso (un collegamento speciale alla cartella Documenti dell'utente), inclusa tale cartella e tutte le `shell://Personal` sottocartelle.  Vedere la tabella seguente.

Nel secondo esempio viene eseguita una ricerca all'interno di C: \\ Immagini, ma non in C: \\ Immagini \\ duplicate.

Il terzo esempio esegue una ricerca all'interno di C: Documenti, limitata ai file con \\ `kind` la proprietà impostata su immagini.

### <a name="constants-for-common-folders"></a>Costanti per cartelle comuni

Windows Vista consente l'uso di valori CSIDL che forniscono un modo univoco indipendente dal sistema per identificare le cartelle speciali usate di frequente dalle applicazioni, ma che potrebbero non avere lo stesso nome o percorso in un sistema specificato. Ad esempio, la cartella di sistema può essere "C: Windows" in un sistema e \\ "C: \\ Winnt" in un altro.

Usare questi percorsi con la sintassi seguente:


```
crumb=location:shell%3a<LocationName>&
```



Nella tabella seguente sono elencati i valori CSIDL. Per altre [**informazioni, vedere ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)



| Nome                        | stringa di ricerca                   | Descrizione                                                                                                                                                                            |
|-----------------------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| STRUMENTI DI AMMINISTRAZIONE        | ADMINISTRATIVE%20TOOLS          | Directory del file system che funge da repository per gli strumenti di amministrazione.                                                                                                            |
| APPDATA                     | APPDATA                         | Directory del file system che funge da repository comune per i dati specifici dell'applicazione. Un percorso tipico è C: \\ Documenti e nome utente Impostazioni dati \\ \\ dell'applicazione.                      |
| CACHE                       | CACHE                           | Directory del file system che funge da repository comune per i file Temporanei Internet. Un percorso tipico è C: \\ Documenti e Impostazioni nome utente File Temporanei \\ \\ Internet.               |
| CD ESEGOTI                  | CD%20SOCIEZIONE                    | Cartella contenente i dati da convertire in CD.                                                                                                                                             |
| STRUMENTI DI AMMINISTRAZIONE COMUNI | COMMON%20ADMINISTRATIVE%20TOOLS | Strumenti di amministrazione per tutti gli utenti.                                                                                                                                                    |
| APPDATA COMUNE              | COMMON%20APPDATA                | Dati dell'applicazione per tutti gli utenti. Un percorso tipico è C: \\ Documents and Impostazioni All Users Application \\ \\ Data.                                                                             |
| DESKTOP COMUNE              | DESKTOP COMUNE                  | Microsoft Windows Desktop per tutti gli utenti. Cartella virtuale che rappresenta la radice dello spazio dei nomi.                                                                                        |
| DOCUMENTI COMUNI            | COMMON%20DOCUMENTS              | Documenti per tutti gli utenti. Un percorso tipico è C: \\ Documents and Impostazioni All Users \\ \\ Documenti.                                                                                        |
| PROGRAMMI COMUNI             | COMMON%20PROGRAMS               | Gruppi di programmi comuni a tutti gli utenti. Un percorso tipico è C: \\ Documents and Impostazioni All Users Start Menu \\ \\ \\ Programs.                                                                     |
| MENU START COMUNE           | COMMON%20START%20MENU           | menu Start elementi comuni a tutti gli utenti. Un percorso tipico è C: \\ Documenti e Impostazioni Menu Start Tutti gli \\ \\ utenti.                                                                             |
| AVVIO COMUNE              | COMMON%20STARTUP                | Gruppo di programmi di avvio comune a tutti gli utenti.                                                                                                                                             |
| MODELLI COMUNI            | COMMON%20TEMPLATES              | Modelli di documento comuni a tutti gli utenti.                                                                                                                                                |
| COMMONMUSIC                 | MY%20MUSIC                      | I Musica di cartella comuni a tutti gli utenti.                                                                                                                                         |
| COMMONPICTURES              | MY%20PICTURES                   | Modelli di cartella Immagini comuni a tutti gli utenti.                                                                                                                                      |
| COMMONVIDEO                 | MY%20VIDEO                      | Modelli di cartella Video comuni a tutti gli utenti.                                                                                                                                         |
| CONNECTIONSFOLDER           | CONNECTIONSFOLDER               | cartella contenente i dati di connessione.                                                                                                                                                     |
| CARTELLA DEL PANNELLO DI CONTROLLO        | CONTROLPANELFOLDER              | Cartella virtuale contenente le icone per le Pannello di controllo applicazioni.                                                                                                                    |
| Biscotti                     | Biscotti                         | Directory del file system che funge da repository comune per i cookie Internet. Un percorso tipico è C: \\ Documenti e Impostazioni nome utente \\ \\ Cookie.                                        |
| DESKTOP                     | DESKTOP                         | Microsoft Windows Desktop. Cartella virtuale che rappresenta la radice dello spazio dei nomi.                                                                                                           |
| PREFERITI                   | PREFERITI                       | Directory del file system che funge da repository comune per gli elementi preferiti dell'utente. Un percorso tipico è C: \\ Documenti e Impostazioni \\ \\ preferiti.                             |
| Caratteri                       | Caratteri                           | Cartella virtuale contenente i tipi di carattere installati. Un percorso tipico è C: \\ Tipi di carattere \\ WINDOWS.                                                                                                       |
| CRONOLOGIA                     | CRONOLOGIA                         | Directory del file system che funge da repository comune per gli elementi della cronologia Internet.                                                                                                   |
| INTERNETFOLDER              | INTERNETFOLDER                  | Cartella che contiene dati Internet.                                                                                                                                                    |
| APPDATA LOCALE               | LOCAL%20APPDATA                 | Directory del file system che funge da repository di dati per applicazioni locali (non mobili). Un percorso tipico è C: \\ Documents and Impostazioni username Local Impostazioni Application \\ \\ \\ Data. |
| LOCALIZEDRESOURCEDIR        | LOCALIZEDRESOURCEDIR            | Directory delle risorse localizzate.                                                                                                                                                          |
| CARTELLA MYCOMPUTER            | CARTELLA MYCOMPUTER                | Risorse del computer. Cartella virtuale contenente tutti gli elementi nel computer locale: dispositivi di archiviazione, stampanti e Pannello di controllo. Questa cartella può contenere anche unità di rete mappate.             |
| MY MUSIC                    | MY%20MUSIC                      | Cartella Musica. Un percorso tipico è C: \\ Documents and Impostazioni username Documenti My \\ \\ \\ Musica.                                                                                       |
| IMMAGINI PERSONALI                 | MY%20PICTURES                   | Cartella Immagini. Un percorso tipico è C: \\ Documents e Impostazioni nome utente Documenti My \\ \\ \\ Pictures.                                                                                 |
| MY VIDEO                    | MY%20VIDEO                      | Cartella Video. Un percorso tipico è C: \\ Documenti e Impostazioni nome utente Documenti My \\ \\ \\ Video.                                                                                       |
| NETHOOD                     | NETHOOD                         | Cartella virtuale che rappresenta la radice della gerarchia dello spazio dei nomi di rete.                                                                                                               |
| CARTELLA RISORSE DI RETE       | NETWORKDPLACESFOLDER            | Una file system contenente gli oggetti collegamento che possono esistere nella cartella virtuale Risorse di rete. Non corrisponde a NETHOOD, che rappresenta la radice dello spazio dei nomi di rete.   |
| COLLEGAMENTI OEM                   | OEM%20LINKS                     | Cartella contenente i collegamenti ai siti OEM.                                                                                                                                                  |
| PERSONAL                    | PERSONAL                        | Directory del file system che funge da repository comune per i documenti di un utente. Un percorso tipico è C: \\ Documenti e Impostazioni nome utente \\ \\ Documenti.                                 |
| CARTELLA PRINTERS             | CARTELLA PRINTERS                 | Cartella virtuale contenente le stampanti installate.                                                                                                                                          |
| PRINTHOOD                   | PRINTHOOD                       | Directory del file system che contiene gli oggetti collegamento che possono esistere nella cartella virtuale Stampanti. Un percorso tipico è C: \\ Documenti e Impostazioni nome utente \\ \\ PrintHood.                 |
| PROGRAMMI                    | PROGRAMMI                        | Directory del file system che contiene i gruppi di programmi dell'utente ,che sono anche file system directory. Un percorso tipico è C: \\ Documenti e Impostazioni nome utente Programmi del menu \\ \\ \\ Start.  |
| PROFILE                     | PROFILE                         | Cartella del profilo dell'utente.                                                                                                                                                                 |
| FILE DI PROGRAMMA               | PROGRAM%20FILES                 | Cartella Programmi. Un percorso tipico è C: \\ Programmi.                                                                                                                             |
| PROGRAMMI COMUNI        | PROGRAMFILESCOMMON              | Cartella Programmi comune a tutti gli utenti.                                                                                                                                              |
| PROGRAMMI COMUNI x86    | PROGRAMFILESCOMMONX86           | Cartella Programmi comune a tutti gli utenti nei computer x86.                                                                                                                              |
| PROGRAM FILESx86            | PROGRAMFILESx86                 | Cartella Programmi nei computer x86.                                                                                                                                                  |
| Recente                      | Recente                          | Directory del file system che contiene i documenti usati più di recente dell'utente. Un percorso tipico è C: \\ Documenti e nome utente Impostazioni \\ \\ recenti.                                           |
| CARTELLA CESTINO          | RECYCLEBINFOLDER                | Cartella virtuale contenente gli oggetti nella cartella dell'Cestino.                                                                                                                       |
| RESOURCEDIR                 | RESOURCEDIR                     | Directory della risorsa.                                                                                                                                                                |
| Sendto                      | Sendto                          | Directory del file system che contiene le voci di menu Invia a. Un percorso tipico è C: \\ Documenti e Impostazioni nome utente \\ \\ SendTo.                                                                |
| START MENU                  | START%20MENU                    | Directory del file system contenente menu Start elementi. Un percorso tipico è C: \\ Documenti e nome utente Impostazioni menu \\ \\ Start.                                                                 |
| Avvio                     | Avvio                         | Directory del file system che corrisponde al gruppo di programmi di avvio dell'utente.                                                                                                            |
| SYSTEMx86                   | SYSTEMx86                       | Cartella di sistema nei computer x86.                                                                                                                                                         |
| TEMPLATES                   | TEMPLATES                       | Directory del file system che funge da repository comune per i modelli di documento.                                                                                                       |
| SYSTEM                      | SYSTEM                          | Cartella di sistema. Un percorso tipico è C: \\ Windows \\ System.                                                                                                                                  |
| WINDOWS                     | WINDOWS                         | Windows directory o SYSROOT.                                                                                                                                                          |



 

### <a name="argument-information"></a>Informazioni sugli argomenti



|                              | Valore                                   |
|------------------------------|-----------------------------------------|
| **Sistema operativo minimo** | Windows Vista con Service Pack 1 (SP1) |



 

 

 




---
description: L'argomento briciolo supporta le istruzioni complete AQS (Advanced Query Syntax) ed è particolarmente utile come mezzo per controllare l'ambito di una ricerca.
title: Argomento BRICIOLo (shell di Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f87a2b7-7f5a-4629-b881-44bf418b2df0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7d38fff38c14a6b537bde068b92e19cedf53d5d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980199"
---
# <a name="crumb-argument-the-windows-shell"></a>Argomento BRICIOLo (shell di Windows)

L' `crumb` argomento supporta le istruzioni complete AQS (Advanced Query Syntax) ed è particolarmente utile come mezzo per controllare l'ambito di una ricerca. Oltre alle istruzioni AQS, l' `crumb` argomento può assumere un parametro speciale `location` in Windows Vista e i `kind` `store` parametri e in Windows XP, come descritto più avanti in questo argomento.

In questo argomento sono incluse le sezioni seguenti:

-   [Sintassi briciola](#crumb-syntax)
    -   [Esempi generali](#general-examples)
-   [Uso di briciole con vista (percorso)](#using-crumb-with-vista-location)
    -   [Esempi di vista](#vista-examples)
    -   [Costanti per le cartelle comuni](#constants-for-common-folders)
    -   [Informazioni argomento](#argument-information)

## <a name="crumb-syntax"></a>Sintassi briciola

La sintassi della briciola è la seguente:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



La <column> parte è qualsiasi proprietà nel sistema di proprietà e il <value> parte è un valore valido per la proprietà. La <label> parte è un alias facoltativo per la proprietà visualizzata come hint dell'interfaccia utente.

### <a name="general-examples"></a>Esempi generali


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



## <a name="using-crumb-with-vista-location"></a>Uso di briciole con vista (percorso)

Nel parametro briciola, Windows Vista supporta AQS completi e anche la `location` proprietà, che dispone di un'implementazione speciale disponibile solo in Windows Vista. È possibile usare una stringa AQS o la `location` proprietà all'interno di un singolo parametro briciolo, ma non entrambi. Se il parametro briciolo include AQS, tutto il resto del parametro briciolo viene ignorato.

La `location` proprietà consente di specificare un percorso per la ricerca. Windows Vista può ignorare l'indicizzatore e attraversare la directory direttamente se il percorso è esterno all'ambito di ricerca per indicizzazione dell'indicizzatore. Di conseguenza, queste ricerche possono risultare più lente delle ricerche che usano l'indicizzatore.

Quando si specifica una `location` proprietà, sono supportati due parametri aggiuntivi e facoltativi:



| Parametro | Valori                  | Descrizione                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| inclusione | Includi, Escludi        | Specifica se la query deve includere o escludere elementi da tale percorso. Il valore predefinito è "include". Windows Vista non supporta le esclusioni senza inclusioni. (Vedere l'esempio) |
| ricorsione | ricorsivo, non ricorsivo | Specifica se la ricerca deve rimaledire tutte le sottocartelle a partire dal valore definito nel percorso:<value>. Il valore predefinito è "ricorsivo".                             |



 

Per definire l'ambito di una ricerca usando il protocollo **Search:** , sono disponibili diverse opzioni a seconda della destinazione dell'ambito.

Cartella in un computer locale:

-   Usare AQS (briciole = Folder: <percorso con codifica URL>)
-   Usare l'argomento location (briciole = location: <percorso con codifica URL>)

Cartella in un computer remoto/rete:

-   Usare l'argomento location (briciole = location: <percorso con codifica URL>)

Cartella a cui si accede tramite un gestore di protocollo Universal Naming Convention (UNC) noto:

-   Usare AQS (briciole = Store: <UNC protocol handler name> )
-   Usare l'argomento location (briciole = location: <percorso con codifica URL>)

### <a name="vista-examples"></a>Esempi di vista


```
search:query=vacation&crumb=location:shell%3aPersonal,include,recursive&
    
search:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 
    
search:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



Nel primo esempio viene eseguita una ricerca di "Vacation" a partire dalla `shell://Personal` posizione (un collegamento speciale alla cartella **documenti** dell'utente), inclusa la cartella e tutte le sottocartelle. Vedere la tabella seguente.

Nel secondo esempio viene eseguita una ricerca all'interno di C: \\ Immagini, ma non in c: \\ Immagini \\ duplicati.

Il terzo esempio esegue una ricerca all'interno di C: \\ Documents, limitato ai file con la `kind` proprietà impostata su pics.

### <a name="constants-for-common-folders"></a>Costanti per le cartelle comuni

Windows Vista consente l'utilizzo di valori CSIDL che forniscono un metodo univoco indipendente dal sistema per identificare le cartelle speciali utilizzate spesso dalle applicazioni, ma che potrebbero non avere lo stesso nome o percorso in un determinato sistema. Ad esempio, la cartella di sistema può essere "C: \\ Windows" in un sistema e "c: \\ WinNT" in un altro.

Usare questi percorsi con questa sintassi:


```
crumb=location:shell%3a<LocationName>&
```



Nella tabella seguente sono elencati i valori CSIDL. Per ulteriori informazioni, fare riferimento a [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .



| Nome                        | stringa di ricerca                   | Descrizione                                                                                                                                                                            |
|-----------------------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| STRUMENTI DI AMMINISTRAZIONE        | % 20TOOLS AMMINISTRATIVO          | Directory del file System che funge da repository per gli strumenti di amministrazione.                                                                                                            |
| APPDATA                     | APPDATA                         | Directory del file System che funge da repository comune per i dati specifici dell'applicazione. Un percorso tipico è C: \\ Documents and Settings \\ nomeutente \\ Application Data.                      |
| CACHE                       | CACHE                           | Directory del file System che funge da repository comune per i file temporanei di Internet. Un percorso tipico è C: \\ Documents and Settings \\ username \\ Temporary Internet Files.               |
| MASTERIZZAZIONE CD                  | CD% 20BURNING                    | Cartella contenente i dati da masterizzare su CD.                                                                                                                                             |
| STRUMENTI DI AMMINISTRAZIONE COMUNI | COMUNE% 20ADMINISTRATIVE% 20TOOLS | Strumenti di amministrazione per tutti gli utenti.                                                                                                                                                    |
| APPDATA COMUNE              | COMUNE% 20APPDATA                | Dati dell'applicazione per tutti gli utenti. Un percorso tipico è C: \\ Documents and Settings \\ All Users \\ Application Data.                                                                             |
| DESKTOP COMUNE              | DESKTOP COMUNE                  | Dati desktop di Microsoft Windows per tutti gli utenti. Cartella virtuale che rappresenta la radice dello spazio dei nomi.                                                                                        |
| DOCUMENTI COMUNI            | COMUNE% 20DOCUMENTS              | Documenti per tutti gli utenti. Un percorso tipico è C: \\ Documents and Settings \\ All Users \\ My Documents.                                                                                        |
| PROGRAMMI COMUNI             | COMUNE% 20PROGRAMS               | Gruppi di programmi comuni a tutti gli utenti. Un percorso tipico è C: \\ Documents and Settings \\ All Users \\ Start menu \\ Programs.                                                                     |
| MENU START COMUNE           | COMUNE% 20START% 20MENU           | Voci del menu Start comuni a tutti gli utenti. Un percorso tipico è C: \\ Documents and Settings \\ All Users \\ Start menu.                                                                             |
| AVVIO COMUNE              | COMUNE% 20STARTUP                | Gruppo di programmi di avvio comune a tutti gli utenti.                                                                                                                                             |
| MODELLI COMUNI            | COMUNE% 20TEMPLATES              | Modelli di documento comuni a tutti gli utenti.                                                                                                                                                |
| COMMONMUSIC                 | MY% 20MUSIC                      | Modelli di cartella musica comune a tutti gli utenti.                                                                                                                                         |
| COMMONPICTURES              | MY% 20PICTURES                   | Modelli di cartella immagini comuni a tutti gli utenti.                                                                                                                                      |
| COMMONVIDEO                 | MY %2 0 VIDEO                      | Modelli di cartella video comuni a tutti gli utenti.                                                                                                                                         |
| CONNECTIONSFOLDER           | CONNECTIONSFOLDER               | cartella contenente i dati di connessione.                                                                                                                                                     |
| CARTELLA PANNELLO DI CONTROLLO        | CONTROLPANELFOLDER              | Cartella virtuale contenente le icone per le applicazioni del pannello di controllo.                                                                                                                    |
| COOKIE                     | COOKIE                         | Directory del file System che funge da repository comune per i cookie di Internet. Un percorso tipico è C: \\ Documents and Settings \\ username \\ cookies.                                        |
| DESKTOP                     | DESKTOP                         | Microsoft Windows desktop. Cartella virtuale che rappresenta la radice dello spazio dei nomi.                                                                                                           |
| PREFERITI                   | PREFERITI                       | Directory del file System che funge da repository comune per gli elementi preferiti dell'utente. Un percorso tipico è C: \\ Documents and Settings \\ nomeutente \\ Preferiti.                             |
| FONT                       | FONT                           | Cartella virtuale che contiene i tipi di carattere installati. Un percorso tipico è C: \\ Windows \\ fonts.                                                                                                       |
| CRONOLOGIA                     | CRONOLOGIA                         | Directory del file System che funge da repository comune per gli elementi della cronologia Internet.                                                                                                   |
| INTERNETFOLDER              | INTERNETFOLDER                  | Cartella che contiene i dati Internet.                                                                                                                                                    |
| APPDATA LOCALE               | % 20APPDATA LOCALE                 | Directory del file System che funge da archivio dati per le applicazioni locali (non in roaming). Un percorso tipico è C: \\ Documents and Settings \\ nome utente \\ impostazioni locali \\ dati applicazione. |
| LOCALIZEDRESOURCEDIR        | LOCALIZEDRESOURCEDIR            | Directory delle risorse localizzata.                                                                                                                                                          |
| MYCOMPUTERFOLDER            | MYCOMPUTERFOLDER                | Risorse del computer. Cartella virtuale che contiene tutto il computer locale: dispositivi di archiviazione, stampanti e pannello di controllo. Questa cartella può inoltre contenere unità di rete mappate.             |
| MUSICA                    | MY% 20MUSIC                      | Cartella musica. Un percorso tipico è C: \\ Documents and Settings \\ username \\ My Documents \\ My Music.                                                                                       |
| IMMAGINI PERSONALI                 | MY% 20PICTURES                   | Cartella immagini. Un percorso tipico è C: \\ Documents and Settings \\ username \\ My Documents \\ My Pictures.                                                                                 |
| VIDEO                    | MY %2 0 VIDEO                      | Cartella video. Un percorso tipico è C: \\ Documents and Settings \\ username \\ My Documents \\ My video.                                                                                       |
| NETHOOD                     | NETHOOD                         | Cartella virtuale che rappresenta la radice della gerarchia dello spazio dei nomi di rete.                                                                                                               |
| CARTELLA POSIZIONI DI RETE       | NETWORKDPLACESFOLDER            | Una cartella file system contenente gli oggetti collegamento che possono esistere nella cartella virtuale risorse di rete. Non è uguale a NETHOOD, che rappresenta la radice dello spazio dei nomi di rete.   |
| COLLEGAMENTI OEM                   | OEM% 20LINKS                     | Cartella contenente i collegamenti ai siti OEM.                                                                                                                                                  |
| PERSONAL                    | PERSONAL                        | Directory del file System che funge da repository comune per i documenti di un utente. Un percorso tipico è C: \\ Documents and Settings \\ username \\ My Documents.                                 |
| CARTELLA STAMPANTI             | CARTELLA STAMPANTI                 | Cartella virtuale contenente le stampanti installate.                                                                                                                                          |
| PRINTHOOD                   | PRINTHOOD                       | Directory del file System che contiene gli oggetti collegamento che possono esistere nella cartella virtuale stampanti. Un percorso tipico è C: \\ Documents and Settings \\ nomeutente \\ PrintHood.                 |
| PROGRAMMI                    | PROGRAMMI                        | Directory del file System che contiene i gruppi di programmi dell'utente (che sono anche file system directory). Un percorso tipico è C: \\ Documents and Settings \\ nome utente \\ programmi menu Start \\ .  |
| PROFILE                     | PROFILE                         | Cartella del profilo dell'utente.                                                                                                                                                                 |
| FILE DI PROGRAMMA               | PROGRAMMA% 20FILES                 | Cartella programmi. Un percorso tipico è C: \\ Program Files.                                                                                                                             |
| FILE DI PROGRAMMA COMUNI        | PROGRAMFILESCOMMON              | Cartella programmi comune a tutti gli utenti.                                                                                                                                              |
| FILE di programma comuni x86    | PROGRAMFILESCOMMONX86           | Cartella programmi comune a tutti gli utenti di computer x86.                                                                                                                              |
| PROGRAMMA FILESx86            | PROGRAMFILESx86                 | Cartella programmi in computer x86.                                                                                                                                                  |
| RECENTE                      | RECENTE                          | Directory del file System che contiene i documenti utilizzati di recente dall'utente. Un percorso tipico è C: \\ Documents and Settings \\ nomeutente \\ recenti.                                           |
| CARTELLA CESTINO          | RECYCLEBINFOLDER                | Cartella virtuale contenente gli oggetti del cestino dell'utente.                                                                                                                       |
| RESOURCEDIR                 | RESOURCEDIR                     | Directory delle risorse.                                                                                                                                                                |
| SENDTO                      | SENDTO                          | Directory del file System che contiene le voci del menu Invia a. Un percorso tipico è C: \\ Documents and Settings \\ nomeutente \\ SendTo.                                                                |
| MENU START                  | INIZIO% 20MENU                    | Directory del file system contenente le voci del menu Start. Un percorso tipico è C: \\ Documents and Settings \\ nome utente \\ menu Start.                                                                 |
| AVVIO                     | AVVIO                         | Directory del file System che corrisponde al gruppo di programmi di avvio dell'utente.                                                                                                            |
| SYSTEMx86                   | SYSTEMx86                       | Cartella di sistema nei computer x86.                                                                                                                                                         |
| TEMPLATES                   | TEMPLATES                       | Directory del file System che funge da repository comune per i modelli di documento.                                                                                                       |
| SYSTEM                      | SYSTEM                          | Cartella di sistema. Un percorso tipico è C: \\ \\ sistema Windows.                                                                                                                                  |
| WINDOWS                     | WINDOWS                         | Directory di Windows o SYSROOT.                                                                                                                                                          |



 

### <a name="argument-information"></a>Informazioni argomento



|                          |                                         |
|--------------------------|-----------------------------------------|
| Sistema operativo minimo | Windows Vista con Service Pack 1 (SP1) |



 

 

 




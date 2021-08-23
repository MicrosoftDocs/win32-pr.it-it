---
title: Giochi con Least-Privileged account utente
description: Questo articolo descrive in che modo gli sviluppatori di giochi possono creare giochi Microsoft Windows che funzionano bene con gli account utente con privilegi minimi (noti anche come account utente limitati).
ms.assetid: 1b7cc3c9-b180-14b1-53c8-57f9e545d009
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 939d22b1d8bf381e98c5b6a7222be29b565c3d9e1f0758788aff94b0915b1807
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340741"
---
# <a name="gaming-with-least-privileged-user-accounts"></a>Giochi con Least-Privileged account utente

Questo articolo descrive in che modo gli sviluppatori di giochi possono creare giochi Microsoft Windows che funzionano bene con gli account utente con privilegi minimi (noti anche come account utente limitati).

-   [Introduzione](#introduction)
-   [Accesso ai file per Least-Privileged utente](#file-access-for-least-privileged-user-accounts)
    -   [Scenario 1: File che non devono essere visualizzati o modificati dagli utenti](#scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users)
    -   [Scenario 2: File che devono essere visualizzati o modificati dagli utenti](#scenario-2-files-that-need-to-be-viewed-or-altered-by-users)
-   [Accesso al Registro di sistema Least-Privileged account utente](#registry-access-for-least-privileged-user-accounts)
-   [Applicazione di patch con Least-Privileged utente](#patching-with-least-privileged-user-accounts)

## <a name="introduction"></a>Introduzione

Windows gestisce gli utenti con gli account. Attualmente, più dell'80% degli utenti di computer a casa condivide il computer con altri membri della famiglia. Quando più utenti condividono un computer Windows, vengono creati più account utente e ogni utente accede con un singolo account per accedere al computer. Con la crescente consapevolezza per la sicurezza, più persone gestiscono i computer con account utente con privilegi minimi, noti anche come account utente limitati, che non hanno il controllo completo sul sistema. Gli account amministratore hanno in genere accesso illimitato a ogni parte del computer. Questo può influire sul funzionamento Windows giochi basati su applicazioni.

Gli sviluppatori di giochi che scrivono giochi possono ottenere vantaggi aggiuntivi per lavorare con account utente con privilegi minimi. In Windows Vista e versioni successive vengono applicati account utente con privilegi minimi, il che significa che ogni account nel sistema, ad eccezione dell'amministratore locale, è un account utente con privilegi minimi. Ciò influirà sul modo in cui i giochi che non seguono le linee guida (applicazioni legacy) vengono eseguiti Windows Vista e versioni successive. Ad esempio, quando un'applicazione tenta di scrivere in una cartella o in un valore del Registro di sistema per cui non dispone dell'autorizzazione, la scrittura di file viene reindirizzata a un archivio file virtuale per l'utente. Questo archivio file virtuale risiederà in una cartella a cui l'utente ha accesso in scrittura. Questo comportamento potrebbe non sembrare irreversivo come l'esito negativo del tentativo di scrittura. Tuttavia, le applicazioni che creano file virtualizzati possono confondere gli utenti perché i file non verranno scritti nel percorso previsto dagli utenti. Ad esempio, i giochi che scrivono file con punteggio elevato nella stessa cartella della cartella eseguibile scriveranno questi file in una cartella virtualizzata. Di conseguenza, un utente non può visualizzare il punteggio elevato ottenuto da un altro utente perché ogni utente ha un archivio file virtualizzato separato.

I giochi che seguono le linee guida in questo articolo verranno eseguiti con account utente con privilegi minimi e, di conseguenza, manterranno la compatibilità con Windows Vista e versioni successive.

## <a name="file-access-for-least-privileged-user-accounts"></a>Accesso ai file per Least-Privileged account utente

Windows supporta due file system: FAT32 e NTFS. FAT32 è una versione legacy file system supportata solo per la compatibilità con le versioni precedenti. NTFS supporta autorizzazioni di file più potenti e affidabili. L'uso di NTFS è in espansione perché i rivenditori stanno spedendo nuovi computer con Windows preinstallati in un disco rigido partizionato NTFS. In un sistema XP Windows NTFS, gli utenti con account utente con privilegi minimi hanno solo accesso limitato a diverse cartelle. Tuttavia, avrebbero accesso completo in un sistema basato su FAT32 Windows XP.

La tabella seguente elenca il percorso predefinito di queste cartelle e le relative autorizzazioni.



| Percorso                                               | Contenuto della cartella              | Lettura | Scrittura | Creazione/Eliminazione |
|----------------------------------------------------|------------------------------|------|-------|---------------|
| <Drive>: \\ Windows                            | Il Windows operativo | X    |       |               |
| <Drive>: \\ Programmi                      | File eseguibili dell'applicazione | X    |       |               |
| <Drive>: \\ documenti e nome Impostazioni utente \\\* | File di ogni utente            | X    | X     | X             |
| <Drive>: \\ documenti e Impostazioni tutti gli \\ utenti  | Tutti i file utente               | X    | X     | X             |



 

\* Username è il nome di accesso dell'utente.

In un account utente con privilegi minimi è possibile leggere, scrivere, creare ed eliminare file in entrambe le cartelle: Documents and Impostazioni Username (Documenti e nome utente di Impostazioni), Documents (Documenti) e Impostazioni All Users (Tutti \\ \\ gli utenti).

Ciò significa che non è consigliabile salvare i giochi in Programmi, ma che devono essere posizionati in una \\ sottocartella in \\ Documenti. Inoltre, è consigliabile non inserire i dati temporanei dell'applicazione in Programmi o Documenti, ma devono essere inseriti nella cartella Dati applicazione \\ \\ (CSIDL \_ LOCAL \_ APPDATA).

In particolare, ogni gioco deve gestire due scenari:

### <a name="scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users"></a>Scenario 1: File che non devono essere visualizzati o modificati dagli utenti

Un esempio tipico è il file di configurazione del gioco, i file temporanei e i file della cache del gioco. Questi file vengono in genere mantenuti nella cartella Dati applicazione. Per ottenere il percorso di questa cartella, chiamare la funzione [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con CSIDL APPDATA o \_ CSIDL LOCAL APPDATA, come illustrato \_ \_ nell'esempio di codice seguente.

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

// Local Application Data
SHGetFolderPath( hWnd, CSIDL_LOCAL_APPDATA, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
// Roaming Application Data
SHGetFolderPath( hWnd, CSIDL_APPDATA, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

La differenza tra le cartelle dati dell'applicazione locali e mobili è che in Windows 2000 e Windows XP il contenuto mobile viene copiato da e verso il server durante il processo di accesso/disconnessione, mentre il contenuto locale non lo è. Per la maggior parte dei giochi, i dati dell'applicazione locale sono sufficienti.

### <a name="scenario-2-files-that-need-to-be-viewed-or-altered-by-users"></a>Scenario 2: File che devono essere visualizzati o modificati dagli utenti

Un esempio tipico è il salvataggio dei file di gioco di un utente. Archiviare i file nella cartella del documento dell'utente in modo che siano facilmente visibili all'utente. Un'applicazione ottiene il percorso della cartella del documento dell'utente chiamando [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con CSIDL PERSONAL, come illustrato \_ nell'esempio di codice seguente:

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

SHGetFolderPath( hWnd, CSIDL_PERSONAL, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

A volte, un gioco potrebbe dover archiviare file che tutti gli utenti devono visualizzare e usare. Un esempio è il record di punteggio elevato, in cui tutti gli utenti scrivono nello stesso file di record in modo che i punteggi alti siano mantenuti a livello di sistema anziché un punteggio elevato separato per ogni utente. Altri esempi sono mappe scaricate, missioni e modifiche del gioco. Se questi sono condivisi, solo un utente deve scaricarli invece di ogni utente. In questo scenario usare la cartella del documento nella cartella del profilo condiviso, come illustrato nel codice seguente.

``` syntax
#include <shlobj.h>
#include <strsafe.h>

#define APPNAME L"MyApp"

WCHAR wszPath[MAX_PATH];

SHGetFolderPath( hWnd, CSIDL_COMMON_DOCUMENTS, NULL, SHGFP_TYPE_CURRENT, wszPath );
StringCchCatW( wszPath, MAX_PATH, L"\\" );
StringCchCatW( wszPath, MAX_PATH, APPNAME );

// Create the folder wszPath
// Then create files in wszPath
```

## <a name="registry-access-for-least-privileged-user-accounts"></a>Accesso al Registro di sistema Least-Privileged account utente

È comune per le applicazioni usare il Registro di Windows per archiviare le informazioni. Analogamente all'accesso ai file, gli account amministratore e utente con privilegi minimi non hanno la stessa autorizzazione per il Registro di sistema. Per gli account utente con privilegi minimi, l'intero nodo HKEY \_ LOCAL MACHINE è di sola \_ lettura. Ad esempio, un gioco può leggere le informazioni di configurazione predefinite, ma potrebbe non scrivere nuove informazioni in questo nodo. Di conseguenza, i giochi in esecuzione in modalità utente con privilegi minimi che devono scrivere nel Registro di sistema dovranno usare il nodo HKEY CURRENT USER per archiviare le informazioni per utente, come illustrato nel codice \_ \_ seguente.

``` syntax
#define APP_REGISTRY_KEY_PATH L"Software\\MyCompany\\MyApp"

LONG lRetVal;
HKEY hKey;

lRetVal = RegCreateKeyExW( HKEY_CURRENT_USER,
                           APP_REGISTRY_KEY_PATH,
                           0,
                           NULL,
                           REG_OPTION_NON_VOLATILE,
                           KEY_WRITE|KEY_READ,
                           NULL,
                           &hKey,
                           NULL );

if( ERROR_SUCCESS == lRetVal )
{
    // Store information in hKey
}
```

Vale la pena notare che durante l'installazione le informazioni del Registro di sistema devono essere scritte in HKEY \_ LOCAL \_ MACHINE, non in HKEY \_ CURRENT \_ USER. Ciò è dovuto al fatto che la persona che esegue l'installazione è in genere un amministratore e potrebbe non essere l'unica persona a usare il programma. In questo caso, la scrittura in HKEY \_ CURRENT USER rende le informazioni non disponibili per gli altri \_ utenti. Questo non è in genere un problema perché le informazioni scritte nel Registro di sistema durante l'installazione sono le impostazioni di configurazione e predefinite che si applicano a ogni utente del programma.

Quando si disinstalla il gioco, è necessario un impegno aggiuntivo per rimuovere ogni valore che il gioco ha scritto nel registro. Poiché il programma di disinstallazione viene eseguito da una sola persona, in genere l'amministratore, la semplice eliminazione delle informazioni rilevanti in HKEY LOCAL MACHINE e HKEY CURRENT USER non rimuoverà i valori per \_ \_ gli altri \_ \_ utenti. Un modo per rimuovere le informazioni per utente nel Registro di sistema è enumerare la radice hive del Registro di sistema HKEY \_ USERS. Ogni sottochiave in HKEY \_ USERS corrisponde all'hive HKEY \_ CURRENT USER per un determinato utente nel \_ sistema. Enumerando HKEY USERS e rimuovendo le informazioni specifiche del gioco in ogni sottochiave, il programma di disinstallazione può garantire che nessuna informazione \_ sia stata lasciata indietro.

## <a name="patching-with-least-privileged-user-accounts"></a>Applicazione di patch con Least-Privileged utente

L'applicazione di patch a un gioco comporta l'aggiornamento dei file del gioco. Di conseguenza, in genere richiede l'accesso in scrittura alla cartella del programma del gioco. L'applicazione di patch a un gioco è un processo semplice quando viene eseguito da un amministratore perché ha accesso illimitato alla cartella del programma del gioco. Al contrario, è stato tradizionalmente difficile, se non impossibile, per un utente con privilegi minimi applicare patch ai giochi a causa della restrizione di accesso. A questo [Windows è](/windows/desktop/Msi/windows-installer-portal) stato migliorato il programma di installazione per rendere possibile l'applicazione di patch agli account utente con privilegi minimi. Per sfruttare i vantaggi di questa funzionalità, i giochi sono invitati a usare Windows programma di installazione per l'installazione e l'applicazione di patch.

A partire Windows Installer 3.0, le patch dell'applicazione possono essere applicate dagli utenti con privilegi minimi quando vengono soddisfatte determinate condizioni. Queste condizioni sono:

-   L'applicazione è stata installata Windows Installer 3.0.
-   L'applicazione è stata installata in origine per computer.
-   L'applicazione viene installata da supporti rimovibili, ad esempio CD-ROM o DVD (Digital Video Disc).
-   Le patch vengono firmate digitalmente da un certificato identificato dal pacchetto del programma di installazione originale (.msi file).
-   Le patch possono essere convalidate in base alla firma digitale.
-   Il pacchetto di installazione originale non ha disabilitato l'applicazione di patch all'account utente con privilegi minimi.
-   L'amministratore di sistema non ha disabilitato l'applicazione di patch all'account utente con privilegi minimi tramite criteri di sistema.

In genere, un utente con privilegi minimi non può modificare i file di programma di un gioco. Tuttavia, quando vengono soddisfatte le condizioni precedenti e l'applicazione di patch LUA è abilitata, il programma di installazione di Windows può aggiornare i file del gioco in modo che l'utente osegua la versione più recente.

> [!Note]  
> Le informazioni contenute in questo articolo riguardano il prodotto software non definitiva, che può essere modificato sostanzialmente prima della prima versione commerciale. Di conseguenza, le informazioni potrebbero non descrivere o riflettere in modo accurato il prodotto software al momento del primo rilascio in commercio. Questo articolo viene fornito solo a scopo informativo e Microsoft non fornisce alcuna garanzia, espressa o implicita, in relazione al presente articolo o alle informazioni in esso contenute.

 

 

 
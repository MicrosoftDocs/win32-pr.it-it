---
title: Giochi con account utente Least-Privileged
description: Questo articolo descrive in che modo gli sviluppatori di giochi possono creare giochi Microsoft Windows che funzionano bene con gli account utente con privilegi minimi (noti anche come account utente limitati).
ms.assetid: 1b7cc3c9-b180-14b1-53c8-57f9e545d009
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c44d94345462fc02ec649c5674ed88c38c12ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473670"
---
# <a name="gaming-with-least-privileged-user-accounts"></a>Giochi con account utente Least-Privileged

Questo articolo descrive in che modo gli sviluppatori di giochi possono creare giochi Microsoft Windows che funzionano bene con gli account utente con privilegi minimi (noti anche come account utente limitati).

-   [Introduzione](#introduction)
-   [Accesso ai file per gli account utente Least-Privileged](#file-access-for-least-privileged-user-accounts)
    -   [Scenario 1: file che non devono essere visualizzati o modificati dagli utenti](#scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users)
    -   [Scenario 2: file che devono essere visualizzati o modificati dagli utenti](#scenario-2-files-that-need-to-be-viewed-or-altered-by-users)
-   [Accesso al registro di sistema per gli account utente Least-Privileged](#registry-access-for-least-privileged-user-accounts)
-   [Applicazione di patch con account utente Least-Privileged](#patching-with-least-privileged-user-accounts)

## <a name="introduction"></a>Introduzione

Windows gestisce gli utenti con gli account. Attualmente, più del 80% degli utenti del computer a casa condivide il proprio computer con altri membri della famiglia. Quando più utenti condividono un computer Windows, vengono creati più account utente e ogni utente accede con un account singolo per accedere al computer. Con la maggiore consapevolezza per la sicurezza, un maggior numero di persone opera nei propri computer con account utente con privilegi minimi, noti anche come account utente limitati, che non hanno il controllo completo sul sistema. Gli account amministratore hanno in genere accesso illimitato a tutte le parti del computer. Questo può influire sul funzionamento di giochi basati su Windows.

Sono disponibili altri vantaggi per gli sviluppatori di giochi che scrivono i giochi per lavorare con gli account utente con privilegi minimi. In Windows Vista e versioni successive, vengono applicati gli account utente con privilegi minimi, il che significa che ogni account del sistema, ad eccezione dell'amministratore locale, è un account utente con privilegi minimi. Questo influirà sulla modalità di esecuzione dei giochi che non seguono le linee guida (applicazioni legacy) in Windows Vista e versioni successive. Ad esempio, quando un'applicazione tenta di scrivere in una cartella o in un valore del registro di sistema a cui non è autorizzato, il file di scrittura viene reindirizzato a un archivio di file virtuale per l'utente. Questo archivio file virtuale si trova in una cartella a cui l'utente ha accesso in scrittura. Questo comportamento potrebbe non sembrare irreversibile perché il tentativo di scrittura non riesce. Tuttavia, le applicazioni che creano file virtualizzati possono confondere gli utenti poiché i file non verranno scritti nel percorso previsto dagli utenti. Ad esempio, i giochi che scrivono file con punteggio elevato nella stessa cartella della cartella eseguibile scriveranno invece questi file in una cartella virtualizzata. Di conseguenza, un utente non è in grado di visualizzare il punteggio massimo ottenuto da un altro utente perché ogni utente dispone di un archivio file virtualizzato separato.

I giochi che seguono le linee guida in questo articolo vengono eseguiti con account utente con privilegi minimi e di conseguenza manterranno la compatibilità con Windows Vista e versioni successive.

## <a name="file-access-for-least-privileged-user-accounts"></a>Accesso ai file per gli account utente Least-Privileged

Windows supporta due file System: FAT32 e NTFS. FAT32 è un file system legacy supportato solo per la compatibilità con le versioni precedenti. NTFS supporta autorizzazioni file più potenti e affidabili. L'uso di NTFS si espande perché i rivenditori stanno spedendo nuovi computer con Windows preinstallato in un disco rigido partizionato NTFS. In un sistema Windows XP basato su NTFS, gli utenti con account utente con privilegi minimi hanno solo accesso limitato a diverse cartelle. Tuttavia, avranno accesso completo a un sistema Windows XP basato su FAT32.

La tabella seguente elenca il percorso predefinito di queste cartelle e le relative autorizzazioni.



| Percorso                                               | Contenuto della cartella              | Lettura | Scrittura | Creazione/Eliminazione |
|----------------------------------------------------|------------------------------|------|-------|---------------|
| <Drive>: \\ Windows                            | Sistema operativo Windows | X    |       |               |
| <Drive>: \\ File di programma                      | File dell'applicazione eseguibile | X    |       |               |
| <Drive>: \\ Documents and Settings \\ username\* | File di ogni utente            | X    | X     | X             |
| <Drive>: \\ Documents and Settings \\ All Users  | Tutti i file utente               | X    | X     | X             |



 

\* Username è il nome di accesso dell'utente.

In un account utente con privilegi minimi, è possibile leggere, scrivere, creare ed eliminare file in una cartella: Documents and Settings \\ username o Documents and Settings \\ All Users.

Ciò significa che non è consigliabile inserire i giochi Save nei \\ file di programma, bensì in una sottocartella dei \\ documenti. Inoltre, è consigliabile non inserire i dati temporanei dell'applicazione in \\ programmi o \\ documenti, ma devono essere posizionati nella cartella Application Data (CSIDL \_ Local \_ AppData).

In particolare, esistono due scenari che devono essere gestiti da ogni gioco:

### <a name="scenario-1-files-that-do-not-need-to-be-viewed-or-altered-by-users"></a>Scenario 1: file che non devono essere visualizzati o modificati dagli utenti

Un esempio tipico è il file di configurazione del gioco, i file temporanei e i file della cache di gioco. Questi file vengono in genere conservati nella cartella Application Data. Per ottenere il percorso di questa cartella, chiamare la funzione [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con CSIDL \_ AppData o CSIDL \_ Local \_ AppData come illustrato nell'esempio di codice seguente.

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

La differenza tra le cartelle di dati delle applicazioni locali e di roaming è che in Windows 2000 e Windows XP il contenuto mobile viene copiato da e verso il server durante il processo di accesso/disconnessione, mentre il contenuto locale non lo è. Per la maggior parte dei giochi, i dati dell'applicazione locale sono sufficienti.

### <a name="scenario-2-files-that-need-to-be-viewed-or-altered-by-users"></a>Scenario 2: file che devono essere visualizzati o modificati dagli utenti

Un esempio tipico è costituito dai file di gioco salvati dall'utente. Archiviare i file nella cartella documenti dell'utente in modo che siano facilmente visibili all'utente. Un'applicazione ottiene il percorso della cartella documenti dell'utente chiamando [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con CSIDL \_ Personal, come illustrato nell'esempio di codice seguente:

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

In alcuni casi, è possibile che un gioco debba archiviare i file che tutti gli utenti devono visualizzare e usare. Un esempio è il record con punteggio elevato, in cui tutti gli utenti scrivono nello stesso file di record in modo che i punteggi elevati vengano mantenuti a livello di sistema anziché un punteggio elevato separato per ogni utente. Altri esempi sono mappe scaricate, missioni e modifiche ai giochi. Se questi elementi sono condivisi, solo un utente deve scaricarli anziché ogni utente. In questo scenario, utilizzare la cartella documento sotto la cartella del profilo condiviso, come illustrato nel codice seguente.

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

## <a name="registry-access-for-least-privileged-user-accounts"></a>Accesso al registro di sistema per gli account utente Least-Privileged

Le applicazioni utilizzano il registro di sistema di Windows per archiviare le informazioni. Analogamente agli account di accesso ai file, l'amministratore e gli account utente con privilegi minimi non hanno le stesse autorizzazioni per il registro di sistema. Per gli account utente con privilegi minimi, l'intero \_ nodo del computer locale HKEY è di sola \_ lettura. Ad esempio, un gioco può leggere le informazioni di configurazione predefinite, ma non può scrivere nuove informazioni in questo nodo. Di conseguenza, i giochi in esecuzione in modalità utente con privilegi minimi che devono scrivere nel registro di sistema dovranno usare il \_ \_ nodo utente corrente di HKEY per archiviare le informazioni per utente, come illustrato nel codice seguente.

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

È importante notare che, durante l'installazione, le informazioni del registro di sistema devono essere scritte nel \_ computer locale HKEY \_ , non HKEY \_ \_ utente corrente. Questo perché la persona che esegue l'installazione è in genere un amministratore e potrebbe non essere l'unica persona a usare il programma. In questa situazione, la scrittura in \_ HKEY \_ l'utente corrente rende le informazioni non disponibili ad altri utenti. Non si tratta in genere di un problema perché le informazioni scritte nel registro di sistema durante l'installazione sono la configurazione e le impostazioni predefinite applicabili a ogni utente del programma.

Quando si disinstalla il gioco, è necessario ulteriore sforzo per rimuovere tutti i valori scritti dal gioco nel registro di sistema. Poiché il disinstallatore viene eseguito da una sola persona, in genere l'amministratore, è sufficiente eliminare le informazioni rilevanti nel \_ computer locale HKEY \_ e l' \_ utente corrente di HKEY \_ non rimuoverà i valori per altri utenti. Un modo per rimuovere le informazioni per utente nel registro di sistema consiste nell'enumerare la \_ radice hive del registro utenti HKEY. Ogni sottochiave in HKEY \_ Users corrisponde all' \_ hive dell'utente corrente di HKEY \_ per un determinato utente nel sistema. Tramite \_ l'enumerazione degli utenti di HKEY e la rimozione delle informazioni specifiche del gioco in ogni sottochiave, il disinstallatore può garantire che non venga lasciata alcuna informazione.

## <a name="patching-with-least-privileged-user-accounts"></a>Applicazione di patch con account utente Least-Privileged

L'applicazione di patch a un gioco comporta l'aggiornamento dei file del gioco. Pertanto, richiede in genere l'accesso in scrittura alla cartella del programma del gioco. L'applicazione di patch a un gioco è un processo semplice quando viene eseguita da un amministratore perché ha accesso illimitato alla cartella del programma del gioco. Viceversa, è stato tradizionalmente difficile, se non impossibile, per un utente con privilegi minimi di applicare patch ai giochi a causa della restrizione di accesso. A questo punto, [Windows Installer](/windows/desktop/Msi/windows-installer-portal) è stato migliorato per rendere possibile l'applicazione di patch per gli account utente con privilegi minimi. Per sfruttare i vantaggi di questa funzionalità, i giochi sono invitati a utilizzare Windows Installer per l'installazione e l'applicazione di patch.

A partire da Windows Installer 3,0, le patch dell'applicazione possono essere applicate da utenti con privilegi minimi quando vengono soddisfatte determinate condizioni. Queste condizioni sono:

-   L'applicazione è stata installata con Windows Installer 3,0.
-   L'applicazione è stata originariamente installata per computer.
-   L'applicazione viene installata da un supporto rimovibile, ad esempio un CD-ROM o un disco video digitale (DVD).
-   Le patch sono firmate digitalmente da un certificato identificato dal pacchetto originale del programma di installazione (file con estensione msi).
-   Le patch possono essere convalidate rispetto alla firma digitale.
-   Il pacchetto di installazione originale non ha disabilitato l'applicazione di patch per gli account utente con privilegi minimi.
-   L'amministratore di sistema non ha disabilitato l'applicazione di patch per l'account utente con privilegi minimi tramite criteri di sistema.

In genere, un utente con privilegi minimi non può modificare i file di programma di un gioco. Tuttavia, quando vengono soddisfatte le condizioni precedenti ed è abilitata l'applicazione di patch LUA, Windows Installer possibile aggiornare i file del gioco in modo che l'utente ottenga la versione più recente.

> [!Note]  
> Le informazioni contenute in questo articolo si riferiscono al prodotto software provvisorio, che può essere modificato in modo sostanziale prima della prima versione commerciale. Di conseguenza, è possibile che le informazioni non descrivano o riflettano in modo accurato il prodotto software alla prima pubblicazione in commercio. Questo articolo viene fornito esclusivamente a scopo informativo e Microsoft non rilascia alcuna garanzia, espressa o implicita, in relazione a questo articolo o alle informazioni contenute nel presente documento.

 

 

 
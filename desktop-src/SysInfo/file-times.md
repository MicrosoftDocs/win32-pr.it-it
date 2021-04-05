---
description: Un'ora di file è un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi trascorsi da 12:00 A.M. 1 gennaio 1601 Coordinated Universal Time (UTC). Il sistema registra i tempi di creazione, accesso e scrittura nei file delle applicazioni.
ms.assetid: 52d80b82-9ab0-4631-9e70-85df21da4946
title: Orari file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5919a2378e08798e4cd64d8f8357cb55692bd22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885838"
---
# <a name="file-times"></a>Orari file

Un' *ora di file* è un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi trascorsi da 12:00 A.M. 1 gennaio 1601 Coordinated Universal Time (UTC). Il sistema registra i tempi di creazione, accesso e scrittura nei file delle applicazioni.

Il file system NTFS archivia i valori di ora in formato UTC, quindi non sono interessati da modifiche nel fuso orario o nell'ora legale. Il file system FAT archivia i valori temporali in base all'ora locale del computer. Ad esempio, un file salvato alle 15:00 PST a Washington viene considerato come le 18.00 EST di New York in un volume NTFS, ma viene considerato come 3:00 EST di New York in un volume FAT.

I timestamp vengono aggiornati in diversi momenti e per vari motivi. L'unica garanzia relativa a un timestamp del file è che l'ora del file viene riflessa correttamente quando l'handle che apporta la modifica viene chiuso.

Non tutti i file System possono registrare i tempi di creazione e di ultimo accesso e non tutti i file System li registrano nello stesso modo. Ad esempio, la risoluzione del tempo di creazione in GRASSetto è di 10 millisecondi, mentre l'ora di scrittura ha una risoluzione di 2 secondi e l'ora di accesso ha una risoluzione di 1 giorno, quindi è effettivamente la data di accesso. Il file system NTFS ritarda gli aggiornamenti all'ora dell'ultimo accesso per un file fino a 1 ora dopo l'ultimo accesso.

Per recuperare le ore dei file per un file specificato, utilizzare la funzione [**GetFileTime ha provocato**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) . **GetFileTime ha provocato** copia le ore di creazione, dell'ultimo accesso e dell'ultima scrittura in singole strutture [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) . È anche possibile recuperare gli orari dei file usando le funzioni [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) e [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) . Queste funzioni copiano le ore dei file nelle strutture **FILETIME** in una struttura di [**\_ \_ dati Find Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) . Quando si scrive in un file, l'ora dell'ultima scrittura non viene aggiornata completamente fino a quando non vengono chiusi tutti gli handle utilizzati per la scrittura.

Per impostare le ore dei file per un file, usare la funzione [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime) . Questa funzione consente di modificare la creazione, l'ultimo accesso e l'ora dell'ultima scrittura senza modificare il contenuto del file. È possibile confrontare gli orari dei diversi file usando la funzione [**CompareFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-comparefiletime) . La funzione Confronta due ore di file e restituisce un valore che indica quale ora è successiva o restituisce 0 (zero) se gli orari sono uguali.

Se si prevede di modificare gli orari dei file per i file specificati, è possibile convertire una data e un'ora del giorno in un'ora del file usando la funzione [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) . È anche possibile ottenere l'ora di sistema in una struttura [**FILEtime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) chiamando la funzione [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) .

Per semplificare la visualizzazione di un file in un utente, utilizzare la funzione [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) . **FileTimeToSystemTime** converte l'ora del file e copia il mese, il giorno, l'anno e l'ora del giorno dall'ora del file in una struttura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) .

## <a name="file-times-and-daylight-saving-time"></a>Orari file e ora legale

È necessario prestare attenzione quando si usano i file quando l'utente ha impostato il sistema in modo da adattarsi automaticamente all'ora legale.

Per convertire un'ora del file nell'ora locale, usare la funzione [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime) . Tuttavia, **FileTimeToLocalFileTime** usa le impostazioni correnti per il fuso orario e l'ora legale. Se, pertanto, si tratta dell'ora legale, l'ora dell'ora legale viene rilasciata in considerazione, anche se il file che si sta convertendo è nell'ora solare.

Il file system FAT registra le ore sul disco nell'ora locale. [**GetFileTime ha provocato**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) recupera i tempi UTC memorizzati nella cache dal file system FAT. Quando diventa ora legale, l'ora recuperata da **GetFileTime ha provocato** è disattivata un'ora, perché la cache non viene aggiornata. Quando si riavvia il computer, l'ora memorizzata nella cache che **GetFileTime ha provocato** recupera è corretta. [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) recupera l'ora locale dal file system FAT e la converte in UTC usando le impostazioni correnti per il fuso orario e l'ora legale. Di conseguenza, se è l'ora legale, **FindFirstFile** prende in considerazione l'ora legale, anche se il file che si sta convertendo è nell'ora solare.

Il file system NTFS registra le ore su disco in formato UTC. Per tenere conto dell'ora legale durante la conversione di un'ora di file in un'ora locale, usare la sequenza di funzioni seguente invece di usare [**FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime):

-   [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)
-   [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)
-   [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)

## <a name="file-times-and-cdfs"></a>Orari file e CDFS

Gli indicatori di data e ora dei file che si trovano in o originano da supporti utilizzando Compact Disk File System (CDFS) vengono regolati per il fuso orario locale. ISO 9660 indica che CDFS è in grado di visualizzare correttamente le informazioni sulla data per il fuso orario locale. Questa operazione viene eseguita in modo che le date per i file in CDFS vengano visualizzate come quelle del formato UDF (Universal Disk Format). UDF è lo standard più recente per i supporti di distribuzione. Se il codice dipende dalle informazioni sulla data non modificate per un file che risiede o ha origine da supporti con CDFS, potrebbe non funzionare correttamente.

 

 

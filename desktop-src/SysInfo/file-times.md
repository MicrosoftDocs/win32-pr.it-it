---
description: Un tempo di file è un valore a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi trascorsi dalle 12:00. 1 gennaio 1601 Coordinated Universal Time (UTC). Il sistema registra gli orari dei file quando le applicazioni creano, accedono e scrivono nei file.
ms.assetid: 52d80b82-9ab0-4631-9e70-85df21da4946
title: Orari dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1492597b4e71775974ed8b19f6109c5900a8a28720b769c1c10dcf2f70166b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764493"
---
# <a name="file-times"></a>Orari dei file

Un *tempo di file* è un valore a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi trascorsi dalle 12:00. 1 gennaio 1601 Coordinated Universal Time (UTC). Il sistema registra gli orari dei file quando le applicazioni creano, accedono e scrivono nei file.

L'file system NTFS archivia i valori di ora in formato UTC, in modo che non siano interessati dalle modifiche apportate al fuso orario o all'ora legale. L'file system FAT archivia i valori di ora in base all'ora locale del computer. Ad esempio, un file salvato alle 15.00 PST di Washington viene visualizzato come EST delle 18.00 a New York in un volume NTFS, ma viene visualizzato come EST alle 15.00 a New York in un volume FAT.

I timestamp vengono aggiornati in momenti diversi e per vari motivi. L'unica garanzia su un timestamp del file è che l'ora del file venga riflessa correttamente quando l'handle che apporta la modifica viene chiuso.

Non tutti i file system possono registrare le ore di creazione e ultimo accesso e non tutti i file system li registrano nello stesso modo. Ad esempio, la risoluzione dell'ora di creazione in FAT è di 10 millisecondi, mentre l'ora di scrittura ha una risoluzione di 2 secondi e l'ora di accesso ha una risoluzione di 1 giorno, quindi è effettivamente la data di accesso. L'file system NTFS ritarda gli aggiornamenti all'ora dell'ultimo accesso per un file fino a 1 ora dopo l'ultimo accesso.

Per recuperare gli orari dei file per un file specificato, usare la [**funzione GetFileTime.**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) **GetFileTime** copia le ore di creazione, ultimo accesso e ultima scrittura nelle singole [**strutture FILETIME.**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) È anche possibile recuperare i tempi dei file usando [**le funzioni FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) [**e FindNextFile.**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) Queste funzioni copiano gli orari dei file in strutture **FILETIME** in una [**struttura \_ WIN32 FIND \_ DATA.**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) Quando si scrive in un file, l'ora dell'ultima scrittura non viene aggiornata completamente fino alla chiusura di tutti gli handle usati per la scrittura.

Per impostare gli orari dei file per un file, usare la [**funzione SetFileTime.**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime) Questa funzione consente di modificare le ore di creazione, ultimo accesso e ultima scrittura senza modificare il contenuto del file. È possibile confrontare gli orari di file diversi usando la [**funzione CompareFileTime.**](/windows/desktop/api/FileAPI/nf-fileapi-comparefiletime) La funzione confronta due volte il file e restituisce un valore che indica quale ora è successiva o restituisce 0 (zero) se gli orari sono uguali.

Se si prevede di modificare gli orari dei file per i file specificati, è possibile convertire una data e un'ora del giorno in un'ora del file usando la [**funzione SystemTimeToFileTime.**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) È anche possibile ottenere l'ora di sistema in una struttura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) chiamando la [**funzione GetSystemTimeAsFileTime.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime)

Per semplificare la visualizzazione dell'ora di un file a un utente, usare la [**funzione FileTimeToSystemTime.**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime) **FileTimeToSystemTime** converte l'ora del file e copia il mese, il giorno, l'anno e l'ora del giorno dall'ora del file a una [**struttura SYSTEMTIME.**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)

## <a name="file-times-and-daylight-saving-time"></a>Ora dei file e ora legale

È necessario fare attenzione quando si usano gli orari dei file se l'utente ha impostato il sistema per la regolazione automatica dell'ora legale.

Per convertire un'ora del file nell'ora locale, usare la [**funzione FileTimeToLocalFileTime.**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime) **FileTimeToLocalFileTime** usa tuttavia le impostazioni correnti per il fuso orario e l'ora legale. Pertanto, se si tratta dell'ora legale, l'ora legale viene prende in considerazione, anche se l'ora del file da convertire è nell'ora solare.

L'file system FAT registra gli orari su disco nell'ora locale. [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) recupera le ore UTC memorizzate nella cache dal file system. Quando diventa ora legale, l'ora recuperata da **GetFileTime** è disattivata di un'ora, perché la cache non viene aggiornata. Quando si riavvia il computer, l'ora memorizzata nella cache recuperata da **GetFileTime** è corretta. [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) recupera l'ora locale dal file system FAT e la converte nell'ora UTC usando le impostazioni correnti per il fuso orario e l'ora legale. Pertanto, se si tratta dell'ora legale, **FindFirstFile** prende in considerazione l'ora legale, anche se l'ora del file da convertire è nell'ora solare.

L'file system NTFS registra le ore su disco in formato UTC. Per conto dell'ora legale durante la conversione di un'ora del file in un'ora locale, usare la sequenza di funzioni seguente invece di [**usare FileTimeToLocalFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime):

-   [**FileTimeToSystemTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)
-   [**SystemTimeToTzSpecificLocalTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)
-   [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)

## <a name="file-times-and-cdfs"></a>Orari dei file e CDFS

I timestamp di data e ora dei file che si trovano o provengono da supporti tramite Compact Disc File System (CDFS) vengono modificati per il fuso orario locale. ISO 9660 indica che CDFS deve visualizzare correttamente le informazioni sulla data per il fuso orario locale. Questa operazione viene eseguita in modo che le date per i file in CDFS siano visualizzate come quelle in formato UDF (Universal Disk Format). La funzione definita dall'utente è lo standard più recente per i supporti di distribuzione. Se il codice dipende dalle informazioni sulla data non modificata per un file che risiede o ha origine da supporti tramite CDFS, potrebbe non funzionare correttamente.

 

 

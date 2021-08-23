---
title: Input e output su nastro
description: Esistono diverse funzioni che le applicazioni possono usare per eseguire input e output (I/O) in un'unità nastro. L'I/O su nastro è simile all'I/O eseguito in un dispositivo di comunicazione.
ms.assetid: 1862c267-0070-4fe8-bb77-40167913978a
keywords:
- Backup di input e output su nastro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281eb6104cb71fbd5e7f0b3d9072cefe562ac7b9cc54e05ede53bece8755178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021270"
---
# <a name="tape-input-and-output"></a>Input e output su nastro

Esistono diverse funzioni che le applicazioni possono usare per eseguire input e output (I/O) in un'unità nastro. L'I/O su nastro è simile all'I/O eseguito in un dispositivo di comunicazione.

Quando si eseguono operazioni di I/O su nastro, alcune unità nastro archiviano le informazioni sul firmware del nastro nei primi blocchi di un nastro, in genere usando una parte dei primi 100 blocchi. Le applicazioni non devono usare tali blocchi. Informazioni più specifiche su questo argomento sono disponibili dai singoli produttori di sistemi di nastri. In generale, un'applicazione che ignora i primi 100 blocchi su un nastro eviterà le idiosincrasie dell'unità nastro.

Le [**funzioni GetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition) [**e SetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition) recuperano e spostano la posizione corrente del nastro. La [**funzione WriteTapemark**](/windows/desktop/api/Winbase/nf-winbase-writetapemark) scrive un numero specificato di setmark, filemark, short filemarks e long filemarks. La [**funzione EraseTape**](/windows/desktop/api/Winbase/nf-winbase-erasetape) cancella tutto o parte di un nastro.

Le [**funzioni ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [**e WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) leggono e scrivono i dati dei file da e sul nastro. I dati vengono letti e scritti in blocchi completi. Se la dimensione del blocco del nastro è di 512 byte, tutte le operazioni di lettura e scrittura devono usare buffer semplici multipli interi delle dimensioni del blocco: 512, 1024, 1536, 2048 e così via. La maggior parte, se non tutte, le unità consentono un'operazione di scrittura solo dopo che il nastro è stato riavvato o dopo che un'operazione di lettura genera un messaggio di errore di fine dati.

Per leggere o scrivere dati di file da o verso un nastro in modalità blocco a lunghezza variabile, seguire questa procedura:

1.  Determinare se l'unità nastro supporta la modalità blocco a lunghezza variabile chiamando la [**funzione GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) e controllando il bit TAPE DRIVE VARIABLE BLOCK del membro FeaturesLow della struttura \_ TAPE GET DRIVE \_ \_ [**\_ \_ \_ PARAMETERS**](/windows/desktop/api/Winnt/ns-winnt-tape_get_drive_parameters) restituita. 
2.  Specificare la modalità di dimensione del blocco variabile chiamando la [**funzione SetTapeParameters,**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) impostando il membro **BlockSize** della struttura [**TAPE SET MEDIA \_ \_ \_ PARAMETERS**](/windows/desktop/api/Winnt/ns-winnt-tape_set_media_parameters) su zero. Usare quindi [**ReadFile o**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) per leggere o scrivere i dati del file.

Se [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) rileva un filemark, i dati fino al filemark vengono letti e la funzione ha esito negativo. La [**funzione GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un codice di errore che indica il tipo di filemark rilevato. Il sistema operativo sposta il nastro oltre il contrassegno file e un'applicazione può chiamare di nuovo **ReadFile** per continuare la lettura.

[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile leggono**](/windows/desktop/api/fileapi/nf-fileapi-writefile) e scrivono solo il flusso di dati. Le [**funzioni BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) e [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) leggono e scrivono tutti i flussi associati a un file. Questi includono dati, attributi estesi, sicurezza e flussi di dati alternativi. La sicurezza e i flussi di dati alternativi sono rilevanti solo nella partizione file system NTFS.

La [**funzione BackupSeek**](/windows/desktop/api/Winbase/nf-winbase-backupseek) cerca in avanti un file inizialmente accessibile da [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) o [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite). Questa funzione consente a un'applicazione di ignorare le informazioni che causano errori di accesso.

Se un'applicazione deve accedere solo ai dati del file, deve usare [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile). Queste funzioni possono anche leggere flussi di dati alternativi se i flussi sono stati creati usando la [**funzione CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

Un'applicazione di backup su nastro deve usare [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) e [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) per copiare tutte le informazioni relative a un file. Tuttavia, queste funzioni non leggono o scrivono caratteristiche del file, ad esempio attributi, ora di creazione del file e così via. Le applicazioni devono usare le funzioni di input e output del file, ad esempio [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) e [**SetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-setfileattributesa), per recuperare e impostare tali valori.

 

 
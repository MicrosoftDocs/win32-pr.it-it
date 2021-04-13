---
title: Input e output su nastro
description: Sono disponibili diverse funzioni che possono essere utilizzate dalle applicazioni per eseguire l'input e l'output (I/O) su un'unità nastro. Le operazioni di I/O su nastro sono simili a quelle eseguite su un dispositivo di comunicazione.
ms.assetid: 1862c267-0070-4fe8-bb77-40167913978a
keywords:
- Backup di input e output su nastro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5946659f1ad0246e37981201e4e08611b45b70b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338494"
---
# <a name="tape-input-and-output"></a>Input e output su nastro

Sono disponibili diverse funzioni che possono essere utilizzate dalle applicazioni per eseguire l'input e l'output (I/O) su un'unità nastro. Le operazioni di I/O su nastro sono simili a quelle eseguite su un dispositivo di comunicazione.

Quando si eseguono le operazioni di I/O su nastro, alcune unità nastro archiviano le informazioni del firmware del nastro nei primi blocchi su un nastro, in genere utilizzando una parte dei primi 100 blocchi. Le applicazioni non devono utilizzare tali blocchi. Informazioni più specifiche su questo argomento sono disponibili nei singoli produttori di sistemi a nastro. In generale, un'applicazione che ignora i primi 100 blocchi su un nastro eviterà le idiosincrasie dell'unità nastro.

Le funzioni [**GetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition) e [**SetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition) recuperano e spostano la posizione corrente del nastro. La funzione [**WriteTapemark**](/windows/desktop/api/Winbase/nf-winbase-writetapemark) scrive un numero specificato di segni di spunta, filemark, brevi filemark e filemarks lunghi. La funzione [**EraseTape**](/windows/desktop/api/Winbase/nf-winbase-erasetape) Cancella tutto o parte di un nastro.

Le funzioni [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) leggono e scrivono i dati dei file da e verso il nastro. I dati vengono letti e scritti in blocchi completi. Se le dimensioni del blocco del nastro sono pari a 512 byte, tutte le operazioni di lettura e scrittura devono usare i buffer che sono semplici multipli Integer della dimensione del blocco: 512, 1024, 1536, 2048 e così via. Nella maggior parte dei casi, le unità consentono solo un'operazione di scrittura dopo che il nastro viene riavvolto o dopo che un'operazione di lettura produce un messaggio di errore di fine dei dati.

Per leggere o scrivere dati di file in o da un nastro in modalità blocco a lunghezza variabile, seguire questa procedura:

1.  Determinare se l'unità nastro supporta la modalità a blocchi a lunghezza variabile chiamando la funzione [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) e controllando \_ il \_ \_ bit di blocco della variabile dell'unità nastro del membro **FeaturesLow** della struttura dei [**\_ \_ \_ parametri di unità del nastro**](/windows/desktop/api/Winnt/ns-winnt-tape_get_drive_parameters) restituito.
2.  Specificare la modalità dimensione blocco variabili chiamando la funzione [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) , impostando il membro **blockSize** della struttura [**dei \_ \_ \_ parametri del supporto del set di nastri**](/windows/desktop/api/Winnt/ns-winnt-tape_set_media_parameters) su zero. Quindi, usare [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) o [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) per leggere o scrivere i dati del file.

Se [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) rileva un filemark, i dati fino al filemark vengono letti e la funzione ha esito negativo. La funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un codice di errore che indica il tipo di filemark rilevato. Il sistema operativo sposta il nastro oltre il filemark e un'applicazione può chiamare nuovamente **ReadFile** per continuare a leggere.

[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) leggono e scrivono solo il flusso di dati. Le funzioni [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) e [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) leggono e scrivono tutti i flussi associati a un file. Sono inclusi dati, attributi estesi, sicurezza e flussi di dati alternativi. I flussi di dati di sicurezza e alternativi sono rilevanti solo per la partizione file system NTFS.

La funzione [**BackupSeek**](/windows/desktop/api/Winbase/nf-winbase-backupseek) Cerca in futuro in un file a cui si accede inizialmente da [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) o [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite). Questa funzione consente a un'applicazione di ignorare le informazioni che causano errori di accesso.

Se un'applicazione deve accedere solo ai dati dei file, deve usare [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile). Queste funzioni possono anche leggere flussi di dati alternativi se i flussi sono stati creati usando la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

Un'applicazione di backup su nastro deve usare [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) e [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) per copiare tutte le informazioni relative a un file. Tuttavia, queste funzioni non leggono o scrivono le caratteristiche dei file, ad esempio attributi, ora di creazione del file e così via. Le applicazioni devono usare le funzioni di input e output dei file, ad esempio [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) e [**SetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-setfileattributesa), per recuperare e impostare tali valori.

 

 
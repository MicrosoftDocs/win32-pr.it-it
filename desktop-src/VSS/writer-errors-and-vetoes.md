---
description: Un writer può non riuscire per diversi motivi programmatici.
ms.assetid: 50eced73-3917-4d7e-96cc-2d793b448738
title: Errori e veto del writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c24c15ad10766fc6ec395ed058ab3cb72a689d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226108"
---
# <a name="writer-errors-and-vetoes"></a>Errori e veto del writer

Un writer può non riuscire per diversi motivi programmatici. Quando si verifica questa situazione, è necessario porre il veto sull'operazione di backup, ripristino o copia shadow in corso chiamando il metodo [**CVssWriter:: SetWriterFailure**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure) in uno dei relativi metodi di gestione (ad esempio, [**CVssWriter:: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) o [**CVssWriter:: OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)) e restituendo **true**. Può anche impostare facoltativamente una stringa del messaggio di errore in risposta a una condizione di errore in determinati metodi del gestore con i metodi [**IVssComponentEx:: SetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setprepareforbackupfailuremsg), [**IVssComponentEx:: SetPostSnapshotFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setpostsnapshotfailuremsg), [**IVssComponent:: SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)e [**IVssComponent:: SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg) . Il richiedente può accettare il veto o continuare con il backup, ignorando il veto.

Un richiedente deve controllare lo stato del writer (usando [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)) dopo ogni evento generato.

In alcuni casi, è possibile recuperare i messaggi di errore da questi errori (usando i metodi [**IVssComponentEx:: GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg), [**IVssComponent:: GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg), [**IVssComponentEx:: GetPostSnapshotFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getpostsnapshotfailuremsg)e [**IVssComponent:: GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg) ) oppure un writer può scegliere di impostare i metadati (usando [**IVssComponent:: SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata) e [**IVssComponent:: SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) con informazioni sullo stato di errore). Per un esempio di codice in cui viene illustrato come visualizzare tali messaggi di errore, vedere [**IVssComponentEx:: GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg).

A seconda dello stato di errore, un richiedente o il relativo operatore può riavviare il backup e la copia shadow con qualsiasi modifica necessaria allo stato del processo o del sistema di backup.

Si supponga, ad esempio, che [**GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) abbia restituito quanto segue:

-   Servizio Copia **shadow \_ del volume E \_ WRITERERROR \_ INCONSISTENTSNAPSHOT** suggerisce che un richiedente potrebbe aggiungere volumi aggiuntivi alla copia shadow
-   Servizio Copia **shadow \_ del volume E \_ WRITERERROR \_** indica che il nuovo tentativo senza riconfigurazione potrebbe funzionare. Se il writer continua a restituire l'errore dopo diversi tentativi, provare a riavviare il servizio che ospita il writer. I writer seguenti sono ospitati nel servizio Copia Shadow del volume: writer del registro di sistema, writer del database di registrazione della classe COM+, writer di ottimizzazione della copia shadow e writer di ripristino automatico del sistema (ASR). Se il writer appartiene a un'applicazione che ospita il writer nel proprio processo, provare a riavviare l'applicazione.

    **Windows Server 2003 e Windows XP:** I writer seguenti sono ospitati nel servizio Copia Shadow del volume: writer del registro di sistema, writer del database di registrazione della classe COM+, writer del registro eventi dell'applicazione e Microsoft SQL Server writer di 2000 Desktop Engine (MSDE).

-   \_ \_ Lo stato VSS e writer \_ \_ non \_ disponibile indica che un writer potrebbe avere raggiunto il numero massimo di sessioni di backup e ripristino disponibili e il nuovo tentativo potrebbe funzionare quando il sistema è meno occupato.
-   Servizio Copia **shadow \_ del volume E \_ WRITERERROR \_ OUTOFRESOURCES** o **VSS \_ e \_ WRITERERROR \_ timeout** potrebbe suggerire la riduzione del carico di sistema prima di riprovare
-   Servizio Copia **shadow \_ del volume E \_ WRITERERROR \_ nonretryable** o **VSS \_ e \_ writer \_ non \_ risponde** probabilmente indicherebbe un errore del writer così grave da impedire il tentativo di eseguire il backup dei dati con VSS.

A seconda del writer e dei componenti che li generano, non è sempre necessario che un'applicazione di backup si interrompa dopo un errore o un veto.

Ad esempio, un richiedente può decidere che lo scopo della copia shadow è eseguire il backup dell'applicazione A e il veto è stato ricevuto dal writer per l'applicazione di backup B. In questo caso, è perfettamente accettabile continuare a eseguire il backup dell'applicazione A ignorando il veto.

Di seguito sono riportati alcuni esempi di veto del writer:

-   Il writer oppone il processo di creazione della copia shadow quando non è stato possibile sospendere le attività durante la creazione della copia shadow. Ciò indica una probabilità elevata che la copia shadow non è valida perché si è verificata un'operazione di scrittura durante lo stato di blocco.
-   Un'applicazione di backup ha richiesto una copia shadow solo del volume C: e un writer determina che una copia shadow di C: e D: deve eseguire il backup dei dati. In questo caso, il writer effettuerà il veto. L'applicazione di backup può esaminare i metadati e determinare se il writer verrà ignorato o se il processo di creazione della copia shadow verrà interrotto e riavviato in un secondo momento.

 

 




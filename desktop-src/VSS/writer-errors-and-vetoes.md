---
description: Un writer può non riuscire per numerosi motivi a livello di codice.
ms.assetid: 50eced73-3917-4d7e-96cc-2d793b448738
title: Errori e veti del writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0835775aec21da9aa69e81b4f7af63f98d765b5c72763cb52af706c4e7a720e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124461"
---
# <a name="writer-errors-and-vetoes"></a>Errori e veti del writer

Un writer può non riuscire per numerosi motivi a livello di codice. In questo caso, deve osare l'operazione di backup, ripristino o copia shadow in corso chiamando il metodo [**CVssWriter::SetWriterFailure**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure) in uno dei relativi metodi del gestore , ad esempio [**CVssWriter::OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) o [**CVssWriter::OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore), e restituisce **TRUE**. Facoltativamente, può anche impostare una stringa di messaggio di errore in risposta a una condizione di errore in determinati metodi del gestore con i metodi [**IVssComponentEx::SetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setprepareforbackupfailuremsg), [**IVssComponentEx::SetPostSnapshotFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setpostsnapshotfailuremsg), [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)e [**IVssComponent::SetPostRestoreFailureMsg.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg) Il richiedente può accettare il veto o continuare con il backup, ignorando il veto.

Un richiedente deve controllare lo stato del writer (usando [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)) dopo ogni evento generato.

In alcuni casi, I messaggi di errore possono essere recuperati da questi errori (usando [**IVssComponentEx::GetPrepareForBackupFailureMsg,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg) [**IVssComponent::GetPreRestoreFailureMsg,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg) [**IVssComponentEx::GetPostSnapshotFa**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getpostsnapshotfailuremsg)i metodi [**IVssComponent::GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg) o un writer può scegliere di impostare i metadati usando [**IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata) e [**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) con informazioni sullo stato di errore. Per codice di esempio che illustra come visualizzare tali messaggi di errore, vedere [**IVssComponentEx::GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg).

A seconda dello stato di errore, un richiedente o il relativo operatore potrebbe riavviare il backup e la copia shadow con qualsiasi modifica necessaria allo stato del processo o del sistema di backup.

Si supponga, ad esempio, [**che GetWriterStatus abbia**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) restituito quanto segue:

-   **VSS \_ E \_ WRITERERROR \_ INCONSISTENTSNAPSHOT** suggerisce che un richiedente potrebbe aggiungere altri volumi alla copia shadow
-   **VSS \_ E \_ WRITERERROR \_ RETRYABLE** indica che potrebbe funzionare un nuovo tentativo senza riconfigurazione. Se il writer continua a restituire l'errore dopo diversi tentativi, provare a riavviare il servizio che ospita il writer. I writer seguenti sono ospitati nel servizio VSS: writer del Registro di sistema, writer di database di registrazione della classe COM+, writer di ottimizzazione delle copie shadow e writer di Ripristino di sistema automatizzato (ASR). Se il writer appartiene a un'applicazione che ospita il writer nel proprio processo, provare a riavviare l'applicazione.

    **Windows Server 2003 e Windows XP:** I writer seguenti sono ospitati nel servizio VSS: writer del Registro di sistema, writer di database di registrazione della classe COM+, writer del log eventi dell'applicazione e writer di Microsoft SQL Server 2000 Desktop Engine (MSDE).

-   VSS E WRITER STATUS NOT AVAILABLE indica che un writer potrebbe aver raggiunto il numero massimo di sessioni di backup e ripristino disponibili e il nuovo tentativo potrebbe funzionare quando il sistema \_ \_ è meno \_ \_ \_ occupato.
-   **VSS \_ E \_ WRITERERROR \_ OUTOFRESOURCES** o **VSS \_ E \_ WRITERERROR \_ TIMEOUT** potrebbe suggerire una riduzione del carico di sistema prima di riprovare
-   **VSS \_ E \_ WRITERERROR \_ NONRETRYABLE** o **VSS \_ E WRITER \_ \_ NOT \_ RESPONDING** indicherà probabilmente un errore del writer così grave da precludere il tentativo di eseguire il backup dei dati con VSS.

A seconda del writer e dei componenti che li generano, non è sempre necessario che un'applicazione di backup si interrompi in seguito a un veto o a un errore.

Ad esempio, un richiedente può decidere che lo scopo della copia shadow è eseguire il backup dell'applicazione A e il veto è stato ricevuto dal writer per l'applicazione di backup B. In questo caso, è perfettamente accettabile continuare a eseguire il backup dell'applicazione A ignorando il veto.

Di seguito sono riportati esempi di veto di un writer:

-   Il writer ha il veto sul processo di creazione della copia shadow quando non è stato possibile sospendere le attività durante la creazione della copia shadow. Ciò indica che esiste una probabilità elevata che la copia shadow non sia valida perché si è verificata un'operazione di scrittura durante lo stato Freeze.
-   Un'applicazione di backup ha richiesto una copia shadow del solo volume C: e un writer determina che una copia shadow di C: e D: deve eseguire il backup dei dati. In questo caso, il writer avrà il veto. L'applicazione di backup può esaminare i metadati e determinare se il writer verrà ignorato o se il processo di creazione della copia shadow verrà interrotto e successivamente riavviato.

 

 




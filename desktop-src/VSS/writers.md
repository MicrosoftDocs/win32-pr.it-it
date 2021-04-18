---
description: I writer sono applicazioni o servizi che archiviano informazioni permanenti nei file su disco e che forniscono i nomi e i percorsi dei file ai richiedenti tramite l'interfaccia copia shadow.
ms.assetid: 24fc2d7c-f8d6-49ca-9bb5-0179bef68e78
title: Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ca409e8dc6153a6b3e2b747dc23cc391055471
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307116"
---
# <a name="writers"></a>Writer

I [*writer*](vssgloss-w.md) sono applicazioni o servizi che archiviano informazioni permanenti nei file su disco e che forniscono i nomi e i percorsi dei file ai richiedenti tramite l'interfaccia copia shadow.

Durante le operazioni di backup, i writer assicurano che i dati siano tranquilli e stabili, adatti per la copia shadow e il backup. I writer collaborano con i ripristini sbloccando i file quando possibile e indicando posizioni alternative quando necessario.

Se durante un'operazione di backup VSS non è presente alcun writer, è comunque possibile creare una copia shadow. In questo caso, tutti i dati nel volume copiato Shadow si troveranno nello [*stato coerente con l'arresto anomalo*](vssgloss-c.md)del sistema.

## <a name="writer-state"></a>Stato del writer

I writer mantengono il proprio stato in un oggetto di metadati basato su XML, il [*documento di metadati del writer*](vssgloss-w.md).

I metadati del writer sono l'unica struttura di dati che contiene il [*set di file*](vssgloss-f.md), ovvero percorso, specifica file e flag di ricorsione, dei dati di cui eseguire il backup e il ripristino.

Il documento dei metadati del writer organizza i set di file del writer in gruppi o [*componenti*](vssgloss-c.md). La relazione di uno di questi componenti durante le operazioni di backup e ripristino sugli altri componenti gestiti dal writer è descritta nel documento dei metadati del writer per la selezione del componente [*per il backup*](vssgloss-s.md), la relativa [*selezione per il ripristino*](vssgloss-s.md)e i [*percorsi logici*](vssgloss-l.md). Per ulteriori informazioni, vedere [configurazione dell'organizzazione dei componenti](definition-of-components-by-writers.md) e [utilizzo di percorsi di selezione e logica](working-with-selectability-and-logical-paths.md).

Questo documento contiene anche informazioni aggiuntive che controllano il ripristino dei file e altri problemi.

Per elaborare un backup o un ripristino, il richiedente deve disporre dei metadati del writer, insieme al documento relativo ai componenti di backup.

A differenza del documento componenti di backup, il documento di metadati del writer deve essere considerato come una struttura di sola lettura. Quando un writer lo crea, il documento non viene modificato.

## <a name="writer-event-handling"></a>Gestione degli eventi del writer

Le operazioni VSS di un writer vengono avviate tramite la ricezione di eventi COM.

Quando non sono presenti eventi, un writer non esegue operazioni VSS, ad esempio un backup o un ripristino VSS. Viene invece eseguita la normale attività, ad esempio la risposta alle query di database, la gestione dei dati utente o la fornitura di altri servizi.

Per assicurarsi che la gestione degli errori per più sessioni di backup e ripristino parallele venga eseguita correttamente e per garantire che una sessione di backup o ripristino non danneggi un altro, è necessario eseguire le operazioni seguenti:

-   Se il gestore eventi di un writer, ad esempio [**CVssWriter:: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze), chiama il metodo [**CVssWriterEx2:: GetSessionID**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-getsessionid), [**CVssWriter:: SetWriterFailure**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure)o [**CVssWriterEx2:: SetWriterFailureEx**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-setwriterfailureex) , il gestore eventi deve chiamare il metodo nello stesso thread che ha chiamato il gestore eventi.
-   Se lo si desidera, l'implementazione del writer di un gestore eventi, ad esempio [**onFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) , può eseguire l'offload del lavoro nei thread di lavoro, purché ogni thread di lavoro esegue il marshalling di tutte le segnalazioni di errori necessarie al thread del gestore eventi originale.

## <a name="handling-identify-events"></a>Gestione degli eventi di identificazione

Fatta eccezione per l'evento di identificazione, il tipo e l'ordine degli eventi ricevuti da un writer dipendono in modo univoco dal tipo di operazioni VSS attualmente in corso.

L'evento di identificazione richiede che i writer forniscano le informazioni di sistema sulla configurazione e i file gestiti tramite il [*documento di metadati del writer*](vssgloss-w.md). Viene generato un evento di identificazione per supportare quasi tutte le operazioni VSS, incluse le query di sistema, nonché le operazioni di copia shadow e backup e ripristino. Pertanto, l'implementazione di qualsiasi writer del gestore eventi di identificazione [**CVssWriter:: Onidentificate**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) deve essere in grado di gestire un evento di identificazione in qualsiasi momento, incluso durante l'elaborazione di un'altra operazione VSS, ad esempio un backup o un ripristino. Un evento di identificazione non dovrebbe mai essere considerato come parte del ciclo di vita di un'operazione VSS, anche se la generazione potrebbe essere prevista e obbligatoria prima dell'avvio dell'operazione.

È particolarmente importante che le informazioni sullo stato relative a un'operazione VSS non vengano modificate in [**CVssWriter:: onidentifi**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), perché la ricezione di un evento non ordinato comporta la reimpostazione delle informazioni.

## <a name="backup-and-restore-events"></a>Eventi di backup e ripristino

A seconda che si tratti di un backup o di un ripristino, un writer riceverà tra due e sette eventi, oltre a un evento di identificazione iniziale.

La gestione di questi eventi costituisce, dal punto di vista di un writer, il ciclo di vita di un'operazione di backup o ripristino.

In una tipica operazione di backup (vedere [Cenni preliminari sull'elaborazione di un backup in VSS](overview-of-processing-a-backup-under-vss.md)), un writer gestirà gli eventi seguenti (oltre a un evento di identificazione iniziale):

-   PrepareForBackup
-   PrepareForSnapshot
-   Freeze
-   Sblocca
-   PostSnapshot
-   BackupComplete
-   BackupShutdown

In un'operazione di ripristino tipica (vedere [Cenni preliminari sull'elaborazione di un ripristino in VSS](overview-of-processing-a-restore-under-vss.md)), un writer gestirà gli eventi seguenti:

-   PreRestore
-   PostRestore

 

 




---
description: La partecipazione del writer in un backup VSS è progettata per consentire alle applicazioni di controllare cosa e come devono essere utilizzati i dati di ripristino.
ms.assetid: 076b2e6f-c2ca-4129-8827-1b18a655d634
title: Ripristini senza partecipazione del writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89fd5ea855d2d91701d351e860bf966148be587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131263"
---
# <a name="restores-without-writer-participation"></a>Ripristini senza partecipazione del writer

La partecipazione del writer in un backup VSS è progettata per consentire alle applicazioni di controllare cosa e come devono essere utilizzati i dati di ripristino.

In generale, se un writer è disponibile in un sistema, non è mai consigliabile ripristinare i dati nel percorso originale senza partecipazione del writer. È probabile che un ripristino di questo tipo riscontri file di destinazione bloccati ed esegua un rischio significativo di danneggiamento dei dati.

Tuttavia, esistono motivi per cui è possibile che un'applicazione di backup desideri o debba ripristinare un backup VSS senza partecipazione del writer:

-   I dati sono gestiti da applicazioni non compatibili con VSS. In quasi tutti i sistemi saranno presenti alcune applicazioni, ovvero editor di testo, lettori di posta elettronica, elaboratori di testo e così via, che non sono in grado di ignorare VSS. Non è possibile ripristinare questi dati utilizzando la partecipazione del writer.

    In genere, questo tipo di dati non è critico per il sistema o per il servizio e il ripristino non dovrebbe essere problematico o almeno non più problematico rispetto a un ripristino convenzionale.

    Come con i preparativi per i ripristini convenzionali, se possibile, gli operatori di ripristino devono tentare di sospendere o terminare tali applicazioni prima di avviare un ripristino VSS.

-   Writer VSS mancanti. Questa situazione può essere abbastanza comune durante il ripristino dello stato di un sistema danneggiato. Un'operazione di backup deve determinare se è opportuno ripristinare i file per i writer mancanti. Se è consigliabile eseguire il ripristino, è possibile ripristinare i file proprio come un backup convenzionale.
-   Ripristino privato dei dati di un writer. Un richiedente può scegliere di ripristinare i dati di un writer in esecuzione in una posizione privata senza notificare il writer. Un esempio potrebbe essere il ripristino dei dati del writer per supportare il confronto offline. In questo tipo di situazione, un richiedente non desidera utilizzare la [*nuova posizione di destinazione*](vssgloss-n.md) durante il ripristino, perché non desidera che il writer acceda ai dati.
-   Non è necessario che un writer venga associato durante il ripristino. Un writer indica questa operazione passando in VSS \_ WRE \_ Never per il parametro *writerRestore* di [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod).
-   Un writer richiede un metodo di ripristino personalizzato. Un writer indica che è necessario un ripristino personalizzato passando in VSS \_ RME \_ Custom per il parametro *Method* di [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod). In questo caso, il writer non deve essere utilizzato nel processo di ripristino, a meno che la documentazione per il ripristino personalizzato per quel writer non indichi diversamente.

Un richiedente implica un writer nel processo di ripristino specificando uno dei componenti di tale writer in una chiamata a [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore). È possibile ripristinare i dati di un writer senza coinvolgere il writer semplicemente non specificando alcun componente di tale writer in una chiamata a **IVssBackupComponents:: SetSelectedForRestore**. Se un writer non prevede alcun evento di ripristino, che implica che il writer nel processo di ripristino può causare la segnalazione di errori non corretti per quel writer.

 

 




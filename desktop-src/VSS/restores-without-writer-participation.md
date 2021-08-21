---
description: La partecipazione del writer a un backup vss è progettata per consentire alle applicazioni di controllare cosa e come devono essere usati i dati di ripristino.
ms.assetid: 076b2e6f-c2ca-4129-8827-1b18a655d634
title: Ripristini senza partecipazione al writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896cbe81a2c3487bb00b01379b6b5bbe4760ecbb28c1bf94c661eeb0049a3d37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056369"
---
# <a name="restores-without-writer-participation"></a>Ripristini senza partecipazione al writer

La partecipazione del writer a un backup vss è progettata per consentire alle applicazioni di controllare cosa e come devono essere usati i dati di ripristino.

In generale, se un writer è disponibile in un sistema, non è mai consigliabile ripristinare i dati nella posizione originale senza la partecipazione del writer. Un ripristino di questo tipo potrebbe riscontrare file di destinazione bloccati ed è a rischio significativo di danneggiare i dati.

Esistono tuttavia motivi per cui un'applicazione di backup potrebbe voler o dover ripristinare un backup vss senza la partecipazione al writer:

-   I dati vengono gestiti da applicazioni non inconsapevoli del Servizio Copia Microsoft. Quasi tutti i sistemi avranno alcune applicazioni, ad esempio editor di testo, lettori di posta elettronica, elaboratori di testo e così via, che non sono a conoscenza del Servizio Copia Desktop remoto. Questi dati non possono essere ripristinati usando la partecipazione del writer.

    In genere, questo tipo di dati non è critico per il sistema o il servizio e il ripristino non dovrebbe essere problematico o almeno non più problematico rispetto a un ripristino convenzionale.

    Come per i preparativi per i ripristini convenzionali, se possibile, gli operatori di ripristino devono tentare di sospendere o terminare tali applicazioni prima di avviare un ripristino vss.

-   VsS writer mancanti. Questa situazione può essere piuttosto comune quando si ripristina lo stato di un sistema danneggiato. Un'operazione di backup deve determinare se è consigliabile ripristinare i file per i writer mancanti. Se il ripristino è auspicabile, i file possono essere ripristinati esattamente come un backup convenzionale.
-   Ripristino privato dei dati di un writer. Un richiedente può scegliere di ripristinare i dati di un writer in esecuzione in una posizione privata senza notificare il writer. Un esempio potrebbe essere il ripristino dei dati del writer per supportare il confronto offline. In questo tipo di situazione, un richiedente [](vssgloss-n.md) non vuole usare il nuovo percorso di destinazione durante l'esecuzione del ripristino, perché non vuole che il writer accedono ai dati.
-   Un writer non deve essere coinvolto durante il ripristino. Un writer indica questa operazione passando VSS WRE NEVER per il \_ \_ parametro *writerRestore* di [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod).
-   Un writer richiede un metodo di ripristino personalizzato. Un writer indica che è necessario un ripristino personalizzato passando VSS RME CUSTOM per il parametro del metodo \_ \_ di [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod).  In questo caso, questo writer non deve essere coinvolto nel processo di ripristino, a meno che la documentazione di ripristino personalizzata per tale writer non indichi diversamente.

Un richiedente coinvolge un writer nel processo di ripristino specificando uno dei componenti del writer in una chiamata a [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore). I dati di un writer possono essere ripristinati senza coinvolgere il writer semplicemente non specificando alcun componente del writer in una chiamata a **IVssBackupComponents::SetSelectedForRestore**. Se un writer non prevede alcun evento di ripristino, il suo coinvolgimento nel processo di ripristino può causare la presenza di errori non eserciti per tale writer.

 

 




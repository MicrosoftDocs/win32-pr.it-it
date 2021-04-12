---
description: La configurazione delle operazioni di ripristino inizia effettivamente durante il backup dei dati, quando i writer specificano nei documenti dei metadati del writer la modalità di ripristino dei dati.
ms.assetid: b1f948cd-d3b0-4637-b76d-b54a74bb5948
title: Impostazione di metodi di ripristino VSS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412cb699fb791a973e280f63fec03bd2854ccd1d
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104234415"
---
# <a name="setting-vss-restore-methods"></a>Impostazione di metodi di ripristino VSS

La configurazione delle operazioni di ripristino inizia effettivamente durante il backup dei dati, quando i writer specificano nei documenti dei metadati del writer la modalità di ripristino dei dati.

Queste specifiche, definite come metodi di [*ripristino*](vssgloss-r.md) o destinazioni di [*ripristino*](vssgloss-r.md)originali, possono essere modificate durante il ripristino da parte di writer che impostano nuove destinazioni di ripristino o da richiedenti che si ripristinano in nuovi percorsi (vedere [percorsi di backup e ripristino non predefiniti](non-default-backup-and-restore-locations.md)).

Chiamando [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod), un writer indica il metodo di ripristino da utilizzare nel documento di metadati del writer. Il metodo Restore è impostato su Wide writer e applicato a tutti i file in tutti i componenti gestiti da un writer.

Un richiedente ottiene (e deve rispettare) queste informazioni chiamando [**IVssExamineWriterMetadata:: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

Il metodo Restore è definito da un'enumerazione [**\_ RESTOREMETHOD \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) di enumerazione VSS, che viene passata a [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) e restituita da [**IVssExamineWriterMetadata:: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

Il documento dei metadati del writer supporta i seguenti metodi di ripristino validi (un metodo di ripristino di VSS \_ RME non \_ definito indica un errore del writer). Le figure riepilogano il modo in cui devono essere implementati i vari metodi di ripristino supportati e definiti (il servizio Copia Shadow del volume \_ RME \_ personalizzato non è associato a una figura, perché per definizione è specifico del writer e deve seguire le API e la documentazione specifiche del writer):

-   \_ripristino RME \_ VSS \_ se \_ non è \_ presente. Ripristinare i file del componente su disco se nessuno dei file è già presente sul disco. Lo stato del file di destinazione deve essere controllato dopo un evento di [**preripristino**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) .
    ![Diagramma che mostra un albero per la risoluzione dei problemi per VSS_RME_RESTORE_IF_NOT_THERE.](images/rint.png)
-   \_ripristino RME VSS se è in \_ grado di \_ \_ \_ sostituire. Ripristinare i file su disco se tutti i file possono essere sostituiti. Lo stato del file di destinazione deve essere controllato dopo un evento di [**preripristino**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) .
    ![Diagramma che mostra un albero per la risoluzione dei problemi per VSS_RME_RESTORE_IF_CAN_REPLACE.](images/ricr.png)
-   avvio dell'arresto del ripristino di VSS \_ RME \_ \_ \_ . Un servizio verrà arrestato prima di ripristinare i file.
    ![Diagramma che mostra un albero per la risoluzione dei problemi per VSS_RME_STOP_RESTORE_START.](images/srr.png)
-   \_ripristino RME \_ VSS \_ in \_ un \_ percorso alternativo. Ripristinare i file su disco in un percorso alternativo. I mapping dei percorsi alternativi vengono specificati nel documento di metadati del writer.
    ![Diagramma che mostra un albero per la risoluzione dei problemi per VSS_RME_RESTORE_TO_ALTERNATE_LOCATION.](images/rtal.png)
-   \_ripristino RME \_ VSS \_ al \_ riavvio. Quando il computer viene riavviato, i file possono essere ripristinati (sovrascritti).
    ![Diagramma che mostra un albero per la risoluzione dei problemi per VSS_RME_RESTORE_AT_REBOOT.](images/rar.png)
-   \_ripristino RME \_ VSS \_ al \_ riavvio \_ se \_ non è in grado di \_ sostituire. Se non è stato possibile ripristinare un file su disco in un sistema in esecuzione, questo viene ripristinato (sovrascritto) al riavvio del computer.
    ![Diagramma che mostra un forVSS_RME_RESTORE_AT_REBOOT_IF_CANNOT_REPLACE dell'albero per la risoluzione dei problemi. ](images/raricr.png)
-   VSS \_ RME \_ personalizzato. Nessuno dei metodi predefiniti funzionerà; per eseguire l'operazione di ripristino, è necessario che l'applicazione di backup utilizzi API specializzate. Per questo metodo di backup, il richiedente deve comprendere completamente il writer in questione. Vedere [casi di utilizzo VSS speciali](special-vss-usage-cases.md) per le istanze attualmente supportate.

 

 




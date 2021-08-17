---
description: La configurazione delle operazioni di ripristino inizia effettivamente durante il backup dei dati, quando i writer specificano nei documenti dei metadati del writer come devono essere ripristinati i dati.
ms.assetid: b1f948cd-d3b0-4637-b76d-b54a74bb5948
title: Impostazione dei metodi di ripristino vss
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f7b0d138555b1e10dba55483c694c08a649e97e59cb66ed65c1a276187d3c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751727"
---
# <a name="setting-vss-restore-methods"></a>Impostazione dei metodi di ripristino vss

La configurazione delle operazioni di ripristino inizia effettivamente durante il backup dei dati, quando i writer specificano nei documenti dei metadati del writer come devono essere ripristinati i dati.

Queste specifiche, denominate metodi [](vssgloss-r.md) di ripristino o destinazioni di ripristino [*originali,*](vssgloss-r.md)possono essere modificate durante il ripristino dai writer che impostano nuove destinazioni di ripristino o dai richiedenti che esere ripristinino in nuovi percorsi (vedere Percorsi di [backup](non-default-backup-and-restore-locations.md)e ripristino non predefiniti).

Chiamando [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod), un writer indica quale metodo di ripristino deve essere usato nel documento di metadati del writer. Il metodo restore viene impostato a livello di writer e applicato a tutti i file in tutti i componenti gestiti da un writer.

Un richiedente ottiene (e deve rispettare) queste informazioni chiamando [**IVssExamineWriterMetadata::GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

Il metodo restore è definito da un'enumerazione [**VSS \_ RESTOREMETHOD \_ ENUM,**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) che viene passata a [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) e restituita da [**IVssExamineWriterMetadata::GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

Il documento di metadati del writer supporta i metodi di ripristino validi seguenti. Un metodo di ripristino di VSS \_ RME \_ UNDEFINED indica un errore del writer. Le figure riepilogano come devono essere implementati i vari metodi di ripristino supportati e definiti (VSS RME CUSTOM non ha alcuna figura associata, perché per definizione è specifico del writer e deve seguire le API e la documentazione specifiche del \_ \_ writer):

-   RIPRISTINO \_ DI VSS RME \_ SE NON È \_ \_ \_ PRESENTE. Ripristinare i file dei componenti su disco se nessuno dei file è già presente sul disco. Lo stato del file di destinazione deve essere controllato dopo [**un evento PreRestore.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
    ![Diagramma che mostra un albero di risoluzione dei problemi per VSS_RME_RESTORE_IF_NOT_THERE.](images/rint.png)
-   RIPRISTINO \_ RME VSS \_ \_ SE PUÒ \_ \_ SOSTITUIRE. Ripristinare i file su disco se tutti i file possono essere sostituiti. Lo stato del file di destinazione deve essere controllato dopo [**un evento PreRestore.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
    ![Diagramma che mostra un albero di risoluzione dei problemi per VSS_RME_RESTORE_IF_CAN_REPLACE.](images/ricr.png)
-   VSS RME STOP RESTORE START ( ARRESTO RIPRISTINO VSS \_ RME \_ \_ \_ START). Un servizio verrà arrestato prima del ripristino dei file.
    ![Diagramma che mostra un albero di risoluzione dei problemi per VSS_RME_STOP_RESTORE_START.](images/srr.png)
-   RIPRISTINO \_ DI VSS RME \_ IN UN PERCORSO \_ \_ \_ ALTERNATIVO. Ripristinare i file su disco in un percorso alternativo. I mapping dei percorsi alternativi vengono specificati nel documento di metadati del writer.
    ![Diagramma che mostra un albero di risoluzione dei problemi per VSS_RME_RESTORE_TO_ALTERNATE_LOCATION.](images/rtal.png)
-   RIPRISTINO DI \_ VSS RME \_ AL \_ \_ RIAVVIO. Fare in modo che i file siano ripristinati (sovrascritti) al riavvio del computer.
    ![Diagramma che mostra un albero di risoluzione dei problemi per VSS_RME_RESTORE_AT_REBOOT.](images/rar.png)
-   RIPRISTINO DI \_ VSS RME \_ AL \_ \_ RIAVVIO \_ SE NON È \_ POSSIBILE \_ SOSTITUIRE. Se non è stato possibile ripristinare un file su disco in un sistema in esecuzione, viene ripristinato (sovrascritto) al riavvio del computer.
    ![Diagramma che mostra un albero di risoluzione dei problemi forVSS_RME_RESTORE_AT_REBOOT_IF_CANNOT_REPLACE. ](images/raricr.png)
-   VSS \_ RME \_ CUSTOM. Nessuno dei metodi predefiniti funzionerà. L'applicazione di backup deve usare API specializzate per eseguire l'operazione di ripristino. Per questo metodo di backup, il richiedente deve comprendere completamente il writer in questione. Per [le istanze attualmente supportate, vedere](special-vss-usage-cases.md) Casi speciali di utilizzo del Servizio Copia Copia Microsoft.

 

 




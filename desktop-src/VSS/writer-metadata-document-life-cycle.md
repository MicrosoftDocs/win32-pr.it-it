---
description: 'In risposta a un evento di identificazione, ogni writer presente nel sistema costruisce il proprio documento di metadati del writer usando IVssCreateWriterMetadata. Un evento di identificazione viene in genere generato da un richiedente che chiama IVssBackupComponents:: GatherWriterMetadata.'
ms.assetid: bae9bbe7-ca55-47cb-b253-8092007cb181
title: Ciclo di vita del documento dei metadati del writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45be5748625d21f99abe3e77e0d6474a62210904
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307119"
---
# <a name="writer-metadata-document-life-cycle"></a>Ciclo di vita del documento dei metadati del writer

In risposta a un [*evento di identificazione*](vssgloss-i.md), ogni writer presente nel sistema costruisce il proprio documento di metadati del writer usando [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata). Un *evento di identificazione* viene in genere generato da un richiedente che chiama [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

Quando si crea un documento di metadati del writer, tramite l'interfaccia [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) o l'inizializzazione del writer ([**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)), un writer deve specificare in modo esplicito quanto segue:

-   [*Metodo Restore*](vssgloss-r.md)
-   Nome writer
-   [*ID classe Writer*](vssgloss-w.md)
-   Utilizzo dei dati ( [**vedere \_ \_ tipo di utilizzo VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type))
-   Tipo di origine data (vedere il [**\_ \_ tipo di origine VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type))

Inoltre, è possibile specificare quanto segue:

-   Componenti (che possono contenere o meno i set di file)
-   Aggiungi mapping alternativi
-   Escludi elenchi di file

Una panoramica della creazione dei documenti dei metadati del writer si trova nelle [azioni del writer durante l'inizializzazione del backup](overview-of-backup-initialization.md).

Per ottenere l'accesso ai metadati del writer, i richiedenti usano in genere uno dei due metodi seguenti:

-   Durante la maggior parte delle operazioni di backup, un richiedente USA [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) per ottenere un'istanza dell'interfaccia [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) per consentire l'accesso ai metadati di un writer attualmente in esecuzione.
-   Per le operazioni di ripristino o i backup che usano copie shadow importate (vedere [importazione di volumi copiati shadow trasportabili](importing-transportable-shadow-copied-volumes.md) per altre informazioni sull'importazione di copie shadow), un richiedente recupera un documento XML contenente i metadati e USA [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) per ottenere un'interfaccia [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) , che usa per leggere i metadati del ripristino.

I documenti di metadati del writer consentono al richiedente di eseguire un backup per ottenere informazioni sui Writer attualmente in esecuzione durante la fase di individuazione di un backup.

Per gli autori scelti per partecipare a un backup, un richiedente importa molte, ma non tutte, le informazioni contenute nel documento dei metadati del writer nel documento relativo ai propri componenti di backup durante la fase di individuazione di un backup.

Tuttavia, solo i documenti dei metadati del writer e non il documento dei componenti di backup contengono le specifiche di file e percorso.

Per ulteriori informazioni sul modo in cui viene eseguita la fase di individuazione di un'operazione di backup, vedere [Cenni preliminari sulla fase di individuazione del backup](overview-of-the-backup-discovery-phase.md).

Inoltre, durante un'operazione di backup solo i componenti [*inclusi in modo esplicito*](vssgloss-e.md) dispongono delle informazioni archiviate nel documento componenti di backup. Le informazioni sui componenti [*inclusi in modo implicito*](vssgloss-i.md) non sono incluse nel documento componenti di backup durante un'operazione di backup e devono essere interpolate utilizzando le informazioni sui componenti inclusi in modo esplicito e sui documenti di metadati del writer disponibili.

È possibile che i componenti inclusi in modo implicito siano ancora [*selezionabili per il ripristino*](vssgloss-s.md) e che debbano essere inclusi in modo esplicito nel documento componenti di backup in fase di ripristino. In questo caso, come l'aggiunta di un componente durante un'operazione di backup, è necessario accedere al documento di metadati del writer writer's del componente (recuperato dal writer), un richiedente dovrà accedere a una copia dei documenti di metadati del writer del writer archiviati in fase di backup.

Pertanto, l'unico modo per ottenere tutte le informazioni su tutti i file e i componenti coinvolti in un backup o un ripristino consiste nel disporre di ogni documento di metadati del writer per ogni writer che partecipa a un backup archiviato insieme al documento componenti di backup. Per ulteriori informazioni, vedere [Panoramica del ripristino effettivo dei file](overview-of-actual-file-restoration.md).

 

 




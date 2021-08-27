---
description: In risposta a un evento Identify, ogni writer presente nel sistema costruisce il proprio documento di metadati del writer usando IVssCreateWriterMetadata. Un evento Identify viene in genere generato da un richiedente che chiama IVssBackupComponents::GatherWriterMetadata.
ms.assetid: bae9bbe7-ca55-47cb-b253-8092007cb181
title: Ciclo di vita del documento dei metadati del writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2796d1a7b995f13829ac81485f74fa342bebe5e0e312b7b014d761a9962aa74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121574"
---
# <a name="writer-metadata-document-life-cycle"></a>Ciclo di vita del documento dei metadati del writer

In risposta a un [*evento Identify,*](vssgloss-i.md)ogni writer presente nel sistema costruisce il proprio documento di metadati del writer [**usando IVssCreateWriterMetadata.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) Un *evento Identify* viene in genere generato da un richiedente che chiama [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

Quando si crea un documento di metadati del writer, tramite [**l'interfaccia IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) o tramite l'inizializzazione del writer ([**CVssWriter::Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)), un writer deve specificare in modo esplicito quanto segue:

-   [*Metodo Restore*](vssgloss-r.md)
-   Nome del writer
-   [*ID classe writer*](vssgloss-w.md)
-   Consumo dati (vedere [**VSS \_ USAGE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type))
-   Tipo di origine data (vedere [**VSS \_ SOURCE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type))

Può anche specificare quanto segue:

-   Componenti (che possono contenere o meno set di file)
-   Aggiungere mapping alternativi
-   Escludere elenchi di file

Una panoramica della creazione di documenti di metadati del writer è disponibile in Writer Actions during Backup Initialization ( Azioni [writer durante l'inizializzazione del backup).](overview-of-backup-initialization.md)

I richiedenti in genere usano uno dei due metodi per ottenere l'accesso ai metadati del writer:

-   Durante la maggior parte delle operazioni di backup, un richiedente usa [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) per ottenere un'istanza [**dell'interfaccia IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) per consentire l'accesso ai metadati di un writer attualmente in esecuzione.
-   Per operazioni di ripristino o backup tramite copie shadow importate (vedere Importazione di volumi copiati [shadow](importing-transportable-shadow-copied-volumes.md) trasportabili per altre informazioni sull'importazione di copie shadow), un richiedente recupera un documento XML contenente i metadati e usa [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) per ottenere [**un'interfaccia IVssExamineWriterMetadata,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) che usa per leggere i metadati di ripristino.

I documenti dei metadati del writer consentono al richiedente di eseguire un backup di acquisire informazioni sull'esecuzione dei writer durante la fase di individuazione di un backup.

Per i writer scelti per partecipare a un backup, un richiedente importa molte, ma non tutte, le informazioni nel documento dei metadati del writer nel proprio documento dei componenti di backup durante la fase di individuazione di un backup.

Tuttavia, solo i documenti di metadati del writer e non il documento dei componenti di backup contengono le specifiche di file e percorso.

Per altre informazioni sul modo in cui viene eseguita la fase di individuazione di un'operazione di backup, vedere [Panoramica della fase di individuazione del backup](overview-of-the-backup-discovery-phase.md).

Inoltre, solo i [*componenti inclusi in modo*](vssgloss-e.md) esplicito hanno le informazioni archiviate nel documento Componenti di backup durante un'operazione di backup. Le informazioni sui componenti inclusi in modo [*implicito*](vssgloss-i.md) non sono incluse nel documento Componenti di backup durante un'operazione di backup e devono essere interpolate usando informazioni sui componenti inclusi in modo esplicito e sui documenti dei metadati del writer disponibili.

I componenti inclusi in [](vssgloss-s.md) modo implicito possono comunque essere selezionabili per il ripristino e potrebbero dover essere inclusi in modo esplicito nel documento Componenti di backup in fase di ripristino. In questo caso, proprio come l'aggiunta di un componente durante un'operazione di backup richiedeva l'accesso al documento dei metadati del writer del componente (quindi recuperato dal writer), un richiedente richiederà l'accesso a una copia dei documenti dei metadati del writer archiviati in fase di backup.

Pertanto, l'unico modo per ottenere tutte le informazioni su tutti i file e i componenti coinvolti in un backup o un ripristino è fare in modo che ogni documento di metadati del writer per ogni writer che partecipa a un backup sia archiviato insieme al documento dei componenti di backup. Per altre informazioni, vedere [Panoramica del ripristino effettivo dei file.](overview-of-actual-file-restoration.md)

 

 




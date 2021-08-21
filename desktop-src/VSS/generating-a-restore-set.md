---
description: Un set di ripristino è un elenco di tutti i file da ripristinare e dei percorsi in cui verranno ripristinati.
ms.assetid: 3196c26c-3407-4c00-a800-c3497df583e5
title: Generazione di un set di ripristino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85dd620869614420e5073f47ef4ac8732b1e2c0d0d218ea0e94ae690cb9f773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958451"
---
# <a name="generating-a-restore-set"></a>Generazione di un set di ripristino

Un set di ripristino è un elenco di tutti i file da ripristinare e dei percorsi in cui verranno ripristinati.

Come per la generazione dell'elenco dei file di backup (vedere Generazione di un set di [backup](generating-a-backup-set.md)), un algoritmo per determinare quali file ripristinare e dove ripristinarli deve procedere istanza [*del writer*](vssgloss-w.md) per istanza del writer e componente per componente per ogni istanza del writer.

È necessario associare ogni file nel supporto di backup al componente che lo ha gestito. È anche necessario ottenere il metodo di ripristino del componente [](vssgloss-r.md) di gestione [*,*](vssgloss-r.md)le informazioni sulla destinazione di ripristino del file e i [*mapping*](vssgloss-a.md) dei percorsi alternativi (se presenti).

Alcuni file possono anche richiedere operazioni [*su file parziali*](vssgloss-p.md) o destinazioni [*indirizzate per*](vssgloss-d.md) il ripristino.

Esaminando la selezionabilità dei componenti per i percorsi logici e di [*backup*](vssgloss-s.md) [*(vedere*](vssgloss-l.md) Uso della selezionabilità e dei percorsi logici), [](working-with-selectability-and-logical-paths.md)un richiedente è in grado di determinare la struttura dei componenti dell'operazione di backup che verrà ripristinata.

Una volta stabilita la struttura del componente del backup, il richiedente può ottenere le informazioni sul set di [*file*](vssgloss-f.md) di ogni componente (specifica del file, percorso e flag di ricorsione). Un richiedente può quindi generare un set di ripristino.

I file [*che*](vssgloss-p.md) [](vssgloss-d.md) richiedono file parziali o destinazioni indirizzate forniscono istruzioni di ripristino dettagliate (vedere Percorsi di [backup](non-default-backup-and-restore-locations.md)e ripristino non predefiniti), che possono quindi essere aggiunti al set di ripristino.

Un meccanismo tipico per la generazione di un set di [](vssgloss-d.md) ripristino per i file non coinvolti in operazioni di file parziali o le destinazioni indirizzate possono procedere eseguendo le operazioni seguenti:

1.  Ottenere un elenco di file nei supporti di backup, inclusi i percorsi originali.

2.  Identificare la [*classe e il*](vssgloss-w.md) componente writer per ogni file nel supporto di backup eseguendo le operazioni seguenti:

    -   Per ogni writer, ottenere informazioni sui componenti ([**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)) chiamando [**IVssExamineWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) su tutti i relativi componenti.
    -   Per ogni componente, ottenere informazioni sul descrittore di file ([**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)) per ogni set di file contenuto dal componente (a seconda dei tipi di dati contenuti dal componente chiamando [**IVssWMComponent::GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent::GetDatabaseFilee**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile) [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile).
    -   Confrontare le informazioni sul nome e sul percorso del file con le informazioni sul percorso restituite dalle informazioni sul percorso contenute nel descrittore di file per ogni set di file in un componente (restituito da [**IVssWMFiledesc::GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), [**IVssWMFiledesc::GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)e [**IVssWMFiledesc::GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)) con le informazioni sul percorso dei file archiviati per determinare se il file fa parte del componente.
        > [!Note]  
        > È consigliabile ignorare eventuali informazioni sul percorso alternativo nel descrittore di file recuperato da un componente trovato in un documento di metadati del writer archiviato, ovvero [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) non restituisce **NULL.** Questo percorso alternativo è il [*percorso alternativo*](vssgloss-a.md), che viene usato solo durante il backup.

         

3.  Ottenere informazioni di mapping alternative per ogni file nei supporti di backup:

    -   I mapping di file alternativi vengono archiviati nel writer, non a livello di componente, e vengono ottenuti dall'oggetto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) restituito da [**IVssExamineWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping).
    -   È possibile determinare se un determinato file ha un mapping di percorso alternativo controllando il percorso e il nome del file rispetto al percorso e alla specifica di file contenuti nel mapping di percorso alternativo restituito da [**IVssExamineWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping), tramite [**IVssWMFiledesc::GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), [**IVssWMFiledesc::GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)e [**IVssWMFiledesc::GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive). Se durante il backup è stato usato un percorso alternativo, tali informazioni devono essere ignorate durante l'elaborazione di un ripristino.
    -   Se un file e un descrittore di file di mapping di percorso alternativo corrispondono, usare il metodo [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) dell'oggetto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) restituito da [**IVssExamineWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) per trovare il percorso alternativo in cui è possibile ripristinare il file.
    -   Il mapping del percorso alternativo ottenuto in questo modo non concorderà necessariamente con quello restituito dal documento dei componenti di backup da [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping). Il [**valore IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) non è blank solo se per un file viene usato il mapping del percorso alternativo.

4.  Con queste informazioni su file e componenti, è possibile eseguire query sul documento dei componenti di backup per ottenere informazioni sulle destinazioni di ripristino, le opzioni e i nuovi percorsi di ripristino per ogni file. Queste informazioni possono essere combinate con l'elenco di file, componenti e percorsi alternativi.

5.  I file non protetti dai writer possono essere selezionati in modo coerente con le operazioni di ripristino tradizionali.

A questo punto, un richiedente deve avere un elenco di tutti i file necessari per il ripristino, insieme alle istruzioni su come ripristinarli, e può iniziare a ripristinare i file in base a:

-   La presenza o l'assenza di un file in tale percorso di destinazione e delle impostazioni dei componenti di VSS RESTORE TARGET e VSS RESTOREMETHOD ENUM dipendono dalla presenza o dall'assenza di un file in tale percorso di destinazione e dalle impostazioni dei componenti di [**VSS \_ RESTORE \_ TARGET**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target) e [**VSS \_ RESTOREMETHOD \_ ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) (vedere Percorsi di [backup](non-default-backup-and-restore-locations.md)e ripristino non predefiniti).
-   La riuscita di un tentativo di ripristino dipenderà da problemi come le autorizzazioni di accesso della destinazione, se i file di destinazione sono bloccati e altri problemi convenzionali coinvolti nel ripristino dei file.
-   L'esito positivo o negativo del ripristino di un determinato componente per una determinata istanza del writer deve essere mantenuto nel documento dei componenti di backup chiamando [**IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus). In questo modo le informazioni saranno accessibili agli autori quando elaborano l'evento PostRestore.
-   Se un file viene ripristinato in un mapping di percorso alternativo, il richiedente deve chiamare [**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping). In questo modo i writer potranno determinare se i file sono stati ripristinati in percorsi alternativi tramite [**IVssComponent::GetAlternateLocationMapping.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)
-   I richiedenti possono trovare utile ripristinare i file in percorsi completamente nuovi. Questo è accettabile, ma il richiedente deve indicare questo al writer usando il metodo [**IVssBackupComponents::AddNewTarget.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)

 

 




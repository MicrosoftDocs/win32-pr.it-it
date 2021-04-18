---
description: Un set di ripristino è un elenco di tutti i file da ripristinare e i percorsi in cui verranno ripristinati.
ms.assetid: 3196c26c-3407-4c00-a800-c3497df583e5
title: Generazione di un set di ripristino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db3447ba6d258a5f22fff958761abc7ac0e4f27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310718"
---
# <a name="generating-a-restore-set"></a>Generazione di un set di ripristino

Un set di ripristino è un elenco di tutti i file da ripristinare e i percorsi in cui verranno ripristinati.

Come durante la generazione dell'elenco dei file di backup (vedere [generazione di un set di backup](generating-a-backup-set.md)), un algoritmo per determinare quali file ripristinare e dove ripristinarli deve continuare l' [*istanza*](vssgloss-w.md) del writer in base all'istanza del writer e per ogni istanza del writer.

È necessario associare ogni file sul supporto di backup con il componente che lo ha gestito. È anche necessario ottenere il [*metodo di ripristino*](vssgloss-r.md)del componente di gestione e le informazioni sulla [*destinazione di ripristino*](vssgloss-r.md) del file e i relativi [*mapping del percorso alternativo*](vssgloss-a.md) (se presenti).

Alcuni file possono anche richiedere operazioni [*parziali sui file*](vssgloss-p.md) o [*destinazioni dirette*](vssgloss-d.md) per il ripristino.

Esaminando la selezione dei componenti [*per*](vssgloss-s.md) i [*percorsi logici*](vssgloss-l.md) e di backup (vedere [utilizzo di selezione e percorsi logici](working-with-selectability-and-logical-paths.md)), un richiedente è in grado di determinare la struttura del componente dell'operazione di backup che verrà ripristinata.

Con la struttura del componente del backup stabilita, il richiedente può ottenere le informazioni sul [*set di file*](vssgloss-f.md) di ogni componente (specifica del file, percorso e flag di ricorsione). Un richiedente può quindi generare un set di ripristino.

I file che richiedono [*file parziali*](vssgloss-p.md)o [*destinazioni dirette*](vssgloss-d.md) forniscono le proprie istruzioni di ripristino dettagliate (vedere [percorsi di backup e ripristino non predefiniti](non-default-backup-and-restore-locations.md)), che possono essere aggiunti al set di ripristino.

Un meccanismo tipico per la generazione di un set di ripristino per i file non interessati da operazioni di file parziali o per le [*destinazioni dirette*](vssgloss-d.md) può procedere con le operazioni seguenti:

1.  Ottenere un elenco di file nel supporto di backup, inclusi i percorsi originali.

2.  Identificare la [*classe*](vssgloss-w.md) e il componente writer per ogni file nel supporto di backup effettuando le operazioni seguenti:

    -   Per ogni writer, ottenere informazioni sul componente ([**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)) chiamando [**IVssExamineWriterMetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) su tutti i relativi componenti.
    -   Per ogni componente, ottenere informazioni sul descrittore del file ([**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)) per ogni set di file contenuti nel componente (a seconda dei tipi di dati contenuti nel componente chiamando [**IVssWMComponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent:: GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)e [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile).
    -   Confrontare le informazioni sul nome e sul percorso del file rispetto a quelle restituite dalle informazioni sul percorso contenute nel descrittore di file per ogni set di file in un componente (restituito da [**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), [**IVssWMFiledesc:: GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)e [**IVssWMFiledesc:: getricorsivy**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)) sulle informazioni sul percorso dei file archiviati per determinare se il file fa parte del componente.
        > [!Note]  
        > È necessario ignorare tutte le informazioni sul percorso alternativo nel descrittore di file recuperato da un componente trovato in un documento di metadati del writer archiviato, ovvero [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) non restituisce **null**. Questo percorso alternativo è il [*percorso alternativo*](vssgloss-a.md), che viene usato solo durante il backup.

         

3.  Ottenere informazioni di mapping alternative per ogni file nel supporto di backup:

    -   I mapping di file alternativi vengono archiviati nel writer, non a livello di componente e ottenuti dall'oggetto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) restituito da [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping).
    -   È possibile determinare se un determinato file ha un mapping del percorso alternativo controllando il percorso e il nome del file in base al percorso e alla specifica del file contenuti nel mapping del percorso alternativo restituito da [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping), tramite [**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), [**IVssWMFiledesc:: GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)e [**IVssWMFiledesc:: getricorsivy**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive). Se durante il backup è stato utilizzato un percorso alternativo, tali informazioni devono essere ignorate durante questa verifica durante l'elaborazione di un ripristino.
    -   Se un file e un percorso alternativo esegue il mapping dei descrittori di file, si usa il metodo [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) dell'oggetto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) restituito da [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) per trovare il percorso alternativo in cui è possibile ripristinare il file.
    -   Il mapping del percorso alternativo ottenuto in questo modo non corrisponderà necessariamente a quello restituito dal documento componenti di backup di [**IVssComponent:: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping). Il valore [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) non è vuoto solo se per un file viene usato il mapping del percorso alternativo.

4.  Con questo file e informazioni sul componente, è possibile eseguire query sul documento componenti di backup per ottenere informazioni sulle destinazioni di ripristino, sulle opzioni e sui nuovi percorsi di ripristino per ogni file. Queste informazioni possono essere combinate con l'elenco di file, componenti e posizioni alternative.

5.  I file non protetti dai writer possono essere selezionati in modo coerente con le normali operazioni di ripristino.

A questo punto, un richiedente deve avere un elenco di tutti i file necessari per il ripristino, oltre a istruzioni su come ripristinarli, e può iniziare a ripristinare i file in base a:

-   Se i mapping del percorso alternativo o il percorso del file originale deve essere usato come destinazione per il ripristino, dipenderà dalla presenza o dall'assenza di un file in tale percorso di destinazione e dalle impostazioni dei componenti della [**\_ \_ destinazione di ripristino VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target) e dell' [**\_ \_ enumerazione RESTOREMETHOD VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) (vedere i [percorsi di backup e ripristino non predefiniti](non-default-backup-and-restore-locations.md)).
-   Se un tentativo di ripristino ha esito positivo dipenderà da problemi quali le autorizzazioni di accesso della destinazione, se i file di destinazione sono bloccati e altri problemi convenzionali correlati al ripristino del file.
-   L'esito positivo o negativo del ripristino di un determinato componente per una determinata istanza di writer deve essere mantenuto nel documento componenti di backup chiamando [**IVssBackupComponents:: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus). In questo modo le informazioni potranno essere accessibili ai writer quando elaborano l'evento PostRestore.
-   Se un file viene ripristinato in un mapping di percorso alternativo, il richiedente deve chiamare [**IVssBackupComponents:: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping). Ciò consentirà ai writer di determinare se i file sono stati ripristinati in percorsi alternativi tramite [**IVssComponent:: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping).
-   I richiedenti possono essere utili per ripristinare i file in posizioni completamente nuove. Questa operazione è accettabile, ma il richiedente deve indicare questo oggetto al writer usando il metodo [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) .

 

 




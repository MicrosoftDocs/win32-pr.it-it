---
description: Un set di backup è un elenco di tutti i file di cui eseguire il backup, i relativi percorsi e come eseguire il backup.
ms.assetid: 34a66a9c-c1bc-437d-b034-59dc0c88228c
title: Generazione di un set di backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120643c827afdabfbb9a2c347fa16290e03969f0e87f913b0c5d9fdb682f2619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122121"
---
# <a name="generating-a-backup-set"></a>Generazione di un set di backup

Un set di backup è un elenco di tutti i file di cui eseguire il backup, i relativi percorsi e come eseguire il backup.

Un richiedente deve usare i file contenuti nei volumi copiati shadow dopo che [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) ha restituito correttamente per generare l'elenco completo dei file di cui eseguire il backup.

Inoltre, un richiedente deve gestire la possibilità che alcuni file [*presentino*](vssgloss-a.md) percorsi alternativi e che alcuni file siano stati esclusi.

Un algoritmo per la selezione dei file di cui eseguire il backup deve essere basato su un'istanza del writer in base all'istanza del [*writer,*](vssgloss-w.md) componente per componente (come nel caso del ripristino; vedere Generazione di un [set](generating-a-restore-set.md)di ripristino) e procedere come segue:

1.  Determinazione dei volumi che contengono i file del writer e gli oggetti dispositivo corrispondenti
2.  Uso delle informazioni sul set di [*file*](vssgloss-f.md) (contenute negli oggetti [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) restituiti da [**IVssExamineWriterMetadata::GetExcludeFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile)) per creare un elenco dei file esclusi in modo esplicito, se necessario usando **FindFileFirst**, **FindFileFirstEx** e **FindNextFile**.
3.  Iterazione di tutti i componenti di un writer, usando [**IVssExamineWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent). Se è selezionato un componente selezionabile, usare [*il percorso*](vssgloss-l.md) logico per ottenere i componenti non selezionabili associati in un set di componenti. Vedere [Uso della selezionabilità e dei percorsi logici.](working-with-selectability-and-logical-paths.md)
4.  Recupero dei [*set di file*](vssgloss-f.md) contenuti in ogni componente selezionato tramite l'interfaccia [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) corrispondente a ogni componente in esso contenuto.
5.  Generazione di un elenco di file dalle specifiche, se necessario usando **FindFileFirst**, **FindFileFirstEx** e **FindNextFile**.
6.  Verifica di ogni file nell'elenco generato dalle informazioni sui componenti rispetto all'elenco dei file esclusi generati in precedenza. Questa operazione deve essere eseguita usando il percorso predefinito per il file (restituito da [**IVssWMFiledesc::GetPath),**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)non dal percorso alternativo restituito da [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation). Se il file corrisponde all'elenco escluso, non verrà eseguito il backup.
7.  Scelta della posizione effettiva da cui eseguire il backup (usando il percorso alternativo se impostato)
8.  A questo punto, è disponibile un elenco completo dei file e dei relativi percorsi ed è possibile avviare un backup.

Dopo aver generato un set di backup iniziale per tutti i writer presenti nel sistema, il richiedente controlla quindi la chiave del Registro di sistema seguente:

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ BackupRestore \\ FilesNotToBackup**

Il richiedente usa le sottochiavi in questa chiave come indicato di seguito:

-   Se un writer è presente nel sistema ed è presente una sottochiave il cui nome corrisponde al nome del writer, tale sottochiave deve essere ignorata.
-   Se un writer era presente nel sistema ma è attualmente assente dal set di backup ed è presente una sottochiave corrispondente, tutti i file specificati nei dati della sottochiave vengono esclusi e devono essere rimossi dal set di backup.
-   L'applicazione di backup aggiunge file ai dati della sottochiave creando un valore MULTI SZ contenente un elenco di specifiche di file per i file di cui non è necessario \_ eseguire il backup. Ogni stringa nel valore MULTI \_ SZ deve contenere una specifica di file.
-   Le specifiche del file possono contenere ? e \* caratteri jolly. Una specifica può essere resa ricorsiva aggiungendo /s alla fine. Se ad esempio si specifica "%TEMP% /s", non verrà eseguito il backup di tutti i file nella directory %TEMP% e in tutte \\ \* le relative sottodirectory.

 

 




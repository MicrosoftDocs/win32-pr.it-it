---
description: Un set di backup è un elenco di tutti i file di cui eseguire il backup, le rispettive posizioni e il modo in cui eseguirne il backup.
ms.assetid: 34a66a9c-c1bc-437d-b034-59dc0c88228c
title: Generazione di un set di backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827d9ecb90ac376aa9818b61e8dab65550ff8c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310717"
---
# <a name="generating-a-backup-set"></a>Generazione di un set di backup

Un set di backup è un elenco di tutti i file di cui eseguire il backup, le rispettive posizioni e il modo in cui eseguirne il backup.

Un richiedente deve usare i file contenuti nei volumi copiati shadow dopo [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) restituisce correttamente l'elenco completo dei file di cui eseguire il backup.

Inoltre, un richiedente deve gestire la possibilità che alcuni file abbiano [*percorsi alternativi*](vssgloss-a.md) e che alcuni file siano stati esclusi.

Un algoritmo per la selezione dei file di cui eseguire il backup deve essere eseguito in un' [*istanza del writer*](vssgloss-w.md) in base a un'istanza del writer, a seconda del componente, come avverrebbe durante il ripristino. vedere [generazione di un set di ripristino](generating-a-restore-set.md)e procedere con le operazioni seguenti:

1.  Determinazione dei volumi che contengono i file del writer e degli oggetti dispositivo corrispondenti
2.  Utilizzando le informazioni sui [*set di file*](vssgloss-f.md) , contenute negli oggetti [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) restituiti da [**IVssExamineWriterMetadata:: GetExcludeFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile), per creare un elenco dei file esclusi in modo esplicito, se necessario utilizzando **FindFileFirst**, **FindFileFirstEx** e **FindNextFile**.
3.  Iterazione su tutti i componenti di un writer usando [**IVssExamineWriterMetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent). Se è selezionato un componente selezionabile, utilizzare il [*percorso logico*](vssgloss-l.md) per ottenere i componenti non selezionabili Associati in un set di componenti. (Vedere [uso di selezione e percorsi logici](working-with-selectability-and-logical-paths.md)).
4.  Ottenere i [*set di file*](vssgloss-f.md) contenuti in ogni componente selezionato usando l'interfaccia [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) corrispondente a ogni componente che contiene.
5.  Generazione di un elenco di file dalle specifiche, se necessario usando **FindFileFirst**, **FindFileFirstEx** e **FindNextFile**.
6.  Controllo di ogni file nell'elenco generato dalle informazioni sul componente rispetto all'elenco dei file esclusi generati in precedenza. Questa operazione deve essere eseguita utilizzando il percorso predefinito per il file (restituito da [**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), non dal percorso alternativo restituito da [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)). Se il file corrisponde all'elenco escluso, non verrà eseguito il backup.
7.  Scelta del percorso effettivo dal quale eseguire il backup (usando il percorso alternativo se è stato impostato)
8.  A questo punto, è disponibile un elenco completo dei file e delle rispettive posizioni ed è possibile iniziare un backup.

Dopo la generazione di un set di backup iniziale per tutti i writer presenti nel sistema, il richiedente controlla la seguente chiave del registro di sistema:

**HKEY \_ Local \_ computer \\ System \\ CurrentControlSet \\ Control \\ backuprestore \\ FilesNotToBackup**

Il richiedente usa le sottochiavi sotto questa chiave come indicato di seguito:

-   Se un writer è presente nel sistema ed è presente una sottochiave il cui nome corrisponde al nome del writer, tale sottochiave deve essere ignorata.
-   Se un writer era presente nel sistema ma è attualmente assente dal set di backup ed è presente una sottochiave corrispondente, tutti i file specificati nei dati della sottochiave vengono esclusi e devono essere rimossi dal set di backup.
-   L'applicazione di backup aggiunge file ai dati della sottochiave creando un \_ valore di più SZ contenente un elenco di specifiche di file per i file di cui non è necessario eseguire il backup. Ogni stringa nel valore di più \_ SZ deve contenere una specifica del file.
-   Le specifiche dei file possono contenere? e \* caratteri jolly. Una specifica può essere resa ricorsiva aggiungendo/s alla fine. Se ad esempio si specifica "% TEMP% \\ \* /s", non sarà possibile eseguire il backup di tutti i file nella directory% Temp% e di tutte le relative sottodirectory.

 

 




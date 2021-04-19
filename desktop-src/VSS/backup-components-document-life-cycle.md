---
description: I richiedenti hanno la responsabilità principale del ciclo di vita di un documento dei componenti di backup.
ms.assetid: 287b7b9a-ac04-4a74-83c1-2cdd4a571ac1
title: Ciclo di vita del documento dei componenti di backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bcb0263f46466d7be2bc19f3c8809167b2da08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318908"
---
# <a name="backup-components-document-life-cycle"></a>Ciclo di vita del documento dei componenti di backup

I richiedenti hanno la responsabilità principale del ciclo di vita di un documento dei componenti di backup.

Questo controllo viene esercitato da un'istanza dell'oggetto interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) restituito da [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents).

Un richiedente deve inizializzare un documento di componenti di backup prima di eseguire un backup o un ripristino chiamando [**IVssBackupComponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) o [**IVssBackupComponents:: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore). Il richiedente può inizializzare il documento come vuoto oppure può caricare una copia precedentemente archiviata del documento.

Per le operazioni di backup, un documento relativo ai componenti di backup viene in genere inizializzato come vuoto. I dati verranno compilati con la collaborazione dei writer del sistema nel corso dell'elaborazione del backup.

Per le operazioni di ripristino, un documento relativo ai componenti di backup viene in genere inizializzato da un documento archiviato generato durante il backup iniziale. In questo modo il ripristino (insieme all'esame dei documenti dei metadati del writer archiviato) consente di determinare quali dati sono stati inizialmente sottoposti a backup e come devono essere ripristinati.

Il backup delle [*copie shadow trasportabili*](vssgloss-t.md) è un'eccezione a questa regola. In tal caso, è possibile che una copia shadow sia stata spostata da un sistema (in cui è stata creata insieme al documento componenti di backup iniziale) a un'altra per mezzo della riassegnazione dell'unità logica di un dispositivo di archiviazione condivisa. Per eseguire il backup in queste circostanze, un richiedente carica lo stato di backup archiviato e procede dal punto in cui il sistema iniziale è stato interrotto. Per ulteriori informazioni, vedere [importazione di volumi con copia shadow trasportabili](importing-transportable-shadow-copied-volumes.md).

Nel corso dell'elaborazione di un backup, il richiedente decide quali componenti copiare effettivamente sulla base dei componenti contrassegnati come [*selezionabili per il backup*](vssgloss-s.md), i [*percorsi logici*](vssgloss-l.md)del componente e la propria logica interna.

Alcuni componenti verranno [*inclusi in modo esplicito*](vssgloss-e.md) nell'operazione di backup; le informazioni sul componente verranno aggiunte al documento componenti di backup. Altri verranno [*inclusi in modo implicito*](vssgloss-i.md) nel backup; le informazioni sui componenti aggiunti non verranno aggiunte al documento componenti di backup.

Tutti i componenti non selezionabili di un writer per i componenti di backup senza predecessore selezionabili nel percorso logico e quelli selezionabili per i componenti di backup scelti dal richiedente verranno aggiunti in modo esplicito.

È possibile aggiungere in modo implicito i componenti non selezionabili e selezionabili per il backup se hanno un predecessore selezionabile nel percorso logico, incluso in modo esplicito nel backup. Questi componenti ([*sottocomponenti*](vssgloss-s.md)) sono membri dei [*set di componenti*](vssgloss-s.md) definiti dal predecessore selezionabile.

Quando si gestiscono le operazioni di ripristino, il richiedente usa la [*selezione per il ripristino*](vssgloss-s.md) anziché la selezione per il backup in combinazione con le informazioni sul percorso logico e la relativa logica interna per decidere quali file ripristinare.

Se un componente che è stato aggiunto in modo implicito al backup è ora aggiunto in modo esplicito al ripristino, il richiedente aggiornerà il documento relativo ai componenti di backup con le informazioni di tale componente.

Le informazioni sui componenti archiviati sono disponibili sia per i richiedenti che per i writer tramite istanze dell'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Tramite le interfacce [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) che i writer possono eseguire query e (fino alla fine di eventi [**PostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) e [**PostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) ) modificare le informazioni nel documento componenti di backup.

Quando viene chiamato il gestore eventi [**CVssWriter:: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup), [**CVssWriter:: OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore), [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot), [**CVssWriter:: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete)o [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) , un writer riceve un'istanza di un'interfaccia [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) .

Si noti che al momento della generazione dell'evento [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) , il documento componenti di backup viene reso di sola lettura e pertanto [**CVssWriter:: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) non può utilizzare l'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) per modificarlo.

Dall'interfaccia [**IVSSWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) , il writer può recuperare le istanze dell'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) che consentiranno all'IT di accedere a tutti i componenti aggiunti in modo esplicito al documento dei componenti di backup e di modificarne lo stato. Per ulteriori informazioni, vedere [Cenni preliminari sull'elaborazione di un backup in VSS](overview-of-processing-a-backup-under-vss.md) e [Panoramica sull'elaborazione di un ripristino in VSS](overview-of-processing-a-restore-under-vss.md).

I documenti dei componenti di backup vengono rimossi dalla memoria quando viene rilasciata l'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) e devono essere archiviati con [**IVssBackupComponents:: saveasxml**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml)o tutte le relative informazioni andranno perse.

Inoltre, quando un documento [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) viene rilasciato correttamente, viene generato un evento [**BackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown) e vengono eliminate le [*copie shadow di rilascio automatico*](vssgloss-a.md) .

 

 




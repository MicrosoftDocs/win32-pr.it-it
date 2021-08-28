---
description: VsS consente a un richiedente di accedere alla copia shadow dei volumi contenenti dati per il backup e di copiare i dati nei supporti di backup.
ms.assetid: 187f26f2-f191-4703-9bde-3357f1ceef0c
title: Panoramica del backup effettivo dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2413111467014b666d219a7a1e92efad26302e5c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475697"
---
# <a name="overview-of-actual-backup-of-files"></a>Panoramica del backup effettivo dei file

VsS consente a un richiedente di accedere alla copia shadow dei volumi contenenti dati per il backup e di copiare i dati nei supporti di backup. I writer in genere procedono con il normale funzionamento durante questo processo. Per altre informazioni, vedere [Panoramica dell'elaborazione di un backup in VSS.](overview-of-processing-a-backup-under-vss.md)

La tabella seguente illustra la sequenza di azioni ed eventi necessari per il backup dei file.




| Azione del richiedente | Evento | Azione writer | 
|------------------|-------|---------------|
| Accedere ai file nel volume copiato automaticamente (vedere <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties"><strong>IVssBackupComponents::GetSnapshotProperties</strong></a>, <a href="/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop"><strong>VSS_SNAPSHOT_PROP</strong></a>) | Nessuno | Nessuno | 
| Generare l'elenco dei file di cui eseguire il backup e copiare i dati dei file nei supporti di backup. | Nessuno | Nessuno | 
| Indicare l'esito positivo o negativo del backup <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded"><strong>con IVssBackupComponents::SetBackupSucceeded</strong></a>. | Nessuno | Nessuno | 
| Il richiedente indica che il backup è stato completato chiamando <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>IVssBackupComponents::BackupComplete.</strong></a> | <a href="vssgloss-b.md"><em>BackupComplete</em></a> | Eseguire qualsiasi pulizia post-backup (vedere <a href="/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete"><strong>CVssWriter::OnBackupComplete</strong></a>, <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents"><strong>IVssWriterComponents</strong></a>, <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent"><strong>IVssComponent</strong></a>). | 
| Il richiedente attende che tutti i writer confermino la ricezione dell'evento <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>IVssBackupComponents::BackupComplete</strong></a> usando <a href="/windows/desktop/api/Vss/nn-vss-ivssasync"><strong>IVssAsync.</strong></a> Deve anche verificare lo stato del writer (vedere <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus"><strong>IVssBackupComponents::GatherWriterStatus</strong></a>, <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus"><strong>IVssBackupComponents::GetWriterStatus</strong></a>). Il richiedente deve chiamare <strong>GatherWriterStatus</strong> in questo momento per fare in modo che la sessione del writer sia impostata su uno stato completato.<blockquote>[!Note]<br />Questa operazione è necessaria solo in Windows Server 2008 con Service Pack 2 (SP2) e versioni precedenti.</blockquote><br /> | Nessuno | Nessuno | 
| Salvare il documento dei componenti di backup e ogni documento di metadati del writer in documenti XML, che possono essere scritti nei supporti di backup (vedere <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml"><strong>IVssBackupComponents::SaveAsXML</strong></a> e <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml"><strong>IVssExamineWriterMetadata::SaveAsXML).</strong></a> | Nessuno | Nessuno | 




 

## <a name="writer-actions-during-backup-of-files"></a>Azioni writer durante il backup di file

Al termine della copia shadow, tutte le operazioni di I/O nel sistema di cui viene eseguito il backup dovrebbero essere in grado di riprendere senza interrompere l'integrità del backup. Questa è una delle motivazioni più avanzate per la funzionalità di copia shadow.

Di conseguenza, come nella fase di individuazione (vedere Panoramica della fase di individuazione dei [backup),](overview-of-the-backup-discovery-phase.md)esistono poche richieste per i writer mentre viene effettivamente eseguito il backup dei file.

Al termine di un backup e dopo che un richiedente ha generato un evento [*BackupComplete,*](vssgloss-b.md) VSS chiamerà il metodo [**CVssWriter::OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) di ogni writer, un metodo virtuale che per impostazione predefinita restituisce **semplicemente TRUE.** Tuttavia, i writer possono eseguire l'override dell'implementazione predefinita e intraprendere azioni come la rimozione dei file temporanei rimanenti oppure [](vssgloss-e.md) usare l'interfaccia [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) con cui viene chiamato per controllare lo stato del backup di ognuno dei componenti inclusi in modo esplicito (e di qualsiasi [*set*](vssgloss-c.md) di componenti che potrebbero definire) recuperando l'oggetto [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) corrispondente. Il writer può quindi determinare e agire sull'esito positivo o negativo del backup chiamando [**IVssComponent:GetBackupSucceeded.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded) Il valore restituito da **IVssComponent:GetBackupSucceeded** sarà **TRUE** solo se è stato eseguito correttamente il backup di tutti i file inclusi in modo esplicito nel componente e di tutti i relativi [*sottocomponenti*](vssgloss-s.md) inclusi in modo [*implicito.*](vssgloss-i.md)

Al termine della chiamata a [**CVssWriter::OnBackupComplete,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) il richiedente deve chiamare [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (per ogni writer) un'ultima volta. La memoria dello stato della sessione del writer è una risorsa limitata e i writer devono riusare gli stati della sessione. Questo passaggio contrassegna lo stato della sessione di backup del writer come completato e notifica a VSS che questo slot della sessione di backup può essere riutilizzato da un'operazione di backup successiva.

## <a name="requester-actions-during-backup-of-files"></a>Azioni del richiedente durante il backup dei file

Come notato in [Panoramica della fase](overview-of-the-backup-discovery-phase.md)di individuazione del backup , è consigliabile non generare l'elenco effettivo dei file di cui eseguire il backup fino al completamento della copia shadow.

[*L'oggetto dispositivo*](vssgloss-d.md) corrispondente alla copia shadow di un determinato volume viene usato per ottenere l'accesso ai file nel volume copiato shadow al termine della copia shadow. L'oggetto dispositivo viene ottenuto [**dall'oggetto \_ \_ VSS SNAPSHOT PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) restituito da [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties). Ogni copia shadow di un set di copie shadow avrà un proprio oggetto dispositivo.

L'oggetto dispositivo e i percorsi ottenuti dalle specifiche del documento di metadati del writer dei componenti vengono quindi usati per selezionare i file per il backup. Per [altre informazioni, vedere Accesso del richiedente ai dati copiati shadow.](requestor-access-to-shadow-copied-data.md)

I file che verranno inclusi nell'elenco di backup dipendono dalla natura del backup specifico, dalla selezionabilità dei componenti per [*il backup*](vssgloss-s.md)e dalla struttura del percorso logico del writer (vedere Working [with Selectability for Backup](working-with-selectability-for-backup.md)).

Oltre ai file specificati nei componenti, un determinato writer può anche aver escluso in modo esplicito i file. L'esclusione di file deve essere sempre rispettata, indipendentemente dal componente selezionato.

Come illustrato in Panoramica della fase di individuazione del [backup,](overview-of-the-backup-discovery-phase.md)una cartella montata o un reparse point può essere visualizzato in una copia shadow ed è possibile eseguire il backup. Tuttavia, una cartella montata o un reparse point non può essere attraversata nel volume copiato shadow (vedere [Working with Mounted Folders and Reparse Points](working-with-reparse-and-mount-points.md)).

È necessario fare attenzione anche durante [](vssgloss-a.md) un'operazione di backup, se il percorso alternativo restituito da [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) non è vuoto. Un percorso alternativo è diverso da un [*mapping*](vssgloss-a.md) di percorso alternativo perché viene usato solo durante i backup, mentre un mapping di percorso alternativo viene usato solo durante i ripristini.

In questo caso, non è necessario eseguire il backup dei dati dalla posizione normale (indicata da [**IVssWMFiledesc::GetPath),**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)ma dalla posizione restituita da [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation). Al ripristino, il file deve essere ripristinato nella posizione normale. Per [altre informazioni, vedere Percorsi di backup e ripristino](non-default-backup-and-restore-locations.md) non predefiniti.

VsS non pone alcuna restrizione sul meccanismo effettivo di backup dei dati in un supporto di archiviazione o sulla scelta di tale supporto. È tuttavia consigliabile elaborare come unità i file di ogni componente di ogni istanza del [*writer.*](vssgloss-w.md) Per una descrizione delle procedure consigliate per la generazione [dell'elenco dei](generating-a-backup-set.md) file di backup, vedere Generazione di un set di backup.

L'esito positivo o negativo del backup di uno dei file gestiti da un determinato componente e (se definisce un [*set*](vssgloss-c.md)di componenti ) i relativi [*sottocomponenti*](vssgloss-s.md) per una determinata istanza del writer devono essere mantenuti nel documento dei componenti di backup chiamando [**IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded). Se non è possibile eseguire il backup di un file gestito da un componente o da un set di componenti, si dice che l'intero componente ha esito negativo. Le informazioni esatte sul file di cui non è stato possibile eseguire il backup devono essere sempre registrate.

Gli sviluppatori possono risultare utili per archiviare un record nei supporti di backup di cui viene eseguito il backup, i componenti e il set di componenti di cui erano membri, la specifica e i percorsi originali. Può anche essere utile archiviare informazioni come la definizione del componente di ogni writer. Questa operazione può semplificare l'operazione di recupero. Tuttavia, tali dettagli vengono lasciati allo sviluppatore richiedente.

Poiché i writer possono modificare il documento dei componenti di backup durante la gestione dell'evento [**PostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) generato dalla chiamata del richiedente [**a IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), il documento dei componenti di backup non deve essere salvato fino al termine della chiamata asincrona.

Anche se può verificarsi in precedenza, questo è anche un momento utile per salvare il documento di metadati del writer.

È molto importante mantenere sia il documento dei componenti di backup che i documenti dei metadati del writer usando [**IVssBackupComponents::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) e [**IVssExamineWriterMetadata::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml). In caso contrario, non sarà possibile usare vss durante il ripristino dei file.

Oltre a archiviare i metadati originali, alcune applicazioni di backup possono risultare utili per salvare una copia del proprio elenco di file (nel proprio formato ottimizzato) e le informazioni relative a scrittura, componente, procedura di ripristino e percorso associate, nei supporti di backup per un successivo recupero. Tale elenco può essere usato per evitare l'analisi e il confronto dei documenti di metadati del writer e dei documenti dei componenti di backup durante il ripristino.

I volumi di cui viene eseguito il backup possono contenere dati non gestiti da VSS writer. È possibile e necessario eseguire il backup di questi dati dal volume copiato shadow, in cui si trova in uno stato [*coerente con l'arresto anomalo del sistema.*](vssgloss-c.md) Per [altre informazioni, vedere Backup senza partecipazione](backups-without-writer-participation.md) al writer.

 

 





---
description: VSS consente a un richiedente di accedere alla copia shadow dei volumi contenenti dati per il backup e di copiare i dati nei supporti di backup.
ms.assetid: 187f26f2-f191-4703-9bde-3357f1ceef0c
title: Panoramica del backup effettivo dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29c4f2d4c0d43e614fe956b2ca3b3253566f0d05a7c27a4e7337ae3b2cd6784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056379"
---
# <a name="overview-of-actual-backup-of-files"></a>Panoramica del backup effettivo dei file

VSS consente a un richiedente di accedere alla copia shadow dei volumi contenenti dati per il backup e di copiare i dati nei supporti di backup. I writer in genere procedono con il normale funzionamento durante questo processo. Per altre informazioni, vedere [Panoramica dell'elaborazione di un backup in VSS.](overview-of-processing-a-backup-under-vss.md)

La tabella seguente illustra la sequenza di azioni ed eventi necessari per il backup dei file.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Azione richiedente</th>
<th>Evento</th>
<th>Azione writer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Accedere ai file nel volume copiato con shadowing (vedere <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties"><strong>IVssBackupComponents::GetSnapshotProperties</strong></a>, <a href="/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop"><strong>VSS_SNAPSHOT_PROP</strong></a>)</td>
<td>Nessuno</td>
<td>Nessuno</td>
</tr>
<tr class="even">
<td>Generare l'elenco di file di cui eseguire il backup e copiare i dati dei file nei supporti di backup.</td>
<td>Nessuno</td>
<td>Nessuno</td>
</tr>
<tr class="odd">
<td>Indicare l'esito positivo o negativo del backup <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded"><strong>con IVssBackupComponents::SetBackupSucceeded</strong></a>.</td>
<td>Nessuno</td>
<td>Nessuno</td>
</tr>
<tr class="even">
<td>Il richiedente indica che il backup è stato completato chiamando <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>IVssBackupComponents::BackupComplete</strong></a>.</td>
<td><a href="vssgloss-b.md"><em>BackupComplete</em></a></td>
<td>Eseguire qualsiasi pulizia post-backup (vedere <a href="/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete"><strong>CVssWriter::OnBackupComplete</strong></a>, <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents"><strong>IVssWriterComponents,</strong></a> <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent"><strong>IVssComponent</strong></a>).</td>
</tr>
<tr class="odd">
<td>Il richiedente attende che tutti i writer riconoscano la ricezione dell'evento <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>IVssBackupComponents::BackupComplete</strong></a> <a href="/windows/desktop/api/Vss/nn-vss-ivssasync"><strong>usando IVssAsync.</strong></a> Deve anche verificare lo stato del writer (vedere <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus"><strong>IVssBackupComponents::GatherWriterStatus</strong></a>, <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus"><strong>IVssBackupComponents::GetWriterStatus</strong></a>). Il richiedente deve chiamare <strong>GatherWriterStatus</strong> in questo momento per impostare la sessione del writer su uno stato completato.
<blockquote>
[!Note]<br />
Questa operazione è necessaria solo in Windows Server 2008 con Service Pack 2 (SP2) e versioni precedenti.
</blockquote>
<br/></td>
<td>Nessuno</td>
<td>Nessuno</td>
</tr>
<tr class="even">
<td>Salvare il documento dei componenti di backup e ogni documento di metadati del writer in documenti XML, che possono essere scritti nel supporto di backup (vedere <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml"><strong>IVssBackupComponents::SaveAsXML</strong></a> e <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml"><strong>IVssExamineWriterMetadata::SaveAsXML).</strong></a></td>
<td>Nessuno</td>
<td>Nessuno</td>
</tr>
</tbody>
</table>



 

## <a name="writer-actions-during-backup-of-files"></a>Azioni writer durante il backup dei file

Al termine della copia shadow, tutte le operazioni di I/O nel sistema di cui viene eseguito il backup dovrebbero essere in grado di riprendere senza interrompere l'integrità del backup. Questa è una delle motivazioni di base per avere la funzionalità di copia shadow.

Pertanto, come nella fase di individuazione (vedere Panoramica della fase di individuazione del [backup),](overview-of-the-backup-discovery-phase.md)i writer devono soddisfare poche richieste durante il backup dei file.

Al termine di un backup e dopo che un richiedente ha generato un evento [*BackupComplete,*](vssgloss-b.md) VSS chiamerà il metodo [**CVssWriter::OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) di ogni writer, un metodo virtuale che per impostazione predefinita restituisce **semplicemente TRUE.** Tuttavia, i writer possono eseguire l'override dell'implementazione predefinita ed eseguire azioni come la rimozione dei file temporanei rimanenti o [](vssgloss-e.md) usare l'interfaccia [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) con cui viene chiamato per controllare lo stato del backup di ognuno dei componenti inclusi in modo esplicito (e di qualsiasi [*set*](vssgloss-c.md) di componenti che potrebbero definire) recuperando l'oggetto [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) corrispondente. Il writer può quindi determinare e agire sull'esito positivo o negativo del backup chiamando [**IVssComponent:GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded). Il valore restituito da **IVssComponent:GetBackupSucceeded** sarà **TRUE** solo se è stato eseguito correttamente il backup di tutti i file inclusi in modo esplicito nel componente e di tutti i relativi [*sottocomponenti*](vssgloss-s.md) inclusi in modo [*implicito.*](vssgloss-i.md)

Al termine della chiamata a [**CVssWriter::OnBackupComplete,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) il richiedente deve chiamare [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (per ogni writer) un'ultima volta. La memoria dello stato della sessione del writer è una risorsa limitata e i writer devono infine riutilizzare gli stati della sessione. Questo passaggio contrassegna lo stato della sessione di backup del writer come completato e notifica a VSS che questo slot di sessione di backup può essere riutilizzato da un'operazione di backup successiva.

## <a name="requester-actions-during-backup-of-files"></a>Azioni del richiedente durante il backup dei file

Come illustrato in [Panoramica della fase](overview-of-the-backup-discovery-phase.md)di individuazione backup , non generare l'elenco effettivo dei file di cui eseguire il backup fino al completamento della copia shadow.

[*L'oggetto dispositivo*](vssgloss-d.md) corrispondente alla copia shadow di un determinato volume viene usato per ottenere l'accesso ai file nel volume shadow copiato al termine della copia shadow. L'oggetto dispositivo viene ottenuto [**dall'oggetto PROP VSS \_ SNAPSHOT \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) restituito da [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties). Ogni copia shadow di un set di copie shadow avrà un proprio oggetto dispositivo.

L'oggetto dispositivo e i percorsi ottenuti dalle specifiche del documento dei metadati del writer dei componenti vengono quindi usati per selezionare i file per il backup. Per altre informazioni, vedere Accesso del richiedente [ai dati copiati shadow.](requestor-access-to-shadow-copied-data.md)

I file che verranno inclusi nell'elenco di backup dipendono dalla natura del backup specifico, dalla selezione dei componenti per [*il backup*](vssgloss-s.md)e dalla struttura del percorso logico del writer (vedere Utilizzo della selezionabilità per [il backup](working-with-selectability-for-backup.md)).

Oltre ai file specificati nei componenti, un writer specificato può anche avere file esclusi in modo esplicito. L'esclusione dei file deve essere sempre rispettata, indipendentemente dal componente selezionato.

Come illustrato in Panoramica della fase di individuazione [del backup,](overview-of-the-backup-discovery-phase.md)una cartella montata o un reparse point può essere visualizzato in una copia shadow ed è possibile eseguire il backup. Tuttavia, non è possibile attraversare una cartella montata o un reparse point sul volume copiato in modo shadow (vedere Uso di cartelle montate [e reparse point).](working-with-reparse-and-mount-points.md)

È necessario fare attenzione anche durante un'operazione di backup, se il percorso alternativo [*restituito*](vssgloss-a.md) da [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) non è vuoto. Un percorso alternativo è diverso da un [*mapping*](vssgloss-a.md) di percorso alternativo in quanto viene usato solo durante i backup, mentre un mapping di percorso alternativo viene usato solo durante i ripristini.

In questo caso, non è necessario eseguire il backup dei dati dalla posizione normale (indicata da [**IVssWMFiledesc::GetPath),**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)ma dal percorso restituito da [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation). Al ripristino, il file deve essere ripristinato nella posizione normale. Per [altre informazioni, vedere Percorsi di backup e ripristino](non-default-backup-and-restore-locations.md) non predefiniti.

VSS non pone alcuna restrizione sul meccanismo effettivo di backup dei dati in un supporto di archiviazione o sulla scelta di tale supporto. È tuttavia consigliabile elaborare i file di ogni componente di ogni istanza del [*writer*](vssgloss-w.md) come unità. Per [una descrizione delle procedure consigliate](generating-a-backup-set.md) per la generazione dell'elenco dei file di backup, vedere Generazione di un set di backup.

L'esito positivo o negativo del backup di uno dei file gestiti da un determinato componente e (se definisce un [*set*](vssgloss-c.md)di componenti) i relativi [*sottocomponenti*](vssgloss-s.md) per una determinata istanza del writer devono essere mantenuti nel documento Componenti di backup chiamando [**IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded). Se il backup di un file gestito da un componente o da un set di componenti non riesce, si dice che l'intero componente avrà esito negativo. Le informazioni esatte sul file di cui non è stato eseguito il backup devono sempre essere registrate.

Gli sviluppatori possono trovare utile archiviare un record nel supporto di backup di cui viene eseguito il backup, i componenti e il set di componenti di cui erano membri, le specifiche e i percorsi originali. Può anche essere utile archiviare informazioni come la definizione del componente di ogni writer. Questa operazione può semplificare l'operazione di recupero. Tuttavia, tali dettagli vengono lasciati allo sviluppatore richiedente.

Poiché i writer possono modificare il documento dei componenti di backup durante la gestione dell'evento [**PostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) generato dalla chiamata del richiedente a [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), il documento dei componenti di backup non deve essere salvato fino al completamento della chiamata asincrona.

Anche se può verificarsi in precedenza, questo è anche un momento utile per salvare il documento dei metadati del writer.

È molto importante mantenere sia il documento dei componenti di backup che i documenti dei metadati del writer usando [**IVssBackupComponents::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) e [**IVssExamineWriterMetadata::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml). In caso contrario, non sarà possibile usare VSS durante il ripristino dei file.

Oltre a archiviare i metadati originali, alcune applicazioni di backup possono risultare utili per salvare una copia del proprio elenco dei file (nel proprio formato ottimizzato) e le informazioni relative a writer, componente, procedura di ripristino e percorso associate, nei supporti di backup per un successivo recupero. Tale elenco può essere usato per evitare l'analisi e il confronto dei documenti dei metadati del writer e dei documenti dei componenti di backup durante il ripristino.

I volumi di cui viene eseguito il backup possono avere dati non gestiti dai writer VSS. Questi dati possono e devono essere sottoposti a backup dal volume shadow copiato, in cui si trova in uno stato coerente [*con l'arresto anomalo del sistema.*](vssgloss-c.md) Per [altre informazioni, vedere Backup senza partecipazione](backups-without-writer-participation.md) al writer.

 

 





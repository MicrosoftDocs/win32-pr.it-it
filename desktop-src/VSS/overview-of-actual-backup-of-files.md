---
description: VSS consente a un richiedente di accedere alla copia shadow dei volumi contenenti i dati per il backup e di copiare i dati nei supporti di backup.
ms.assetid: 187f26f2-f191-4703-9bde-3357f1ceef0c
title: Panoramica del backup effettivo dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98a504ff5a41725e33a2eb27792a3c6c89d00276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310695"
---
# <a name="overview-of-actual-backup-of-files"></a>Panoramica del backup effettivo dei file

VSS consente a un richiedente di accedere alla copia shadow dei volumi contenenti i dati per il backup e di copiare i dati nei supporti di backup. In genere i writer procedono con il normale funzionamento durante questo processo. Per ulteriori informazioni, vedere [Cenni preliminari sull'elaborazione di un backup in VSS](overview-of-processing-a-backup-under-vss.md).

Nella tabella seguente viene illustrata la sequenza di azioni ed eventi necessari per i file di cui eseguire il backup.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Azione del richiedente</th>
<th>Evento</th>
<th>Azione del writer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Accedere ai file nel volume copiato Shadow (vedere <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties"><strong>IVssBackupComponents:: GetSnapshotProperties</strong></a>, <a href="/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop"><strong>VSS_SNAPSHOT_PROP</strong></a>)</td>
<td>nessuno</td>
<td>nessuno</td>
</tr>
<tr class="even">
<td>Generare l'elenco dei file di cui eseguire il backup e copiare i dati dei file nei supporti di backup.</td>
<td>nessuno</td>
<td>nessuno</td>
</tr>
<tr class="odd">
<td>Indicare l'esito positivo o negativo del backup con <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded"><strong>IVssBackupComponents:: SetBackupSucceeded</strong></a>.</td>
<td>nessuno</td>
<td>nessuno</td>
</tr>
<tr class="even">
<td>Il richiedente indica che il backup è stato completato chiamando <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>IVssBackupComponents:: BackupComplete</strong></a>.</td>
<td><a href="vssgloss-b.md"><em>BackupComplete</em></a></td>
<td>Eseguire una pulizia successiva al backup (vedere <a href="/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete"><strong>CVssWriter:: OnBackupComplete</strong></a>, <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents"><strong>IVssWriterComponents</strong></a>, <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent"><strong>IVssComponent</strong></a>).</td>
</tr>
<tr class="odd">
<td>Il richiedente attende che tutti i writer riconosca la ricezione dell'evento <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>IVssBackupComponents:: BackupComplete</strong></a> usando <a href="/windows/desktop/api/Vss/nn-vss-ivssasync"><strong>IVssAsync</strong></a>. Deve inoltre verificare lo stato del writer (vedere <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus"><strong>IVssBackupComponents:: GatherWriterStatus</strong></a>, <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus"><strong>IVssBackupComponents:: GetWriterStatus</strong></a>). Il richiedente deve chiamare <strong>GatherWriterStatus</strong> in questo momento per fare in modo che la sessione del writer venga impostata sullo stato completato.
<blockquote>
[!Note]<br />
Questa operazione è necessaria solo in Windows Server 2008 con Service Pack 2 (SP2) e versioni precedenti.
</blockquote>
<br/></td>
<td>nessuno</td>
<td>nessuno</td>
</tr>
<tr class="even">
<td>Salvare i componenti di backup documento e ogni documento di metadati del writer in documenti XML, che possono essere scritti nei supporti di backup (vedere <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml"><strong>IVssBackupComponents:: saveasxml</strong></a> e <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml"><strong>IVssExamineWriterMetadata:: saveasxml</strong></a>).</td>
<td>nessuno</td>
<td>nessuno</td>
</tr>
</tbody>
</table>



 

## <a name="writer-actions-during-backup-of-files"></a>Azioni del writer durante il backup dei file

Al termine della copia shadow, tutte le operazioni di I/O nel sistema di cui viene eseguito il backup dovrebbero essere in grado di riprendere senza compromettere l'integrità del backup. Questa è una delle motivazioni principali per avere la funzionalità copia shadow.

Pertanto, come nella fase di individuazione (vedere [Panoramica della fase di individuazione del backup](overview-of-the-backup-discovery-phase.md)), è possibile che vengano rilevate alcune richieste nei writer mentre è in corso il backup dei file.

Dopo che un backup è stato completato e un richiedente ha generato un evento [*BackupComplete*](vssgloss-b.md) , VSS chiamerà il metodo [**CVssWriter:: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) di ogni writer, un metodo virtuale che, per impostazione predefinita, restituisce semplicemente **true**. Tuttavia, i writer possono eseguire l'override dell'implementazione predefinita ed eseguire azioni come la rimozione dei file temporanei rimanenti oppure utilizzare l'interfaccia [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) con cui viene chiamata per verificare lo stato del backup di ognuno dei componenti [*inclusi in modo esplicito*](vssgloss-e.md) (e di qualsiasi [*set di componenti*](vssgloss-c.md) che potrebbero definire) recuperando l'oggetto [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) corrispondente. Il writer può quindi determinare e agire sull'esito positivo o negativo del backup chiamando [**IVssComponent: GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded). Il valore restituito da **IVssComponent: GetBackupSucceeded** sarà **true** solo se è stato eseguito il backup di tutti i file inclusi in modo esplicito nel componente e di tutti i relativi [*sottocomponenti*](vssgloss-s.md) inclusi in modo [*implicito*](vssgloss-i.md) .

Quando la chiamata a [**CVssWriter:: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) è stata completata, il richiedente deve chiamare [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (per ogni writer) un'ultima volta. La memoria dello stato della sessione del writer è una risorsa limitata e i writer devono riutilizzare gli Stati della sessione. Questo passaggio contrassegna lo stato della sessione di backup del writer come completato e notifica a VSS che questo slot della sessione di backup può essere riutilizzato da un'operazione di backup successiva.

## <a name="requester-actions-during-backup-of-files"></a>Azioni del richiedente durante il backup dei file

Come indicato nella [Panoramica della fase di individuazione del backup](overview-of-the-backup-discovery-phase.md), non è necessario generare l'elenco effettivo dei file di cui eseguire il backup finché la copia shadow non è stata completata.

L' [*oggetto dispositivo*](vssgloss-d.md) che corrisponde alla copia shadow di un determinato volume viene usato per ottenere l'accesso ai file nel volume copiato dall'ombreggiatura una volta completata la copia shadow. L'oggetto dispositivo viene ottenuto dall'oggetto [**\_ \_ prop dello snapshot VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) restituito da [**IVssBackupComponents:: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties). Ogni copia shadow di un set di copie shadow avrà un proprio oggetto dispositivo.

L'oggetto dispositivo e i percorsi ottenuti dalle specifiche dei documenti dei metadati del writer vengono quindi utilizzati per selezionare i file per il backup. Per ulteriori informazioni, vedere [richiesta di accesso ai dati copiati in Shadow](requestor-access-to-shadow-copied-data.md) .

I file che verranno inclusi nell'elenco di backup variano a seconda della natura del backup specifico, della selezione dei componenti [*per il backup*](vssgloss-s.md)e della struttura del percorso logico del writer. vedere Utilizzo della [selezione per il backup](working-with-selectability-for-backup.md).

Oltre ai file specificati nei componenti, è possibile che un determinato writer includa anche file esclusi in modo esplicito. L'esclusione di file deve sempre essere rispettata, indipendentemente dai componenti selezionati.

Come indicato nella [Panoramica della fase di individuazione del backup](overview-of-the-backup-discovery-phase.md), una cartella montata o un punto di analisi può essere visualizzato in una copia shadow ed è possibile eseguirne il backup. Tuttavia, non è possibile attraversare una cartella montata o un punto di analisi nel volume copiato in Shadow (vedere [uso di cartelle montate e reparse point](working-with-reparse-and-mount-points.md)).

È necessario prestare attenzione anche durante un'operazione di backup, se il [*percorso alternativo*](vssgloss-a.md) restituito da [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) non è vuoto. Un percorso alternativo è diverso da un [*mapping del percorso alternativo*](vssgloss-a.md) perché viene usato solo durante i backup, mentre un mapping del percorso alternativo viene usato solo durante i ripristini.

In questo caso, non è necessario eseguire il backup dei dati dal percorso normale (indicato da [**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), ma dal percorso restituito da [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation). Durante il ripristino, il file deve essere restituito al percorso normale. Per ulteriori informazioni, vedere [percorsi di backup e ripristino non predefiniti](non-default-backup-and-restore-locations.md) .

VSS non impone alcuna restrizione sul meccanismo effettivo di esecuzione del backup dei dati in un supporto di archiviazione o nella scelta del supporto. È tuttavia consigliabile che i file di ogni componente di ogni istanza di [*writer*](vssgloss-w.md) vengano elaborati come unità. Vedere [generazione di un set di backup](generating-a-backup-set.md) per una descrizione delle procedure consigliate per la generazione dell'elenco dei file di backup.

L'esito positivo o negativo del backup di uno dei file gestiti da un determinato componente e (se definisce un [*set di componenti*](vssgloss-c.md)) i relativi [*sottocomponenti*](vssgloss-s.md) per una determinata istanza di Writer devono essere conservati nel documento componenti di backup chiamando [**IVssBackupComponents:: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded). Se non è possibile eseguire il backup di un file gestito da un componente o da un set di componenti, viene detto che l'intero componente avrà esito negativo. Le informazioni esatte sul file di cui non è stato eseguito il backup devono sempre essere registrate.

Gli sviluppatori possono essere utili per archiviare un record sui supporti di backup di cui viene eseguito il backup dei file, i componenti e il set di componenti di cui sono membri, la loro specifica e i percorsi originali. Può anche essere utile archiviare informazioni come la definizione del componente di ogni writer. Questa operazione può rendere più semplice l'operazione di recupero. Tuttavia, tali dettagli vengono lasciati allo sviluppatore del richiedente.

Poiché i writer possono modificare il documento dei componenti di backup durante la gestione dell'evento post- [**snapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) generato dalla chiamata del richiedente a [**IVssBackupComponents::D Osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), il documento dei componenti di backup non deve essere salvato finché non viene completata la chiamata asincrona.

Sebbene possa essere eseguita in precedenza, questo è anche il momento opportuno per salvare il documento di metadati del writer.

È molto importante che sia il documento dei componenti di backup che i documenti dei metadati del writer vengano conservati usando [**IVssBackupComponents:: saveasxml**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) e [**IVssExamineWriterMetadata:: saveasxml**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml). In caso contrario, non sarà possibile utilizzare VSS durante il ripristino del file.

Oltre a archiviare i metadati originali, è possibile che alcune applicazioni di backup richiedano di salvare una copia del proprio elenco dei file (in un formato ottimizzato) e il writer, il componente, la procedura di ripristino e le informazioni sulla posizione associati al supporto di backup per un successivo recupero. Tale elenco può essere utilizzato per evitare l'analisi e il confronto dei documenti di metadati del writer e dei documenti del componente di backup durante il ripristino.

I volumi di cui viene eseguito il backup possono contenere dati non gestiti da writer VSS. È possibile eseguire il backup di questi dati dal volume copiato Shadow, in cui si troverà in uno [*stato coerente con l'arresto anomalo*](vssgloss-c.md)del sistema. Per ulteriori informazioni, vedere [backup senza partecipazione al writer](backups-without-writer-participation.md) .

 

 





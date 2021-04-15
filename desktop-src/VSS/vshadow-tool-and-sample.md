---
description: VShadow è uno strumento da riga di comando che è possibile utilizzare per creare e gestire copie shadow del volume.
ms.assetid: 19109f92-b9da-4df7-8628-374e37a3f624
title: Strumento VShadow ed esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7a9a697ecdf39f91d43fa0c66faebd37cfbfed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485028"
---
# <a name="vshadow-tool-and-sample"></a>Strumento VShadow ed esempio

VShadow è uno strumento da riga di comando che è possibile utilizzare per creare e gestire copie shadow del volume.

> [!Note]  
> VShadow è incluso in Microsoft Windows Software Development Kit (SDK) per Windows Vista e versioni successive. VSS 7,2 SDK include una versione di VShadow che viene eseguita solo in Windows Server 2003. Per informazioni sul download del Windows SDK e di VSS 7,2 SDK, vedere [servizio Copia Shadow del volume](volume-shadow-copy-service-portal.md).

 

Lo strumento VShadow utilizza opzioni della riga di comando e flag facoltativi per identificare le operazioni da eseguire. Quando viene usato senza alcuna opzione della riga di comando, il comando VShadow crea un nuovo set di copie shadow.

I comandi VShadow eseguono le operazioni seguenti:

-   [Creazione di un set di copie shadow](#creating-a-shadow-copy-set)
-   [Importazione di un set di copie shadow](#importing-a-shadow-copy-set)
-   [Esecuzione di query sulle proprietà della copia shadow](#querying-shadow-copy-properties)
-   [Eliminazione di copie shadow](#deleting-shadow-copies)
-   [Suddivisione di un set di copie shadow](#breaking-a-shadow-copy-set)
-   [Suddivisione di un set di copie shadow tramite il metodo BreakSnapshotSetEx](#breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method)
-   [Esposizione locale di una copia shadow](#exposing-a-shadow-copy-locally)
-   [Esposizione di una copia shadow in modalità remota](#exposing-a-shadow-copy-remotely)
-   [Elenco di metadati e stato del writer](#listing-writer-status-and-metadata)
-   [Esecuzione di operazioni di ripristino](#performing-restore-operations)
-   [Ripristino di una copia shadow precedente](#reverting-to-a-previous-shadow-copy)
-   [Risincronizzazione di lun](#resynchronizing-luns)

## <a name="creating-a-shadow-copy-set"></a>Creazione di un set di copie shadow

**vshadow** \[ \] *Volume* OptionalFlags

Questo comando crea un nuovo set di copie shadow.

*Volume* list è un elenco di nomi di volumi. VShadow crea una copia shadow per ogni volume presente nell'elenco. Facoltativamente, un nome di volume può terminare con una barra rovesciata ( \\ ). Ad esempio, C: e C: \\ sono nomi di volume validi. È inoltre possibile specificare le cartelle montate (ad esempio, C: \\ DirectoryName) o i nomi dei GUID del volume (ad esempio, \\ \\ ? \\ Volume {edbed95e-7e8d-11D8-9D01-505054503030}).

*OptionalFlags* è una maschera di maschera dei valori facoltativi dei flag della tabella seguente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore del flag facoltativo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong><br/></td>
<td>Questo flag facoltativo specifica le copie shadow dell'hardware differenziale. Questo flag e il flag <strong>-AP</strong> si escludono a vicenda.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-ap"></span><span id="-AP"></span><strong>-AP</strong><br/></td>
<td>Questo flag facoltativo specifica le copie shadow dell'hardware Plex. Questo flag e il flag <strong>-ad</strong> si escludono a vicenda.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span><strong></strong> <strong>-BC =</strong><em>file</em><strong>. XML</strong><br/></td>
<td>Questo flag facoltativo specifica le copie shadow non trasferibili e archivia nel file specificato il documento relativo ai componenti di backup. Questo file può essere utilizzato in un'operazione di ripristino successiva. Questo flag e il flag <strong>-t</strong> si escludono a vicenda.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-Exec =</strong><em>comando</em><br/></td>
<td>Questo flag facoltativo esegue un comando o uno script dopo la creazione delle copie shadow, ma prima che lo strumento VShadow venga chiuso. Il <em>comando</em> può specificare un comando della shell eseguibile o un file cmd. Se specifica un comando della shell, non è possibile specificare parametri di comando.<br/>
<blockquote>
[!Note]<br />
Per motivi di sicurezza e per semplificare l'implementazione, il flag facoltativo <strong>-Exec</strong> non accetterà parametri da passare al comando o allo script. L'intera stringa passata al flag facoltativo <strong>-Exec</strong> viene considerata come un singolo file cmd o exe. Per ulteriori informazioni su questa limitazione, vedere il codice sorgente di VShadow.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong><br/></td>
<td>Questo flag facoltativo specifica che l'operazione di copia shadow deve essere completata solo se è possibile ripristinare tutte le firme del disco.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows Server.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Non supportato.<br/></td>
</tr>
<tr class="even">
<td><span id="-mask"></span><span id="-MASK"></span><strong>-maschera</strong><br/></td>
<td>Questo flag facoltativo specifica che i LUN della copia shadow devono essere mascherati dal computer quando il set di copie shadow è danneggiato.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows Server.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Non supportato.<br/></td>
</tr>
<tr class="odd">
<td><span id="-nar"></span><span id="-NAR"></span><strong>-Nar</strong><br/></td>
<td>Questo flag facoltativo specifica le copie shadow senza ripristino automatico. Per ulteriori informazioni su questa opzione, vedere la documentazione relativa al flag di VSS_VOLSNAP_ATTR_NO_AUTORECOVERY dell'enumerazione <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-Revert</strong><br/></td>
<td>Questo flag facoltativo specifica che le firme del disco non devono essere ripristinate.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows Server.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Non supportato.<br/></td>
</tr>
<tr class="odd">
<td><span id="-nw"></span><span id="-NW"></span><strong>-NW</strong><br/></td>
<td>Questo flag facoltativo specifica le copie shadow senza coinvolgere i writer. Per ulteriori informazioni sulle copie shadow senza partecipazione del writer, vedere la pagina relativa ai <a href="shadow-copy-creation-details.md">Dettagli della creazione della copia shadow</a>. Questo flag e i flag <strong>-Wi</strong> e <strong>-WX</strong> si escludono a vicenda.<br/></td>
</tr>
<tr class="even">
<td><span id="-p"></span><span id="-P"></span><strong>-p</strong><br/></td>
<td>Questo flag facoltativo specifica le <a href="vssgloss-p.md"><em>copie shadow permanenti</em></a>.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-rw"></span><span id="-RW"></span><strong>-RW</strong><br/></td>
<td>Questo flag facoltativo specifica che i LUN della copia shadow devono essere resi di lettura/scrittura quando il set di copie shadow è danneggiato.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows Server.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Non supportato.<br/></td>
</tr>
<tr class="even">
<td><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong><br/></td>
<td>Questo flag facoltativo specifica le <a href="vssgloss-c.md"><em>copie shadow accessibili dal client</em></a>.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script =</strong><em>file</em><strong>. cmd</strong><br/></td>
<td>Questo flag facoltativo genera un file CMD contenente le variabili di ambiente correlate alle copie shadow create, ad esempio gli ID copia shadow e gli ID del set di copie shadow.<br/></td>
</tr>
<tr class="even">
<td><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t =</strong><em>file</em><strong>. XML</strong><br/></td>
<td>Questo flag facoltativo specifica le copie shadow trasportabili e archivia i componenti di backup del documento nel file specificato dal parametro <em>File.xml</em> . Questo file può essere utilizzato in un'operazione di importazione e/o ripristino successiva. Questo flag e il flag <strong>-BC</strong> si escludono a vicenda.<br/> <strong>Windows server 2003, Standard Edition e Windows server 2003, Web Edition:</strong> Le copie shadow trasportabili non sono supportate. Tutte le edizioni di Windows Server 2003 con Service Pack 1 (SP1) supportano le copie shadow trasportabili.<br/></td>
</tr>
<tr class="odd">
<td><span id="-tr"></span><span id="-TR"></span><strong>-TR</strong><br/></td>
<td>Questo flag facoltativo specifica che è necessario applicare il ripristino TxF durante la creazione della copia shadow.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows Server.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-tracing"></span><span id="-TRACING"></span><strong>-traccia</strong><br/></td>
<td>Questo flag facoltativo genera un output dettagliato che può essere utilizzato per la risoluzione dei problemi.<br/></td>
</tr>
<tr class="odd">
<td><span id="-wait"></span><span id="-WAIT"></span><strong>-attesa</strong><br/></td>
<td>Questo flag facoltativo fa in modo che lo strumento VShadow attenda la conferma dell'utente prima di uscire.<br/></td>
</tr>
<tr class="even">
<td><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-Wi =</strong><em>writer</em><br/></td>
<td>Questo flag facoltativo verifica che il writer o il componente specificato sia incluso nella copia shadow. Il <em>writer</em> può specificare un percorso componente, un nome di writer, un ID writer o un ID istanza writer. Questo flag e il flag <strong>-NW</strong> si escludono a vicenda.<br/></td>
</tr>
<tr class="odd">
<td><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-WX =</strong><em>writer</em><br/></td>
<td>Questo flag facoltativo verifica che il writer o il componente specificato venga escluso dalla copia shadow. Il <em>writer</em> può specificare un percorso componente, un nome di writer, un ID writer o un ID istanza writer. Questo flag e il flag <strong>-NW</strong> si escludono a vicenda.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="importing-a-shadow-copy-set"></a>Importazione di un set di copie shadow

**vshadow** \[ OptionalFlags \] **-i =**_file_*_. XML_*

L'opzione della riga di comando **-i** importa un set di copie shadow trasportabili.

> [!Note]  
> Questa opzione della riga di comando è supportata solo nei sistemi operativi Windows Server.

 

Il file di *File.xml* deve essere un file di documento dei componenti di backup per un set di copie shadow trasportabili creato con il flag facoltativo **-t** o **-BC** .

Un set di copie shadow è una [*Copia Shadow persistente*](vssgloss-p.md) se è stata creata con il flag **-p** facoltativo. Se il set di copie shadow trasportabili è non persistente, viene visualizzato per un breve periodo di tempo mentre il comando per la creazione della copia shadow è in esecuzione e viene eliminato automaticamente quando il comando restituisce un risultato. È possibile importare copie shadow non permanenti solo durante la creazione della copia shadow, creando il set di copie shadow usando il flag facoltativo **-Exec** per eseguire un file cmd che chiama vshadow **-i**.

Impossibile combinare l'opzione della riga di comando **-i** con altre opzioni della riga di comando.

*OptionalFlags* è una maschera di maschera dei valori facoltativi dei flag della tabella seguente.



| Valore del flag facoltativo                                                                                                            | Descrizione                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-Exec =**_comando_<br/> | Questo flag facoltativo esegue un comando o uno script dopo l'importazione delle copie shadow ma prima della chiusura dello Strumento VShadow. Il *comando* può specificare un comando della shell eseguibile o un file cmd. Se specifica un comando della shell, non è possibile specificare parametri di comando.<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-traccia**<br/>                                                  | Questo flag facoltativo genera un output dettagliato che può essere utilizzato per la risoluzione dei problemi.<br/>                                                                                                                                                                                 |
| <span id="-wait"></span><span id="-WAIT"></span>**-attesa**<br/>                                                           | Questo flag facoltativo fa in modo che lo strumento VShadow attenda la conferma dell'utente prima di uscire.<br/>                                                                                                                                                                          |



 

## <a name="querying-shadow-copy-properties"></a>Esecuzione di query sulle proprietà della copia shadow

**vshadow** **-q**

**vshadow** **-QX =**_ShadowCopySetId_

**vshadow** **-s =**_ShadowCopyId_

L'opzione della riga di comando **-q** elenca le proprietà di tutte le copie shadow nel computer.

L'opzione della riga di comando **-QX** elenca le proprietà di tutte le copie shadow nel set di copie shadow il cui ID è specificato da *ShadowCopySetId*.

L'opzione della riga di comando **-s** elenca le proprietà della copia shadow il cui ID è specificato da *ShadowCopyId*.

Queste opzioni della riga di comando usano una combinazione di [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) e [**IVssBackupComponents:: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) per ottenere le proprietà del set di copie shadow specificato.

Le opzioni della riga **di comando-q**, **-QX** e **-s** si escludono a vicenda e non possono essere combinate con altre opzioni della riga di comando.

## <a name="deleting-shadow-copies"></a>Eliminazione di copie shadow

**vshadow** **-da**

**vshadow** **-do**

**vshadow** **-DX =**_ShadowCopySetId_

**vshadow** **-DS =**_ShadowCopyId_

Il comando **-da** Elimina tutte le copie shadow nel computer.

> [!Note]  
> L'opzione della riga di comando **-da** richiede la conferma dell'utente.

 

L'opzione della riga di comando **-do** Elimina la copia shadow meno recente nel computer.

L'opzione della riga di comando **-dx** Elimina tutte le copie shadow nel set di copie shadow il cui ID è specificato da *ShadowCopySetId*.

L'opzione della riga di comando **-DS** Elimina la copia shadow il cui ID è specificato da *ShadowCopyId*.

Queste opzioni della riga di comando sono utilizzabili solo con [*copie shadow permanenti*](vssgloss-p.md) . Non è necessario eliminare in modo esplicito le copie shadow non permanenti perché vengono eliminate automaticamente al termine del comando di creazione VShadow.

Le opzioni della riga di comando **-da**, **-do**, **-DX** e **-DS** si escludono a vicenda e non possono essere combinate con altre opzioni della riga di comando.

## <a name="breaking-a-shadow-copy-set"></a>Suddivisione di un set di copie shadow

**vshadow** **-b =**_ShadowCopySetId_

**vshadow** **-BW =**_ShadowCopySetId_

L'opzione della riga di comando **-b =**_ShadowCopySetId_ converte ogni copia shadow nel set di copie shadow in un volume autonomo di sola lettura.

L'opzione della riga di comando **-BW =**_ShadowCopySetId_ converte ogni copia shadow nel set di copie shadow in un volume scrivibile autonomo.

> [!Note]  
> Le opzioni della riga di comando **-b** e **-BW** sono supportate solo nei sistemi operativi Windows Server.

 

Per informazioni su come suddividere un set di copie shadow, vedere [interruzioni di copie shadow](breaking-shadow-copies.md).

Dopo che il set di copie shadow è stato danneggiato, il set di copie shadow e le singole copie shadow non esistono più e non possono essere gestiti con i comandi VSS.

Un set di copie shadow è persistente se è stato creato con il flag **-p** facoltativo. Se il set di copie shadow trasportabili è non persistente, viene visualizzato per un breve periodo di tempo mentre il comando per la creazione della copia shadow è in esecuzione e viene eliminato automaticamente quando il comando restituisce un risultato. È possibile interrompere i set di copie shadow non permanenti solo durante la creazione della copia shadow, creando il set di copie shadow usando il flag **-Exec** facoltativo per eseguire un file cmd che chiama **vshadow** **-b** o **vshadow** **-BW**.

Le opzioni della riga di comando **-b** e **-BW** si escludono a vicenda e non possono essere combinate con altre opzioni della riga di comando.

## <a name="breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method"></a>Suddivisione di un set di copie shadow tramite il metodo BreakSnapshotSetEx

**vshadow** **-Bex**

L'opzione della riga di comando **-Bex** interrompe un set di copie shadow in base alle opzioni specificate dai flag facoltativi **-mask**, **-RW**, **-forcerevert** e **-Revert** . Questa opzione della riga di comando è simile alle opzioni della riga di comando **-b** e **-BW** . L'opzione della riga di comando **-Bex** usa il metodo [**IVssBackupComponentsEx2:: BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) , mentre le opzioni della riga di comando **-b** e **-BW** usano il metodo [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .

Per informazioni su come suddividere un set di copie shadow, vedere [interruzioni di copie shadow](breaking-shadow-copies.md).

> [!Note]  
> L'opzione della riga di comando **-Bex** è supportata solo nei sistemi operativi Windows Server.

 

**vshadow** **-Bex** **-mask**

Il flag **-mask** specifica che il lun della copia shadow verrà mascherato dall'host. Se viene specificato il flag **-mask** , non è possibile specificare i flag **-RW**, **-forcerevert** e **-Revert** .

**vshadow** **-Bex** **-RW**

Il flag **-RW** specifica che il lun della copia shadow verrà esposto all'host come volume di lettura/scrittura.

**vshadow** **-Bex** **-forcerevert**

Il flag **-forcerevert** specifica che gli identificatori del disco di tutti i LUN della copia shadow verranno ripristinati a quelli dei lun originali. Tuttavia, se uno dei lun originali è presente nel sistema, l'operazione avrà esito negativo e nessuno degli identificatori verrà ripristinato. Questo flag e il flag **-Revert** si escludono a vicenda.

**vshadow** **-Bex** **-Revert**

Il flag **-Revert** specifica che nessuno degli identificatori del disco lun della copia shadow verrà ripristinato. Questo flag e il flag **-forcerevert** si escludono a vicenda.

## <a name="exposing-a-shadow-copy-locally"></a>Esposizione locale di una copia shadow

**vshadow** **-El =**_ShadowCopyId_*_,_*_LocalEmptyDirectory_

 **vshadow** **-El =**_ShadowCopyId_*_,_*_UnusedDriveLetter_

L'opzione della riga di comando **-El** assegna una cartella montata o una lettera di unità a una copia shadow permanente. Si noti che il contenuto del volume resterà di sola lettura, a meno che non venga successivamente chiamato **vshadow** **-BW** per interrompere il set di copie shadow.

> [!Note]  
> Le copie shadow non permanenti e le [*copie shadow accessibili dal client*](vssgloss-c.md) non possono essere esposte localmente.

 

Se, ad esempio, {edbed95e-7e8d-11D8-9D01-505054503030} è il GUID di una copia shadow persistente esistente e X: è una lettera di unità inutilizzata, il comando seguente espone la copia shadow in X:

**vshadow** **-El = {edbed95e-7e8d-11D8-9D01-505054503030}, x:**

Nell'esempio seguente viene illustrato come esporre la stessa copia shadow nella cartella montata C: \\ ShadowCopies \\ June23:

**mkdir c: \\ ShadowCopies \\ June23**

**vshadow** **-El = {edbed95e-7e8d-11D8-9D01-505054503030}, c: \\ ShadowCopies \\ June23**

Non è possibile combinare l'opzione della riga di comando **-El** con altre opzioni della riga di comando.

## <a name="exposing-a-shadow-copy-remotely"></a>Esposizione di una copia shadow in modalità remota

**vshadow** **-er =**_ShadowCopyId_*_,_*_UnusedShareName_

 **vshadow** **-er =**_ShadowCopyId_*_,_*_UnusedShareName_*_,_*_PathFromRootOnShadow_

L'opzione della riga di comando **-er** assegna un nome di condivisione di sola lettura alla directory radice (o a una sottodirectory) dalla copia shadow. Si noti che il contenuto della condivisione rimarrà di sola lettura, a meno che non venga successivamente chiamato **vshadow** **-BW** per interrompere il set di copie shadow.

> [!Note]  
> Le [*copie shadow accessibili dal client*](vssgloss-c.md) non possono essere esposte in remoto.

 

Se, ad esempio, {edbed95e-7e8d-11D8-9D01-505054503030} è il GUID di una copia shadow persistente esistente e la condivisione \_ 123 è un nome di condivisione non usato, il comando seguente espone la copia shadow in share \_ 123:

**vshadow** **-er = {edbed95e-7e8d-11D8-9D01-505054503030}, condivisione \_ 123**

Nell'esempio seguente viene illustrato come esporre solo un sottoalbero (denominato "Folder1 \\ Cartella2") della stessa copia shadow nella stessa condivisione:

**vshadow** **-er = {edbed95e-7e8d-11D8-9D01-505054503030}, share \_ 123, Folder1 \\ Cartella2**

Non è possibile combinare l'opzione della riga di comando **-er** con altre opzioni della riga di comando.

## <a name="listing-writer-status-and-metadata"></a>Elenco di metadati e stato del writer

**vshadow** **-WS**

**vshadow** **-WM**

**vshadow** **-wm2**

**vshadow** **-WM3**

L'opzione della riga **di comando-WS** enumera i writer del servizio Copia Shadow del volume attualmente in esecuzione nel computer e ne descrive lo stato. Questo comando è l'equivalente del comando [vssadmin list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) . Esistono sei possibili valori di stato: stabile, non riuscito, sconosciuto, in attesa di blocco, bloccato e in attesa del completamento.

L'opzione della riga di comando **-WM** elenca un riepilogo dei metadati del writer, inclusi i volumi interessati.

L'opzione della riga di comando **-wm2** elenca tutti i metadati del writer.

L'opzione della riga di comando **-WM3** elenca tutti i metadati del writer in formato XML non elaborato.

**Windows Vista e Windows Server 2003:** L'opzione della riga di comando **-WM3** non è supportata.

È possibile utilizzare queste informazioni per determinare i volumi da includere nel set di copie shadow del volume.

> [!Note]  
> Se lo stato del writer è stabile o in attesa del completamento, è possibile considerare che il writer è in uno stato stabile, pronto per il backup successivo.

 

Le opzioni della riga **di comando-WS**, **-WM**, **-wm2** e **-WM3** si escludono a vicenda e non possono essere combinate con altre opzioni della riga di comando.

## <a name="performing-restore-operations"></a>Esecuzione di operazioni di ripristino

**vshadow** \[ OptionalFlags \] **-r =**_file_*_. XML_*

**vshadow** \[ OptionalFlags \] **-RS =**_file_*_. XML_*

L'opzione della riga di comando **-r** esegue un'operazione di ripristino.

L'opzione della riga di comando **-RS** esegue un'operazione di ripristino simulato.

Il file di *File.xml* deve essere un file di documento dei componenti di backup per un set di copie shadow creato con il flag facoltativo **-t** o **-BC** .

Le opzioni della riga di comando **-r** e **-RS** si escludono a vicenda e non possono essere combinate con altre opzioni della riga di comando.

*OptionalFlags* è una maschera di maschera dei valori facoltativi dei flag della tabella seguente.



| Valore del flag facoltativo                                                                                                            | Descrizione                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-Wi =**_writer_<br/>             | Questo flag facoltativo verifica che il writer o il componente specificato sia incluso nel ripristino. Il *writer* può specificare un percorso componente, un nome di writer, un ID writer o un ID istanza writer.<br/>                                                                                    |
| <span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-WX =**_writer_<br/>             | Questo flag facoltativo verifica che il writer o il componente specificato venga escluso dal ripristino. Il *writer* può specificare un percorso componente, un nome di writer, un ID writer o un ID istanza writer.<br/>                                                                                  |
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-Exec =**_comando_<br/> | Questo flag facoltativo esegue un comando o uno script tra gli eventi di pre-ripristino e post-ripristino inviati ai writer. Il *comando* può specificare un comando della shell eseguibile o un file cmd. Se specifica un comando della shell, non è possibile specificare parametri di comando.<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-traccia**<br/>                                                  | Questo flag facoltativo genera un output dettagliato che può essere utilizzato per la risoluzione dei problemi.<br/>                                                                                                                                                                                       |



 

## <a name="reverting-to-a-previous-shadow-copy"></a>Ripristino di una copia shadow precedente

**vshadow** **-Revert =**_ShadowCopyId_

> [!Note]  
> Questa opzione della riga di comando è supportata solo nei sistemi operativi Windows Server.

 

**Windows server 2008 e Windows server 2003:** Non supportato.

L'opzione **-Revert** Command-line ripristina un volume alla precedente copia shadow il cui ID è specificato da *ShadowCopyId*.

Impossibile combinare l'opzione **-Revert** dalla riga di comando con altre opzioni della riga di comando.

## <a name="resynchronizing-luns"></a>Risincronizzazione di lun

**vshadow** **-addresync =**_ShadowCopyId_ **-Resync =**_BCDFileName_ \[ OptionalResyncFlags\]

**vshadow** **-addresync =**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-Resync =**_BCDFileName_ \[ OptionalResyncFlags\]

L'opzione della riga di comando **-addresync** specifica i volumi da includere in un'operazione di risincronizzazione LUN. Il parametro *ShadowCopyId* specifica l'identificatore della copia shadow. Il parametro facoltativo *TargetVolumeDriveLetter* specifica il volume di destinazione in cui deve essere copiato il contenuto del volume della copia shadow.

L'opzione della riga di comando **-Resync** avvia un'operazione di risincronizzazione LUN. Al termine dell'operazione, la firma di ogni LUN di destinazione deve essere identica a quella del LUN del volume di destinazione. Il parametro *BCDFileName* specifica il nome del file XML che contiene il documento del componente di backup.

> [!Note]  
> Le opzioni della riga di comando **-addresync** e **-Resync** sono supportate solo nei sistemi operativi Windows Server.

 

**Windows server 2008 e Windows server 2003:** Non supportato.

*OptionalResyncFlags* è una maschera di maschera dei valori facoltativi dei flag della tabella seguente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore del flag facoltativo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong><br/></td>
<td>Questo flag facoltativo specifica che, al termine dell'operazione, la firma di ogni LUN di destinazione deve essere identica a quella del LUN originale utilizzato per creare la copia shadow, non il LUN del volume di destinazione.<br/>
<blockquote>
[!Note]<br />
Il flag <strong>-revertsig</strong> è supportato solo nei sistemi operativi Windows Server.
</blockquote>
<br/> <strong>Windows server 2008 e Windows server 2003:</strong> Non supportato.<br/></td>
</tr>
<tr class="even">
<td><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong><br/></td>
<td>Questo flag facoltativo specifica che il servizio VSS non deve verificare la presenza di volumi non selezionati che verrebbero sovrascritti dall'operazione di risincronizzazione LUN.<br/>
<blockquote>
[!Note]<br />
Il flag <strong>-novolcheck</strong> è supportato solo nei sistemi operativi Windows Server.
</blockquote>
<br/> <strong>Windows server 2008 e Windows server 2003:</strong> Non supportato.<br/></td>
</tr>
</tbody>
</table>



 

 

 

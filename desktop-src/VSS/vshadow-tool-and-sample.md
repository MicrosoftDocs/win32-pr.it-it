---
description: VShadow è uno strumento da riga di comando che è possibile usare per creare e gestire copie shadow del volume.
ms.assetid: 19109f92-b9da-4df7-8628-374e37a3f624
title: Strumento e esempio VShadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 306d759d10875b03cb0d2e4e2064a85614400ff5240800da3fc4c1ce94add8c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998071"
---
# <a name="vshadow-tool-and-sample"></a>Strumento e esempio VShadow

VShadow è uno strumento da riga di comando che è possibile usare per creare e gestire copie shadow del volume.

> [!Note]  
> VShadow è incluso in Microsoft Windows Software Development Kit (SDK) per Windows Vista e versioni successive. VSS 7.2 SDK include una versione di VShadow che viene eseguita solo in Windows Server 2003. Per informazioni sul download di Windows SDK e VSS 7.2 SDK, vedere [Servizio Copia Shadow del volume](volume-shadow-copy-service-portal.md).

 

Lo strumento VShadow usa opzioni della riga di comando e flag facoltativi per identificare il lavoro da eseguire. Se usato senza opzioni della riga di comando, il comando VShadow crea un nuovo set di copie shadow.

I comandi di VShadow eseguono le operazioni seguenti:

-   [Creazione di un set di copie shadow](#creating-a-shadow-copy-set)
-   [Importazione di un set di copie shadow](#importing-a-shadow-copy-set)
-   [Esecuzione di query su proprietà della copia shadow](#querying-shadow-copy-properties)
-   [Eliminazione di copie shadow](#deleting-shadow-copies)
-   [Interruzione di un set di copie shadow](#breaking-a-shadow-copy-set)
-   [Interruzione di un set di copie shadow tramite il metodo BreakSnapshotSetEx](#breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method)
-   [Esposizione di una copia shadow in locale](#exposing-a-shadow-copy-locally)
-   [Esposizione di una copia shadow in remoto](#exposing-a-shadow-copy-remotely)
-   [Elenco dello stato e dei metadati del writer](#listing-writer-status-and-metadata)
-   [Esecuzione di operazioni di ripristino](#performing-restore-operations)
-   [Ripristino di una copia shadow precedente](#reverting-to-a-previous-shadow-copy)
-   [Risincronizzazione dei LUN](#resynchronizing-luns)

## <a name="creating-a-shadow-copy-set"></a>Creazione di un set di copie shadow

**vshadow** \[ OptionalFlags \] *VolumeList*

Questo comando crea un nuovo set di copie shadow.

*VolumeList è* un elenco di nomi di volume. VShadow crea una copia shadow per ogni volume nell'elenco. Un nome di volume può facoltativamente terminare con una barra rovesciata ( \\ ). Ad esempio, sia C: che C: \\ sono nomi di volume validi. È anche possibile specificare le cartelle montate (ad esempio, C: Nome Directory) o i nomi GUID del \\ volume (ad esempio, \\ \\ ? \\ Volume{edbed95e-7e8d-11d8-9d01-505054503030}).

*OptionalFlags è* una maschera di bit di valori flag facoltativi della tabella seguente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore flag facoltativo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong><br/></td>
<td>Questo flag facoltativo specifica copie shadow hardware differenziali. Questo flag e il flag <strong>-ap</strong> si escludono a vicenda.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows server.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-ap"></span><span id="-AP"></span><strong>-ap</strong><br/></td>
<td>Questo flag facoltativo specifica copie shadow hardware plex. Questo flag e il flag <strong>-ad</strong> si escludono a vicenda.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows server.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span><strong></strong> <strong>-bc=</strong><em>File</em> <strong>.xml</strong><br/></td>
<td>Questo flag facoltativo specifica copie shadow non trasportabili e archivia il documento dei componenti di backup nel file specificato. Questo file può essere usato in un'operazione di ripristino successiva. Questo flag e il flag <strong>-t</strong> si escludono a vicenda.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows server.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec=</strong><em>Comando</em><br/></td>
<td>Questo flag facoltativo esegue un comando o uno script dopo la creazione delle copie shadow, ma prima della chiusura dello strumento VShadow. <em>Il comando</em> può specificare un comando della shell eseguibile o un file CMD. Se specifica un comando della shell, non è possibile specificare parametri di comando.<br/>
<blockquote>
[!Note]<br />
Per motivi di sicurezza e per mantenere semplice l'implementazione, il flag facoltativo <strong>-exec</strong> non accetta parametri da passare al comando o allo script. L'intera stringa passata al flag <strong>facoltativo -exec</strong> viene considerata come un singolo file CMD o EXE. Per altre informazioni su questa limitazione, vedere il codice sorgente di VShadow.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong><br/></td>
<td>Questo flag facoltativo specifica che l'operazione di copia shadow deve essere completata solo se è possibile ripristinare tutte le firme del disco.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows server.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Non supportato.<br/></td>
</tr>
<tr class="even">
<td><span id="-mask"></span><span id="-MASK"></span><strong>-mask</strong><br/></td>
<td>Questo flag facoltativo specifica che i LUN della copia shadow devono essere mascherati dal computer quando il set di copie shadow viene interrotto.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows server.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Non supportato.<br/></td>
</tr>
<tr class="odd">
<td><span id="-nar"></span><span id="-NAR"></span><strong>-nar</strong><br/></td>
<td>Questo flag facoltativo specifica le copie shadow senza ripristino automatico. Per altre informazioni su questa opzione, vedere la documentazione relativa al flag VSS_VOLSNAP_ATTR_NO_AUTORECOVERY <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>dell'enumerazione _VSS_VOLUME_SNAPSHOT_ATTRIBUTES.</strong></a><br/></td>
</tr>
<tr class="even">
<td><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong><br/></td>
<td>Questo flag facoltativo specifica che le firme del disco non devono essere ripristinate.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows server.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Non supportato.<br/></td>
</tr>
<tr class="odd">
<td><span id="-nw"></span><span id="-NW"></span><strong>-nw</strong><br/></td>
<td>Questo flag facoltativo specifica le copie shadow senza coinvolgere i writer. Per altre informazioni sulle copie shadow senza partecipazione al writer, vedere <a href="shadow-copy-creation-details.md">Dettagli di creazione della copia shadow.</a> Questo flag e i <strong>flag -wi</strong> <strong>e -wx</strong> si escludono a vicenda.<br/></td>
</tr>
<tr class="even">
<td><span id="-p"></span><span id="-P"></span><strong>-p</strong><br/></td>
<td>Questo flag facoltativo specifica <a href="vssgloss-p.md"><em>copie shadow persistenti.</em></a><br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows server.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-rw"></span><span id="-RW"></span><strong>-rw</strong><br/></td>
<td>Questo flag facoltativo specifica che i LUN della copia shadow devono essere resi di lettura/scrittura quando il set di copie shadow viene interrotto.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows server.
</blockquote>
<br/> <strong>Windows Server 2003:</strong> Non supportato.<br/></td>
</tr>
<tr class="even">
<td><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong><br/></td>
<td>Questo flag facoltativo specifica <a href="vssgloss-c.md"><em>le copie shadow accessibili dal client.</em></a><br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows server.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script=</strong><em>File</em><strong>.cmd</strong><br/></td>
<td>Questo flag facoltativo genera un file CMD contenente le variabili di ambiente correlate alle copie shadow create, ad esempio gli ID copia shadow e gli ID del set di copie shadow.<br/></td>
</tr>
<tr class="even">
<td><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t=</strong><em>File</em> <strong>.xml</strong><br/></td>
<td>Questo flag facoltativo specifica le copie shadow trasportabili e archivia il documento dei componenti di backup nel file specificato dal <em>parametroFile.xml.</em> Questo file può essere usato in un'operazione di importazione e/o ripristino successiva. Questo flag e il flag <strong>-bc</strong> si escludono a vicenda.<br/> <strong>Windows Server 2003, edizione Standard e Windows Server 2003, Web Edition:</strong> Le copie shadow trasportabili non sono supportate. Tutte le edizioni di Windows Server 2003 con Service Pack 1 (SP1) supportano le copie shadow trasportabili.<br/></td>
</tr>
<tr class="odd">
<td><span id="-tr"></span><span id="-TR"></span><strong>-tr</strong><br/></td>
<td>Questo flag facoltativo specifica che il ripristino TxF deve essere applicato durante la creazione della copia shadow.<br/>
<blockquote>
[!Note]<br />
Questo flag è supportato solo nei sistemi operativi Windows server.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="-tracing"></span><span id="-TRACING"></span><strong>-tracing</strong><br/></td>
<td>Questo flag facoltativo genera un output dettagliato che può essere usato per la risoluzione dei problemi.<br/></td>
</tr>
<tr class="odd">
<td><span id="-wait"></span><span id="-WAIT"></span><strong>-wait</strong><br/></td>
<td>Questo flag facoltativo fa sì che lo strumento VShadow attenda la conferma dell'utente prima di uscire.<br/></td>
</tr>
<tr class="even">
<td><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-wi=</strong><em>Writer</em><br/></td>
<td>Questo flag facoltativo verifica che il writer o il componente specificato sia incluso nella copia shadow. <em>Writer</em> può specificare un percorso del componente, il nome del writer, l'ID writer o l'ID istanza del writer. Questo flag e il flag <strong>-nw</strong> si escludono a vicenda.<br/></td>
</tr>
<tr class="odd">
<td><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-wx=</strong><em>Writer</em><br/></td>
<td>Questo flag facoltativo verifica che il writer o il componente specificato sia escluso dalla copia shadow. <em>Writer</em> può specificare un percorso del componente, il nome del writer, l'ID writer o l'ID istanza del writer. Questo flag e il flag <strong>-nw</strong> si escludono a vicenda.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="importing-a-shadow-copy-set"></a>Importazione di un set di copie shadow

**vshadow** \[ OptionalFlags \] **-i=**_File_ *_.xml_*

L'opzione della riga di comando **-i** importa un set di copie shadow trasportabili.

> [!Note]  
> Questa opzione della riga di comando è supportata solo nei Windows server.

 

Il *File.xml* file deve essere un file di documento dei componenti di backup per un set di copie shadow trasportabili creato con il flag facoltativo **-t** o **-bc.**

Un set di copie shadow è [*una copia shadow permanente*](vssgloss-p.md) se è stato creato con il flag **facoltativo -p.** Se il set di copie shadow trasportabili non è permanente, viene visualizzato per un breve periodo di tempo durante l'esecuzione del comando di creazione della copia shadow e viene eliminato automaticamente al termine del comando. È possibile importare copie shadow non costanti solo durante la creazione della copia shadow creando il set di copie shadow usando il flag facoltativo **-exec** per eseguire un file CMD che chiama VShadow **-i**.

L'opzione della riga di comando **-i** non può essere combinata con altre opzioni della riga di comando.

*OptionalFlags* è una maschera di bit di valori flag facoltativi della tabella seguente.



| Valore flag facoltativo                                                                                                            | Descrizione                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Comando_<br/> | Questo flag facoltativo esegue un comando o uno script dopo l'importazione delle copie shadow, ma prima della chiusura dello strumento VShadow. *Il comando* può specificare un comando della shell eseguibile o un file CMD. Se specifica un comando della shell, non è possibile specificare parametri di comando.<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-tracing**<br/>                                                  | Questo flag facoltativo genera un output dettagliato che può essere usato per la risoluzione dei problemi.<br/>                                                                                                                                                                                 |
| <span id="-wait"></span><span id="-WAIT"></span>**-wait**<br/>                                                           | Questo flag facoltativo fa sì che lo strumento VShadow attenda la conferma dell'utente prima di uscire.<br/>                                                                                                                                                                          |



 

## <a name="querying-shadow-copy-properties"></a>Esecuzione di query su proprietà della copia shadow

**vshadow** **-q**

**vshadow** **-qx=**_ShadowCopySetId_

**vshadow** **-s=**_ShadowCopyId_

L'opzione della riga di comando **-q** elenca le proprietà di tutte le copie shadow nel computer.

L'opzione della riga di comando **-qx** elenca le proprietà di tutte le copie shadow nel set di copie shadow il cui ID è specificato da *ShadowCopySetId*.

L'opzione della riga di comando **-s** elenca le proprietà della copia shadow il cui ID è specificato da *ShadowCopyId*.

Queste opzioni della riga di comando usano una combinazione [**di IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) e [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) per ottenere le proprietà del set specificato di copie shadow.

Le opzioni della riga di comando **-q**, **-qx** e **-s** si escludono a vicenda e non possono essere combinate con altre opzioni della riga di comando.

## <a name="deleting-shadow-copies"></a>Eliminazione di copie shadow

**vshadow** **-da**

**vshadow** **-do**

**vshadow** **-dx=**_ShadowCopySetId_

**vshadow** **-ds=**_ShadowCopyId_

Il **comando -da** elimina tutte le copie shadow nel computer.

> [!Note]  
> L'opzione della riga di comando **-da** richiede la conferma dell'utente.

 

L'opzione della riga di comando **-do** elimina la copia shadow meno recente nel computer.

L'opzione della riga di comando **-dx** elimina tutte le copie shadow nel set di copie shadow il cui ID è specificato da *ShadowCopySetId*.

L'opzione della riga di comando **-ds** elimina la copia shadow il cui ID è specificato da *ShadowCopyId*.

Queste opzioni della riga di comando possono essere usate solo con [*copie shadow permanenti.*](vssgloss-p.md) Le copie shadow non permanente non devono essere eliminate in modo esplicito, perché vengono eliminate automaticamente alla chiusura del comando di creazione di VShadow.

Le opzioni della riga di comando **-da**, **-do**, **-dx** e **-ds** si escludono a vicenda e non possono essere combinate con altre opzioni della riga di comando.

## <a name="breaking-a-shadow-copy-set"></a>Interruzione di un set di copie shadow

**vshadow** **-b=**_ShadowCopySetId_

**vshadow** **-bw=**_ShadowCopySetId_

L'opzione della riga di comando **-b=**_ShadowCopySetId_ converte ogni copia shadow nel set di copie shadow in un volume autonomo di sola lettura.

L'opzione della riga di comando **-bw=**_ShadowCopySetId_ converte ogni copia shadow nel set di copie shadow in un volume scrivibile autonomo.

> [!Note]  
> Le **opzioni della riga** di comando **-b e -bw** sono supportate solo nei Windows server.

 

Per informazioni sull'interruzione di un set di copie shadow, vedere [Breaking Shadow Copies](breaking-shadow-copies.md).

Dopo che il set di copie shadow è stato interrotto, il set di copie shadow e le singole copie shadow non esistono più e non possono essere gestiti tramite i comandi di Vss.

Un set di copie shadow è persistente se è stato creato con il flag **facoltativo -p.** Se il set di copie shadow trasportabili non è permanente, viene visualizzato per un breve periodo di tempo durante l'esecuzione del comando di creazione della copia shadow e viene eliminato automaticamente al termine del comando. È possibile interrompere i set di copie shadow non costanti solo durante la creazione della copia shadow creando il set di copie shadow usando il flag facoltativo **-exec** per eseguire un file CMD che chiama **vshadow** **-b** o **vshadow** **-bw**.

Le **opzioni della riga** di comando **-b e -bw** si escludono a vicenda e non possono essere combinate con altre opzioni della riga di comando.

## <a name="breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method"></a>Interruzione di un set di copie shadow tramite il metodo BreakSnapshotSetEx

**vshadow** **-bex**

L'opzione della riga di comando **-bex** interrompe un set di copie shadow in base alle opzioni specificate dai flag **facoltativi -mask**, **-rw**, **-forcerevert** e **-norevert.** Questa opzione della riga di comando è simile alle **opzioni della** riga di comando **-b e -bw.** L'opzione della riga di comando **-bex** usa il metodo [**IVssBackupComponentsEx2::BreakSnapshotSetEx,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) mentre le opzioni della riga di comando **-b** **e -bw** usano il metodo [**IVssBackupComponents::BreakSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)

Per informazioni sull'interruzione di un set di copie shadow, vedere [Breaking Shadow Copies](breaking-shadow-copies.md).

> [!Note]  
> L'opzione della riga di comando **-bex** è supportata solo nei Windows server.

 

**vshadow** **-bex** **-mask**

Il **flag -mask** specifica che il LUN della copia shadow verrà mascherato dall'host. Se viene specificato il flag **-mask,** non è possibile specificare i flag **-rw**, **-forcerevert** e **-norevert.**

**vshadow** **-bex** **-rw**

Il **flag -rw** specifica che il LUN della copia shadow verrà esposto all'host come volume di lettura/scrittura.

**vshadow** **-bex** **-forcerevert**

Il flag **-forcerevert** specifica che gli identificatori di disco di tutti i LUN della copia shadow verranno ripristinati a quello dei LUN originali. Tuttavia, se uno dei LUN originali è presente nel sistema, l'operazione avrà esito negativo e nessuno degli identificatori verrà ripristinato. Questo flag e il flag **-norevert** si escludono a vicenda.

**vshadow** **-bex** **-norevert**

Il **flag -norevert** specifica che nessuno degli identificatori del disco LUN della copia shadow verrà ripristinato. Questo flag e il flag **-forcerevert** si escludono a vicenda.

## <a name="exposing-a-shadow-copy-locally"></a>Esposizione di una copia shadow in locale

**vshadow** **-el=**_ShadowCopyId,_**_LocalEmptyDirectory_

 **vshadow** **-el=**_ShadowCopyId,_**_UnusedDriveLetter_

L'opzione della riga di comando **-el** assegna una cartella montata o una lettera di unità a una copia shadow permanente. Si noti che il contenuto del volume rimarrà di sola lettura a meno che non si chiami successivamente **vshadow** **-bw** per interrompere il set di copie shadow.

> [!Note]  
> Le copie shadow non disposte e le [*copie shadow*](vssgloss-c.md) accessibili dal client non possono essere esposte in locale.

 

Ad esempio, se {edbed95e-7e8d-11d8-9d01-505054503030} è il GUID di una copia shadow permanente esistente e X: è una lettera di unità inutilizzata, il comando seguente espone la copia shadow in X:

**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},x:**

L'esempio seguente illustra come esporre la stessa copia shadow nella cartella montata C: \\ ShadowCopies \\ June23:

**mkdir c: \\ ShadowCopies \\ June23**

**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},c: \\ ShadowCopies \\ June23**

L'opzione della riga di comando **-el** non può essere combinata con altre opzioni della riga di comando.

## <a name="exposing-a-shadow-copy-remotely"></a>Esposizione di una copia shadow in remoto

**vshadow** **-er=**_ShadowCopyId,_**_UnusedShareName_

 **vshadow** **-er=**_ShadowCopyId,_**_UnusedShareName,_**_PathFromRootOnShadow_

L'opzione della riga di comando **-er** assegna un nome di condivisione di sola lettura alla directory radice (o a una sottodirectory) dalla copia shadow. Si noti che il contenuto della condivisione rimarrà di sola lettura a meno che non si chiami successivamente **vshadow** **-bw** per interrompere il set di copie shadow.

> [!Note]  
> [*Le copie shadow accessibili dal client non*](vssgloss-c.md) possono essere esposte in modalità remota.

 

Ad esempio, se {edbed95e-7e8d-11d8-9d01-505054503030} è il GUID di una copia shadow permanente esistente e la condivisione 123 è un nome di condivisione non usato, il comando seguente espone la copia shadow nella condivisione \_ \_ 123:

**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share \_ 123**

L'esempio seguente illustra come esporre solo un sottoalbero (denominato "Cartella1 Folder2") della stessa \\ copia shadow nella stessa condivisione:

**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share \_ 123,Folder1 \\ Folder2**

L'opzione della riga di comando **-er** non può essere combinata con altre opzioni della riga di comando.

## <a name="listing-writer-status-and-metadata"></a>Elenco dello stato e dei metadati del writer

**vshadow** **-ws**

**vshadow** **-wm**

**vshadow** **-wm2**

**vshadow** **-wm3**

L'opzione della riga di comando **-ws** enumera i writer VSS attualmente in esecuzione nel computer e ne descrive lo stato. Questo comando equivale al comando [Vssadmin list writers.](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) Sono disponibili sei valori di stato possibili: Stabile, Non riuscito, Sconosciuto, In attesa di blocco, Bloccato e In attesa del completamento.

L'opzione della riga di comando **-wm** elenca un riepilogo dei metadati del writer, inclusi i volumi interessati.

L'opzione della riga di **comando -wm2** elenca tutti i metadati del writer.

L'opzione della riga di comando **-wm3** elenca tutti i metadati del writer in formato XML non elaborato.

**Windows Vista e Windows Server 2003:** L'opzione della riga di comando **-wm3** non è supportata.

È possibile usare queste informazioni per determinare i volumi da includere nel set di copie shadow del volume.

> [!Note]  
> Se lo stato del writer è Stabile o In attesa del completamento, il writer può essere considerato stabile, pronto per il backup successivo.

 

Le opzioni della riga di comando **-ws**, **-wm**, **-wm2** e **-wm3** si escludono a vicenda e non possono essere combinate con altre opzioni della riga di comando.

## <a name="performing-restore-operations"></a>Esecuzione di operazioni di ripristino

**vshadow** \[ OptionalFlags \] **-r=**_File_ *_.xml_*

**vshadow** \[ OptionalFlags \] **-rs=**_File_ *_.xml_*

L'opzione della riga di comando **-r** esegue un'operazione di ripristino.

L'opzione della riga di comando **-rs** esegue un'operazione di ripristino simulata.

Il *File.xml* file deve essere un file di documento dei componenti di backup per un set di copie shadow creato con il flag facoltativo **-t** o **-bc.**

Le opzioni della riga di comando **-r** e **-rs** si escludono a vicenda e non possono essere combinate con altre opzioni della riga di comando.

*OptionalFlags* è una maschera di bit di valori flag facoltativi della tabella seguente.



| Valore flag facoltativo                                                                                                            | Descrizione                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-wi=**_Writer_<br/>             | Questo flag facoltativo verifica che il writer o il componente specificato sia incluso nel ripristino. *Writer* può specificare un percorso del componente, il nome del writer, l'ID writer o l'ID istanza del writer.<br/>                                                                                    |
| <span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-wx=**_Writer_<br/>             | Questo flag facoltativo verifica che il writer o il componente specificato sia escluso dal ripristino. *Writer* può specificare un percorso del componente, il nome del writer, l'ID writer o l'ID istanza del writer.<br/>                                                                                  |
| <span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Comando_<br/> | Questo flag facoltativo esegue uno script o un comando tra gli eventi pre-ripristino e post-ripristino inviati ai writer. *Il comando* può specificare un comando della shell eseguibile o un file CMD. Se specifica un comando della shell, non è possibile specificare parametri di comando.<br/> |
| <span id="-tracing"></span><span id="-TRACING"></span>**-tracing**<br/>                                                  | Questo flag facoltativo genera un output dettagliato che può essere usato per la risoluzione dei problemi.<br/>                                                                                                                                                                                       |



 

## <a name="reverting-to-a-previous-shadow-copy"></a>Ripristino di una copia shadow precedente

**vshadow** **-revert=**_ShadowCopyId_

> [!Note]  
> Questa opzione della riga di comando è supportata solo nei sistemi Windows server.

 

**Windows Server 2008 e Windows Server 2003:** Non supportato.

L'opzione della riga di comando **-revert** ripristina un volume alla copia shadow precedente il cui ID è specificato da *ShadowCopyId*.

L'opzione della riga di comando **-revert** non può essere combinata con altre opzioni della riga di comando.

## <a name="resynchronizing-luns"></a>Risincronizzazione dei LUN

**vshadow** **-addresync=**_ShadowCopyId_ **-resync=**_BCDFileName_ \[ OptionalResyncFlags\]

**vshadow** **-addresync=**_ShadowCopyId,_** *TargetVolumeDriveLetter* **-resync=**_BCDFileName_ \[ OptionalResyncFlags\]

L'opzione della riga di comando **-addresync** specifica i volumi da includere in un'operazione di risincronizzazione LUN. Il *parametro ShadowCopyId* consente di specificare l'identificatore della copia shadow. Il parametro *facoltativo TargetVolumeDriveLetter* consente di specificare il volume di destinazione in cui copiare il contenuto del volume della copia shadow.

L'opzione della riga di comando **-resync** avvia un'operazione di risincronizzazione LUN. Al termine dell'operazione, la firma di ogni LUN di destinazione deve essere identica a quella del LUN del volume di destinazione. Il *parametro BCDFileName* specifica il nome del file XML che contiene il documento del componente di backup.

> [!Note]  
> Le opzioni della riga di comando **-addresync** e **-resync** sono supportate solo nei sistemi operativi Windows server.

 

**Windows Server 2008 e Windows Server 2003:** Non supportato.

*OptionalResyncFlags* è una maschera di bit di valori flag facoltativi della tabella seguente.



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
<td>Questo flag facoltativo specifica che al termine dell'operazione, la firma di ogni LUN di destinazione deve essere identica a quella del LUN originale usato per creare la copia shadow, non il LUN del volume di destinazione.<br/>
<blockquote>
[!Note]<br />
Il <strong>flag -revertsig</strong> è supportato solo nei sistemi operativi Windows server.
</blockquote>
<br/> <strong>Windows Server 2008 e Windows Server 2003:</strong> Non supportato.<br/></td>
</tr>
<tr class="even">
<td><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong><br/></td>
<td>Questo flag facoltativo specifica che il servizio VSS non deve verificare la presenza di volumi non selezionati che verrebbero sovrascritti dall'operazione di risincronizzazione LUN.<br/>
<blockquote>
[!Note]<br />
Il <strong>flag -novolcheck</strong> è supportato solo nei sistemi operativi Windows server.
</blockquote>
<br/> <strong>Windows Server 2008 e Windows Server 2003:</strong> Non supportato.<br/></td>
</tr>
</tbody>
</table>



 

 

 

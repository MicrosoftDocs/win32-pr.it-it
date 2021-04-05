---
description: MFTrace è uno strumento per la generazione di log di traccia per applicazioni Microsoft Media Foundation.
ms.assetid: f93060dc-cb64-4623-847d-5d78bca59d50
title: Uso di MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022f888ba8b202e4b77a3a571a25874032ec233e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755247"
---
# <a name="using-mftrace"></a>Uso di MFTrace

MFTrace è uno strumento per la generazione di log di traccia per applicazioni Microsoft Media Foundation.

MFTrace usa la libreria Detours per eseguire l'hook Media Foundation chiamate API e generare log di traccia. MFTrace può anche registrare tracce da qualsiasi componente che usa Event Tracing for Windows (ETW) o il preprocessore di traccia software (WPP) per generare tracce. È possibile generare i log di traccia avviando un nuovo processo da MFTrace o collegando MFTrace a un processo esistente.

## <a name="usage"></a>Utilizzo

**mftrace** \[ **-a** *Process* \] \[ **-c** *ConfigurationFile* \] \[ **-DC** \] \[ **-es** \] \[ **-k** *Keywords* \] \[ **-l** *Level* \] \[ **-o** *outputfile* \] \[ **-v** \] \[ **-** ? \] \[ {*Command* \| *ETL_FILE*}\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomenti della riga di comando</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-a_Process_ID_or_Process_Name"></span><span id="-a_process_id_or_process_name"></span><span id="-A_PROCESS_ID_OR_PROCESS_NAME"></span><strong>-a</strong> <strong></strong> <em>ID processo o nome processo</em><br/></td>
<td>Connettersi a un processo in esecuzione.<br/></td>
</tr>
<tr class="even">
<td><span id="-c_Configuration_File"></span><span id="-c_configuration_file"></span><span id="-C_CONFIGURATION_FILE"></span><strong>-c</strong> <strong></strong> <em>File di configurazione</em><br/></td>
<td>Legge le impostazioni dal file di configurazione specificato. Vedere <a href="mftrace-configuration-file.md">file di configurazione MFTrace</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="-dc"></span><span id="-DC"></span><strong>-DC</strong><br/></td>
<td>Disabilitare la traccia per i processi figlio. Per impostazione predefinita, la traccia è abilitata per i processi figlio.<br/></td>
</tr>
<tr class="even">
<td><span id="-es"></span><span id="-ES"></span><strong>-es</strong><br/></td>
<td>Abilita simboli pubblici.<br/></td>
</tr>
<tr class="odd">
<td><span id="-k_Keywords"></span><span id="-k_keywords"></span><span id="-K_KEYWORDS"></span><strong>-k</strong> <strong></strong> <em>Parole chiave</em><br/></td>
<td>Elenco di parole chiave separate da virgole. Vedere <a href="mftrace-keywords.md">parole chiave MFTrace</a>.<br/></td>
</tr>
<tr class="even">
<td><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span><strong>-l</strong> <strong></strong> <em>Livello</em> di<br/></td>
<td>Livello di traccia.<br/>
<ul>
<li>0: Nessuno</li>
<li>1: critico</li>
<li>2: errore</li>
<li>3: avviso</li>
<li>4: informativo</li>
<li>5: dettagliato</li>
<li>16: debug</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="-o_Output_File"></span><span id="-o_output_file"></span><span id="-O_OUTPUT_FILE"></span><strong>-o</strong> <strong></strong> <em>File di output</em><br/></td>
<td>Consente di scrivere l'output di traccia nel file specificato. Per impostazione predefinita, l'output passa a <strong>stdout</strong>.<br/> Se viene specificato un file di output, l'estensione del nome file deve essere una delle seguenti:<br/>
<ul>
<li>. etl: file di log di traccia eventi (ETL).</li>
<li>. log o. txt: file di testo.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="-v"></span><span id="-V"></span><strong>-v</strong><br/></td>
<td>Abilitare la modalità dettagliata.<br/></td>
</tr>
<tr class="odd">
<td><span id="-_"></span><strong>-?</strong><br/></td>
<td>Visualizza le informazioni sull'utilizzo.<br/></td>
</tr>
<tr class="even">
<td><span id="COMMAND"></span><span id="command"></span><em>COMANDO</em><br/></td>
<td>Argomenti della riga di comando per creare un nuovo processo.<br/></td>
</tr>
<tr class="odd">
<td><span id="ETL_FILE"></span><span id="etl_file"></span><em>ETL_FILE</em><br/></td>
<td>Nome di un file ETL esistente. Se viene specificato questo argomento, il file ETL viene convertito nell'output di testo.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="environment-variables"></a>Variabili di ambiente

<dl> <dt>

<span id="TRACE_FORMAT_SEARCH_PATH"></span><span id="trace_format_search_path"></span>TRACE_FORMAT_SEARCH_PATH
</dt> <dd>

Per tracciare i componenti che utilizzano il preprocessore di traccia software di Windows (WPP), impostare questa variabile di ambiente sul percorso per specificare il percorso dei file di formato del messaggio di traccia (MDF) per il componente.

</dd> <dt>

<span id="_NT_SYMBOL_PATH"></span><span id="_nt_symbol_path"></span>_NT_SYMBOL_PATH
</dt> <dd>

Se la ricerca dei simboli è abilitata (**-es**), impostare questa variabile di ambiente per specificare il percorso del simbolo.

</dd> </dl>

## <a name="examples"></a>Esempio

Creare un nuovo processo e tracciare il processo:

``` syntax
mftrace.exe wmplayer.exe Wildlife.wmv
```

Connetti MFTrace a un processo esistente:

``` syntax
mftrace.exe -a wmplayer.exe
mftrace.exe -a 9132
```

Inviare l'output di traccia a un file di testo:

``` syntax
mftrace.exe -a wmplayer.exe -o trace.txt
```

Traccia eventi ETW o WPP:

``` syntax
mftrace.exe -c config.xml -o trace.txt
mftrace.exe -c config.xml -o trace.etl
```

> [!Note]  
> Nel primo esempio viene generato un file di testo. Nel secondo esempio viene generato un file ETL.

 

Convertire un file ETL in un file di testo:

``` syntax
mftrace.exe -o trace.txt trace.etl
```

## <a name="remarks"></a>Commenti

Per impostazione predefinita, MFTrace genera solo tracce di detouring. Per generare tracce ETW o WPP, è necessario fornire un file di configurazione. Il file di configurazione assegna i nomi dei provider di traccia. Per altre informazioni, vedere [file di configurazione MFTrace](mftrace-configuration-file.md).

MFTrace può inviare l'output alle destinazioni seguenti:

-   **stdout** (impostazione predefinita).
-   Un file di testo.
-   Un file ETL binario.

Se si registrano tracce ETW/WPP, un file ETL è l'opzione più efficiente, perché i dati di traccia vengono salvati come BLOB binari. Al termine della sessione di traccia, è possibile usare MFTrace per convertire il file ETL in un file di testo.

> [!Note]  
> Per la traccia di deviazioni, l'output di testo è altrettanto efficiente di un file ETL. Di conseguenza, se si registrano solo le tracce di detouring (senza tracce ETW/WPP), è consigliabile usare l'output di testo.

 

Per la traccia di deviazioni, è necessario aggiungere MFTrace a un processo in esecuzione (**-a**) o usare MFTrace per creare un nuovo processo. Per le tracce ETW/WPP, MFTrace è in ascolto di tutti i provider di eventi elencati nel file di configurazione.

È possibile filtrare i risultati della traccia specificando le parole chiave Trace, tramite l'opzione della riga di comando **-k** o nel file di configurazione. L'uso più comune, tuttavia, consiste nel registrare tutte le tracce e quindi usare uno script o **grep** per cercare modelli di stringa specifici.

## <a name="interpreting-the-trace-results"></a>Interpretazione dei risultati della traccia

È possibile usare MFTrace per rispondere a domande su ciò che accade all'interno dell'applicazione o del componente Media Foundation. Nella tabella seguente sono elencate alcune domande tipiche. La seconda colonna restituisce la stringa di ricerca che può aiutare a rispondere alla domanda.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Domanda</th>
<th>Stringhe di ricerca</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Si è verificato un errore?</td>
<td>&quot;0xc00d&quot;</td>
</tr>
<tr class="even">
<td>La topologia è stata risolta correttamente?</td>
<td>&quot;CTopologyHelpers:: Trace&quot;</td>
</tr>
<tr class="odd">
<td>La sessione multimediale è stata avviata?</td>
<td>&quot;MESessionStarted&quot;</td>
</tr>
<tr class="even">
<td>Quale file è stato riprodotto?</td>
<td>&quot;CMFSourceResolverDetours&quot;</td>
</tr>
<tr class="odd">
<td>Quali sono i tipi di supporto per i flussi di origine?</td>
<td>&quot;Nuovo flusso &quot; , &quot; MENewStream &quot; , &quot; CMFMediaSourceDetours:: TracePD&quot;</td>
</tr>
<tr class="even">
<td>I flussi di origine generano esempi?</td>
<td>&quot;CMFMediaStreamDetours:: HandleEvent &quot; , &quot; MEMediaSample&quot;</td>
</tr>
<tr class="odd">
<td>La riproduzione ha raggiunto la fine dei dati?</td>
<td>&quot;MEEndOfStream &quot; , &quot; MEEndOfPresentation&quot;</td>
</tr>
<tr class="even">
<td>Il formato è stato modificato?</td>
<td>&quot;MEStreamFormatChanged &quot; (origini supporti), &quot; nuovo formato &quot; , &quot; MESessionStreamSinkFormatChanged &quot; (sink di supporto)</td>
</tr>
<tr class="odd">
<td>Quali oggetti sono stati creati?</td>
<td>&quot;COle32ExportDetours:: CoCreateInstance&quot;</td>
</tr>
<tr class="even">
<td>Le trasformazioni di Media Foundation (MFTs) nella pipeline elaborano tutti i dati?</td>
<td>&quot;CMFTransformDetours::P rocessOutput &quot; , &quot; CMFTransformDetours::P rocessinput&quot;</td>
</tr>
<tr class="odd">
<td>Quali Stati sono stati impostati in MFTs?</td>
<td>&quot;CMFTransformDetours::P rocessMessage&quot;</td>
</tr>
<tr class="even">
<td>I dati di input della richiesta MFT sono stati richiesti?</td>
<td>&quot;MF_E_TRANSFORM_NEED_MORE_INPUT &quot; (MFT sincrono), &quot; METRANSFORMNEEDINPUT &quot; (MFT asincrono).</td>
</tr>
<tr class="odd">
<td>Un MFT asincrono produce dati di output?</td>
<td>&quot;ProcessOutputs disponibile&quot;</td>
</tr>
<tr class="even">
<td>Sono stati rilevati esempi di richieste di sink multimediale?</td>
<td>&quot;MEStreamSinkRequestSample&quot;</td>
</tr>
<tr class="odd">
<td>Sono stati ricevuti esempi da un sink multimediale?</td>
<td>&quot;CMFStreamSinkDetours::P rocessSample&quot;</td>
</tr>
<tr class="even">
<td>DirectShow: quali esempi sono stati elaborati?</td>
<td>&quot;esempio &quot; , &quot; CMemInputPinDetours&quot;</td>
</tr>
<tr class="odd">
<td>DirectShow: quale grafico filtro è stato usato?</td>
<td>&quot;CGraphHelpers:: Trace&quot;</td>
</tr>
<tr class="even">
<td>Ci sono più processi?</td>
<td>&quot;CreateProcess&quot;
<blockquote>
[!Note]<br />
Cercare anche l'identificatore del processo, che viene visualizzato all'inizio di ogni riga della traccia.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[MFTrace](mftrace.md)
</dt> </dl>

 

 





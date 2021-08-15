---
description: MFTrace è uno strumento per la generazione di log di traccia per Microsoft Media Foundation applicazioni.
ms.assetid: f93060dc-cb64-4623-847d-5d78bca59d50
title: Uso di MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03cb19f17978236b3e4edd8415f524913c90d99d7a7caf4183dd885d340cfbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737324"
---
# <a name="using-mftrace"></a>Uso di MFTrace

MFTrace è uno strumento per la generazione di log di traccia per Microsoft Media Foundation applicazioni.

MFTrace usa la libreria Detours per eseguire l'hook Media Foundation chiamate API e generare log di traccia. MFTrace può anche registrare tracce da qualsiasi componente che usa Event Tracing for Windows (ETW) o il preprocessore di traccia software (WPP) per generare tracce. I log di traccia possono essere generati avviando un nuovo processo da MFTrace o collegando MFTrace a un processo esistente.

## <a name="usage"></a>Uso

**mftrace** \[ **-a** *Process* \] \[ **-c** *ConfigurationFile* \] \[  \] \[ **-dc -es** \] \[ **-k** *KeyWords* \] \[ **-l** *Level* \] \[ **-o** *OutputFile* \] \[ **-v** \] \[ **-?** \] \[ {*COMMAND* \| *ETL_FILE*}\]



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
<td>Legge le impostazioni dal file di configurazione specificato. Vedere <a href="mftrace-configuration-file.md">File di configurazione di MFTrace</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="-dc"></span><span id="-DC"></span><strong>-dc</strong><br/></td>
<td>Disabilitare la traccia per i processi figlio. Per impostazione predefinita, la traccia è abilitata per i processi figlio.<br/></td>
</tr>
<tr class="even">
<td><span id="-es"></span><span id="-ES"></span><strong>-es</strong><br/></td>
<td>Abilitare i simboli pubblici.<br/></td>
</tr>
<tr class="odd">
<td><span id="-k_Keywords"></span><span id="-k_keywords"></span><span id="-K_KEYWORDS"></span><strong>-k</strong> <strong></strong> <em>Parole chiave</em><br/></td>
<td>Elenco delimitato da virgole di parole chiave. Vedere <a href="mftrace-keywords.md">Parole chiave di MFTrace</a>.<br/></td>
</tr>
<tr class="even">
<td><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span><strong>-l</strong> <strong></strong> <em>Livello</em><br/></td>
<td>Livello di traccia.<br/>
<ul>
<li>0: Nessuno</li>
<li>1: Critico</li>
<li>2: Errore</li>
<li>3: Avviso</li>
<li>4: Informativo</li>
<li>5: Dettagliato</li>
<li>16: Eseguire il debug</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="-o_Output_File"></span><span id="-o_output_file"></span><span id="-O_OUTPUT_FILE"></span><strong>-o</strong> <strong></strong> <em>File di output</em><br/></td>
<td>Scrivere l'output di traccia nel file specificato. Per impostazione predefinita, l'output passa a <strong>stdout</strong>.<br/> Se viene specificato un file di output, l'estensione del nome file deve essere una delle seguenti:<br/>
<ul>
<li>.etl: file di log di traccia eventi (ETL).</li>
<li>.log o .txt: file di testo.</li>
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
<td><span id="COMMAND"></span><span id="command"></span><em>Comando</em><br/></td>
<td>Argomenti della riga di comando per creare un nuovo processo.<br/></td>
</tr>
<tr class="odd">
<td><span id="ETL_FILE"></span><span id="etl_file"></span><em>ETL_FILE</em><br/></td>
<td>Nome di un file ETL esistente. Se viene specificato questo argomento, il file ETL viene convertito in output di testo.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="environment-variables"></a>Variabili di ambiente

<dl> <dt>

<span id="TRACE_FORMAT_SEARCH_PATH"></span><span id="trace_format_search_path"></span>TRACE_FORMAT_SEARCH_PATH
</dt> <dd>

Per tracciare i componenti che usano il preprocessore WPP (Software Trace Preprocessor) di Windows, impostare questa variabile di ambiente su specificare il percorso dei file TMF (Trace Message Format) per il componente.

</dd> <dt>

<span id="_NT_SYMBOL_PATH"></span><span id="_nt_symbol_path"></span>_NT_SYMBOL_PATH
</dt> <dd>

Se la ricerca dei simboli è abilitata (**-es**), impostare questa variabile di ambiente per specificare il percorso del simbolo.

</dd> </dl>

## <a name="examples"></a>Esempio

Creare un nuovo processo e tracciare tale processo:

``` syntax
mftrace.exe wmplayer.exe Wildlife.wmv
```

Collegare MFTrace a un processo esistente:

``` syntax
mftrace.exe -a wmplayer.exe
mftrace.exe -a 9132
```

Inviare l'output di traccia a un file di testo:

``` syntax
mftrace.exe -a wmplayer.exe -o trace.txt
```

Tracciare eventi ETW o WPP:

``` syntax
mftrace.exe -c config.xml -o trace.txt
mftrace.exe -c config.xml -o trace.etl
```

> [!Note]  
> Il primo esempio genera un file di testo. Il secondo esempio genera un file ETL.

 

Convertire un file ETL in un file di testo:

``` syntax
mftrace.exe -o trace.txt trace.etl
```

## <a name="remarks"></a>Commenti

Per impostazione predefinita, MFTrace genera solo tracce detours. Per generare tracce ETW o WPP, è necessario specificare un file di configurazione. Il file di configurazione fornisce i nomi dei provider di traccia. Per altre informazioni, vedere [File di configurazione di MFTrace](mftrace-configuration-file.md).

MFTrace può inviare l'output alle destinazioni seguenti:

-   **stdout** (impostazione predefinita).
-   Un file di testo.
-   Un file ETL binario.

Se si stanno registrare tracce ETW/WPP, un file ETL è l'opzione più efficiente, perché i dati di traccia vengono salvati come BLOB binari. Al termine della sessione di traccia, è possibile usare MFTrace per convertire il file ETL in un file di testo.

> [!Note]  
> Per la traccia di Detours, l'output di testo è efficiente quanto un file ETL. Pertanto, se si registrano solo tracce detours (senza tracce ETW/WPP), è consigliabile eseguire l'output di testo.

 

Per la traccia di Detours, è necessario collegare MFTrace a un processo in esecuzione (**-a**) o usare MFTrace per creare un nuovo processo. Per le tracce ETW/WPP, MFTrace è in ascolto di qualsiasi provider di eventi elencato nel file di configurazione.

È possibile filtrare i risultati della traccia specificando le parole chiave di traccia, tramite l'opzione della riga di comando **-k** o nel file di configurazione. L'utilizzo più tipico, tuttavia, è registrare tutte le tracce e quindi usare uno script o **grep** per cercare modelli di stringa specifici.

## <a name="interpreting-the-trace-results"></a>Interpretazione dei risultati della traccia

È possibile usare MFTrace per rispondere a domande su cosa accade all'interno dell Media Foundation appalto o del componente. Nella tabella seguente sono elencate alcune domande tipiche. La seconda colonna fornisce la stringa di ricerca che consente di rispondere alla domanda.



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
<td>&quot;CTopologyHelpers::Trace&quot;</td>
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
<td>Quali sono i tipi di supporti per i flussi di origine?</td>
<td>&quot;Nuovo flusso &quot; , &quot; MENewStream &quot; , &quot; CMFMediaSourceDetours::TracePD&quot;</td>
</tr>
<tr class="even">
<td>I flussi di origine hanno generato esempi?</td>
<td>&quot;CMFMediaStreamDetours::HandleEvent &quot; , &quot; MEMediaSample&quot;</td>
</tr>
<tr class="odd">
<td>La riproduzione ha raggiunto la fine dei dati?</td>
<td>&quot;MEEndOfStream &quot; , &quot; MEEndOfPresentation&quot;</td>
</tr>
<tr class="even">
<td>Il formato è cambiato?</td>
<td>&quot;MEStreamFormatChanged &quot; (origini multimediali), &quot; Nuovo formato , &quot; &quot; MESessionStreamSinkFormatChanged &quot; (sink multimediali)</td>
</tr>
<tr class="odd">
<td>Quali oggetti sono stati creati?</td>
<td>&quot;COle32ExportDetours::CoCreateInstance&quot;</td>
</tr>
<tr class="even">
<td>I Media Foundation transforms (MFT) nella pipeline elaborano dati?</td>
<td>&quot;CMFTransformDetours::ProcessOutput &quot; , &quot; CMFTransformDetours::ProcessInput&quot;</td>
</tr>
<tr class="odd">
<td>Quali stati sono stati impostati nei MFT?</td>
<td>&quot;CMFTransformDetours::P rocessMessage&quot;</td>
</tr>
<tr class="even">
<td>Un MFT ha richiesto i dati di input?</td>
<td>&quot;MF_E_TRANSFORM_NEED_MORE_INPUT &quot; (MFT sincrono), &quot; METransformNeedInput &quot; (MFT asincrono).</td>
</tr>
<tr class="odd">
<td>Un MFT asincrono ha prodotto dati di output?</td>
<td>&quot;ProcessOutputs disponibili&quot;</td>
</tr>
<tr class="even">
<td>Un sink multimediale ha richiesto esempi?</td>
<td>&quot;MEStreamSinkRequestSample&quot;</td>
</tr>
<tr class="odd">
<td>Un sink multimediale ha ricevuto esempi?</td>
<td>&quot;CMFStreamSinkDetours::P rocessSample&quot;</td>
</tr>
<tr class="even">
<td>DirectShow: Quali campioni sono stati elaborati?</td>
<td>&quot;esempio, &quot; &quot; CMemInputPinDetours&quot;</td>
</tr>
<tr class="odd">
<td>DirectShow: Quale grafo di filtro è stato usato?</td>
<td>&quot;CGraphHelpers::Trace&quot;</td>
</tr>
<tr class="even">
<td>Sono presenti più processi?</td>
<td>&quot;CreateProcess&quot;
<blockquote>
[!Note]<br />
Cercare anche l'identificatore di processo, che viene visualizzato all'inizio di ogni riga di traccia.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[MFTrace](mftrace.md)
</dt> </dl>

 

 





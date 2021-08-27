---
description: MFTrace è uno strumento per la generazione di log di traccia per Microsoft Media Foundation applicazioni.
ms.assetid: f93060dc-cb64-4623-847d-5d78bca59d50
title: Uso di MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8416fbde708dd44858fe5df580945f326944a1f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469968"
---
# <a name="using-mftrace"></a>Uso di MFTrace

MFTrace è uno strumento per la generazione di log di traccia per Microsoft Media Foundation applicazioni.

MFTrace usa la libreria Detours per eseguire l'hook Media Foundation chiamate API e generare log di traccia. MFTrace può anche registrare tracce da qualsiasi componente che usa Event Tracing for Windows (ETW) o il preprocessore di traccia software (WPP) per generare tracce. I log di traccia possono essere generati avviando un nuovo processo da MFTrace o collegando MFTrace a un processo esistente.

## <a name="usage"></a>Utilizzo

**mftrace** \[ **-a** *Process* \] \[ **-c** *ConfigurationFile* \] \[ **-dc** \] \[ **-es** \] \[ **-k** *KeyWords* \] \[ **-l** *Level* \] \[ **-o** *OutputFile* \] \[ **-v** \] \[ **-?** \] \[ {*COMMAND* \| *ETL_FILE*}\]




| Argomenti della riga di comando | Descrizione | 
|------------------------|-------------|
| <span id="-a_Process_ID_or_Process_Name"></span><span id="-a_process_id_or_process_name"></span><span id="-A_PROCESS_ID_OR_PROCESS_NAME"></span><strong>-a</strong> <strong></strong> <em>ID processo o nome del processo</em><br /> | Connettersi a un processo in esecuzione.<br /> | 
| <span id="-c_Configuration_File"></span><span id="-c_configuration_file"></span><span id="-C_CONFIGURATION_FILE"></span><strong>-c</strong> <strong></strong> <em>File di configurazione</em><br /> | Legge le impostazioni dal file di configurazione specificato. Vedere <a href="mftrace-configuration-file.md">File di configurazione di MFTrace</a>.<br /> | 
| <span id="-dc"></span><span id="-DC"></span><strong>-dc</strong><br /> | Disabilitare la traccia per i processi figlio. Per impostazione predefinita, la traccia è abilitata per i processi figlio.<br /> | 
| <span id="-es"></span><span id="-ES"></span><strong>-es</strong><br /> | Abilitare i simboli pubblici.<br /> | 
| <span id="-k_Keywords"></span><span id="-k_keywords"></span><span id="-K_KEYWORDS"></span><strong>-k</strong> <strong></strong> <em>Parole chiave</em><br /> | Elenco delimitato da virgole di parole chiave. Vedere <a href="mftrace-keywords.md">Parole chiave di MFTrace.</a><br /> | 
| <span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span><strong>-l</strong> <strong></strong> <em>Livello</em><br /> | Livello di traccia.<br /><ul><li>0: Nessuno</li><li>1: Critico</li><li>2: Errore</li><li>3: Avviso</li><li>4: Informativo</li><li>5: Dettagliato</li><li>16: Debug</li></ul> | 
| <span id="-o_Output_File"></span><span id="-o_output_file"></span><span id="-O_OUTPUT_FILE"></span><strong>-o</strong> <strong></strong> <em>File di output</em><br /> | Scrive l'output di traccia nel file specificato. Per impostazione predefinita, l'output passa <strong>a stdout</strong>.<br /> Se viene specificato un file di output, l'estensione del nome file deve essere una delle seguenti:<br /><ul><li>.etl: file di log di traccia eventi (ETL).</li><li>.log o .txt: file di testo.</li></ul> | 
| <span id="-v"></span><span id="-V"></span><strong>-v</strong><br /> | Abilitare la modalità dettagliata.<br /> | 
| <span id="-_"></span><strong>-?</strong><br /> | Visualizza le informazioni sull'utilizzo.<br /> | 
| <span id="COMMAND"></span><span id="command"></span><em>COMANDO</em><br /> | Argomenti della riga di comando per creare un nuovo processo.<br /> | 
| <span id="ETL_FILE"></span><span id="etl_file"></span><em>ETL_FILE</em><br /> | Nome di un file ETL esistente. Se viene specificato questo argomento, il file ETL viene convertito in output di testo.<br /> | 




 

## <a name="environment-variables"></a>Variabili di ambiente

<dl> <dt>

<span id="TRACE_FORMAT_SEARCH_PATH"></span><span id="trace_format_search_path"></span>TRACE_FORMAT_SEARCH_PATH
</dt> <dd>

Per tracciare i componenti che usano il preprocessore WPP (Software Trace Preprocessor) di Windows, impostare questa variabile di ambiente su per specificare il percorso dei file TMF (Trace Message Format) per il componente.

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

Per impostazione predefinita, MFTrace genera solo tracce detours. Per generare tracce ETW o WPP, è necessario specificare un file di configurazione. Il file di configurazione fornisce i nomi dei provider di traccia. Per altre informazioni, vedere [File di configurazione di MFTrace.](mftrace-configuration-file.md)

MFTrace può inviare l'output alle destinazioni seguenti:

-   **stdout** (impostazione predefinita).
-   File di testo.
-   File ETL binario.

Se si stanno registrare tracce ETW/WPP, un file ETL è l'opzione più efficiente, perché i dati di traccia vengono salvati come BLOB binari. Al termine della sessione di traccia, è possibile usare MFTrace per convertire il file ETL in un file di testo.

> [!Note]  
> Per la traccia di Detours, l'output di testo è efficiente quanto un file ETL. Pertanto, se si registrano solo tracce Detours (senza tracce ETW/WPP), è consigliabile l'output di testo.

 

Per la traccia di Detours, è necessario collegare MFTrace a un processo in esecuzione (**-a**) o usare MFTrace per creare un nuovo processo. Per le tracce ETW/WPP, MFTrace è in ascolto di qualsiasi provider di eventi elencato nel file di configurazione.

È possibile filtrare i risultati della traccia specificando parole chiave di traccia, tramite l'opzione della riga di comando **-k** o nel file di configurazione. L'utilizzo più tipico, tuttavia, è registrare tutte le tracce e quindi usare uno script o **grep** per cercare modelli di stringa specifici.

## <a name="interpreting-the-trace-results"></a>Interpretazione dei risultati della traccia

È possibile usare MFTrace per rispondere a domande su ciò che accade all'interno dell'Media Foundation o del componente. Nella tabella seguente sono elencate alcune domande tipiche. La seconda colonna fornisce la stringa di ricerca che può essere utile per rispondere alla domanda.




| Domanda | Stringhe di ricerca | 
|----------|----------------|
| Si è verificato un errore? | "0xc00d" | 
| La topologia è stata risolta correttamente? | "CTopologyHelpers::Trace" | 
| La sessione multimediale è stata avviata? | "MESessionStarted" | 
| Quale file è stato riprodotto? | "CMFSourceResolverDetours" | 
| Quali sono i tipi di supporti per i flussi di origine? | "New stream", "MENewStream", "CMFMediaSourceDetours::TracePD" | 
| I flussi di origine hanno generato esempi? | "CMFMediaStreamDetours::HandleEvent", "MEMediaSample" | 
| La riproduzione ha raggiunto la fine dei dati? | "MEEndOfStream", "MEEndOfPresentation" | 
| Il formato è cambiato? | "MEStreamFormatChanged" (origini multimediali), "Nuovo formato", "MESessionStreamSinkFormatChanged" (sink multimediali) | 
| Quali oggetti sono stati creati? | "COle32ExportDetours::CoCreateInstance" | 
| Le trasformazioni Media Foundation (MFT) nella pipeline hanno processato dati? | "CMFTransformDetours::P rocessOutput", "CMFTransformDetours::P rocessInput" | 
| Quali stati sono stati impostati nei MFT? | "CMFTransformDetours::P rocessMessage" | 
| Un MFT ha richiesto i dati di input? | "MF_E_TRANSFORM_NEED_MORE_INPUT" (MFT sincrono), "METransformNeedInput" (MFT asincrono). | 
| Un MFT asincrono ha prodotto dati di output? | "ProcessOutputs available" | 
| Un sink multimediale ha richiesto esempi? | "MEStreamSinkRequestSample" | 
| Un sink multimediale ha ricevuto esempi? | "CMFStreamSinkDetours::P rocessSample" | 
| DirectShow: Quali campioni sono stati elaborati? | "sample", "CMemInputPinDetours" | 
| DirectShow: Quale grafo di filtro è stato usato? | "CGraphHelpers::Trace" | 
| Sono presenti più processi? | "CreateProcess"<blockquote>[!Note]<br />Cercare anche l'identificatore di processo, che viene visualizzato all'inizio di ogni riga di traccia.</blockquote><br /><br /> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[MFTrace](mftrace.md)
</dt> </dl>

 

 





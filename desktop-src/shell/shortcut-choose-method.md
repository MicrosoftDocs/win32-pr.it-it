---
description: 'Questo argomento è organizzato nel modo seguente:'
title: Scelta di un metodo di menu di scelta rapida statico o dinamico
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 70c6cb74e2c9a432bfdae2f26da1fdbebfc5f00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057841"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a>Scelta di un metodo di menu di scelta rapida statico o dinamico

Questo argomento è organizzato nel modo seguente:

-   [Scegliere un metodo verb](#choose-a-verb-method)
    -   [Metodi di verbi statici](#static-verb-methods)
    -   [Metodi di verbi dinamici Preferiti](#preferred-dynamic-verb-methods)
    -   [Metodi di verbi dinamici sconsigliati](#discouraged-dynamic-verb-methods)
-   [Estendi un menu di scelta rapida](#extend-a-shortcut-menu)
-   [Supporto per i metodi Verb per sistema operativo](#support-for-verb-methods-by-operating-system)
-   [Argomenti correlati](#related-topics)

## <a name="choose-a-verb-method"></a>Scegliere un metodo verb

Si consiglia di implementare un menu di scelta rapida utilizzando uno dei metodi del verbo statico.

### <a name="static-verb-methods"></a>Metodi di verbi statici

I verbi statici sono i verbi più semplici da implementare, ma forniscono comunque funzionalità avanzate. Scegliere sempre il metodo di menu di scelta rapida più semplice che soddisfi le proprie esigenze.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Verbo statico</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> con parametri della riga di comando</td>
<td>Questo è il metodo più semplice e più noto per implementare un verbo statico. Un processo viene richiamato tramite una chiamata alla funzione <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> con i file selezionati e tutti i parametri facoltativi passati come riga di comando. Verrà aperto il file o la cartella.<br/> Questo metodo presenta le limitazioni seguenti:
<ul>
<li>La lunghezza della riga di comando è limitata a 2000 caratteri, che limita il numero di elementi che il verbo è in grado di gestire.</li>
<li>Può essere utilizzato solo con elementi file system.</li>
<li>Non consente il riutilizzo di un processo già in esecuzione.</li>
<li>Richiede l'installazione di un eseguibile per gestire il verbo.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>IDropTarget</strong></a></td>
<td>Un'attivazione di verbi basata su COM significa che supporta l'attivazione in-process o out-of-process. <strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> supporta inoltre il riutilizzo di un gestore già in esecuzione quando l'interfaccia <strong>IDropTarget</strong> viene implementata da un server locale. Inoltre, esprime perfettamente gli elementi tramite l'oggetto dati di cui è stato effettuato il marshalling e fornisce un riferimento alla catena di siti chiamante per poter interagire con l'invoker tramite <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</td>
</tr>
<tr class="odd">
<td>Windows 7 e versioni successive: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>IExecuteCommand</strong></a></td>
<td>Metodo di implementazione più diretto. Poiché si tratta di un metodo Invoke basato su COM (ad esempio DropTarget), questa interfaccia supporta l'attivazione in-process e out-of-process. Il verbo implementa <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>e, facoltativamente, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>. Gli elementi vengono passati direttamente come matrice di elementi della shell e la maggior parte dei parametri dell'invoker sono disponibili per l'implementazione del verbo, inclusi il punto di richiamo, lo stato della tastiera e così via.</td>
</tr>
<tr class="even">
<td>Windows 7 e versioni successive:<strong>ExplorerCommand</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></td>
<td>Consente alle origini dati che forniscono i comandi del modulo di comando tramite <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> di utilizzare tali comandi come verbi in un menu di scelta rapida. Poiché questa interfaccia supporta solo l'attivazione in-process, è consigliabile utilizzarla dalle origini dati della shell che devono condividere l'implementazione tra i comandi e i menu di scelta rapida.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) è un ibrido tra un verbo statico e dinamico. **IExplorerCommand** è stato dichiarato in Windows Vista, ma la sua capacità di implementare un verbo in un menu di scelta rapida è una novità di Windows 7.

 

Per ulteriori informazioni sulle query [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e Shell per gli attributi di associazione file, vedere [tipi percepiti e registrazione di applicazioni](fa-perceivedtypes.md).

### <a name="preferred-dynamic-verb-methods"></a>Metodi di verbi dinamici Preferiti

Sono preferibili i metodi dei verbi dinamici seguenti:



| Tipo di verbo                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verbo statico (elencato nella tabella precedente) + sintassi di query avanzata (AQS)                  | Questa scelta ottiene la visibilità dinamica del verbo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Windows 7 e versioni successive: [ **IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)                         | Questa scelta consente un'implementazione comune di verbi e comandi di Explorer visualizzati nel modulo Command in Esplora risorse.                                                                                                                                                                                                                                                                                                                                                                                               |
| Windows 7 e versioni successive: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + verbo statico | Questa scelta consente inoltre di ottenere la visibilità dinamica del verbo. Si tratta di un modello ibrido in cui viene usato un semplice gestore in-process per calcolare se un determinato verbo statico deve essere visualizzato. Questo può essere applicato a tutti i metodi di implementazione del verbo statico per ottenere un comportamento dinamico e ridurre al minimo l'esposizione della logica in-process. [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) ha il vantaggio di essere eseguito in un thread in background, evitando in tal modo blocchi dell'interfaccia utente. È molto più semplice di [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). |



 

### <a name="discouraged-dynamic-verb-methods"></a>Metodi di verbi dinamici sconsigliati

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) è il metodo più potente ma anche il più complesso da implementare. Si basa su oggetti COM in-process eseguiti sul thread del chiamante, che in genere è Esplora risorse, ma può essere qualsiasi applicazione che ospita gli elementi. **IContextMenu** supporta la visibilità del verbo, l'ordinamento e il disegno personalizzato. Alcune di queste funzionalità sono state aggiunte alle funzionalità dei verbi statici, ad esempio un'icona da associare a un comando e [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) per gestire la visibilità.

Se è necessario estendere il menu di scelta rapida per un tipo di file registrando un verbo dinamico per il tipo di file, seguire le istruzioni fornite in [personalizzazione di un menu di scelta rapida usando verbi dinamici](shortcut-menu-using-dynamic-verbs.md).

## <a name="extend-a-shortcut-menu"></a>Estendi un menu di scelta rapida

Dopo aver scelto un metodo verbo, è possibile estendere un menu di scelta rapida per un tipo di file registrando un verbo statico per il tipo di file. Per altre informazioni, vedere [creazione di gestori di menu di scelta rapida](context-menu-handlers.md).

## <a name="support-for-verb-methods-by-operating-system"></a>Supporto per i metodi Verb per sistema operativo

Nella tabella seguente sono elencati il supporto per i metodi di chiamata ai verbi per sistema operativo.



|                      |            |               |                      |
|----------------------|------------|---------------|----------------------|
|                      | Windows XP | Windows Vista | Windows 7 e versioni successive |
| CreateProcess        | X          | X             | X                    |
| DDE                  | X          | X             | X                    |
| DropTarget           | X          | X             | X                    |
| ExecuteCommand       |            | X             | X                    |
| ExplorerCommand      |            |               | X                    |
| ExplorerCommandState |            |               | X                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure consigliate per i gestori di menu di scelta rapida e più verbi di selezione](verbs-best-practices.md)
</dt> <dt>

[Creazione di gestori di menu di scelta rapida](context-menu-handlers.md)
</dt> <dt>

[Personalizzazione di un menu di scelta rapida tramite verbi dinamici](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menu di scelta rapida (contesto) e gestori di menu di scelta rapida](context-menu.md)
</dt> <dt>

[Riferimento al menu di scelta rapida](context-menu-reference.md)
</dt> <dt>

[Verbi e associazioni di file](fa-verbs.md)
</dt> </dl>

 

 

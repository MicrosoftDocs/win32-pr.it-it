---
description: Scegliere un metodo di menu di scelta rapida statico o dinamico quando si implementa un formato di file personalizzato in Windows Shell.
title: Scelta di un metodo di menu di scelta rapida statico o dinamico
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c910407dbd9de9f12853973f9891fe092a0603ca50a03e59183697b0f92b07e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968320"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a>Scelta di un metodo di menu di scelta rapida statico o dinamico

Questo argomento è organizzato come segue:

-   [Scegliere un metodo verbo](#choose-a-verb-method)
    -   [Metodi di verbi statici](#static-verb-methods)
    -   [Metodi di verbi dinamici preferiti](#preferred-dynamic-verb-methods)
    -   [Metodi di verbi dinamici sconsigliati](#discouraged-dynamic-verb-methods)
-   [Estendere un menu di scelta rapida](#extend-a-shortcut-menu)
-   [Supporto per i metodi verbi dal sistema operativo](#support-for-verb-methods-by-operating-system)
-   [Argomenti correlati](#related-topics)

## <a name="choose-a-verb-method"></a>Scegliere un metodo verbo

È consigliabile implementare un menu di scelta rapida usando uno dei metodi di verbi statici.

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
<td><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess con</strong></a> parametri della riga di comando</td>
<td>Questo è il modo più semplice e familiare per implementare un verbo statico. Un processo viene richiamato tramite una chiamata alla <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>funzione CreateProcess</strong></a> con i file selezionati ed eventuali parametri facoltativi passati come riga di comando. Verrà aperto il file o la cartella.<br/> Questo metodo presenta le limitazioni seguenti:
<ul>
<li>La lunghezza della riga di comando è limitata a 2000 caratteri, che limita il numero di elementi che il verbo può gestire.</li>
<li>Può essere usato solo con file system elementi.</li>
<li>Non abilita il nuovo uso di un processo già in esecuzione.</li>
<li>Richiede l'installazione di un eseguibile per gestire il verbo.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>IDropTarget</strong></a></td>
<td>Un'attivazione verbo basata su COM significa che supporta l'attivazione in-process o out-of-process. <strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> supporta anche il nuovo uso di un gestore già in esecuzione quando <strong>l'interfaccia IDropTarget</strong> viene implementata da un server locale. Esprime inoltre perfettamente gli elementi tramite l'oggetto dati di cui è stato effettuato il marshalling e fornisce un riferimento alla catena del sito di chiamata in modo che sia possibile interagire con l'invoker tramite <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</td>
</tr>
<tr class="odd">
<td>Windows 7 e versioni successive: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>IExecuteCommand</strong></a></td>
<td>Metodo di implementazione più diretto. Poiché si tratta di un metodo invoke basato su COM (come DropTarget), questa interfaccia supporta l'attivazione in-process e out-of-process. Il verbo implementa <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>e facoltativamente <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>. Gli elementi vengono passati direttamente come matrice di elementi shell e altri parametri dell'invoker sono disponibili per l'implementazione del verbo, tra cui il punto di richiamo, lo stato della tastiera e così via.</td>
</tr>
<tr class="even">
<td>Windows 7 e versioni successive:<strong>ExplorerCommand</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></td>
<td>Consente alle origini dati che forniscono i comandi del modulo di comando <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>tramite IExplorerCommandProvider</strong></a> di usare tali comandi come verbi in un menu di scelta rapida. Poiché questa interfaccia supporta solo l'attivazione in-process, è consigliabile usarla dalle origini dati shell che devono condividere l'implementazione tra comandi e menu di scelta rapida.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> [**IExplorerCommand è**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) un ibrido tra un verbo statico e un verbo dinamico. **IExplorerCommand** è stato dichiarato in Windows Vista, ma la possibilità di implementare un verbo in un menu di scelta rapida è una novità Windows 7.

 

Per altre informazioni sulle [**query IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e Shell per gli attributi di associazione file, vedere [Tipi percepiti e Registrazione dell'applicazione](fa-perceivedtypes.md).

### <a name="preferred-dynamic-verb-methods"></a>Metodi di verbi dinamici preferiti

Sono preferibili i metodi di verbi dinamici seguenti:



| Tipo di verbo                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verbo statico (elencato nella tabella precedente) + Sintassi di query avanzata (AQS)                  | Questa scelta ottiene la visibilità dinamica del verbo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Windows 7 e versioni successive: [ **IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)                         | Questa scelta consente un'implementazione comune di verbi e comandi di esplorazione visualizzati nel modulo di comando in Windows Explorer.                                                                                                                                                                                                                                                                                                                                                                                               |
| Windows 7 e versioni successive: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + verbo statico | Questa scelta ottiene anche la visibilità dinamica del verbo. Si tratta di un modello ibrido in cui viene usato un semplice gestore in-process per calcolare se un verbo statico specificato deve essere displyed. Questo può essere applicato a tutti i metodi di implementazione dei verbi statici per ottenere un comportamento dinamico e ridurre al minimo l'esposizione della logica in-process. [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) ha il vantaggio di essere eseguito in un thread in background e quindi evita blocchi dell'interfaccia utente. È notevolmente più semplice di [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). |



 

### <a name="discouraged-dynamic-verb-methods"></a>Metodi di verbi dinamici sconsigliati

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) è il metodo più potente ma anche il metodo più complesso da implementare. Si basa su oggetti COM in-process eseguiti sul thread del chiamante, che in genere Windows Explorer, ma può essere qualsiasi applicazione che ospita gli elementi. **IContextMenu supporta** la visibilità dei verbi, l'ordinamento e il disegno personalizzato. Alcune di queste funzionalità sono state aggiunte alle funzionalità dei verbi statici, ad esempio un'icona da associare a un comando, e [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) per gestire la visibilità.

Se è necessario estendere il menu di scelta rapida per un tipo di file registrando un verbo dinamico per il tipo di file, seguire le istruzioni fornite in Personalizzazione di un menu di scelta rapida tramite [verbi dinamici](shortcut-menu-using-dynamic-verbs.md).

## <a name="extend-a-shortcut-menu"></a>Estendere un menu di scelta rapida

Dopo aver scelto un metodo verbo, è possibile estendere un menu di scelta rapida per un tipo di file registrando un verbo statico per il tipo di file. Per altre informazioni, vedere [Creazione di gestori del menu di scelta rapida](context-menu-handlers.md).

## <a name="support-for-verb-methods-by-operating-system"></a>Supporto per i metodi verbi dal sistema operativo

Il supporto per i metodi di chiamata di verbi per sistema operativo è elencato nella tabella seguente.



| Metodo Verb          | Windows XP | Windows Vista | Windows 7 e oltre |
|----------------------|------------|---------------|----------------------|
| CreateProcess        | X          | X             | X                    |
| DDE                  | X          | X             | X                    |
| DropTarget           | X          | X             | X                    |
| ExecuteCommand       |            | X             | X                    |
| ExplorerCommand      |            |               | X                    |
| ExplorerCommandState |            |               | X                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure consigliate per i gestori del menu di scelta rapida e più verbi di selezione](verbs-best-practices.md)
</dt> <dt>

[Creazione di gestori di menu di scelta rapida](context-menu-handlers.md)
</dt> <dt>

[Personalizzazione di un menu di scelta rapida tramite verbi dinamici](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menu di scelta rapida e gestori del menu di scelta rapida](context-menu.md)
</dt> <dt>

[Informazioni di riferimento sul menu di scelta rapida](context-menu-reference.md)
</dt> <dt>

[Verbi e associazioni di file](fa-verbs.md)
</dt> </dl>

 

 

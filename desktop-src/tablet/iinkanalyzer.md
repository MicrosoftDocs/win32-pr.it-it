---
description: Consente di accedere all'analisi del layout, alla classificazione di scrittura e disegno e al riconoscimento della grafia.
ms.assetid: 3a19db78-df14-43c2-9e3e-8cf674aa7b9c
title: Interfaccia IInkAnalyzer (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bd1bca0a00cbe95c4d32b2dfad8afe6c5db8ad63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346616"
---
# <a name="iinkanalyzer-interface"></a>Interfaccia IInkAnalyzer

Consente di accedere all'analisi del layout, alla classificazione di scrittura e disegno e al riconoscimento della grafia.

## <a name="members"></a>Membri

L'interfaccia **IInkAnalyzer** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IInkAnalyzer** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IInkAnalyzer** dispone di questi metodi.



| Metodo                                                                                                  | Descrizione                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interruzione**](iinkanalyzer-abort.md)                                                                     | Annulla l'operazione di analisi corrente.<br/>                                                                                                                                           |
| [**AddStroke**](iinkanalyzer-addstroke.md)                                                             | Aggiunge i dati del tratto per un singolo tratto a **IInkAnalyzer** e assegna l'identificatore delle impostazioni cultura del thread di input attivo al tratto.<br/>                                              |
| [**AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)                                       | Aggiunge i dati del tratto per un singolo tratto a **IInkAnalyzer** e assegna un identificatore di impostazioni cultura specifico al tratto.<br/>                                                             |
| [**AddStrokes**](iinkanalyzer-addstrokes.md)                                                           | Aggiunge i dati del tratto per più tratti a **IInkAnalyzer** e assegna l'identificatore delle impostazioni cultura del thread di input attivo ai tratti.<br/>                                            |
| [**AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)                                     | Aggiunge i dati del tratto per più tratti a **IInkAnalyzer** e assegna l'identificatore delle impostazioni cultura specificato ai tratti.<br/>                                                        |
| [**AddStrokesToCustomRecognizer**](iinkanalyzer-addstrokestocustomrecognizer.md)                       | Aggiunge dati Stroke per più tratti a un nodo di riconoscimento personalizzato.<br/>                                                                                                                |
| [**AddStrokeToCustomRecognizer**](iinkanalyzer-addstroketocustomrecognizer.md)                         | Aggiunge i dati del tratto per un singolo tratto a un nodo di riconoscimento personalizzato.<br/>                                                                                                                 |
| [**Analisi**](iinkanalyzer-analyze.md)                                                                 | Esegue l'analisi dell'input sincrono.<br/>                                                                                                                                                |
| [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)                                             | Esegue l'analisi asincrona dell'input penna.<br/>                                                                                                                                               |
| [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md)                                                 | Cancella i dati dei pacchetti Stroke dal **IInkAnalyzer**.<br/>                                                                                                                              |
| [**CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)                                           | Aggiunge un nuovo nodo hint di analisi con un'area infinita a **IInkAnalyzer**.<br/>                                                                                                      |
| [**CreateContextNodes**](iinkanalyzer-createcontextnodes.md)                                           | Crea un oggetto [**IContextNodes**](icontextnodes.md) .<br/>                                                                                                                         |
| [**CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)                                   | Crea un nuovo nodo di riconoscimento personalizzato per **IInkAnalyzer**.<br/>                                                                                                                    |
| [**DeleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)                                           | Rimuove un hint di analisi da **IInkAnalyzer**.<br/>                                                                                                                               |
| [**FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)                                               | Recupera tutti i nodi foglia dell'input penna.<br/>                                                                                                                                              |
| [**FindInkLeafNodesForStrokes**](iinkanalyzer-findinkleafnodesforstrokes.md)                           | Recupera i nodi foglia dell'input penna che contengono i tratti specificati.<br/>                                                                                                                  |
| [**FindLeafNodes**](iinkanalyzer-findleafnodes.md)                                                     | Recupera tutti i nodi foglia.<br/>                                                                                                                                                  |
| [**FindNode**](iinkanalyzer-findnode.md)                                                               | Recupera l'oggetto [**IContextNode**](icontextnode.md) per un identificatore univoco globale (Guid) specificato.<br/>                                                                      |
| [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md)                                                 | Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) del tipo specificato.<br/>                                                                                          |
| [**FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)                             | Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) del tipo specificato che contengono i tratti specificati.<br/>                                                       |
| [**FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)                               | Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) del tipo specificato che sono discendenti dell'oggetto **IContextNode** specificato.<br/>                            |
| [**FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)                                     | Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) che corrispondono ai criteri specificati.<br/>                                                                              |
| [**FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)                   | Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) che corrispondono ai criteri specificati e sono discendenti dell'oggetto **IContextNode** specificato.<br/>                 |
| [**GetAlternates**](iinkanalyzer-getalternates.md)                                                     | Recupera 10 alternative di analisi per tutti gli input penna associati a **IInkAnalyzer**.<br/>                                                                                                |
| [**GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)                       | Recupera le alternative di analisi per i nodi in una raccolta [**IContextNodes**](icontextnodes.md) specificata.<br/>                                                                     |
| [**GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)                                 | Recupera le alternative di analisi per i tratti con gli identificatori di tratto specificati.<br/>                                                                                              |
| [**GetAnalysisHints**](iinkanalyzer-getanalysishints.md)                                               | Recupera tutti gli oggetti hint di analisi [**IContextNode**](icontextnode.md) collegati a **IInkAnalyzer**.<br/>                                                        |
| [**GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)                                   | Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) hint di analisi collegati a **IInkAnalyzer** e con il nome specificato.<br/>                       |
| [**GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)                                               | Recupera i flag che controllano il modo in cui **IInkAnalyzer** esegue l'analisi dell'input penna.<br/>                                                                                                      |
| [**GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)                                                   | Recupera l'area modificata dall'ultima operazione di analisi.<br/>                                                                                                            |
| [**GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)         | Recupera una raccolta ordinata di oggetti [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .<br/>                                                                              |
| [**GetNodesFromTextRange**](iinkanalyzer-getnodesfromtextrange.md)                                     | Recupera una raccolta di oggetti [**IContextNode**](icontextnode.md) che sono rilevanti per l'intervallo di testo specificato per i nodi di contesto specificati.<br/>                             |
| [**GetRecognizedString**](iinkanalyzer-getrecognizedstring.md)                                         | Recupera la stringa di risultato migliore dell'operazione di riconoscimento per l'intero albero del nodo di contesto in **IInkAnalyzer**.<br/>                                                           |
| [**GetRootNode**](iinkanalyzer-getrootnode.md)                                                         | Recupera il [**IContextNode**](icontextnode.md) radice dell'albero del contesto dell'oggetto **IInkAnalyzer** .<br/>                                                                            |
| [**GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md)                                         | Recupera l'identificatore delle impostazioni locali del tratto specificato.<br/>                                                                                                                          |
| [**GetStrokeType**](iinkanalyzer-getstroketype.md)                                                     | Recupera il tipo del tratto specificato.<br/>                                                                                                                                       |
| [**GetTextRangeFromNodes**](iinkanalyzer-gettextrangefromnodes.md)                                     | Trova l'intervallo di testo nella stringa riconosciuta che corrisponde a una raccolta di oggetti [**IContextNode**](icontextnode.md) .<br/>                                                   |
| [**IsAnalyzing**](iinkanalyzer-isanalyzing.md)                                                         | Recupera un valore che indica se **IInkAnalyzer** esegue l'analisi dell'input penna.<br/>                                                                                             |
| [**LoadResults**](iinkanalyzer-loadresults.md)                                                         | Carica i risultati dell'analisi salvata in **IInkAnalyzer**.<br/>                                                                                                                           |
| [**ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)                                           | Modifica l'alternanza principale corrente nell'alternativa specificata e cancella il tipo di conferma per tutti gli oggetti [**IContextNode**](icontextnode.md) associati all'alternativa.<br/> |
| [**ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)           | Modifica l'alternanza principale corrente nel [**IAnalysisAlternate**](ianalysisalternate.md)specificato.<br/>                                                                              |
| [**Reconcile**](iinkanalyzer-reconcile.md)                                                             | Determina quali parti dei risultati dell'analisi sono state modificate durante l'analisi dell'input penna in background.<br/>                                                                                    |
| [**RemoveStroke**](iinkanalyzer-removestroke.md)                                                       | Rimuove il tratto specificato da **IInkAnalyzer**.<br/>                                                                                                                           |
| [**RemoveStrokes**](iinkanalyzer-removestrokes.md)                                                     | Rimuove i tratti specificati da **IInkAnalyzer**.<br/>                                                                                                                          |
| [**SaveResults**](iinkanalyzer-saveresults.md)                                                         | Salva tutti i risultati dell'analisi per un **IInkAnalyzer**.<br/>                                                                                                                               |
| [**SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)                                         | Salva i risultati dell'analisi per una raccolta di nodi di contesto specifica associata a un **IInkAnalyzer**.<br/>                                                                                |
| [**SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md)                                     | Salva i risultati dell'analisi per i tratti specificati associati a un **IInkAnalyzer**.<br/>                                                                                             |
| [**Cerca**](iinkanalyzer-search.md)                                                                   | Fornisce una ricerca basata su frasi fuzzy senza distinzione tra maiuscole e minuscole per i tratti di scrittura analizzati e i tratti di disegno analizzati con tipi riconosciuti.<br/>                                      |
| [**SearchWithLanguageId**](iinkanalyzer-searchwithlanguageid.md)                                       | Fornisce una ricerca basata su frasi fuzzy senza distinzione tra maiuscole e minuscole per i tratti di scrittura analizzati e i tratti di disegno analizzati con tipi riconosciuti.<br/>                                      |
| [**SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)                                               | Modifica i flag che controllano il modo in cui **IInkAnalyzer** esegue l'analisi dell'input penna.<br/>                                                                                                       |
| [**SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)                                                   | Modifica l'area che è stata modificata dopo l'ultima operazione di analisi.<br/>                                                                                                             |
| [**SetHighestPriorityInkAnalysisRecognizer**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) | Sposta il [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) specificato nella prima posizione dell'elenco di riconoscitori di input penna dell'oggetto **IInkAnalyzer** .<br/>                      |
| [**SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md)                                         | Modifica l'identificatore delle impostazioni locali per il tratto specificato.<br/>                                                                                                                           |
| [**SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md)                                       | Modifica l'identificatore delle impostazioni locali per i tratti specificati.<br/>                                                                                                                          |
| [**SetStrokesType**](iinkanalyzer-setstrokestype.md)                                                   | Modifica il tipo dei tratti specificati.<br/>                                                                                                                                        |
| [**SetStrokeType**](iinkanalyzer-setstroketype.md)                                                     | Modifica il tipo del tratto specificato.<br/>                                                                                                                                         |
| [**UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md)                                             | Aggiorna i dati dei pacchetti per i tratti specificati.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Commenti

**IInkAnalyzer** usa i dati dei pacchetti Stroke per analizzare l'input penna e non interagisce direttamente con gli oggetti della [**classe InkDisp**](inkdisp-class.md) o della [raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

Per aggiungere o rimuovere tratti a **IInkAnalyzer** per l'analisi, usare uno dei metodi seguenti.

-   [**Metodo IInkAnalyzer:: AddStroke**](iinkanalyzer-addstroke.md)
-   [**Metodo IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)
-   [**Metodo IInkAnalyzer:: RemoveStroke**](iinkanalyzer-removestroke.md)
-   [**Metodo IInkAnalyzer:: RemoveStrokes**](iinkanalyzer-removestrokes.md)

Questi metodi aggiornano l'area dirty (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)), che rappresenta l'area per cui vengono analizzati i tratti nella successiva operazione di analisi.

Per analizzare l'input penna, usare il metodo [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) o il metodo [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) . Durante l'analisi, **IInkAnalyzer** esegue l'analisi del layout, la classificazione del tratto e il riconoscimento della grafia.

Per modificare le impostazioni di analisi del layout e classificazione del tratto, utilizzare la proprietà del [**Metodo IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md) .

Durante l'analisi, il **IInkAnalyzer** riceve un certo numero di eventi, inclusi gli eventi generati durante l'analisi in background. [**\_ IAnalysisProxyEvents**](-ianalysisproxyevents.md) supporta le funzionalità del proxy di dati di **IInkAnalyzer**. Per altre informazioni, vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md). Per arrestare il processo di analisi dall'interno di un gestore eventi, chiamare il [**Metodo IInkAnalyzer:: Abort**](iinkanalyzer-abort.md).

Per modificare la lingua utilizzata dall'analizzatore di input penna per riconoscere la grafia, utilizzare il metodo [**IInkAnalyzer:: SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md) o [**IInkAnalyzer:: SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md). Per modificare il modo in cui l'analizzatore di input penna classifica i tratti specifici, usare il metodo [**IInkAnalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md) o [**IInkAnalyzer:: SetStrokesType**](iinkanalyzer-setstrokestype.md).

**IInkAnalyzer** carica le informazioni per tutti i riconoscitori di input penna installati. Il [**Metodo IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) restituisce una raccolta [**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md) contenente ogni [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)disponibile. Se più di un riconoscimento input penna supporta una lingua specifica, usare il [**Metodo IInkAnalyzer:: SetHighestPriorityInkAnalysisRecognizer**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) per impostare il riconoscimento dell'input penna che gestisce i tratti per tale lingua.

L'utilizzo di hint di analisi può migliorare l'accuratezza del riconoscimento fornendo un contesto aggiuntivo all'analizzatore di input penna. Le informazioni aggiuntive sul contesto possono aiutare l'analizzatore di input penna a limitare il numero di possibili risultati del riconoscimento. Ad esempio, è possibile restringere l'ambito definendo factoids e le parole previste o strutturando l'input in una guida al riconoscimento. Per ulteriori informazioni su come fornire il contesto all'analizzatore di input penna, vedere:

-   [**Metodo IInkAnalyzer:: CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)
-   [**IInkAnalyzer::D Metodo eleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)
-   [**Metodo IInkAnalyzer:: GetAnalysisHints**](iinkanalyzer-getanalysishints.md)
-   [**Metodo IInkAnalyzer:: GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)

L'analizzatore di input penna rappresenta i risultati dell'analisi come stringa o come albero di oggetti [**IContextNode**](icontextnode.md) . Per accedere alla stringa riconosciuta, usare il [**Metodo IInkAnalyzer:: GetRecognizedString**](iinkanalyzer-getrecognizedstring.md). Per accedere alla radice dell'albero del nodo di contesto, usare il [**Metodo IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md). Ink Analyzer presenta i metodi seguenti per trovare i nodi di contesto o il testo specifici.

-   [**Metodo IInkAnalyzer:: FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)
-   [**Metodo IInkAnalyzer:: FindInkLeafNodesForStrokes**](iinkanalyzer-findinkleafnodesforstrokes.md)
-   [**Metodo IInkAnalyzer:: FindLeafNodes**](iinkanalyzer-findleafnodes.md)
-   [**Metodo IInkAnalyzer:: FindNode**](iinkanalyzer-findnode.md)
-   [**Metodo IInkAnalyzer:: FindNodesOfType**](iinkanalyzer-findnodesoftype.md)
-   [**Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)
-   [**Metodo IInkAnalyzer:: FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)
-   [**Metodo IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
-   [**Metodo IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)

Per lavorare con i risultati dell'analisi alternativa, usare uno dei metodi seguenti.

-   [**Metodo IInkAnalyzer:: getalters**](iinkanalyzer-getalternates.md)
-   [**Metodo IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)
-   [**Metodo IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)
-   [**Metodo IInkAnalyzer:: ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)
-   [**Metodo IInkAnalyzer:: ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)

Per salvare i risultati dell'analisi, utilizzare uno dei metodi seguenti.

-   [**Metodo IInkAnalyzer:: SaveResults**](iinkanalyzer-saveresults.md)
-   [**Metodo IInkAnalyzer:: SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)
-   [**Metodo IInkAnalyzer:: SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md)

Per caricare i risultati salvati, usare il [**Metodo IInkAnalyzer:: LoadResults**](iinkanalyzer-loadresults.md).

Per altre informazioni sull'uso di **IInkAnalyzer** per analizzare l'input penna, vedere [Cenni preliminari sull'analisi dell'input penna](ink-analysis-overview.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


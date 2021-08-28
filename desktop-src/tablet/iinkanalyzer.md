---
description: Fornisce accesso all'analisi del layout, alla classificazione di scrittura e disegno e al riconoscimento della grafia.
ms.assetid: 3a19db78-df14-43c2-9e3e-8cf674aa7b9c
title: Interfaccia IInkAnalyzer (IACom.h)
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
ms.openlocfilehash: b37e6d72b87ac31bda7e6c9b0d6f9bf3d35af524eea201e446b50905447404b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939851"
---
# <a name="iinkanalyzer-interface"></a>Interfaccia IInkAnalyzer

Fornisce accesso all'analisi del layout, alla classificazione di scrittura e disegno e al riconoscimento della grafia.

## <a name="members"></a>Membri

**L'interfaccia IInkAnalyzer** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IInkAnalyzer** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IInkAnalyzer** include questi metodi.



| Metodo                                                                                                  | Descrizione                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interrompere**](iinkanalyzer-abort.md)                                                                     | Annulla l'operazione di analisi corrente.<br/>                                                                                                                                           |
| [**AddStroke**](iinkanalyzer-addstroke.md)                                                             | Aggiunge i dati del tratto per un singolo tratto a **IInkAnalyzer** e assegna l'identificatore delle impostazioni cultura del thread di input attivo al tratto.<br/>                                              |
| [**AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)                                       | Aggiunge i dati del tratto per un singolo tratto a **IInkAnalyzer** e assegna un identificatore delle impostazioni cultura specifico al tratto.<br/>                                                             |
| [**AddStrokes**](iinkanalyzer-addstrokes.md)                                                           | Aggiunge i dati del tratto per più tratti a **IInkAnalyzer** e assegna l'identificatore delle impostazioni cultura del thread di input attivo ai tratti.<br/>                                            |
| [**AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)                                     | Aggiunge i dati del tratto per più tratti a **IInkAnalyzer** e assegna l'identificatore delle impostazioni cultura specificato ai tratti.<br/>                                                        |
| [**AddStrokesToCustomRecognizer**](iinkanalyzer-addstrokestocustomrecognizer.md)                       | Aggiunge i dati del tratto per più tratti a un nodo del riconoscitore personalizzato.<br/>                                                                                                                |
| [**AddStrokeToCustomRecognizer**](iinkanalyzer-addstroketocustomrecognizer.md)                         | Aggiunge i dati del tratto per un singolo tratto a un nodo del riconoscitore personalizzato.<br/>                                                                                                                 |
| [**Analizzare**](iinkanalyzer-analyze.md)                                                                 | Esegue l'analisi sincrona dell'input penna.<br/>                                                                                                                                                |
| [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)                                             | Esegue l'analisi asincrona dell'input penna.<br/>                                                                                                                                               |
| [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md)                                                 | Cancella i dati dei pacchetti di tratti **da IInkAnalyzer.**<br/>                                                                                                                              |
| [**CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)                                           | Aggiunge un nuovo nodo dei suggerimenti di analisi con un'area infinita a **IInkAnalyzer.**<br/>                                                                                                      |
| [**CreateContextNodes**](iinkanalyzer-createcontextnodes.md)                                           | Crea un [**oggetto IContextNodes.**](icontextnodes.md)<br/>                                                                                                                         |
| [**CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)                                   | Crea un nuovo nodo di riconoscimento personalizzato per **L'oggetto IInkAnalyzer.**<br/>                                                                                                                    |
| [**DeleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)                                           | Rimuove un hint di analisi da **IInkAnalyzer.**<br/>                                                                                                                               |
| [**FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)                                               | Recupera tutti i nodi foglia dell'input penna.<br/>                                                                                                                                              |
| [**FindInkLeafNodesForStrokes**](iinkanalyzer-findinkleafnodesforstrokes.md)                           | Recupera i nodi foglia dell'input penna che contengono i tratti specificati.<br/>                                                                                                                  |
| [**FindLeafNodes**](iinkanalyzer-findleafnodes.md)                                                     | Recupera tutti i nodi foglia.<br/>                                                                                                                                                  |
| [**FindNode**](iinkanalyzer-findnode.md)                                                               | Recupera [**l'oggetto IContextNode**](icontextnode.md) per un identificatore univoco globale (GUID) specificato.<br/>                                                                      |
| [**Findnodesoftype**](iinkanalyzer-findnodesoftype.md)                                                 | Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) del tipo specificato.<br/>                                                                                          |
| [**FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)                             | Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) del tipo specificato che contengono i tratti specificati.<br/>                                                       |
| [**FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)                               | Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) del tipo specificato discendenti **dell'oggetto IContextNode** specificato.<br/>                            |
| [**FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)                                     | Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) che corrispondono ai criteri specificati.<br/>                                                                              |
| [**FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)                   | Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) che corrispondono ai criteri specificati e sono discendenti dell'oggetto **IContextNode** specificato.<br/>                 |
| [**Getalternates**](iinkanalyzer-getalternates.md)                                                     | Recupera 10 alternative di analisi per tutto l'input penna associato a **IInkAnalyzer.**<br/>                                                                                                |
| [**GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)                       | Recupera le alternative di analisi per i nodi in una raccolta [**IContextNodes**](icontextnodes.md) specificata.<br/>                                                                     |
| [**GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)                                 | Recupera le alternative di analisi per i tratti con gli identificatori di tratto specificati.<br/>                                                                                              |
| [**GetAnalysisHints**](iinkanalyzer-getanalysishints.md)                                               | Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) dell'hint di analisi collegati a **IInkAnalyzer.**<br/>                                                        |
| [**GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)                                   | Recupera tutti gli oggetti [**IContextNode**](icontextnode.md) dell'hint di analisi associati a **IInkAnalyzer** e con il nome specificato.<br/>                       |
| [**GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)                                               | Recupera i flag che controllano il modo in cui **IInkAnalyzer esegue** l'analisi dell'input penna.<br/>                                                                                                      |
| [**GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)                                                   | Recupera l'area modificata dopo l'ultima operazione di analisi.<br/>                                                                                                            |
| [**GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)         | Recupera una raccolta ordinata [**di oggetti IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)<br/>                                                                              |
| [**GetNodesFromTextRange**](iinkanalyzer-getnodesfromtextrange.md)                                     | Recupera una raccolta di oggetti [**IContextNode**](icontextnode.md) rilevanti per l'intervallo di testo specificato per i nodi di contesto specificati.<br/>                             |
| [**GetRecognizedString**](iinkanalyzer-getrecognizedstring.md)                                         | Recupera la stringa con il risultato migliore dell'operazione di riconoscimento per l'intero albero del nodo di contesto in **IInkAnalyzer.**<br/>                                                           |
| [**GetRootNode**](iinkanalyzer-getrootnode.md)                                                         | Recupera [**l'elemento IContextNode radice**](icontextnode.md) dell'albero di contesto **dell'oggetto IInkAnalyzer.**<br/>                                                                            |
| [**GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md)                                         | Recupera l'identificatore delle impostazioni locali del tratto specificato.<br/>                                                                                                                          |
| [**GetStrokeType**](iinkanalyzer-getstroketype.md)                                                     | Recupera il tipo del tratto specificato.<br/>                                                                                                                                       |
| [**GetTextRangeFromNodes**](iinkanalyzer-gettextrangefromnodes.md)                                     | Trova l'intervallo di testo nella stringa riconosciuta che corrisponde a una raccolta di [**oggetti IContextNode.**](icontextnode.md)<br/>                                                   |
| [**Analisi di isanalisi**](iinkanalyzer-isanalyzing.md)                                                         | Recupera un valore che indica se **IInkAnalyzer** sta eseguendo l'analisi dell'input penna.<br/>                                                                                             |
| [**Valori loadResults**](iinkanalyzer-loadresults.md)                                                         | Carica i risultati dell'analisi salvati in **IInkAnalyzer.**<br/>                                                                                                                           |
| [**ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)                                           | Modifica l'oggetto alternativo superiore corrente in quello alternativo specificato e cancella il tipo di conferma per tutti gli oggetti [**IContextNode**](icontextnode.md) associati all'alternativa.<br/> |
| [**ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)           | Modifica l'oggetto alternativo superiore corrente [**nell'oggetto IAnalysisAlternate specificato.**](ianalysisalternate.md)<br/>                                                                              |
| [**Reconcile**](iinkanalyzer-reconcile.md)                                                             | Determina quali parti dei risultati dell'analisi sono state modificate durante l'analisi dell'input penna in background.<br/>                                                                                    |
| [**RemoveStroke**](iinkanalyzer-removestroke.md)                                                       | Rimuove il tratto specificato da **IInkAnalyzer.**<br/>                                                                                                                           |
| [**RemoveStrokes**](iinkanalyzer-removestrokes.md)                                                     | Rimuove i tratti specificati da **IInkAnalyzer.**<br/>                                                                                                                          |
| [**SaveResults**](iinkanalyzer-saveresults.md)                                                         | Salva tutti i risultati dell'analisi per **un oggetto IInkAnalyzer.**<br/>                                                                                                                               |
| [**SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)                                         | Salva i risultati dell'analisi per una raccolta di nodi di contesto specifica associata a **un oggetto IInkAnalyzer.**<br/>                                                                                |
| [**SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md)                                     | Salva i risultati dell'analisi per i tratti specificati associati a **un oggetto IInkAnalyzer.**<br/>                                                                                             |
| [**Cerca**](iinkanalyzer-search.md)                                                                   | Fornisce una ricerca fuzzy basata su frasi senza distinzione tra maiuscole e minuscole per i tratti di scrittura analizzati e i tratti di disegno analizzati con tipi riconosciuti.<br/>                                      |
| [**SearchWithLanguageId**](iinkanalyzer-searchwithlanguageid.md)                                       | Fornisce una ricerca fuzzy basata su frasi senza distinzione tra maiuscole e minuscole per i tratti di scrittura analizzati e i tratti di disegno analizzati con tipi riconosciuti.<br/>                                      |
| [**SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)                                               | Modifica i flag che controllano il modo in cui **IInkAnalyzer esegue** l'analisi dell'input penna.<br/>                                                                                                       |
| [**SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)                                                   | Modifica l'area modificata dopo l'ultima operazione di analisi.<br/>                                                                                                             |
| [**SetHighestPriorityInkAnalysisRecognizer**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) | Sposta [**l'oggetto IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) specificato nella prima posizione nell'elenco di riconoscitori input penna dell'oggetto **IInkAnalyzer.**<br/>                      |
| [**SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md)                                         | Modifica l'identificatore delle impostazioni locali per il tratto specificato.<br/>                                                                                                                           |
| [**SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md)                                       | Modifica l'identificatore delle impostazioni locali per i tratti specificati.<br/>                                                                                                                          |
| [**SetStrokesType**](iinkanalyzer-setstrokestype.md)                                                   | Modifica il tipo dei tratti specificati.<br/>                                                                                                                                        |
| [**SetStrokeType**](iinkanalyzer-setstroketype.md)                                                     | Modifica il tipo del tratto specificato.<br/>                                                                                                                                         |
| [**UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md)                                             | Aggiorna i dati del pacchetto per i tratti specificati.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Commenti

**IInkAnalyzer usa i** dati dei pacchetti di tratti per analizzare l'input penna e non interagisce direttamente con gli oggetti [**InkDisp Class**](inkdisp-class.md) o [InkStrokes Collection.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))

Per aggiungere o rimuovere tratti in **IInkAnalyzer** per l'analisi, usare uno dei metodi seguenti.

-   [**Metodo IInkAnalyzer::AddStroke**](iinkanalyzer-addstroke.md)
-   [**Metodo IInkAnalyzer::AddStrokes**](iinkanalyzer-addstrokes.md)
-   [**Metodo IInkAnalyzer::RemoveStroke**](iinkanalyzer-removestroke.md)
-   [**Metodo IInkAnalyzer::RemoveStrokes**](iinkanalyzer-removestrokes.md)

Questi metodi aggiornano l'area dirty (vedere il metodo [**IInkAnalyzer::GetDirtyRegion),**](iinkanalyzer-getdirtyregion.md)che è l'area per cui i tratti vengono analizzati nella successiva operazione di analisi.

Per analizzare l'input penna, usare il metodo [**IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md) o il metodo [**IInkAnalyzer::BackgroundAnalyze.**](iinkanalyzer-backgroundanalyze.md) Durante l'analisi, **IInkAnalyzer esegue** l'analisi del layout, la classificazione dei tratti e il riconoscimento della grafia.

Per modificare le impostazioni di analisi del layout e classificazione dei tratti, usare la proprietà [**Metodo IInkAnalyzer::SetAnalysisModes.**](iinkanalyzer-setanalysismodes.md)

Durante l'analisi, **IInkAnalyzer** riceve una serie di eventi, inclusi gli eventi generati durante l'analisi in background. [**\_ IAnalysisProxyEvents supporta**](-ianalysisproxyevents.md) le funzionalità proxy dati di **IInkAnalyzer.** Per altre informazioni, vedere [Proxy dati con analisi input penna.](data-proxy-with-ink-analysis.md) Per arrestare il processo di analisi dall'interno di un gestore eventi, chiamare il metodo [**IInkAnalyzer::Abort**](iinkanalyzer-abort.md).

Per modificare la lingua utilizzata dall'analizzatore input penna per riconoscere la grafia, usare il metodo [**IInkAnalyzer::SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md) o il metodo [**IInkAnalyzer::SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md). Per modificare il modo in cui l'analizzatore input penna classifica tratti specifici, usare il metodo [**IInkAnalyzer::SetStrokeType**](iinkanalyzer-setstroketype.md) o il metodo [**IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md).

**IInkAnalyzer carica** informazioni per tutti i riconoscitori input penna installati. Il metodo [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) restituisce una raccolta [**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md) contenente ogni [**IInkAnalysisRecognizer disponibile.**](iinkanalysisrecognizer.md) Se più riconoscitori input penna supportano una lingua specifica, usare il metodo [**IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) per impostare quale riconoscimento input penna gestisce i tratti per tale lingua.

L'uso di hint di analisi può migliorare l'accuratezza del riconoscimento fornendo contesto aggiuntivo all'analizzatore input penna. Le informazioni aggiuntive sul contesto consentono all'analizzatore input penna di limitare il numero di possibili risultati di riconoscimento. Ad esempio, è possibile restringere l'ambito definendo factoid e parole previste o strutturando l'input in una guida al riconoscimento. Per altre informazioni su come fornire contesto all'analizzatore input penna, vedere:

-   [**Metodo IInkAnalyzer::CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)
-   [**Metodo IInkAnalyzer::D eleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)
-   [**Metodo IInkAnalyzer::GetAnalysisHints**](iinkanalyzer-getanalysishints.md)
-   [**Metodo IInkAnalyzer::GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)

L'analizzatore input penna rappresenta i risultati dell'analisi come stringa o come albero di [**oggetti IContextNode.**](icontextnode.md) Per accedere alla stringa riconosciuta, usare [**il metodo IInkAnalyzer::GetRecognizedString**](iinkanalyzer-getrecognizedstring.md). Per accedere alla radice dell'albero del nodo di contesto, usare [**il metodo IInkAnalyzer::GetRootNode**](iinkanalyzer-getrootnode.md). L'analizzatore input penna ha i metodi seguenti per trovare testo o nodi di contesto specifici.

-   [**Metodo IInkAnalyzer::FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)
-   [**Metodo IInkAnalyzer::FindInkLeafNodesForStrokes**](iinkanalyzer-findinkleafnodesforstrokes.md)
-   [**Metodo IInkAnalyzer::FindLeafNodes**](iinkanalyzer-findleafnodes.md)
-   [**Metodo IInkAnalyzer::FindNode**](iinkanalyzer-findnode.md)
-   [**Metodo IInkAnalyzer::FindNodesOfType**](iinkanalyzer-findnodesoftype.md)
-   [**Metodo IInkAnalyzer::FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)
-   [**Metodo IInkAnalyzer::FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)
-   [**Metodo IInkAnalyzer::FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
-   [**Metodo IInkAnalyzer::FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)

Per usare risultati di analisi alternativi, usare uno dei metodi seguenti.

-   [**Metodo IInkAnalyzer::GetAlternates**](iinkanalyzer-getalternates.md)
-   [**Metodo IInkAnalyzer::GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)
-   [**Metodo IInkAnalyzer::GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)
-   [**Metodo IInkAnalyzer::ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)
-   [**Metodo IInkAnalyzer::ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)

Per salvare i risultati dell'analisi, usare uno dei metodi seguenti.

-   [**Metodo IInkAnalyzer::SaveResults**](iinkanalyzer-saveresults.md)
-   [**Metodo IInkAnalyzer::SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)
-   [**Metodo IInkAnalyzer::SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md)

Per caricare i risultati salvati, usare [**il metodo IInkAnalyzer::LoadResults**](iinkanalyzer-loadresults.md).

Per altre informazioni sull'uso di **IInkAnalyzer** per analizzare l'input penna, vedere Cenni preliminari [sull'analisi dell'input penna.](ink-analysis-overview.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Analysismodes**](analysismodes.md)
</dt> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 


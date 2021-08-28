---
description: Queste costanti definiscono valori che specificano il tipo di oggetti IContextNode.
ms.assetid: 333db79e-f503-4545-84fd-7c1a39a96728
title: Tipi di nodo di contesto (Iaguid.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNT_ANALYSISHINT
- GUID_CNT_CUSTOMRECOGNIZER
- GUID_CNT_IMAGE
- GUID_CNT_INKBULLET
- GUID_CNT_INKDRAWING
- GUID_CNT_INKWORD
- GUID_CNT_LINE
- GUID_CNT_OBJECT
- GUID_CNT_PARAGRAPH
- GUID_CNT_ROOT
- GUID_CNT_TEXTWORD
- GUID_CNT_UNCLASSIFIEDINKNODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 2bb2064cc72b398d290fa78606b31bd37208535e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473887"
---
# <a name="context-node-types"></a>Tipi di nodo di contesto

Queste costanti definiscono valori che specificano il tipo di [**oggetti IContextNode.**](icontextnode.md)




| Costante/valore | Descrizione | 
|----------------|-------------|
| <span id="GUID_CNT_ANALYSISHINT"></span><span id="guid_cnt_analysishint"></span><dl><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt><dt>(AnalysisHint)</dt></dl> | Rappresenta un nodo che contiene informazioni di contesto aggiuntive per un'area utilizzata da <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> per migliorarne l'analisi.<br /> | 
| <span id="GUID_CNT_CUSTOMRECOGNIZER"></span><span id="guid_cnt_customrecognizer"></span><dl><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt><dt>(CustomRecognizer)</dt></dl> | Rappresenta un nodo utilizzato per una singola operazione di riconoscimento.<br /> Tutti i tratti e i nodi all'interno di un nodo di riconoscimento personalizzato vengono riconosciuti da un'operazione di riconoscimento indipendente e non vengono analizzati da <a href="iinkanalyzer.md"><strong>IInkAnalyzer.</strong></a><br /> Un nodo di riconoscimento personalizzato deve essere l'elemento figlio diretto del nodo radice dell'analizzatore input penna.<br /> Un nodo di riconoscimento personalizzato può contenere i tipi di elementi figlio seguenti:<br /><ul><li>Qualsiasi numero di nodi UnclassifiedInk.</li><li>Numero qualsiasi di nodi Object.</li><li>Qualsiasi numero di nodi Line.</li><li>Qualsiasi numero di nodi InkWord.</li><li>Qualsiasi numero di nodi con un valore Guid sconosciuto.</li></ul> | 
| <span id="GUID_CNT_IMAGE"></span><span id="guid_cnt_image"></span><dl><dt><strong>GUID_CNT_IMAGE</strong></dt><dt>(immagine)</dt></dl> | Rappresenta un nodo per un'area bidimensionale in cui possono esistere immagini non a penna nel documento.<br /> <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> non produce nodi immagine. Usare <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode</strong></a> per aggiungere un nodo immagine all'albero del nodo di contesto. <strong>IInkAnalyzer</strong> usa quindi le aree definite dal nodo immagine per determinare se un input penna annota l'immagine non input penna.<br /> Un nodo immagine non può avere elementi figlio.<br /> | 
| <span id="GUID_CNT_INKBULLET"></span><span id="guid_cnt_inkbullet"></span><dl><dt><strong>GUID_CNT_INKBULLET</strong></dt><dt>(InkBullet)</dt></dl> | InkBullet ContextNodeType rappresenta una raccolta di tratti che costituiscono un punto elenco in un elenco puntato.<br /> Un elemento ContextNode di tipo InkBullet non può avere elementi figlio. Può essere solo un elemento figlio di un oggetto ContextNode paragraph. Un solo InkBullet può essere visualizzato in un singolo ContextNode di paragrafo.<br /> | 
| <span id="GUID_CNT_INKDRAWING"></span><span id="guid_cnt_inkdrawing"></span><dl><dt><strong>GUID_CNT_INKDRAWING</strong></dt><dt>(InkDrawing)</dt></dl> | Rappresenta un nodo per una raccolta di tratti che costituisce un disegno.<br /> I disegni sono tratti determinati come forme o disegni astratti. Si tratta in genere di tratti non classificati come tratti di scrittura.<br /> Un nodo di disegno a penna non può avere elementi figlio.<br /> | 
| <span id="GUID_CNT_INKWORD"></span><span id="guid_cnt_inkword"></span><dl><dt><strong>GUID_CNT_INKWORD</strong></dt><dt>(InkWord)</dt></dl> | Rappresenta un nodo per una raccolta di tratti che costituisce un raggruppamento logico per formare una parola riconoscibile.<br /> Un nodo di parole input penna non può contenere elementi figlio.<br /> | 
| <span id="GUID_CNT_LINE"></span><span id="guid_cnt_line"></span><dl><dt><strong>GUID_CNT_LINE</strong></dt><dt>(riga)</dt></dl> | Rappresenta un nodo per una riga di parole.<br /> Un nodo riga può contenere i tipi di elementi figlio seguenti:<br /><ul><li>Qualsiasi numero di nodi di parole input penna.</li><li>Qualsiasi numero di nodi di parole di testo.</li><li>Qualsiasi numero di nodi con un valore <strong>GUID</strong> sconosciuto.</li></ul> | 
| <span id="GUID_CNT_OBJECT"></span><span id="guid_cnt_object"></span><dl><dt><strong>GUID_CNT_OBJECT</strong></dt><dt>(oggetto)</dt></dl> | Rappresenta un nodo per un oggetto restituito da un riconoscitore personalizzato "oggetto".<br /> Un nodo oggetto non può contenere elementi figlio.<br /> Solo i nodi di riconoscimento personalizzati possono contenere nodi oggetto.<br /> | 
| <span id="GUID_CNT_PARAGRAPH"></span><span id="guid_cnt_paragraph"></span><dl><dt><strong>GUID_CNT_PARAGRAPH</strong></dt><dt>(paragrafo)</dt></dl> | Rappresenta un nodo per una raccolta di nodi che costituisce un raggruppamento logico di righe.<br /> La definizione esatta di un paragrafo è determinata dai motori di analisi. In generale, un paragrafo contiene gruppi di righe che verrebbero riflusso se la casella contenente le righe fosse stata ridimensionata.<br /> Un nodo paragrafo può contenere i tipi di elementi figlio seguenti:<br /><ul><li>Qualsiasi numero di nodi punto elenco a penna.</li><li>Qualsiasi numero di nodi di riga.</li><li>Qualsiasi numero di nodi con un valore <strong>GUID</strong> sconosciuto.</li></ul> | 
| <span id="GUID_CNT_ROOT"></span><span id="guid_cnt_root"></span><dl><dt><strong>GUID_CNT_ROOT</strong></dt><dt>(radice)</dt></dl> | Rappresenta un nodo per il nodo superiore di un albero di nodi che descrivono i risultati dell'analisi dell'input penna.<br /> I nodi radice vengono in genere ottenuti dal <a href="iinkanalyzer-getrootnode.md"><strong>metodo IInkAnalyzer::GetRootNode.</strong></a><br /> Un nodo radice può contenere i tipi seguenti di elementi figlio:<br /><ul><li>Qualsiasi numero di nodi hint di analisi.</li><li>Numero qualsiasi di nodi di riconoscimento personalizzati.</li><li>Qualsiasi numero di nodi immagine.</li><li>Qualsiasi numero di nodi di disegno a penna.</li><li>Numero qualsiasi di nodi dell'area di scrittura.</li><li>Numero qualsiasi di nodi input penna non classificati.</li><li>Qualsiasi numero di nodi con un valore <strong>GUID</strong> sconosciuto.</li></ul> | 
| <span id="GUID_CNT_TEXTWORD"></span><span id="guid_cnt_textword"></span><dl><dt><strong>GUID_CNT_TEXTWORD</strong></dt><dt>(TextWord)</dt></dl> | Rappresenta un nodo per l'area bidimensionale in cui può essere presente qualsiasi testo non input penna nel documento.<br /> <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> non produce nodi di testo. Usare <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode</strong></a> per aggiungere un nodo di parola di testo all'albero del nodo di contesto. <strong>IInkAnalyzer</strong> usa quindi le aree definite dal nodo della parola di testo per determinare se un input penna annota il testo non input penna.<br /> I riconoscitori futuri possono usare l'area definita da un nodo di parole di testo per determinare se un input penna annota la parola non input penna.<br /> Un nodo di parole di testo non può avere elementi figlio<br /> | 
| <span id="GUID_CNT_UNCLASSIFIEDINKNODE"></span><span id="guid_cnt_unclassifiedinknode"></span><dl><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt><dt>(UnclassifiedInk)</dt></dl> | Rappresenta un nodo per tutti i tratti che non sono ancora stati classificati o riconosciuti.<br /> Un nodo input penna non classificato non può avere elementi figlio.<br /> | 




## <a name="remarks"></a>Commenti

Per altre informazioni sui diversi tipi di nodo di contesto, vedere [Cenni preliminari sull'analisi input penna](ink-analysis-overview.md).

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Iaguid.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[**IContextNode::GetType**](icontextnode-gettype.md)
</dt> <dt>

[**Metodo IInkAnalyzer::CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**Metodo IInkAnalyzer::CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNodesOfType**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





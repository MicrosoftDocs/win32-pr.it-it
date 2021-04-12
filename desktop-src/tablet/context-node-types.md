---
description: Queste costanti definiscono i valori che specificano il tipo di oggetti IContextNode.
ms.assetid: 333db79e-f503-4545-84fd-7c1a39a96728
title: Tipi di nodo di contesto (Iaguid. h)
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
ms.openlocfilehash: 918b7cf818ebcedc98f45bff7c41ee66ad4d1592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127815"
---
# <a name="context-node-types"></a>Tipi di nodo di contesto

Queste costanti definiscono i valori che specificano il tipo di oggetti [**IContextNode**](icontextnode.md) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante/valore</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_ANALYSISHINT"></span><span id="guid_cnt_analysishint"></span><dl> <dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt>(ANALYSISHINT)</dt> </dl></td>
<td style="text-align: left;">Rappresenta un nodo che contiene informazioni aggiuntive sul contesto per un'area utilizzata da <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> per migliorare l'analisi.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_CUSTOMRECOGNIZER"></span><span id="guid_cnt_customrecognizer"></span><dl> <dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt>(CUSTOMRECOGNIZER)</dt> </dl></td>
<td style="text-align: left;">Rappresenta un nodo utilizzato per una singola operazione di riconoscimento.<br/> Tutti i tratti e i nodi all'interno di un nodo di riconoscimento personalizzato sono riconosciuti da un'operazione di riconoscimento indipendente e non vengono analizzati da <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>.<br/> Un nodo di riconoscimento personalizzato deve essere il figlio diretto del nodo radice dell'analizzatore di input penna.<br/> Un nodo di riconoscimento personalizzato può contenere i seguenti tipi di elementi figlio:<br/>
<ul>
<li>Qualsiasi numero di nodi UnclassifiedInk.</li>
<li>Qualsiasi numero di nodi oggetto.</li>
<li>Qualsiasi numero di nodi riga.</li>
<li>Qualsiasi numero di nodi InkWord.</li>
<li>Qualsiasi numero di nodi con un valore Guid sconosciuto.</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_IMAGE"></span><span id="guid_cnt_image"></span><dl> <dt><strong>GUID_CNT_IMAGE</strong></dt> <dt>(immagine)</dt> </dl></td>
<td style="text-align: left;">Rappresenta un nodo per un'area bidimensionale in cui è possibile che nel documento siano presenti immagini non input penna.<br/> <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> non produce nodi Image. Usare <a href="icontextnode-createsubnode.md"><strong>IContextNode:: CreateSubNode</strong></a> per aggiungere un nodo immagine alla struttura ad albero del nodo di contesto. Il <strong>IInkAnalyzer</strong> usa quindi le aree definite dal nodo immagine per determinare se un input penna annota l'immagine non input penna.<br/> Un nodo immagine non può contenere elementi figlio.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKBULLET"></span><span id="guid_cnt_inkbullet"></span><dl> <dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt>(INKBULLET)</dt> </dl></td>
<td style="text-align: left;">InkBullet ContextNodeType rappresenta una raccolta di tratti che costituiscono un punto elenco in un elenco puntato.<br/> Un oggetto ContextNode di tipo InkBullet non può contenere elementi figlio. Può essere solo un elemento figlio di un oggetto ContextNode di paragrafo. In un singolo oggetto ContextNode di paragrafo può essere presente un solo InkBullet.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_INKDRAWING"></span><span id="guid_cnt_inkdrawing"></span><dl> <dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt>(INKDRAWING)</dt> </dl></td>
<td style="text-align: left;">Rappresenta un nodo per una raccolta di tratti che costituisce un disegno.<br/> I disegni sono tratti che vengono determinati come forme o sketch astratti. Si tratta in genere di tratti non classificati come tratti di scrittura.<br/> Un nodo di disegno input penna non può contenere elementi figlio.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKWORD"></span><span id="guid_cnt_inkword"></span><dl> <dt><strong>GUID_CNT_INKWORD</strong></dt> <dt>(InkWord)</dt> </dl></td>
<td style="text-align: left;">Rappresenta un nodo per una raccolta di tratti che costituisce un raggruppamento logico per formare una parola riconoscibile.<br/> Un nodo di Word di input penna non può contenere elementi figlio.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_LINE"></span><span id="guid_cnt_line"></span><dl> <dt><strong>GUID_CNT_LINE</strong></dt> <dt>(riga)</dt> </dl></td>
<td style="text-align: left;">Rappresenta un nodo per una riga di parole.<br/> Un nodo linea può contenere i seguenti tipi di elementi figlio:<br/>
<ul>
<li>Qualsiasi numero di nodi di Word di input penna.</li>
<li>Qualsiasi numero di nodi di testo alfanumerici.</li>
<li>Qualsiasi numero di nodi con un valore <strong>GUID</strong> sconosciuto.</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_OBJECT"></span><span id="guid_cnt_object"></span><dl> <dt><strong>GUID_CNT_OBJECT</strong></dt> <dt>(oggetto)</dt> </dl></td>
<td style="text-align: left;">Rappresenta un nodo per un oggetto restituito da un &quot; riconoscimento personalizzato di un oggetto &quot; .<br/> Un nodo oggetto non può contenere elementi figlio.<br/> Solo i nodi di riconoscimento personalizzati possono contenere nodi oggetto.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_PARAGRAPH"></span><span id="guid_cnt_paragraph"></span><dl> <dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt>(paragrafo)</dt> </dl></td>
<td style="text-align: left;">Rappresenta un nodo per una raccolta di nodi che costituisce un raggruppamento logico di righe.<br/> La definizione esatta di un paragrafo è determinata dai motori di analisi. In generale, un paragrafo contiene gruppi di righe che vengono riflussi insieme se la casella che contiene le righe è stata ridimensionata.<br/> Un nodo di paragrafo può contenere i seguenti tipi di elementi figlio:<br/>
<ul>
<li>Qualsiasi numero di nodi Bullet input penna.</li>
<li>Qualsiasi numero di nodi riga.</li>
<li>Qualsiasi numero di nodi con un valore <strong>GUID</strong> sconosciuto.</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_ROOT"></span><span id="guid_cnt_root"></span><dl> <dt><strong>GUID_CNT_ROOT</strong></dt> <dt>(radice)</dt> </dl></td>
<td style="text-align: left;">Rappresenta un nodo per il nodo principale di una struttura ad albero di nodi che descrivono i risultati dell'analisi dell'input penna.<br/> I nodi radice vengono in genere ottenuti dal metodo <a href="iinkanalyzer-getrootnode.md"><strong>IInkAnalyzer:: GetRootNode Method</strong></a> .<br/> Un nodo radice può contenere i seguenti tipi di elementi figlio:<br/>
<ul>
<li>Qualsiasi numero di nodi hint di analisi.</li>
<li>Qualsiasi numero di nodi di riconoscimento personalizzati.</li>
<li>Qualsiasi numero di nodi Image.</li>
<li>Qualsiasi numero di nodi di disegno input penna.</li>
<li>Qualsiasi numero di nodi dell'area di scrittura.</li>
<li>Qualsiasi numero di nodi Ink non classificati.</li>
<li>Qualsiasi numero di nodi con un valore <strong>GUID</strong> sconosciuto.</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_TEXTWORD"></span><span id="guid_cnt_textword"></span><dl> <dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt>(TEXTWORD)</dt> </dl></td>
<td style="text-align: left;">Rappresenta un nodo per l'area bidimensionale in cui è possibile che nel documento esista un testo non input penna.<br/> <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> non produce nodi di Word di testo. Usare <a href="icontextnode-createsubnode.md"><strong>IContextNode:: CreateSubNode</strong></a> per aggiungere un nodo della parola di testo all'albero del nodo di contesto. Il <strong>IInkAnalyzer</strong> usa quindi le aree definite dal nodo della parola di testo per determinare se un input penna annota il testo non input penna.<br/> I riconoscitori futuri possono usare l'area definita da un nodo Word di testo per determinare se un input penna annota la parola non input penna.<br/> Un nodo di testo di Word non può contenere elementi figlio<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_UNCLASSIFIEDINKNODE"></span><span id="guid_cnt_unclassifiedinknode"></span><dl> <dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt>(UnclassifiedInk)</dt> </dl></td>
<td style="text-align: left;">Rappresenta un nodo per tutti i tratti che non sono stati ancora classificati o riconosciuti.<br/> Un nodo Ink non classificato non può contenere elementi figlio.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

Per altre informazioni sui diversi tipi di nodo di contesto, vedere [Cenni preliminari sull'analisi dell'input penna](ink-analysis-overview.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Iaguid. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextNode:: CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode:: CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[**IContextNode:: GetType**](icontextnode-gettype.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesOfType**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





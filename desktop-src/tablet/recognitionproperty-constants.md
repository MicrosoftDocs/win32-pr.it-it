---
description: Definisce i valori che specificano le proprietà di un'alternativa di riconoscimento. Il Application Programming Interface di Tablet PC (API) USA identificatori univoci globali (GUID) per identificare le proprietà dei pacchetti, che in automazione sono stringhe costanti.
ms.assetid: 2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8
title: Costanti RecognitionProperty (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62971276b6348af3d8ac971851d70b03f7b003c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348636"
---
# <a name="recognitionproperty-constants"></a>Costanti RecognitionProperty

Definisce i valori che specificano le proprietà di un'alternativa di riconoscimento. Il Application Programming Interface di Tablet PC (API) USA identificatori univoci globali (GUID) per identificare le proprietà dei pacchetti, che in automazione sono stringhe costanti.

La tabella seguente elenca i campi GUID (Globally Unique Identifier) delle proprietà alternative di riconoscimento disponibili. Usare questi GUID per accedere alle proprietà di un oggetto [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) chiamando il metodo [**GetPropertyValue**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Nome costante</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINENUMBER_________"></span><span id="___________inkrecognitionproperty_linenumber_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong></dt> </dl></td>
<td style="text-align: left;">GUID che identifica la proprietà per il numero di riga dell'oggetto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> . <br/> LineNumber specifica le alternative con un numero di riga specifico.<br/>
<blockquote>
[!Note]<br />
Questo campo non è supportato per i riconoscitori dei caratteri asiatici orientali.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_SEGMENTATION_________"></span><span id="___________inkrecognitionproperty_segmentation_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong></dt> </dl></td>
<td style="text-align: left;">GUID che identifica la proprietà per la segmentazione dell'oggetto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> . <br/> Segmentazione specifica il frammento di input o l'unità di base che il riconoscimento USA per produrre un risultato del riconoscimento.<br/>
<blockquote>
[!Note]<br />
Non implementato.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_HOTPOINT_________"></span><span id="___________inkrecognitionproperty_hotpoint_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong></dt> </dl></td>
<td style="text-align: left;">GUID che identifica la proprietà per il punto critico di riconoscimento dell'oggetto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> . <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT_________"></span><span id="___________inkrecognitionproperty_maximumstrokecount_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong></dt> </dl></td>
<td style="text-align: left;">GUID che identifica la proprietà per il numero massimo di tratti del risultato del riconoscimento per l'oggetto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> . <br/>
<blockquote>
[!Note]<br />
Non implementato.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_POINTSPERINCH_________"></span><span id="___________inkrecognitionproperty_pointsperinch_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong></dt> </dl></td>
<td style="text-align: left;">GUID che identifica la proprietà per la metrica dei punti per pollice dell'oggetto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> . <br/>
<blockquote>
[!Note]<br />
Non implementato.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_CONFIDENCELEVEL_________"></span><span id="___________inkrecognitionproperty_confidencelevel_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong></dt> </dl></td>
<td style="text-align: left;">GUID che identifica la proprietà relativa al livello di confidenza del riconoscimento nel risultato del riconoscimento.<br/>
<blockquote>
[!Note]<br />
La valutazione della confidenza è disponibile solo per Stati Uniti lingua inglese e per tutti i riconoscitori di movimento in Microsoft Windows XP Tablet PC Edition e Windows Vista. Metodi che forniscono la proprietà confidenza per qualsiasi altro riconoscitore restituito E_NOTIMPL.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINEMETRICS_________"></span><span id="___________inkrecognitionproperty_linemetrics_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong></dt> </dl></td>
<td style="text-align: left;">GUID che identifica la proprietà per le metriche della riga dell'oggetto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate</strong></a> , ovvero la riga per la quale recuperare le metriche. <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

In C++ è possibile accedere a queste costanti nel file di intestazione Msinkaut. h, che si trova nella <systemdrive> \\ Directory: programmi \\ Microsoft SDK \\ Windows \\ v 6.0 \\ include directory se è stato installato l'SDK nel percorso predefinito.

> [!Note]  
> In C++, queste costanti sono WCHAR, non BSTR. Convertirli in BSTR prima di usarli. Per ulteriori informazioni sul tipo di dati BSTR, vedere [utilizzo della libreria com](using-the-com-library.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo AlternatesWithConstantPropertyValues**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues)
</dt> <dt>

[**Proprietà ConfidenceAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidencealternates)
</dt> <dt>

[**Proprietà LineAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linealternates)
</dt> <dt>

[**Interfaccia IInkRecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates)
</dt> </dl>

 

 





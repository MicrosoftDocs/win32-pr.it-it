---
description: Definisce i valori che specificano le proprietà di un'alternativa di riconoscimento. L'API (Application Programming Interface) per Tablet PC usa identificatori univoci globali (GUID) per identificare le proprietà dei pacchetti, che in Automazione sono stringhe costanti.
ms.assetid: 2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8
title: Costanti RecognitionProperty (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd18aeae50e0ae08337dd89a494292a7accbb389e6d02f0b990035fbf9644879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856422"
---
# <a name="recognitionproperty-constants"></a>Costanti RecognitionProperty

Definisce i valori che specificano le proprietà di un'alternativa di riconoscimento. L'API (Application Programming Interface) per Tablet PC usa identificatori univoci globali (GUID) per identificare le proprietà dei pacchetti, che in Automazione sono stringhe costanti.

Nella tabella seguente sono elencati i campi dell'identificatore univoco globale (GUID) delle proprietà alternative di riconoscimento disponibili. Usare questi GUID per accedere alle proprietà di un [**oggetto IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) chiamando il [**metodo GetPropertyValue.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue)



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
<td style="text-align: left;">GUID che identifica la proprietà per il numero di riga <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>dell'oggetto IInkRecognitionAlternate.</strong></a> <br/> LineNumber specifica le alternative con un determinato numero di riga.<br/>
<blockquote>
[!Note]<br />
Questo campo non è supportato per i riconoscitori di caratteri dell'Asia orientale.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_SEGMENTATION_________"></span><span id="___________inkrecognitionproperty_segmentation_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong></dt> </dl></td>
<td style="text-align: left;">GUID che identifica la proprietà per la segmentazione <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>dell'oggetto IInkRecognitionAlternate.</strong></a> <br/> La segmentazione specifica il frammento o l'unità di input penna di base che il riconoscimento usa per produrre un risultato di riconoscimento.<br/>
<blockquote>
[!Note]<br />
Non implementato.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_HOTPOINT_________"></span><span id="___________inkrecognitionproperty_hotpoint_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong></dt> </dl></td>
<td style="text-align: left;">GUID che identifica la proprietà per il punto di accesso hot di riconoscimento <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>dell'oggetto IInkRecognitionAlternate.</strong></a> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT_________"></span><span id="___________inkrecognitionproperty_maximumstrokecount_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong></dt> </dl></td>
<td style="text-align: left;">GUID che identifica la proprietà per il numero massimo di tratti del risultato del riconoscimento per <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>l'oggetto IInkRecognitionAlternate.</strong></a> <br/>
<blockquote>
[!Note]<br />
Non implementato.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_POINTSPERINCH_________"></span><span id="___________inkrecognitionproperty_pointsperinch_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong></dt> </dl></td>
<td style="text-align: left;">GUID che identifica la proprietà per la metrica punti per pollice <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>dell'oggetto IInkRecognitionAlternate.</strong></a> <br/>
<blockquote>
[!Note]<br />
Non implementato.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_CONFIDENCELEVEL_________"></span><span id="___________inkrecognitionproperty_confidencelevel_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong></dt> </dl></td>
<td style="text-align: left;">GUID che identifica la proprietà per il livello di attendibilità del riconoscimento nel risultato del riconoscimento.<br/>
<blockquote>
[!Note]<br />
La valutazione dell'attendibilità è disponibile solo per Stati Uniti inglese e per tutti i riconoscitori movimenti in Microsoft Windows XP Tablet PC Edition e Windows Vista. I metodi che forniscono la proprietà di attendibilità per qualsiasi altro sistema di riconoscimento restituiscono E_NOTIMPL.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________INKRECOGNITIONPROPERTY_LINEMETRICS_________"></span><span id="___________inkrecognitionproperty_linemetrics_________"></span><dl> <dt><strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong></dt> </dl></td>
<td style="text-align: left;">GUID che identifica la proprietà per le metriche di linea dell'oggetto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate,</strong></a> ovvero la riga per la quale recuperare le metriche. <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

In C++ è possibile accedere a queste costanti nel file di intestazione Msinkaut.h, che si trova nella <systemdrive> directory : Programmi Microsoft \\ \\ SDKs \\ Windows \\ v6.0 \\ Include se l'SDK è stato installato nel percorso predefinito.

> [!Note]  
> In C++ queste costanti sono WCHAR, non BSTR. Convertirli in BSTR prima dell'uso. Per altre informazioni sul tipo di dati BSTR, vedere [Uso della libreria COM.](using-the-com-library.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |



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

 

 





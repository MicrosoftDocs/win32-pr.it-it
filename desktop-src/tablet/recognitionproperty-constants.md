---
description: Definisce i valori che specificano le proprietà di un'alternativa di riconoscimento. L'API (Application Programming Interface) di Tablet PC usa identificatori univoci globali (GUID) per identificare le proprietà dei pacchetti, che in Automazione sono stringhe costanti.
ms.assetid: 2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8
title: Costanti RecognitionProperty (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d06d2eed3b28ed99d180dbe3971e9e018554ff5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467988"
---
# <a name="recognitionproperty-constants"></a>Costanti RecognitionProperty

Definisce i valori che specificano le proprietà di un'alternativa di riconoscimento. L'API (Application Programming Interface) di Tablet PC usa identificatori univoci globali (GUID) per identificare le proprietà dei pacchetti, che in Automazione sono stringhe costanti.

Nella tabella seguente sono elencati i campi dell'identificatore univoco globale (GUID) delle proprietà alternative di riconoscimento disponibili. Usare questi GUID per accedere alle proprietà di [**un oggetto IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) chiamando il [**metodo GetPropertyValue.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-getpropertyvalue)




| Nome costante | Descrizione | 
|---------------|-------------|
| <span id="___________INKRECOGNITIONPROPERTY_LINENUMBER_________"></span><span id="___________inkrecognitionproperty_linenumber_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_LINENUMBER</strong></dt></dl> | GUID che identifica la proprietà per il numero di riga <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>dell'oggetto IInkRecognitionAlternate.</strong></a> <br /> LineNumber specifica le alternative con un numero di riga specifico.<br /><blockquote>[!Note]<br />Questo campo non è supportato per i riconoscitori di caratteri dell'Asia orientale.</blockquote><br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_SEGMENTATION_________"></span><span id="___________inkrecognitionproperty_segmentation_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_SEGMENTATION</strong></dt></dl> | GUID che identifica la proprietà per la segmentazione <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>dell'oggetto IInkRecognitionAlternate.</strong></a> <br /> La segmentazione specifica il frammento o l'unità di input penna di base utilizzata dal riconoscimento per produrre un risultato di riconoscimento.<br /><blockquote>[!Note]<br />Non implementato.</blockquote><br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_HOTPOINT_________"></span><span id="___________inkrecognitionproperty_hotpoint_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_HOTPOINT</strong></dt></dl> | GUID che identifica la proprietà per il punto di riconoscimento <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>dell'oggetto IInkRecognitionAlternate.</strong></a> <br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT_________"></span><span id="___________inkrecognitionproperty_maximumstrokecount_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_MAXIMUMSTROKECOUNT</strong></dt></dl> | GUID che identifica la proprietà per il numero massimo di tratti del risultato del riconoscimento per <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>l'oggetto IInkRecognitionAlternate.</strong></a> <br /><blockquote>[!Note]<br />Non implementato.</blockquote><br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_POINTSPERINCH_________"></span><span id="___________inkrecognitionproperty_pointsperinch_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_POINTSPERINCH</strong></dt></dl> | GUID che identifica la proprietà per la metrica points-per-inch <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>dell'oggetto IInkRecognitionAlternate.</strong></a> <br /><blockquote>[!Note]<br />Non implementato.</blockquote><br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_CONFIDENCELEVEL_________"></span><span id="___________inkrecognitionproperty_confidencelevel_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_CONFIDENCELEVEL</strong></dt></dl> | GUID che identifica la proprietà per il livello di attendibilità del riconoscimento nel risultato del riconoscimento.<br /><blockquote>[!Note]<br />La valutazione dell'attendibilità è disponibile solo Stati Uniti inglese e tutti i riconoscitori movimenti in Microsoft Windows XP Tablet PC Edition e Windows Vista. I metodi che forniscono la proprietà confidence per qualsiasi altro sistema di riconoscimento restituiscono E_NOTIMPL.</blockquote><br /> | 
| <span id="___________INKRECOGNITIONPROPERTY_LINEMETRICS_________"></span><span id="___________inkrecognitionproperty_linemetrics_________"></span><dl><dt><strong>INKRECOGNITIONPROPERTY_LINEMETRICS</strong></dt></dl> | GUID che identifica la proprietà per le metriche di riga dell'oggetto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate"><strong>IInkRecognitionAlternate,</strong></a> ovvero la riga per cui recuperare le metriche. <br /> | 




## <a name="remarks"></a>Commenti

In C++ è possibile accedere a queste costanti nel file di intestazione Msinkaut.h, che si trova nella <systemdrive> directory : Programmi Microsoft SDK Windows \\ \\ \\ \\ v6.0 \\ Include se l'SDK è stato installato nel percorso predefinito.

> [!Note]  
> In C++, queste costanti sono WCHAR, non BSTR. Convertirli in BSTR prima dell'uso. Per altre informazioni sul tipo di dati BSTR, vedere [Uso della libreria COM](using-the-com-library.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                       |
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

 

 





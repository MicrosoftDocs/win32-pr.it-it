---
description: Specifica gli attributi di un IInkAnalysisRecognizer.
ms.assetid: e9577d83-0212-4f2f-88d7-e9153ec9fae5
title: Enumerazione RecognizerCapabilities (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerCapabilities
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 96e932b8e47f323198e1b0cc87da0df7839a593a76850c00c2c2e4d095854851
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091451"
---
# <a name="recognizercapabilities-enumeration"></a>Enumerazione RecognizerCapabilities

Specifica gli attributi di un [**oggetto IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

## <a name="syntax"></a>Sintassi


```C++
typedef enum RecognizerCapabilities { 
  RC_None                            = 0,
  RC_DoNotCare                       = 0x1,
  RC_Object                          = 0x2,
  RC_FreeInput                       = 0x4,
  RC_LinedInput                      = 0x8,
  RC_BoxedInput                      = 0x10,
  RC_CharacterAutoCompletionInput    = 0x20,
  RC_RightAndDown                    = 0x40,
  RC_LeftAndDown                     = 0x80,
  RC_DownAndLeft                     = 0x100,
  RC_DownAndRight                    = 0x200,
  RC_ArbitraryAngle                  = 0x400,
  RC_Lattice                         = 0x800,
  RC_AdviseInkChange                 = 0x1000,
  RC_StrokeReorder                   = 0x2000,
  RC_Personalizable                  = 0x4000,
  RC_PrefersArbitraryAngle           = 0x8000,
  RC_PrefersParagraphBreaking        = 0x10000,
  RC_PrefersSegmentationRecognition  = 0x20000
} InkAnalysisRecognizerCapabilities;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC \_ Nessuno**
</dt> <dd>

Nessuna funzionalità specificata.

</dd> <dt>

<span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**RC \_ DoNotCare**
</dt> <dd>

Ignora tutti gli altri flag impostati.

</dd> <dt>

<span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**Oggetto \_ RC**
</dt> <dd>

Supporta il riconoscimento degli oggetti; in caso contrario, riconosce solo il testo.

</dd> <dt>

<span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**RC \_ FreeInput**
</dt> <dd>

Supporta l'input libero, in cui l'input penna viene immesso senza l'uso di una guida di riconoscimento, ad esempio una linea o una casella.

</dd> <dt>

<span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**RC \_ LinedInput**
</dt> <dd>

Supporta l'input a linee, che è simile alla scrittura su carta a linee.

</dd> <dt>

<span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**RC \_ BoxedInput**
</dt> <dd>

Supporta l'input boxed, in cui ogni carattere o parola viene immesso in una casella.

</dd> <dt>

<span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**RC \_ CharacterAutoCompletionInput**
</dt> <dd>

Supporta il completamento automatico dei caratteri. I riconoscitori che supportano il completamento automatico dei caratteri richiedono l'input boxed.

</dd> <dt>

<span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**RC \_ RightAndDown**
</dt> <dd>

Supporta l'input per la grafia in ordine destro e inferiore, ad esempio nelle lingue occidentali e in alcune lingue dell'Asia orientale.

</dd> <dt>

<span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**RC \_ LeftAndDown**
</dt> <dd>

Supporta l'input per la grafia in ordine sinistro e inferiore, ad esempio nelle lingue ebraiche e arabe.

</dd> <dt>

<span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**RC \_ DownAndLeft**
</dt> <dd>

Supporta l'input per la grafia in ordine inferiore e sinistro, ad esempio in alcune lingue dell'Asia orientale.

</dd> <dt>

<span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**RC \_ DownAndRight**
</dt> <dd>

Supporta l'input per la grafia in ordine inferiore e corretto, ad esempio in alcune lingue dell'Asia orientale.

</dd> <dt>

<span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**RC \_ ArbitraryAngle**
</dt> <dd>

Supporta il testo scritto ad angoli arbitrari.

</dd> <dt>

<span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**RC \_ Lattice**
</dt> <dd>

Supporta la restituzione di un reticolo come stringa alternativa per i risultati del riconoscimento della grafia.

</dd> <dt>

<span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**RC \_ AdviseInkChange**
</dt> <dd>

Supporta l'interruzione del riconoscimento dello sfondo, ad esempio quando l'input penna è stato modificato.

</dd> <dt>

<span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**RC \_ StrokeReorder**
</dt> <dd>

Supporta che l'ordine dei tratti, spaziale e temporale, viene gestito come parte dell'operazione di riconoscimento. [**IInkAnalyzer**](iinkanalyzer.md) non riordina i tratti prima di inviare input penna a [**IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

</dd> <dt>

<span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**RC \_ Personalizable**
</dt> <dd>

Supporta la grafia personalizzata, in cui il riconoscimento migliora il riconoscimento quando è esposto alla stessa grafia nel tempo.

</dd> <dt>

<span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**RC \_ PrefersArbitraryAngle**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) non deve ruotare la grafia su un orientamento orizzontale prima di inviare l'input penna a [**IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

</dd> <dt>

<span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**RC \_ PreferisceParagraphBreaking**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) deve inviare interi paragrafi di input penna a [**IInkAnalysisRecognizer,**](iinkanalysisrecognizer.md)consentendo a **IInkAnalysisRecognizer** di eseguire l'interruzione di riga e l'interruzione di parola (o carattere).

</dd> <dt>

<span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**RC \_ PrefersSegmentationRecognition**
</dt> <dd>

Riconosce una sola parola o carattere per ogni operazione di riconoscimento. [**IInkAnalyzer**](iinkanalyzer.md) esegue la segmentazione della grafia e invia un solo segmento alla volta a [**IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione consente una combinazione bit per bit dei relativi valori dei membri. Usare questa enumerazione per trovare un sistema di riconoscimento input penna installato che supporta gli attributi necessari.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalysisRecognizer::GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





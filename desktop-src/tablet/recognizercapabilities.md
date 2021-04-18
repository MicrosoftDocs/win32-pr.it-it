---
description: Specifica gli attributi di un IInkAnalysisRecognizer.
ms.assetid: e9577d83-0212-4f2f-88d7-e9153ec9fae5
title: Enumerazione RecognizerCapabilities (IACom. h)
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
ms.openlocfilehash: b2471e77fec02900804de831fc1197c071b9f566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313445"
---
# <a name="recognizercapabilities-enumeration"></a>Enumerazione RecognizerCapabilities

Specifica gli attributi di un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

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

<span id="RC_None"></span><span id="rc_none"></span><span id="RC_NONE"></span>**RC \_ nessuno**
</dt> <dd>

Nessuna funzionalità specificata.

</dd> <dt>

<span id="RC_DoNotCare"></span><span id="rc_donotcare"></span><span id="RC_DONOTCARE"></span>**\_DONOTCARE RC**
</dt> <dd>

Ignora tutti gli altri flag impostati.

</dd> <dt>

<span id="RC_Object"></span><span id="rc_object"></span><span id="RC_OBJECT"></span>**RC ( \_ oggetto)**
</dt> <dd>

Supporta il riconoscimento degli oggetti. in caso contrario, riconosce solo il testo.

</dd> <dt>

<span id="RC_FreeInput"></span><span id="rc_freeinput"></span><span id="RC_FREEINPUT"></span>**\_FREEINPUT RC**
</dt> <dd>

Supporta l'input libero, in cui viene immesso l'input penna senza utilizzare una guida per il riconoscimento, ad esempio una riga o una casella.

</dd> <dt>

<span id="RC_LinedInput"></span><span id="rc_linedinput"></span><span id="RC_LINEDINPUT"></span>**\_LINEDINPUT RC**
</dt> <dd>

Supporta l'input rigato, che è simile alla scrittura su un foglio di carta.

</dd> <dt>

<span id="RC_BoxedInput"></span><span id="rc_boxedinput"></span><span id="RC_BOXEDINPUT"></span>**\_BOXEDINPUT RC**
</dt> <dd>

Supporta l'input boxed, in cui ogni carattere o parola viene immesso in una casella.

</dd> <dt>

<span id="RC_CharacterAutoCompletionInput"></span><span id="rc_characterautocompletioninput"></span><span id="RC_CHARACTERAUTOCOMPLETIONINPUT"></span>**\_CHARACTERAUTOCOMPLETIONINPUT RC**
</dt> <dd>

Supporta il completamento automatico del carattere. I riconoscitori che supportano il completamento automatico del carattere richiedono input boxed.

</dd> <dt>

<span id="RC_RightAndDown"></span><span id="rc_rightanddown"></span><span id="RC_RIGHTANDDOWN"></span>**\_RIGHTANDDOWN RC**
</dt> <dd>

Supporta l'input della grafia nell'ordine a destra e in basso, ad esempio nelle lingue occidentali e in alcune lingue asiatiche orientali.

</dd> <dt>

<span id="RC_LeftAndDown"></span><span id="rc_leftanddown"></span><span id="RC_LEFTANDDOWN"></span>**\_LEFTANDDOWN RC**
</dt> <dd>

Supporta l'input della grafia nell'ordine di sinistra e in basso, ad esempio in lingua ebraica e araba.

</dd> <dt>

<span id="RC_DownAndLeft"></span><span id="rc_downandleft"></span><span id="RC_DOWNANDLEFT"></span>**\_DOWNANDLEFT RC**
</dt> <dd>

Supporta l'input della grafia nell'ordine inverso e a sinistra, ad esempio in alcune lingue asiatiche orientali.

</dd> <dt>

<span id="RC_DownAndRight"></span><span id="rc_downandright"></span><span id="RC_DOWNANDRIGHT"></span>**\_DOWNANDRIGHT RC**
</dt> <dd>

Supporta l'input della grafia in ordine inverso e corretto, ad esempio in alcune lingue asiatiche orientali.

</dd> <dt>

<span id="RC_ArbitraryAngle"></span><span id="rc_arbitraryangle"></span><span id="RC_ARBITRARYANGLE"></span>**\_ARBITRARYANGLE RC**
</dt> <dd>

Supporta testo scritto a angoli arbitrari.

</dd> <dt>

<span id="RC_Lattice"></span><span id="rc_lattice"></span><span id="RC_LATTICE"></span>**\_Reticolo RC**
</dt> <dd>

Supporta la restituzione di un reticolo come alternativa a una stringa per i risultati del riconoscimento della grafia.

</dd> <dt>

<span id="RC_AdviseInkChange"></span><span id="rc_adviseinkchange"></span><span id="RC_ADVISEINKCHANGE"></span>**\_ADVISEINKCHANGE RC**
</dt> <dd>

Supporta l'interruzione del riconoscimento in background, ad esempio quando l'input penna è stato modificato.

</dd> <dt>

<span id="RC_StrokeReorder"></span><span id="rc_strokereorder"></span><span id="RC_STROKEREORDER"></span>**\_STROKEREORDER RC**
</dt> <dd>

Supporta l'ordine dei tratti, spaziale e temporale, viene gestito come parte dell'operazione di riconoscimento. Il [**IInkAnalyzer**](iinkanalyzer.md) non riordina i tratti prima di inviare input penna al [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="RC_Personalizable"></span><span id="rc_personalizable"></span><span id="RC_PERSONALIZABLE"></span>**\_Personalizzabile RC**
</dt> <dd>

Supporta la grafia personalizzata, in cui il riconoscimento migliora il riconoscimento quando viene esposto alla stessa grafia nel tempo.

</dd> <dt>

<span id="RC_PrefersArbitraryAngle"></span><span id="rc_prefersarbitraryangle"></span><span id="RC_PREFERSARBITRARYANGLE"></span>**\_PREFERSARBITRARYANGLE RC**
</dt> <dd>

Il [**IInkAnalyzer**](iinkanalyzer.md) non deve ruotare la grafia a un orientamento orizzontale prima di inviare l'input penna al [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="RC_PrefersParagraphBreaking"></span><span id="rc_prefersparagraphbreaking"></span><span id="RC_PREFERSPARAGRAPHBREAKING"></span>**\_PREFERSPARAGRAPHBREAKING RC**
</dt> <dd>

Il [**IInkAnalyzer**](iinkanalyzer.md) deve inviare interi paragrafi di input penna al [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md), consentendo al **IInkAnalysisRecognizer** di eseguire le interruzioni di riga e di parola (o carattere).

</dd> <dt>

<span id="RC_PrefersSegmentationRecognition"></span><span id="rc_preferssegmentationrecognition"></span><span id="RC_PREFERSSEGMENTATIONRECOGNITION"></span>**\_PREFERSSEGMENTATIONRECOGNITION RC**
</dt> <dd>

Riconosce solo una parola o un carattere per ogni operazione di riconoscimento. [**IInkAnalyzer**](iinkanalyzer.md) esegue la segmentazione sulla grafia e invia un solo segmento alla volta al [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione consente una combinazione bit per bit dei relativi valori dei membri. Usare questa enumerazione per trovare un riconoscimento input penna installato che supporta gli attributi necessari.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalysisRecognizer:: GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





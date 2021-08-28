---
description: Indica il livello di attendibilità di IInkAnalyzer nell'accuratezza del risultato del riconoscimento.
ms.assetid: fd4fc350-b4db-4f9a-a5ae-00065e33606c
title: Enumerazione RecognitionConfidence (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognitionConfidence
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b5943b303c01a681b1df9d6d919df1822a5f2345c85fb5c52e3ab865ee58dd0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596631"
---
# <a name="recognitionconfidence-enumeration"></a>Enumerazione RecognitionConfidence

Indica il livello di attendibilità di [**IInkAnalyzer**](iinkanalyzer.md) nell'accuratezza del risultato del riconoscimento.

## <a name="syntax"></a>Sintassi


```C++
typedef enum RecognitionConfidence { 
  RecognitionConfidence_Strong        = 0,
  RecognitionConfidence_Intermediate  = 1,
  RecognitionConfidence_Poor          = 2,
  RecognitionConfidence_Unknown       = 3
} RecognitionConfidence;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence \_ Strong**
</dt> <dd>

Attendibilità totale nel risultato o alternativa.

</dd> <dt>

<span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence \_ Intermediate**
</dt> <dd>

Attendibilità intermedia nel risultato o alternativa.

</dd> <dt>

<span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence \_ Poor**
</dt> <dd>

Scarsa attendibilità nel risultato o alternativa.

</dd> <dt>

<span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence \_ Unknown**
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) che ha generato il testo riconosciuto non supporta i livelli di attendibilità.

</dd> </dl>

## <a name="remarks"></a>Commenti

[**IInkAnalyzer**](iinkanalyzer.md) usa uno o più [**oggetti IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) per convertire la grafia in testo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo IAnalysisAlternate::GetRecognitionConfidence**](ianalysisalternate-getrecognitionconfidence.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[Proprietà del nodo di contesto](context-node-properties.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





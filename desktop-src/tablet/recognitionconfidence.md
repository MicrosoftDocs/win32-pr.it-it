---
description: Indica il livello di confidenza del IInkAnalyzer nell'accuratezza del risultato del riconoscimento.
ms.assetid: fd4fc350-b4db-4f9a-a5ae-00065e33606c
title: Enumerazione RecognitionConfidence (IACom. h)
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
ms.openlocfilehash: e0358aacf789c391d99c10fc0fea64670dc4710e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318687"
---
# <a name="recognitionconfidence-enumeration"></a>Enumerazione RecognitionConfidence

Indica il livello di confidenza del [**IInkAnalyzer**](iinkanalyzer.md) nell'accuratezza del risultato del riconoscimento.

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

<span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence \_ forte**
</dt> <dd>

Confidenza assoluta nel risultato o in alternativa.

</dd> <dt>

<span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence \_ intermedio**
</dt> <dd>

Confidenza intermedia nel risultato o in alternativa.

</dd> <dt>

<span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence \_ poor**
</dt> <dd>

Scarsa confidenza nel risultato o in alternativa.

</dd> <dt>

<span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence \_ sconosciuto**
</dt> <dd>

Il [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) che ha generato il testo riconosciuto non supporta i livelli di confidenza.

</dd> </dl>

## <a name="remarks"></a>Commenti

[**IInkAnalyzer**](iinkanalyzer.md) utilizza uno o più oggetti [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) per convertire la grafia in testo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo IAnalysisAlternate:: GetRecognitionConfidence**](ianalysisalternate-getrecognitionconfidence.md)
</dt> <dt>

[**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[Proprietà del nodo di contesto](context-node-properties.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





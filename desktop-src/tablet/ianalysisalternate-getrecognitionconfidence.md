---
description: Ottiene un valore che indica il livello di attendibilità di IInkAnalyzer nell'accuratezza di IAnalysisAlternate.
ms.assetid: ac1c68df-2e0c-4633-b7ee-519482a4d67a
title: 'Metodo IAnalysisAlternate:: GetRecognitionConfidence (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognitionConfidence
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eacaf7e5a8feaddcd437e68cf7acfa4fc5a7fc80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751882"
---
# <a name="ianalysisalternategetrecognitionconfidence-method"></a>Metodo IAnalysisAlternate:: GetRecognitionConfidence

Ottiene un valore che indica il livello di attendibilità di [**IInkAnalyzer**](iinkanalyzer.md) nell'accuratezza di [**IAnalysisAlternate**](ianalysisalternate.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRecognitionConfidence(
  [out] RecognitionConfidence *pConfidence
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pConfidence* \[ out\]
</dt> <dd>

Puntatore a un' [**Enumerazione InkRecognitionConfidence**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) che indica il livello di confidenza del [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) nell'accuratezza dell'alternativa del riconoscimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**RecognitionConfidence**](recognitionconfidence.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





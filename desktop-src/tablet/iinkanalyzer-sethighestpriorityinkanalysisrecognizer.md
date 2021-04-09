---
description: Sposta il IInkAnalysisRecognizer specificato nella prima posizione dell'elenco di riconoscitori di input penna dell'oggetto IInkAnalyzer.
ms.assetid: 9126187f-02dd-4988-91b8-c4f3d3b6f773
title: 'Metodo IInkAnalyzer:: SetHighestPriorityInkAnalysisRecognizer (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetHighestPriorityInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 534b94e4f2964aa81f04e0adac6f45f346c530c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879326"
---
# <a name="iinkanalyzersethighestpriorityinkanalysisrecognizer-method"></a>Metodo IInkAnalyzer:: SetHighestPriorityInkAnalysisRecognizer

Sposta il [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) specificato nella prima posizione dell'elenco di riconoscitori di input penna dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetHighestPriorityInkAnalysisRecognizer(
  [in] IInkAnalysisRecognizer *pInkAnalysisRecognizer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInkAnalysisRecognizer* \[ in\]
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) da inserire nella prima posizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Per ottenere l'elenco dei riconoscitori di input penna in ordine di priorità, chiamare il [**Metodo IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).

Questo metodo non influisce sull'ordine degli altri oggetti [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) nell'elenco di riconoscitori di input penna dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) .

L'ordine dei riconoscitori Ink restituiti dal [**Metodo IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) indica l'ordine in cui [**IInkAnalyzer**](iinkanalyzer.md) valuta gli oggetti [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) disponibili.

L'utilizzo dei riconoscitori Ink viene valutato in base al relativo ordine nell'elenco.

Durante l'analisi dell'input penna, [**IInkAnalyzer**](iinkanalyzer.md) scorre i riconoscitori dell'input penna nell'elenco finché non trova un riconoscimento che supporta la lingua e altre proprietà dei tratti. Questo riconoscimento viene utilizzato per il riconoscimento dell'input penna per tali tratti.

Se [**IInkAnalyzer**](iinkanalyzer.md) non trova un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) che supporta un set di tratti durante l'analisi, **IInkAnalyzer** genera un [**IAnalysisWarning**](ianalysiswarning.md) con un codice di avviso di **AnalysisWarningCode \_ InkAnalysisRecognizerNotInstalled** (vedere [**IAnalysisWarning:: GetWarningCode**](ianalysiswarning-getwarningcode.md)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





---
description: Sposta l'oggetto IInkAnalysisRecognizer specificato nella prima posizione nell'elenco di riconoscitori input penna dell'oggetto IInkAnalyzer.
ms.assetid: 9126187f-02dd-4988-91b8-c4f3d3b6f773
title: Metodo IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer (IACom.h)
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
ms.openlocfilehash: 8404a2e1e89980ce5e8cadac1a468b3383d37d4952349f3702539975a304ac92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935211"
---
# <a name="iinkanalyzersethighestpriorityinkanalysisrecognizer-method"></a>Metodo IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer

Sposta [**l'oggetto IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) specificato nella prima posizione nell'elenco di riconoscitori input penna dell'oggetto [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetHighestPriorityInkAnalysisRecognizer(
  [in] IInkAnalysisRecognizer *pInkAnalysisRecognizer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInkAnalysisRecognizer* \[ Pollici\]
</dt> <dd>

Oggetto [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) da posizionare nella prima posizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Per ottenere l'elenco dei riconoscitori input penna in ordine di priorità, chiamare il metodo [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).

Questo metodo non influisce sull'ordine degli altri oggetti [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) nell'elenco dei riconoscitori input penna dell'oggetto [**IInkAnalyzer.**](iinkanalyzer.md)

L'ordine dei riconoscitori input penna restituiti dal metodo [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) indica l'ordine in cui [**IInkAnalyzer**](iinkanalyzer.md) valuta gli oggetti [**IInkAnalysisRecognizer disponibili.**](iinkanalysisrecognizer.md)

L'uso dei riconoscitori input penna viene valutato in base al relativo ordine nell'elenco.

Durante l'analisi dell'input penna, [**IInkAnalyzer**](iinkanalyzer.md) scorre i riconoscitori input penna nel relativo elenco finché non trova un sistema di riconoscimento che supporta la lingua e altre proprietà dei tratti. Questo sistema di riconoscimento viene usato per il riconoscimento input penna per tali tratti.

Se [**IInkAnalyzer**](iinkanalyzer.md) non trova un [**oggetto IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) che supporta un set di tratti durante l'analisi, **IInkAnalyzer** genera un [**oggetto IAnalysisWarning**](ianalysiswarning.md) con un codice di avviso **AnalysisWarningCode \_ InkAnalysisRecognizerNotInstalled** (vedere [**IAnalysisWarning::GetWarningCode).**](ianalysiswarning-getwarningcode.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





---
description: Recupera una raccolta ordinata di oggetti IInkAnalysisRecognizer.
ms.assetid: 67399237-38e2-4905-a97c-10ca72c7799b
title: Metodo IInkAnalyzer::GetInkAnalysisRecognizersByPriority (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetInkAnalysisRecognizersByPriority
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc663385006eedaca163f529af1f9f8a2da2eb5d3d41db823ffb53ee91775b93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713411"
---
# <a name="iinkanalyzergetinkanalysisrecognizersbypriority-method"></a>Metodo IInkAnalyzer::GetInkAnalysisRecognizersByPriority

Recupera una raccolta ordinata di [**oggetti IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetInkAnalysisRecognizersByPriority(
  [out] IInkAnalysisRecognizers **ppInkAnalysisRecognizers
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppInkAnalysisRecognizers* \[ Cambio\]
</dt> <dd>

Raccolta ordinata di [**oggetti IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppInkAnalysisRecognizers* quando non è più necessario usare l'oggetto .

 

L'ordine dei riconoscitori in questa raccolta indica l'ordine in cui [**IInkAnalyzer**](iinkanalyzer.md) valuta i riconoscitori disponibili. **IInkAnalyzer** usa il linguaggio dei tratti come criterio principale per l'applicazione di [**un oggetto IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md) Come criterio secondario, **IInkAnalyzer** confronta le informazioni dei suggerimenti di analisi con le funzionalità supportate di un oggetto **IInkAnalysisRecognizer** (vedere [**IInkAnalysisRecognizer::GetCapabilities).**](iinkanalysisrecognizer-getcapabilities.md) Per altre informazioni sugli hint di analisi, vedere [**Metodo IInkAnalyzer::CreateAnalysisHint**](iinkanalyzer-createanalysishint.md).

Se più di un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supporta un identificatore di lingua, [**IInkAnalyzer**](iinkanalyzer.md) usa un algoritmo "first-fit" per selezionare il primo **IInkAnalysisRecognizer** per analizzare i tratti di tale lingua.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**Metodo IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


---
description: Recupera il codice di errore per l'operazione di analisi dell'input penna in background se si è verificato un errore.
ms.assetid: 0255751e-9b2a-46f1-aa45-6509f9d1c658
title: 'Metodo IAnalysisWarning:: GetBackgroundError (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetBackgroundError
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4367b1d52ee5d2a3bb65af0e4edd4922b8ae9a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226171"
---
# <a name="ianalysiswarninggetbackgrounderror-method"></a>Metodo IAnalysisWarning:: GetBackgroundError

Recupera il codice di errore per l'operazione di analisi dell'input penna in background se si è verificato un errore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBackgroundError();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Se si verifica un errore all'interno di un'operazione di analisi in background, [**IInkAnalyzer**](iinkanalyzer.md) non può restituire il codice di errore perché si sta verificando in un thread diverso. Al contrario, il gestore dell'evento [**\_ IAnalysisEvents:: results**](-ianalysisevents-results.md) riceve un [**IAnalysisStatus**](ianalysisstatus.md) contenente un [**IAnalysisWarning**](ianalysiswarning.md) con [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) di **AnalysisWarningCode \_ BackgroundException**. Questo **IAnalysisWarning** contiene il codice di errore per l'operazione di analisi in background. In generale, il gestore dell'evento **\_ IAnalysisEvents:: results** restituirà questo codice di errore in modo che possa essere gestito altrove nell'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_IAnalysisEvents:: results**](-ianalysisevents-results.md)
</dt> <dt>

[**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


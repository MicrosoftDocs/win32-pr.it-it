---
description: Recupera il codice di errore per l'operazione di analisi dell'input penna in background se si è verificato un errore.
ms.assetid: 0255751e-9b2a-46f1-aa45-6509f9d1c658
title: Metodo IAnalysisWarning::GetBackgroundError (IACom.h)
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
ms.openlocfilehash: aa8c9c3c60f51ffd854ccdfebb6538337e7676a8c63e45899737333c41d99aad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057961"
---
# <a name="ianalysiswarninggetbackgrounderror-method"></a>Metodo IAnalysisWarning::GetBackgroundError

Recupera il codice di errore per l'operazione di analisi dell'input penna in background se si è verificato un errore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBackgroundError();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Se si verifica un errore all'interno di un'operazione di analisi in background, [**IInkAnalyzer**](iinkanalyzer.md) non può restituire il codice di errore perché si verifica in un thread diverso. Il gestore dell'evento [**\_ IAnalysisEvents::Results**](-ianalysisevents-results.md) riceve invece un [**oggetto IAnalysisStatus**](ianalysisstatus.md) che contiene [**un oggetto IAnalysisWarning**](ianalysiswarning.md) con [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) di **AnalysisWarningCode \_ BackgroundException.** Questo **IAnalysisWarning contiene il codice di** errore per l'operazione di analisi in background. In generale, il gestore eventi **\_ IAnalysisEvents::Results** restituirà questo codice di errore in modo che possa essere gestito altrove nell'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**Metodo IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_IAnalysisEvents::Results**](-ianalysisevents-results.md)
</dt> <dt>

[**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 


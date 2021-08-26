---
description: Recupera l'hint di analisi che ha causato l'avviso.
ms.assetid: 715aa4b2-6c45-414b-96f2-44c73a073213
title: Metodo IAnalysisWarning::GetHint (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 51eb76839b157c2ac9611ef9be978ea967c8e9b3506513a23b0ca70906dd32b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940511"
---
# <a name="ianalysiswarninggethint-method"></a>Metodo IAnalysisWarning::GetHint

Recupera l'hint di analisi che ha causato l'avviso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetHint(
  [out] IContextNode **pAnalysisHint
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAnalysisHint* \[ Cambio\]
</dt> <dd>

Nodo di contesto dell'hint di analisi che ha causato l'avviso oppure **NULL se** un hint di analisi non ha generato questo avviso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *pAnalysisHint* quando non è più necessario usare il nodo di contesto dell'hint di analisi.

 

Un esempio di hint di analisi che genera [**un IAnalysisWarning**](ianalysiswarning.md) è un hint di analisi che contiene un factoid digitato in modo non corretto. In questo caso, l'analisi input penna restituisce un [**oggetto IAnalysisStatus**](ianalysisstatus.md) che contiene **un elemento IAnalysisWarning** che fa riferimento al nodo di contesto dell'hint di analisi con il factoid con errori di ortografia. In questo caso, il metodo [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md) dell'avviso di analisi restituisce un valore [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) di **AnalysisWarningCode \_ FactoidNotSupported.**

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

[**Metodo IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Metodo IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 


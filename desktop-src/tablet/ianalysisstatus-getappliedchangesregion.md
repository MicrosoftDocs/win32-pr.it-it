---
description: Recupera l'area del documento che corrisponde alle modifiche apportate nell'albero del nodo di contesto dell'oggetto IInkAnalyzer come risultato dell'analisi dell'input penna.
ms.assetid: 25d511fb-ba2d-4c46-8a8c-8bb4187c9a5c
title: Metodo IAnalysisStatus::GetAppliedChangesRegion (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.GetAppliedChangesRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d3b2fec2528cbf961956e8b41f9eb6c985bd745d5dad097eb05544e64c42d122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044994"
---
# <a name="ianalysisstatusgetappliedchangesregion-method"></a>Metodo IAnalysisStatus::GetAppliedChangesRegion

Recupera l'area del documento che corrisponde alle modifiche apportate nell'albero dei nodi di contesto dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) come risultato dell'analisi dell'input penna.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAppliedChangesRegion(
  [out] IAnalysisRegion **pAppliedChangesRegion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAppliedChangesRegion* \[ Cambio\]
</dt> <dd>

Puntatore [**all'area IAnalysis del**](ianalysisregion.md) documento in cui sono state apportate modifiche.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* *in pAppliedChangesRegion* quando non è più necessario usare l'area di analisi.

 

Questo metodo viene usato più di frequente quando l'applicazione riceve informazioni a scopo di debug e deve invalidare l'area in cui possono verificarsi modifiche in modo che le informazioni di debug vengono disegnate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**Area IAnalysis**](ianalysisregion.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


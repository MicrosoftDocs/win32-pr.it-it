---
description: Recupera l'area del documento che corrisponde alle modifiche apportate nell'albero del nodo di contesto dell'oggetto IInkAnalyzer come risultato dell'analisi dell'input penna.
ms.assetid: 25d511fb-ba2d-4c46-8a8c-8bb4187c9a5c
title: 'Metodo IAnalysisStatus:: GetAppliedChangesRegion (IACom. h)'
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
ms.openlocfilehash: 08f6690091207b648c39cded161de64585e44b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526545"
---
# <a name="ianalysisstatusgetappliedchangesregion-method"></a>Metodo IAnalysisStatus:: GetAppliedChangesRegion

Recupera l'area del documento che corrisponde alle modifiche apportate nell'albero del nodo di contesto dell'oggetto [**IInkAnalyzer**](iinkanalyzer.md) come risultato dell'analisi dell'input penna.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAppliedChangesRegion(
  [out] IAnalysisRegion **pAppliedChangesRegion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pAppliedChangesRegion* \[ out\]
</dt> <dd>

Puntatore al [**IAnalysisRegion**](ianalysisregion.md) del documento in cui sono state apportate modifiche.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su \* *pAppliedChangesRegion* quando non è più necessario usare l'area di analisi.

 

Questo metodo viene usato più di frequente quando l'applicazione riceve informazioni a scopo di debug e deve invalidare l'area in cui potrebbero verificarsi le modifiche in modo da disegnare le informazioni di debug.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 


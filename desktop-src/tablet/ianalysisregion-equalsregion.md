---
description: Determina se l'oggetto IAnalysisRegion specificato contiene lo stesso valore dell'oggetto IAnalysisRegion corrente.
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: Metodo IAnalysisRegion::EqualsRegion (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.EqualsRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: aecf7bd065c2da0c507c2424c0305526510c9d4f64844dfa229183cf43d5554a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596801"
---
# <a name="ianalysisregionequalsregion-method"></a>Metodo IAnalysisRegion::EqualsRegion

Determina se [**l'oggetto IAnalysisRegion specificato**](ianalysisregion.md) contiene lo stesso valore dell'oggetto **IAnalysisRegion** corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EqualsRegion(
  [in]  IAnalysisRegion *pOtherRegion,
  [out] VARIANT_BOOL    *pfRegionsEqual
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOtherRegion* \[ Pollici\]
</dt> <dd>

Oggetto [**IAnalysisRegion**](ianalysisregion.md) da confrontare con l'oggetto **IAnalysisRegion corrente.**

</dd> <dt>

*pfRegionsEqual* \[ Cambio\]
</dt> <dd>

**VARIANT \_ TRUE** se [**l'oggetto IAnalysisRegion specificato**](ianalysisregion.md) contiene lo stesso valore dell'oggetto IAnalysisRegion corrente; in caso contrario, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Area IAnalysis**](ianalysisregion.md)
</dt> </dl>

 

 





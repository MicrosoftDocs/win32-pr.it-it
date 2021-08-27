---
description: Espande l'area di questa area IAnalysisRegion nell'area creata dalla relativa unione con l'area IAnalysisRegion specificata.
ms.assetid: cc3ec5c6-98ff-442e-a1e8-d1a57752ad56
title: Metodo IAnalysisRegion::UnionRegion (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 760296552dc13ac394d4554903d84f596faba14318db9af3145c79f156c736fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720008"
---
# <a name="ianalysisregionunionregion-method"></a>Metodo IAnalysisRegion::UnionRegion

Espande l'area di [**questa area IAnalysisRegion nell'area**](ianalysisregion.md) creata dalla relativa unione con l'elemento **IAnalysisRegion specificato.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnionRegion(
  [in] IAnalysisRegion *pRegionToUnion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRegionToUnion* \[ Pollici\]
</dt> <dd>

[**IAnalysisRegion con**](ianalysisregion.md) cui combinare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Se una delle due aree è infinita, anche la nuova area è infinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Area IAnalysis**](ianalysisregion.md)
</dt> <dt>

[**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
</dt> <dt>

[**Metodo IAnalysisRegion::ExcludeRegion**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**Metodo IAnalysisRegion::IntersectRectangle**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**Metodo IAnalysisRegion::IntersectRegion**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**Metodo IAnalysisRegion::UnionRectangle**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





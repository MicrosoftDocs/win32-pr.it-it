---
description: Limita l'area di IAnalysisRegion all'area creata dall'intersezione con l'area IAnalysisRegion specificata.
ms.assetid: 02b3049f-ada9-4de3-a7a2-f9ff8313fbab
title: Metodo IAnalysisRegion::IntersectRegion (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 0db58dcc7fc1c1e7458cf804eb82af236de8f1997ddcc658391da19641d1cfdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058081"
---
# <a name="ianalysisregionintersectregion-method"></a>Metodo IAnalysisRegion::IntersectRegion

Limita l'area di [**IAnalysisRegion all'area**](ianalysisregion.md) creata dall'intersezione con l'elemento **IAnalysisRegion specificato.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT IntersectRegion(
  [in] IAnalysisRegion *pRegionToIntersect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRegionToIntersect* \[ Pollici\]
</dt> <dd>

[**IAnalysisRegion con**](ianalysisregion.md) cui intersecare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Se le due aree non si intersecano, la nuova area è vuota.

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

[**Metodo IAnalysisRegion::UnionRectangle**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**Metodo IAnalysisRegion::UnionRegion**](ianalysisregion-unionregion.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





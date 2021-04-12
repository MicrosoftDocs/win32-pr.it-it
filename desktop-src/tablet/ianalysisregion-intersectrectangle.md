---
description: Limita l'area di questo IAnalysisRegion all'area creata dalla relativa intersezione con il rettangolo specificato.
ms.assetid: de6b565f-34c1-4551-ab92-db6bacb8608d
title: 'Metodo IAnalysisRegion:: IntersectRectangle (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4ce0e514b24aba0331d9ea604333680db1c67c8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526556"
---
# <a name="ianalysisregionintersectrectangle-method"></a>Metodo IAnalysisRegion:: IntersectRectangle

Limita l'area di questo [**IAnalysisRegion**](ianalysisregion.md) all'area creata dalla relativa intersezione con il rettangolo specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IntersectRectangle(
  [in] RECT *pIntersectingRectangle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pIntersectingRectangle* \[ in\]
</dt> <dd>

Puntatore al rettangolo con cui intersecare le coordinate dello spazio input penna.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Le coordinate del rettangolo sono espresse in unità HIMETRIC.

Se le due aree non si intersecano, la nuova area è vuota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
</dt> <dt>

[**Metodo IAnalysisRegion:: ExcludeRegion**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**Metodo IAnalysisRegion:: IntersectRegion**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**Metodo IAnalysisRegion:: UnionRectangle**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**Metodo IAnalysisRegion:: UnionRegion**](ianalysisregion-unionregion.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





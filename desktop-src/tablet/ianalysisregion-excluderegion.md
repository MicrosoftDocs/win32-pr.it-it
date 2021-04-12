---
description: Limita l'area di IAnalysisRegion alla parte dell'area che non interseca il IAnalysisRegion specificato.
ms.assetid: 7a11d2a8-c2ca-4088-b932-8a6c3e789b7f
title: 'Metodo IAnalysisRegion:: ExcludeRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13324d872a76a9184e6ea67b227dbd7444684bb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526557"
---
# <a name="ianalysisregionexcluderegion-method"></a>Metodo IAnalysisRegion:: ExcludeRegion

Limita l'area di [**IAnalysisRegion**](ianalysisregion.md) alla parte dell'area che non interseca il **IAnalysisRegion** specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ExcludeRegion(
  [in] IAnalysisRegion *pRegionToExclude
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRegionToExclude* \[ in\]
</dt> <dd>

[**IAnalysisRegion**](ianalysisregion.md) da escludere da questo **IAnalysisRegion**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Se le due aree non si intersecano, questo [**IAnalysisRegion**](ianalysisregion.md) è invariato.

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

[**Metodo IAnalysisRegion:: IntersectRectangle**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**Metodo IAnalysisRegion:: IntersectRegion**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**Metodo IAnalysisRegion:: UnionRectangle**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**Metodo IAnalysisRegion:: UnionRegion**](ianalysisregion-unionregion.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





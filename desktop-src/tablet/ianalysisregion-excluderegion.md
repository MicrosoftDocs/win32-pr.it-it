---
description: Limita l'area di IAnalysisRegion alla parte della relativa area che non interseca l'area IAnalysisRegion specificata.
ms.assetid: 7a11d2a8-c2ca-4088-b932-8a6c3e789b7f
title: Metodo IAnalysisRegion::ExcludeRegion (IACom.h)
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
ms.openlocfilehash: 4a26bc234a5a99d2ba692b02097d348b83878c47ea3c9a1cbd21e1558fc41950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092352"
---
# <a name="ianalysisregionexcluderegion-method"></a>Metodo IAnalysisRegion::ExcludeRegion

Limita l'area di [**IAnalysisRegion**](ianalysisregion.md) alla parte della relativa area che non interseca l'oggetto **IAnalysisRegion specificato.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT ExcludeRegion(
  [in] IAnalysisRegion *pRegionToExclude
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRegionToExclude* \[ Pollici\]
</dt> <dd>

[**IAnalysisRegion**](ianalysisregion.md) da escludere da **questa area IAnalysisRegion.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Se le due aree non si intersecano, [**L'area IAnalysis rimane**](ianalysisregion.md) invariata.

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
</dt> <dt>

[**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
</dt> <dt>

[**Metodo IAnalysisRegion::IntersectRectangle**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**Metodo IAnalysisRegion::IntersectRegion**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**Metodo IAnalysisRegion::UnionRectangle**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**Metodo IAnalysisRegion::UnionRegion**](ianalysisregion-unionregion.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





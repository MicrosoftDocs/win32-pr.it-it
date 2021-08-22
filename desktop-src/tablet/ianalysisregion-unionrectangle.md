---
description: Espande l'area di questa area IAnalysisRegion nell'area creata dalla relativa unione con il rettangolo specificato.
ms.assetid: 9b12f509-4f6a-43b0-9639-bef060fd6d50
title: Metodo IAnalysisRegion::UnionRectangle (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da3eefb3a527646ba416d62783421d6dfe9be5706c0527df7eb321d3945b6f92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596752"
---
# <a name="ianalysisregionunionrectangle-method"></a>Metodo IAnalysisRegion::UnionRectangle

Espande l'area di [**questa area IAnalysisRegion**](ianalysisregion.md) nell'area creata dalla relativa unione con il rettangolo specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnionRectangle(
  [in] RECT *pRectangle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRectangle* \[ Pollici\]
</dt> <dd>

Puntatore al rettangolo con cui combinare, in coordinate dello spazio input penna.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

Le coordinate del rettangolo sono in unità HIMETRIC.

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

[**Metodo IAnalysisRegion::UnionRegion**](ianalysisregion-unionregion.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





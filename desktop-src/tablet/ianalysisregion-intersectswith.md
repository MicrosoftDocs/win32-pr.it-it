---
description: Determina se l'area di IAnalysisRegion interseca il rettangolo specificato.
ms.assetid: 683c3ad8-0236-474e-a16d-6164c2244cfb
title: Metodo IAnalysisRegion::IntersectsWith (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectsWith
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 04613e061929bba04c14be37914b22a51de0377f125b21fa29db9c56fc8dfeff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720018"
---
# <a name="ianalysisregionintersectswith-method"></a>Metodo IAnalysisRegion::IntersectsWith

Determina se l'area di [**IAnalysisRegion**](ianalysisregion.md) interseca il rettangolo specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IntersectsWith(
  [in]  RECT         *pRectangle,
  [out] VARIANT_BOOL *pfIsIntersecting
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRectangle* \[ Pollici\]
</dt> <dd>

Puntatore al rettangolo con cui eseguire il confronto, in coordinate dello spazio input penna.

</dd> <dt>

*pfIsIntersecting* \[ Cambio\]
</dt> <dd>

**VARIANT \_ TRUE** se l'area [**di IAnalysisRegion**](ianalysisregion.md) interseca il rettangolo specificato. in caso contrario, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Il confronto è in coordinate dello spazio input penna.

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

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





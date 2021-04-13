---
description: Determina se l'area del IAnalysisRegion interseca il rettangolo specificato.
ms.assetid: 683c3ad8-0236-474e-a16d-6164c2244cfb
title: 'Metodo IAnalysisRegion:: IntersectsWith (IACom. h)'
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
ms.openlocfilehash: 99ff1ce8d3039b04d83f9cdd5c1d6aebe00be407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526551"
---
# <a name="ianalysisregionintersectswith-method"></a>Metodo IAnalysisRegion:: IntersectsWith

Determina se l'area del [**IAnalysisRegion**](ianalysisregion.md) interseca il rettangolo specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IntersectsWith(
  [in]  RECT         *pRectangle,
  [out] VARIANT_BOOL *pfIsIntersecting
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRectangle* \[ in\]
</dt> <dd>

Puntatore al rettangolo con il quale eseguire il confronto, in coordinate dello spazio input penna.

</dd> <dt>

*pfIsIntersecting* \[ out\]
</dt> <dd>

**Variante \_ TRUE** se l'area di [**IAnalysisRegion**](ianalysisregion.md) si interseca con il rettangolo specificato. in caso contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

Il confronto si trova nelle coordinate dello spazio input penna.

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

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





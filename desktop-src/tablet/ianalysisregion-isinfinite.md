---
description: Recupera un valore che indica se IAnalysisRegion rappresenta un'area infinita.
ms.assetid: b84ec9ec-42d0-4d03-b78b-433e55d04897
title: Metodo IAnalysisRegion::IsInfinite (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsInfinite
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 872c780a3ec1bc60834957eff6aa2fcdb574487eee4397b2d2ec89871684d20f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118045291"
---
# <a name="ianalysisregionisinfinite-method"></a>Metodo IAnalysisRegion::IsInfinite

Recupera un valore che indica se [**IAnalysisRegion**](ianalysisregion.md) rappresenta un'area infinita.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsInfinite(
  [out] VARIANT_BOOL *pfIsInfinite
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pfIsInfinite* \[ Cambio\]
</dt> <dd>

**VARIANT \_ TRUE** se l'area rappresentata è infinita; in caso contrario, **VARIANT \_ FALSE.**

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
</dt> <dt>

[**Metodo IAnalysisRegion::IsEmpty**](ianalysisregion-isempty.md)
</dt> <dt>

[**Metodo IAnalysisRegion::MakeEmpty**](ianalysisregion-makeempty.md)
</dt> <dt>

[**Metodo IAnalysisRegion::MakeInfinite**](ianalysisregion-makeinfinite.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





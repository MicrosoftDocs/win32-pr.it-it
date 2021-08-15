---
description: Recupera un valore che indica se IAnalysisRegion rappresenta un'area vuota.
ms.assetid: 3a536b01-e7ee-4103-88c4-d83377ea9fdb
title: Metodo IAnalysisRegion::IsEmpty (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsEmpty
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a599d88371a1a6726ed2ec4ee217c36b3ea3cd71d6117305a59860cb9a8bf09f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092322"
---
# <a name="ianalysisregionisempty-method"></a>Metodo IAnalysisRegion::IsEmpty

Recupera un valore che indica se [**IAnalysisRegion rappresenta**](ianalysisregion.md) un'area vuota.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsEmpty(
  [out] VARIANT_BOOL *pfIsEmpty
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pfIsEmpty* \[ Cambio\]
</dt> <dd>

**VARIANT \_ TRUE** se l'area rappresentata è vuota. in caso contrario, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

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

[**Metodo IAnalysisRegion::IsInfinite**](ianalysisregion-isinfinite.md)
</dt> <dt>

[**Metodo IAnalysisRegion::MakeEmpty**](ianalysisregion-makeempty.md)
</dt> <dt>

[**Metodo IAnalysisRegion::MakeInfinite**](ianalysisregion-makeinfinite.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





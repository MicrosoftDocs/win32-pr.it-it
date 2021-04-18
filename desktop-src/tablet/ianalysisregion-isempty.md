---
description: Recupera un valore che indica se IAnalysisRegion rappresenta un'area vuota.
ms.assetid: 3a536b01-e7ee-4103-88c4-d83377ea9fdb
title: 'Metodo IAnalysisRegion:: IsEmpty (IACom. h)'
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
ms.openlocfilehash: c1fb4ebbe487119c65f153f78e192de38e6393fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307462"
---
# <a name="ianalysisregionisempty-method"></a>Metodo IAnalysisRegion:: IsEmpty

Recupera un valore che indica se [**IAnalysisRegion**](ianalysisregion.md) rappresenta un'area vuota.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsEmpty(
  [out] VARIANT_BOOL *pfIsEmpty
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pfIsEmpty* \[ out\]
</dt> <dd>

**Variante \_ TRUE** se l'area rappresentata è vuota. in caso contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

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

[**Metodo IAnalysisRegion:: infinite**](ianalysisregion-isinfinite.md)
</dt> <dt>

[**Metodo IAnalysisRegion:: MakeEmpty**](ianalysisregion-makeempty.md)
</dt> <dt>

[**Metodo IAnalysisRegion:: MakeInfinite**](ianalysisregion-makeinfinite.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





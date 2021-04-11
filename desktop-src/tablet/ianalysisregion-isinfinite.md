---
description: Recupera un valore che indica se IAnalysisRegion rappresenta un'area infinita.
ms.assetid: b84ec9ec-42d0-4d03-b78b-433e55d04897
title: 'Metodo IAnalysisRegion:: infinite (IACom. h)'
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
ms.openlocfilehash: 4f7d284c043f38a681b969f72d751f9acaa954c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226175"
---
# <a name="ianalysisregionisinfinite-method"></a>Metodo IAnalysisRegion:: infinite

Recupera un valore che indica se [**IAnalysisRegion**](ianalysisregion.md) rappresenta un'area infinita.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsInfinite(
  [out] VARIANT_BOOL *pfIsInfinite
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pfIsInfinite* \[ out\]
</dt> <dd>

**Variante \_ TRUE** se l'area rappresentata è infinita; in caso contrario, **Variant \_ false**.

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

[**Metodo IAnalysisRegion:: IsEmpty**](ianalysisregion-isempty.md)
</dt> <dt>

[**Metodo IAnalysisRegion:: MakeEmpty**](ianalysisregion-makeempty.md)
</dt> <dt>

[**Metodo IAnalysisRegion:: MakeInfinite**](ianalysisregion-makeinfinite.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 





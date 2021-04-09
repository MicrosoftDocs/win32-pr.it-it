---
description: Determina se il IAnalysisRegion specificato contiene lo stesso valore dell'oggetto IAnalysisRegion corrente.
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: 'Metodo IAnalysisRegion:: EqualsRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.EqualsRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6a647c13f1279cd39e4947b9fdbcc9ed4e1ef4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129523"
---
# <a name="ianalysisregionequalsregion-method"></a>Metodo IAnalysisRegion:: EqualsRegion

Determina se il [**IAnalysisRegion**](ianalysisregion.md) specificato contiene lo stesso valore dell'oggetto **IAnalysisRegion** corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EqualsRegion(
  [in]  IAnalysisRegion *pOtherRegion,
  [out] VARIANT_BOOL    *pfRegionsEqual
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pOtherRegion* \[ in\]
</dt> <dd>

Oggetto [**IAnalysisRegion**](ianalysisregion.md) da confrontare con il **IAnalysisRegion** corrente.

</dd> <dt>

*pfRegionsEqual* \[ out\]
</dt> <dd>

**Variante \_ TRUE** se l'oggetto [**IAnalysisRegion**](ianalysisregion.md) specificato contiene lo stesso valore dell'oggetto IAnalysisRegion corrente. in caso contrario, **Variant \_ false**.

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
</dt> </dl>

 

 





---
title: Funzione FreeRepairInfos (Ndattributils.h)
description: Dealloca la memoria allocata internamente a una matrice di strutture RepairInfo.
ms.assetid: c40f9d10-8d9e-4c79-ac0b-fa88608888f1
keywords:
- Funzione FreeRepairInfos NDF
topic_type:
- apiref
api_name:
- FreeRepairInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 745f6cd9a7fd484db943fc91c5c9dadf440b3635f31cdb539b356358c22362a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798606"
---
# <a name="freerepairinfos-function"></a>Funzione FreeRepairInfos

La **funzione FreeRepairInfos** dealloca la memoria allocata internamente a una matrice [**di strutture RepairInfo.**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) Questa funzione chiama [**CoTaskMemFree per**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) deallocare la memoria.

## <a name="syntax"></a>Sintassi


```C++
VOID FreeRepairInfos(
  _In_ RepairInfo *pInfo,
       ULONG      RepairCount,
       BOOL       bFreePointer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInfo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\***

Matrice di strutture . La memoria allocata a cui puntano queste strutture verrà liberata.

</dd> <dt>

*RepairCount* 
</dt> <dd>

Tipo: **ULONG**

Numero di strutture nella matrice a cui punta *pInfo*.

</dd> <dt>

*bFreePointer* 
</dt> <dd>

Tipo: **BOOL**

True se anche la matrice di strutture deve essere eliminata; in caso contrario, false.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 


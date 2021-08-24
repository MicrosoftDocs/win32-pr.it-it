---
title: Funzione FreeRepairInfoExs (Ndattributils.h)
description: Dealloca la memoria allocata internamente a una matrice di strutture RepairInfoEx.
ms.assetid: b4e3e758-88cd-4ce2-b1a4-5b47889aae9b
keywords:
- Funzione FreeRepairInfoExs NDF
topic_type:
- apiref
api_name:
- FreeRepairInfoExs
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b75d3d3ee8ba710b0b0ed4755e5ee01309f955bcc1658145dc1d42fe3b9e1ed8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802421"
---
# <a name="freerepairinfoexs-function"></a>Funzione FreeRepairInfoExs

La **funzione FreeRepairInfoExs** dealloca la memoria allocata internamente a una matrice [**di strutture RepairInfoEx.**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) Questa funzione chiama [**CoTaskMemFree per**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) deallocare la memoria.

## <a name="syntax"></a>Sintassi


```C++
VOID FreeRepairInfoExs(
  _In_ RepairInfoEx *pInfo,
       ULONG        RepairCount,
       BOOL         bFreePointer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInfo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)\***

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

[**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 


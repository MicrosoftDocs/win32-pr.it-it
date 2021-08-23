---
title: Funzione FreeRootCauseInfos (Ndattributils.h)
description: Dealloca la memoria allocata internamente a una matrice di strutture RootCauseInfo.
ms.assetid: b45fa432-0db4-470b-80ce-ae25c33f88d6
keywords:
- Funzione FreeRootCauseInfos NDF
topic_type:
- apiref
api_name:
- FreeRootCauseInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9cbd0386af86ebe5e1fdc5e6350cebfb305f44544f8822e0f2bde4d46cb55f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065241"
---
# <a name="freerootcauseinfos-function"></a>Funzione FreeRootCauseInfos

La **funzione FreeRootCauseInfos** dealloca la memoria allocata internamente a una matrice di [**strutture RootCauseInfo.**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) Questa funzione chiama [**CoTaskMemFree per**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) deallocare la memoria.

## <a name="syntax"></a>Sintassi


```C++
VOID FreeRootCauseInfos(
  _In_ RootCauseInfo *pInfo,
       ULONG         RootCauseCount,
       BOOL          bFreePointer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInfo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\***

Matrice di strutture . La memoria allocata a cui puntano queste strutture verrà liberata.

</dd> <dt>

*RootCauseCount* 
</dt> <dd>

Tipo: **ULONG**

Numero di strutture nella matrice a cui punta *pInfo*.

</dd> <dt>

*bFreePointer* 
</dt> <dd>

Tipo: **BOOL**

True se deve essere eliminata anche la matrice di strutture. in caso contrario, false.

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

[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 


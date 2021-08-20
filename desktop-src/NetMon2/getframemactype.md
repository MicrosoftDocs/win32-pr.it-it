---
description: La funzione GetFrameMacType restituisce il tipo MAC del frame.
ms.assetid: 8d3da770-1392-4638-a267-32c2dae289b0
title: Funzione GetFrameMacType (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4202e05d6820718166b4eb2e66fc0c37e7e4e3461b235069278f2128278cc7ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117982369"
---
# <a name="getframemactype-function"></a>Funzione GetFrameMacType

La **funzione GetFrameMacType** restituisce il tipo MAC del frame.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI GetFrameMacType(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ Pollici\]
</dt> <dd>

Handle per il frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce il tipo MAC del frame, che può avere uno dei valori seguenti.

-   TIPO MAC \_ \_ SCONOSCIUTO
-   TIPO MAC \_ \_ ETHERNET
-   TOKENRING \_ DEL TIPO MAC \_
-   TIPO MAC \_ \_ FDDI

## <a name="remarks"></a>Commenti

[*Esperti*](e.md) e [*parser possono*](p.md) chiamare la **funzione GetFrameMacType.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





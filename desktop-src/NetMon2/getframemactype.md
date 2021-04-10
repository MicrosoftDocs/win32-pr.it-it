---
description: La funzione GetFrameMacType restituisce il tipo MAC del frame.
ms.assetid: 8d3da770-1392-4638-a267-32c2dae289b0
title: Funzione GetFrameMacType (Netmon. h)
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
ms.openlocfilehash: b85accc64a6e29424e3f65d070bafcf29bb3ec0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966469"
---
# <a name="getframemactype-function"></a>GetFrameMacType (funzione)

La funzione **GetFrameMacType** restituisce il tipo Mac del frame.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI GetFrameMacType(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ in\]
</dt> <dd>

Handle per il frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce il tipo MAC del frame, che può avere uno dei valori seguenti.

-   \_tipo Mac \_ sconosciuto
-   \_Ethernet di tipo Mac \_
-   \_Tokenring di tipo Mac \_
-   \_FDDI di tipo Mac \_

## <a name="remarks"></a>Commenti

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameMacType** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





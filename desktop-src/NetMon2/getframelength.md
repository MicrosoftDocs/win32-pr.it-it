---
description: La funzione GetFrameLength restituisce la lunghezza del frame.
ms.assetid: 30be1f5c-9b13-42ad-944a-92b1aee8a6bc
title: Funzione GetFrameLength (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2344f2401995af3bac2e8245f48824dfb992076113eb8c27dcb9eff0a54eae04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795703"
---
# <a name="getframelength-function"></a>Funzione GetFrameLength

La **funzione GetFrameLength** restituisce la lunghezza del frame.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI GetFrameLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ Pollici\]
</dt> <dd>

Handle per un frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è la lunghezza del frame in byte.

Se la funzione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

[*Esperti*](e.md) e [*parser possono*](p.md) chiamare la **funzione GetFrameLength.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





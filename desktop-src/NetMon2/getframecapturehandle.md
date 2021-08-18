---
description: La funzione GetFrameCaptureHandle restituisce un handle all'acquisizione in base a un frame specificato.
ms.assetid: 71b32799-194c-40f8-8438-36aebaba31c7
title: Funzione GetFrameCaptureHandle (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameCaptureHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 9e7bf14cd7eae73ac1e5c8e21f8036574628932032a1545f8ac1c653dbbf8adb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910751"
---
# <a name="getframecapturehandle-function"></a>Funzione GetFrameCaptureHandle

La **funzione GetFrameCaptureHandle** restituisce un handle all'acquisizione in base a un frame specificato.

## <a name="syntax"></a>Sintassi


```C++
HCAPTURE WINAPI GetFrameCaptureHandle(
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

Se la funzione ha esito positivo, il valore restituito è un handle per l'acquisizione.

Se la funzione ha esito negativo, il valore restituito è 0.

## <a name="remarks"></a>Commenti

[*Esperti*](e.md) e [*parser*](p.md) possono chiamare la **funzione GetFrameCaptureHandle.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





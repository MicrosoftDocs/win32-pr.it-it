---
description: La funzione GetFrameFromFrameHandle restituisce un puntatore a un frame da un handle di frame.
ms.assetid: 790fe5fe-a857-4947-a471-d0538c0f0d61
title: Funzione GetFrameFromFrameHandle (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameFromFrameHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 56ee96fd04d4860648dac2ec6b20a537ba420beb070c8f9b7248d9e3b4acd184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366545"
---
# <a name="getframefromframehandle-function"></a>Funzione GetFrameFromFrameHandle

La **funzione GetFrameFromFrameHandle** restituisce un puntatore a un frame da un handle di frame.

## <a name="syntax"></a>Sintassi


```C++
ULPFRAME WINAPI GetFrameFromFrameHandle(
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

Se la funzione ha esito positivo, il valore restituito è un puntatore al frame.

Se la funzione ha esito negativo, il valore restituito è 0.

## <a name="remarks"></a>Commenti

La **funzione GetFrameFromFrameHandle** recupera i dati che non possono essere recuperati dalle altre funzioni helper Network Monitor disponibili. Quando possibile, usare le funzioni seguenti.

<dl>

[**GetFrameDstAddressOffset**](getframedstaddressoffset.md)  
[**GetFrameSrcAddressOffset**](getframesrcaddressoffset.md)  
[**GetFrameCaptureHandle**](getframecapturehandle.md)  
[**GetFrameDestAddress**](getframedestaddress.md)  
[**GetFrameSourceAddress**](getframesourceaddress.md)  
[**GetFrameMacHeaderLength**](getframemacheaderlength.md)  
[**GetFrameLength**](getframelength.md)  
[**GetFrameStoredLength**](getframestoredlength.md)  
[**GetFrameMacType**](getframemactype.md)  
[**GetFrameNumber**](getframenumber.md)  
[**GetFrameTimeStamp**](getframetimestamp.md)  
</dl>

[*Esperti*](e.md) e [*parser*](p.md) possono chiamare la **funzione GetFrameFromFrameHandle.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





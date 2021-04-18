---
description: La funzione GetFrameFromFrameHandle restituisce un puntatore a un frame da un handle di frame.
ms.assetid: 790fe5fe-a857-4947-a471-d0538c0f0d61
title: Funzione GetFrameFromFrameHandle (Netmon. h)
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
ms.openlocfilehash: ce8151b2f4c81c61dea5969ff52e9ddf2d6615a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305908"
---
# <a name="getframefromframehandle-function"></a>GetFrameFromFrameHandle (funzione)

La funzione **GetFrameFromFrameHandle** restituisce un puntatore a un frame da un handle di frame.

## <a name="syntax"></a>Sintassi


```C++
ULPFRAME WINAPI GetFrameFromFrameHandle(
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

Se la funzione ha esito positivo, il valore restituito è un puntatore al frame.

Se la funzione ha esito negativo, il valore restituito è 0.

## <a name="remarks"></a>Commenti

La funzione **GetFrameFromFrameHandle** recupera i dati che non possono essere recuperati dalle altre funzioni helper fornite da Network Monitor. Quando possibile, utilizzare le funzioni seguenti.

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

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrameFromFrameHandle** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





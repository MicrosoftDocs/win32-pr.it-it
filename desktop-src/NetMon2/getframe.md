---
description: La funzione GetFrame restituisce un handle a un frame specificato all'interno di un'acquisizione.
ms.assetid: d40bc364-0028-4006-a6c2-6ee100366ba3
title: Funzione GetFrame (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5f6f992c0c61978e2de6f90755852c9e29d6ac51d7ae7f2405ef981ed695c4b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779251"
---
# <a name="getframe-function"></a>Funzione GetFrame

La **funzione GetFrame** restituisce un handle a un frame specificato all'interno di un'acquisizione.

## <a name="syntax"></a>Sintassi


```C++
HFRAME WINAPI GetFrame(
  _In_ HCAPTURE hCapture,
  _In_ DWORD    FrameNumber
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hCapture* \[ Pollici\]
</dt> <dd>

Handle per un'acquisizione. Per ottenere l'handle di acquisizione, chiamare [la funzione GetFrameCaptureHandle.](getframecapturehandle.md)

</dd> <dt>

*FrameNumber* \[ Pollici\]
</dt> <dd>

Numero (in base zero) del frame. Il numero del primo frame in un'acquisizione è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle per il frame.

Se la funzione ha esito negativo, ovvero se *hCapture* non è valido o il numero di frame non è compreso nell'intervallo, il valore restituito è **NULL.**

## <a name="remarks"></a>Commenti

Usare la **funzione GetFrame** per ottenere l'handle di frame necessario quando si individuano istanze di una proprietà. Le funzioni usate per individuare le istanze di proprietà sono [FindPropertyInstance](findpropertyinstance.md) che individua la prima istanza e [FindPropertyInstanceRestart,](findpropertyinstancerestart.md) che individua l'istanza successiva.

[*Esperti*](e.md) e [*parser possono*](p.md) chiamare la **funzione GetFrame.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[FindPropertyInstance](findpropertyinstance.md)
</dt> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 





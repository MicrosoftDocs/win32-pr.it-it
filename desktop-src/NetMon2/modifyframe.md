---
description: La funzione ModifyFrame modifica un frame esistente con nuovi dati.
ms.assetid: ebd248e4-b248-4f4a-8b94-a6d1c331d12a
title: Funzione ModifyFrame (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ModifyFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 04bc22af11d83078ecf98d0386b061b520fbf9a8dcab6f6beb360c45b1c6fe96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555821"
---
# <a name="modifyframe-function"></a>Funzione ModifyFrame

La **funzione ModifyFrame** modifica un frame esistente con nuovi dati.

## <a name="syntax"></a>Sintassi


```C++
HFRAME WINAPI ModifyFrame(
  _In_  HCAPTURE hCapture,
  _In_  DWORD    FrameNumber,
  _In_  LPBYTE   FrameData,
  _In_  DWORD    FrameLength,
  _Out_ __int64  TimeStamp
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hCapture* \[ Pollici\]
</dt> <dd>

Handle per l'acquisizione. Per informazioni su come ottenere l'handle di acquisizione, vedere la sezione Osservazioni di questo **argomento ModifyFrame.**

</dd> <dt>

*FrameNumber* \[ Pollici\]
</dt> <dd>

Numero di indice del frame.

</dd> <dt>

*FrameData* \[ Pollici\]
</dt> <dd>

Puntatore a una matrice di byte che contengono i nuovi dati del frame.

</dd> <dt>

*FrameLength* \[ Pollici\]
</dt> <dd>

Lunghezza dei nuovi dati, in byte.

</dd> <dt>

*TimeStamp* \[ Cambio\]
</dt> <dd>

Timestamp che indica quando il frame è stato modificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle per un nuovo frame.

Se la funzione ha esito negativo, il valore restituito è **NULL.**

## <a name="remarks"></a>Commenti

Se la chiamata ha esito positivo, **la funzione ModifyFrame** elimina il frame originale.

[*Esperti*](e.md) e [*parser possono*](p.md) chiamare la **funzione ModifyFrame.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





---
description: La funzione ModifyFrame modifica un frame esistente con nuovi dati.
ms.assetid: ebd248e4-b248-4f4a-8b94-a6d1c331d12a
title: Funzione ModifyFrame (Netmon. h)
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
ms.openlocfilehash: af3ef6c2c5ccae2b6410ac8fc81c815f790b17a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307714"
---
# <a name="modifyframe-function"></a>ModifyFrame (funzione)

La funzione **ModifyFrame** modifica un frame esistente con nuovi dati.

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

*hCapture* \[ in\]
</dt> <dd>

Handle per l'acquisizione. Per informazioni sull'acquisizione dell'handle di acquisizione, vedere la sezione Osservazioni di questo argomento **ModifyFrame** .

</dd> <dt>

*NumeroFrame* \[ in\]
</dt> <dd>

Numero di indice del frame.

</dd> <dt>

*FrameData* \[ in\]
</dt> <dd>

Puntatore a una matrice di byte che contiene i nuovi dati del frame.

</dd> <dt>

*FrameLength* \[ in\]
</dt> <dd>

Lunghezza dei nuovi dati, in byte.

</dd> <dt>

*Timestamp* \[ out\]
</dt> <dd>

Timestamp che indica il momento in cui è stato modificato il frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle per un nuovo frame.

Se la funzione ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

Se la chiamata ha esito positivo, la funzione **ModifyFrame** Elimina il frame originale.

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **ModifyFrame** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





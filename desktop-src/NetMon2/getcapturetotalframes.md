---
description: La funzione GetCaptureTotalFrames restituisce il numero totale di fotogrammi nell'acquisizione.
ms.assetid: a2b7902c-b80f-4a0a-b12a-2a139df30fca
title: Funzione GetCaptureTotalFrames (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTotalFrames
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2a7cae78dd95521fa80dfd9b9637b332c72ed1c82b90ba1f6c932824181ef565
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910781"
---
# <a name="getcapturetotalframes-function"></a>Funzione GetCaptureTotalFrames

La **funzione GetCaptureTotalFrames** restituisce il numero totale di fotogrammi nell'acquisizione.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI GetCaptureTotalFrames(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hCapture* \[ Pollici\]
</dt> <dd>

Handle per l'acquisizione. Per informazioni su come ottenere l'handle di acquisizione, vedere la sezione Osservazioni di questo **argomento GetCaptureTotalFrames.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è il numero totale di frame nell'acquisizione.

Se la funzione ha esito negativo, il valore restituito è 0.

## <a name="remarks"></a>Commenti

[*Esperti*](e.md) e [*parser*](p.md) possono chiamare **la funzione GetCaptureTotalFrames.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 





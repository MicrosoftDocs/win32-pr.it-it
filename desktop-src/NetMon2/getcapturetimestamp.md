---
description: La funzione GetCaptureTimeStamp restituisce l'ora e la data in cui l'acquisizione ha avviato la registrazione dei fotogrammi.
ms.assetid: a7120a7c-5031-4c71-a177-f08c41037b3c
title: Funzione GetCaptureTimeStamp (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 93ae1c94a5e83d0029aba4403ad4ba23db0f4006bb5b9be68cc469939e63c734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366636"
---
# <a name="getcapturetimestamp-function"></a>Funzione GetCaptureTimeStamp

La **funzione GetCaptureTimeStamp** restituisce l'ora e la data in cui l'acquisizione ha avviato la registrazione dei fotogrammi.

## <a name="syntax"></a>Sintassi


```C++
LPSYSTEMTIME WINAPI GetCaptureTimeStamp(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hCapture* \[ Pollici\]
</dt> <dd>

Handle per l'acquisizione. Per informazioni su come ottenere l'handle di acquisizione, vedere la sezione Osservazioni di questo **argomento GetCaptureTimeStamp.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore a una [struttura SYSTEMTIME.](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

Se la funzione ha esito negativo, il valore restituito è **NULL.**

## <a name="remarks"></a>Commenti

La **funzione GetCaptureTimeStamp** restituisce l'ora in cui il provider di pacchetti di rete (NPP) inizia a raccogliere dati, non quando l'esperto carica l'acquisizione per l'analisi.

Non sovrascrivere i dati nella **struttura SYSTEMTIME.** I dati fanno parte dell'acquisizione. Il tentativo di modificare i dati causa una violazione di accesso.

[*Esperti*](e.md) e [*parser*](p.md) possono chiamare la **funzione GetCaptureTimeStamp.**

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

[Systemtime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 


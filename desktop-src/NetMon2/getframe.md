---
description: La funzione GetFrame restituisce un handle per un frame specificato all'interno di un'acquisizione.
ms.assetid: d40bc364-0028-4006-a6c2-6ee100366ba3
title: Funzione GetFrame (Netmon. h)
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
ms.openlocfilehash: 3f79e7fa6fc4e79f4dea804769cc9d51b8096860
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128342"
---
# <a name="getframe-function"></a>Funzione GetFrame

La funzione **GetFrame** restituisce un handle per un frame specificato all'interno di un'acquisizione.

## <a name="syntax"></a>Sintassi


```C++
HFRAME WINAPI GetFrame(
  _In_ HCAPTURE hCapture,
  _In_ DWORD    FrameNumber
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hCapture* \[ in\]
</dt> <dd>

Handle per un'acquisizione. Per ottenere l'handle di acquisizione, chiamare la funzione [GetFrameCaptureHandle](getframecapturehandle.md) .

</dd> <dt>

*NumeroFrame* \[ in\]
</dt> <dd>

Numero (in base zero) del frame. Il numero del primo fotogramma in un'acquisizione è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle per il frame.

Se la funzione ha esito negativo, ovvero se *hCapture* non è valido o il numero di frame non è compreso nell'intervallo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

Usare la funzione **GetFrame** per ottenere l'handle di frame necessario per l'individuazione delle istanze di una proprietà. Le funzioni utilizzate per individuare le istanze di proprietà sono [FindPropertyInstance](findpropertyinstance.md) che individua la prima istanza e [FindPropertyInstanceRestart](findpropertyinstancerestart.md) che individua l'istanza successiva.

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetFrame** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[FindPropertyInstance](findpropertyinstance.md)
</dt> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 





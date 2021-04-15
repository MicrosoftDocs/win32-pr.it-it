---
description: La funzione GetCaptureTimeStamp restituisce l'ora e la data di inizio della registrazione dei frame dall'acquisizione.
ms.assetid: a7120a7c-5031-4c71-a177-f08c41037b3c
title: Funzione GetCaptureTimeStamp (Netmon. h)
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
ms.openlocfilehash: 855aa8b5432fd06bb25571fcb48c091dcfe502f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525140"
---
# <a name="getcapturetimestamp-function"></a>GetCaptureTimeStamp (funzione)

La funzione **GetCaptureTimeStamp** restituisce l'ora e la data di inizio della registrazione dei frame dall'acquisizione.

## <a name="syntax"></a>Sintassi


```C++
LPSYSTEMTIME WINAPI GetCaptureTimeStamp(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hCapture* \[ in\]
</dt> <dd>

Handle per l'acquisizione. Per informazioni sull'acquisizione dell'handle di acquisizione, vedere la sezione Osservazioni di questo argomento **GetCaptureTimeStamp** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore a una struttura [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .

Se la funzione ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

La funzione **GetCaptureTimeStamp** restituisce l'ora in cui il provider di pacchetti di rete (NPP) inizia a raccogliere i dati, non quando l'esperto carica l'acquisizione per l'analisi.

Non sovrascrivere i dati nella struttura **SYSTEMTIME** . I dati fanno parte dell'acquisizione. Il tentativo di modificare i dati causa una violazione di accesso.

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetCaptureTimeStamp** .

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

[SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 


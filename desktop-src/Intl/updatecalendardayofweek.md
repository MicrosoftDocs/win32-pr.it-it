---
description: Deprecato. Ottiene il giorno della settimana che corrisponde a un giorno specificato e popola il membro DayOfWeek nella struttura CALDATETIME specificata con tale valore.
ms.assetid: b9ae250a-73bb-4ec2-bb0d-e1f8b25c173c
title: Funzione UpdateCalendarDayOfWeek
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateCalendarDayOfWeek
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 0e7060c03b06fe855c096e94469797dedb20d74ec1d9de43e11b866c3afb0ed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560651"
---
# <a name="updatecalendardayofweek-function"></a>Funzione UpdateCalendarDayOfWeek

Deprecato. Ottiene il giorno della settimana che corrisponde a un giorno specificato e popola il membro **DayOfWeek** nella struttura [**CALDATETIME**](caldatetime.md) specificata con tale valore.

## <a name="syntax"></a>Sintassi


```C++
BOOL UpdateCalendarDayOfWeek(
  _Inout_ LPCALDATETIME lpCalDateTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpCalDateTime* \[ in, out\]
</dt> <dd>

Puntatore alla [**struttura CALDATETIME**](caldatetime.md) contenente la data per la quale impostare il giorno della settimana.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo o FALSE **in** caso contrario. Per ottenere informazioni estese sull'errore, l'applicazione può [**chiamare GetLastError,**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)che può restituire uno dei codici di errore seguenti:

-   DATA \_ ERRORE NON COMPRESO \_ \_ \_ NELL'INTERVALLO. La data specificata non è in intervallo.
-   ERRORE \_ PARAMETRO NON \_ VALIDO. Uno dei valori dei parametri non è valido.

## <a name="remarks"></a>Commenti

A questa funzione non è associato un file di intestazione o un file di libreria. L'applicazione può chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della DLL (Kernel32.dll) per ottenere un handle di modulo. Può quindi chiamare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con l'handle del modulo e il nome di questa funzione per ottenere l'indirizzo della funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto linguistico nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto per il linguaggio nazionale](national-language-support-functions.md)
</dt> <dt>

[**CALDATETIME**](caldatetime.md)
</dt> </dl>

 

 

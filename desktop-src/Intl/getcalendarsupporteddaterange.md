---
description: Deprecato. Ottiene l'intervallo di date supportato per un calendario specificato.
ms.assetid: fe036ac5-77c0-4e83-8d70-db3fa0f7c803
title: GetCalendarSupportedDateRange (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarSupportedDateRange
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 57b1175ef7bcf5b6b5d91af63682ca565bc0f1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967917"
---
# <a name="getcalendarsupporteddaterange-function"></a>GetCalendarSupportedDateRange (funzione)

Deprecato. Ottiene l'intervallo di date supportato per un calendario specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL GetCalendarSupportedDateRange(
  _In_  CALID         Calendar,
  _Out_ LPCALDATETIME lpCalMinDateTime,
  _Out_ LPCALDATETIME lpCalMaxDateTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Calendario* \[ in\]
</dt> <dd>

[Identificatore del calendario](calendar-identifiers.md) per il quale ottenere l'intervallo di date supportato.

</dd> <dt>

*lpCalMinDateTime* \[ out\]
</dt> <dd>

Puntatore a una struttura [**CALDATETIME**](caldatetime.md) che definisce la data minima supportata.

</dd> <dt>

*lpCalMaxDateTime* \[ out\]
</dt> <dd>

Puntatore a una struttura [**CALDATETIME**](caldatetime.md) che definisce la data massima supportata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario. Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:

-   ERRORE \_ parametro non valido \_ . Uno dei valori di parametro non è valido.

## <a name="remarks"></a>Commenti

La data meno recente supportata da questa funzione è il 1 gennaio 1601.

A questa funzione non è associato un file di intestazione o un file di libreria. L'applicazione può chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome della DLL (Kernel32.dll) per ottenere un handle del modulo. Può quindi chiamare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con l'handle del modulo e il nome di questa funzione per ottenere l'indirizzo della funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto per lingua nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto del linguaggio nazionale](national-language-support-functions.md)
</dt> <dt>

[NLS: esempio di API basate su nome](nls--name-based-apis-sample.md)
</dt> </dl>

 

 

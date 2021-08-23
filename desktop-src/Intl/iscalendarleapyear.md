---
description: Deprecato. Identifica se l'anno specificato è bisestile all'interno dell'era specificata per il calendario specifico.
ms.assetid: 91f58915-f0c6-4c7a-9d9a-96e255d799fd
title: Funzione IsCalendarLeapYear
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCalendarLeapYear
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: fe89f11bbaf41235449e882626680cf4d4af075d93f76c2d2aacd90d8d38707a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948730"
---
# <a name="iscalendarleapyear-function"></a>Funzione IsCalendarLeapYear

Deprecato. Identifica se l'anno specificato è bisestile all'interno dell'era specificata per il calendario specifico.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsCalendarLeapYear(
  _In_ CALID calId,
  _In_ UINT  year,
  _In_ UINT  era
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*calId* \[ Pollici\]
</dt> <dd>

Identificatore [del calendario da](calendar-identifiers.md) utilizzare per controllare l'anno bisestile.

</dd> <dt>

*year* \[ Pollici\]
</dt> <dd>

Anno da controllare.

</dd> <dt>

*era* \[ Pollici\]
</dt> <dd>

Era da controllare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'anno specificato è bisestile oppure FALSE in caso **contrario.** Per ottenere informazioni estese sull'errore, l'applicazione può [**chiamare GetLastError,**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)che può restituire uno dei codici di errore seguenti:

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
</dt> </dl>

 

 

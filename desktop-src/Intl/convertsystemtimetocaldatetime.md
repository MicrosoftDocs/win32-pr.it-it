---
description: Deprecato. Converte una struttura SYSTEMTIME specificata in una struttura CALDATETIME.
ms.assetid: d21f75bc-1a93-4cb9-8b9b-6fa0e81886bf
title: Funzione ConvertSystemTimeToCalDateTime
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertSystemTimeToCalDateTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 01eb78f9045e43db3e97b252a8fdf8fe8ed7297905174efeff2f3b2bbe1a5171
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746041"
---
# <a name="convertsystemtimetocaldatetime-function"></a>Funzione ConvertSystemTimeToCalDateTime

Deprecato. Converte una struttura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) specificata in una [**struttura CALDATETIME.**](caldatetime.md)

## <a name="syntax"></a>Sintassi


```C++
BOOL ConvertSystemTimeToCalDateTime(
  _In_  const SYSTEMTIME   *lpSysTime,
  _In_        CALID         calId,
  _Out_       LPCALDATETIME lpCalDateTime

);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpSysTime* \[ Pollici\]
</dt> <dd>

Puntatore alla [**struttura SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) da convertire.

</dd> <dt>

*calId* \[ Pollici\]
</dt> <dd>

Identificatore del [calendario di sistema](calendar-identifiers.md) da utilizzare nella conversione.

</dd> <dt>

*lpCalDateTime* \[ Cambio\]
</dt> <dd>

Puntatore alla struttura [**CALDATETIME**](caldatetime.md) equivalente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o FALSE **in** caso contrario. Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:

-   ERRORE \_ PARAMETRO \_ NON VALIDO. Uno dei valori dei parametri non è valido.

## <a name="remarks"></a>Commenti

La data meno recente supportata da questa funzione è il 1° gennaio 1601.

A questa funzione non è associato un file di intestazione o un file di libreria. L'applicazione può chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) con il nome dll (Kernel32.dll) per ottenere un handle del modulo. Può quindi chiamare [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) con l'handle del modulo e il nome di questa funzione per ottenere l'indirizzo della funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto linguistico nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto linguistico nazionale](national-language-support-functions.md)
</dt> <dt>

[Recupero di informazioni su ora e data](time-and-date.md)
</dt> </dl>

 

 

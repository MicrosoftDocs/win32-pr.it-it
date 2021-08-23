---
description: Deprecato. Regola una data in base a un numero specificato di anni, mesi, settimane o giorni.
ms.assetid: be8d61fd-efa3-4386-969f-30216c282ebc
title: Funzione AdjustCalendarDate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdjustCalendarDate
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 061d0e246f7839345b0f1e55221d26d276f52af4997a7cb47d62b680d2638fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520621"
---
# <a name="adjustcalendardate-function"></a>Funzione AdjustCalendarDate

Deprecato. Regola una data in base a un numero specificato di anni, mesi, settimane o giorni.

## <a name="syntax"></a>Sintassi


```C++
BOOL AdjustCalendarDate(
  _Inout_ LPCALDATETIME        lpCalDateTime,
  _In_    CALDATETIME_DATEUNIT calUnit,
  _Out_   INT                  amount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpCalDateTime* \[ in, out\]
</dt> <dd>

Puntatore a una [**struttura CALDATETIME**](caldatetime.md) che contiene le informazioni sulla data e sul calendario da modificare.

</dd> <dt>

*calUnit* \[ Pollici\]
</dt> <dd>

Valore [**di enumerazione CALDATETIME \_ DATEUNIT**](caldatetime-dateunit.md) che indica l'unità di data, ad esempio DayUnit.

</dd> <dt>

*amount* \[ Cambio\]
</dt> <dd>

Importo in base al quale modificare la data specificata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o FALSE **in** caso contrario. Per ottenere informazioni estese sull'errore, l'applicazione può chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), che può restituire uno dei codici di errore seguenti:

-   DATA \_ DI ERRORE NON COMPRESO \_ \_ \_ NELL'INTERVALLO. La data specificata non è in intervallo.
-   ERRORE \_ PARAMETRO \_ NON VALIDO. Uno dei valori dei parametri non è valido.

## <a name="remarks"></a>Commenti

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

[NLS: Esempio di API basate sui nomi](nls--name-based-apis-sample.md)
</dt> </dl>

 

 

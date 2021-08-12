---
description: Apre la chiave del Registro di sistema specificata in un hive del Registro di sistema offline.
ms.assetid: 4a4afbef-5107-4006-bd67-aecb5d3b5112
title: Funzione OROpenKey (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 4c0f641925fbc35fba6072ee395f67fad540dcd2ec5198b945ad658a723238b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667096"
---
# <a name="oropenkey-function"></a>OROpenKey - funzione

Apre la chiave del Registro di sistema specificata in un hive del Registro di sistema offline.

## <a name="syntax"></a>Sintassi


```C++
DWORD OROpenKey(
  _In_     ORHKEY  Handle,
  _In_opt_ PCWSTR  lpSubKeyName,
  _Out_    PORHKEY phkResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Handle* \[ Pollici\]
</dt> <dd>

Handle per una chiave del Registro di sistema aperta in un hive del Registro di sistema offline.

</dd> <dt>

*lpSubKeyName* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa UNICODE contenente il nome della chiave del Registro di sistema da aprire. Questa chiave deve essere una sottochiave della chiave identificata dal *parametro Handle.*

I nomi delle chiavi non supportano la distinzione tra maiuscole e minuscole.

Se questo parametro è **NULL** o un puntatore a una stringa vuota, la funzione restituisce lo stesso handle passato. Se la chiave specificata dal parametro *Handle* è la chiave radice dell'hive, la funzione restituisce ERROR \_ INVALID \_ PARAMETER.

Per altre informazioni, vedere [Limiti delle dimensioni degli elementi del Registro di sistema.](../sysinfo/registry-element-size-limits.md)

</dd> <dt>

*phkResult* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve un handle per la chiave aperta. Usare la [**funzione ORCloseKey**](orclosekey.md) per chiudere la chiave dopo aver terminato di usare l'handle.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror.h. È possibile usare la [funzione FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con il flag FORMAT \_ MESSAGE FROM SYSTEM per ottenere una \_ \_ descrizione generica dell'errore.

Se l'handle da restituire è un handle per la chiave radice dell'hive, la funzione restituisce ERROR \_ INVALID \_ PARAMETER.

Se la chiave specificata è stata contrassegnata come eliminata, questa funzione restituisce ERROR \_ KEY \_ DELETED.

## <a name="remarks"></a>Commenti

La **funzione OROpenKey** non può essere usata per aprire la chiave radice in un hive del Registro di sistema offline. Per ottenere un handle per la chiave radice di un hive, usare la [**funzione OROpenHive**](oropenhive.md) per caricare l'hive in memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows Libreria del Registro di sistema offline versione 1.0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenHive**](oropenhive.md)
</dt> </dl>

 

 

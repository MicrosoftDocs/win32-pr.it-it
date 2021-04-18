---
description: Apre la chiave del registro di sistema specificata in un hive del registro di sistema offline.
ms.assetid: 4a4afbef-5107-4006-bd67-aecb5d3b5112
title: Funzione OROpenKey (offreg. h)
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
ms.openlocfilehash: 4a55bb2c06d8b2d13491b766bf08184631fa2164
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331465"
---
# <a name="oropenkey-function"></a>OROpenKey (funzione)

Apre la chiave del registro di sistema specificata in un hive del registro di sistema offline.

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

*Gestisci* \[ in\]
</dt> <dd>

Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.

</dd> <dt>

*lpSubKeyName* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una stringa UNICODE che contiene il nome della chiave del registro di sistema da aprire. Questa chiave deve essere una sottochiave della chiave identificata dal parametro *handle* .

Per i nomi di chiave non viene fatta distinzione tra maiuscole

Se questo parametro è **null** o un puntatore a una stringa vuota, la funzione restituisce lo stesso handle passato. Se la chiave specificata dal parametro *handle* è la chiave radice dell'hive, la funzione restituisce un parametro di errore \_ non valido \_ .

Per altre informazioni, vedere [limiti delle dimensioni degli elementi del registro di sistema](../sysinfo/registry-element-size-limits.md).

</dd> <dt>

*phkResult* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve un handle per la chiave aperta. Usare la funzione [**ORCloseKey**](orclosekey.md) per chiudere la chiave dopo aver terminato di usare l'handle.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.

Se l'handle da restituire è un handle per la chiave radice dell'hive, la funzione restituisce l'errore \_ parametro non valido \_ .

Se la chiave specificata è stata contrassegnata come eliminata, questa funzione restituisce la chiave di errore \_ \_ eliminata.

## <a name="remarks"></a>Commenti

Non è possibile usare la funzione **OROpenKey** per aprire la chiave radice in un hive del registro di sistema offline. Per ottenere un handle per la chiave radice di un hive, usare la funzione [**OROpenHive**](oropenhive.md) per caricare l'hive in memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows offline Registry Library versione 1,0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
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

 

 

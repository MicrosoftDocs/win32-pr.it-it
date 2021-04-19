---
description: Elimina una sottochiave e i relativi valori da un hive del registro di sistema offline.
ms.assetid: 651795d3-4328-4281-9a7f-ba75b4ec4da1
title: Funzione ORDeleteKey (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a122be2e738bb16730eee31772fc2c1c0671eddb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331954"
---
# <a name="ordeletekey-function"></a>ORDeleteKey (funzione)

Elimina una sottochiave e i relativi valori da un hive del registro di sistema offline.

## <a name="syntax"></a>Sintassi


```C++
DWORD ORDeleteKey(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpSubKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Gestisci* \[ in\]
</dt> <dd>

Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline. Questo handle viene restituito dalla funzione [**ORCreateKey**](orcreatekey.md) o [**OROpenKey**](oropenkey.md) .

</dd> <dt>

*lpSubKey* \[ in, facoltativo\]
</dt> <dd>

Nome della chiave da eliminare. Deve essere una sottochiave della chiave che *gestisce* gli identificatori, ma non può avere sottochiavi.

Se la sottochiave non esiste, la funzione restituisce un errore \_ non \_ trovato.

Se questo parametro è **null**, la funzione Elimina la chiave specificata dal parametro *handle* . Se la chiave specificata dal parametro *handle* è la chiave radice dell'hive, la funzione restituisce un parametro di errore \_ non valido \_ .

Per i nomi di chiave non viene fatta distinzione tra maiuscole

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag. I codici di errore possibili includono i seguenti:

-   Se la sottochiave specificata non esiste, la funzione restituisce il \_ file di errore \_ non \_ trovato.
-   Se la sottochiave specificata è la chiave radice dell'hive del registro di sistema, la funzione restituisce l'errore \_ parametro non valido \_ .
-   Se la sottochiave specificata include sottochiavi, la funzione restituisce la chiave di errore \_ \_ con \_ elementi figlio.

## <a name="remarks"></a>Commenti

Se la chiave del registro di sistema specificata esiste, viene contrassegnata come eliminata. Una chiave eliminata non viene rimossa fino a quando non viene chiuso l'ultimo handle.

La chiave da eliminare non deve contenere sottochiavi. Per eliminare una chiave e tutte le relative sottochiavi, utilizzare la funzione [**OREnumKey**](orenumkey.md) per enumerare le sottochiavi ed eliminarle singolarmente.

È possibile chiamare solo la funzione [**ORCloseKey**](orclosekey.md) su una chiave eliminata. tutte le altre operazioni del registro di sistema offline non riescono Se la chiave eliminata è stata creata in modo esplicito chiamando [**ORCreateKey**](orcreatekey.md), le risorse associate alla chiave vengono rilasciate quando viene chiuso l'ultimo handle per la chiave eliminata.

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

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 

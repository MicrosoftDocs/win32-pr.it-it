---
description: Elimina una sottochiave e i relativi valori da un hive del Registro di sistema offline.
ms.assetid: 651795d3-4328-4281-9a7f-ba75b4ec4da1
title: Funzione ORDeleteKey (Offreg.h)
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
ms.openlocfilehash: 9f3be934eca97d88f4dfeb1b1576d9fcd06f5681351a2e85d8ae7f6ba31e8860
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571931"
---
# <a name="ordeletekey-function"></a>Funzione ORDeleteKey

Elimina una sottochiave e i relativi valori da un hive del Registro di sistema offline.

## <a name="syntax"></a>Sintassi


```C++
DWORD ORDeleteKey(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpSubKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Handle* \[ Pollici\]
</dt> <dd>

Handle di una chiave del Registro di sistema aperta in un hive del Registro di sistema offline. Questo handle viene restituito dalla [**funzione ORCreateKey**](orcreatekey.md) [**o OROpenKey.**](oropenkey.md)

</dd> <dt>

*lpSubKey* \[ in, facoltativo\]
</dt> <dd>

Nome della chiave da eliminare. Deve essere una sottochiave della chiave identificata da *Handle,* ma non può avere sottochiavi.

Se la sottochiave non esiste, la funzione restituisce ERROR \_ NOT \_ FOUND.

Se questo parametro è **NULL,** la funzione elimina la chiave specificata dal *parametro Handle.* Se la chiave specificata dal *parametro Handle* è la chiave radice dell'hive, la funzione restituisce ERROR \_ INVALID \_ PARAMETER.

Per i nomi delle chiavi non viene fatto distinzione tra maiuscole e minuscole.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror.h. È possibile usare la [funzione FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con il flag FORMAT \_ MESSAGE FROM SYSTEM per ottenere una \_ \_ descrizione generica dell'errore. I codici di errore possibili includono i seguenti:

-   Se la sottochiave specificata non esiste, la funzione restituisce ERROR \_ FILE \_ NOT \_ FOUND.
-   Se la sottochiave specificata è la chiave radice dell'hive del Registro di sistema, la funzione restituisce ERROR \_ INVALID \_ PARAMETER.
-   Se la sottochiave specificata contiene sottochiavi, la funzione restituisce ERROR \_ KEY \_ HAS \_ CHILDREN.

## <a name="remarks"></a>Commenti

Se la chiave del Registro di sistema specificata esiste, viene contrassegnata come eliminata. Una chiave eliminata non viene rimossa fino alla chiusura dell'ultimo handle.

La chiave da eliminare non deve avere sottochiavi. Per eliminare una chiave e tutte le relative sottochiavi, usare la [**funzione OREnumKey**](orenumkey.md) per enumerare le sottochiavi ed eliminarle singolarmente.

Solo la [**funzione ORCloseKey**](orclosekey.md) può essere chiamata su una chiave eliminata. tutte le altre operazioni del Registro di sistema offline hanno esito negativo. Se la chiave eliminata è stata creata in modo esplicito chiamando [**ORCreateKey,**](orcreatekey.md)le risorse associate alla chiave vengono rilasciate alla chiusura dell'ultimo handle per la chiave eliminata.

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

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 

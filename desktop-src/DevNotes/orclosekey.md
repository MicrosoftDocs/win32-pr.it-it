---
description: Chiude un handle per la chiave del Registro di sistema specificata in un hive del Registro di sistema offline.
ms.assetid: 01bb21b1-217b-4716-ae1e-466cf8383155
title: Funzione ORCloseKey (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 28f93c2bb1de61da072d7fde6d811463106be0c56f049b3ebf7e74f79ef740fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572111"
---
# <a name="orclosekey-function"></a>Funzione ORCloseKey

Chiude un handle per la chiave del Registro di sistema specificata in un hive del Registro di sistema offline.

## <a name="syntax"></a>Sintassi


```C++
DWORD ORCloseKey(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Handle* \[ Pollici\]
</dt> <dd>

Handle di una chiave del Registro di sistema aperta in un hive del Registro di sistema offline.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror.h. È possibile usare la [funzione FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con il flag FORMAT \_ MESSAGE FROM SYSTEM per ottenere una \_ \_ descrizione generica dell'errore.

Se la chiave specificata è la chiave radice dell'hive del Registro di sistema, la funzione ha esito negativo con ERROR \_ INVALID \_ PARAMETER.

## <a name="remarks"></a>Commenti

L'handle per una chiave specificata non deve essere usato dopo la chiusura, perché non sarà più valido. Gli handle di chiave non devono essere lasciati aperti più a lungo del necessario.

Usare la [**funzione ORCloseHive**](orclosehive.md) per chiudere un hive del Registro di sistema offline.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows Libreria del Registro di sistema offline versione 1.0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 

---
description: Rimuove un valore denominato dalla chiave del registro di sistema specificata in un hive del registro di sistema offline.
ms.assetid: d2192607-34b8-4915-ac86-8ee206993071
title: Funzione ORDeleteValue (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 426765950fd38cbb3e3c99f4001db2965ddb07e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331949"
---
# <a name="ordeletevalue-function"></a>ORDeleteValue (funzione)

Rimuove un valore denominato dalla chiave del registro di sistema specificata in un hive del registro di sistema offline.

## <a name="syntax"></a>Sintassi


```C++
DWORD ORDeleteValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Gestisci* \[ in\]
</dt> <dd>

Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.

</dd> <dt>

*lpValueName* \[ in, facoltativo\]
</dt> <dd>

Valore del registro di sistema da rimuovere. Se questo parametro è **null** o una stringa vuota, viene rimosso il valore predefinito senza nome impostato dalla funzione [**ORSetValue**](orsetvalue.md) .

Per i nomi di valore non viene fatta distinzione tra maiuscole

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows offline Registry Library versione 1,0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORSetValue**](orsetvalue.md)
</dt> </dl>

 

 

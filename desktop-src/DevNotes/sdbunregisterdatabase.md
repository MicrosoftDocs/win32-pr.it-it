---
description: Annulla la registrazione del database specificato, rendendolo non più disponibile.
ms.assetid: 7e6c50f4-85f6-4b33-b639-d8fda143e5e7
title: SdbUnregisterDatabase (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbUnregisterDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 72171e1f9ae20ac2213a285046b2499093be4313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483117"
---
# <a name="sdbunregisterdatabase-function"></a>SdbUnregisterDatabase (funzione)

Annulla la registrazione del database specificato, rendendolo non più disponibile.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbUnregisterDatabase(
  _In_ GUID *pguidDB
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pguidDB* \[ in\]
</dt> <dd>

GUID del database. Questo parametro non può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbRegisterDatabaseEx**](sdbregisterdatabaseex.md)
</dt> </dl>

 

 





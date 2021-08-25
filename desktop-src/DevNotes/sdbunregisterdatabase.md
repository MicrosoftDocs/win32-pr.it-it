---
description: Annulla la registrazione del database specificato, rendendolo non più disponibile.
ms.assetid: 7e6c50f4-85f6-4b33-b639-d8fda143e5e7
title: Funzione SdbUnregisterDatabase
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
ms.openlocfilehash: 2ea0cfeedbf74bea02af60b8c01d04b9e0e02f527ba35c0478da801253687b8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815311"
---
# <a name="sdbunregisterdatabase-function"></a>Funzione SdbUnregisterDatabase

Annulla la registrazione del database specificato, rendendolo non più disponibile.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbUnregisterDatabase(
  _In_ GUID *pguidDB
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pguidDB* \[ Pollici\]
</dt> <dd>

GUID del database. Questo parametro non può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **TRUE in caso** di esito positivo o FALSE **in** caso di esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbRegisterDatabaseEx**](sdbregisterdatabaseex.md)
</dt> </dl>

 

 





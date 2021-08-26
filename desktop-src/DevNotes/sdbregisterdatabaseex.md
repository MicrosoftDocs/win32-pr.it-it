---
description: Registra il database specificato.
ms.assetid: 65eceb1a-9ce1-4b97-98d7-731932797794
title: Funzione SdbRegisterDatabaseEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbRegisterDatabaseEx
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 512e180549c246a5504bc14675d61082c68904aa767d98deca5111d9a275dc60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984101"
---
# <a name="sdbregisterdatabaseex-function"></a>Funzione SdbRegisterDatabaseEx

Registra il database specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbRegisterDatabaseEx(
  _In_     LPCTSTR    pszDatabasePath,
  _In_     DWORD      dwDatabaseType,
  _In_opt_ PULONGLONG pTimeStamp
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszDatabasePath* \[ Pollici\]
</dt> <dd>

Percorso del database. Questo parametro non può essere **NULL.**

</dd> <dt>

*dwDatabaseType* \[ Pollici\]
</dt> <dd>

Tipo di database. Per [un elenco di valori, vedere Tipi di database Shim.](shim-database-types.md)

</dd> <dt>

*pTimeStamp* \[ in, facoltativo\]
</dt> <dd>

Timestamp per il database. Se questo parametro è **NULL,** viene usata l'ora di sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **TRUE in caso** di esito positivo o FALSE **in** caso di errore.

## <a name="remarks"></a>Commenti

Un database deve essere registrato prima di poter usare qualsiasi altra funzione SDB.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbUnregisterDatabase**](sdbunregisterdatabase.md)
</dt> </dl>

 

 





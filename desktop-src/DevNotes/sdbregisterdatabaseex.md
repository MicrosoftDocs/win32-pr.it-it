---
description: Registra il database specificato.
ms.assetid: 65eceb1a-9ce1-4b97-98d7-731932797794
title: SdbRegisterDatabaseEx (funzione)
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
ms.openlocfilehash: 74872f8895032abe02b024396fda12c43dc1611d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523345"
---
# <a name="sdbregisterdatabaseex-function"></a>SdbRegisterDatabaseEx (funzione)

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

*pszDatabasePath* \[ in\]
</dt> <dd>

Percorso del database. Questo parametro non può essere **null**.

</dd> <dt>

*dwDatabaseType* \[ in\]
</dt> <dd>

Tipo di database. Vedere [tipi di database shim](shim-database-types.md) per un elenco di valori.

</dd> <dt>

*pTimeStamp* \[ in, facoltativo\]
</dt> <dd>

Timestamp del database. Se questo parametro è **null**, viene utilizzata l'ora di sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.

## <a name="remarks"></a>Commenti

Prima di poter utilizzare qualsiasi altra funzione SDB, è necessario registrare un database.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbUnregisterDatabase**](sdbunregisterdatabase.md)
</dt> </dl>

 

 





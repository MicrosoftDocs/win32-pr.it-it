---
description: Apre il database shim specificato.
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: Funzione SdbOpenDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: df0081d7373bf67d3df1723be7d5beb272ef7ee4c77c54da8a6985dfe250d7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161194"
---
# <a name="sdbopendatabase-function"></a>Funzione SdbOpenDatabase

Apre il database shim specificato.

## <a name="syntax"></a>Sintassi


```C++
PDB WINAPI SdbOpenDatabase(
  _In_ LPCTSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwszPath* \[ Pollici\]
</dt> <dd>

Percorso del database. Questo parametro non può essere **NULL.**

</dd> <dt>

*eType* \[ Pollici\]
</dt> <dd>

Tipo di percorso. Per un elenco di valori, vedere PATH [**\_ TYPE.**](path-type.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un handle al database shim.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> </dl>

 

 





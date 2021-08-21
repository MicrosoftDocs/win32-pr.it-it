---
description: Crea un nuovo database shim.
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: Funzione SdbCreateDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCreateDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 6c7ac5d30c9c5a0154d770266410d278c5c3f31a65166515078a5384b1b8b55d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161558"
---
# <a name="sdbcreatedatabase-function"></a>Funzione SdbCreateDatabase

Crea un nuovo database shim.

## <a name="syntax"></a>Sintassi


```C++
PDB WINAPI SdbCreateDatabase(
  _In_ LPCWSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwszPath* \[ Pollici\]
</dt> <dd>

Percorso in cui salvare il database. Questo parametro non può essere **NULL.**

</dd> <dt>

*eType* \[ Pollici\]
</dt> <dd>

Tipo di percorso. Per un elenco di valori, vedere PATH [**\_ TYPE.**](path-type.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un handle al database shim o **NULL in caso** di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 





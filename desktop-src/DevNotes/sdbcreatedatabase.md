---
description: Crea un nuovo database shim.
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: SdbCreateDatabase (funzione)
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
ms.openlocfilehash: 1ab8b8071cc210f6129545985d2d2e089680f0f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966116"
---
# <a name="sdbcreatedatabase-function"></a>SdbCreateDatabase (funzione)

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

*pwszPath* \[ in\]
</dt> <dd>

Percorso in cui salvare il database. Questo parametro non può essere **null**.

</dd> <dt>

*etype* \[ in\]
</dt> <dd>

Tipo di percorso. Per un elenco di valori, vedere [**\_ tipo di percorso**](path-type.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un handle per il database shim o **null** in caso di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 





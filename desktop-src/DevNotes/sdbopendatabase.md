---
description: Apre il database shim specificato.
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: SdbOpenDatabase (funzione)
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
ms.openlocfilehash: ae0bca035f203593c43bb36e70119fbaf3024059
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747855"
---
# <a name="sdbopendatabase-function"></a>SdbOpenDatabase (funzione)

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

*pwszPath* \[ in\]
</dt> <dd>

Percorso del database. Questo parametro non può essere **null**.

</dd> <dt>

*etype* \[ in\]
</dt> <dd>

Tipo di percorso. Per un elenco di valori, vedere [**\_ tipo di percorso**](path-type.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un handle per il database shim.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> </dl>

 

 





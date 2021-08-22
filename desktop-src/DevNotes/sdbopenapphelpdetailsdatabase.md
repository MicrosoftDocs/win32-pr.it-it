---
description: Apre il database dei dettagli apphelp specificato.
ms.assetid: c3b07c00-a3c6-419c-94c6-34c573a04d6d
title: Funzione SdbOpenApphelpDetailsDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpDetailsDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: d6bd0bc7cbd1404c3bcf5459254f53e62a777d0936b89a0f7a282dd8d0094227
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045161"
---
# <a name="sdbopenapphelpdetailsdatabase-function"></a>Funzione SdbOpenApphelpDetailsDatabase

Apre il database dei dettagli apphelp specificato.

## <a name="syntax"></a>Sintassi


```C++
PDB WINAPI SdbOpenApphelpDetailsDatabase(
  _In_opt_ LPCWSTR pwsDetailsDatabasePath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwsDetailsDatabasePath* \[ in, facoltativo\]
</dt> <dd>

Percorso del database. Se questo parametro è **NULL,** viene aperto il database di sistema locale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un handle per il database dei dettagli di Apphelp.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 





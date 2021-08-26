---
description: Recupera il TAG associato al TAGID specificato.
ms.assetid: 194d2035-fc2c-445d-a730-90db2ccea8af
title: Funzione SdbGetTagFromTagID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetTagFromTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a7e58343cf9a863f6b3cecc7f9b6414414387e2f2b33859de1eb015d65f1a78b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058471"
---
# <a name="sdbgettagfromtagid-function"></a>Funzione SdbGetTagFromTagID

Recupera il TAG associato all'elemento **TAGID specificato.**

## <a name="syntax"></a>Sintassi


```C++
TAG WINAPI SdbGetTagFromTagID(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdb* \[ Pollici\]
</dt> <dd>

Handle per il database shim.

</dd> <dt>

*tiWhich* \[ Pollici\]
</dt> <dd>

**TAGID per** il TAG.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce IL TAG.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TAG**](tag.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 





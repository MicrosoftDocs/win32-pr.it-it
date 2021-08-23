---
description: Scrive una voce NULL nel database specificato.
ms.assetid: 2a29389b-d4f6-4527-a429-c9459b095f2f
title: Funzione SdbWriteNULLTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteNULLTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 363f137ecc7887114040bac76607438e0b0bfd4dbf4f3e74659c98c0906164a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815081"
---
# <a name="sdbwritenulltag-function"></a>Funzione SdbWriteNULLTag

Scrive una **voce NULL** nel database specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbWriteNULLTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdb* \[ Pollici\]
</dt> <dd>

Handle per il database shim.

</dd> <dt>

*tTag* \[ Pollici\]
</dt> <dd>

TAG per la voce. Questo TAG deve essere di tipo **TAG \_ TYPE \_ NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **TRUE in caso** di esito positivo o FALSE **in** caso di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbWriteBinaryTag**](sdbwritebinarytag.md)
</dt> <dt>

[**SdbWriteDWORDTag**](sdbwritedwordtag.md)
</dt> <dt>

[**SdbWriteStringTag**](sdbwritestringtag.md)
</dt> <dt>

[**SdbWriteWORDTag**](sdbwritewordtag.md)
</dt> </dl>

 

 





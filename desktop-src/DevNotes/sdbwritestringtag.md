---
description: Scrive una stringa nel database specificato.
ms.assetid: 72c62d91-0c1c-4ff8-8829-1c3ec1fa8648
title: Funzione SdbWriteStringTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 942d7995e002f7f211a84c333d44e26531e361beec0adfaaa75ad7dc433ea3b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075965"
---
# <a name="sdbwritestringtag-function"></a>Funzione SdbWriteStringTag

Scrive una stringa nel database specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbWriteStringTag(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszData
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

TAG per la voce. Questo TAG deve essere di tipo **TAG \_ TYPE \_ STRINGREF**.

</dd> <dt>

*pwszData* \[ Pollici\]
</dt> <dd>

Stringa con terminazione Null. Questo parametro non può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **TRUE in caso** di esito positivo o FALSE **in** caso di esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbWriteBinaryTag**](sdbwritebinarytag.md)
</dt> <dt>

[**SdbWriteDWORDTag**](sdbwritedwordtag.md)
</dt> <dt>

[**SdbWriteQWORDTag**](sdbwriteqwordtag.md)
</dt> <dt>

[**SdbWriteWORDTag**](sdbwritewordtag.md)
</dt> </dl>

 

 





---
description: Recupera i dati binari per il TAGID specificato.
ms.assetid: 18992406-67b4-4c48-9629-04d6bf1c5824
title: Funzione SdbGetBinaryTagData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetBinaryTagData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5bb2155c7fe2ff1ae2d9784777e39740e5b3224cfc60881fbe0d961ddb422360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058521"
---
# <a name="sdbgetbinarytagdata-function"></a>Funzione SdbGetBinaryTagData

Recupera i dati binari per l'elemento **TAGID specificato.**

## <a name="syntax"></a>Sintassi


```C++
PVOID WINAPI SdbGetBinaryTagData(
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

**TAGID** che corrisponde ai dati da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un puntatore ai dati binari o **NULL se** **TAGID** non è valido.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
</dt> <dt>

[**SdbReadDWORDTag**](sdbreaddwordtag.md)
</dt> <dt>

[**SdbReadQWORDTag**](sdbreadqwordtag.md)
</dt> <dt>

[**SdbReadStringTag**](sdbreadstringtag.md)
</dt> </dl>

 

 





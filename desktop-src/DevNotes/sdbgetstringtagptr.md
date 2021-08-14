---
description: Recupera i dati stringa per l'ELEMENTO TAGID specificato.
ms.assetid: c558e0bb-7e35-4298-93fb-400db00a2972
title: Funzione SdbGetStringTagPtr
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetStringTagPtr
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e14c499b5f23f342192ad42b72f8a4c29f8312adbf6bbcb8310ee182cd457f18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404430"
---
# <a name="sdbgetstringtagptr-function"></a>Funzione SdbGetStringTagPtr

Recupera i dati stringa per **l'ELEMENTO TAGID specificato.**

## <a name="syntax"></a>Sintassi


```C++
LPTSTR WINAPI SdbGetStringTagPtr(
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

**TAGID** che corrisponde ai dati stringa da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un puntatore ai dati stringa o **NULL** se **TAGID** non è valido o non è di tipo **TAG TYPE \_ \_ STRING** o **TAG TYPE \_ \_ STRINGREF.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbGetBinaryTagData**](sdbgetbinarytagdata.md)
</dt> <dt>

[**SdbReadDWORDTag**](sdbreaddwordtag.md)
</dt> <dt>

[**SdbReadQWORDTag**](sdbreadqwordtag.md)
</dt> <dt>

[**SdbReadStringTag**](sdbreadstringtag.md)
</dt> </dl>

 

 





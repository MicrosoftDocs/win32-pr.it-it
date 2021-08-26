---
Description: Recupera la stringa per il TAGID specificato.
ms.assetid: d67d386d-a2c5-46e2-8887-9ee20ea427f9
title: Funzione SdbReadStringTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 8f8652e944328298b7cd3888fa93c41d3551ba913f4acd848f60fa053ed0067e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044941"
---
# <a name="sdbreadstringtag-function"></a>Funzione SdbReadStringTag

Recupera la stringa per **l'ELEMENTO TAGID specificato.**

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SdbReadStringTag(
  _In_  PDB    pdb,
  _In_  TAGID  tiWhich,
  _Out_ LPTSTR pwszBuffer,
  _In_  DWORD  cchBufferSize
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

</dd> <dt>

*pwszBuffer* \[ Cambio\]
</dt> <dd>

Buffer che riceve la stringa. Questo parametro non può essere **NULL.**

</dd> <dt>

*cchBufferSize* \[ Pollici\]
</dt> <dd>

Dimensione del buffer *pwszBuffer,* in caratteri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce **TRUE in caso** di esito positivo o FALSE **in** caso di errore.

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

[**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
</dt> <dt>

[**SdbReadBinaryTag**](sdbreadbinarytag.md)
</dt> <dt>

[**SdbReadDWORDTag**](sdbreaddwordtag.md)
</dt> </dl>

 

 





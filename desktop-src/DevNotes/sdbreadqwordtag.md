---
Description: Recupera il valore QWORD per l'ELEMENTO TAGID specificato.
ms.assetid: 5fa94a95-c7f3-477b-ab7c-931e8d62d501
title: Funzione SdbReadQWORDTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4280c21983fa86312229930b7496625c594f0caac384f0dc6d130f673ce68509
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815281"
---
# <a name="sdbreadqwordtag-function"></a>Funzione SdbReadQWORDTag

Recupera il valore **QWORD** per l'elemento **TAGID specificato.**

## <a name="syntax"></a>Sintassi


```C++
ULONGLONG WINAPI SdbReadQWORDTag(
  _In_ PDB       pdb,
  _In_ TAGID     tiWhich,
  _In_ ULONGLONG qwDefault
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

*qwDefault* \[ Pollici\]
</dt> <dd>

Valore predefinito da restituire in caso di errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce il valore in caso di esito positivo o *qwDefault in* caso di esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbGetBinaryTagData**](sdbgetbinarytagdata.md)
</dt> <dt>

[**SdbGetStringTagPtr**](sdbgetstringtagptr.md)
</dt> <dt>

[**SdbReadDWORDTag**](sdbreaddwordtag.md)
</dt> <dt>

[**SdbReadStringTag**](sdbreadstringtag.md)
</dt> </dl>

 

 





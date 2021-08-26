---
description: Crea un nuovo tag di elenco per le operazioni di scrittura.
ms.assetid: 3a52e2f2-9648-45fb-b487-ccfe5ed24f7f
title: Funzione SdbBeginWriteListTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbBeginWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 448b57e73bec0115d4c2ae87be96630cad6542833da66a2de8e02037c264de83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058581"
---
# <a name="sdbbeginwritelisttag-function"></a>Funzione SdbBeginWriteListTag

Crea un nuovo tag di elenco per le operazioni di scrittura.

## <a name="syntax"></a>Sintassi


```C++
TAGID WINAPI SdbBeginWriteListTag(
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

TAG per la nuova voce. Questo valore deve essere di tipo **TAG \_ TYPE \_ LIST.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce il [**TAGID del**](tagid.md) nuovo elenco in caso di esito positivo o **TAGID \_ NULL in** caso di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbCloseDatabase**](sdbclosedatabase.md)
</dt> <dt>

[**SdbCloseDatabaseWrite**](sdbclosedatabasewrite.md)
</dt> <dt>

[**SdbEndWriteListTag**](sdbendwritelisttag.md)
</dt> <dt>

[**TAG**](tag.md)
</dt> <dt>

[Tipi TAG](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 





---
description: Cerca un TAG figlio all'interno dell'elemento padre specificato e restituisce il TAGID del primo elemento figlio.
ms.assetid: 67538c7e-6360-40fa-b50f-dcbc7a6a147d
title: Funzione SdbGetFirstChild
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFirstChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 58e63b3c1c8b3e56c9610ec795c1706fe58990e4611c36886ee4a3061d0816fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075975"
---
# <a name="sdbgetfirstchild-function"></a>Funzione SdbGetFirstChild

Cerca un TAG figlio all'interno dell'elemento padre specificato e restituisce **il TAGID** del primo elemento figlio.

## <a name="syntax"></a>Sintassi


```C++
TAGID WINAPI SdbGetFirstChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdb* \[ Pollici\]
</dt> <dd>

Handle per il database shim.

</dd> <dt>

*tiParent* \[ Pollici\]
</dt> <dd>

**TAGID dell'inizio** della ricerca. Questo parametro può essere **TAGID \_ ROOT o** **TAG TYPE \_ \_ LIST.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

TagID **del** primo elemento figlio o **TAGID \_ NULL** non trovato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> <dt>

[**SdbFindNextTag**](sdbfindnexttag.md)
</dt> <dt>

[**SdbGetNextChild**](sdbgetnextchild.md)
</dt> </dl>

 

 





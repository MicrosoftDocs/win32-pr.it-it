---
description: Cerca il TAG figlio successivo all'interno dell'elemento padre specificato e restituisce il TAGID del successivo elemento figlio.
ms.assetid: c7311f20-15ca-4b2d-a08d-8bb992a3a0cd
title: Funzione SdbGetNextChild
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetNextChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 210e0aab8cb5e43bfc649e8abb72cf565c4d4f892f651708286f7a3f87d11ce2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045314"
---
# <a name="sdbgetnextchild-function"></a>Funzione SdbGetNextChild

Cerca il TAG figlio successivo all'interno dell'elemento padre specificato e restituisce **il TAGID** del successivo elemento figlio.

## <a name="syntax"></a>Sintassi


```C++
TAGID WINAPI SdbGetNextChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
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

</dd> <dt>

*tiPrev* \[ Pollici\]
</dt> <dd>

**TAGID dell'elemento** figlio precedente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**TAGID dell'elemento** figlio o **TAGID \_ NULL** se non viene trovato alcun elemento figlio.

## <a name="remarks"></a>Commenti

Prima di chiamare questa funzione, chiamare la [**funzione SdbGetFirstChild.**](sdbgetfirstchild.md)

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

[**SdbGetFirstChild**](sdbgetfirstchild.md)
</dt> </dl>

 

 





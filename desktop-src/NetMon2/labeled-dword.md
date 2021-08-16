---
description: La struttura \_ DWORD CON ETICHETTA definisce un'etichetta che viene visualizzata quando viene rilevato un valore di proprietà DWORD specifico.
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: LABELED_DWORD struttura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_DWORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 10f3e0dd09b37821a00f2c10f99c0ea6d509ff388e9d7394a8b2c4958438f979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364846"
---
# <a name="labeled_dword-structure"></a>Struttura \_ DWORD CON ETICHETTA

La **struttura \_ DWORD CON ETICHETTA** definisce un'etichetta che viene visualizzata quando viene rilevato un valore di proprietà DWORD specifico.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _LABELED_DWORD {
  DWORD Value;
  LPSTR Label;
} LABELED_DWORD, *LPLABELED_DWORD;
```



## <a name="members"></a>Members

<dl> <dt>

**Valore**
</dt> <dd>

Valore DWORD della proprietà che si desidera rilevare.

</dd> <dt>

**Etichetta**
</dt> <dd>

Descrizione testuale o etichetta visualizzata quando viene rilevato il valore DWORD specificato nel **membro** Value.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **membro lpLabeledDwordTable** della struttura [SET](set.md) punta a una matrice di strutture **SET** che definiscono uno o più membri **Label** delle coppie di valori DWORD. Le coppie vengono usate quando si vuole visualizzare un'etichetta al posto di un valore DWORD specifico presente nel pacchetto del protocollo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 





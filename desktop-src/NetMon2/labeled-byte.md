---
description: La struttura LABELED \_ BYTE definisce una coppia BIT etichettata. L'etichetta della coppia BIT etichettata viene visualizzata quando viene rilevato un valore della proprietà byte specifico.
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: LABELED_BYTE struttura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BYTE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 05aa29942768c0c40816eafce112f12a95cd0a713bebe612d2e5ad32776a33a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494981"
---
# <a name="labeled_byte-structure"></a>Struttura LABELED \_ BYTE

La **struttura LABELED \_ BYTE** definisce una coppia BIT etichettata. **L'etichetta** della coppia BIT etichettata viene visualizzata quando viene rilevato un valore della proprietà byte specifico.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _LABELED_BYTE {
  BYTE  Value;
  LPSTR Label;
} LABELED_BYTE, *LPLABELED_BYTE;
```



## <a name="members"></a>Members

<dl> <dt>

**Valore**
</dt> <dd>

Valore BYTE della proprietà che si desidera rilevare.

</dd> <dt>

**Etichetta**
</dt> <dd>

Descrizione testuale o etichetta visualizzata quando viene rilevato il valore specificato nel **membro** Value.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **membro lpLabeledByteTable** della struttura [SET](set.md) punta a una matrice di strutture **SET** che definiscono uno o più membri **Label** delle coppie valore BYTE. Queste coppie vengono usate quando si vuole visualizzare un'etichetta al posto di un valore BYTE specifico presente nel pacchetto del protocollo.

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

 

 





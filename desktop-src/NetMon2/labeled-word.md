---
description: La struttura LABELED \_ WORD definisce un'etichetta che viene visualizzata quando viene rilevato un valore della proprietà WORD specifico.
ms.assetid: bfb1d34e-4a07-493f-8e43-508b77cce581
title: LABELED_WORD struttura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_WORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2e2e1ec7aad8c62828596839a537e49c5ff613fc10f3fb0d7966c926194433b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063791"
---
# <a name="labeled_word-structure"></a>Struttura WORD \_ CON ETICHETTA

La **struttura LABELED \_ WORD** definisce un'etichetta che viene visualizzata quando viene rilevato un valore della proprietà WORD specifico.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _LABELED_WORD {
  WORD  Value;
  LPSTR Label;
} LABELED_WORD, *LPLABELED_WORD;
```



## <a name="members"></a>Members

<dl> <dt>

**Valore**
</dt> <dd>

Valore WORD della proprietà che si desidera rilevare.

</dd> <dt>

**Etichetta**
</dt> <dd>

Descrizione testuale o etichetta visualizzata quando viene rilevato il valore WORD specificato nel **membro** Value.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **membro lpLabeledWordTable** della struttura [SET](set.md) punta a una matrice di strutture SET per definire una o più coppie di valori di etichetta. Queste coppie vengono usate quando si desidera visualizzare un'etichetta al posto di un valore WORD specifico trovato in un pacchetto di protocollo.

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

 

 





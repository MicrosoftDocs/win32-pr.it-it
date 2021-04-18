---
description: La struttura di \_ parole con etichetta definisce un'etichetta che viene visualizzata quando viene rilevato un valore della proprietà Word specifico.
ms.assetid: bfb1d34e-4a07-493f-8e43-508b77cce581
title: Struttura LABELED_WORD (Netmon. h)
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
ms.openlocfilehash: 445b24245d2e9d15c1c2b6d69de20c464cbf1724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315453"
---
# <a name="labeled_word-structure"></a>Struttura di \_ parole con etichetta

La struttura di **\_ parole con etichetta** definisce un'etichetta che viene visualizzata quando viene rilevato un valore della proprietà Word specifico.

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

Valore di parola della proprietà che si desidera rilevare.

</dd> <dt>

**Etichetta**
</dt> <dd>

Descrizione testuale o etichetta visualizzata quando viene rilevato il valore WORD specificato nel membro **value** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Il membro **lpLabeledWordTable** della struttura del [set](set.md) punta a una matrice di strutture set per definire una o più coppie di valori di etichetta. Queste coppie vengono utilizzate quando si desidera visualizzare un'etichetta al posto di un valore WORD specifico presente in un pacchetto di protocollo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 





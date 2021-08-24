---
description: La struttura LABELED \_ LARGEINT definisce un'etichetta che viene visualizzata quando viene rilevato un valore di proprietà LARGEINT specifico.
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: LABELED_LARGEINT struttura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_LARGEINT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: fab2942a2a5188527c57663af0c6000aa2cb628eaa2499eef054854df9187784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778771"
---
# <a name="labeled_largeint-structure"></a>Struttura \_ LARGEINT ETICHETTATA

La **struttura LABELED \_ LARGEINT** definisce un'etichetta che viene visualizzata quando viene rilevato un valore di proprietà LARGEINT specifico.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _LABELED_LARGEINT {
  LARGE_INTEGER Value;
  LPSTR         Label;
} LABELED_LARGEINT, *LPLABELED_LARGEINT;
```



## <a name="members"></a>Members

<dl> <dt>

**Valore**
</dt> <dd>

Valore LARGEINT della proprietà che si desidera rilevare.

</dd> <dt>

**Etichetta**
</dt> <dd>

Descrizione testuale o etichetta visualizzata quando viene rilevato il valore LARGEINT specificato nel **membro** Value.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **membro lpLabeledLargeIntTable** della struttura [SET](set.md) punta a una matrice di strutture **SET** che definiscono uno o più membri **Label** delle coppie di valori LARGEINT. Le coppie vengono usate quando si desidera visualizzare un'etichetta al posto di un valore LARGEINT specifico trovato in un pacchetto di protocollo.

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

 

 





---
description: La \_ struttura largeInt con etichetta definisce un'etichetta che viene visualizzata quando viene rilevato un valore specifico della proprietà LARGEINT.
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: Struttura LABELED_LARGEINT (Netmon. h)
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
ms.openlocfilehash: 4de92c3e67567ef86bb3d46905e595bd9d54c194
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050081"
---
# <a name="labeled_largeint-structure"></a>\_Struttura largeInt con etichetta

La struttura **\_ largeInt con etichetta** definisce un'etichetta che viene visualizzata quando viene rilevato un valore specifico della proprietà LARGEINT.

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

Descrizione testuale o etichetta visualizzata quando viene rilevato il valore LARGEINT specificato nel membro **value** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Il membro **lpLabeledLargeIntTable** della struttura [set](set.md) punta a una matrice di strutture **set** che definiscono uno o più membri **Label** delle coppie valore LARGEINT. Le coppie vengono utilizzate quando si desidera visualizzare un'etichetta al posto di un valore LARGEINT specifico presente in un pacchetto di protocollo.

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

 

 





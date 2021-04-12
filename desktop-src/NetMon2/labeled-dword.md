---
description: La \_ struttura DWORD con etichetta definisce un'etichetta che viene visualizzata quando viene rilevato un valore di proprietà DWORD specifico.
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: Struttura LABELED_DWORD (Netmon. h)
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
ms.openlocfilehash: 0bec068622683172116bf8c4f6e88450d5752920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232675"
---
# <a name="labeled_dword-structure"></a>\_Struttura DWORD con etichetta

La struttura **\_ DWORD con etichetta** definisce un'etichetta che viene visualizzata quando viene rilevato un valore di proprietà DWORD specifico.

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

Descrizione testuale o etichetta visualizzata quando viene rilevato il valore DWORD specificato nel membro **value** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Il membro **lpLabeledDwordTable** della struttura [set](set.md) punta a una matrice di strutture **set** che definiscono uno o più membri **Label** delle coppie valore DWORD. Le coppie vengono utilizzate quando si desidera visualizzare un'etichetta al posto di uno specifico valore DWORD presente nel pacchetto del protocollo.

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

 

 





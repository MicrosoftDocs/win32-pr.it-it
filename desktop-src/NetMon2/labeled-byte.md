---
description: La \_ struttura di byte con etichetta definisce una coppia di bit con etichetta. L'etichetta della coppia di BIT con etichetta viene visualizzata quando viene rilevato un valore di proprietà byte specifico.
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: Struttura LABELED_BYTE (Netmon. h)
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
ms.openlocfilehash: 4768e605892b9bfe2a3df67fbdea862f67dc1a16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315454"
---
# <a name="labeled_byte-structure"></a>Struttura di \_ byte con etichetta

La struttura di **\_ byte con etichetta** definisce una coppia di bit con etichetta. L' **etichetta** della coppia di bit con etichetta viene visualizzata quando viene rilevato un valore di proprietà byte specifico.

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

Descrizione testuale o etichetta visualizzata quando viene rilevato il valore specificato nel membro **value** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Il membro **lpLabeledByteTable** della struttura [set](set.md) punta a una matrice di strutture **set** che definiscono uno o più membri **Label** delle coppie valore byte. Queste coppie vengono utilizzate quando si desidera visualizzare un'etichetta al posto di uno specifico valore BYTE trovato nel pacchetto del protocollo.

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

 

 





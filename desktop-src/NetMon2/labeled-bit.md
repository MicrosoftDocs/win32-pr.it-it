---
description: La \_ struttura di bit con etichetta definisce una coppia di bit etichetta.
ms.assetid: 500b5159-bf9f-49d4-8567-d8e462015eb0
title: Struttura LABELED_BIT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BIT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 24a56e832600b551dd3ab43ea93d59c5805af630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308163"
---
# <a name="labeled_bit-structure"></a>Struttura di \_ bit con etichetta

La struttura di **\_ bit con etichetta** definisce una coppia di bit etichetta.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _LABELED_BIT {
  BYTE  BitNumber;
  LPSTR LabelOff;
  LPSTR LabelOn;
} LABELED_BIT, *LPLABELED_BIT;
```



## <a name="members"></a>Members

<dl> <dt>

**BitNumber**
</dt> <dd>

Numero di BIT della coppia di BIT dell'etichetta. I valori sono compresi tra 0 e 255. Impostare il membro **bitnumber** sul bit utilizzato nel confronto del valore della proprietà.

</dd> <dt>

**LabelOff**
</dt> <dd>

Stringa o etichetta visualizzata quando il BIT specificato in **BitNumber** è uguale a zero. Ad esempio, una possibile etichetta è "bit OFF".

</dd> <dt>

**Sconosciutain**
</dt> <dd>

Stringa o etichetta visualizzata quando il BIT specificato in **BitNumber** è uguale a 1. Ad esempio, una possibile etichetta è "bit ON".

</dd> </dl>

## <a name="remarks"></a>Commenti

Una matrice di strutture di **\_ bit con etichetta** viene utilizzata per definire un set di coppie di bit di etichette. Un puntatore alla matrice viene specificato nel membro **lpLabeledBit** della struttura del [set](set.md) . Le coppie vengono utilizzate quando si desidera visualizzare un'etichetta basata sull'impostazione di ogni BIT. In genere, questo tipo di set viene utilizzato per indicare il valore di bit ON o OFF.

Quando viene specificato un set di BIT, Network Monitor Visualizza solo i bit inclusi nella matrice di strutture **set** . I bit non inclusi nella struttura del **set** non vengono visualizzati.

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

 

 





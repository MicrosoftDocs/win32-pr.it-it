---
description: La struttura LABELED \_ BIT definisce una coppia BIT di etichetta.
ms.assetid: 500b5159-bf9f-49d4-8567-d8e462015eb0
title: LABELED_BIT struttura (Netmon.h)
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
ms.openlocfilehash: fe08288929a5f14c4a920c52121c2ccfbdb35888f2ed220291e30e53a3ef0c6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364836"
---
# <a name="labeled_bit-structure"></a>Struttura LABELED \_ BIT

La **struttura LABELED \_ BIT** definisce una coppia BIT di etichetta.

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

**Numero di bit**
</dt> <dd>

Numero BIT della coppia BIT dell'etichetta. I valori sono compreso tra 0 e 255. Impostare il **membro Bitnumber** sul bit usato nel confronto del valore della proprietà.

</dd> <dt>

**LabelOff**
</dt> <dd>

Stringa o etichetta visualizzata quando bit specificato in **BitNumber** è uguale a zero. Ad esempio, una possibile etichetta è "Bit OFF".

</dd> <dt>

**LabelOn**
</dt> <dd>

Stringa o etichetta visualizzata quando bit specificato in **BitNumber** è uguale a 1. Ad esempio, una possibile etichetta è "Bit ON".

</dd> </dl>

## <a name="remarks"></a>Commenti

Una matrice di **strutture LABELED \_ BIT** viene usata per definire un set di coppie BIT di etichetta. Un puntatore alla matrice viene specificato nel **membro lpLabeledBit** della [struttura SET.](set.md) Le coppie vengono usate quando si vuole visualizzare un'etichetta in base all'impostazione di ogni BIT. In genere, questo tipo di set viene usato per indicare il valore ON o OFF dei BIT.

Quando si specifica un set BIT, Network Monitor visualizza solo i BIT inclusi nella matrice di **strutture SET.** I BIT non presenti nella **struttura SET** non vengono visualizzati.

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

 

 





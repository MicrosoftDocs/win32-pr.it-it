---
title: KEYARRAY (Mmsystem.h)
description: KEYARRAY specifica un tipo usato per definire una matrice di chiavi.
ms.assetid: af1a1d2f-4558-4374-93ab-5a705fc879ca
keywords:
- KEYARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 507c5f578b912a7b184f9f455bc4a730132b2316472d061532c48847c312302d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140041"
---
# <a name="keyarray"></a>KEYARRAY

KEYARRAY specifica un tipo usato per definire una matrice di chiavi.


```C++
typedef WORD KEYARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**KEYARRAY \[ MIDIPATCHSIZE\]**
</dt> <dd>

Ogni elemento nella matrice corrisponde a una patch di patch basata su chiave con ognuno dei 16 bit che rappresenta uno dei 16 canali MIDI. I bit vengono impostati per ognuno dei canali che usano la patch specifica. Ad esempio, se la patch per il numero di chiave 60 viene usata dai canali MIDI fisici 9 e 15, l'elemento 60 della matrice deve essere impostato su 0x8200.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Versione<br/>                  | MidI (Instrument Digital Interface), MIDI Types<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi MIDI](midi-event-types.md)
</dt> </dl>

 

 






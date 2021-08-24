---
title: PATCHARRAY (Mmsystem.h)
description: PATCHARRAY è un tipo usato per definire una matrice di patch MIDI.
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- PATCHARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d1d14696d7bb76827f902609cb1411f7890adeac53092e1b66b7eda16604320
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806071"
---
# <a name="patcharray"></a>PATCHARRAY

PATCHARRAY è un tipo usato per definire una matrice di patch MIDI.


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**PATCHARRAY \[ MIDIPATCHSIZE\]**
</dt> <dd>

Ogni elemento nella matrice corrisponde a una patch con ognuno dei 16 bit che rappresenta uno dei 16 canali MIDI. I bit vengono impostati per ognuno dei canali che usano la patch specifica. Ad esempio, se il numero di patch 0 viene usato dai canali MIDI fisici 0 e 8, l'elemento 0 della matrice deve essere impostato su 0x0101.

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

 

 






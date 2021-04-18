---
title: Matrice di matrici (mmsystem. h)
description: Key ARRAY specifica un tipo usato per definire una matrice di chiavi.
ms.assetid: af1a1d2f-4558-4374-93ab-5a705fc879ca
keywords:
- MIDIPATCHSIZE DI MATRICI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e45e46417fb3b6653ecae605aa60f775c1d654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301700"
---
# <a name="keyarray"></a>Matrice di matrici

Key ARRAY specifica un tipo usato per definire una matrice di chiavi.


```C++
typedef WORD KEYARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**MIDIPATCHSIZE di matrici \[\]**
</dt> <dd>

Ogni elemento nella matrice corrisponde a una patch di percussione basata su chiave con ognuno dei 16 bit che rappresenta uno dei 16 canali MIDI. Per ognuno dei canali che usano tale patch particolare sono impostati bit. Se, ad esempio, la patch di percussione per il numero di chiave 60 viene usata dai canali MIDI fisici 9 e 15, l'elemento 60 della matrice deve essere impostato su 0x8200.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Versione<br/>                  | MIDI (Musical Instrument Digital Interface), tipi MIDI<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi MIDI](midi-event-types.md)
</dt> </dl>

 

 






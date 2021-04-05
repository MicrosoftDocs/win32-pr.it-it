---
title: PATCHARRAY (mmsystem. h)
description: PATCHARRAY è un tipo usato per definire una matrice di patch MIDI.
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- PATCHARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e07af0e878fc0d2fc79d6d17aafd48fbd991fb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874625"
---
# <a name="patcharray"></a>PATCHARRAY

PATCHARRAY è un tipo usato per definire una matrice di patch MIDI.


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**\[MIDIPATCHSIZE PATCHARRAY\]**
</dt> <dd>

Ogni elemento nella matrice corrisponde a una patch con ognuno dei 16 bit che rappresenta uno dei 16 canali MIDI. Per ognuno dei canali che usano tale patch particolare sono impostati bit. Se, ad esempio, il numero di patch 0 viene usato dai canali MIDI fisici 0 e 8, l'elemento 0 della matrice deve essere impostato su 0x0101.

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

 

 






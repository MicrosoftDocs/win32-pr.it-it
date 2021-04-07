---
description: La struttura con etichetta \_ SYSTEMTIME definisce un'etichetta che viene visualizzata quando viene rilevato un valore specifico della Proprietà SYSTEMTIME.
ms.assetid: 307b490a-af8e-4f2a-a45a-33a84fcb4d5c
title: Struttura LABELED_SYSTEMTIME (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_SYSTEMTIME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4484d5ec55f700410eb80d11d2249cceceef43ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885470"
---
# <a name="labeled_systemtime-structure"></a>Struttura con etichetta \_ SYSTEMTIME

La struttura con **etichetta \_ SYSTEMTIME** definisce un'etichetta che viene visualizzata quando viene rilevato un valore specifico della Proprietà SYSTEMTIME.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _LABELED_SYSTEMTIME {
  SYSTEMTIME Value;
  LPSTR      Label;
} LABELED_SYSTEMTIME, *LPLABELED_SYSTEMTIME;
```



## <a name="members"></a>Members

<dl> <dt>

**Valore**
</dt> <dd>

Valore di SYSTEMTIME di una proprietà che si desidera rilevare.

</dd> <dt>

**Etichetta**
</dt> <dd>

Descrizione testuale o etichetta visualizzata quando viene rilevato il valore SYSTEMTIME specificato nel membro **value** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Il membro **lpLabeledSystemTimeTable** della struttura del [set](set.md) punta a una matrice di strutture **set** che definiscono una o più coppie di valori di etichetta. Le coppie vengono utilizzate quando si desidera visualizzare un'etichetta al posto di un valore LARGEINT specifico trovato nel pacchetto del protocollo.

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

 

 





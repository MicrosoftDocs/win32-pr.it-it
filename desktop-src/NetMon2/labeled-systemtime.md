---
description: La struttura LABELED \_ SYSTEMTIME definisce un'etichetta che viene visualizzata quando viene rilevato un valore della proprietà SYSTEMTIME specifico.
ms.assetid: 307b490a-af8e-4f2a-a45a-33a84fcb4d5c
title: LABELED_SYSTEMTIME struttura (Netmon.h)
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
ms.openlocfilehash: 94ce2a2e0b86c24ea6c16627fd0b866e18aaf48f3c1f0b318a601809e1ee03dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742711"
---
# <a name="labeled_systemtime-structure"></a>Struttura \_ SYSTEMTIME ETICHETTATA

La **struttura LABELED \_ SYSTEMTIME** definisce un'etichetta che viene visualizzata quando viene rilevato un valore della proprietà SYSTEMTIME specifico.

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

Valore SYSTEMTIME di una proprietà che si desidera rilevare.

</dd> <dt>

**Etichetta**
</dt> <dd>

Descrizione testuale o etichetta visualizzata quando viene rilevato il valore SYSTEMTIME specificato nel **membro** Value.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **membro lpLabeledSystemTimeTable** della struttura [SET](set.md) punta a una matrice di strutture **SET** che definiscono una o più coppie di valori di etichetta. Le coppie vengono usate quando si desidera visualizzare un'etichetta al posto di un valore LARGEINT specifico trovato nel pacchetto del protocollo.

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

 

 





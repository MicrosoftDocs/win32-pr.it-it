---
description: La struttura ANDEXP contiene una matrice di corrispondenze di criteri usate per valutare i dati dei frame.
ms.assetid: e5f4c030-eb2b-4cc9-9032-9ad4701b6503
title: Struttura ANDEXP (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ANDEXP
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7ee2ac65e10e0dc9be46ab103fe21abcc78dc403302b298f3eb2fc83000802cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117982953"
---
# <a name="andexp-structure"></a>Struttura ANDEXP

La **struttura ANDEXP** contiene una matrice di corrispondenze di criteri usate per valutare i dati dei frame.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _ANDEXP {
  DWORD        nPatternMatches;
  PATTERNMATCH PatternMatch[MAX_PATTERNS];
} ANDEXP, *LPANDEXP;
```



## <a name="members"></a>Members

<dl> <dt>

**nPatternMatches**
</dt> <dd>

Numero di corrispondenze di criteri.

</dd> <dt>

**PatternMatch**
</dt> <dd>

Matrice di elementi di corrispondenza del criterio. Si noti che ogni **struttura ANDEXP** può contenere fino a quattro elementi pattern match. Per altre informazioni su questo membro, vedere [Acquisizione di filtri](capture-filters.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

I modelli nella matrice **PatternMatch** MAX PATTERNS vengono uniti come peer nelle istruzioni \[ OR \_ \] logiche nel formato

(Modello 1 \| \| Modello 2 \| \| Modello 3).

Per altre informazioni sull'implementazione di questa struttura, vedere [Acquisizione di filtri](capture-filters.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 





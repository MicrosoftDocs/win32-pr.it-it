---
description: La struttura ANDEXP contiene una matrice di corrispondenze del criterio usate per valutare i dati del frame.
ms.assetid: e5f4c030-eb2b-4cc9-9032-9ad4701b6503
title: Struttura ANDEXP (Netmon. h)
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
ms.openlocfilehash: 1d27d5bdd51a45b31f518271053f44b45917cdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346836"
---
# <a name="andexp-structure"></a>Struttura ANDEXP

La struttura **ANDEXP** contiene una matrice di corrispondenze del criterio usate per valutare i dati del frame.

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

Numero di corrispondenze del criterio.

</dd> <dt>

**PatternMatch**
</dt> <dd>

Matrice di elementi delle corrispondenze dei criteri. Si noti che ogni struttura **ANDEXP** può contenere un massimo di quattro elementi di corrispondenza del criterio. Per ulteriori informazioni su questo membro, vedere [Capture filters](capture-filters.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

I modelli nella matrice **PatternMatch** \[ Max \_ patterns \] vengono uniti come peer nelle istruzioni OR logiche nel formato

(Modello 1 \| \| Schema 2 \| \| modello 3).

Per ulteriori informazioni sull'implementazione di questa struttura, vedere [Capture filters](capture-filters.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 





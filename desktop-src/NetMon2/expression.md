---
description: Contiene un gruppo di matrici ANDEXP valutate come peer.
ms.assetid: 14fa568c-9535-4415-923d-7e93ba4d2e80
title: Struttura EXPRESSION (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPRESSION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4efa1f79477e3dcc13bedfddb2cdca7fd660f5430b7d7f2b87dbd9d4b4425098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366839"
---
# <a name="expression-structure"></a>Struttura EXPRESSION

La **struttura EXPRESSION** contiene un gruppo di matrici **ANDEXP** valutate come peer nelle espressioni AND logiche, che hanno il formato

(ANDEXP 1 && ANDEXP 2 && ANDEXP 3).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _EXPRESSION {
  DWORD  nAndExps;
  ANDEXP AndExp[MAX_PATTERNS];
} EXPRESSION, *LPEXPRESSION;
```



## <a name="members"></a>Members

<dl> <dt>

**nAndExps**
</dt> <dd>

Numero di **modelli ANDEXP.**

</dd> <dt>

**AndExp**
</dt> <dd>

Matrice di **modelli ANDEXP.** Il filtro di acquisizione dispone tutte le righe di questa matrice come istruzioni AND logiche. Tenere presente che ogni struttura EXPRESSION può contenere un massimo di quattro **modelli ANDEXP.**

</dd> </dl>

## <a name="remarks"></a>Commenti

Per altre informazioni sull'implementazione di questa struttura come parte di un filtro di acquisizione, vedere [Filtri di acquisizione](capture-filters.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ANDEXP](andexp.md)
</dt> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 





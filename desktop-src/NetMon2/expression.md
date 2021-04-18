---
description: Contiene un gruppo di matrici ANDEXP valutate come peer.
ms.assetid: 14fa568c-9535-4415-923d-7e93ba4d2e80
title: Struttura di espressioni (Netmon. h)
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
ms.openlocfilehash: b6565c294c0d8e0a7a277769404cb8b1b206380e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305940"
---
# <a name="expression-structure"></a>Struttura dell'espressione

La struttura dell' **espressione** contiene un gruppo di matrici **ANDEXP** valutate come peer nelle espressioni and logiche, che hanno il formato

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

Numero di modelli di **ANDEXP** .

</dd> <dt>

**AndExp**
</dt> <dd>

Matrice di modelli di **ANDEXP** . Il filtro di acquisizione dispone tutte le righe di questa matrice come istruzioni AND logiche. Tenere presente che ogni struttura dell'espressione può contenere un massimo di quattro modelli di **ANDEXP** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Per ulteriori informazioni sull'implementazione di questa struttura come parte di un filtro di acquisizione, vedere [Capture filters](capture-filters.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ANDEXP](andexp.md)
</dt> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 





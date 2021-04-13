---
title: OP_POLICY_PART
description: Definizione di OP_POLICY_PART IDL
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: ef0e3b96ce564ed7ff8e2ce0886e33ca474a1cf8
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104399880"
---
# <a name="op_policy_part-structure"></a>Struttura OP_POLICY_PART

Contiene una matrice di strutture di OP_POLICY_ELEMENT_LIST.

## <a name="syntax"></a>Sintassi

```C++
typedef struct _OP_POLICY_PART
{
    ULONG                                       cElementLists;
    [size_is(cElementLists)]
                        POP_POLICY_ELEMENT_LIST pElementLists;
    OP_BLOB                                     Extension;
} OP_POLICY_PART, *POP_POLICY_PART;
```

## <a name="members"></a>Members

### <a name="celementlists"></a>cElementLists

Contiene il numero di elementi in pElementLists.

### <a name="pelementlists"></a>pElementLists

Contiene una matrice di strutture di OP_POLICY_ELEMENT_LIST.

### <a name="extension"></a>Estensione

Riservato per usi futuri e deve contenere tutti zeri.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)

[**\_ \_ elenco elementi criteri \_ op**](odj-op_policy_element_list.md)

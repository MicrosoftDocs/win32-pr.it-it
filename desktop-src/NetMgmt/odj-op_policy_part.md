---
title: OP_POLICY_PART
description: OP_POLICY_PART IDL Definition
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 8ad479c2e24d8c38e87a2100658be2afcf37d70d321e99433e3b05a3af35fa60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911481"
---
# <a name="op_policy_part-structure"></a>OP_POLICY_PART struttura

Contiene una matrice di OP_POLICY_ELEMENT_LIST struttura .

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

Contiene una matrice di OP_POLICY_ELEMENT_LIST struttura .

### <a name="extension"></a>Estensione

Riservato per un uso futuro e deve contenere tutti zeri.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta a un dominio offline**](odj-idl.md)

[**ELENCO DI \_ ELEMENTI DEI CRITERI DELLE \_ \_ OPERAZIONI**](odj-op_policy_element_list.md)

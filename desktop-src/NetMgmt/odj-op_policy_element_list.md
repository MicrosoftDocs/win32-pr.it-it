---
title: OP_POLICY_ELEMENT_LIST
description: OP_POLICY_ELEMENT_LIST definizione IDL
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 1fde1bb1d2794be4fd1bf799282a0257b78ae213453566208ff64bcf7a312654
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796863"
---
# <a name="op_policy_element_list-structure"></a>OP_POLICY_ELEMENT_LIST struttura

Definisce una chiave del Registro di sistema radice e una matrice di elementi chiave del Registro di sistema da configurare in tale chiave.

## <a name="syntax"></a>Sintassi

```C++
typedef struct _OP_POLICY_ELEMENT_LIST
{
    [string] wchar_t                            *pSource;
    ULONG                                       ulRootKeyId;
    ULONG                                       cElements;
    [size_is(cElements)]    POP_POLICY_ELEMENT  pElements;
} OP_POLICY_ELEMENT_LIST, *POP_POLICY_ELEMENT_LIST;
```

## <a name="members"></a>Members

### <a name="psource"></a>pSource

Contiene il percorso del Criteri di gruppo file da cui sono stati provenienti gli elementi contenuti.

### <a name="ulrootkeyid"></a>ulRootKeyId

Contiene l'identificatore della chiave del Registro di sistema radice. attualmente deve essere impostato su HKEY_LOCAL_MACHINE.

### <a name="celements"></a>cElements

Contiene il numero di elementi in pElements.

### <a name="pelements"></a>pElements

Contiene una matrice di OP_POLICY_ELEMENT elementi.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta a un dominio offline**](odj-idl.md)

[**ELEMENTO \_ CRITERI \_ OP**](odj-op_policy_element.md)

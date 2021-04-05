---
title: OP_POLICY_ELEMENT_LIST
description: Definizione di OP_POLICY_ELEMENT_LIST IDL
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3c46e7208e6c142b9f58a7704be9bd3461c845b2
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "103734698"
---
# <a name="op_policy_element_list-structure"></a>Struttura OP_POLICY_ELEMENT_LIST

Definisce una chiave del registro di sistema radice e una matrice di elementi chiave del registro di sistema da configurare con tale chiave.

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

Contiene il percorso del file Criteri di gruppo dal quale sono stati originati gli elementi contenuti.

### <a name="ulrootkeyid"></a>ulRootKeyId

Contiene l'identificatore della chiave del registro di sistema radice. attualmente deve essere impostato su HKEY_LOCAL_MACHINE.

### <a name="celements"></a>cElements

Contiene il numero di elementi in pEles.

### <a name="pelements"></a>pEle

Contiene una matrice di elementi OP_POLICY_ELEMENT.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)

[**\_elemento dei criteri op \_**](odj-op_policy_element.md)

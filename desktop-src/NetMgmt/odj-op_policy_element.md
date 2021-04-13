---
title: OP_POLICY_ELEMENT
description: Definizione di OP_POLICY_ELEMENT IDL
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: df6fc6852a5efd0a6a2e01a805878ed51bc7c263
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "104339834"
---
# <a name="op_policy_element-structure"></a>Struttura OP_POLICY_ELEMENT

Definisce una chiave del registro di sistema e un nome, un tipo e un valore che devono essere configurati in base a tale chiave.

## <a name="syntax"></a>Sintassi

```C++
typedef struct _OP_POLICY_ELEMENT
{
    [string] wchar_t                *pKeyPath;
    [string] wchar_t                *pValueName;
    ULONG                           ulValueType;
    ULONG                           cbValueData;
    [size_is(cbValueData)]  PBYTE   pValueData;
} OP_POLICY_ELEMENT, *POP_POLICY_ELEMENT;
```

## <a name="members"></a>Members

### <a name="pkeypath"></a>pKeyPath

Contiene il percorso della chiave del registro di sistema.

### <a name="pvaluename"></a>pValueName

Contiene il nome del valore del registro di sistema.

### <a name="ulvaluetype"></a>ulValueType

Contiene uno dei valori dei [tipi di valore del registro di sistema](../sysinfo/registry-value-types.md).

### <a name="cbvaluedata"></a>cbValueData

Contiene la dimensione di pValueData in byte.

### <a name="ulvaluetype"></a>ulValueType

Contiene il valore del valore del registro di sistema.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)
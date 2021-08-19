---
title: OP_POLICY_ELEMENT
description: OP_POLICY_ELEMENT definizione IDL
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74e81f09f4d45d42f5e9df585b88051ac1e96e8cd33e4c15807701e61825b43b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983385"
---
# <a name="op_policy_element-structure"></a>OP_POLICY_ELEMENT struttura

Definisce una chiave del Registro di sistema e un nome di valore, un tipo e un valore che devono essere configurati in tale chiave.

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

Contiene il percorso della chiave del Registro di sistema.

### <a name="pvaluename"></a>pValueName

Contiene il nome del valore del Registro di sistema.

### <a name="ulvaluetype"></a>ulValueType

Contiene uno dei valori di Tipi di valore [del Registro di sistema](../sysinfo/registry-value-types.md).

### <a name="cbvaluedata"></a>cbValueData

Contiene le dimensioni di pValueData in byte.

### <a name="ulvaluetype"></a>ulValueType

Contiene il valore del valore del Registro di sistema.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta a un dominio offline**](odj-idl.md)
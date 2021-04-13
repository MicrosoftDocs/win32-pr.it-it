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
# <a name="op_policy_element-structure"></a><span data-ttu-id="691f0-103">Struttura OP_POLICY_ELEMENT</span><span class="sxs-lookup"><span data-stu-id="691f0-103">OP_POLICY_ELEMENT structure</span></span>

<span data-ttu-id="691f0-104">Definisce una chiave del registro di sistema e un nome, un tipo e un valore che devono essere configurati in base a tale chiave.</span><span class="sxs-lookup"><span data-stu-id="691f0-104">Defines a registry key and a value name, type, and value that should be configured under that key.</span></span>

## <a name="syntax"></a><span data-ttu-id="691f0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="691f0-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="691f0-106">Members</span><span class="sxs-lookup"><span data-stu-id="691f0-106">Members</span></span>

### <a name="pkeypath"></a><span data-ttu-id="691f0-107">pKeyPath</span><span class="sxs-lookup"><span data-stu-id="691f0-107">pKeyPath</span></span>

<span data-ttu-id="691f0-108">Contiene il percorso della chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="691f0-108">Contains the path of the registry key.</span></span>

### <a name="pvaluename"></a><span data-ttu-id="691f0-109">pValueName</span><span class="sxs-lookup"><span data-stu-id="691f0-109">pValueName</span></span>

<span data-ttu-id="691f0-110">Contiene il nome del valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="691f0-110">Contains the name of the registry value.</span></span>

### <a name="ulvaluetype"></a><span data-ttu-id="691f0-111">ulValueType</span><span class="sxs-lookup"><span data-stu-id="691f0-111">ulValueType</span></span>

<span data-ttu-id="691f0-112">Contiene uno dei valori dei [tipi di valore del registro di sistema](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="691f0-112">Contains one of the values from [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>

### <a name="cbvaluedata"></a><span data-ttu-id="691f0-113">cbValueData</span><span class="sxs-lookup"><span data-stu-id="691f0-113">cbValueData</span></span>

<span data-ttu-id="691f0-114">Contiene la dimensione di pValueData in byte.</span><span class="sxs-lookup"><span data-stu-id="691f0-114">Contains the size of pValueData in bytes.</span></span>

### <a name="ulvaluetype"></a><span data-ttu-id="691f0-115">ulValueType</span><span class="sxs-lookup"><span data-stu-id="691f0-115">ulValueType</span></span>

<span data-ttu-id="691f0-116">Contiene il valore del valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="691f0-116">Contains the value of the registry value.</span></span>

## <a name="see-also"></a><span data-ttu-id="691f0-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="691f0-117">See also</span></span>

[<span data-ttu-id="691f0-118">**Definizioni IDL di aggiunta al dominio offline**</span><span class="sxs-lookup"><span data-stu-id="691f0-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
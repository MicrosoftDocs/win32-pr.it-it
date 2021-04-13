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
# <a name="op_policy_part-structure"></a><span data-ttu-id="6eaba-103">Struttura OP_POLICY_PART</span><span class="sxs-lookup"><span data-stu-id="6eaba-103">OP_POLICY_PART structure</span></span>

<span data-ttu-id="6eaba-104">Contiene una matrice di strutture di OP_POLICY_ELEMENT_LIST.</span><span class="sxs-lookup"><span data-stu-id="6eaba-104">Contains an array of OP_POLICY_ELEMENT_LIST structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eaba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6eaba-105">Syntax</span></span>

```C++
typedef struct _OP_POLICY_PART
{
    ULONG                                       cElementLists;
    [size_is(cElementLists)]
                        POP_POLICY_ELEMENT_LIST pElementLists;
    OP_BLOB                                     Extension;
} OP_POLICY_PART, *POP_POLICY_PART;
```

## <a name="members"></a><span data-ttu-id="6eaba-106">Members</span><span class="sxs-lookup"><span data-stu-id="6eaba-106">Members</span></span>

### <a name="celementlists"></a><span data-ttu-id="6eaba-107">cElementLists</span><span class="sxs-lookup"><span data-stu-id="6eaba-107">cElementLists</span></span>

<span data-ttu-id="6eaba-108">Contiene il numero di elementi in pElementLists.</span><span class="sxs-lookup"><span data-stu-id="6eaba-108">Contains the number of elements in pElementLists.</span></span>

### <a name="pelementlists"></a><span data-ttu-id="6eaba-109">pElementLists</span><span class="sxs-lookup"><span data-stu-id="6eaba-109">pElementLists</span></span>

<span data-ttu-id="6eaba-110">Contiene una matrice di strutture di OP_POLICY_ELEMENT_LIST.</span><span class="sxs-lookup"><span data-stu-id="6eaba-110">Contains an array of OP_POLICY_ELEMENT_LIST structures.</span></span>

### <a name="extension"></a><span data-ttu-id="6eaba-111">Estensione</span><span class="sxs-lookup"><span data-stu-id="6eaba-111">Extension</span></span>

<span data-ttu-id="6eaba-112">Riservato per usi futuri e deve contenere tutti zeri.</span><span class="sxs-lookup"><span data-stu-id="6eaba-112">Reserved for future use and must contain all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="6eaba-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6eaba-113">See also</span></span>

[<span data-ttu-id="6eaba-114">**Definizioni IDL di aggiunta al dominio offline**</span><span class="sxs-lookup"><span data-stu-id="6eaba-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="6eaba-115">**\_ \_ elenco elementi criteri \_ op**</span><span class="sxs-lookup"><span data-stu-id="6eaba-115">**OP\_POLICY\_ELEMENT\_LIST**</span></span>](odj-op_policy_element_list.md)

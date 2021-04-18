---
description: La \_ struttura PF HANDOFFSET definisce i protocolli che vengono consegnati al parser o i protocolli a cui il parser passa.
ms.assetid: 2fda399d-a09e-47b4-bb2e-95996de9f950
title: Struttura PF_HANDOFFSET (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1b5dc9620f3b1860b27af973432aa4218c05b63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314751"
---
# <a name="pf_handoffset-structure"></a><span data-ttu-id="bb766-103">\_Struttura PF HANDOFFSET</span><span class="sxs-lookup"><span data-stu-id="bb766-103">PF\_HANDOFFSET structure</span></span>

<span data-ttu-id="bb766-104">La struttura **PF \_ HANDOFFSET** definisce i protocolli che vengono consegnati al parser o i protocolli a cui il parser passa.</span><span class="sxs-lookup"><span data-stu-id="bb766-104">The **PF\_HANDOFFSET** structure defines the protocols that hand off to the parser, or the protocols that the parser hands off to.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb766-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb766-105">Syntax</span></span>


```C++
typedef struct _PF_HANDOFFSET {
  DWORD           nEntries;
  PF_HANDOFFENTRY Entry[];
} PF_HANDOFFSET, *PPF_HANDOFFSET;
```



## <a name="members"></a><span data-ttu-id="bb766-106">Members</span><span class="sxs-lookup"><span data-stu-id="bb766-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bb766-107">**nEntries**</span><span class="sxs-lookup"><span data-stu-id="bb766-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="bb766-108">Numero di protocolli.</span><span class="sxs-lookup"><span data-stu-id="bb766-108">Number of protocols.</span></span>

</dd> <dt>

<span data-ttu-id="bb766-109">**Voce**</span><span class="sxs-lookup"><span data-stu-id="bb766-109">**Entry**</span></span>
</dt> <dd>

<span data-ttu-id="bb766-110">Matrice di strutture [PF \_ HANDOFFENTRY](pf-handoffentry.md) che definiscono ogni protocollo.</span><span class="sxs-lookup"><span data-stu-id="bb766-110">An array of [PF\_HANDOFFENTRY](pf-handoffentry.md) structures that define each protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb766-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb766-111">Remarks</span></span>

<span data-ttu-id="bb766-112">La struttura [PF \_ PARSERINFO](pf-parserinfo.md) usa la struttura **PF \_ HANDOFFSET** per elencare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="bb766-112">The [PF\_PARSERINFO](pf-parserinfo.md) structure uses the **PF\_HANDOFFSET** structure to list the following:</span></span>

-   <span data-ttu-id="bb766-113">Protocolli passati al parser.</span><span class="sxs-lookup"><span data-stu-id="bb766-113">Which protocols hand off to the parser.</span></span>
-   <span data-ttu-id="bb766-114">Protocolli a cui il parser passa.</span><span class="sxs-lookup"><span data-stu-id="bb766-114">Which protocols the parser hands off to.</span></span>

<span data-ttu-id="bb766-115">È necessario allocare la struttura **PF \_ HANDOFFSET** usando **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="bb766-115">The **PF\_HANDOFFSET** structure must be allocated using **HeapAlloc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb766-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb766-116">Requirements</span></span>



| <span data-ttu-id="bb766-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb766-117">Requirement</span></span> | <span data-ttu-id="bb766-118">Valore</span><span class="sxs-lookup"><span data-stu-id="bb766-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bb766-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb766-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bb766-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bb766-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bb766-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb766-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bb766-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bb766-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bb766-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb766-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb766-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb766-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb766-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb766-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb766-126">PF \_ PARSERINFO</span><span class="sxs-lookup"><span data-stu-id="bb766-126">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> <dt>

[<span data-ttu-id="bb766-127">PF \_ HANDOFFENTRY</span><span class="sxs-lookup"><span data-stu-id="bb766-127">PF\_HANDOFFENTRY</span></span>](pf-handoffentry.md)
</dt> </dl>

 

 





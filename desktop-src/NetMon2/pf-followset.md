---
description: La struttura PF followt \_ definisce i protocolli che possono precedere o seguire un protocollo.
ms.assetid: ef444af9-edae-4547-9548-8a682c279f08
title: Struttura PF_FOLLOWSET (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f5c286d3b137df24f7da7f0fc5ae269a7a3d946d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314173"
---
# <a name="pf_followset-structure"></a><span data-ttu-id="aa3a0-103">\_Struttura PF follower</span><span class="sxs-lookup"><span data-stu-id="aa3a0-103">PF\_FOLLOWSET structure</span></span>

<span data-ttu-id="aa3a0-104">La **struttura \_ PF** followt definisce i protocolli che possono precedere o seguire un protocollo.</span><span class="sxs-lookup"><span data-stu-id="aa3a0-104">The **PF\_FOLLOWSET** structure defines the protocols that may precede or follow a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa3a0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa3a0-105">Syntax</span></span>


```C++
typedef struct _PF_FOLLOWSET {
  DWORD          nEntries;
  PF_FOLLOWENTRY Entry[];
} PF_FOLLOWSET, *PPF_FOLLOWSET;
```



## <a name="members"></a><span data-ttu-id="aa3a0-106">Members</span><span class="sxs-lookup"><span data-stu-id="aa3a0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="aa3a0-107">**nEntries**</span><span class="sxs-lookup"><span data-stu-id="aa3a0-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="aa3a0-108">Numero di protocolli nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="aa3a0-108">Number of protocols in the list.</span></span>

</dd> <dt>

<span data-ttu-id="aa3a0-109">**Voce**</span><span class="sxs-lookup"><span data-stu-id="aa3a0-109">**Entry**</span></span>
</dt> <dd>

<span data-ttu-id="aa3a0-110">Matrice di strutture [PF \_ FOLLOWENTRY](pf-followentry.md) che descrivono ogni protocollo.</span><span class="sxs-lookup"><span data-stu-id="aa3a0-110">Array of [PF\_FOLLOWENTRY](pf-followentry.md) structures that describe each protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa3a0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa3a0-111">Remarks</span></span>

<span data-ttu-id="aa3a0-112">La struttura [PF \_ PARSERINFO](pf-parserinfo.md) usa la struttura **PF \_ follower** per elencare i protocolli che possono precedere o seguire il protocollo rilevato dal parser.</span><span class="sxs-lookup"><span data-stu-id="aa3a0-112">The [PF\_PARSERINFO](pf-parserinfo.md) structure uses the **PF\_FOLLOWSET** structure to list the protocols that may precede or follow the protocol that the parser detects.</span></span>

<span data-ttu-id="aa3a0-113">Network Monitor usa le informazioni contenute nella **struttura \_ PF** follower per aggiornare i set di parser specifici.</span><span class="sxs-lookup"><span data-stu-id="aa3a0-113">Network Monitor uses the information in the **PF\_FOLLOWSET** structure to update the follow sets of specific parsers.</span></span> <span data-ttu-id="aa3a0-114">La struttura **PF \_ followt** deve essere allocata mediante **HeapAlloc**.</span><span class="sxs-lookup"><span data-stu-id="aa3a0-114">The **PF\_FOLLOWSET** structure must be allocated using **HeapAlloc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa3a0-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa3a0-115">Requirements</span></span>



| <span data-ttu-id="aa3a0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa3a0-116">Requirement</span></span> | <span data-ttu-id="aa3a0-117">Valore</span><span class="sxs-lookup"><span data-stu-id="aa3a0-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aa3a0-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa3a0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="aa3a0-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aa3a0-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="aa3a0-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa3a0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="aa3a0-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aa3a0-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="aa3a0-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa3a0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa3a0-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa3a0-123"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa3a0-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa3a0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa3a0-125">PF \_ FOLLOWENTRY</span><span class="sxs-lookup"><span data-stu-id="aa3a0-125">PF\_FOLLOWENTRY</span></span>](pf-followentry.md)
</dt> <dt>

[<span data-ttu-id="aa3a0-126">PF \_ PARSERINFO</span><span class="sxs-lookup"><span data-stu-id="aa3a0-126">PF\_PARSERINFO</span></span>](pf-parserinfo.md)
</dt> </dl>

 

 





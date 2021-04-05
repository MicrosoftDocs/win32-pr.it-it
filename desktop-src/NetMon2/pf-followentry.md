---
description: La \_ struttura PF FOLLOWENTRY definisce un protocollo che Network Monitor aggiunge al set seguente di un parser.
ms.assetid: 931ae70f-8c5e-4b7a-aae6-64a33dac3b23
title: Struttura PF_FOLLOWENTRY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f93ec4784fc8d0f92f68fdff3914e230ffd3cdce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882906"
---
# <a name="pf_followentry-structure"></a><span data-ttu-id="132dc-103">\_Struttura PF FOLLOWENTRY</span><span class="sxs-lookup"><span data-stu-id="132dc-103">PF\_FOLLOWENTRY structure</span></span>

<span data-ttu-id="132dc-104">La struttura **PF \_ FOLLOWENTRY** definisce un protocollo che Network Monitor aggiunge al set seguente di un parser.</span><span class="sxs-lookup"><span data-stu-id="132dc-104">The **PF\_FOLLOWENTRY** structure defines a protocol that Network Monitor adds to the follow set of a parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="132dc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="132dc-105">Syntax</span></span>


```C++
typedef struct _PF_FOLLOWENTRY {
  char szProtocol[MAX_PROTOCOL_NAME_LEN];
} PF_FOLLOWENTRY, *PPF_FOLLOWENTRY;
```



## <a name="members"></a><span data-ttu-id="132dc-106">Members</span><span class="sxs-lookup"><span data-stu-id="132dc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="132dc-107">**szProtocol**</span><span class="sxs-lookup"><span data-stu-id="132dc-107">**szProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="132dc-108">Nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="132dc-108">The name of the protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="132dc-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="132dc-109">Remarks</span></span>

<span data-ttu-id="132dc-110">La struttura [PF \_ follower](pf-followset.md) usa una matrice di strutture **PF \_ FOLLOWENTRY** .</span><span class="sxs-lookup"><span data-stu-id="132dc-110">The [PF\_FOLLOWSET](pf-followset.md) structure uses an array of **PF\_FOLLOWENTRY** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="132dc-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="132dc-111">Requirements</span></span>



| <span data-ttu-id="132dc-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="132dc-112">Requirement</span></span> | <span data-ttu-id="132dc-113">Valore</span><span class="sxs-lookup"><span data-stu-id="132dc-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="132dc-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="132dc-114">Minimum supported client</span></span><br/> | <span data-ttu-id="132dc-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="132dc-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="132dc-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="132dc-116">Minimum supported server</span></span><br/> | <span data-ttu-id="132dc-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="132dc-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="132dc-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="132dc-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="132dc-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="132dc-119"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="132dc-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="132dc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="132dc-121">PF \_</span><span class="sxs-lookup"><span data-stu-id="132dc-121">PF\_FOLLOWSET</span></span>](pf-followset.md)
</dt> </dl>

 

 





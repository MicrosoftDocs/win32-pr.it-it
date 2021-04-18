---
description: Questo argomento si applica a Windows XP Service Pack 2 o versioni successive. La \_ struttura di connessione KSTOPOLOGY descrive una connessione nodo all'interno di un filtro di streaming kernel (KS). Un nodo può essere connesso a un altro nodo all'interno del filtro o a un pin sul filtro.
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: Struttura KSTOPOLOGY_CONNECTION (KS. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSTOPOLOGY_CONNECTION
api_type:
- HeaderDef
api_location:
- Ks.h
ms.openlocfilehash: f523d378a54311845781c144b33e131d5875e41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330389"
---
# <a name="kstopology_connection-structure"></a><span data-ttu-id="3b873-105">\_Struttura di connessione KSTOPOLOGY</span><span class="sxs-lookup"><span data-stu-id="3b873-105">KSTOPOLOGY\_CONNECTION structure</span></span>

<span data-ttu-id="3b873-106">Questo argomento si applica a Windows XP Service Pack 2 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3b873-106">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="3b873-107">La struttura di **\_ connessione KSTOPOLOGY** descrive una connessione nodo all'interno di un filtro di streaming kernel (KS).</span><span class="sxs-lookup"><span data-stu-id="3b873-107">The **KSTOPOLOGY\_CONNECTION** structure describes a node connection within a kernel-streaming (KS) filter.</span></span> <span data-ttu-id="3b873-108">Un nodo può essere connesso a un altro nodo all'interno del filtro o a un pin sul filtro.</span><span class="sxs-lookup"><span data-stu-id="3b873-108">A node can be connected to another node within the filter, or to a pin on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b873-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b873-109">Syntax</span></span>


```C++
typedef struct {
  ULONG FromNode;
  ULONG FromNodePin;
  ULONG ToNode;
  ULONG ToNodePin;
} KSTOPOLOGY_CONNECTION, *PKSTOPOLOGY_CONNECTION;
```



## <a name="members"></a><span data-ttu-id="3b873-110">Members</span><span class="sxs-lookup"><span data-stu-id="3b873-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="3b873-111">**FromNode**</span><span class="sxs-lookup"><span data-stu-id="3b873-111">**FromNode**</span></span>
</dt> <dd>

<span data-ttu-id="3b873-112">Indice del nodo upstream nella connessione.</span><span class="sxs-lookup"><span data-stu-id="3b873-112">Index of the upstream node in the connection.</span></span> <span data-ttu-id="3b873-113">Se la connessione upstream è un PIN, anziché un nodo, il valore è KSFILTER \_ node.</span><span class="sxs-lookup"><span data-stu-id="3b873-113">If the upstream connection is a pin, rather than a node, the value is KSFILTER\_NODE.</span></span>

</dd> <dt>

<span data-ttu-id="3b873-114">**FromNodePin**</span><span class="sxs-lookup"><span data-stu-id="3b873-114">**FromNodePin**</span></span>
</dt> <dd>

<span data-ttu-id="3b873-115">Se il valore del campo **FromNode** è KSFILTER \_ node, questo campo specifica l'indice del pin upstream.</span><span class="sxs-lookup"><span data-stu-id="3b873-115">If the value of the **FromNode** field is KSFILTER\_NODE, this field specifies the index of the upstream pin.</span></span> <span data-ttu-id="3b873-116">In caso contrario, questo campo viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="3b873-116">Otherwise, this field is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="3b873-117">**ToNode**</span><span class="sxs-lookup"><span data-stu-id="3b873-117">**ToNode**</span></span>
</dt> <dd>

<span data-ttu-id="3b873-118">Indice del nodo downstream nella connessione.</span><span class="sxs-lookup"><span data-stu-id="3b873-118">Index of the downstream node in the connection.</span></span> <span data-ttu-id="3b873-119">Se la connessione downstream è un PIN, anziché un nodo, il valore è KSFILTER \_ node.</span><span class="sxs-lookup"><span data-stu-id="3b873-119">If the downstream connection is a pin, rather than a node, the value is KSFILTER\_NODE.</span></span>

</dd> <dt>

<span data-ttu-id="3b873-120">**ToNodePin**</span><span class="sxs-lookup"><span data-stu-id="3b873-120">**ToNodePin**</span></span>
</dt> <dd>

<span data-ttu-id="3b873-121">Se il valore del campo **ToNode** è KSFILTER \_ , questo campo specifica l'indice del pin downstream.</span><span class="sxs-lookup"><span data-stu-id="3b873-121">If the value of the **ToNode** field is KSFILTER\_NODE, this field specifies the index of the downstream pin.</span></span> <span data-ttu-id="3b873-122">In caso contrario, questo campo viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="3b873-122">Otherwise, this field is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b873-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b873-123">Requirements</span></span>



| <span data-ttu-id="3b873-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b873-124">Requirement</span></span> | <span data-ttu-id="3b873-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3b873-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="3b873-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b873-126">Header</span></span><br/> | <dl> <span data-ttu-id="3b873-127"><dt>KS. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b873-127"><dt>Ks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b873-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b873-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b873-129">Strutture DirectShow</span><span class="sxs-lookup"><span data-stu-id="3b873-129">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="3b873-130">**IKsTopologyInfo:: Get \_ ConnectionInfo**</span><span class="sxs-lookup"><span data-stu-id="3b873-130">**IKsTopologyInfo::get\_ConnectionInfo**</span></span>](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 





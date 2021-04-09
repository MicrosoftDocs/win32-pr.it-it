---
title: Struttura IPX_SPECIFIC_DATA (RTM. h)
description: La \_ struttura di dati specifici di IPX \_ contiene dati specifici di IPX.
ms.assetid: 4d97092d-692c-4dc7-af7f-260dc76c6c08
keywords:
- RAS struttura IPX_SPECIFIC_DATA
- RAS puntatore alla struttura PIPX_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- IPX_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56badfb6149e416c71b447aca93564b5eb5aba7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963729"
---
# <a name="ipx_specific_data-structure"></a><span data-ttu-id="5d7fe-105">\_Struttura di dati specifici di IPX \_</span><span class="sxs-lookup"><span data-stu-id="5d7fe-105">IPX\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="5d7fe-106">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="5d7fe-107">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="5d7fe-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="5d7fe-108">La struttura di **\_ \_ dati specifici di IPX** contiene dati specifici di IPX.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-108">The **IPX\_SPECIFIC\_DATA** structure contains IPX-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d7fe-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d7fe-109">Syntax</span></span>


```C++
typedef struct _IPX_SPECIFIC_DATA {
  DWORD  FSD_Flags;
  USHORT FSD_TickCount;
  USHORT FSD_HopCount;
} IPX_SPECIFIC_DATA, *PIPX_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="5d7fe-110">Members</span><span class="sxs-lookup"><span data-stu-id="5d7fe-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="5d7fe-111">**\_Flag FSD**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-111">**FSD\_Flags**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-112">Specifica i flag che descrivono la route.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-112">Specifies flags that describe the route.</span></span> <span data-ttu-id="5d7fe-113">Attualmente, questo membro è pari a zero o al valore del flag seguente.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-113">Currently, this member is either zero or the following flag value.</span></span>



| <span data-ttu-id="5d7fe-114">Valore</span><span class="sxs-lookup"><span data-stu-id="5d7fe-114">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="5d7fe-115">Significato</span><span class="sxs-lookup"><span data-stu-id="5d7fe-115">Meaning</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="IPX_GLOBAL_CLIENT_WAN_ROUTE"></span><span id="ipx_global_client_wan_route"></span><dl> <span data-ttu-id="5d7fe-116"><dt>**\_ \_ \_ Route WAN client globale \_ IPX**</dt></span><span class="sxs-lookup"><span data-stu-id="5d7fe-116"><dt>**IPX\_GLOBAL\_CLIENT\_WAN\_ROUTE**</dt></span></span> </dl> | <span data-ttu-id="5d7fe-117">Specifica che questa route è destinata alla rete globale allocata per tutti i client WAN.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-117">Specifies that this route is for the global network allocated for all WAN clients.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5d7fe-118">**\_TickCount FSD**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-118">**FSD\_TickCount**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-119">Specifica il numero di cicli necessari per raggiungere la rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-119">Specifies the number of ticks it takes to reach the destination network.</span></span> <span data-ttu-id="5d7fe-120">I protocolli di routing diversi da RIP devono convertire le metriche in cicli.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-120">Routing protocols other than RIP should convert their metrics into ticks.</span></span>

</dd> <dt>

<span data-ttu-id="5d7fe-121">**\_HopCount FSD**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-121">**FSD\_HopCount**</span></span>
</dt> <dd>

<span data-ttu-id="5d7fe-122">Specifica il numero di hop associato alla route.</span><span class="sxs-lookup"><span data-stu-id="5d7fe-122">Specifies the hop count associated with the route.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d7fe-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d7fe-123">Requirements</span></span>



| <span data-ttu-id="5d7fe-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d7fe-124">Requirement</span></span> | <span data-ttu-id="5d7fe-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5d7fe-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5d7fe-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d7fe-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5d7fe-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5d7fe-127">None supported</span></span><br/>                                                        |
| <span data-ttu-id="5d7fe-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d7fe-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5d7fe-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5d7fe-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5d7fe-130">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="5d7fe-130">End of server support</span></span><br/>    | <span data-ttu-id="5d7fe-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5d7fe-131">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="5d7fe-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d7fe-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d7fe-133"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d7fe-133"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d7fe-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d7fe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d7fe-135">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="5d7fe-135">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="5d7fe-136">Strutture di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="5d7fe-136">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="5d7fe-137">**\_Route IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="5d7fe-137">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 






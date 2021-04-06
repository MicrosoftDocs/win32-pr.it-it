---
title: Struttura MPSTATUS_DATA (MpClient. h)
description: Contiene dati sullo stato corrente di un componente del prodotto.
ms.assetid: 6AEF485C-30D1-47DB-92B6-048B8CAA7833
keywords:
- Struttura MPSTATUS_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPSTATUS_DATA
topic_type:
- apiref
api_name:
- MPSTATUS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5da4ea9c8c51d8ee74d3242e5020df23f758228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742303"
---
# <a name="mpstatus_data-structure"></a><span data-ttu-id="dc9bc-105">\_Struttura dei dati MPSTATUS</span><span class="sxs-lookup"><span data-stu-id="dc9bc-105">MPSTATUS\_DATA structure</span></span>

<span data-ttu-id="dc9bc-106">Contiene dati sullo stato corrente di un componente del prodotto.</span><span class="sxs-lookup"><span data-stu-id="dc9bc-106">Contains data about the current status of a component of the product.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc9bc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc9bc-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_DATA {
  MPCOMPONENT_ID ComponentID;
  BOOL           fEnable;
  union {
    PMPSTATUS_DATAEX_UNUSED p1;
    PMPSTATUS_DATAEX_UNUSED p2;
    PMPSTATUS_DATAEX_UNUSED p3;
    PMPSTATUS_DATAEX_UNUSED p4;
    PMPSTATUS_DATAEX_UNUSED p5;
    PMPSTATUS_DATAEX_UNUSED p6;
    PMPSTATUS_DATAEX_UNUSED p7;
    PMPSTATUS_DATAEX_UNUSED p8;
    PMPSTATUS_DATAEX_UNUSED p9;
    PMPSTATUS_DATAEX_UNUSED pa;
    PMPSTATUS_DATAEX_UNUSED pb;
  } ComponentStatus;
} MPSTATUS_DATA, *PMPSTATUS_DATA;
```



## <a name="members"></a><span data-ttu-id="dc9bc-108">Members</span><span class="sxs-lookup"><span data-stu-id="dc9bc-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc9bc-109">**ComponentID**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-109">**ComponentID**</span></span>
</dt> <dd>

<span data-ttu-id="dc9bc-110">Tipo: **[ **MPCOMPONENT \_ ID**](mpcomponent-id.md)**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-110">Type: **[**MPCOMPONENT\_ID**](mpcomponent-id.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc9bc-111">ID componente specifico per il quale viene segnalato lo stato.</span><span class="sxs-lookup"><span data-stu-id="dc9bc-111">Specific component ID for which status is reported.</span></span>

</dd> <dt>

<span data-ttu-id="dc9bc-112">**fEnable**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-112">**fEnable**</span></span>
</dt> <dd>

<span data-ttu-id="dc9bc-113">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-113">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="dc9bc-114">Stato richiesto per il componente.</span><span class="sxs-lookup"><span data-stu-id="dc9bc-114">Status requested for the component.</span></span> <span data-ttu-id="dc9bc-115">**HRESULT** nei dati di callback indica l'esito positivo o negativo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="dc9bc-115">**hResult** in the callback data signifies success or failure for the request.</span></span>

</dd> <dt>

<span data-ttu-id="dc9bc-116">**ComponentStatus**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-116">**ComponentStatus**</span></span>
</dt> <dd>

<span data-ttu-id="dc9bc-117">Dati di stato aggiuntivi a seconda del valore di **ComponentID**.</span><span class="sxs-lookup"><span data-stu-id="dc9bc-117">Extra status data depending on value of **ComponentID**.</span></span>

> [!Note]  
> <span data-ttu-id="dc9bc-118">Attualmente produce un puntatore a una struttura fittizia per tutti i possibili valori di **ComponentID**.</span><span class="sxs-lookup"><span data-stu-id="dc9bc-118">Currently results in a pointer to a dummy structure for all possible values of **ComponentID**.</span></span>

 

<dl> <dt>

<span data-ttu-id="dc9bc-119">**P1**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-119">**p1**</span></span>
</dt> <dd>

<span data-ttu-id="dc9bc-120">Tipo: **PMPSTATUS \_ DATAEX non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-120">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="dc9bc-121">Quando **ComponentID**  ==  **MPCOMPONENT \_ As \_ Signature**.</span><span class="sxs-lookup"><span data-stu-id="dc9bc-121">When **ComponentID** == **MPCOMPONENT\_AS\_SIGNATURE**.</span></span> <span data-ttu-id="dc9bc-122">Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="dc9bc-122">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc9bc-123">**P2**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-123">**p2**</span></span>
</dt> <dd>

<span data-ttu-id="dc9bc-124">Tipo: **PMPSTATUS \_ DATAEX non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-124">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="dc9bc-125">Quando **ComponentID**  ==  **MPCOMPONENT \_ AV \_ Signature**.</span><span class="sxs-lookup"><span data-stu-id="dc9bc-125">When **ComponentID** == **MPCOMPONENT\_AV\_SIGNATURE**.</span></span> <span data-ttu-id="dc9bc-126">Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="dc9bc-126">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc9bc-127">**P3**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-127">**p3**</span></span>
</dt> <dd>

<span data-ttu-id="dc9bc-128">Tipo: **PMPSTATUS \_ DATAEX non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-128">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="dc9bc-129">Quando **ComponentID**  ==  **MPCOMPONENT \_ realtime \_ Monitor**.</span><span class="sxs-lookup"><span data-stu-id="dc9bc-129">When **ComponentID** == **MPCOMPONENT\_REALTIME\_MONITOR**.</span></span> <span data-ttu-id="dc9bc-130">Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="dc9bc-130">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc9bc-131">**P4**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-131">**p4**</span></span>
</dt> <dd>

<span data-ttu-id="dc9bc-132">Tipo: **PMPSTATUS \_ DATAEX non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-132">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="dc9bc-133">Quando **ComponentID**  ==  **MPCOMPONENT \_ onaccess \_ Protection**.</span><span class="sxs-lookup"><span data-stu-id="dc9bc-133">When **ComponentID** == **MPCOMPONENT\_ONACCESS\_PROTECTION**.</span></span> <span data-ttu-id="dc9bc-134">Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="dc9bc-134">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc9bc-135">**P5**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-135">**p5**</span></span>
</dt> <dd>

<span data-ttu-id="dc9bc-136">Tipo: **PMPSTATUS \_ DATAEX non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-136">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="dc9bc-137">Quando **ComponentID**  ==  **MPCOMPONENT \_ IOAV \_ Protection**.</span><span class="sxs-lookup"><span data-stu-id="dc9bc-137">When **ComponentID** == **MPCOMPONENT\_IOAV\_PROTECTION**.</span></span> <span data-ttu-id="dc9bc-138">Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="dc9bc-138">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc9bc-139">**P6**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-139">**p6**</span></span>
</dt> <dd>

<span data-ttu-id="dc9bc-140">Tipo: **PMPSTATUS \_ DATAEX non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-140">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="dc9bc-141">Quando **ComponentID**  ==  **MPCOMPONENT \_ Behavior \_ Monitor**.</span><span class="sxs-lookup"><span data-stu-id="dc9bc-141">When **ComponentID** == **MPCOMPONENT\_BEHAVIOR\_MONITOR**.</span></span> <span data-ttu-id="dc9bc-142">Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="dc9bc-142">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc9bc-143">**P7**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-143">**p7**</span></span>
</dt> <dd>

<span data-ttu-id="dc9bc-144">Tipo: **PMPSTATUS \_ DATAEX non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-144">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="dc9bc-145">Quando **ComponentID**  ==  **MPCOMPONENT \_ auto \_ Scan**.</span><span class="sxs-lookup"><span data-stu-id="dc9bc-145">When **ComponentID** == **MPCOMPONENT\_AUTO\_SCAN**.</span></span> <span data-ttu-id="dc9bc-146">Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="dc9bc-146">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc9bc-147">**P8**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-147">**p8**</span></span>
</dt> <dd>

<span data-ttu-id="dc9bc-148">Tipo: **PMPSTATUS \_ DATAEX non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-148">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="dc9bc-149">Quando **ComponentID**  ==  **MPCOMPONENT \_ auto \_ SIGUPDATE**.</span><span class="sxs-lookup"><span data-stu-id="dc9bc-149">When **ComponentID** == **MPCOMPONENT\_AUTO\_SIGUPDATE**.</span></span> <span data-ttu-id="dc9bc-150">Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="dc9bc-150">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc9bc-151">**P9**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-151">**p9**</span></span>
</dt> <dd>

<span data-ttu-id="dc9bc-152">Tipo: **PMPSTATUS \_ DATAEX non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-152">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="dc9bc-153">Quando **ComponentID**  ==  **MPCOMPONENT \_ IPC**.</span><span class="sxs-lookup"><span data-stu-id="dc9bc-153">When **ComponentID** == **MPCOMPONENT\_IPC**.</span></span> <span data-ttu-id="dc9bc-154">Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="dc9bc-154">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc9bc-155">**pa**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-155">**pa**</span></span>
</dt> <dd>

<span data-ttu-id="dc9bc-156">Tipo: **PMPSTATUS \_ DATAEX non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-156">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="dc9bc-157">Quando **ComponentID**  ==  **MPCOMPONENT \_ NIS**.</span><span class="sxs-lookup"><span data-stu-id="dc9bc-157">When **ComponentID** == **MPCOMPONENT\_NIS**.</span></span> <span data-ttu-id="dc9bc-158">Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="dc9bc-158">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc9bc-159">**PB**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-159">**pb**</span></span>
</dt> <dd>

<span data-ttu-id="dc9bc-160">Tipo: **PMPSTATUS \_ DATAEX non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-160">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="dc9bc-161">Quando **ComponentID**  ==  **MPCOMPONENT \_ Elam**.</span><span class="sxs-lookup"><span data-stu-id="dc9bc-161">When **ComponentID** == **MPCOMPONENT\_ELAM**.</span></span> <span data-ttu-id="dc9bc-162">Vedere [**MPSTATUS \_ DATAEX \_ inutilizzato**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="dc9bc-162">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc9bc-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc9bc-163">Requirements</span></span>



| <span data-ttu-id="dc9bc-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc9bc-164">Requirement</span></span> | <span data-ttu-id="dc9bc-165">Valore</span><span class="sxs-lookup"><span data-stu-id="dc9bc-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9bc-166">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc9bc-166">Minimum supported client</span></span><br/> | <span data-ttu-id="dc9bc-167">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dc9bc-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="dc9bc-168">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc9bc-168">Minimum supported server</span></span><br/> | <span data-ttu-id="dc9bc-169">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dc9bc-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc9bc-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc9bc-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc9bc-171"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc9bc-171"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc9bc-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc9bc-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc9bc-173">**\_ID MPCOMPONENT**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-173">**MPCOMPONENT\_ID**</span></span>](mpcomponent-id.md)
</dt> <dt>

[<span data-ttu-id="dc9bc-174">**MPSTATUS \_ DATAEX non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="dc9bc-174">**MPSTATUS\_DATAEX\_UNUSED**</span></span>](mpstatus-dataex-unused.md)
</dt> </dl>

 

 






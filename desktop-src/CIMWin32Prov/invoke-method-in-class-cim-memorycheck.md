---
description: Il metodo Invoke della classe CIM \_ MemoryCheck valuta un particolare controllo. I dettagli relativi al modo in cui il metodo valuta un particolare controllo in un contesto CIM sono descritti dalle sottoclassi di controllo CIM non astratte \_ . Questo metodo viene ereditato dal \_ controllo CIM.
ms.assetid: 264a7690-b066-4024-8cb1-d988b829dc72
ms.tgt_platform: multiple
title: Metodo Invoke della classe CIM_MemoryCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d8788b8e910e0a5b7debd9990c18dfb4edef140e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126468"
---
# <a name="invoke-method-of-the-cim_memorycheck-class"></a><span data-ttu-id="b9fc6-105">Metodo Invoke della classe CIM \_ MemoryCheck</span><span class="sxs-lookup"><span data-stu-id="b9fc6-105">Invoke method of the CIM\_MemoryCheck class</span></span>

<span data-ttu-id="b9fc6-106">Il metodo **Invoke** della classe [**CIM \_ MemoryCheck**](cim-memorycheck.md) valuta un particolare controllo.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-106">The **Invoke** method of the [**CIM\_MemoryCheck**](cim-memorycheck.md) class evaluates a particular check.</span></span> <span data-ttu-id="b9fc6-107">I dettagli relativi al modo in cui il metodo valuta un particolare controllo in un contesto CIM sono descritti dalle sottoclassi di [**\_ controllo CIM**](cim-check.md) non astratte.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-107">Details of how the method evaluates a particular check in a CIM context is described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="b9fc6-108">Questo metodo viene ereditato dal **\_ controllo CIM**.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-108">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b9fc6-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b9fc6-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b9fc6-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b9fc6-111">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b9fc6-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b9fc6-112">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b9fc6-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9fc6-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9fc6-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="b9fc6-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9fc6-114">Parameters</span></span>

<span data-ttu-id="b9fc6-115">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9fc6-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9fc6-116">Return value</span></span>

<span data-ttu-id="b9fc6-117">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9fc6-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9fc6-118">Remarks</span></span>

<span data-ttu-id="b9fc6-119">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="b9fc6-120">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="b9fc6-121">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b9fc6-122">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="b9fc6-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9fc6-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9fc6-123">Requirements</span></span>



| <span data-ttu-id="b9fc6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9fc6-124">Requirement</span></span> | <span data-ttu-id="b9fc6-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b9fc6-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9fc6-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9fc6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b9fc6-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9fc6-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b9fc6-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9fc6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b9fc6-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9fc6-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b9fc6-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b9fc6-130">Namespace</span></span><br/>                | <span data-ttu-id="b9fc6-131">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b9fc6-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b9fc6-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b9fc6-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9fc6-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9fc6-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9fc6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b9fc6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9fc6-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9fc6-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9fc6-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9fc6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9fc6-137">\_MEMORYCHECK CIM</span><span class="sxs-lookup"><span data-stu-id="b9fc6-137">CIM\_MemoryCheck</span></span>](invoke-method-in-class-cim-memorycheck.md)
</dt> <dt>

[<span data-ttu-id="b9fc6-138">**\_MEMORYCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="b9fc6-138">**CIM\_MemoryCheck**</span></span>](cim-memorycheck.md)
</dt> </dl>

 


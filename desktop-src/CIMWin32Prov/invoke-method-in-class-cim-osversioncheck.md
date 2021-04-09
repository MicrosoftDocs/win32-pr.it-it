---
description: Il metodo Invoke della classe CIM \_ OSVersionCheck valuta un particolare controllo. I dettagli relativi al modo in cui il metodo valuta un particolare controllo in un contesto CIM sono descritti dalle sottoclassi di controllo CIM non astratte \_ . Questo metodo viene ereditato dal \_ controllo CIM.
ms.assetid: ff06772c-e40c-49c8-b334-5ee480926245
ms.tgt_platform: multiple
title: Metodo Invoke della classe CIM_OSVersionCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSVersionCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 49d6944c4a28c956356fef430e47bc8636082930
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126465"
---
# <a name="invoke-method-of-the-cim_osversioncheck-class"></a><span data-ttu-id="20cd8-105">Metodo Invoke della classe CIM \_ OSVersionCheck</span><span class="sxs-lookup"><span data-stu-id="20cd8-105">Invoke method of the CIM\_OSVersionCheck class</span></span>

<span data-ttu-id="20cd8-106">Il metodo **Invoke** della classe [**CIM \_ OSVersionCheck**](cim-osversioncheck.md) valuta un particolare controllo.</span><span class="sxs-lookup"><span data-stu-id="20cd8-106">The **Invoke** method of the [**CIM\_OSVersionCheck**](cim-osversioncheck.md) class evaluates a particular check.</span></span> <span data-ttu-id="20cd8-107">I dettagli relativi al modo in cui il metodo valuta un particolare controllo in un contesto CIM sono descritti dalle sottoclassi [**di \_ controllo CIM**](cim-check.md) non astratte.</span><span class="sxs-lookup"><span data-stu-id="20cd8-107">The details of how the method evaluates a particular check in a CIM context is described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="20cd8-108">Questo metodo viene ereditato dal **\_ controllo CIM**.</span><span class="sxs-lookup"><span data-stu-id="20cd8-108">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="20cd8-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="20cd8-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="20cd8-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="20cd8-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="20cd8-111">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="20cd8-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="20cd8-112">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="20cd8-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="20cd8-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20cd8-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="20cd8-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="20cd8-114">Parameters</span></span>

<span data-ttu-id="20cd8-115">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="20cd8-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="20cd8-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20cd8-116">Return value</span></span>

<span data-ttu-id="20cd8-117">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="20cd8-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="20cd8-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="20cd8-118">Remarks</span></span>

<span data-ttu-id="20cd8-119">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="20cd8-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="20cd8-120">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="20cd8-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="20cd8-121">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="20cd8-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="20cd8-122">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="20cd8-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="20cd8-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20cd8-123">Requirements</span></span>



| <span data-ttu-id="20cd8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="20cd8-124">Requirement</span></span> | <span data-ttu-id="20cd8-125">Valore</span><span class="sxs-lookup"><span data-stu-id="20cd8-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20cd8-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20cd8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="20cd8-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20cd8-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="20cd8-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20cd8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="20cd8-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20cd8-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="20cd8-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="20cd8-130">Namespace</span></span><br/>                | <span data-ttu-id="20cd8-131">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="20cd8-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="20cd8-132">MOF</span><span class="sxs-lookup"><span data-stu-id="20cd8-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20cd8-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20cd8-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="20cd8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="20cd8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20cd8-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20cd8-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20cd8-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20cd8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20cd8-137">\_OSVERSIONCHECK CIM</span><span class="sxs-lookup"><span data-stu-id="20cd8-137">CIM\_OSVersionCheck</span></span>](invoke-method-in-class-cim-osversioncheck.md)
</dt> <dt>

[<span data-ttu-id="20cd8-138">**\_OSVERSIONCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="20cd8-138">**CIM\_OSVersionCheck**</span></span>](cim-osversioncheck.md)
</dt> </dl>

 


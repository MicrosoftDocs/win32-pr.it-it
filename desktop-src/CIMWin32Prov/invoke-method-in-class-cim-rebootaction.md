---
description: Il metodo Invoke della classe CIM \_ rebootaction esegue una determinata azione. I dettagli del modo in cui il metodo esegue l'azione sono specifici dell'implementazione. Questo metodo viene ereditato dall' \_ azione CIM.
ms.assetid: 27b6571e-94fe-423e-89ab-5ba2bc632882
ms.tgt_platform: multiple
title: Metodo Invoke della classe CIM_RebootAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RebootAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e68849a486cc6a5b61dc55cf86e259e2f58435e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304671"
---
# <a name="invoke-method-of-the-cim_rebootaction-class"></a><span data-ttu-id="7fe9e-105">Metodo Invoke della classe CIM \_ rebootaction</span><span class="sxs-lookup"><span data-stu-id="7fe9e-105">Invoke method of the CIM\_RebootAction class</span></span>

<span data-ttu-id="7fe9e-106">Il metodo **Invoke** della classe [**CIM \_ rebootaction**](cim-rebootaction.md) esegue una determinata azione.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-106">The **Invoke** method of the [**CIM\_RebootAction**](cim-rebootaction.md) class takes a particular action.</span></span> <span data-ttu-id="7fe9e-107">I dettagli del modo in cui il metodo esegue l'azione sono specifici dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-107">The details of how the method performs the action are implementation specific.</span></span> <span data-ttu-id="7fe9e-108">Questo metodo viene ereditato dall' [**\_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="7fe9e-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7fe9e-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7fe9e-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7fe9e-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7fe9e-111">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="7fe9e-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7fe9e-112">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7fe9e-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7fe9e-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7fe9e-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="7fe9e-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="7fe9e-114">Parameters</span></span>

<span data-ttu-id="7fe9e-115">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7fe9e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7fe9e-116">Return value</span></span>

<span data-ttu-id="7fe9e-117">Restituisce un valore intero pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-117">Returns an integer value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fe9e-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="7fe9e-118">Remarks</span></span>

<span data-ttu-id="7fe9e-119">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="7fe9e-120">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="7fe9e-121">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7fe9e-122">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="7fe9e-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fe9e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7fe9e-123">Requirements</span></span>



| <span data-ttu-id="7fe9e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fe9e-124">Requirement</span></span> | <span data-ttu-id="7fe9e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="7fe9e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe9e-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fe9e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7fe9e-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7fe9e-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7fe9e-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fe9e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7fe9e-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fe9e-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7fe9e-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7fe9e-130">Namespace</span></span><br/>                | <span data-ttu-id="7fe9e-131">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="7fe9e-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7fe9e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="7fe9e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fe9e-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fe9e-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fe9e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7fe9e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fe9e-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fe9e-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fe9e-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7fe9e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fe9e-137">\_REBOOTACTION CIM</span><span class="sxs-lookup"><span data-stu-id="7fe9e-137">CIM\_RebootAction</span></span>](invoke-method-in-class-cim-rebootaction.md)
</dt> <dt>

[<span data-ttu-id="7fe9e-138">**\_REBOOTACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="7fe9e-138">**CIM\_RebootAction**</span></span>](cim-rebootaction.md)
</dt> </dl>

 


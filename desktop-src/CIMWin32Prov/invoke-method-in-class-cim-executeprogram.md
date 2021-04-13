---
description: Il metodo Invoke della classe CIM \_ ExecuteProgram esegue una determinata azione. I dettagli del modo in cui il metodo esegue l'azione sono specifici dell'implementazione. Questo metodo viene ereditato dall' \_ azione CIM.
ms.assetid: 14a12fae-14a6-412a-a778-8dd34a5843d1
ms.tgt_platform: multiple
title: Metodo Invoke della classe CIM_ExecuteProgram
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExecuteProgram.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bdf9a4edb78bb47c0354991d161339099e4dc49f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401416"
---
# <a name="invoke-method-of-the-cim_executeprogram-class"></a><span data-ttu-id="4e5f5-105">Metodo Invoke della classe CIM \_ ExecuteProgram</span><span class="sxs-lookup"><span data-stu-id="4e5f5-105">Invoke method of the CIM\_ExecuteProgram class</span></span>

<span data-ttu-id="4e5f5-106">Il metodo **Invoke** della classe [**CIM \_ ExecuteProgram**](cim-executeprogram.md) esegue una determinata azione.</span><span class="sxs-lookup"><span data-stu-id="4e5f5-106">The **Invoke** method of the [**CIM\_ExecuteProgram**](cim-executeprogram.md) class takes a particular action.</span></span> <span data-ttu-id="4e5f5-107">I dettagli del modo in cui il metodo esegue l'azione sono specifici dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="4e5f5-107">The details of how the method performs the action are implementation specific.</span></span> <span data-ttu-id="4e5f5-108">Questo metodo viene ereditato dall' [**\_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="4e5f5-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e5f5-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="4e5f5-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4e5f5-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4e5f5-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4e5f5-111">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4e5f5-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4e5f5-112">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4e5f5-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4e5f5-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e5f5-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="4e5f5-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e5f5-114">Parameters</span></span>

<span data-ttu-id="4e5f5-115">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4e5f5-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e5f5-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e5f5-116">Return value</span></span>

<span data-ttu-id="4e5f5-117">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="4e5f5-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e5f5-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e5f5-118">Remarks</span></span>

<span data-ttu-id="4e5f5-119">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="4e5f5-119">WMI does not implement this class.</span></span>

<span data-ttu-id="4e5f5-120">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="4e5f5-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4e5f5-121">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="4e5f5-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e5f5-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e5f5-122">Requirements</span></span>



| <span data-ttu-id="4e5f5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e5f5-123">Requirement</span></span> | <span data-ttu-id="4e5f5-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4e5f5-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e5f5-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e5f5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4e5f5-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e5f5-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e5f5-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e5f5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4e5f5-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e5f5-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e5f5-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4e5f5-129">Namespace</span></span><br/>                | <span data-ttu-id="4e5f5-130">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4e5f5-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e5f5-131">MOF</span><span class="sxs-lookup"><span data-stu-id="4e5f5-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e5f5-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e5f5-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e5f5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4e5f5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e5f5-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e5f5-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e5f5-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e5f5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e5f5-136">\_EXECUTEPROGRAM CIM</span><span class="sxs-lookup"><span data-stu-id="4e5f5-136">CIM\_ExecuteProgram</span></span>](invoke-method-in-class-cim-executeprogram.md)
</dt> <dt>

[<span data-ttu-id="4e5f5-137">**\_EXECUTEPROGRAM CIM**</span><span class="sxs-lookup"><span data-stu-id="4e5f5-137">**CIM\_ExecuteProgram**</span></span>](cim-executeprogram.md)
</dt> </dl>

 


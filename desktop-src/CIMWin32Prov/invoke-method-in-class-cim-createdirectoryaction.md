---
description: Il metodo Invoke della classe CIM \_ CreateDirectoryAction esegue una determinata azione. Informazioni dettagliate sul modo in cui il metodo esegue l'azione sono specifiche dell'implementazione. Questo metodo viene ereditato dall' \_ azione CIM.
ms.assetid: f14e215d-31f2-46c5-b45e-3de64ce46bf2
ms.tgt_platform: multiple
title: Metodo Invoke della classe CIM_CreateDirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CreateDirectoryAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 690a29ae0ea85e0b965d2a426703eea87aee9184
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748114"
---
# <a name="invoke-method-of-the-cim_createdirectoryaction-class"></a><span data-ttu-id="7b23a-105">Metodo Invoke della classe CIM \_ CreateDirectoryAction</span><span class="sxs-lookup"><span data-stu-id="7b23a-105">Invoke method of the CIM\_CreateDirectoryAction class</span></span>

<span data-ttu-id="7b23a-106">Il metodo **Invoke** della classe [**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) esegue una determinata azione.</span><span class="sxs-lookup"><span data-stu-id="7b23a-106">The **Invoke** method of the [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class takes a particular action.</span></span> <span data-ttu-id="7b23a-107">Informazioni dettagliate sul modo in cui il metodo esegue l'azione sono specifiche dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="7b23a-107">Details about how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="7b23a-108">Questo metodo viene ereditato dall' [**\_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="7b23a-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7b23a-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="7b23a-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7b23a-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7b23a-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7b23a-111">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="7b23a-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7b23a-112">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7b23a-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7b23a-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b23a-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="7b23a-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b23a-114">Parameters</span></span>

<span data-ttu-id="7b23a-115">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7b23a-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b23a-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b23a-116">Return value</span></span>

<span data-ttu-id="7b23a-117">Restituisce un valore pari a 0 in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="7b23a-117">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b23a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b23a-118">Remarks</span></span>

<span data-ttu-id="7b23a-119">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="7b23a-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="7b23a-120">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="7b23a-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="7b23a-121">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="7b23a-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7b23a-122">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="7b23a-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b23a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b23a-123">Requirements</span></span>



| <span data-ttu-id="7b23a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b23a-124">Requirement</span></span> | <span data-ttu-id="7b23a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="7b23a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b23a-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b23a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7b23a-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b23a-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7b23a-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b23a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7b23a-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b23a-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7b23a-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7b23a-130">Namespace</span></span><br/>                | <span data-ttu-id="7b23a-131">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="7b23a-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7b23a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="7b23a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b23a-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b23a-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b23a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7b23a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b23a-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b23a-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b23a-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b23a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b23a-137">**\_CREATEDIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="7b23a-137">**CIM\_CreateDirectoryAction**</span></span>](invoke-method-in-class-cim-createdirectoryaction.md)
</dt> <dt>

[<span data-ttu-id="7b23a-138">**\_CREATEDIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="7b23a-138">**CIM\_CreateDirectoryAction**</span></span>](cim-createdirectoryaction.md)
</dt> </dl>

 


---
description: Il metodo Invoke della classe CIM \_ DirectoryAction esegue una determinata azione. I dettagli relativi all'esecuzione dell'azione da parte del metodo sono specifici dell'implementazione. Questo metodo viene ereditato dall' \_ azione CIM.
ms.assetid: e919dfdb-a52d-4bcb-abff-e1273c406226
ms.tgt_platform: multiple
title: Metodo Invoke della classe CIM_DirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f30184fe46cd8e8b9a595545ccba9a7d738af18e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877578"
---
# <a name="invoke-method-of-the-cim_directoryaction-class"></a><span data-ttu-id="f8cd9-105">Metodo Invoke della classe CIM \_ DirectoryAction</span><span class="sxs-lookup"><span data-stu-id="f8cd9-105">Invoke method of the CIM\_DirectoryAction class</span></span>

<span data-ttu-id="f8cd9-106">Il metodo **Invoke** della classe [**CIM \_ DirectoryAction**](cim-directoryaction.md) esegue una determinata azione.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-106">The **Invoke** method of the [**CIM\_DirectoryAction**](cim-directoryaction.md) class takes a particular action.</span></span> <span data-ttu-id="f8cd9-107">I dettagli relativi all'esecuzione dell'azione da parte del metodo sono specifici dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-107">Details of how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="f8cd9-108">Questo metodo viene ereditato dall' [**\_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="f8cd9-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f8cd9-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f8cd9-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f8cd9-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f8cd9-111">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f8cd9-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f8cd9-112">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f8cd9-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f8cd9-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8cd9-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="f8cd9-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8cd9-114">Parameters</span></span>

<span data-ttu-id="f8cd9-115">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8cd9-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8cd9-116">Return value</span></span>

<span data-ttu-id="f8cd9-117">Restituisce un valore pari a 0 (zero) in caso di esito positivo, 1 (uno) se il metodo non è supportato e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-117">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8cd9-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8cd9-118">Remarks</span></span>

<span data-ttu-id="f8cd9-119">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-119">WMI does not implement this class.</span></span>

<span data-ttu-id="f8cd9-120">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f8cd9-121">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="f8cd9-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8cd9-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8cd9-122">Requirements</span></span>



| <span data-ttu-id="f8cd9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8cd9-123">Requirement</span></span> | <span data-ttu-id="f8cd9-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f8cd9-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8cd9-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8cd9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f8cd9-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8cd9-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f8cd9-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8cd9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f8cd9-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8cd9-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8cd9-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f8cd9-129">Namespace</span></span><br/>                | <span data-ttu-id="f8cd9-130">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f8cd9-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f8cd9-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f8cd9-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8cd9-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8cd9-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8cd9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f8cd9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8cd9-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8cd9-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8cd9-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8cd9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8cd9-136">\_DIRECTORYACTION CIM</span><span class="sxs-lookup"><span data-stu-id="f8cd9-136">CIM\_DirectoryAction</span></span>](invoke-method-in-class-cim-directoryaction.md)
</dt> <dt>

[<span data-ttu-id="f8cd9-137">**\_DIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="f8cd9-137">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> </dl>

 


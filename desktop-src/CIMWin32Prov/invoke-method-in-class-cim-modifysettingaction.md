---
description: Il metodo Invoke della classe CIM \_ ModifySettingAction esegue una determinata azione. I dettagli relativi all'esecuzione dell'azione da parte del metodo sono specifici dell'implementazione. Questo metodo viene ereditato dall' \_ azione CIM.
ms.assetid: 360e3e00-1c09-495a-8fc0-ce2e9d1f9e77
ms.tgt_platform: multiple
title: Metodo Invoke della classe CIM_ModifySettingAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ModifySettingAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f4e4c5dc08f4e9ad27d7f4578ca5c82543253b57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304672"
---
# <a name="invoke-method-of-the-cim_modifysettingaction-class"></a><span data-ttu-id="b2649-105">Metodo Invoke della classe CIM \_ ModifySettingAction</span><span class="sxs-lookup"><span data-stu-id="b2649-105">Invoke method of the CIM\_ModifySettingAction class</span></span>

<span data-ttu-id="b2649-106">Il metodo **Invoke** della classe [**CIM \_ ModifySettingAction**](cim-modifysettingaction.md) esegue una determinata azione.</span><span class="sxs-lookup"><span data-stu-id="b2649-106">The **Invoke** method of the [**CIM\_ModifySettingAction**](cim-modifysettingaction.md) class takes a particular action.</span></span> <span data-ttu-id="b2649-107">I dettagli relativi all'esecuzione dell'azione da parte del metodo sono specifici dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="b2649-107">Details of how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="b2649-108">Questo metodo viene ereditato dall' [**\_ azione CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="b2649-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2649-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="b2649-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b2649-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b2649-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b2649-111">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b2649-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b2649-112">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b2649-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2649-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2649-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="b2649-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2649-114">Parameters</span></span>

<span data-ttu-id="b2649-115">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b2649-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b2649-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2649-116">Return value</span></span>

<span data-ttu-id="b2649-117">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="b2649-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2649-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2649-118">Remarks</span></span>

<span data-ttu-id="b2649-119">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="b2649-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="b2649-120">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="b2649-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="b2649-121">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="b2649-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b2649-122">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="b2649-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2649-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2649-123">Requirements</span></span>



| <span data-ttu-id="b2649-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2649-124">Requirement</span></span> | <span data-ttu-id="b2649-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b2649-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2649-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2649-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b2649-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2649-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b2649-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2649-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b2649-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2649-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b2649-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b2649-130">Namespace</span></span><br/>                | <span data-ttu-id="b2649-131">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b2649-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b2649-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b2649-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2649-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2649-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2649-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b2649-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2649-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2649-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2649-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2649-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2649-137">\_MODIFYSETTINGACTION CIM</span><span class="sxs-lookup"><span data-stu-id="b2649-137">CIM\_ModifySettingAction</span></span>](invoke-method-in-class-cim-modifysettingaction.md)
</dt> <dt>

[<span data-ttu-id="b2649-138">**\_MODIFYSETTINGACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="b2649-138">**CIM\_ModifySettingAction**</span></span>](cim-modifysettingaction.md)
</dt> </dl>

 


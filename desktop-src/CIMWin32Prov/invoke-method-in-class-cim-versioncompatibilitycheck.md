---
description: Il metodo Invoke della classe CIM \_ VersionCompatibilityCheck valuta un particolare controllo.
ms.assetid: d1ccc248-340e-4277-9696-063e1e2bf915
ms.tgt_platform: multiple
title: Metodo Invoke della classe CIM_VersionCompatibilityCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VersionCompatibilityCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bccbb6072ae84a238b60247daf6b81cfaa74e608
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877573"
---
# <a name="invoke-method-of-the-cim_versioncompatibilitycheck-class"></a><span data-ttu-id="fbc3d-103">Metodo Invoke della classe CIM \_ VersionCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="fbc3d-103">Invoke method of the CIM\_VersionCompatibilityCheck class</span></span>

<span data-ttu-id="fbc3d-104">Il metodo **Invoke** della classe [**CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) valuta un particolare controllo.</span><span class="sxs-lookup"><span data-stu-id="fbc3d-104">The **Invoke** method of the [**CIM\_VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) class evaluates a particular check.</span></span> <span data-ttu-id="fbc3d-105">I dettagli relativi al modo in cui il metodo valuta un particolare controllo in un contesto CIM sono descritti dalle sottoclassi [**di \_ controllo CIM**](cim-check.md) non astratte.</span><span class="sxs-lookup"><span data-stu-id="fbc3d-105">The details of how the method evaluates a particular check in a CIM context are described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="fbc3d-106">Questo metodo viene ereditato dal **\_ controllo CIM**.</span><span class="sxs-lookup"><span data-stu-id="fbc3d-106">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fbc3d-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="fbc3d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fbc3d-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fbc3d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fbc3d-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="fbc3d-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fbc3d-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fbc3d-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fbc3d-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fbc3d-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="fbc3d-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="fbc3d-112">Parameters</span></span>

<span data-ttu-id="fbc3d-113">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="fbc3d-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fbc3d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fbc3d-114">Return value</span></span>

<span data-ttu-id="fbc3d-115">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="fbc3d-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbc3d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="fbc3d-116">Remarks</span></span>

<span data-ttu-id="fbc3d-117">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="fbc3d-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="fbc3d-118">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="fbc3d-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="fbc3d-119">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="fbc3d-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fbc3d-120">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="fbc3d-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbc3d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbc3d-121">Requirements</span></span>



| <span data-ttu-id="fbc3d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbc3d-122">Requirement</span></span> | <span data-ttu-id="fbc3d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="fbc3d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbc3d-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fbc3d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fbc3d-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fbc3d-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fbc3d-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fbc3d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fbc3d-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbc3d-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fbc3d-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fbc3d-128">Namespace</span></span><br/>                | <span data-ttu-id="fbc3d-129">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="fbc3d-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fbc3d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="fbc3d-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbc3d-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbc3d-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbc3d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fbc3d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbc3d-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbc3d-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbc3d-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fbc3d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbc3d-135">\_VERSIONCOMPATIBILITYCHECK CIM</span><span class="sxs-lookup"><span data-stu-id="fbc3d-135">CIM\_VersionCompatibilityCheck</span></span>](invoke-method-in-class-cim-versioncompatibilitycheck.md)
</dt> <dt>

[<span data-ttu-id="fbc3d-136">**\_VERSIONCOMPATIBILITYCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="fbc3d-136">**CIM\_VersionCompatibilityCheck**</span></span>](cim-versioncompatibilitycheck.md)
</dt> </dl>

 


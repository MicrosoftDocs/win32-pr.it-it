---
description: Il metodo Reset della classe CIM \_ PhysicalExtent richiede la reimpostazione del dispositivo logico.
ms.assetid: ee96cdc8-f695-430c-9d51-94c12f8fe1d4
ms.tgt_platform: multiple
title: Reimposta il metodo della classe CIM_PhysicalExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalExtent.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4859305e09fb50c048f420141f3a2c56caace21e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126859"
---
# <a name="reset-method-of-the-cim_physicalextent-class"></a><span data-ttu-id="0df21-103">Metodo Reset della classe CIM \_ PhysicalExtent</span><span class="sxs-lookup"><span data-stu-id="0df21-103">Reset method of the CIM\_PhysicalExtent class</span></span>

<span data-ttu-id="0df21-104">Il metodo **Reset** della classe CIM \_ PhysicalExtent richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="0df21-104">The **Reset** method of the CIM\_PhysicalExtent class requests a reset of the logical device.</span></span> <span data-ttu-id="0df21-105">Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="0df21-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0df21-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="0df21-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0df21-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0df21-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0df21-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0df21-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="0df21-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0df21-109">Parameters</span></span>

<span data-ttu-id="0df21-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0df21-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0df21-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0df21-111">Return value</span></span>

<span data-ttu-id="0df21-112">Restituisce 0 (zero) se la richiesta è stata eseguita correttamente, 1 (uno) se la richiesta non è supportata e un altro valore se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="0df21-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="0df21-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0df21-113">Remarks</span></span>

<span data-ttu-id="0df21-114">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="0df21-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0df21-115">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="0df21-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0df21-116">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="0df21-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0df21-117">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="0df21-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0df21-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0df21-118">Requirements</span></span>



| <span data-ttu-id="0df21-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0df21-119">Requirement</span></span> | <span data-ttu-id="0df21-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0df21-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0df21-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0df21-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0df21-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0df21-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0df21-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0df21-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0df21-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0df21-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0df21-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0df21-125">Namespace</span></span><br/>                | <span data-ttu-id="0df21-126">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0df21-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0df21-127">MOF</span><span class="sxs-lookup"><span data-stu-id="0df21-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0df21-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0df21-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0df21-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0df21-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0df21-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0df21-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0df21-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0df21-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0df21-132">\_PHYSICALEXTENT CIM</span><span class="sxs-lookup"><span data-stu-id="0df21-132">CIM\_PhysicalExtent</span></span>](reset-method-in-class-cim-physicalextent.md)
</dt> <dt>

[<span data-ttu-id="0df21-133">**\_PHYSICALEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="0df21-133">**CIM\_PhysicalExtent**</span></span>](cim-physicalextent.md)
</dt> </dl>

 

 





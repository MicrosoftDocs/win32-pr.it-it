---
description: Il metodo Reboot richiede il riavvio del sistema operativo.
ms.assetid: 2ce766dd-51a4-4ffb-a45a-40399f1110f6
ms.tgt_platform: multiple
title: Metodo reboot della classe CIM_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e498dd16372503b23aa56471224faf4d5d0ff012
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304439"
---
# <a name="reboot-method-of-the-cim_operatingsystem-class"></a><span data-ttu-id="94d88-103">Metodo reboot della \_ classe CIM OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="94d88-103">Reboot method of the CIM\_OperatingSystem class</span></span>

<span data-ttu-id="94d88-104">Il metodo **reboot** richiede il riavvio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="94d88-104">The **Reboot** method requests a reboot of the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94d88-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="94d88-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="94d88-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="94d88-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="94d88-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="94d88-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="94d88-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="94d88-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="94d88-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94d88-109">Syntax</span></span>


```mof
uint32 Reboot();
```



## <a name="parameters"></a><span data-ttu-id="94d88-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="94d88-110">Parameters</span></span>

<span data-ttu-id="94d88-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="94d88-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="94d88-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="94d88-112">Return value</span></span>

<span data-ttu-id="94d88-113">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="94d88-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="94d88-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="94d88-114">Remarks</span></span>

<span data-ttu-id="94d88-115">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="94d88-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="94d88-116">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="94d88-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="94d88-117">Per le classi WMI derivate da [**CIM \_ OperatingSystem**](cim-operatingsystem.md), vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="94d88-117">For WMI classes that are derived from [**CIM\_OperatingSystem**](cim-operatingsystem.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="94d88-118">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="94d88-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="94d88-119">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="94d88-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="94d88-120">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="94d88-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="94d88-121">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="94d88-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="94d88-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94d88-122">Requirements</span></span>



| <span data-ttu-id="94d88-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="94d88-123">Requirement</span></span> | <span data-ttu-id="94d88-124">Valore</span><span class="sxs-lookup"><span data-stu-id="94d88-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94d88-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94d88-125">Minimum supported client</span></span><br/> | <span data-ttu-id="94d88-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94d88-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94d88-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94d88-127">Minimum supported server</span></span><br/> | <span data-ttu-id="94d88-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94d88-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94d88-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="94d88-129">Namespace</span></span><br/>                | <span data-ttu-id="94d88-130">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="94d88-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="94d88-131">MOF</span><span class="sxs-lookup"><span data-stu-id="94d88-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94d88-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94d88-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="94d88-133">DLL</span><span class="sxs-lookup"><span data-stu-id="94d88-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94d88-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94d88-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94d88-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94d88-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94d88-136">\_OPERATINGSYSTEM CIM</span><span class="sxs-lookup"><span data-stu-id="94d88-136">CIM\_OperatingSystem</span></span>](reboot-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="94d88-137">**\_OPERATINGSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="94d88-137">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> </dl>

 


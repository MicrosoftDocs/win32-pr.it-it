---
description: Il metodo Shutdown richiede un arresto del sistema operativo.
ms.assetid: f2a2a98b-2f4f-4aa1-9f54-515660273c8d
ms.tgt_platform: multiple
title: Metodo Shutdown della classe CIM_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78a11f325b8682b0024ff281a48989b837d3073a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877281"
---
# <a name="shutdown-method-of-the-cim_operatingsystem-class"></a><span data-ttu-id="a7404-103">Metodo Shutdown della classe CIM \_ OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a7404-103">Shutdown method of the CIM\_OperatingSystem class</span></span>

<span data-ttu-id="a7404-104">Il metodo **Shutdown** richiede un arresto del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a7404-104">The **Shutdown** method requests a shutdown of the operating system.</span></span> <span data-ttu-id="a7404-105">L'implementazione o la sottoclasse del sistema operativo può stabilire dipendenze tra i metodi di **arresto** e [**riavvio**](reboot-method-in-class-cim-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="a7404-105">The implementation or subclass of the operating system can establish dependencies between the **Shutdown** and [**Reboot**](reboot-method-in-class-cim-operatingsystem.md) methods.</span></span> <span data-ttu-id="a7404-106">È ad esempio possibile fornire funzionalità più sofisticate, ad esempio un arresto e un riavvio pianificati.</span><span class="sxs-lookup"><span data-stu-id="a7404-106">For example, more sophisticated capabilities can be provided, such as a scheduled shutdown and reboot.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7404-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a7404-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a7404-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a7404-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a7404-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="a7404-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a7404-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a7404-110">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7404-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7404-111">Syntax</span></span>


```mof
uint32 Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="a7404-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7404-112">Parameters</span></span>

<span data-ttu-id="a7404-113">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a7404-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7404-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7404-114">Return value</span></span>

<span data-ttu-id="a7404-115">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="a7404-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7404-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7404-116">Remarks</span></span>

<span data-ttu-id="a7404-117">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="a7404-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a7404-118">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="a7404-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a7404-119">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a7404-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a7404-120">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a7404-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7404-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7404-121">Requirements</span></span>



| <span data-ttu-id="a7404-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7404-122">Requirement</span></span> | <span data-ttu-id="a7404-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a7404-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7404-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7404-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a7404-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7404-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a7404-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7404-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a7404-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7404-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a7404-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a7404-128">Namespace</span></span><br/>                | <span data-ttu-id="a7404-129">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a7404-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a7404-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a7404-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7404-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7404-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7404-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a7404-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7404-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7404-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7404-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7404-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7404-135">\_OPERATINGSYSTEM CIM</span><span class="sxs-lookup"><span data-stu-id="a7404-135">CIM\_OperatingSystem</span></span>](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="a7404-136">**\_OPERATINGSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="a7404-136">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> </dl>

 


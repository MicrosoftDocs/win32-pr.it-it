---
description: Arresta il servizio rappresentato dall'oggetto derivato dal servizio CIM \_ .
ms.assetid: f9eedde7-8d71-40a2-b1e9-7ba97e634f64
ms.tgt_platform: multiple
title: Metodo StopService della classe CIM_Service (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 14a7d378b514a93906c3be4f711bd6ab5b88bf17
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126849"
---
# <a name="stopservice-method-of-the-cim_service-class-sdoiash"></a><span data-ttu-id="e022a-103">Metodo StopService della classe CIM_Service (Sdoias. h)</span><span class="sxs-lookup"><span data-stu-id="e022a-103">StopService method of the CIM_Service class (Sdoias.h)</span></span>

<span data-ttu-id="e022a-104">Il metodo **StopService** arresta il servizio rappresentato dall'oggetto derivato dal [**\_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="e022a-104">The **StopService** method stops the service represented by the object derived from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e022a-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="e022a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e022a-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e022a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e022a-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="e022a-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e022a-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e022a-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e022a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e022a-109">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="e022a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e022a-110">Parameters</span></span>

<span data-ttu-id="e022a-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e022a-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e022a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e022a-112">Return value</span></span>

<span data-ttu-id="e022a-113">Restituisce un valore pari a 0 (zero) se il servizio è stato arrestato correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="e022a-113">Returns a value of 0 (zero) if the service was successfully stopped, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e022a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e022a-114">Remarks</span></span>

<span data-ttu-id="e022a-115">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="e022a-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e022a-116">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="e022a-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="e022a-117">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="e022a-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e022a-118">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="e022a-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e022a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e022a-119">Requirements</span></span>



| <span data-ttu-id="e022a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e022a-120">Requirement</span></span> | <span data-ttu-id="e022a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e022a-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e022a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e022a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e022a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e022a-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e022a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e022a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e022a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e022a-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e022a-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e022a-126">Namespace</span></span><br/>                | <span data-ttu-id="e022a-127">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e022a-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e022a-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e022a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e022a-129"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="e022a-129"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="e022a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e022a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e022a-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e022a-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e022a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e022a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e022a-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e022a-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e022a-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e022a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e022a-135">\_Servizio CIM</span><span class="sxs-lookup"><span data-stu-id="e022a-135">CIM\_Service</span></span>](stopservice-method-in-class-cim-service.md)
</dt> <dt>

[<span data-ttu-id="e022a-136">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="e022a-136">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 


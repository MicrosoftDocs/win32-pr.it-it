---
description: Arresta il servizio rappresentato dall'oggetto derivato da CIM \_ ClusteringService.
ms.assetid: b8dbaeeb-819b-469b-9f5e-d658e88d1a6e
ms.tgt_platform: multiple
title: Metodo StopService della classe CIM_ClusteringService (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3a55f7b0a9527092e51156d55c7513ee59c4861
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877833"
---
# <a name="stopservice-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="c978c-103">Metodo StopService della classe CIM \_ ClusteringService</span><span class="sxs-lookup"><span data-stu-id="c978c-103">StopService method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="c978c-104">Il metodo **StopService** arresta il servizio rappresentato dall'oggetto derivato da [**CIM \_ ClusteringService**](cim-clusteringservice.md).</span><span class="sxs-lookup"><span data-stu-id="c978c-104">The **StopService** method stops the service represented by the object derived from [**CIM\_ClusteringService**](cim-clusteringservice.md).</span></span> <span data-ttu-id="c978c-105">Questo metodo viene ereditato dal [**\_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="c978c-105">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c978c-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="c978c-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c978c-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c978c-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c978c-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c978c-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c978c-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c978c-109">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c978c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c978c-110">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="c978c-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="c978c-111">Parameters</span></span>

<span data-ttu-id="c978c-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c978c-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c978c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c978c-113">Return value</span></span>

<span data-ttu-id="c978c-114">Restituisce un valore pari a 0 (zero) se il servizio è stato arrestato correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="c978c-114">Returns a value of 0 (zero) if the service was successfully stopped, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="c978c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c978c-115">Remarks</span></span>

<span data-ttu-id="c978c-116">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="c978c-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c978c-117">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="c978c-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c978c-118">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="c978c-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c978c-119">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="c978c-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c978c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c978c-120">Requirements</span></span>



| <span data-ttu-id="c978c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c978c-121">Requirement</span></span> | <span data-ttu-id="c978c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c978c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c978c-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c978c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c978c-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c978c-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c978c-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c978c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c978c-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c978c-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c978c-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c978c-127">Namespace</span></span><br/>                | <span data-ttu-id="c978c-128">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c978c-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c978c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c978c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c978c-130"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="c978c-130"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="c978c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c978c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c978c-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c978c-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c978c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c978c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c978c-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c978c-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c978c-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c978c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c978c-136">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="c978c-136">**CIM\_ClusteringService**</span></span>](stopservice-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="c978c-137">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="c978c-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 


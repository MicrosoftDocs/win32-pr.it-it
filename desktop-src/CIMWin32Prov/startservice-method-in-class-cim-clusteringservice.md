---
description: Il metodo StartService inserisce il servizio in uno stato avviato.
ms.assetid: 2efd2a06-a03c-4f4c-b2fa-889f84faac0f
ms.tgt_platform: multiple
title: Metodo StartService della classe CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8abdeffa234461952f99013524042dcbba6e682
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225660"
---
# <a name="startservice-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="c3ad2-103">Metodo StartService della classe CIM \_ ClusteringService</span><span class="sxs-lookup"><span data-stu-id="c3ad2-103">StartService method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="c3ad2-104">Il metodo **StartService** inserisce il servizio in uno stato avviato.</span><span class="sxs-lookup"><span data-stu-id="c3ad2-104">The **StartService** method puts the service in a started state.</span></span> <span data-ttu-id="c3ad2-105">In una sottoclasse, il set di possibili codici restituiti può essere specificato utilizzando un qualificatore **ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="c3ad2-105">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="c3ad2-106">Le stringhe a cui viene convertito il contenuto **ValueMap** possono anche essere specificate nella sottoclasse come qualificatore della matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="c3ad2-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="c3ad2-107">Questo metodo viene ereditato dal [**\_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="c3ad2-107">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c3ad2-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="c3ad2-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c3ad2-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c3ad2-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c3ad2-110">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c3ad2-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c3ad2-111">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c3ad2-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c3ad2-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3ad2-112">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="c3ad2-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3ad2-113">Parameters</span></span>

<span data-ttu-id="c3ad2-114">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c3ad2-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3ad2-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3ad2-115">Return value</span></span>

<span data-ttu-id="c3ad2-116">Restituisce un valore pari a 0 (zero) se il servizio è stato avviato correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="c3ad2-116">Returns a value of 0 (zero) if the service was successfully started, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3ad2-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3ad2-117">Remarks</span></span>

<span data-ttu-id="c3ad2-118">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="c3ad2-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c3ad2-119">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="c3ad2-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c3ad2-120">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="c3ad2-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c3ad2-121">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="c3ad2-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3ad2-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3ad2-122">Requirements</span></span>



| <span data-ttu-id="c3ad2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3ad2-123">Requirement</span></span> | <span data-ttu-id="c3ad2-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c3ad2-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3ad2-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3ad2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c3ad2-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3ad2-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c3ad2-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3ad2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c3ad2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3ad2-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c3ad2-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c3ad2-129">Namespace</span></span><br/>                | <span data-ttu-id="c3ad2-130">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c3ad2-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c3ad2-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c3ad2-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3ad2-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3ad2-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3ad2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c3ad2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3ad2-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3ad2-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3ad2-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3ad2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3ad2-136">\_CLUSTERINGSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="c3ad2-136">CIM\_ClusteringService</span></span>](startservice-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="c3ad2-137">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="c3ad2-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 


---
description: Il metodo Reset richiede la reimpostazione del dispositivo logico. Questo metodo viene ereditato da \_ LOGICALDEVICE CIM.
ms.assetid: 4ddbad2a-e586-434a-a33e-7d60dcb67b3a
ms.tgt_platform: multiple
title: Reimposta il metodo della classe CIM_DiscreteSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiscreteSensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d45544e62144c2d3aa14d898b5d595d3ea5b34f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747767"
---
# <a name="reset-method-of-the-cim_discretesensor-class"></a><span data-ttu-id="b8647-104">Metodo Reset della classe CIM \_ DiscreteSensor</span><span class="sxs-lookup"><span data-stu-id="b8647-104">Reset method of the CIM\_DiscreteSensor class</span></span>

<span data-ttu-id="b8647-105">Il metodo **Reset** richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="b8647-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="b8647-106">Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="b8647-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8647-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="b8647-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b8647-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b8647-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b8647-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8647-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="b8647-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8647-110">Parameters</span></span>

<span data-ttu-id="b8647-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b8647-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8647-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8647-112">Return value</span></span>

<span data-ttu-id="b8647-113">Restituisce 0 (zero) se la richiesta è stata eseguita correttamente, 1 (uno) se la richiesta non è supportata e un altro valore se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="b8647-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8647-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8647-114">Remarks</span></span>

<span data-ttu-id="b8647-115">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="b8647-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="b8647-116">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="b8647-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="b8647-117">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="b8647-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b8647-118">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="b8647-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8647-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8647-119">Requirements</span></span>



| <span data-ttu-id="b8647-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8647-120">Requirement</span></span> | <span data-ttu-id="b8647-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b8647-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8647-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8647-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b8647-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8647-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8647-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8647-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b8647-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8647-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8647-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b8647-126">Namespace</span></span><br/>                | <span data-ttu-id="b8647-127">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b8647-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b8647-128">MOF</span><span class="sxs-lookup"><span data-stu-id="b8647-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8647-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8647-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8647-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b8647-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8647-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8647-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8647-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8647-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8647-133">\_DISCRETESENSOR CIM</span><span class="sxs-lookup"><span data-stu-id="b8647-133">CIM\_DiscreteSensor</span></span>](reset-method-in-class-cim-discretesensor.md)
</dt> <dt>

[<span data-ttu-id="b8647-134">**\_DISCRETESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="b8647-134">**CIM\_DiscreteSensor**</span></span>](cim-discretesensor.md)
</dt> </dl>

 

 





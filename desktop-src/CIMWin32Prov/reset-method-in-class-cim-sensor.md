---
description: Il metodo Reset richiede la reimpostazione del dispositivo logico. Questo metodo viene ereditato da \_ LOGICALDEVICE CIM.
ms.assetid: d764986b-b512-4f38-8284-d16b1f670871
ms.tgt_platform: multiple
title: Reimposta il metodo della classe CIM_Sensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Sensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e7aaddafd0c2316bb2fb996ec5f9640e0135899c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127626"
---
# <a name="reset-method-of-the-cim_sensor-class"></a><span data-ttu-id="8e2c3-104">Reimposta il metodo della \_ classe CIM Sensor</span><span class="sxs-lookup"><span data-stu-id="8e2c3-104">Reset method of the CIM\_Sensor class</span></span>

<span data-ttu-id="8e2c3-105">Il metodo **Reset** richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="8e2c3-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="8e2c3-106">Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8e2c3-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8e2c3-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="8e2c3-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8e2c3-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8e2c3-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8e2c3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e2c3-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="8e2c3-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e2c3-110">Parameters</span></span>

<span data-ttu-id="8e2c3-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8e2c3-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e2c3-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e2c3-112">Return value</span></span>

<span data-ttu-id="8e2c3-113">Restituisce 0 (zero) se la richiesta è stata eseguita correttamente, 1 (uno) se la richiesta non è supportata e un altro valore se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="8e2c3-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e2c3-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e2c3-114">Remarks</span></span>

<span data-ttu-id="8e2c3-115">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="8e2c3-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8e2c3-116">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="8e2c3-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="8e2c3-117">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="8e2c3-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8e2c3-118">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="8e2c3-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e2c3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e2c3-119">Requirements</span></span>



| <span data-ttu-id="8e2c3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e2c3-120">Requirement</span></span> | <span data-ttu-id="8e2c3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8e2c3-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e2c3-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e2c3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8e2c3-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e2c3-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e2c3-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e2c3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8e2c3-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e2c3-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e2c3-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8e2c3-126">Namespace</span></span><br/>                | <span data-ttu-id="8e2c3-127">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8e2c3-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e2c3-128">MOF</span><span class="sxs-lookup"><span data-stu-id="8e2c3-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e2c3-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e2c3-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e2c3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8e2c3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e2c3-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e2c3-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e2c3-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e2c3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e2c3-133">\_Sensore CIM</span><span class="sxs-lookup"><span data-stu-id="8e2c3-133">CIM\_Sensor</span></span>](reset-method-in-class-cim-sensor.md)
</dt> <dt>

[<span data-ttu-id="8e2c3-134">**\_Sensore CIM**</span><span class="sxs-lookup"><span data-stu-id="8e2c3-134">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

 





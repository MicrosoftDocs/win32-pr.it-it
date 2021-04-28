---
description: 'Metodo Reset della classe CIM_Sensor: il metodo Reset richiede una reimpostazione del dispositivo logico. Questo metodo viene ereditato da CIM \_ LogicalDevice.'
ms.assetid: d764986b-b512-4f38-8284-d16b1f670871
ms.tgt_platform: multiple
title: Metodo Reset della classe CIM_Sensor
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
ms.openlocfilehash: 9a17599216226f2420504ee07fccd2174d7eff4e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096859"
---
# <a name="reset-method-of-the-cim_sensor-class"></a><span data-ttu-id="0a97d-104">Metodo Reset della classe Sensor \_ CIM</span><span class="sxs-lookup"><span data-stu-id="0a97d-104">Reset method of the CIM\_Sensor class</span></span>

<span data-ttu-id="0a97d-105">Il **metodo Reset** richiede una reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="0a97d-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="0a97d-106">Questo metodo viene ereditato da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="0a97d-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a97d-107">Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model) sono le classi padre su cui vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="0a97d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0a97d-108">WMI attualmente supporta solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0a97d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0a97d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a97d-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="0a97d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a97d-110">Parameters</span></span>

<span data-ttu-id="0a97d-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0a97d-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0a97d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a97d-112">Return value</span></span>

<span data-ttu-id="0a97d-113">Restituisce 0 (zero) se la richiesta è stata eseguita correttamente, 1 (uno) se la richiesta non è supportata e un altro valore se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="0a97d-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a97d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a97d-114">Remarks</span></span>

<span data-ttu-id="0a97d-115">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="0a97d-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0a97d-116">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="0a97d-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0a97d-117">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="0a97d-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0a97d-118">Microsoft potrebbe aver apportato modifiche per correggere errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="0a97d-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a97d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a97d-119">Requirements</span></span>



| <span data-ttu-id="0a97d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a97d-120">Requirement</span></span> | <span data-ttu-id="0a97d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0a97d-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a97d-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a97d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0a97d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a97d-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0a97d-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a97d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0a97d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a97d-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0a97d-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0a97d-126">Namespace</span></span><br/>                | <span data-ttu-id="0a97d-127">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0a97d-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0a97d-128">MOF</span><span class="sxs-lookup"><span data-stu-id="0a97d-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a97d-129"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a97d-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a97d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0a97d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a97d-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a97d-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a97d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a97d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a97d-133">Sensore \_ CIM</span><span class="sxs-lookup"><span data-stu-id="0a97d-133">CIM\_Sensor</span></span>](reset-method-in-class-cim-sensor.md)
</dt> <dt>

[<span data-ttu-id="0a97d-134">**Sensore \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="0a97d-134">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

 





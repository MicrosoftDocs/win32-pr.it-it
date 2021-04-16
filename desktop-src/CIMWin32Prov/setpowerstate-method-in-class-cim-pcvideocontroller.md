---
description: Il metodo SetPowerState della classe CIM \_ PCVideoController imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.
ms.assetid: db219a22-0f03-432e-b1c9-071771059ed6
ms.tgt_platform: multiple
title: Metodo SetPowerState della classe CIM_PCVideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCVideoController.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad70e0609e8793da314382a5732bc90b11348e33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524329"
---
# <a name="setpowerstate-method-of-the-cim_pcvideocontroller-class"></a><span data-ttu-id="8baeb-103">Metodo SetPowerState della classe CIM \_ PCVideoController</span><span class="sxs-lookup"><span data-stu-id="8baeb-103">SetPowerState method of the CIM\_PCVideoController class</span></span>

<span data-ttu-id="8baeb-104">Il metodo **SetPowerState** della classe CIM \_ PCVideoController imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="8baeb-104">The **SetPowerState** method of the CIM\_PCVideoController class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="8baeb-105">In una sottoclasse, è necessario specificare il set di possibili codici restituiti utilizzando un qualificatore **ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="8baeb-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="8baeb-106">Le stringhe a cui viene convertito il contenuto **ValueMap** devono essere specificate anche nella sottoclasse come qualificatore della matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="8baeb-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="8baeb-107">Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8baeb-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8baeb-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="8baeb-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8baeb-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8baeb-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8baeb-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8baeb-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="8baeb-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="8baeb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8baeb-112">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8baeb-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8baeb-113">Valore **ValueMap** che specifica lo stato di alimentazione desiderato per questo dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="8baeb-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="8baeb-114">1</span><span class="sxs-lookup"><span data-stu-id="8baeb-114">1</span></span>
</dt> <dd>

<span data-ttu-id="8baeb-115">Potenza piena.</span><span class="sxs-lookup"><span data-stu-id="8baeb-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="8baeb-116">2</span><span class="sxs-lookup"><span data-stu-id="8baeb-116">2</span></span>
</dt> <dd>

<span data-ttu-id="8baeb-117">Risparmio energia-modalità a basso consumo.</span><span class="sxs-lookup"><span data-stu-id="8baeb-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="8baeb-118">3</span><span class="sxs-lookup"><span data-stu-id="8baeb-118">3</span></span>
</dt> <dd>

<span data-ttu-id="8baeb-119">Risparmio energia standby.</span><span class="sxs-lookup"><span data-stu-id="8baeb-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="8baeb-120">4</span><span class="sxs-lookup"><span data-stu-id="8baeb-120">4</span></span>
</dt> <dd>

<span data-ttu-id="8baeb-121">Risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="8baeb-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="8baeb-122">5</span><span class="sxs-lookup"><span data-stu-id="8baeb-122">5</span></span>
</dt> <dd>

<span data-ttu-id="8baeb-123">Ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="8baeb-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="8baeb-124">6</span><span class="sxs-lookup"><span data-stu-id="8baeb-124">6</span></span>
</dt> <dd>

<span data-ttu-id="8baeb-125">Spegnimento.</span><span class="sxs-lookup"><span data-stu-id="8baeb-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8baeb-126">*Ora* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8baeb-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8baeb-127">Specifica quando deve essere impostato lo stato di alimentazione, come valore di data e ora normale o come valore di intervallo, in cui l'intervallo inizia quando viene ricevuta la chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="8baeb-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="8baeb-128">Quando il parametro *PowerState* è uguale a 5 ("ciclo di alimentazione"), il parametro *Time* indica quando riaccendere il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8baeb-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="8baeb-129">Lo spegnimento è immediato.</span><span class="sxs-lookup"><span data-stu-id="8baeb-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8baeb-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8baeb-130">Return value</span></span>

<span data-ttu-id="8baeb-131">Restituisce 0 (zero) se ha esito positivo, 1 (uno) se la richiesta *PowerState* e *Time* specificata non è supportata e un altro valore se si sono verificati altri errori.</span><span class="sxs-lookup"><span data-stu-id="8baeb-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="8baeb-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="8baeb-132">Remarks</span></span>

<span data-ttu-id="8baeb-133">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="8baeb-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8baeb-134">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="8baeb-134">To use this method, you must implement it in your own provider.</span></span> <span data-ttu-id="8baeb-135">Per le classi WMI derivate da [**CIM \_ PCVideoController**](cim-pcvideocontroller.md), vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8baeb-135">For WMI classes derived from [**CIM\_PCVideoController**](cim-pcvideocontroller.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8baeb-136">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="8baeb-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8baeb-137">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="8baeb-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8baeb-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8baeb-138">Requirements</span></span>



| <span data-ttu-id="8baeb-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8baeb-139">Requirement</span></span> | <span data-ttu-id="8baeb-140">Valore</span><span class="sxs-lookup"><span data-stu-id="8baeb-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8baeb-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8baeb-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8baeb-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8baeb-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8baeb-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8baeb-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8baeb-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8baeb-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8baeb-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8baeb-145">Namespace</span></span><br/>                | <span data-ttu-id="8baeb-146">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8baeb-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8baeb-147">MOF</span><span class="sxs-lookup"><span data-stu-id="8baeb-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8baeb-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8baeb-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8baeb-149">DLL</span><span class="sxs-lookup"><span data-stu-id="8baeb-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8baeb-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8baeb-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8baeb-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8baeb-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8baeb-152">\_PCVIDEOCONTROLLER CIM</span><span class="sxs-lookup"><span data-stu-id="8baeb-152">CIM\_PCVideoController</span></span>](setpowerstate-method-in-class-cim-pcvideocontroller.md)
</dt> <dt>

[<span data-ttu-id="8baeb-153">**\_PCVIDEOCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="8baeb-153">**CIM\_PCVideoController**</span></span>](cim-pcvideocontroller.md)
</dt> </dl>

 

 





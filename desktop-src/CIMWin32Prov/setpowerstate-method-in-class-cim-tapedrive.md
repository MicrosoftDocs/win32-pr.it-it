---
description: Il metodo SetPowerState della classe CIM \_ TapeDrive imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.
ms.assetid: 73f98d08-49da-4b21-91c4-cbe420c648e4
ms.tgt_platform: multiple
title: Metodo SetPowerState della classe CIM_TapeDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a6efcfe08dfddca3477081f65fac35780f713005
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524153"
---
# <a name="setpowerstate-method-of-the-cim_tapedrive-class"></a><span data-ttu-id="aa75d-103">Metodo SetPowerState della classe CIM \_ TapeDrive</span><span class="sxs-lookup"><span data-stu-id="aa75d-103">SetPowerState method of the CIM\_TapeDrive class</span></span>

<span data-ttu-id="aa75d-104">Il metodo **SetPowerState** della classe CIM \_ TapeDrive imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="aa75d-104">The **SetPowerState** method of the CIM\_TapeDrive class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="aa75d-105">In una sottoclasse, è necessario specificare il set di possibili codici restituiti utilizzando un qualificatore **ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="aa75d-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="aa75d-106">Le stringhe a cui viene convertito il contenuto **ValueMap** devono essere specificate anche nella sottoclasse come qualificatore della matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="aa75d-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="aa75d-107">Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa75d-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa75d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa75d-108">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="aa75d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa75d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa75d-110">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa75d-110">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa75d-111">Valore **ValueMap** che specifica lo stato di alimentazione desiderato per questo dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="aa75d-111">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="aa75d-112">1</span><span class="sxs-lookup"><span data-stu-id="aa75d-112">1</span></span>
</dt> <dd>

<span data-ttu-id="aa75d-113">Potenza piena.</span><span class="sxs-lookup"><span data-stu-id="aa75d-113">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="aa75d-114">2</span><span class="sxs-lookup"><span data-stu-id="aa75d-114">2</span></span>
</dt> <dd>

<span data-ttu-id="aa75d-115">Risparmio energia-modalità a basso consumo.</span><span class="sxs-lookup"><span data-stu-id="aa75d-115">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="aa75d-116">3</span><span class="sxs-lookup"><span data-stu-id="aa75d-116">3</span></span>
</dt> <dd>

<span data-ttu-id="aa75d-117">Risparmio energia standby.</span><span class="sxs-lookup"><span data-stu-id="aa75d-117">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="aa75d-118">4</span><span class="sxs-lookup"><span data-stu-id="aa75d-118">4</span></span>
</dt> <dd>

<span data-ttu-id="aa75d-119">Risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="aa75d-119">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="aa75d-120">5</span><span class="sxs-lookup"><span data-stu-id="aa75d-120">5</span></span>
</dt> <dd>

<span data-ttu-id="aa75d-121">Ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="aa75d-121">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="aa75d-122">6</span><span class="sxs-lookup"><span data-stu-id="aa75d-122">6</span></span>
</dt> <dd>

<span data-ttu-id="aa75d-123">Spegnimento.</span><span class="sxs-lookup"><span data-stu-id="aa75d-123">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="aa75d-124">*Ora* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="aa75d-124">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa75d-125">Specifica quando deve essere impostato lo stato di alimentazione, come valore di data e ora normale o come valore di intervallo, in cui l'intervallo inizia quando viene ricevuta la chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="aa75d-125">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="aa75d-126">Quando il parametro *PowerState* è uguale a 5 ("ciclo di alimentazione"), il parametro *Time* indica quando riaccendere il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa75d-126">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="aa75d-127">Lo spegnimento è immediato.</span><span class="sxs-lookup"><span data-stu-id="aa75d-127">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa75d-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa75d-128">Return value</span></span>

<span data-ttu-id="aa75d-129">Restituisce 0 (zero) se ha esito positivo, 1 (uno) se la richiesta *PowerState* e *Time* specificata non è supportata e un altro valore se si sono verificati altri errori.</span><span class="sxs-lookup"><span data-stu-id="aa75d-129">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa75d-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa75d-130">Remarks</span></span>

<span data-ttu-id="aa75d-131">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="aa75d-131">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="aa75d-132">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="aa75d-132">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="aa75d-133">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="aa75d-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="aa75d-134">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="aa75d-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa75d-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa75d-135">Requirements</span></span>



| <span data-ttu-id="aa75d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa75d-136">Requirement</span></span> | <span data-ttu-id="aa75d-137">Valore</span><span class="sxs-lookup"><span data-stu-id="aa75d-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa75d-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa75d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="aa75d-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa75d-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aa75d-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa75d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="aa75d-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa75d-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aa75d-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aa75d-142">Namespace</span></span><br/>                | <span data-ttu-id="aa75d-143">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="aa75d-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aa75d-144">MOF</span><span class="sxs-lookup"><span data-stu-id="aa75d-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa75d-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa75d-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa75d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="aa75d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa75d-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa75d-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa75d-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa75d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa75d-149">\_TAPEDRIVE CIM</span><span class="sxs-lookup"><span data-stu-id="aa75d-149">CIM\_TapeDrive</span></span>](setpowerstate-method-in-class-cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="aa75d-150">**\_TAPEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="aa75d-150">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> </dl>

 

 





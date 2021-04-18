---
description: Il metodo SetPowerState della classe CIM \_ LogicalDevice imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.
ms.assetid: 0d9678e0-a956-45d3-ac41-5c1604478fd7
ms.tgt_platform: multiple
title: Metodo SetPowerState della classe CIM_LogicalDevice (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd258a4372c16a7f98f2fe3ea8b84bbfef44f69e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304888"
---
# <a name="setpowerstate-method-of-the-cim_logicaldevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="ce2ab-103">Metodo SetPowerState della classe CIM_LogicalDevice (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="ce2ab-103">SetPowerState method of the CIM_LogicalDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ce2ab-104">Il metodo **SetPowerState** della classe CIM \_ LogicalDevice imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-104">The **SetPowerState** method of the CIM\_LogicalDevice class sets the desired power state for a logical device and when a device should be put into that state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ce2ab-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ce2ab-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ce2ab-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ce2ab-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce2ab-107">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="ce2ab-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce2ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce2ab-109">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce2ab-109">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce2ab-110">Valore **ValueMap** che specifica lo stato di alimentazione desiderato per questo dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-110">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="ce2ab-111"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Potenza completa** (1)</span><span class="sxs-lookup"><span data-stu-id="ce2ab-111"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ce2ab-112">Potenza piena.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-112">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ce2ab-113"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (2)</span><span class="sxs-lookup"><span data-stu-id="ce2ab-113"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ce2ab-114">Risparmio energia-modalità a basso consumo.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-114">Power save   low-power mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ce2ab-115"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (3)</span><span class="sxs-lookup"><span data-stu-id="ce2ab-115"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ce2ab-116">Risparmio energia standby.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-116">Power save   standby.</span></span>

</dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="ce2ab-117"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Risparmio energia-altro** (4)</span><span class="sxs-lookup"><span data-stu-id="ce2ab-117"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Power Save - Other** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ce2ab-118">Risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-118">Power save   other.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ce2ab-119"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (5)</span><span class="sxs-lookup"><span data-stu-id="ce2ab-119"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ce2ab-120">Ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-120">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ce2ab-121"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (6** )</span><span class="sxs-lookup"><span data-stu-id="ce2ab-121"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ce2ab-122">Spegnimento.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-122">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ce2ab-123">*Ora* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ce2ab-123">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce2ab-124">Specifica quando deve essere impostato lo stato di alimentazione, come valore di data e ora normale o come valore di intervallo, in cui l'intervallo inizia quando viene ricevuta la chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-124">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="ce2ab-125">Quando il parametro *PowerState* è uguale a 5 ("ciclo di alimentazione"), il parametro *Time* indica quando riaccendere il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-125">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="ce2ab-126">Lo spegnimento è immediato.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-126">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce2ab-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce2ab-127">Return value</span></span>

<span data-ttu-id="ce2ab-128">Restituisce 0 (zero) se ha esito positivo, 1 (uno) se la richiesta *PowerState* e *Time* specificata non è supportata e un altro valore se si sono verificati altri errori.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-128">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce2ab-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce2ab-129">Remarks</span></span>

<span data-ttu-id="ce2ab-130">In una sottoclasse, è necessario specificare il set di possibili codici restituiti utilizzando un qualificatore **ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-130">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="ce2ab-131">Le stringhe a cui viene convertito il contenuto **ValueMap** devono essere specificate anche nella sottoclasse come qualificatore della matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="ce2ab-131">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="ce2ab-132">Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ce2ab-132">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ce2ab-133">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="ce2ab-134">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="ce2ab-135">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ce2ab-136">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ce2ab-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce2ab-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce2ab-137">Requirements</span></span>



| <span data-ttu-id="ce2ab-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce2ab-138">Requirement</span></span> | <span data-ttu-id="ce2ab-139">Valore</span><span class="sxs-lookup"><span data-stu-id="ce2ab-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce2ab-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce2ab-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ce2ab-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce2ab-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ce2ab-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce2ab-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ce2ab-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce2ab-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ce2ab-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ce2ab-144">Namespace</span></span><br/>                | <span data-ttu-id="ce2ab-145">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ce2ab-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ce2ab-146">MOF</span><span class="sxs-lookup"><span data-stu-id="ce2ab-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce2ab-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce2ab-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce2ab-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ce2ab-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce2ab-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce2ab-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce2ab-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce2ab-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce2ab-151">\_LOGICALDEVICE CIM</span><span class="sxs-lookup"><span data-stu-id="ce2ab-151">CIM\_LogicalDevice</span></span>](setpowerstate-method-in-class-cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="ce2ab-152">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="ce2ab-152">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 





---
description: Il metodo SetPowerState della classe CIM \_ UnitaryComputerSystem imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.
ms.assetid: a02991d5-3c93-4579-b1f5-f70ad7c7052b
ms.tgt_platform: multiple
title: Metodo SetPowerState della classe CIM_UnitaryComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UnitaryComputerSystem.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4d9b69306c7bb362dceaee254be5dae8f5d37a52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965899"
---
# <a name="setpowerstate-method-of-the-cim_unitarycomputersystem-class"></a><span data-ttu-id="9366d-103">Metodo SetPowerState della classe CIM \_ UnitaryComputerSystem</span><span class="sxs-lookup"><span data-stu-id="9366d-103">SetPowerState method of the CIM\_UnitaryComputerSystem class</span></span>

<span data-ttu-id="9366d-104">Il metodo **SetPowerState** della classe CIM \_ UnitaryComputerSystem imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="9366d-104">The **SetPowerState** method of the CIM\_UnitaryComputerSystem class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="9366d-105">In una sottoclasse, è necessario specificare il set di possibili codici restituiti utilizzando un qualificatore **ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="9366d-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="9366d-106">Le stringhe a cui viene convertito il contenuto **ValueMap** devono essere specificate anche nella sottoclasse come qualificatore della matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="9366d-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="9366d-107">Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9366d-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9366d-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="9366d-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9366d-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9366d-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9366d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9366d-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="9366d-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="9366d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9366d-112">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9366d-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9366d-113">Valore **ValueMap** che specifica lo stato di alimentazione desiderato per questo dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9366d-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="9366d-114"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Potenza completa** (1)</span><span class="sxs-lookup"><span data-stu-id="9366d-114"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9366d-115">Potenza piena.</span><span class="sxs-lookup"><span data-stu-id="9366d-115">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="9366d-116"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (2)</span><span class="sxs-lookup"><span data-stu-id="9366d-116"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9366d-117">Risparmio energia-modalità a basso consumo.</span><span class="sxs-lookup"><span data-stu-id="9366d-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="9366d-118"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (3)</span><span class="sxs-lookup"><span data-stu-id="9366d-118"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9366d-119">Risparmio energia standby.</span><span class="sxs-lookup"><span data-stu-id="9366d-119">Power save   standby.</span></span>

</dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="9366d-120"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Risparmio energia-altro** (4)</span><span class="sxs-lookup"><span data-stu-id="9366d-120"><span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Power Save - Other** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9366d-121">Risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="9366d-121">Power save   other.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="9366d-122"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (5)</span><span class="sxs-lookup"><span data-stu-id="9366d-122"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9366d-123">Ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="9366d-123">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="9366d-124"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (6** )</span><span class="sxs-lookup"><span data-stu-id="9366d-124"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9366d-125">Spegnimento.</span><span class="sxs-lookup"><span data-stu-id="9366d-125">Power off.</span></span>

</dd> <dt>

<span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>

<span data-ttu-id="9366d-126"><span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>**Ibernazione** (7)</span><span class="sxs-lookup"><span data-stu-id="9366d-126"><span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>**Hibernate** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9366d-127">Hibernate.</span><span class="sxs-lookup"><span data-stu-id="9366d-127">Hibernate.</span></span>

</dd> <dt>

<span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>

<span data-ttu-id="9366d-128"><span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>**Soft off** (8)</span><span class="sxs-lookup"><span data-stu-id="9366d-128"><span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>**Soft Off** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9366d-129">Soft off.</span><span class="sxs-lookup"><span data-stu-id="9366d-129">Soft off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9366d-130">*Ora* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9366d-130">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9366d-131">Specifica quando deve essere impostato lo stato di alimentazione, come valore di data e ora normale o come valore di intervallo, in cui l'intervallo inizia quando viene ricevuta la chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="9366d-131">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="9366d-132">Quando il parametro *PowerState* è uguale a 5 ("ciclo di alimentazione"), il parametro *Time* indica quando riaccendere il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9366d-132">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="9366d-133">Lo spegnimento è immediato.</span><span class="sxs-lookup"><span data-stu-id="9366d-133">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9366d-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9366d-134">Return value</span></span>

<span data-ttu-id="9366d-135">Restituisce 0 (zero) se ha esito positivo, 1 (uno) se la richiesta *PowerState* e *Time* specificata non è supportata e un altro valore se si sono verificati altri errori.</span><span class="sxs-lookup"><span data-stu-id="9366d-135">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="9366d-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="9366d-136">Remarks</span></span>

<span data-ttu-id="9366d-137">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="9366d-137">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="9366d-138">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="9366d-138">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="9366d-139">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="9366d-139">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9366d-140">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="9366d-140">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9366d-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9366d-141">Requirements</span></span>



| <span data-ttu-id="9366d-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="9366d-142">Requirement</span></span> | <span data-ttu-id="9366d-143">Valore</span><span class="sxs-lookup"><span data-stu-id="9366d-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9366d-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9366d-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9366d-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9366d-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9366d-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9366d-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9366d-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9366d-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9366d-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9366d-148">Namespace</span></span><br/>                | <span data-ttu-id="9366d-149">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9366d-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9366d-150">MOF</span><span class="sxs-lookup"><span data-stu-id="9366d-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9366d-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9366d-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9366d-152">DLL</span><span class="sxs-lookup"><span data-stu-id="9366d-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9366d-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9366d-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9366d-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9366d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9366d-155">\_UNITARYCOMPUTERSYSTEM CIM</span><span class="sxs-lookup"><span data-stu-id="9366d-155">CIM\_UnitaryComputerSystem</span></span>](setpowerstate-method-in-class-cim-unitarycomputersystem.md)
</dt> <dt>

[<span data-ttu-id="9366d-156">**\_UNITARYCOMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="9366d-156">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> </dl>

 

 





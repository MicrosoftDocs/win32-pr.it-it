---
description: La \_ classe CIM USBControllerHasHub definisce gli hub a valle del controller USB.
ms.assetid: 38bc0342-3ff0-42c8-9c1e-ea5a5822e1d3
ms.tgt_platform: multiple
title: Classe CIM_USBControllerHasHub
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBControllerHasHub
- CIM_USBControllerHasHub.NegotiatedDataWidth
- CIM_USBControllerHasHub.NegotiatedSpeed
- CIM_USBControllerHasHub.AccessState
- CIM_USBControllerHasHub.NumberOfHardResets
- CIM_USBControllerHasHub.NumberOfSoftResets
- CIM_USBControllerHasHub.Dependent
- CIM_USBControllerHasHub.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba0f6d9a618a194faa8d16f9b2f53c6ce10653cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125826"
---
# <a name="cim_usbcontrollerhashub-class"></a><span data-ttu-id="f65d2-103">CIM \_ USBControllerHasHub (classe)</span><span class="sxs-lookup"><span data-stu-id="f65d2-103">CIM\_USBControllerHasHub class</span></span>

<span data-ttu-id="f65d2-104">La classe **CIM \_ USBControllerHasHub** definisce gli hub a valle del controller USB.</span><span class="sxs-lookup"><span data-stu-id="f65d2-104">The **CIM\_USBControllerHasHub** class defines the hubs that are downstream of the USB controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f65d2-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="f65d2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f65d2-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f65d2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f65d2-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f65d2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f65d2-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f65d2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f65d2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f65d2-109">Syntax</span></span>

``` syntax
[AMENDMENT]
class CIM_USBControllerHasHub : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBHub        REF Dependent;
  CIM_USBController REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="f65d2-110">Members</span><span class="sxs-lookup"><span data-stu-id="f65d2-110">Members</span></span>

<span data-ttu-id="f65d2-111">La classe **CIM \_ USBControllerHasHub** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f65d2-111">The **CIM\_USBControllerHasHub** class has these types of members:</span></span>

-   [<span data-ttu-id="f65d2-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f65d2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f65d2-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f65d2-113">Properties</span></span>

<span data-ttu-id="f65d2-114">La classe **CIM \_ USBControllerHasHub** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f65d2-114">The **CIM\_USBControllerHasHub** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f65d2-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="f65d2-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f65d2-116">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f65d2-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f65d2-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f65d2-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f65d2-118">Indica se il controller sta attivando o accedendo attivamente al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f65d2-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="f65d2-119">Queste informazioni sono necessarie quando è possibile eseguire il comando o l'accesso a un dispositivo logico tramite più controller.</span><span class="sxs-lookup"><span data-stu-id="f65d2-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="f65d2-120">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="f65d2-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f65d2-121">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f65d2-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="f65d2-122">**Attivo** (1)</span><span class="sxs-lookup"><span data-stu-id="f65d2-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="f65d2-123">**Inattivo** (2)</span><span class="sxs-lookup"><span data-stu-id="f65d2-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f65d2-124">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="f65d2-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f65d2-125">Tipo di dati: **CIM \_ USBController**</span><span class="sxs-lookup"><span data-stu-id="f65d2-125">Data type: **CIM\_USBController**</span></span>
</dt> <dt>

<span data-ttu-id="f65d2-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f65d2-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f65d2-127">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="f65d2-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f65d2-128">Un [**\_ USBController CIM**](cim-usbcontroller.md) che descrive il USBController.</span><span class="sxs-lookup"><span data-stu-id="f65d2-128">A [**CIM\_USBController**](cim-usbcontroller.md) describing the USBController.</span></span>

</dd> <dt>

<span data-ttu-id="f65d2-129">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="f65d2-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f65d2-130">Tipo di dati: **CIM \_ USBHub**</span><span class="sxs-lookup"><span data-stu-id="f65d2-130">Data type: **CIM\_USBHub**</span></span>
</dt> <dt>

<span data-ttu-id="f65d2-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f65d2-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f65d2-132">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="f65d2-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f65d2-133">Un [**\_ USBHub CIM**](cim-usbhub.md) che descrive il USBHub associato al controller.</span><span class="sxs-lookup"><span data-stu-id="f65d2-133">A [**CIM\_USBHub**](cim-usbhub.md) describing the USBHub that is associated with the Controller.</span></span>

</dd> <dt>

<span data-ttu-id="f65d2-134">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="f65d2-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f65d2-135">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f65d2-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f65d2-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f65d2-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f65d2-137">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="f65d2-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="f65d2-138">Quando sono possibili più larghezze di dati del bus o della connessione, questa proprietà definisce quella in uso tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="f65d2-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="f65d2-139">La larghezza dei dati è specificata in bit.</span><span class="sxs-lookup"><span data-stu-id="f65d2-139">Data width is specified in bits.</span></span> <span data-ttu-id="f65d2-140">Se la larghezza dei dati non è negoziata o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="f65d2-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="f65d2-141">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="f65d2-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="f65d2-142">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="f65d2-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f65d2-143">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f65d2-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f65d2-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f65d2-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f65d2-145">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="f65d2-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="f65d2-146">Quando sono possibili più velocità di connessione o bus, questa proprietà definisce quella usata tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="f65d2-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="f65d2-147">La velocità è specificata in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="f65d2-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="f65d2-148">Se le velocità di connessione o di bus non vengono negoziate o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="f65d2-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="f65d2-149">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f65d2-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f65d2-150">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="f65d2-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="f65d2-151">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="f65d2-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f65d2-152">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f65d2-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f65d2-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f65d2-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f65d2-154">Numero di reimpostazioni rigide rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="f65d2-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="f65d2-155">Una reimpostazione hardware restituisce il dispositivo alla relativa inizializzazione o allo stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="f65d2-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="f65d2-156">Tutte le informazioni sullo stato del dispositivo interno e i dati vengono persi.</span><span class="sxs-lookup"><span data-stu-id="f65d2-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="f65d2-157">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="f65d2-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="f65d2-158">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="f65d2-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f65d2-159">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f65d2-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f65d2-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f65d2-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f65d2-161">Numero di reimpostazioni software rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="f65d2-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="f65d2-162">Un ripristino soft non cancella completamente i dati e lo stato corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f65d2-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="f65d2-163">La semantica esatta dipende dal dispositivo e dai protocolli e dai meccanismi usati per comunicare con esso.</span><span class="sxs-lookup"><span data-stu-id="f65d2-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="f65d2-164">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="f65d2-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f65d2-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="f65d2-165">Remarks</span></span>

<span data-ttu-id="f65d2-166">La classe **CIM \_ USBControllerHasHub** è derivata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="f65d2-166">The **CIM\_USBControllerHasHub** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="f65d2-167">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="f65d2-167">WMI does not implement this class.</span></span> <span data-ttu-id="f65d2-168">Per le classi WMI derivate da **CIM \_ USBControllerHasHub**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f65d2-168">For WMI classes derived from **CIM\_USBControllerHasHub**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f65d2-169">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f65d2-169">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f65d2-170">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="f65d2-170">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f65d2-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f65d2-171">Requirements</span></span>



| <span data-ttu-id="f65d2-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="f65d2-172">Requirement</span></span> | <span data-ttu-id="f65d2-173">Valore</span><span class="sxs-lookup"><span data-stu-id="f65d2-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f65d2-174">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f65d2-174">Minimum supported client</span></span><br/> | <span data-ttu-id="f65d2-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f65d2-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f65d2-176">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f65d2-176">Minimum supported server</span></span><br/> | <span data-ttu-id="f65d2-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f65d2-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f65d2-178">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f65d2-178">Namespace</span></span><br/>                | <span data-ttu-id="f65d2-179">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f65d2-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f65d2-180">MOF</span><span class="sxs-lookup"><span data-stu-id="f65d2-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f65d2-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f65d2-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f65d2-182">DLL</span><span class="sxs-lookup"><span data-stu-id="f65d2-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f65d2-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f65d2-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f65d2-184">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f65d2-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f65d2-185">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="f65d2-185">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 


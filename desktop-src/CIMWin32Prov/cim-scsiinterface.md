---
description: Rappresenta una \_ relazione CIM ControlledBy che indica i dispositivi a cui si accede tramite un controller SCSI e le caratteristiche di accesso.
ms.assetid: a036dbf9-f9ce-4c85-9184-fefcbe4583ba
ms.tgt_platform: multiple
title: Classe CIM_SCSIInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIInterface
- CIM_SCSIInterface.NegotiatedDataWidth
- CIM_SCSIInterface.NegotiatedSpeed
- CIM_SCSIInterface.AccessState
- CIM_SCSIInterface.NumberOfHardResets
- CIM_SCSIInterface.NumberOfSoftResets
- CIM_SCSIInterface.Dependent
- CIM_SCSIInterface.Antecedent
- CIM_SCSIInterface.SCSIRetries
- CIM_SCSIInterface.SCSITimeouts
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1211b142681f15aa8b4d5e61c1d2165a59f5a62c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748594"
---
# <a name="cim_scsiinterface-class"></a><span data-ttu-id="679b3-103">CIM \_ SCSIInterface (classe)</span><span class="sxs-lookup"><span data-stu-id="679b3-103">CIM\_SCSIInterface class</span></span>

<span data-ttu-id="679b3-104">La classe **CIM \_ SCSIInterface** rappresenta una relazione [**CIM \_ ControlledBy**](cim-controlledby.md) che indica i dispositivi a cui si accede tramite un controller SCSI e le caratteristiche di accesso.</span><span class="sxs-lookup"><span data-stu-id="679b3-104">The **CIM\_SCSIInterface** class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through a SCSI controller and the access characteristics.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="679b3-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="679b3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="679b3-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="679b3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="679b3-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="679b3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="679b3-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="679b3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="679b3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="679b3-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{7CE7448E-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SCSIInterface : CIM_ControlledBy
{
  uint32                 NegotiatedDataWidth;
  uint64                 NegotiatedSpeed;
  uint16                 AccessState;
  uint32                 NumberOfHardResets;
  uint32                 NumberOfSoftResets;
  CIM_LogicalDevice  REF Dependent;
  CIM_SCSIController REF Antecedent;
  uint32                 SCSIRetries;
  uint32                 SCSITimeouts;
};
```

## <a name="members"></a><span data-ttu-id="679b3-110">Members</span><span class="sxs-lookup"><span data-stu-id="679b3-110">Members</span></span>

<span data-ttu-id="679b3-111">La classe **CIM \_ SCSIInterface** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="679b3-111">The **CIM\_SCSIInterface** class has these types of members:</span></span>

-   [<span data-ttu-id="679b3-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="679b3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="679b3-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="679b3-113">Properties</span></span>

<span data-ttu-id="679b3-114">La classe **CIM \_ SCSIInterface** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="679b3-114">The **CIM\_SCSIInterface** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="679b3-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="679b3-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="679b3-116">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="679b3-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="679b3-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="679b3-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="679b3-118">Indica se il controller sta attivando o accedendo attivamente al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="679b3-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="679b3-119">Queste informazioni sono necessarie quando è possibile eseguire il comando o l'accesso a un dispositivo logico tramite più controller.</span><span class="sxs-lookup"><span data-stu-id="679b3-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="679b3-120">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="679b3-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="679b3-121">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="679b3-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="679b3-122">**Attivo** (1)</span><span class="sxs-lookup"><span data-stu-id="679b3-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="679b3-123">**Inattivo** (2)</span><span class="sxs-lookup"><span data-stu-id="679b3-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="679b3-124">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="679b3-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="679b3-125">Tipo di dati: **CIM \_ controller SCSI**</span><span class="sxs-lookup"><span data-stu-id="679b3-125">Data type: **CIM\_SCSIController**</span></span>
</dt> <dt>

<span data-ttu-id="679b3-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="679b3-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="679b3-127">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="679b3-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="679b3-128">Un [**\_ controller SCSI CIM**](cim-scsicontroller.md) che descrive il controller SCSI.</span><span class="sxs-lookup"><span data-stu-id="679b3-128">A [**CIM\_SCSIController**](cim-scsicontroller.md) that describes the SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="679b3-129">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="679b3-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="679b3-130">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="679b3-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="679b3-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="679b3-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="679b3-132">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="679b3-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="679b3-133">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="679b3-133">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="679b3-134">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="679b3-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="679b3-135">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="679b3-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="679b3-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="679b3-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="679b3-137">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="679b3-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="679b3-138">Quando sono possibili più larghezze di dati del bus o della connessione, questa proprietà definisce quella in uso tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="679b3-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="679b3-139">La larghezza dei dati è specificata in bit.</span><span class="sxs-lookup"><span data-stu-id="679b3-139">Data width is specified in bits.</span></span> <span data-ttu-id="679b3-140">Se la larghezza dei dati non è negoziata o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="679b3-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="679b3-141">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="679b3-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="679b3-142">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="679b3-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="679b3-143">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="679b3-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="679b3-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="679b3-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="679b3-145">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="679b3-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="679b3-146">Quando sono possibili più velocità di connessione o bus, questa proprietà definisce quella usata tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="679b3-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="679b3-147">La velocità è specificata in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="679b3-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="679b3-148">Se le velocità di connessione o di bus non vengono negoziate o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="679b3-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="679b3-149">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="679b3-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="679b3-150">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="679b3-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="679b3-151">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="679b3-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="679b3-152">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="679b3-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="679b3-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="679b3-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="679b3-154">Numero di reimpostazioni rigide rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="679b3-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="679b3-155">Una reimpostazione hardware restituisce il dispositivo alla relativa inizializzazione o allo stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="679b3-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="679b3-156">Tutte le informazioni sullo stato del dispositivo interno e i dati vengono persi.</span><span class="sxs-lookup"><span data-stu-id="679b3-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="679b3-157">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="679b3-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="679b3-158">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="679b3-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="679b3-159">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="679b3-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="679b3-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="679b3-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="679b3-161">Numero di reimpostazioni software rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="679b3-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="679b3-162">Un ripristino soft non cancella completamente i dati e lo stato corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="679b3-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="679b3-163">La semantica esatta dipende dal dispositivo e dai protocolli e dai meccanismi usati per comunicare con esso.</span><span class="sxs-lookup"><span data-stu-id="679b3-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="679b3-164">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="679b3-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="679b3-165">**SCSIRetries**</span><span class="sxs-lookup"><span data-stu-id="679b3-165">**SCSIRetries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="679b3-166">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="679b3-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="679b3-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="679b3-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="679b3-168">Numero di tentativi SCSI che si sono verificati dopo l'ultimo ripristino hardware o soft correlato al dispositivo controllato.</span><span class="sxs-lookup"><span data-stu-id="679b3-168">Number of SCSI retries that have occurred since the last hard or soft reset related to the controlled device.</span></span> <span data-ttu-id="679b3-169">L'ora dell'ultima reimpostazione è indicata nella proprietà **TimeOfDeviceReset (ora** , ereditata dall'associazione [**CIM \_ ControlledBy**](cim-controlledby.md) .</span><span class="sxs-lookup"><span data-stu-id="679b3-169">The time of the last reset is indicated in the **TimeOfDeviceReset** property, inherited from the [**CIM\_ControlledBy**](cim-controlledby.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="679b3-170">**SCSITimeouts**</span><span class="sxs-lookup"><span data-stu-id="679b3-170">**SCSITimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="679b3-171">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="679b3-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="679b3-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="679b3-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="679b3-173">Numero di timeout SCSI che si sono verificati dopo l'ultimo ripristino hardware o soft correlato al dispositivo controllato.</span><span class="sxs-lookup"><span data-stu-id="679b3-173">Number of SCSI time-outs that occurred since last hard or soft reset related to the controlled device.</span></span> <span data-ttu-id="679b3-174">L'ora dell'ultima reimpostazione è indicata nella proprietà **TimeOfDeviceReset (ora** , ereditata dall'associazione [**CIM \_ ControlledBy**](cim-controlledby.md) .</span><span class="sxs-lookup"><span data-stu-id="679b3-174">The time of the last reset is indicated in the **TimeOfDeviceReset** property, inherited from the [**CIM\_ControlledBy**](cim-controlledby.md) association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="679b3-175">Commenti</span><span class="sxs-lookup"><span data-stu-id="679b3-175">Remarks</span></span>

<span data-ttu-id="679b3-176">La classe **CIM \_ SCSIInterface** è derivata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="679b3-176">The **CIM\_SCSIInterface** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="679b3-177">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="679b3-177">WMI does not implement this class.</span></span>

<span data-ttu-id="679b3-178">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="679b3-178">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="679b3-179">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="679b3-179">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="679b3-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="679b3-180">Requirements</span></span>



| <span data-ttu-id="679b3-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="679b3-181">Requirement</span></span> | <span data-ttu-id="679b3-182">Valore</span><span class="sxs-lookup"><span data-stu-id="679b3-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="679b3-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="679b3-183">Minimum supported client</span></span><br/> | <span data-ttu-id="679b3-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="679b3-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="679b3-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="679b3-185">Minimum supported server</span></span><br/> | <span data-ttu-id="679b3-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="679b3-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="679b3-187">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="679b3-187">Namespace</span></span><br/>                | <span data-ttu-id="679b3-188">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="679b3-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="679b3-189">MOF</span><span class="sxs-lookup"><span data-stu-id="679b3-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="679b3-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="679b3-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="679b3-191">DLL</span><span class="sxs-lookup"><span data-stu-id="679b3-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="679b3-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="679b3-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="679b3-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="679b3-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="679b3-194">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="679b3-194">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 


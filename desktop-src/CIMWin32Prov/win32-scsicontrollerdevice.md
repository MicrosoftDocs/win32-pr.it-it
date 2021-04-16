---
description: La \_ classe WMI dell'associazione SCSIControllerDevice Win32 mette in correlazione un controller small computer System Interface (SCSI) e il dispositivo logico (unità disco) connesso.
ms.assetid: 0334829c-3625-4acf-8ef3-da934c51e9bf
ms.tgt_platform: multiple
title: Classe Win32_SCSIControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SCSIControllerDevice
- Win32_SCSIControllerDevice.NegotiatedDataWidth
- Win32_SCSIControllerDevice.NegotiatedSpeed
- Win32_SCSIControllerDevice.AccessState
- Win32_SCSIControllerDevice.NumberOfHardResets
- Win32_SCSIControllerDevice.NumberOfSoftResets
- Win32_SCSIControllerDevice.Antecedent
- Win32_SCSIControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a3189f9d9b75321df7c69214e68779864953f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524258"
---
# <a name="win32_scsicontrollerdevice-class"></a><span data-ttu-id="03853-103">Win32 \_ SCSIControllerDevice (classe)</span><span class="sxs-lookup"><span data-stu-id="03853-103">Win32\_SCSIControllerDevice class</span></span>

<span data-ttu-id="03853-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SCSIControllerDevice Win32** mette in correlazione un controller small computer System Interface (SCSI) e il dispositivo logico (unità disco) connesso.</span><span class="sxs-lookup"><span data-stu-id="03853-104">The **Win32\_SCSIControllerDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a small computer system interface (SCSI) controller and the logical device (disk drive) connected to it.</span></span>

<span data-ttu-id="03853-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="03853-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="03853-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="03853-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="03853-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03853-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{CC0F48D2-C847-11d2-911E-0060081A46FD}"), AMENDMENT]
class Win32_SCSIControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_SCSIController REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="03853-108">Members</span><span class="sxs-lookup"><span data-stu-id="03853-108">Members</span></span>

<span data-ttu-id="03853-109">La classe **Win32 \_ SCSIControllerDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="03853-109">The **Win32\_SCSIControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="03853-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03853-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03853-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03853-111">Properties</span></span>

<span data-ttu-id="03853-112">La classe **Win32 \_ SCSIControllerDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="03853-112">The **Win32\_SCSIControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03853-113">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="03853-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03853-114">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03853-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03853-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03853-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03853-116">Indica se il controller sta attivando o accedendo attivamente al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03853-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="03853-117">Queste informazioni sono necessarie quando è possibile eseguire il comando o l'accesso a un dispositivo logico tramite più controller.</span><span class="sxs-lookup"><span data-stu-id="03853-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="03853-118">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="03853-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03853-119">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="03853-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="03853-120">**Attivo** (1)</span><span class="sxs-lookup"><span data-stu-id="03853-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="03853-121">**Inattivo** (2)</span><span class="sxs-lookup"><span data-stu-id="03853-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03853-122">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="03853-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03853-123">Tipo di dati: **Win32 \_ controller SCSI**</span><span class="sxs-lookup"><span data-stu-id="03853-123">Data type: **Win32\_SCSIController**</span></span>
</dt> <dt>

<span data-ttu-id="03853-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03853-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03853-125">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| CIM \_ Win32 controller SCSI")</span><span class="sxs-lookup"><span data-stu-id="03853-125">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|Win32\_SCSIController")</span></span>
</dt> </dl>

<span data-ttu-id="03853-126">Il riferimento all'attività precedente [**Win32 \_ controller SCSI**](win32-scsicontroller.md) rappresenta il controller SCSI associato a questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03853-126">The [**Win32\_SCSIController**](win32-scsicontroller.md) antecedent reference represents the SCSI controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="03853-127">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="03853-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03853-128">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="03853-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="03853-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03853-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03853-130">Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("dipendente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="03853-130">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="03853-131">Il riferimento dipendente [**CIM \_ LogicalDevice**](cim-logicaldevice.md) rappresenta il dispositivo logico connesso al controller SCSI.</span><span class="sxs-lookup"><span data-stu-id="03853-131">The [**CIM\_LogicalDevice**](cim-logicaldevice.md) dependent reference represents the logical device connected to the SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="03853-132">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="03853-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03853-133">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03853-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03853-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03853-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03853-135">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("bits")</span><span class="sxs-lookup"><span data-stu-id="03853-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="03853-136">Quando sono possibili più larghezze di dati del bus o della connessione, questa proprietà definisce quella in uso tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="03853-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="03853-137">La larghezza dei dati è specificata in bit.</span><span class="sxs-lookup"><span data-stu-id="03853-137">Data width is specified in bits.</span></span> <span data-ttu-id="03853-138">Se la larghezza dei dati non è negoziata o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="03853-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="03853-139">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="03853-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="03853-140">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="03853-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03853-141">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="03853-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="03853-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03853-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03853-143">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="03853-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="03853-144">Quando sono possibili più velocità di connessione o bus, questa proprietà definisce quella usata tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="03853-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="03853-145">La velocità è specificata in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="03853-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="03853-146">Se le velocità di connessione o di bus non vengono negoziate o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="03853-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="03853-147">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="03853-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="03853-148">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="03853-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="03853-149">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="03853-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03853-150">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03853-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03853-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03853-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03853-152">Numero di reimpostazioni rigide rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="03853-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="03853-153">Una reimpostazione hardware restituisce il dispositivo alla relativa inizializzazione o allo stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="03853-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="03853-154">Tutte le informazioni sullo stato del dispositivo interno e i dati vengono persi.</span><span class="sxs-lookup"><span data-stu-id="03853-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="03853-155">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="03853-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="03853-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="03853-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03853-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03853-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03853-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03853-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03853-159">Numero di reimpostazioni software rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="03853-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="03853-160">Un ripristino soft non cancella completamente i dati e lo stato corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03853-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="03853-161">La semantica esatta dipende dal dispositivo e dai protocolli e dai meccanismi usati per comunicare con esso.</span><span class="sxs-lookup"><span data-stu-id="03853-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="03853-162">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="03853-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03853-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="03853-163">Remarks</span></span>

<span data-ttu-id="03853-164">La classe **Win32 \_ SCSIControllerDevice** è derivata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="03853-164">The **Win32\_SCSIControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03853-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03853-165">Requirements</span></span>



| <span data-ttu-id="03853-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="03853-166">Requirement</span></span> | <span data-ttu-id="03853-167">Valore</span><span class="sxs-lookup"><span data-stu-id="03853-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03853-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03853-168">Minimum supported client</span></span><br/> | <span data-ttu-id="03853-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03853-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03853-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03853-170">Minimum supported server</span></span><br/> | <span data-ttu-id="03853-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03853-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03853-172">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="03853-172">Namespace</span></span><br/>                | <span data-ttu-id="03853-173">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="03853-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="03853-174">MOF</span><span class="sxs-lookup"><span data-stu-id="03853-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03853-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03853-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="03853-176">DLL</span><span class="sxs-lookup"><span data-stu-id="03853-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03853-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03853-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03853-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03853-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03853-179">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="03853-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="03853-180">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="03853-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

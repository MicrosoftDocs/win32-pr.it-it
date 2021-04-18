---
description: La \_ classe WMI dell'associazione USBControllerDevice Win32 mette in correlazione un controller USB (Universal Serial Bus) e l' \_ istanza CIM LogicalDevice connessa.
ms.assetid: a0c64984-9116-4cb8-86e0-38c897cb7119
ms.tgt_platform: multiple
title: Classe Win32_USBControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_USBControllerDevice
- Win32_USBControllerDevice.NegotiatedDataWidth
- Win32_USBControllerDevice.NegotiatedSpeed
- Win32_USBControllerDevice.AccessState
- Win32_USBControllerDevice.NumberOfHardResets
- Win32_USBControllerDevice.NumberOfSoftResets
- Win32_USBControllerDevice.Antecedent
- Win32_USBControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9bf72c92a4ae23ac7750cdd52914e86f5dbcdd01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304574"
---
# <a name="win32_usbcontrollerdevice-class"></a><span data-ttu-id="48df7-103">Win32 \_ USBControllerDevice (classe)</span><span class="sxs-lookup"><span data-stu-id="48df7-103">Win32\_USBControllerDevice class</span></span>

<span data-ttu-id="48df7-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ USBControllerDevice Win32** mette in correlazione un controller USB (Universal Serial Bus) e l'istanza [**CIM \_ LogicalDevice**](cim-logicaldevice.md) connessa.</span><span class="sxs-lookup"><span data-stu-id="48df7-104">The **Win32\_USBControllerDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a universal serial bus (USB) controller and the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance connected to it.</span></span>

<span data-ttu-id="48df7-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="48df7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="48df7-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="48df7-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="48df7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48df7-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{DE57D792-A032-11D2-90F0-0060081A46FD}"), AMENDMENT]
class Win32_USBControllerDevice : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBController REF Antecedent;
  CIM_LogicalDevice REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="48df7-108">Members</span><span class="sxs-lookup"><span data-stu-id="48df7-108">Members</span></span>

<span data-ttu-id="48df7-109">La classe **Win32 \_ USBControllerDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="48df7-109">The **Win32\_USBControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="48df7-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="48df7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48df7-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="48df7-111">Properties</span></span>

<span data-ttu-id="48df7-112">La classe **Win32 \_ USBControllerDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="48df7-112">The **Win32\_USBControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48df7-113">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="48df7-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48df7-114">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48df7-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48df7-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48df7-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48df7-116">Indica se il controller sta attivando o accedendo attivamente al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48df7-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="48df7-117">Queste informazioni sono necessarie quando è possibile eseguire il comando o l'accesso a un dispositivo logico tramite più controller.</span><span class="sxs-lookup"><span data-stu-id="48df7-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="48df7-118">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="48df7-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48df7-119">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="48df7-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="48df7-120">**Attivo** (1)</span><span class="sxs-lookup"><span data-stu-id="48df7-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="48df7-121">**Inattivo** (2)</span><span class="sxs-lookup"><span data-stu-id="48df7-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="48df7-122">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="48df7-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48df7-123">Tipo di dati: **CIM \_ USBController**</span><span class="sxs-lookup"><span data-stu-id="48df7-123">Data type: **CIM\_USBController**</span></span>
</dt> <dt>

<span data-ttu-id="48df7-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48df7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48df7-125">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| CIM \_ CIM USBController")</span><span class="sxs-lookup"><span data-stu-id="48df7-125">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_USBController")</span></span>
</dt> </dl>

<span data-ttu-id="48df7-126">Un [**\_ USBController CIM**](cim-usbcontroller.md) che rappresenta il controller USB (Universal Serial Bus) associato a questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48df7-126">A [**CIM\_USBController**](cim-usbcontroller.md) representing the Universal Serial Bus (USB) controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="48df7-127">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="48df7-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48df7-128">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="48df7-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="48df7-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48df7-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48df7-130">Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("dipendente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="48df7-130">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="48df7-131">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive il dispositivo logico connesso al controller USB (Universal Serial Bus).</span><span class="sxs-lookup"><span data-stu-id="48df7-131">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) describing the logical device connected to the Universal Serial Bus (USB) controller.</span></span>

</dd> <dt>

<span data-ttu-id="48df7-132">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="48df7-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48df7-133">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48df7-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48df7-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48df7-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48df7-135">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("bits")</span><span class="sxs-lookup"><span data-stu-id="48df7-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="48df7-136">Quando sono possibili più larghezze di dati del bus o della connessione, questa proprietà definisce quella in uso tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="48df7-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="48df7-137">La larghezza dei dati è specificata in bit.</span><span class="sxs-lookup"><span data-stu-id="48df7-137">Data width is specified in bits.</span></span> <span data-ttu-id="48df7-138">Se la larghezza dei dati non è negoziata o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="48df7-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="48df7-139">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="48df7-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="48df7-140">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="48df7-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48df7-141">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48df7-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48df7-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48df7-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48df7-143">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="48df7-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="48df7-144">Quando sono possibili più velocità di connessione o bus, questa proprietà definisce quella usata tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="48df7-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="48df7-145">La velocità è specificata in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="48df7-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="48df7-146">Se le velocità di connessione o di bus non vengono negoziate o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="48df7-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="48df7-147">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="48df7-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="48df7-148">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="48df7-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="48df7-149">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="48df7-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48df7-150">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48df7-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48df7-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48df7-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48df7-152">Numero di reimpostazioni rigide rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="48df7-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="48df7-153">Una reimpostazione hardware restituisce il dispositivo alla relativa inizializzazione o allo stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="48df7-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="48df7-154">Tutte le informazioni sullo stato del dispositivo interno e i dati vengono persi.</span><span class="sxs-lookup"><span data-stu-id="48df7-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="48df7-155">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="48df7-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="48df7-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="48df7-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48df7-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48df7-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="48df7-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48df7-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48df7-159">Numero di reimpostazioni software rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="48df7-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="48df7-160">Un ripristino soft non cancella completamente i dati e lo stato corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48df7-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="48df7-161">La semantica esatta dipende dal dispositivo e dai protocolli e dai meccanismi usati per comunicare con esso.</span><span class="sxs-lookup"><span data-stu-id="48df7-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="48df7-162">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="48df7-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48df7-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="48df7-163">Remarks</span></span>

<span data-ttu-id="48df7-164">La classe **Win32 \_ USBControllerDevice** è derivata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="48df7-164">The **Win32\_USBControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="48df7-165">Per una discussione sull'uso di, vedere l'articolo [visualizzazione dei dispositivi USB con WMI](https://devblogs.microsoft.com/powershell/displaying-usb-devices-using-wmi/) .</span><span class="sxs-lookup"><span data-stu-id="48df7-165">For a discussion on using, see the [Displaying USB Devices using WMI](https://devblogs.microsoft.com/powershell/displaying-usb-devices-using-wmi/) blog article.</span></span> <span data-ttu-id="48df7-166">Per informazioni sull'uso delle classi di associazione, vedere l'articolo relativo all'uso delle classi di [associazione WMI in PowerShell in Get-USB](https://devblogs.microsoft.com/powershell/get-usb-using-wmi-association-classes-in-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="48df7-166">For a discussion of using association classes, see the [Get-USB – Using WMI Association Classes in PowerShell](https://devblogs.microsoft.com/powershell/get-usb-using-wmi-association-classes-in-powershell/) article.</span></span>

## <a name="examples"></a><span data-ttu-id="48df7-167">Esempio</span><span class="sxs-lookup"><span data-stu-id="48df7-167">Examples</span></span>

<span data-ttu-id="48df7-168">Nell'esempio di PowerShell seguente viene recuperato il dispositivo logico dipendente e vengono visualizzate le informazioni rilevanti.</span><span class="sxs-lookup"><span data-stu-id="48df7-168">The following PowerShell example retrieves the dependent logical device and displays the relevant information.</span></span>


```PowerShell
gwmi Win32_USBControllerDevice |%{[wmi]($_.Dependent)} | Sort Manufacturer,Description,DeviceID | Ft -GroupBy Manufacturer Description,Service,DeviceID
```



## <a name="requirements"></a><span data-ttu-id="48df7-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48df7-169">Requirements</span></span>



| <span data-ttu-id="48df7-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="48df7-170">Requirement</span></span> | <span data-ttu-id="48df7-171">Valore</span><span class="sxs-lookup"><span data-stu-id="48df7-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48df7-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48df7-172">Minimum supported client</span></span><br/> | <span data-ttu-id="48df7-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48df7-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48df7-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48df7-174">Minimum supported server</span></span><br/> | <span data-ttu-id="48df7-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48df7-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48df7-176">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="48df7-176">Namespace</span></span><br/>                | <span data-ttu-id="48df7-177">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="48df7-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="48df7-178">MOF</span><span class="sxs-lookup"><span data-stu-id="48df7-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48df7-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48df7-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="48df7-180">DLL</span><span class="sxs-lookup"><span data-stu-id="48df7-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48df7-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48df7-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48df7-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48df7-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48df7-183">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="48df7-183">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="48df7-184">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="48df7-184">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 

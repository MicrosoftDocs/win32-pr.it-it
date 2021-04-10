---
description: La \_ classe WMI dell'associazione 1394ControllerDevice Win32 mette in correlazione il controller di bus seriale (IEEE 1394 FireWire) ad alta velocità e l' \_ istanza CIM LogicalDevice connessa.
ms.assetid: 327fbced-4637-4402-a06f-6ac352da920c
ms.tgt_platform: multiple
title: Classe Win32_1394ControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_1394ControllerDevice
- Win32_1394ControllerDevice.NegotiatedDataWidth
- Win32_1394ControllerDevice.NegotiatedSpeed
- Win32_1394ControllerDevice.AccessState
- Win32_1394ControllerDevice.NumberOfHardResets
- Win32_1394ControllerDevice.NumberOfSoftResets
- Win32_1394ControllerDevice.Antecedent
- Win32_1394ControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: af3a54db81a388184da148cd411895ebb910de7d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878238"
---
# <a name="win32_1394controllerdevice-class"></a><span data-ttu-id="efeb5-103">Win32 \_ 1394ControllerDevice (classe)</span><span class="sxs-lookup"><span data-stu-id="efeb5-103">Win32\_1394ControllerDevice class</span></span>

<span data-ttu-id="efeb5-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ 1394ControllerDevice Win32** mette in correlazione il controller di bus seriale (IEEE 1394 FireWire) ad alta velocità e l'istanza [**CIM \_ LogicalDevice**](cim-logicaldevice.md) connessa.</span><span class="sxs-lookup"><span data-stu-id="efeb5-104">The **Win32\_1394ControllerDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates the high-speed serial bus (IEEE 1394 Firewire) Controller and the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance connected to it.</span></span> <span data-ttu-id="efeb5-105">Questo bus seriale offre una connettività migliorata per un'ampia gamma di dispositivi, inclusi i componenti audio o video del consumer, le periferiche di archiviazione, altri computer e dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="efeb5-105">This serial bus provides enhanced connectivity for a wide range of devices, including consumer audio or video components, storage peripherals, other computers, and portable devices.</span></span> <span data-ttu-id="efeb5-106">IEEE 1394 è stato adottato dal settore dell'elettronica consumer e fornisce un'interfaccia di espansione compatibile con Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="efeb5-106">IEEE 1394 has been adopted by the consumer electronics industry and provides a Plug and Play-compatible expansion interface.</span></span>

<span data-ttu-id="efeb5-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="efeb5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="efeb5-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="efeb5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="efeb5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efeb5-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8835CFC9-BAEF-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_1394ControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_1394Controller REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="efeb5-110">Members</span><span class="sxs-lookup"><span data-stu-id="efeb5-110">Members</span></span>

<span data-ttu-id="efeb5-111">La classe **Win32 \_ 1394ControllerDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="efeb5-111">The **Win32\_1394ControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="efeb5-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="efeb5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="efeb5-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="efeb5-113">Properties</span></span>

<span data-ttu-id="efeb5-114">La classe **Win32 \_ 1394ControllerDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="efeb5-114">The **Win32\_1394ControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="efeb5-115">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="efeb5-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efeb5-116">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="efeb5-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="efeb5-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efeb5-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efeb5-118">Indica se il controller sta attivando o accedendo attivamente al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efeb5-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="efeb5-119">Queste informazioni sono necessarie quando è possibile eseguire il comando o l'accesso a un dispositivo logico tramite più controller.</span><span class="sxs-lookup"><span data-stu-id="efeb5-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="efeb5-120">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="efeb5-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="efeb5-121">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="efeb5-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="efeb5-122">**Attivo** (1)</span><span class="sxs-lookup"><span data-stu-id="efeb5-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="efeb5-123">**Inattivo** (2)</span><span class="sxs-lookup"><span data-stu-id="efeb5-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="efeb5-124">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="efeb5-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efeb5-125">Tipo di dati: **Win32 \_ 1394Controller**</span><span class="sxs-lookup"><span data-stu-id="efeb5-125">Data type: **Win32\_1394Controller**</span></span>
</dt> <dt>

<span data-ttu-id="efeb5-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efeb5-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efeb5-127">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| WMI \_ Win32 1394Controller")</span><span class="sxs-lookup"><span data-stu-id="efeb5-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_1394Controller")</span></span>
</dt> </dl>

<span data-ttu-id="efeb5-128">Il riferimento all'attività \_ precedente Win32 1394Controller rappresenta il controller 1394 associato a questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efeb5-128">The Win32\_1394Controller antecedent reference represents the 1394 controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="efeb5-129">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="efeb5-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efeb5-130">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="efeb5-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="efeb5-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efeb5-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efeb5-132">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="efeb5-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="efeb5-133">Il \_ riferimento dipendente CIM LogicalDevice rappresenta il \_ LogicalDevice CIM connesso al controller 1394.</span><span class="sxs-lookup"><span data-stu-id="efeb5-133">The CIM\_LogicalDevice dependent reference represents the CIM\_LogicalDevice connected to the 1394 controller.</span></span>

</dd> <dt>

<span data-ttu-id="efeb5-134">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="efeb5-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efeb5-135">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efeb5-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efeb5-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efeb5-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efeb5-137">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="efeb5-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="efeb5-138">Quando sono possibili più larghezze di dati del bus o della connessione, questa proprietà definisce quella in uso tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="efeb5-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="efeb5-139">La larghezza dei dati è specificata in bit.</span><span class="sxs-lookup"><span data-stu-id="efeb5-139">Data width is specified in bits.</span></span> <span data-ttu-id="efeb5-140">Se la larghezza dei dati non è negoziata o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="efeb5-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="efeb5-141">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="efeb5-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="efeb5-142">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="efeb5-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efeb5-143">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="efeb5-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="efeb5-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efeb5-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efeb5-145">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="efeb5-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="efeb5-146">Quando sono possibili più velocità di connessione o bus, questa proprietà definisce quella usata tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="efeb5-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="efeb5-147">La velocità è specificata in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="efeb5-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="efeb5-148">Se le velocità di connessione o di bus non vengono negoziate o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="efeb5-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="efeb5-149">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="efeb5-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="efeb5-150">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="efeb5-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="efeb5-151">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="efeb5-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efeb5-152">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efeb5-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efeb5-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efeb5-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efeb5-154">Numero di reimpostazioni rigide rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="efeb5-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="efeb5-155">Una reimpostazione hardware restituisce il dispositivo alla relativa inizializzazione o allo stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="efeb5-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="efeb5-156">Tutte le informazioni sullo stato del dispositivo interno e i dati vengono persi.</span><span class="sxs-lookup"><span data-stu-id="efeb5-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="efeb5-157">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="efeb5-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="efeb5-158">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="efeb5-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efeb5-159">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efeb5-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efeb5-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="efeb5-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efeb5-161">Numero di reimpostazioni software rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="efeb5-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="efeb5-162">Un ripristino soft non cancella completamente i dati e lo stato corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efeb5-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="efeb5-163">La semantica esatta dipende dal dispositivo e dai protocolli e dai meccanismi usati per comunicare con esso.</span><span class="sxs-lookup"><span data-stu-id="efeb5-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="efeb5-164">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="efeb5-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="efeb5-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="efeb5-165">Remarks</span></span>

<span data-ttu-id="efeb5-166">La classe **Win32 \_ 1394ControllerDevice** è derivata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="efeb5-166">The **Win32\_1394ControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="examples"></a><span data-ttu-id="efeb5-167">Esempio</span><span class="sxs-lookup"><span data-stu-id="efeb5-167">Examples</span></span>

<span data-ttu-id="efeb5-168">L'esempio di codice PowerShell seguente recupera le informazioni sul dispositivo del controller 1394.</span><span class="sxs-lookup"><span data-stu-id="efeb5-168">The following PowerShell code sample retrieves 1394 controller device information.</span></span>


```PowerShell
# Helper function to return AccessState

function get-WmiAccessState {
param ([uint16] $char)

# parse and return values

If ($char -le 2 -and $char -ge 0) {

switch ($char) {
0 {"00-Reserved"}
1 {"01-Reserved"}
2 {"02-Unknown"}
}
}

Else {
"$char - unknown value"
}
}

# Get 1394 Controller Device information from WMI
$1394Cont = Get-WMIObject Win32_1394ControllerDevice

# Display Details
"Win32_1394ControllerDevice WMI Information"
"=========================================="

foreach ($device in $1394Cont) {

"Device Characteristics - Device {0}" -f ++$i

"Access State : {0}" -f (Get-WmiAccessState($ch))
"Antecedent : {0}" -f $device.Antecedent
"Negotiated Data Width : {0}" -f $device.NegotiatedDataWidth
"Negotiated Speed : {0}" -f $device.NegotiatedSpeed
"Number of Hard Resets : {0}" -f $device.NumberofHardResets
"Number of Soft Resets : {0}" -f $device.NumberofSoftResets
} 
```



<span data-ttu-id="efeb5-169">Nell'esempio di codice precedente vengono restituite le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="efeb5-169">The previous code sample returns the following information:</span></span>

``` syntax
# Win32_1394ControllerDevice WMI Information

Device Characteristics -Device 1
Access State : 00-Reserved
Antecedent : \\UK0N055\root\CIMV2:Win32_1394Controller.DeviceID="PCI\\VEN_1217&DEV_00F7&SUBSYS_01CC1028
&REV_02\\4&2FE911E8&0&0CF0"
Negotiated Data Width :
Negotiated Speed :
Number of Hard Resets :
Number of Soft Resets :
```

## <a name="requirements"></a><span data-ttu-id="efeb5-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efeb5-170">Requirements</span></span>



| <span data-ttu-id="efeb5-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="efeb5-171">Requirement</span></span> | <span data-ttu-id="efeb5-172">Valore</span><span class="sxs-lookup"><span data-stu-id="efeb5-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="efeb5-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efeb5-173">Minimum supported client</span></span><br/> | <span data-ttu-id="efeb5-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="efeb5-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="efeb5-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efeb5-175">Minimum supported server</span></span><br/> | <span data-ttu-id="efeb5-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="efeb5-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="efeb5-177">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="efeb5-177">Namespace</span></span><br/>                | <span data-ttu-id="efeb5-178">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="efeb5-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="efeb5-179">MOF</span><span class="sxs-lookup"><span data-stu-id="efeb5-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efeb5-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="efeb5-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="efeb5-181">DLL</span><span class="sxs-lookup"><span data-stu-id="efeb5-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efeb5-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efeb5-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efeb5-183">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efeb5-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efeb5-184">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="efeb5-184">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="efeb5-185">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="efeb5-185">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 


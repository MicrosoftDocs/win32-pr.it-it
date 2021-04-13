---
description: La \_ classe WMI dell'associazione IDEControllerDevice Win32 mette in correlazione un controller IDE (Integrated Drive Electronics) e il dispositivo logico connesso, ad esempio, un'unità disco.
ms.assetid: 1b0a551c-d836-4147-91ed-a0a7d97f4a5b
ms.tgt_platform: multiple
title: Classe Win32_IDEControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_IDEControllerDevice
- Win32_IDEControllerDevice.NegotiatedDataWidth
- Win32_IDEControllerDevice.NegotiatedSpeed
- Win32_IDEControllerDevice.AccessState
- Win32_IDEControllerDevice.NumberOfHardResets
- Win32_IDEControllerDevice.NumberOfSoftResets
- Win32_IDEControllerDevice.Antecedent
- Win32_IDEControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc690aadd442d656132b2d9e4539cc27961c3ef9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401498"
---
# <a name="win32_idecontrollerdevice-class"></a><span data-ttu-id="e017d-103">Win32 \_ IDEControllerDevice (classe)</span><span class="sxs-lookup"><span data-stu-id="e017d-103">Win32\_IDEControllerDevice class</span></span>

<span data-ttu-id="e017d-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ IDEControllerDevice Win32** mette in correlazione un controller IDE (Integrated Drive Electronics) e il dispositivo logico connesso, ad esempio, un'unità disco.</span><span class="sxs-lookup"><span data-stu-id="e017d-104">The **Win32\_IDEControllerDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates an Integrated Drive Electronics (IDE) controller and the logical device connected to, for example, a disk drive.</span></span>

<span data-ttu-id="e017d-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e017d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e017d-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="e017d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e017d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e017d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{5BC42B62-C7A1-11d2-911D-0060081A46FD}"), AMENDMENT]
class Win32_IDEControllerDevice : CIM_ControlledBy
{
  uint32                  NegotiatedDataWidth;
  uint64                  NegotiatedSpeed;
  uint16                  AccessState;
  uint32                  NumberOfHardResets;
  uint32                  NumberOfSoftResets;
  Win32_IDEController REF Antecedent;
  CIM_LogicalDevice   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e017d-108">Members</span><span class="sxs-lookup"><span data-stu-id="e017d-108">Members</span></span>

<span data-ttu-id="e017d-109">La classe **Win32 \_ IDEControllerDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e017d-109">The **Win32\_IDEControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="e017d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e017d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e017d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e017d-111">Properties</span></span>

<span data-ttu-id="e017d-112">La classe **Win32 \_ IDEControllerDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e017d-112">The **Win32\_IDEControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e017d-113">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="e017d-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e017d-114">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e017d-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e017d-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e017d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e017d-116">Indica se il controller sta attivando o accedendo attivamente al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e017d-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="e017d-117">Queste informazioni sono necessarie quando è possibile eseguire il comando o l'accesso a un dispositivo logico tramite più controller.</span><span class="sxs-lookup"><span data-stu-id="e017d-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="e017d-118">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="e017d-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e017d-119">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e017d-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="e017d-120">**Attivo** (1)</span><span class="sxs-lookup"><span data-stu-id="e017d-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="e017d-121">**Inattivo** (2)</span><span class="sxs-lookup"><span data-stu-id="e017d-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e017d-122">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="e017d-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e017d-123">Tipo di dati: **Win32 \_ IDECONTROLLER**</span><span class="sxs-lookup"><span data-stu-id="e017d-123">Data type: **Win32\_IDEController**</span></span>
</dt> <dt>

<span data-ttu-id="e017d-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e017d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e017d-125">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| CIM \_ Win32 IDECONTROLLER")</span><span class="sxs-lookup"><span data-stu-id="e017d-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|Win32\_IDEController")</span></span>
</dt> </dl>

<span data-ttu-id="e017d-126">[**\_ IDECONTROLLER Win32**](win32-idecontroller.md) che rappresenta il controller IDE associato a questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e017d-126">A [**Win32\_IDEController**](win32-idecontroller.md) that represents the IDE controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="e017d-127">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="e017d-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e017d-128">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="e017d-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="e017d-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e017d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e017d-130">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="e017d-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="e017d-131">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che rappresenta il dispositivo logico connesso al controller IDE.</span><span class="sxs-lookup"><span data-stu-id="e017d-131">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the logical device connected to the IDE controller.</span></span>

</dd> <dt>

<span data-ttu-id="e017d-132">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="e017d-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e017d-133">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e017d-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e017d-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e017d-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e017d-135">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span><span class="sxs-lookup"><span data-stu-id="e017d-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="e017d-136">Quando sono possibili più larghezze di dati del bus o della connessione, questa proprietà definisce quella in uso tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="e017d-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="e017d-137">La larghezza dei dati è specificata in bit.</span><span class="sxs-lookup"><span data-stu-id="e017d-137">Data width is specified in bits.</span></span> <span data-ttu-id="e017d-138">Se la larghezza dei dati non è negoziata o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e017d-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="e017d-139">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="e017d-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="e017d-140">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="e017d-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e017d-141">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e017d-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e017d-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e017d-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e017d-143">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="e017d-143">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="e017d-144">Quando sono possibili più velocità di connessione o bus, questa proprietà definisce quella usata tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="e017d-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="e017d-145">La velocità è specificata in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="e017d-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="e017d-146">Se le velocità di connessione o di bus non vengono negoziate o se queste informazioni non sono disponibili o sono importanti per la gestione dei dispositivi, la proprietà deve essere impostata su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e017d-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="e017d-147">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e017d-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="e017d-148">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="e017d-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="e017d-149">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="e017d-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e017d-150">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e017d-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e017d-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e017d-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e017d-152">Numero di reimpostazioni rigide rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="e017d-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="e017d-153">Una reimpostazione hardware restituisce il dispositivo alla relativa inizializzazione o allo stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="e017d-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="e017d-154">Tutte le informazioni sullo stato del dispositivo interno e i dati vengono persi.</span><span class="sxs-lookup"><span data-stu-id="e017d-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="e017d-155">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="e017d-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="e017d-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="e017d-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e017d-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e017d-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e017d-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e017d-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e017d-159">Numero di reimpostazioni software rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="e017d-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="e017d-160">Un ripristino soft non cancella completamente i dati e lo stato corrente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e017d-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="e017d-161">La semantica esatta dipende dal dispositivo e dai protocolli e dai meccanismi usati per comunicare con esso.</span><span class="sxs-lookup"><span data-stu-id="e017d-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="e017d-162">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="e017d-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e017d-163">Commenti</span><span class="sxs-lookup"><span data-stu-id="e017d-163">Remarks</span></span>

<span data-ttu-id="e017d-164">La classe **Win32 \_ IDEControllerDevice** è derivata da [**CIM \_ ControlledBy**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="e017d-164">The **Win32\_IDEControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e017d-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e017d-165">Requirements</span></span>



| <span data-ttu-id="e017d-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="e017d-166">Requirement</span></span> | <span data-ttu-id="e017d-167">Valore</span><span class="sxs-lookup"><span data-stu-id="e017d-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e017d-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e017d-168">Minimum supported client</span></span><br/> | <span data-ttu-id="e017d-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e017d-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e017d-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e017d-170">Minimum supported server</span></span><br/> | <span data-ttu-id="e017d-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e017d-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e017d-172">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e017d-172">Namespace</span></span><br/>                | <span data-ttu-id="e017d-173">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e017d-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e017d-174">MOF</span><span class="sxs-lookup"><span data-stu-id="e017d-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e017d-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e017d-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e017d-176">DLL</span><span class="sxs-lookup"><span data-stu-id="e017d-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e017d-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e017d-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e017d-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e017d-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e017d-179">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="e017d-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="e017d-180">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="e017d-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 


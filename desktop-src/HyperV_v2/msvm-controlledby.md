---
description: Associa un dispositivo di archiviazione al controller di archiviazione proprietario del dispositivo.
ms.assetid: 3DE05EDC-C54A-4C3C-9057-4418246037D5
title: Classe Msvm_ControlledBy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ControlledBy
- Msvm_ControlledBy.NegotiatedSpeed
- Msvm_ControlledBy.NegotiatedDataWidth
- Msvm_ControlledBy.Antecedent
- Msvm_ControlledBy.Dependent
- Msvm_ControlledBy.AccessState
- Msvm_ControlledBy.TimeOfDeviceReset
- Msvm_ControlledBy.NumberOfHardResets
- Msvm_ControlledBy.NumberOfSoftResets
- Msvm_ControlledBy.DeviceNumber
- Msvm_ControlledBy.AccessMode
- Msvm_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7986ffb842f7a1a104a0a8d846c1b6ee47a21523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317194"
---
# <a name="msvm_controlledby-class"></a><span data-ttu-id="d15dc-103">\_Classe MSVM ControlledBy</span><span class="sxs-lookup"><span data-stu-id="d15dc-103">Msvm\_ControlledBy class</span></span>

<span data-ttu-id="d15dc-104">Associa un dispositivo di archiviazione al controller di archiviazione proprietario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d15dc-104">Associates a storage device with the storage controller that owns the device.</span></span> <span data-ttu-id="d15dc-105">Questa associazione viene utilizzata con i controller IDE e floppy.</span><span class="sxs-lookup"><span data-stu-id="d15dc-105">This association is used with both IDE and floppy controllers.</span></span>

<span data-ttu-id="d15dc-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d15dc-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d15dc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d15dc-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ControlledBy : CIM_ControlledBy
{
  uint64                NegotiatedSpeed = 0;
  uint32                NegotiatedDataWidth = 0;
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState = 1;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode = 2;
  uint16                AccessPriority = 0;
};
```

## <a name="members"></a><span data-ttu-id="d15dc-108">Members</span><span class="sxs-lookup"><span data-stu-id="d15dc-108">Members</span></span>

<span data-ttu-id="d15dc-109">La **classe \_ ControlledBy di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d15dc-109">The **Msvm\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="d15dc-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d15dc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d15dc-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d15dc-111">Properties</span></span>

<span data-ttu-id="d15dc-112">La **classe \_ ControlledBy di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d15dc-112">The **Msvm\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d15dc-113">**AccessMode**</span><span class="sxs-lookup"><span data-stu-id="d15dc-113">**AccessMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15dc-114">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d15dc-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d15dc-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d15dc-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15dc-116">Accessibilità del dispositivo tramite il controller precedente.</span><span class="sxs-lookup"><span data-stu-id="d15dc-116">The accessibility of the device through the antecedent controller.</span></span> <span data-ttu-id="d15dc-117">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)ed è sempre impostata su 2 (lettura/scrittura).</span><span class="sxs-lookup"><span data-stu-id="d15dc-117">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 2 (read/write).</span></span>

</dd> <dt>

<span data-ttu-id="d15dc-118">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="d15dc-118">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15dc-119">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d15dc-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d15dc-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d15dc-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15dc-121">Priorità assegnata ad accessi del dispositivo tramite questo controller.</span><span class="sxs-lookup"><span data-stu-id="d15dc-121">The priority given to accesses of the device through this controller.</span></span> <span data-ttu-id="d15dc-122">Il percorso con la priorità più alta avrà il valore più basso.</span><span class="sxs-lookup"><span data-stu-id="d15dc-122">The highest priority path will have the lowest value.</span></span> <span data-ttu-id="d15dc-123">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)ed è sempre impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="d15dc-123">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="d15dc-124">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="d15dc-124">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15dc-125">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d15dc-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d15dc-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d15dc-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15dc-127">Indica se il controller sta attivando o accedendo attivamente al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d15dc-127">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="d15dc-128">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)ed è sempre impostata su 1 (attivo).</span><span class="sxs-lookup"><span data-stu-id="d15dc-128">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 1 (Active).</span></span>

</dd> <dt>

<span data-ttu-id="d15dc-129">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="d15dc-129">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15dc-130">Tipo di dati: **[ **\_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller)**</span><span class="sxs-lookup"><span data-stu-id="d15dc-130">Data type: **[**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller)**</span></span>
</dt> <dt>

<span data-ttu-id="d15dc-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d15dc-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15dc-132">Riferimento al controller.</span><span class="sxs-lookup"><span data-stu-id="d15dc-132">A reference to the controller.</span></span> <span data-ttu-id="d15dc-133">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span><span class="sxs-lookup"><span data-stu-id="d15dc-133">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="d15dc-134">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="d15dc-134">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15dc-135">Tipo di dati: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="d15dc-135">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="d15dc-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d15dc-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15dc-137">Riferimento al dispositivo controllato.</span><span class="sxs-lookup"><span data-stu-id="d15dc-137">A reference to the controlled device.</span></span> <span data-ttu-id="d15dc-138">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span><span class="sxs-lookup"><span data-stu-id="d15dc-138">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="d15dc-139">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="d15dc-139">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15dc-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d15dc-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d15dc-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d15dc-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15dc-142">Indirizzo del dispositivo associato nel contesto del controller precedente.</span><span class="sxs-lookup"><span data-stu-id="d15dc-142">The address of the associated device in the context of the antecedent controller.</span></span> <span data-ttu-id="d15dc-143">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span><span class="sxs-lookup"><span data-stu-id="d15dc-143">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="d15dc-144">**NegotiatedDataWidth**</span><span class="sxs-lookup"><span data-stu-id="d15dc-144">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15dc-145">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d15dc-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d15dc-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d15dc-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15dc-147">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)ed è sempre impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="d15dc-147">This property is inherited from [**CIM\_DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="d15dc-148">**NegotiatedSpeed**</span><span class="sxs-lookup"><span data-stu-id="d15dc-148">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15dc-149">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d15dc-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d15dc-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d15dc-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15dc-151">Questa proprietà viene ereditata da [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)ed è sempre impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="d15dc-151">This property is inherited from [**CIM\_DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="d15dc-152">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="d15dc-152">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15dc-153">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d15dc-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d15dc-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d15dc-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15dc-155">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="d15dc-155">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d15dc-156">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="d15dc-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15dc-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d15dc-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d15dc-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d15dc-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15dc-159">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="d15dc-159">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d15dc-160">**TimeOfDeviceReset (ora**</span><span class="sxs-lookup"><span data-stu-id="d15dc-160">**TimeOfDeviceReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d15dc-161">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d15dc-161">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d15dc-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d15dc-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d15dc-163">Questa proprietà viene ereditata da [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="d15dc-163">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d15dc-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="d15dc-164">Remarks</span></span>

<span data-ttu-id="d15dc-165">L'accesso alla **classe \_ ControlledBy di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="d15dc-165">Access to the **Msvm\_ControlledBy** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d15dc-166">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d15dc-166">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d15dc-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d15dc-167">Requirements</span></span>



| <span data-ttu-id="d15dc-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="d15dc-168">Requirement</span></span> | <span data-ttu-id="d15dc-169">Valore</span><span class="sxs-lookup"><span data-stu-id="d15dc-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d15dc-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d15dc-170">Minimum supported client</span></span><br/> | <span data-ttu-id="d15dc-171">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d15dc-171">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d15dc-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d15dc-172">Minimum supported server</span></span><br/> | <span data-ttu-id="d15dc-173">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d15dc-173">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d15dc-174">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d15dc-174">Namespace</span></span><br/>                | <span data-ttu-id="d15dc-175">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d15dc-175">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d15dc-176">MOF</span><span class="sxs-lookup"><span data-stu-id="d15dc-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d15dc-177"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d15dc-177"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d15dc-178">DLL</span><span class="sxs-lookup"><span data-stu-id="d15dc-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d15dc-179"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d15dc-179"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d15dc-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d15dc-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d15dc-181">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="d15dc-181">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="d15dc-182">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="d15dc-182">**CIM\_ControlledBy**</span></span>](/windows/desktop/CIMWin32Prov/cim-controlledby)
</dt> <dt>

[<span data-ttu-id="d15dc-183">Classi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d15dc-183">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 


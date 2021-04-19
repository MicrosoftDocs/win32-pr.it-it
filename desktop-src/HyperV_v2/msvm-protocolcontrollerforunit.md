---
description: Questa associazione indica che una sottoclasse di un dispositivo logico, ad esempio un volume di archiviazione, è connessa tramite un controller di protocollo specifico.
ms.assetid: 93025450-BE6C-48DC-913C-2050674DF81A
title: Classe Msvm_ProtocolControllerForUnit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProtocolControllerForUnit
- Msvm_ProtocolControllerForUnit.Antecedent
- Msvm_ProtocolControllerForUnit.Dependent
- Msvm_ProtocolControllerForUnit.DeviceNumber
- Msvm_ProtocolControllerForUnit.AccessPriority
- Msvm_ProtocolControllerForUnit.AccessState
- Msvm_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1470192fc4f10e60bdfef013146483b47cbfa7f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310010"
---
# <a name="msvm_protocolcontrollerforunit-class"></a><span data-ttu-id="b98f0-103">\_Classe MSVM ProtocolControllerForUnit</span><span class="sxs-lookup"><span data-stu-id="b98f0-103">Msvm\_ProtocolControllerForUnit class</span></span>

<span data-ttu-id="b98f0-104">Questa associazione indica che una sottoclasse di un dispositivo logico, ad esempio un volume di archiviazione, è connessa tramite un controller di protocollo specifico.</span><span class="sxs-lookup"><span data-stu-id="b98f0-104">This association indicates that a subclass of logical device (for example a storage volume) is connected through a specific protocol controller.</span></span> <span data-ttu-id="b98f0-105">In molte situazioni, ad esempio mascheramento LUN di archiviazione, è possibile che molte di queste associazioni vengano usate per correlare oggetti diversi.</span><span class="sxs-lookup"><span data-stu-id="b98f0-105">In many situations (for example storage LUN masking), there may be many of these associations used to relate to different objects.</span></span> <span data-ttu-id="b98f0-106">Pertanto, le sottoclassi sono state definite per ottimizzare l'enumerazione delle associazioni.</span><span class="sxs-lookup"><span data-stu-id="b98f0-106">Therefore, subclasses have been defined to optimize enumeration of the associations.</span></span>

<span data-ttu-id="b98f0-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b98f0-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b98f0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b98f0-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProtocolControllerForUnit : CIM_ProtocolControllerForUnit
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a><span data-ttu-id="b98f0-109">Members</span><span class="sxs-lookup"><span data-stu-id="b98f0-109">Members</span></span>

<span data-ttu-id="b98f0-110">La **classe \_ ProtocolControllerForUnit di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b98f0-110">The **Msvm\_ProtocolControllerForUnit** class has these types of members:</span></span>

-   [<span data-ttu-id="b98f0-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b98f0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b98f0-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b98f0-112">Properties</span></span>

<span data-ttu-id="b98f0-113">La **classe \_ ProtocolControllerForUnit di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b98f0-113">The **Msvm\_ProtocolControllerForUnit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b98f0-114">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="b98f0-114">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b98f0-115">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b98f0-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b98f0-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b98f0-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b98f0-117">Priorità assegnata ad accessi del dispositivo tramite questo controller.</span><span class="sxs-lookup"><span data-stu-id="b98f0-117">The priority given to accesses of the device through this controller.</span></span> <span data-ttu-id="b98f0-118">Il percorso con la priorità più alta avrà il valore più basso per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b98f0-118">The highest priority path will have the lowest value for this parameter.</span></span> <span data-ttu-id="b98f0-119">Questa classe è ereditata da **CIM \_ ProtocolControllerForDevice**.</span><span class="sxs-lookup"><span data-stu-id="b98f0-119">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

</dd> <dt>

<span data-ttu-id="b98f0-120">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="b98f0-120">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b98f0-121">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b98f0-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b98f0-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b98f0-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b98f0-123">Indica se il controller sta attivamente eseguendo il comando o accede al dispositivo (2) o meno (3).</span><span class="sxs-lookup"><span data-stu-id="b98f0-123">Indicates whether the controller is actively commanding or accessing the device (2) or not (3).</span></span> <span data-ttu-id="b98f0-124">È inoltre possibile definire il valore 0 (sconosciuto).</span><span class="sxs-lookup"><span data-stu-id="b98f0-124">Also, the value, 0 (Unknown), can be defined.</span></span> <span data-ttu-id="b98f0-125">Queste informazioni sono necessarie quando è possibile eseguire il comando o l'accesso a un dispositivo logico tramite più controller di protocollo.</span><span class="sxs-lookup"><span data-stu-id="b98f0-125">This information is necessary when a logical device can be commanded by, or accessed through, multiple protocol controllers.</span></span> <span data-ttu-id="b98f0-126">Questa classe è ereditata da **CIM \_ ProtocolControllerForDevice**.</span><span class="sxs-lookup"><span data-stu-id="b98f0-126">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

<dl> <dt>

<span data-ttu-id="b98f0-127"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b98f0-127"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b98f0-128"><span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Attivo** (2)</span><span class="sxs-lookup"><span data-stu-id="b98f0-128"><span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Active** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b98f0-129"><span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inattivo** (3)</span><span class="sxs-lookup"><span data-stu-id="b98f0-129"><span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inactive** (3 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b98f0-130">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="b98f0-130">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b98f0-131">Tipo di dati: **[ **CIM \_ ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**</span><span class="sxs-lookup"><span data-stu-id="b98f0-131">Data type: **[**CIM\_ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**</span></span>
</dt> <dt>

<span data-ttu-id="b98f0-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b98f0-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b98f0-133">Controller del protocollo.</span><span class="sxs-lookup"><span data-stu-id="b98f0-133">The protocol controller.</span></span> <span data-ttu-id="b98f0-134">Questa classe viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="b98f0-134">This class is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="b98f0-135">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="b98f0-135">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b98f0-136">Tipo di dati: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="b98f0-136">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="b98f0-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b98f0-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b98f0-138">Dispositivo controllato.</span><span class="sxs-lookup"><span data-stu-id="b98f0-138">The controlled device.</span></span> <span data-ttu-id="b98f0-139">Questa classe viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="b98f0-139">This class is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="b98f0-140">**DeviceAccess**</span><span class="sxs-lookup"><span data-stu-id="b98f0-140">**DeviceAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b98f0-141">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b98f0-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b98f0-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b98f0-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b98f0-143">Diritti di accesso concessi al dispositivo tramite questo controller.</span><span class="sxs-lookup"><span data-stu-id="b98f0-143">The access rights granted to the device through this controller.</span></span> <span data-ttu-id="b98f0-144">Questa classe è ereditata da **CIM \_ ProtocolControllerForUnit**.</span><span class="sxs-lookup"><span data-stu-id="b98f0-144">This class is inherited from **CIM\_ProtocolControllerForUnit**.</span></span>



| <span data-ttu-id="b98f0-145">Valore</span><span class="sxs-lookup"><span data-stu-id="b98f0-145">Value</span></span>                                                                               | <span data-ttu-id="b98f0-146">Significato</span><span class="sxs-lookup"><span data-stu-id="b98f0-146">Meaning</span></span>                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="b98f0-147"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b98f0-147"><dt>0</dt></span></span> </dl>        | <span data-ttu-id="b98f0-148">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="b98f0-148">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="b98f0-149"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b98f0-149"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="b98f0-150">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="b98f0-150">Read/Write</span></span><br/>      |
| <dl> <span data-ttu-id="b98f0-151"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b98f0-151"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="b98f0-152">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="b98f0-152">Read-only</span></span><br/>       |
| <dl> <span data-ttu-id="b98f0-153"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b98f0-153"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="b98f0-154">Nessun accesso.</span><span class="sxs-lookup"><span data-stu-id="b98f0-154">No access.</span></span><br/>      |
| <dl> <span data-ttu-id="b98f0-155"><dt>5.. 15999</dt></span><span class="sxs-lookup"><span data-stu-id="b98f0-155"><dt>5..15999</dt></span></span> </dl> | <span data-ttu-id="b98f0-156">DMTF riservato</span><span class="sxs-lookup"><span data-stu-id="b98f0-156">DMTF Reserved</span></span><br/>   |
| <dl> <span data-ttu-id="b98f0-157"><dt>16000..</dt></span><span class="sxs-lookup"><span data-stu-id="b98f0-157"><dt>16000..</dt></span></span> </dl>  | <span data-ttu-id="b98f0-158">Fornitore riservato</span><span class="sxs-lookup"><span data-stu-id="b98f0-158">Vendor reserved</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b98f0-159">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="b98f0-159">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b98f0-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b98f0-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b98f0-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b98f0-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b98f0-162">Indirizzo del dispositivo associato nel contesto del controller precedente.</span><span class="sxs-lookup"><span data-stu-id="b98f0-162">The address of the associated device in the context of the antecedent controller.</span></span> <span data-ttu-id="b98f0-163">Questa classe è ereditata da **CIM \_ ProtocolControllerForDevice**.</span><span class="sxs-lookup"><span data-stu-id="b98f0-163">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b98f0-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="b98f0-164">Remarks</span></span>

<span data-ttu-id="b98f0-165">L'accesso alla **classe \_ ProtocolControllerForUnit di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="b98f0-165">Access to the **Msvm\_ProtocolControllerForUnit** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b98f0-166">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b98f0-166">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b98f0-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b98f0-167">Requirements</span></span>



| <span data-ttu-id="b98f0-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="b98f0-168">Requirement</span></span> | <span data-ttu-id="b98f0-169">Valore</span><span class="sxs-lookup"><span data-stu-id="b98f0-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b98f0-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b98f0-170">Minimum supported client</span></span><br/> | <span data-ttu-id="b98f0-171">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b98f0-171">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b98f0-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b98f0-172">Minimum supported server</span></span><br/> | <span data-ttu-id="b98f0-173">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b98f0-173">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b98f0-174">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b98f0-174">Namespace</span></span><br/>                | <span data-ttu-id="b98f0-175">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b98f0-175">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b98f0-176">MOF</span><span class="sxs-lookup"><span data-stu-id="b98f0-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b98f0-177"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b98f0-177"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b98f0-178">DLL</span><span class="sxs-lookup"><span data-stu-id="b98f0-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b98f0-179"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b98f0-179"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b98f0-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b98f0-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b98f0-181">**\_PROTOCOLCONTROLLERFORUNIT CIM**</span><span class="sxs-lookup"><span data-stu-id="b98f0-181">**CIM\_ProtocolControllerForUnit**</span></span>](cim-protocolcontrollerforunit.md)
</dt> <dt>

<span data-ttu-id="b98f0-182">[**\_PROTOCOLCONTROLLERFORUNIT CIM**](/previous-versions//cc150672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b98f0-182">[**CIM\_ProtocolControllerForUnit**](/previous-versions//cc150672(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b98f0-183">Classi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b98f0-183">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 


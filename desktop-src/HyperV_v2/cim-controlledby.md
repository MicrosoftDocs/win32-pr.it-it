---
description: Rappresenta una relazione tra un controller e un dispositivo logico gestito dal controller.
ms.assetid: 5a938fa4-3b91-42ad-beee-12ed0ce6df9a
title: Classe CIM_ControlledBy (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.TimeOfDeviceReset
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
- CIM_ControlledBy.DeviceNumber
- CIM_ControlledBy.AccessMode
- CIM_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7b035a93c47f9c33d981614ba6fc46b35f916e7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879770"
---
# <a name="cim_controlledby-class-hyper-v-management"></a><span data-ttu-id="b291b-103">Classe CIM_ControlledBy (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="b291b-103">CIM_ControlledBy class (Hyper-V management)</span></span>

<span data-ttu-id="b291b-104">Rappresenta una relazione tra un controller e un dispositivo logico gestito dal controller.</span><span class="sxs-lookup"><span data-stu-id="b291b-104">Represents a relationship between a controller and a logical device that is managed by the controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="b291b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b291b-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode;
  uint16                AccessPriority;
};
```

## <a name="members"></a><span data-ttu-id="b291b-106">Members</span><span class="sxs-lookup"><span data-stu-id="b291b-106">Members</span></span>

<span data-ttu-id="b291b-107">La classe **CIM \_ ControlledBy** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b291b-107">The **CIM\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="b291b-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b291b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b291b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b291b-109">Properties</span></span>

<span data-ttu-id="b291b-110">La classe **CIM \_ ControlledBy** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b291b-110">The **CIM\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b291b-111">**AccessMode**</span><span class="sxs-lookup"><span data-stu-id="b291b-111">**AccessMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b291b-112">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b291b-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b291b-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b291b-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b291b-114">Questa proprietà che descrive l'accessibilità del dispositivo tramite il controller.</span><span class="sxs-lookup"><span data-stu-id="b291b-114">This property that describes the accessibility of the device through the controller.</span></span>

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

<span data-ttu-id="b291b-115">**ReadWrite** (2)</span><span class="sxs-lookup"><span data-stu-id="b291b-115">**ReadWrite** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

<span data-ttu-id="b291b-116">**ReadOnly** (3)</span><span class="sxs-lookup"><span data-stu-id="b291b-116">**ReadOnly** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="NoAccess"></span><span id="noaccess"></span><span id="NOACCESS"></span>

<span data-ttu-id="b291b-117">**NoAccess** (4)</span><span class="sxs-lookup"><span data-stu-id="b291b-117">**NoAccess** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b291b-118">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="b291b-118">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b291b-119">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b291b-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b291b-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b291b-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b291b-121">Priorità per l'accesso del dispositivo tramite il controller.</span><span class="sxs-lookup"><span data-stu-id="b291b-121">The priority for access of the device through the controller.</span></span> <span data-ttu-id="b291b-122">Un valore inferiore indica una priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="b291b-122">A lower value indicates a higher priority.</span></span>

</dd> <dt>

<span data-ttu-id="b291b-123">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="b291b-123">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b291b-124">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b291b-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b291b-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b291b-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b291b-126">Indica se il controller sta gestendo attivamente il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b291b-126">Indicates whether the controller is actively managing the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b291b-127">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b291b-127">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="b291b-128">**Attivo** (1)</span><span class="sxs-lookup"><span data-stu-id="b291b-128">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="b291b-129">**Inattivo** (2)</span><span class="sxs-lookup"><span data-stu-id="b291b-129">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b291b-130">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="b291b-130">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b291b-131">Tipo di dati **: \_ controller CIM**</span><span class="sxs-lookup"><span data-stu-id="b291b-131">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="b291b-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b291b-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b291b-133">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="b291b-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b291b-134">Controller.</span><span class="sxs-lookup"><span data-stu-id="b291b-134">The controller.</span></span>

</dd> <dt>

<span data-ttu-id="b291b-135">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="b291b-135">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b291b-136">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="b291b-136">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="b291b-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b291b-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b291b-138">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="b291b-138">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b291b-139">Dispositivi logici.</span><span class="sxs-lookup"><span data-stu-id="b291b-139">The logical devices.</span></span>

</dd> <dt>

<span data-ttu-id="b291b-140">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="b291b-140">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b291b-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b291b-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b291b-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b291b-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b291b-143">Indirizzo del dispositivo associato nel contesto del controller.</span><span class="sxs-lookup"><span data-stu-id="b291b-143">The address of the associated device in the context of the controller.</span></span>

</dd> <dt>

<span data-ttu-id="b291b-144">**NumberOfHardResets**</span><span class="sxs-lookup"><span data-stu-id="b291b-144">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b291b-145">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b291b-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b291b-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b291b-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b291b-147">Qualificatori: **contatore**</span><span class="sxs-lookup"><span data-stu-id="b291b-147">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="b291b-148">Numero di reimpostazioni rigide rilasciate dal controller.</span><span class="sxs-lookup"><span data-stu-id="b291b-148">The number of hard resets issued by the controller.</span></span> <span data-ttu-id="b291b-149">Una reimpostazione hardware restituisce un dispositivo alla relativa inizializzazione o allo stato di avvio, dopo il quale vengono perse tutte le informazioni e i dati sullo stato dei dispositivi interni.</span><span class="sxs-lookup"><span data-stu-id="b291b-149">A hard reset returns a device to its initialization or boot-up state, after which all internal device state information and data are lost.</span></span>

</dd> <dt>

<span data-ttu-id="b291b-150">**NumberOfSoftResets**</span><span class="sxs-lookup"><span data-stu-id="b291b-150">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b291b-151">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b291b-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b291b-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b291b-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b291b-153">Qualificatori: **contatore**</span><span class="sxs-lookup"><span data-stu-id="b291b-153">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="b291b-154">Numero di reimpostazioni Soft emesse dal controller.</span><span class="sxs-lookup"><span data-stu-id="b291b-154">The number of soft resets issued by the controller.</span></span> <span data-ttu-id="b291b-155">Un ripristino soft non cancella lo stato o i dati del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b291b-155">A soft reset does not clear the device state or data.</span></span>

</dd> <dt>

<span data-ttu-id="b291b-156">**TimeOfDeviceReset (ora**</span><span class="sxs-lookup"><span data-stu-id="b291b-156">**TimeOfDeviceReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b291b-157">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b291b-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b291b-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b291b-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b291b-159">Ora dell'ultima reimpostazione del dispositivo downstream da parte del controller.</span><span class="sxs-lookup"><span data-stu-id="b291b-159">The time when the downstream device was last reset by the controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b291b-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b291b-160">Requirements</span></span>



| <span data-ttu-id="b291b-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="b291b-161">Requirement</span></span> | <span data-ttu-id="b291b-162">Valore</span><span class="sxs-lookup"><span data-stu-id="b291b-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b291b-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b291b-163">Minimum supported client</span></span><br/> | <span data-ttu-id="b291b-164">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b291b-164">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b291b-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b291b-165">Minimum supported server</span></span><br/> | <span data-ttu-id="b291b-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b291b-166">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b291b-167">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b291b-167">Namespace</span></span><br/>                | <span data-ttu-id="b291b-168">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b291b-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b291b-169">MOF</span><span class="sxs-lookup"><span data-stu-id="b291b-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b291b-170"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b291b-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b291b-171">DLL</span><span class="sxs-lookup"><span data-stu-id="b291b-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b291b-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b291b-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b291b-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b291b-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b291b-174">**\_DEVICECONNECTION CIM**</span><span class="sxs-lookup"><span data-stu-id="b291b-174">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> </dl>

 


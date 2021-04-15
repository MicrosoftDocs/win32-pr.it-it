---
description: Registra un servizio che fornisce oggetti correlati alle risorse specifiche della macchina virtuale.
ms.assetid: 85782C4D-E0A3-4EED-9A26-7928862C559B
title: Classe Msvm_VirtualSystemResourceRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceRegistration
- Msvm_VirtualSystemResourceRegistration.ResourceType
- Msvm_VirtualSystemResourceRegistration.Component
- Msvm_VirtualSystemResourceRegistration.IsRootDevice
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7cef3699de973bd22985215a64100c594f223be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525188"
---
# <a name="msvm_virtualsystemresourceregistration-class"></a><span data-ttu-id="78efe-103">\_Classe MSVM VirtualSystemResourceRegistration</span><span class="sxs-lookup"><span data-stu-id="78efe-103">Msvm\_VirtualSystemResourceRegistration class</span></span>

<span data-ttu-id="78efe-104">Registra un servizio che fornisce oggetti correlati alle risorse specifiche della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="78efe-104">Registers a service that provides virtual machine-specific resource-related objects.</span></span>

<span data-ttu-id="78efe-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="78efe-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="78efe-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78efe-106">Syntax</span></span>

``` syntax
class Msvm_VirtualSystemResourceRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition         REF ResourceType;
  Msvm_VirtualSystemResourceComponent REF Component;
  boolean                                 IsRootDevice = False;
};
```

## <a name="members"></a><span data-ttu-id="78efe-107">Members</span><span class="sxs-lookup"><span data-stu-id="78efe-107">Members</span></span>

<span data-ttu-id="78efe-108">La **classe \_ VirtualSystemResourceRegistration di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="78efe-108">The **Msvm\_VirtualSystemResourceRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="78efe-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="78efe-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78efe-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="78efe-110">Properties</span></span>

<span data-ttu-id="78efe-111">La **classe \_ VirtualSystemResourceRegistration di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="78efe-111">The **Msvm\_VirtualSystemResourceRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78efe-112">**Componente**</span><span class="sxs-lookup"><span data-stu-id="78efe-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78efe-113">Tipo di dati: **[ **MSVM \_ VirtualSystemResourceComponent**](msvm-virtualsystemresourcecomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="78efe-113">Data type: **[**Msvm\_VirtualSystemResourceComponent**](msvm-virtualsystemresourcecomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="78efe-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="78efe-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78efe-115">Riferimento a un'istanza di che descrive l'oggetto COM che implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="78efe-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="78efe-116">**IsRootDevice**</span><span class="sxs-lookup"><span data-stu-id="78efe-116">**IsRootDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78efe-117">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="78efe-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78efe-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="78efe-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78efe-119">**True** se la registrazione indica se il tipo di risorsa specificato è il dispositivo radice (o senza padre) per il servizio. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="78efe-119">**True** if this registration indicates whether the specified resource type is the root (or parent-less) device for this service; otherwise, **False**.</span></span> <span data-ttu-id="78efe-120">Quando **IsRootDevice** è impostato su **true**, può esistere una sola registrazione.</span><span class="sxs-lookup"><span data-stu-id="78efe-120">Only one registration can exist when **IsRootDevice** is set to **True**.</span></span> <span data-ttu-id="78efe-121">In caso contrario, la registrazione rappresenta un mapping a un sottodispositivo.</span><span class="sxs-lookup"><span data-stu-id="78efe-121">Otherwise, this registration represents a mapping to a sub-device.</span></span> <span data-ttu-id="78efe-122">Questa proprietà è sempre impostata su **false**.</span><span class="sxs-lookup"><span data-stu-id="78efe-122">This property is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="78efe-123">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="78efe-123">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78efe-124">Tipo di dati: **[ **MSVM \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="78efe-124">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="78efe-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="78efe-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78efe-126">Riferimento a un'istanza di che descrive un tipo di risorsa supportato dal servizio.</span><span class="sxs-lookup"><span data-stu-id="78efe-126">A reference to an instance that describes a resource type supported by the service.</span></span> <span data-ttu-id="78efe-127">Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span><span class="sxs-lookup"><span data-stu-id="78efe-127">This property is inherited from [**Msvm\_VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78efe-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="78efe-128">Remarks</span></span>

<span data-ttu-id="78efe-129">L'accesso alla **classe \_ VirtualSystemResourceRegistration di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="78efe-129">Access to the **Msvm\_VirtualSystemResourceRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="78efe-130">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="78efe-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="78efe-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78efe-131">Requirements</span></span>



| <span data-ttu-id="78efe-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="78efe-132">Requirement</span></span> | <span data-ttu-id="78efe-133">Valore</span><span class="sxs-lookup"><span data-stu-id="78efe-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78efe-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78efe-134">Minimum supported client</span></span><br/> | <span data-ttu-id="78efe-135">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="78efe-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="78efe-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78efe-136">Minimum supported server</span></span><br/> | <span data-ttu-id="78efe-137">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="78efe-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="78efe-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="78efe-138">End of client support</span></span><br/>    | <span data-ttu-id="78efe-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="78efe-139">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="78efe-140">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="78efe-140">End of server support</span></span><br/>    | <span data-ttu-id="78efe-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="78efe-141">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="78efe-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="78efe-142">Namespace</span></span><br/>                | <span data-ttu-id="78efe-143">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="78efe-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="78efe-144">MOF</span><span class="sxs-lookup"><span data-stu-id="78efe-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78efe-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78efe-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="78efe-146">DLL</span><span class="sxs-lookup"><span data-stu-id="78efe-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78efe-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="78efe-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="78efe-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78efe-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78efe-149">**\_VirtualizationComponentRegistration MSVM**</span><span class="sxs-lookup"><span data-stu-id="78efe-149">**Msvm\_VirtualizationComponentRegistration**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[<span data-ttu-id="78efe-150">**\_VirtualizationComponentRegistration MSVM**</span><span class="sxs-lookup"><span data-stu-id="78efe-150">**Msvm\_VirtualizationComponentRegistration**</span></span>](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 


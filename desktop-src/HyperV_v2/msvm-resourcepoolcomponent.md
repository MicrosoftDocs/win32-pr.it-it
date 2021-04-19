---
description: Rappresenta un elemento del pool di risorse della piattaforma Microsoft Windows Hyper-V.
ms.assetid: DF48E8A6-240F-44E9-9DA3-1E6694396F10
title: Classe Msvm_ResourcePoolComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolComponent
- Msvm_ResourcePoolComponent.CLSID
- Msvm_ResourcePoolComponent.Context
- Msvm_ResourcePoolComponent.Enabled
- Msvm_ResourcePoolComponent.Name
- Msvm_ResourcePoolComponent.AllocationCapabilitiesClassName
- Msvm_ResourcePoolComponent.ResourcePoolClassName
- Msvm_ResourcePoolComponent.ResourcePoolSettingDataClassName
- Msvm_ResourcePoolComponent.PhysicalDeviceClassName
- Msvm_ResourcePoolComponent.WmiFactoryCLSID
- Msvm_ResourcePoolComponent.MaxParentPools
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a0cf64a9e01d904aa4e6c6ec263fdeec92eb7c94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313843"
---
# <a name="msvm_resourcepoolcomponent-class"></a><span data-ttu-id="bac9e-103">\_Classe MSVM ResourcePoolComponent</span><span class="sxs-lookup"><span data-stu-id="bac9e-103">Msvm\_ResourcePoolComponent class</span></span>

<span data-ttu-id="bac9e-104">Rappresenta un elemento del pool di risorse della piattaforma Microsoft Windows Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="bac9e-104">Represents a resource pool element of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="bac9e-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="bac9e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bac9e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bac9e-106">Syntax</span></span>

``` syntax
class Msvm_ResourcePoolComponent : Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
  string  AllocationCapabilitiesClassName;
  string  ResourcePoolClassName;
  string  ResourcePoolSettingDataClassName = "Msvm_ResourcePoolSettingData";
  string  PhysicalDeviceClassName;
  string  WmiFactoryCLSID;
  uint8   MaxParentPools = 0;
};
```

## <a name="members"></a><span data-ttu-id="bac9e-107">Members</span><span class="sxs-lookup"><span data-stu-id="bac9e-107">Members</span></span>

<span data-ttu-id="bac9e-108">La **classe \_ ResourcePoolComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bac9e-108">The **Msvm\_ResourcePoolComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="bac9e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bac9e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bac9e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bac9e-110">Properties</span></span>

<span data-ttu-id="bac9e-111">La **classe \_ ResourcePoolComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bac9e-111">The **Msvm\_ResourcePoolComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bac9e-112">**AllocationCapabilitiesClassName**</span><span class="sxs-lookup"><span data-stu-id="bac9e-112">**AllocationCapabilitiesClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bac9e-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bac9e-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bac9e-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bac9e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bac9e-115">Nome della classe derivata da [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) che descrive le funzionalità di allocazione del pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="bac9e-115">The name of the class derived from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) that describes the allocation capabilities of this resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="bac9e-116">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="bac9e-116">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bac9e-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bac9e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bac9e-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bac9e-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bac9e-119">**GUID** che rappresenta l'identificatore di classe dell'oggetto com del servizio.</span><span class="sxs-lookup"><span data-stu-id="bac9e-119">A **GUID** that represents the class identifier of the service's COM object.</span></span> <span data-ttu-id="bac9e-120">Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="bac9e-120">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="bac9e-121">**Contesto**</span><span class="sxs-lookup"><span data-stu-id="bac9e-121">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bac9e-122">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bac9e-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bac9e-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bac9e-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bac9e-124">Contesto in cui viene eseguito l'oggetto appena creato.</span><span class="sxs-lookup"><span data-stu-id="bac9e-124">The context in which the newly created object will run.</span></span> <span data-ttu-id="bac9e-125">Questo valore viene passato al parametro *dwClsContext* a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="bac9e-125">This value is passed in the *dwClsContext* parameter to **CoCreateInstance**.</span></span> <span data-ttu-id="bac9e-126">Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)ed è sempre impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="bac9e-126">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="bac9e-127">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="bac9e-127">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bac9e-128">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bac9e-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bac9e-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bac9e-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bac9e-130">**True** se questa istanza è abilitata e può essere utilizzata per completare le richieste del client. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="bac9e-130">**True** if this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="bac9e-131">Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)ed è sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="bac9e-131">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="bac9e-132">**MaxParentPools**</span><span class="sxs-lookup"><span data-stu-id="bac9e-132">**MaxParentPools**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bac9e-133">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="bac9e-133">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bac9e-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bac9e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bac9e-135">Numero massimo di pool di risorse padre supportati da un pool figlio.</span><span class="sxs-lookup"><span data-stu-id="bac9e-135">The maximum number of parent resource pools that a child pool supports.</span></span>

</dd> <dt>

<span data-ttu-id="bac9e-136">**Nome**</span><span class="sxs-lookup"><span data-stu-id="bac9e-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bac9e-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bac9e-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bac9e-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bac9e-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bac9e-139">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="bac9e-139">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bac9e-140">Stringa indipendente dal linguaggio che identifica in modo univoco l'elemento.</span><span class="sxs-lookup"><span data-stu-id="bac9e-140">A language-neutral string that uniquely identifies the element.</span></span> <span data-ttu-id="bac9e-141">Per evitare conflitti di denominazione, è consigliabile il formato seguente: \| " \| versione componente fornitore".</span><span class="sxs-lookup"><span data-stu-id="bac9e-141">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="bac9e-142">Questo nome rappresenta ad esempio la versione 1,0 del componente della porta di rete emulata Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| v 1.0".</span><span class="sxs-lookup"><span data-stu-id="bac9e-142">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span> <span data-ttu-id="bac9e-143">Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="bac9e-143">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="bac9e-144">**PhysicalDeviceClassName**</span><span class="sxs-lookup"><span data-stu-id="bac9e-144">**PhysicalDeviceClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bac9e-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bac9e-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bac9e-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bac9e-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bac9e-147">Nome della classe derivata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) che implementa il dispositivo fisico da cui questo pool alloca le risorse.</span><span class="sxs-lookup"><span data-stu-id="bac9e-147">The name of the class derived from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) that implements the physical device from which this pool allocates resources.</span></span> <span data-ttu-id="bac9e-148">Questa proprietà può essere **null** se la classe del dispositivo virtuale allocata da questo pool è la stessa della classe del dispositivo fisico.</span><span class="sxs-lookup"><span data-stu-id="bac9e-148">This property can be **Null** if the virtual device class allocated from this pool is the same as the physical device class.</span></span>

</dd> <dt>

<span data-ttu-id="bac9e-149">**ResourcePoolClassName**</span><span class="sxs-lookup"><span data-stu-id="bac9e-149">**ResourcePoolClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bac9e-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bac9e-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bac9e-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bac9e-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bac9e-152">Nome della classe derivata da [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)) che implementa il pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="bac9e-152">The name of the class derived from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)) that implements the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="bac9e-153">**ResourcePoolSettingDataClassName**</span><span class="sxs-lookup"><span data-stu-id="bac9e-153">**ResourcePoolSettingDataClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bac9e-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bac9e-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bac9e-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bac9e-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bac9e-156">Nome della classe derivata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) che descrive le impostazioni non correlate all'allocazione del pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="bac9e-156">The name of the class derived from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) that describes the non-allocation related settings of the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="bac9e-157">**WmiFactoryCLSID**</span><span class="sxs-lookup"><span data-stu-id="bac9e-157">**WmiFactoryCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bac9e-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bac9e-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bac9e-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bac9e-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bac9e-160">**GUID** che rappresenta l'identificatore di classe della factory dell'oggetto WMI del componente.</span><span class="sxs-lookup"><span data-stu-id="bac9e-160">A **GUID** that represents the class identifier of the component's WMI object factory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bac9e-161">Commenti</span><span class="sxs-lookup"><span data-stu-id="bac9e-161">Remarks</span></span>

<span data-ttu-id="bac9e-162">L'accesso alla **classe \_ ResourcePoolComponent di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="bac9e-162">Access to the **Msvm\_ResourcePoolComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bac9e-163">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="bac9e-163">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="bac9e-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bac9e-164">Requirements</span></span>



| <span data-ttu-id="bac9e-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="bac9e-165">Requirement</span></span> | <span data-ttu-id="bac9e-166">Valore</span><span class="sxs-lookup"><span data-stu-id="bac9e-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bac9e-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bac9e-167">Minimum supported client</span></span><br/> | <span data-ttu-id="bac9e-168">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bac9e-168">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bac9e-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bac9e-169">Minimum supported server</span></span><br/> | <span data-ttu-id="bac9e-170">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bac9e-170">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bac9e-171">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bac9e-171">End of client support</span></span><br/>    | <span data-ttu-id="bac9e-172">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="bac9e-172">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="bac9e-173">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="bac9e-173">End of server support</span></span><br/>    | <span data-ttu-id="bac9e-174">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bac9e-174">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="bac9e-175">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bac9e-175">Namespace</span></span><br/>                | <span data-ttu-id="bac9e-176">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="bac9e-176">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bac9e-177">MOF</span><span class="sxs-lookup"><span data-stu-id="bac9e-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bac9e-178"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bac9e-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bac9e-179">DLL</span><span class="sxs-lookup"><span data-stu-id="bac9e-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bac9e-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bac9e-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bac9e-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bac9e-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bac9e-182">**\_VirtualizationComponent MSVM**</span><span class="sxs-lookup"><span data-stu-id="bac9e-182">**Msvm\_VirtualizationComponent**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[<span data-ttu-id="bac9e-183">**\_VirtualizationComponent MSVM**</span><span class="sxs-lookup"><span data-stu-id="bac9e-183">**Msvm\_VirtualizationComponent**</span></span>](msvm-virtualizationcomponent.md)
</dt> </dl>

 


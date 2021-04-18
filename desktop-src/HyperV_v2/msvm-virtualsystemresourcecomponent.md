---
description: Rappresenta un servizio di dispositivo virtuale della piattaforma Microsoft Windows Hyper-V.
ms.assetid: 865D83E1-0FC6-4F96-94BB-AA5116890127
title: Classe Msvm_VirtualSystemResourceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceComponent
- Msvm_VirtualSystemResourceComponent.Name
- Msvm_VirtualSystemResourceComponent.CLSID
- Msvm_VirtualSystemResourceComponent.Context
- Msvm_VirtualSystemResourceComponent.Enabled
- Msvm_VirtualSystemResourceComponent.AdditionalClassNames
- Msvm_VirtualSystemResourceComponent.Type
- Msvm_VirtualSystemResourceComponent.HotAdd
- Msvm_VirtualSystemResourceComponent.HotRemove
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 81c2d31a6497325ac77003ded266333518de890a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305986"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a><span data-ttu-id="277e5-103">\_Classe MSVM VirtualSystemResourceComponent</span><span class="sxs-lookup"><span data-stu-id="277e5-103">Msvm\_VirtualSystemResourceComponent class</span></span>

<span data-ttu-id="277e5-104">Rappresenta un servizio di dispositivo virtuale della piattaforma Microsoft Windows Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="277e5-104">Represents a virtual device service of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="277e5-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="277e5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="277e5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="277e5-106">Syntax</span></span>

``` syntax
class Msvm_VirtualSystemResourceComponent : Msvm_VirtualizationComponent
{
  string  Name;
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  AdditionalClassNames[];
  uint16  Type = 1;
  boolean HotAdd = False;
  boolean HotRemove = False;
};
```

## <a name="members"></a><span data-ttu-id="277e5-107">Members</span><span class="sxs-lookup"><span data-stu-id="277e5-107">Members</span></span>

<span data-ttu-id="277e5-108">La **classe \_ VirtualSystemResourceComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="277e5-108">The **Msvm\_VirtualSystemResourceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="277e5-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="277e5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="277e5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="277e5-110">Properties</span></span>

<span data-ttu-id="277e5-111">La **classe \_ VirtualSystemResourceComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="277e5-111">The **Msvm\_VirtualSystemResourceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="277e5-112">**AdditionalClassNames**</span><span class="sxs-lookup"><span data-stu-id="277e5-112">**AdditionalClassNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277e5-113">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="277e5-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="277e5-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="277e5-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277e5-115">Matrice di stringhe contenente classi non di associazione aggiuntive emerse da questa istanza di **MSVM \_ VirtualSystemResourceComponent** .</span><span class="sxs-lookup"><span data-stu-id="277e5-115">An array of strings containing additional non-association classes surfaced by this **Msvm\_VirtualSystemResourceComponent** instance.</span></span> <span data-ttu-id="277e5-116">Queste classi devono derivare da né [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) né [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="277e5-116">These classes must derive from neither [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) nor [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="277e5-117">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="277e5-117">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277e5-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="277e5-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="277e5-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="277e5-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277e5-120">GUID che rappresenta l'identificatore di classe dell'oggetto COM del servizio.</span><span class="sxs-lookup"><span data-stu-id="277e5-120">A GUID that represents the class identifier of the service's COM object.</span></span> <span data-ttu-id="277e5-121">Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="277e5-121">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="277e5-122">**Contesto**</span><span class="sxs-lookup"><span data-stu-id="277e5-122">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277e5-123">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="277e5-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="277e5-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="277e5-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277e5-125">Contesto in cui viene eseguito l'oggetto appena creato.</span><span class="sxs-lookup"><span data-stu-id="277e5-125">The context in which the newly created object will run.</span></span> <span data-ttu-id="277e5-126">Questo valore viene passato al parametro *dwClsContext* a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="277e5-126">This value is passed in the *dwClsContext* parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="277e5-127">Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)ed è sempre impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="277e5-127">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="277e5-128">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="277e5-128">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277e5-129">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="277e5-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="277e5-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="277e5-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277e5-131">**True** se questa istanza è abilitata e può essere utilizzata per completare le richieste del client. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="277e5-131">**True** if this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="277e5-132">Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)ed è sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="277e5-132">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="277e5-133">**HotAdd**</span><span class="sxs-lookup"><span data-stu-id="277e5-133">**HotAdd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277e5-134">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="277e5-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="277e5-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="277e5-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277e5-136">**True** se questa istanza può essere aggiunta a caldo a una macchina virtuale. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="277e5-136">**True** if this instance can be hot-added to a virtual machine; otherwise, **False**.</span></span> <span data-ttu-id="277e5-137">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="277e5-137">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="277e5-138">**HotRemove**</span><span class="sxs-lookup"><span data-stu-id="277e5-138">**HotRemove**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277e5-139">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="277e5-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="277e5-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="277e5-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277e5-141">**True** se questa istanza può essere rimossa a caldo da una macchina virtuale. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="277e5-141">**True** if this instance can be hot-removed from a virtual machine; otherwise, **False**.</span></span> <span data-ttu-id="277e5-142">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="277e5-142">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="277e5-143">**Nome**</span><span class="sxs-lookup"><span data-stu-id="277e5-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277e5-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="277e5-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="277e5-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="277e5-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="277e5-146">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="277e5-146">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="277e5-147">Stringa indipendente dal linguaggio che identifica in modo univoco il servizio.</span><span class="sxs-lookup"><span data-stu-id="277e5-147">A language-neutral string that uniquely identifies the service.</span></span> <span data-ttu-id="277e5-148">Per evitare conflitti di denominazione, è consigliabile il formato seguente: \| " \| versione componente fornitore".</span><span class="sxs-lookup"><span data-stu-id="277e5-148">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="277e5-149">Questo nome rappresenta ad esempio la versione 1,0 del componente della porta di rete emulata Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| v 1.0".</span><span class="sxs-lookup"><span data-stu-id="277e5-149">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span> <span data-ttu-id="277e5-150">Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="277e5-150">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="277e5-151">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="277e5-151">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="277e5-152">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="277e5-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="277e5-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="277e5-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="277e5-154">La relazione dell'oggetto WMI descritta qui con il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="277e5-154">The relationship of the WMI object that is described here with the virtual device.</span></span>



| <span data-ttu-id="277e5-155">Valore</span><span class="sxs-lookup"><span data-stu-id="277e5-155">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="277e5-156">Significato</span><span class="sxs-lookup"><span data-stu-id="277e5-156">Meaning</span></span>                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> <span data-ttu-id="277e5-157"><dt>**"Non modificabile"**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="277e5-157"><dt>**"Not Changeable"**</dt> <dt>0</dt></span></span> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> <span data-ttu-id="277e5-158"><dt>**"Singleton"**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="277e5-158"><dt>**"Singleton"**</dt> <dt>1</dt></span></span> </dl>                     | <span data-ttu-id="277e5-159">Singleton è un oggetto WMI di primo livello associato a 1:1 con un dispositivo virtuale che può esistere solo una volta per ogni macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="277e5-159">Singleton is a top level WMI object that is tied 1:1 with a Virtual Device and can only exist once per virtual machine.</span></span> <span data-ttu-id="277e5-160">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="277e5-160">This is the default value.</span></span><br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <span data-ttu-id="277e5-161"><dt>**"Multiistanza"**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="277e5-161"><dt>**"MultiInstance"**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="277e5-162">Multi-instance è un oggetto WMI di primo livello che può esistere più volte per macchina virtuale ed è associato a 1:1 con un dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="277e5-162">MultiInstance is a top level WMI object that can exist multiple times per virtual machine and is tied 1:1 with a Virtual Device.</span></span><br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <span data-ttu-id="277e5-163"><dt>**"Sottodispositivo"**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="277e5-163"><dt>**"Subdevice"**</dt> <dt>3</dt></span></span> </dl>                     | <span data-ttu-id="277e5-164">Il sottodispositivo è un oggetto WMI che non contiene riferimenti padre ma è controllato da un solo dispositivo virtuale che può esistere una sola volta per ogni macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="277e5-164">Subdevice is a WMI object that has not parent reference but is controlled by only one Virtual Device that can exist only once per virtual machine.</span></span> <span data-ttu-id="277e5-165">L'oggetto WMI può tuttavia esistere più volte.</span><span class="sxs-lookup"><span data-stu-id="277e5-165">The WMI object though can exist multiples times.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="277e5-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="277e5-166">Remarks</span></span>

<span data-ttu-id="277e5-167">L'accesso alla **classe \_ VirtualSystemResourceComponent di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="277e5-167">Access to the **Msvm\_VirtualSystemResourceComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="277e5-168">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="277e5-168">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="277e5-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="277e5-169">Requirements</span></span>



| <span data-ttu-id="277e5-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="277e5-170">Requirement</span></span> | <span data-ttu-id="277e5-171">Valore</span><span class="sxs-lookup"><span data-stu-id="277e5-171">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="277e5-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="277e5-172">Minimum supported client</span></span><br/> | <span data-ttu-id="277e5-173">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="277e5-173">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="277e5-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="277e5-174">Minimum supported server</span></span><br/> | <span data-ttu-id="277e5-175">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="277e5-175">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="277e5-176">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="277e5-176">End of client support</span></span><br/>    | <span data-ttu-id="277e5-177">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="277e5-177">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="277e5-178">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="277e5-178">End of server support</span></span><br/>    | <span data-ttu-id="277e5-179">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="277e5-179">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="277e5-180">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="277e5-180">Namespace</span></span><br/>                | <span data-ttu-id="277e5-181">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="277e5-181">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="277e5-182">MOF</span><span class="sxs-lookup"><span data-stu-id="277e5-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="277e5-183"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="277e5-183"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="277e5-184">DLL</span><span class="sxs-lookup"><span data-stu-id="277e5-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="277e5-185"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="277e5-185"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="277e5-186">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="277e5-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="277e5-187">**\_VirtualizationComponent MSVM**</span><span class="sxs-lookup"><span data-stu-id="277e5-187">**Msvm\_VirtualizationComponent**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[<span data-ttu-id="277e5-188">**\_VirtualizationComponent MSVM**</span><span class="sxs-lookup"><span data-stu-id="277e5-188">**Msvm\_VirtualizationComponent**</span></span>](msvm-virtualizationcomponent.md)
</dt> </dl>

 


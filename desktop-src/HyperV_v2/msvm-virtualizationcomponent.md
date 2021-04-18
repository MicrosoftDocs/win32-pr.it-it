---
description: Rappresenta un servizio della piattaforma Microsoft Windows Hyper-V.
ms.assetid: 309EFE4C-EEA4-454C-943D-CBF99D64FE15
title: Classe Msvm_VirtualizationComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponent
- Msvm_VirtualizationComponent.CLSID
- Msvm_VirtualizationComponent.Context
- Msvm_VirtualizationComponent.Enabled
- Msvm_VirtualizationComponent.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 19811b224a4e93e85420539248b7d010491335aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306019"
---
# <a name="msvm_virtualizationcomponent-class"></a><span data-ttu-id="4f615-103">\_Classe MSVM VirtualizationComponent</span><span class="sxs-lookup"><span data-stu-id="4f615-103">Msvm\_VirtualizationComponent class</span></span>

<span data-ttu-id="4f615-104">Rappresenta un servizio della piattaforma Microsoft Windows Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="4f615-104">Represents a service of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="4f615-105">La sintassi seguente è semplificata Managed Object Format codice (MOF).</span><span class="sxs-lookup"><span data-stu-id="4f615-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f615-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f615-106">Syntax</span></span>

``` syntax
[Abstract]
class Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="4f615-107">Members</span><span class="sxs-lookup"><span data-stu-id="4f615-107">Members</span></span>

<span data-ttu-id="4f615-108">La **classe \_ VirtualizationComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4f615-108">The **Msvm\_VirtualizationComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="4f615-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4f615-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f615-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4f615-110">Properties</span></span>

<span data-ttu-id="4f615-111">La **classe \_ VirtualizationComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4f615-111">The **Msvm\_VirtualizationComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f615-112">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="4f615-112">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f615-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4f615-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f615-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f615-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f615-115">**GUID** che rappresenta l'identificatore di classe dell'oggetto com del servizio.</span><span class="sxs-lookup"><span data-stu-id="4f615-115">A **GUID** that represents the class identifier of the service's COM object.</span></span>

</dd> <dt>

<span data-ttu-id="4f615-116">**Contesto**</span><span class="sxs-lookup"><span data-stu-id="4f615-116">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f615-117">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f615-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4f615-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f615-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f615-119">Qualificatori: **sperimentale**</span><span class="sxs-lookup"><span data-stu-id="4f615-119">Qualifiers: **Experimental**</span></span>
</dt> </dl>

<span data-ttu-id="4f615-120">Contesto in cui viene eseguito l'oggetto appena creato.</span><span class="sxs-lookup"><span data-stu-id="4f615-120">The context in which the newly created object will run.</span></span> <span data-ttu-id="4f615-121">Questo valore viene passato al parametro *dwClsContext* a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="4f615-121">This value is passed in the *dwClsContext* parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="4f615-122">Questa proprietà è sempre impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="4f615-122">This property is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="4f615-123">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="4f615-123">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f615-124">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4f615-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4f615-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f615-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f615-126">**True** se questa istanza è abilitata e può essere utilizzata per completare le richieste del client. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="4f615-126">**True** is this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="4f615-127">Questa proprietà è sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="4f615-127">This property is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="4f615-128">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4f615-128">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f615-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4f615-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f615-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4f615-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f615-131">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="4f615-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4f615-132">Stringa indipendente dal linguaggio che identifica in modo univoco il servizio.</span><span class="sxs-lookup"><span data-stu-id="4f615-132">A language-neutral string that uniquely identifies the service.</span></span> <span data-ttu-id="4f615-133">Per evitare conflitti di denominazione, è consigliabile il formato seguente: \| " \| versione componente fornitore".</span><span class="sxs-lookup"><span data-stu-id="4f615-133">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="4f615-134">Questo nome rappresenta ad esempio la versione 1,0 del componente della porta di rete emulata Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| v 1.0".</span><span class="sxs-lookup"><span data-stu-id="4f615-134">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f615-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f615-135">Remarks</span></span>

<span data-ttu-id="4f615-136">L'accesso alla **classe \_ VirtualizationComponent di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="4f615-136">Access to the **Msvm\_VirtualizationComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4f615-137">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4f615-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f615-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f615-138">Requirements</span></span>



| <span data-ttu-id="4f615-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f615-139">Requirement</span></span> | <span data-ttu-id="4f615-140">Valore</span><span class="sxs-lookup"><span data-stu-id="4f615-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f615-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f615-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4f615-142">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4f615-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4f615-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f615-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4f615-144">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4f615-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f615-145">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4f615-145">End of client support</span></span><br/>    | <span data-ttu-id="4f615-146">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4f615-146">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4f615-147">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="4f615-147">End of server support</span></span><br/>    | <span data-ttu-id="4f615-148">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4f615-148">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4f615-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4f615-149">Namespace</span></span><br/>                | <span data-ttu-id="4f615-150">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4f615-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4f615-151">MOF</span><span class="sxs-lookup"><span data-stu-id="4f615-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f615-152"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f615-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f615-153">DLL</span><span class="sxs-lookup"><span data-stu-id="4f615-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f615-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4f615-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


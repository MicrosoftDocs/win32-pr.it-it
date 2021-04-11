---
description: Registra un servizio che fornisce oggetti globali correlati al pool di risorse.
ms.assetid: B602F6E1-2889-43CF-AAF1-40F339231DB4
title: Classe Msvm_ResourcePoolRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolRegistration
- Msvm_ResourcePoolRegistration.ResourceType
- Msvm_ResourcePoolRegistration.Component
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6eecfefc8c542eeb3a06c509533060f8036d447e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131839"
---
# <a name="msvm_resourcepoolregistration-class"></a><span data-ttu-id="f0afd-103">\_Classe MSVM ResourcePoolRegistration</span><span class="sxs-lookup"><span data-stu-id="f0afd-103">Msvm\_ResourcePoolRegistration class</span></span>

<span data-ttu-id="f0afd-104">Registra un servizio che fornisce oggetti globali correlati al pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="f0afd-104">Registers a service that provides global resource pool-related objects.</span></span>

<span data-ttu-id="f0afd-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f0afd-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0afd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0afd-106">Syntax</span></span>

``` syntax
class Msvm_ResourcePoolRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition REF ResourceType;
  Msvm_ResourcePoolComponent  REF Component;
};
```

## <a name="members"></a><span data-ttu-id="f0afd-107">Members</span><span class="sxs-lookup"><span data-stu-id="f0afd-107">Members</span></span>

<span data-ttu-id="f0afd-108">La **classe \_ ResourcePoolRegistration di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f0afd-108">The **Msvm\_ResourcePoolRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="f0afd-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f0afd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f0afd-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f0afd-110">Properties</span></span>

<span data-ttu-id="f0afd-111">La **classe \_ ResourcePoolRegistration di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f0afd-111">The **Msvm\_ResourcePoolRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f0afd-112">**Componente**</span><span class="sxs-lookup"><span data-stu-id="f0afd-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0afd-113">Tipo di dati: **[ **MSVM \_ ResourcePoolComponent**](msvm-resourcepoolcomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="f0afd-113">Data type: **[**Msvm\_ResourcePoolComponent**](msvm-resourcepoolcomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f0afd-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f0afd-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0afd-115">Riferimento a un'istanza di che descrive l'oggetto COM che implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="f0afd-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="f0afd-116">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="f0afd-116">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0afd-117">Tipo di dati: **[ **MSVM \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="f0afd-117">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f0afd-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f0afd-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0afd-119">Riferimento a un'istanza di che descrive un tipo di risorsa supportato dal servizio.</span><span class="sxs-lookup"><span data-stu-id="f0afd-119">A reference to an instance that describes a resource type supported by the service.</span></span> <span data-ttu-id="f0afd-120">Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span><span class="sxs-lookup"><span data-stu-id="f0afd-120">This property is inherited from [**Msvm\_VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0afd-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0afd-121">Remarks</span></span>

<span data-ttu-id="f0afd-122">L'accesso alla **classe \_ ResourcePoolRegistration di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="f0afd-122">Access to the **Msvm\_ResourcePoolRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f0afd-123">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f0afd-123">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0afd-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0afd-124">Requirements</span></span>



| <span data-ttu-id="f0afd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0afd-125">Requirement</span></span> | <span data-ttu-id="f0afd-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f0afd-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0afd-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0afd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f0afd-128">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f0afd-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f0afd-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0afd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f0afd-130">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f0afd-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0afd-131">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f0afd-131">End of client support</span></span><br/>    | <span data-ttu-id="f0afd-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f0afd-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f0afd-133">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="f0afd-133">End of server support</span></span><br/>    | <span data-ttu-id="f0afd-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f0afd-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f0afd-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f0afd-135">Namespace</span></span><br/>                | <span data-ttu-id="f0afd-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f0afd-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f0afd-137">MOF</span><span class="sxs-lookup"><span data-stu-id="f0afd-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0afd-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0afd-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0afd-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f0afd-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0afd-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f0afd-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f0afd-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0afd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0afd-142">**\_VirtualizationComponentRegistration MSVM**</span><span class="sxs-lookup"><span data-stu-id="f0afd-142">**Msvm\_VirtualizationComponentRegistration**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[<span data-ttu-id="f0afd-143">**\_VirtualizationComponentRegistration MSVM**</span><span class="sxs-lookup"><span data-stu-id="f0afd-143">**Msvm\_VirtualizationComponentRegistration**</span></span>](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 


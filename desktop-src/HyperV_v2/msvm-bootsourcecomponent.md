---
description: Associa il \_ BootSourceSettingData MSVM al VirtualSystemSettingData globale MSVM \_ .
ms.assetid: DB2E66F1-CC2C-49FC-96CE-D9DE441AA809
title: Classe Msvm_BootSourceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceComponent
- Msvm_BootSourceComponent.GroupComponent
- Msvm_BootSourceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44dfe86fa7882b1b20e5b5abbbdaa9d4f37f231f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308342"
---
# <a name="msvm_bootsourcecomponent-class"></a><span data-ttu-id="eab23-103">\_Classe MSVM BootSourceComponent</span><span class="sxs-lookup"><span data-stu-id="eab23-103">Msvm\_BootSourceComponent class</span></span>

<span data-ttu-id="eab23-104">Associa il [**\_ BootSourceSettingData MSVM**](msvm-bootsourcesettingdata.md) al VirtualSystemSettingData globale [**MSVM \_**](msvm-virtualsystemsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="eab23-104">Associates the [**Msvm\_BootSourceSettingData**](msvm-bootsourcesettingdata.md) to the overall [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).</span></span> <span data-ttu-id="eab23-105">Questa classe deriva dal [**\_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="eab23-105">This class derives from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

<span data-ttu-id="eab23-106">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="eab23-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eab23-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eab23-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceComponent : CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="eab23-108">Members</span><span class="sxs-lookup"><span data-stu-id="eab23-108">Members</span></span>

<span data-ttu-id="eab23-109">La **classe \_ BootSourceComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="eab23-109">The **Msvm\_BootSourceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="eab23-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eab23-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eab23-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="eab23-111">Properties</span></span>

<span data-ttu-id="eab23-112">La **classe \_ BootSourceComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="eab23-112">The **Msvm\_BootSourceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eab23-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="eab23-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eab23-114">Tipo di dati: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="eab23-114">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="eab23-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eab23-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eab23-116">Riferimento all'elemento padre nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="eab23-116">Reference to the parent element in the association.</span></span> <span data-ttu-id="eab23-117">Questa proprietà viene ereditata [**dal \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="eab23-117">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> <dt>

<span data-ttu-id="eab23-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="eab23-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eab23-119">Tipo di dati: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="eab23-119">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="eab23-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="eab23-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eab23-121">Riferimento all'elemento figlio nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="eab23-121">Reference to the child element in the association.</span></span> <span data-ttu-id="eab23-122">Questa proprietà viene ereditata [**dal \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="eab23-122">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eab23-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eab23-123">Requirements</span></span>



| <span data-ttu-id="eab23-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="eab23-124">Requirement</span></span> | <span data-ttu-id="eab23-125">Valore</span><span class="sxs-lookup"><span data-stu-id="eab23-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eab23-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eab23-126">Minimum supported client</span></span><br/> | <span data-ttu-id="eab23-127">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="eab23-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="eab23-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eab23-128">Minimum supported server</span></span><br/> | <span data-ttu-id="eab23-129">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="eab23-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eab23-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="eab23-130">Namespace</span></span><br/>                | <span data-ttu-id="eab23-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="eab23-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="eab23-132">MOF</span><span class="sxs-lookup"><span data-stu-id="eab23-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eab23-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eab23-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eab23-134">DLL</span><span class="sxs-lookup"><span data-stu-id="eab23-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eab23-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eab23-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eab23-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eab23-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eab23-137">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="eab23-137">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="eab23-138">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="eab23-138">**CIM\_Component**</span></span>](/windows/desktop/CIMWin32Prov/cim-component)
</dt> <dt>

[<span data-ttu-id="eab23-139">**\_BootSourceSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="eab23-139">**Msvm\_BootSourceSettingData**</span></span>](msvm-bootsourcesettingdata.md)
</dt> <dt>

[<span data-ttu-id="eab23-140">**\_VirtualSystemSettingData MSVM**</span><span class="sxs-lookup"><span data-stu-id="eab23-140">**Msvm\_VirtualSystemSettingData**</span></span>](msvm-virtualsystemsettingdata.md)
</dt> </dl>

 


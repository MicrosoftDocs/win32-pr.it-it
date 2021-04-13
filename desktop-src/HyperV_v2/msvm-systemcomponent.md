---
description: Stabilisce un &\# 0034; parte della&\# 0034; relazione tra un sistema e qualsiasi elemento di sistema gestito di cui è composto.
ms.assetid: 6BF72E36-9B6C-4853-A553-DDAF65991C86
title: Classe Msvm_SystemComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemComponent
- Msvm_SystemComponent.GroupComponent
- Msvm_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee150793143b549c90d280eef287ee6a5afb66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401612"
---
# <a name="msvm_systemcomponent-class"></a><span data-ttu-id="7e2ec-103">\_Classe MSVM SystemComponent</span><span class="sxs-lookup"><span data-stu-id="7e2ec-103">Msvm\_SystemComponent class</span></span>

<span data-ttu-id="7e2ec-104">Stabilisce una relazione "parte di" tra un sistema e qualsiasi elemento di sistema gestito di cui è composto.</span><span class="sxs-lookup"><span data-stu-id="7e2ec-104">Establishes a "part of" relationship between a system and any managed system element of which it is composed.</span></span>

<span data-ttu-id="7e2ec-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7e2ec-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e2ec-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e2ec-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), Association, Aggregation]
class Msvm_SystemComponent : CIM_SystemComponent
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="7e2ec-107">Members</span><span class="sxs-lookup"><span data-stu-id="7e2ec-107">Members</span></span>

<span data-ttu-id="7e2ec-108">La **classe \_ SystemComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7e2ec-108">The **Msvm\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="7e2ec-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7e2ec-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e2ec-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7e2ec-110">Properties</span></span>

<span data-ttu-id="7e2ec-111">La **classe \_ SystemComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7e2ec-111">The **Msvm\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e2ec-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="7e2ec-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e2ec-113">Tipo di dati: **[ **\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)**</span><span class="sxs-lookup"><span data-stu-id="7e2ec-113">Data type: **[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system)**</span></span>
</dt> <dt>

<span data-ttu-id="7e2ec-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7e2ec-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e2ec-115">Elemento padre nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="7e2ec-115">The parent element in the association.</span></span> <span data-ttu-id="7e2ec-116">Questa proprietà viene ereditata da [**CIM \_ SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span><span class="sxs-lookup"><span data-stu-id="7e2ec-116">This property is inherited from [**CIM\_SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span></span>

</dd> <dt>

<span data-ttu-id="7e2ec-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="7e2ec-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e2ec-118">Tipo di dati: **[ **CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**</span><span class="sxs-lookup"><span data-stu-id="7e2ec-118">Data type: **[**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**</span></span>
</dt> <dt>

<span data-ttu-id="7e2ec-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7e2ec-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e2ec-120">Elemento figlio nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="7e2ec-120">The child element in the association.</span></span> <span data-ttu-id="7e2ec-121">Questa proprietà viene ereditata da [**CIM \_ SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span><span class="sxs-lookup"><span data-stu-id="7e2ec-121">This property is inherited from [**CIM\_SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e2ec-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e2ec-122">Requirements</span></span>



| <span data-ttu-id="7e2ec-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e2ec-123">Requirement</span></span> | <span data-ttu-id="7e2ec-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7e2ec-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e2ec-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e2ec-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7e2ec-126">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7e2ec-126">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="7e2ec-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e2ec-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7e2ec-128">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e2ec-128">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7e2ec-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7e2ec-129">Namespace</span></span><br/>                | <span data-ttu-id="7e2ec-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7e2ec-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7e2ec-131">MOF</span><span class="sxs-lookup"><span data-stu-id="7e2ec-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e2ec-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e2ec-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e2ec-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7e2ec-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e2ec-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7e2ec-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


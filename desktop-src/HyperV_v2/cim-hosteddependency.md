---
description: Rappresenta un'associazione in cui un elemento gestito è ospitato da un altro oggetto.
ms.assetid: ae8476f7-38a4-4d08-a7dc-21e120d3cbe1
title: Classe CIM_HostedDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedDependency
- CIM_HostedDependency.Antecedent
- CIM_HostedDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 551931fd88fac88f85bcc8ffd51423538de3bb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305667"
---
# <a name="cim_hosteddependency-class"></a><span data-ttu-id="53bb7-103">CIM \_ HostedDependency (classe)</span><span class="sxs-lookup"><span data-stu-id="53bb7-103">CIM\_HostedDependency class</span></span>

<span data-ttu-id="53bb7-104">Rappresenta un'associazione in cui un elemento gestito è ospitato da un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="53bb7-104">Represents an association where a managed element is hosted by another.</span></span>

## <a name="syntax"></a><span data-ttu-id="53bb7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53bb7-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_HostedDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="53bb7-106">Members</span><span class="sxs-lookup"><span data-stu-id="53bb7-106">Members</span></span>

<span data-ttu-id="53bb7-107">La classe **CIM \_ HostedDependency** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="53bb7-107">The **CIM\_HostedDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="53bb7-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="53bb7-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53bb7-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="53bb7-109">Properties</span></span>

<span data-ttu-id="53bb7-110">La classe **CIM \_ HostedDependency** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="53bb7-110">The **CIM\_HostedDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53bb7-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="53bb7-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53bb7-112">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="53bb7-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="53bb7-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="53bb7-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53bb7-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="53bb7-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="53bb7-115">Elemento gestito dall'host.</span><span class="sxs-lookup"><span data-stu-id="53bb7-115">The host managed element.</span></span>

</dd> <dt>

<span data-ttu-id="53bb7-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="53bb7-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53bb7-117">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="53bb7-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="53bb7-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="53bb7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53bb7-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="53bb7-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="53bb7-120">Elemento gestito ospitato.</span><span class="sxs-lookup"><span data-stu-id="53bb7-120">The hosted managed element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53bb7-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53bb7-121">Requirements</span></span>



| <span data-ttu-id="53bb7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="53bb7-122">Requirement</span></span> | <span data-ttu-id="53bb7-123">Valore</span><span class="sxs-lookup"><span data-stu-id="53bb7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53bb7-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53bb7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="53bb7-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="53bb7-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="53bb7-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53bb7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="53bb7-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53bb7-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="53bb7-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="53bb7-128">Namespace</span></span><br/>                | <span data-ttu-id="53bb7-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="53bb7-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="53bb7-130">MOF</span><span class="sxs-lookup"><span data-stu-id="53bb7-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53bb7-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53bb7-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="53bb7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="53bb7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53bb7-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="53bb7-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="53bb7-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53bb7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53bb7-135">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="53bb7-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


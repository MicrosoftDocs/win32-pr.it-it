---
description: Rappresenta un'associazione generica tra un elemento gestito padre e un elemento gestito figlio in cui l'elemento figlio rappresenta un componente o parte dell'elemento padre.
ms.assetid: b5cef452-2d00-483c-8e70-f804f1e3536b
title: Classe CIM_Component (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56ff83a4da51ba18205a8d8ab5e6e57ea1a7794b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313383"
---
# <a name="cim_component-class-hyper-v-management"></a><span data-ttu-id="d485c-103">Classe CIM_Component (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="d485c-103">CIM_Component class (Hyper-V management)</span></span>

<span data-ttu-id="d485c-104">Rappresenta un'associazione generica tra un elemento gestito padre e un elemento gestito figlio in cui l'elemento figlio rappresenta un componente o parte dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="d485c-104">Represents a generic association between a parent managed element and a child managed element where the child represents a component or part of the parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="d485c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d485c-105">Syntax</span></span>

``` syntax
[Association, Abstract, Aggregation, Version("2.7.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="d485c-106">Members</span><span class="sxs-lookup"><span data-stu-id="d485c-106">Members</span></span>

<span data-ttu-id="d485c-107">La classe del **\_ componente CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d485c-107">The **CIM\_Component** class has these types of members:</span></span>

-   [<span data-ttu-id="d485c-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d485c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d485c-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d485c-109">Properties</span></span>

<span data-ttu-id="d485c-110">La classe del **\_ componente CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d485c-110">The **CIM\_Component** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d485c-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="d485c-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d485c-112">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="d485c-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d485c-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d485c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d485c-114">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**aggregazione**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d485c-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d485c-115">Elemento padre nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="d485c-115">The parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="d485c-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d485c-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d485c-117">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="d485c-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d485c-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d485c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d485c-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d485c-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d485c-120">Elemento figlio nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="d485c-120">The child element in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d485c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d485c-121">Requirements</span></span>



| <span data-ttu-id="d485c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d485c-122">Requirement</span></span> | <span data-ttu-id="d485c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d485c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d485c-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d485c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d485c-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d485c-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d485c-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d485c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d485c-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d485c-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d485c-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d485c-128">Namespace</span></span><br/>                | <span data-ttu-id="d485c-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d485c-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d485c-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d485c-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d485c-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d485c-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d485c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d485c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d485c-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d485c-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


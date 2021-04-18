---
description: Rappresenta un'associazione generica utilizzata per stabilire relazioni di dipendenza tra gli elementi gestiti.
ms.assetid: a81beedc-5473-49a6-8e7f-67e831d3e8bc
title: Classe CIM_Dependency (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Dependency
- CIM_Dependency.Antecedent
- CIM_Dependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4e85f59b190e0024fc34489315fa2fae1c0d6b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308360"
---
# <a name="cim_dependency-class-hyper-v-management"></a><span data-ttu-id="45eb8-103">Classe CIM_Dependency (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="45eb8-103">CIM_Dependency class (Hyper-V management)</span></span>

<span data-ttu-id="45eb8-104">Rappresenta un'associazione generica utilizzata per stabilire relazioni di dipendenza tra gli elementi gestiti.</span><span class="sxs-lookup"><span data-stu-id="45eb8-104">Represents a generic association used to establish dependency relationships between managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="45eb8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45eb8-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="45eb8-106">Members</span><span class="sxs-lookup"><span data-stu-id="45eb8-106">Members</span></span>

<span data-ttu-id="45eb8-107">La classe di **\_ dipendenza CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="45eb8-107">The **CIM\_Dependency** class has these types of members:</span></span>

-   [<span data-ttu-id="45eb8-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="45eb8-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="45eb8-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="45eb8-109">Properties</span></span>

<span data-ttu-id="45eb8-110">La classe di **\_ dipendenza CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="45eb8-110">The **CIM\_Dependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45eb8-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="45eb8-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45eb8-112">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="45eb8-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="45eb8-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45eb8-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45eb8-114">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="45eb8-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="45eb8-115">Oggetto indipendente in questa associazione.</span><span class="sxs-lookup"><span data-stu-id="45eb8-115">The independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="45eb8-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="45eb8-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45eb8-117">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="45eb8-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="45eb8-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45eb8-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45eb8-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="45eb8-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="45eb8-120">Oggetto dipendente nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="45eb8-120">The dependent object in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45eb8-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45eb8-121">Requirements</span></span>



| <span data-ttu-id="45eb8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="45eb8-122">Requirement</span></span> | <span data-ttu-id="45eb8-123">Valore</span><span class="sxs-lookup"><span data-stu-id="45eb8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45eb8-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45eb8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="45eb8-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="45eb8-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="45eb8-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45eb8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="45eb8-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45eb8-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="45eb8-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="45eb8-128">Namespace</span></span><br/>                | <span data-ttu-id="45eb8-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="45eb8-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="45eb8-130">MOF</span><span class="sxs-lookup"><span data-stu-id="45eb8-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45eb8-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45eb8-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="45eb8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="45eb8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45eb8-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="45eb8-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


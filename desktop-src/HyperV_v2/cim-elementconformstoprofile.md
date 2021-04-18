---
description: Rappresenta un'associazione in cui un elemento gestito è conforme allo standard di un profilo registrato.
ms.assetid: 9d5704b6-c764-4f68-bce3-384d5a244e28
title: Classe CIM_ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConformsToProfile
- CIM_ElementConformsToProfile.ConformantStandard
- CIM_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7034001641029099d1b52090b3cc518b6589dc50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308343"
---
# <a name="cim_elementconformstoprofile-class"></a><span data-ttu-id="fd9dd-103">CIM \_ ElementConformsToProfile (classe)</span><span class="sxs-lookup"><span data-stu-id="fd9dd-103">CIM\_ElementConformsToProfile class</span></span>

<span data-ttu-id="fd9dd-104">Rappresenta un'associazione in cui un elemento gestito è conforme allo standard di un profilo registrato.</span><span class="sxs-lookup"><span data-stu-id="fd9dd-104">Represents an association in which a managed element conforms to the standard of a registered profile.</span></span> <span data-ttu-id="fd9dd-105">Questa associazione viene in genere applicata a un'istanza di livello superiore, ad esempio un sistema, uno spazio dei nomi o un servizio.</span><span class="sxs-lookup"><span data-stu-id="fd9dd-105">This association usually applies to a higher level instance, such as a system, namespace, or service.</span></span> <span data-ttu-id="fd9dd-106">Quando viene applicato a un'istanza di livello superiore, tutte le parti costituenti devono comportarsi in modo appropriato per supportare la conformità della funzione gestita al RegisteredProfile denominato.</span><span class="sxs-lookup"><span data-stu-id="fd9dd-106">When applied to a higher level instance, all constituent parts MUST behave appropriately in support of the ManagedElement's conformance to the named RegisteredProfile.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd9dd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd9dd-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Interop")]
class CIM_ElementConformsToProfile
{
  CIM_RegisteredProfile REF ConformantStandard;
  CIM_ManagedElement    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="fd9dd-108">Members</span><span class="sxs-lookup"><span data-stu-id="fd9dd-108">Members</span></span>

<span data-ttu-id="fd9dd-109">La classe **CIM \_ ElementConformsToProfile** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fd9dd-109">The **CIM\_ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="fd9dd-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fd9dd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd9dd-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fd9dd-111">Properties</span></span>

<span data-ttu-id="fd9dd-112">La classe **CIM \_ ElementConformsToProfile** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fd9dd-112">The **CIM\_ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd9dd-113">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="fd9dd-113">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd9dd-114">Tipo di dati: **CIM \_ RegisteredProfile**</span><span class="sxs-lookup"><span data-stu-id="fd9dd-114">Data type: **CIM\_RegisteredProfile**</span></span>
</dt> <dt>

<span data-ttu-id="fd9dd-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd9dd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd9dd-116">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd9dd-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd9dd-117">Profilo registrato a cui è conforme l'elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="fd9dd-117">The registered profile to which the managed element conforms.</span></span>

</dd> <dt>

<span data-ttu-id="fd9dd-118">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="fd9dd-118">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd9dd-119">Tipo di dati: **CIM \_ Managed**</span><span class="sxs-lookup"><span data-stu-id="fd9dd-119">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="fd9dd-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd9dd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd9dd-121">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd9dd-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd9dd-122">Elemento gestito conforme al profilo registrato.</span><span class="sxs-lookup"><span data-stu-id="fd9dd-122">The managed element that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd9dd-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd9dd-123">Requirements</span></span>



| <span data-ttu-id="fd9dd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd9dd-124">Requirement</span></span> | <span data-ttu-id="fd9dd-125">Valore</span><span class="sxs-lookup"><span data-stu-id="fd9dd-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9dd-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd9dd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fd9dd-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fd9dd-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="fd9dd-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd9dd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fd9dd-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fd9dd-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="fd9dd-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fd9dd-130">Namespace</span></span><br/>                | <span data-ttu-id="fd9dd-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="fd9dd-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fd9dd-132">MOF</span><span class="sxs-lookup"><span data-stu-id="fd9dd-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd9dd-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd9dd-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd9dd-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fd9dd-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd9dd-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fd9dd-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


---
description: Definisce i profili registrati a cui è conforme il sistema a cui si fa riferimento.
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Classe Msvm_ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementConformsToProfile
- Msvm_ElementConformsToProfile.ConformantStandard
- Msvm_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b0afdc7dd9d55a036de0695f9a88a95d2b01308
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314831"
---
# <a name="msvm_elementconformstoprofile-class"></a><span data-ttu-id="04ab1-103">\_Classe MSVM ElementConformsToProfile</span><span class="sxs-lookup"><span data-stu-id="04ab1-103">Msvm\_ElementConformsToProfile class</span></span>

<span data-ttu-id="04ab1-104">Definisce i profili registrati a cui è conforme il sistema a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="04ab1-104">Defines the registered profiles to which the referenced system conforms.</span></span> <span data-ttu-id="04ab1-105">Questa associazione può essere applicata a qualsiasi elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="04ab1-105">This association may apply to any managed element.</span></span> <span data-ttu-id="04ab1-106">L'utilizzo tipico lo applicherà a un'istanza di livello superiore, ad esempio un sistema, uno spazio dei nomi o un servizio.</span><span class="sxs-lookup"><span data-stu-id="04ab1-106">Typical usage will apply it to a higher level instance, such as a System, Namespace, or Service.</span></span> <span data-ttu-id="04ab1-107">Quando viene applicato a un'istanza di livello superiore, tutte le parti costituenti devono comportarsi in modo appropriato per supportare la conformità dell'elemento gestito al profilo registrato denominato.</span><span class="sxs-lookup"><span data-stu-id="04ab1-107">When applied to a higher level instance, all constituent parts must behave appropriately in support of the managed element's conformance to the named registered profile.</span></span>

<span data-ttu-id="04ab1-108">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="04ab1-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="04ab1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04ab1-109">Syntax</span></span>

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="04ab1-110">Members</span><span class="sxs-lookup"><span data-stu-id="04ab1-110">Members</span></span>

<span data-ttu-id="04ab1-111">La **classe \_ ElementConformsToProfile di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="04ab1-111">The **Msvm\_ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="04ab1-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="04ab1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="04ab1-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="04ab1-113">Properties</span></span>

<span data-ttu-id="04ab1-114">La **classe \_ ElementConformsToProfile di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="04ab1-114">The **Msvm\_ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04ab1-115">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="04ab1-115">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04ab1-116">Tipo di dati: **[ **MSVM \_ RegisteredProfile**](msvm-registeredprofile.md)**</span><span class="sxs-lookup"><span data-stu-id="04ab1-116">Data type: **[**Msvm\_RegisteredProfile**](msvm-registeredprofile.md)**</span></span>
</dt> <dt>

<span data-ttu-id="04ab1-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="04ab1-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04ab1-118">Qualificatori: [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="04ab1-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="04ab1-119">Riferimento a un'istanza della classe [**MSVM \_ RegisteredProfile**](msvm-registeredprofile.md) che rappresenta il profilo registrato a cui è conforme il sistema.</span><span class="sxs-lookup"><span data-stu-id="04ab1-119">A reference to an instance of the [**Msvm\_RegisteredProfile**](msvm-registeredprofile.md) class that represents the registered profile to which the system conforms.</span></span>

</dd> <dt>

<span data-ttu-id="04ab1-120">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="04ab1-120">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04ab1-121">Tipo di dati: **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="04ab1-121">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="04ab1-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="04ab1-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04ab1-123">Qualificatori: [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="04ab1-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="04ab1-124">Riferimento a un'istanza della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta il sistema conforme al profilo registrato.</span><span class="sxs-lookup"><span data-stu-id="04ab1-124">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the system that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04ab1-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04ab1-125">Requirements</span></span>



| <span data-ttu-id="04ab1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="04ab1-126">Requirement</span></span> | <span data-ttu-id="04ab1-127">Valore</span><span class="sxs-lookup"><span data-stu-id="04ab1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04ab1-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04ab1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="04ab1-129">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="04ab1-129">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="04ab1-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04ab1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="04ab1-131">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="04ab1-131">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="04ab1-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="04ab1-132">Namespace</span></span><br/>                | <span data-ttu-id="04ab1-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="04ab1-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="04ab1-134">MOF</span><span class="sxs-lookup"><span data-stu-id="04ab1-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04ab1-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04ab1-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="04ab1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="04ab1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04ab1-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="04ab1-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


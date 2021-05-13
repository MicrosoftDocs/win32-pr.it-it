---
description: Definisce i profili registrati a cui è conforme il sistema di riferimento.
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Msvm_ElementConformsToProfile classe
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
ms.openlocfilehash: e9b4e257c2ebc0584a8291461439f75238599d35
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843282"
---
# <a name="msvm_elementconformstoprofile-class"></a><span data-ttu-id="91af3-103">Classe Msvm \_ ElementConformsToProfile</span><span class="sxs-lookup"><span data-stu-id="91af3-103">Msvm\_ElementConformsToProfile class</span></span>

<span data-ttu-id="91af3-104">Definisce i profili registrati a cui è conforme il sistema di riferimento.</span><span class="sxs-lookup"><span data-stu-id="91af3-104">Defines the registered profiles to which the referenced system conforms.</span></span> <span data-ttu-id="91af3-105">Questa associazione può essere applicata a qualsiasi elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="91af3-105">This association may apply to any managed element.</span></span> <span data-ttu-id="91af3-106">L'utilizzo tipico lo applicherà a un'istanza di livello superiore, ad esempio un sistema, uno spazio dei nomi o un servizio.</span><span class="sxs-lookup"><span data-stu-id="91af3-106">Typical usage will apply it to a higher level instance, such as a System, Namespace, or Service.</span></span> <span data-ttu-id="91af3-107">Quando viene applicato a un'istanza di livello superiore, tutte le parti costituenti devono comportarsi in modo appropriato per supportare la conformità dell'elemento gestito al profilo registrato denominato.</span><span class="sxs-lookup"><span data-stu-id="91af3-107">When applied to a higher level instance, all constituent parts must behave appropriately in support of the managed element's conformance to the named registered profile.</span></span>

<span data-ttu-id="91af3-108">La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="91af3-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="91af3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91af3-109">Syntax</span></span>

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="91af3-110">Members</span><span class="sxs-lookup"><span data-stu-id="91af3-110">Members</span></span>

<span data-ttu-id="91af3-111">La **classe Msvm \_ ElementConformsToProfile** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="91af3-111">The **Msvm\_ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="91af3-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="91af3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="91af3-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="91af3-113">Properties</span></span>

<span data-ttu-id="91af3-114">La **classe Msvm \_ ElementConformsToProfile** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="91af3-114">The **Msvm\_ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="91af3-115">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="91af3-115">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91af3-116">Tipo di dati: **[ **Msvm \_ RegisteredProfile**](msvm-registeredprofile.md)**</span><span class="sxs-lookup"><span data-stu-id="91af3-116">Data type: **[**Msvm\_RegisteredProfile**](msvm-registeredprofile.md)**</span></span>
</dt> <dt>

<span data-ttu-id="91af3-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="91af3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91af3-118">Qualificatori: [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="91af3-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="91af3-119">Riferimento a un'istanza della [**classe Msvm \_ RegisteredProfile**](msvm-registeredprofile.md) che rappresenta il profilo registrato a cui il sistema è conforme.</span><span class="sxs-lookup"><span data-stu-id="91af3-119">A reference to an instance of the [**Msvm\_RegisteredProfile**](msvm-registeredprofile.md) class that represents the registered profile to which the system conforms.</span></span>

</dd> <dt>

<span data-ttu-id="91af3-120">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="91af3-120">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91af3-121">Tipo di dati: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="91af3-121">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="91af3-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="91af3-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91af3-123">Qualificatori: [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="91af3-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="91af3-124">Riferimento a un'istanza della [**classe Msvm \_ ComputerSystem**](msvm-computersystem.md) che rappresenta il sistema conforme al profilo registrato.</span><span class="sxs-lookup"><span data-stu-id="91af3-124">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the system that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91af3-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91af3-125">Requirements</span></span>



| <span data-ttu-id="91af3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="91af3-126">Requirement</span></span> | <span data-ttu-id="91af3-127">Valore</span><span class="sxs-lookup"><span data-stu-id="91af3-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91af3-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91af3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="91af3-129">Windows 8.1 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="91af3-129">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="91af3-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91af3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="91af3-131">Solo app desktop di Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="91af3-131">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="91af3-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="91af3-132">Namespace</span></span><br/>                | <span data-ttu-id="91af3-133">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="91af3-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="91af3-134">MOF</span><span class="sxs-lookup"><span data-stu-id="91af3-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91af3-135"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="91af3-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="91af3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="91af3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91af3-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="91af3-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


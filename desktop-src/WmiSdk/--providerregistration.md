---
description: Funge da classe padre per le classi di registrazione per diversi tipi di provider.
ms.assetid: 1e5d95cb-0961-4be8-b80a-37b598c9ccfe
ms.tgt_platform: multiple
title: Classe __ProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7359f3d5cdcfb2447b724fd6d369a1029d8fcd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131771"
---
# <a name="__providerregistration-class"></a><span data-ttu-id="d8789-103">\_\_Classe ProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="d8789-103">\_\_ProviderRegistration class</span></span>

<span data-ttu-id="d8789-104">La classe di sistema astratta **\_ \_ ProviderRegistration** funge da classe padre per le classi di registrazione per diversi tipi di provider.</span><span class="sxs-lookup"><span data-stu-id="d8789-104">The **\_\_ProviderRegistration** abstract system class serves as the parent class for registration classes for various types of providers.</span></span>

<span data-ttu-id="d8789-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d8789-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d8789-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="d8789-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8789-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8789-107">Syntax</span></span>

``` syntax
[abstract]
class __ProviderRegistration : __SystemClass
{
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="d8789-108">Members</span><span class="sxs-lookup"><span data-stu-id="d8789-108">Members</span></span>

<span data-ttu-id="d8789-109">La classe **\_ \_ ProviderRegistration** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d8789-109">The **\_\_ProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="d8789-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d8789-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8789-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d8789-111">Properties</span></span>

<span data-ttu-id="d8789-112">La classe **\_ \_ ProviderRegistration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d8789-112">The **\_\_ProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d8789-113">**provider**</span><span class="sxs-lookup"><span data-stu-id="d8789-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8789-114">Tipo di dati: **\_ \_ provider**</span><span class="sxs-lookup"><span data-stu-id="d8789-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="d8789-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d8789-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d8789-116">Riferimento a un'istanza del [**\_ \_ provider**](--provider.md) che rappresenta il percorso dell'oggetto al provider.</span><span class="sxs-lookup"><span data-stu-id="d8789-116">Reference to an instance of [**\_\_Provider**](--provider.md) representing the object path to the provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8789-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8789-117">Remarks</span></span>

<span data-ttu-id="d8789-118">La classe **\_ \_ ProviderRegistration** deriva da [**\_ \_ SystemClass**](--systemclass.md), che non dispone di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d8789-118">The **\_\_ProviderRegistration** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="d8789-119">Le istanze della classe di sistema **\_ \_ ProviderRegistration** non vengono mai create.</span><span class="sxs-lookup"><span data-stu-id="d8789-119">Instances of the **\_\_ProviderRegistration** system class are never created.</span></span> <span data-ttu-id="d8789-120">Le classi utilizzate dai provider per creare istanze per la registrazione derivano direttamente o indirettamente da questa classe.</span><span class="sxs-lookup"><span data-stu-id="d8789-120">The classes that providers use to create instances for registration derive either directly or indirectly from this class.</span></span> <span data-ttu-id="d8789-121">Tali classi sono:</span><span class="sxs-lookup"><span data-stu-id="d8789-121">These classes are:</span></span>

[<span data-ttu-id="d8789-122">**\_\_ClassProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="d8789-122">**\_\_ClassProviderRegistration**</span></span>](--classproviderregistration.md)

[<span data-ttu-id="d8789-123">**\_\_EventConsumerProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="d8789-123">**\_\_EventConsumerProviderRegistration**</span></span>](--eventconsumerproviderregistration.md)

[<span data-ttu-id="d8789-124">**\_\_EventProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="d8789-124">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)

[<span data-ttu-id="d8789-125">**\_\_InstanceProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="d8789-125">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)

[<span data-ttu-id="d8789-126">**\_\_MethodProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="d8789-126">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)

[<span data-ttu-id="d8789-127">**\_\_ObjectProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="d8789-127">**\_\_ObjectProviderRegistration**</span></span>](--objectproviderregistration.md)

[<span data-ttu-id="d8789-128">**\_\_PropertyProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="d8789-128">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)

<span data-ttu-id="d8789-129">Solo gli amministratori possono registrare o eliminare un provider creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e registrando tale provider.</span><span class="sxs-lookup"><span data-stu-id="d8789-129">Only administrators can register or delete a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and registering it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8789-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8789-130">Requirements</span></span>



| <span data-ttu-id="d8789-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8789-131">Requirement</span></span> | <span data-ttu-id="d8789-132">Valore</span><span class="sxs-lookup"><span data-stu-id="d8789-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d8789-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8789-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d8789-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8789-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d8789-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8789-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d8789-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8789-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="d8789-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d8789-137">Namespace</span></span><br/>                | <span data-ttu-id="d8789-138">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="d8789-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="d8789-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8789-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8789-140">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="d8789-140">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="d8789-141">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="d8789-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="d8789-142">Registrazione di un provider</span><span class="sxs-lookup"><span data-stu-id="d8789-142">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 


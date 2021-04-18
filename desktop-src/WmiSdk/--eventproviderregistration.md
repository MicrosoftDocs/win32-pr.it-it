---
description: Utilizzato per registrare i provider di eventi con Strumentazione gestione Windows (WMI).
ms.assetid: d87f61a8-5549-4f33-ba67-31b5d72b5282
ms.tgt_platform: multiple
title: Classe __EventProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: caaad1b4ab03cfc1b43e4239b9144d3ceeade82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314606"
---
# <a name="__eventproviderregistration-class"></a><span data-ttu-id="dde4f-103">\_\_Classe EventProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="dde4f-103">\_\_EventProviderRegistration class</span></span>

<span data-ttu-id="dde4f-104">La classe di sistema **\_ \_ EventProviderRegistration** viene utilizzata per registrare i provider di eventi con Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="dde4f-104">The **\_\_EventProviderRegistration** system class is used to register event providers with Windows Management Instrumentation (WMI).</span></span>

<span data-ttu-id="dde4f-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="dde4f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="dde4f-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="dde4f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dde4f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dde4f-107">Syntax</span></span>

``` syntax
class __EventProviderRegistration : __ProviderRegistration
{
  string         EventQueryList[];
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="dde4f-108">Members</span><span class="sxs-lookup"><span data-stu-id="dde4f-108">Members</span></span>

<span data-ttu-id="dde4f-109">La classe **\_ \_ EventProviderRegistration** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dde4f-109">The **\_\_EventProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="dde4f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dde4f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dde4f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dde4f-111">Properties</span></span>

<span data-ttu-id="dde4f-112">La classe **\_ \_ EventProviderRegistration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="dde4f-112">The **\_\_EventProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dde4f-113">**EventQueryList**</span><span class="sxs-lookup"><span data-stu-id="dde4f-113">**EventQueryList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dde4f-114">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="dde4f-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dde4f-115">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dde4f-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dde4f-116">Una o più query WQL (Strumentazione gestione Windows Query Language) che descrivono gli eventi supportati dal provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="dde4f-116">One or more Windows Management Instrumentation Query Language (WQL) queries that describe the events that the event provider supports.</span></span>

</dd> <dt>

<span data-ttu-id="dde4f-117">**provider**</span><span class="sxs-lookup"><span data-stu-id="dde4f-117">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dde4f-118">Tipo di dati: **\_ \_ provider**</span><span class="sxs-lookup"><span data-stu-id="dde4f-118">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="dde4f-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dde4f-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dde4f-120">Percorso dell'oggetto per il provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="dde4f-120">Object path to the event provider.</span></span> <span data-ttu-id="dde4f-121">Questa proprietà viene ereditata da [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="dde4f-121">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dde4f-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="dde4f-122">Remarks</span></span>

<span data-ttu-id="dde4f-123">Solo gli amministratori possono registrare o eliminare un provider di eventi creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ EventProviderRegistration**](--eventconsumerproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="dde4f-123">Only administrators can register or delete an event provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventconsumerproviderregistration.md).</span></span> <span data-ttu-id="dde4f-124">La classe **\_ \_ EventProviderRegistration** deriva da [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="dde4f-124">The **\_\_EventProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dde4f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dde4f-125">Requirements</span></span>



| <span data-ttu-id="dde4f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="dde4f-126">Requirement</span></span> | <span data-ttu-id="dde4f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="dde4f-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="dde4f-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dde4f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dde4f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dde4f-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="dde4f-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dde4f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dde4f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dde4f-131">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="dde4f-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dde4f-132">Namespace</span></span><br/>                | <span data-ttu-id="dde4f-133">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="dde4f-133">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="dde4f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dde4f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dde4f-135">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="dde4f-135">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="dde4f-136">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="dde4f-136">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="dde4f-137">Registrazione di un provider di eventi</span><span class="sxs-lookup"><span data-stu-id="dde4f-137">Registering an Event Provider</span></span>](registering-an-event-provider.md)
</dt> <dt>

[<span data-ttu-id="dde4f-138">Scrittura di un provider di eventi</span><span class="sxs-lookup"><span data-stu-id="dde4f-138">Writing an Event Provider</span></span>](writing-an-event-provider.md)
</dt> </dl>

 


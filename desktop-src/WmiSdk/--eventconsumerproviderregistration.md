---
description: Registra i provider di consumer di eventi con WMI.
ms.assetid: 31ff43dc-dc70-4ba0-866f-37445912f837
ms.tgt_platform: multiple
title: Classe __EventConsumerProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 38552519221018735c3c7543d9a1f3f2d4b680e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884001"
---
# <a name="__eventconsumerproviderregistration-class"></a><span data-ttu-id="55665-103">\_\_Classe EventConsumerProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="55665-103">\_\_EventConsumerProviderRegistration class</span></span>

<span data-ttu-id="55665-104">La classe di sistema **\_ \_ EventConsumerProviderRegistration** registra i provider di consumer di eventi con WMI.</span><span class="sxs-lookup"><span data-stu-id="55665-104">The **\_\_EventConsumerProviderRegistration** system class registers event consumer providers with WMI.</span></span>

<span data-ttu-id="55665-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="55665-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="55665-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="55665-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="55665-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55665-107">Syntax</span></span>

``` syntax
class __EventConsumerProviderRegistration : __ProviderRegistration
{
  string         ConsumerClassNames[];
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="55665-108">Members</span><span class="sxs-lookup"><span data-stu-id="55665-108">Members</span></span>

<span data-ttu-id="55665-109">La classe **\_ \_ EventConsumerProviderRegistration** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="55665-109">The **\_\_EventConsumerProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="55665-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="55665-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55665-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="55665-111">Properties</span></span>

<span data-ttu-id="55665-112">La classe **\_ \_ EventConsumerProviderRegistration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="55665-112">The **\_\_EventConsumerProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55665-113">**ConsumerClassNames**</span><span class="sxs-lookup"><span data-stu-id="55665-113">**ConsumerClassNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55665-114">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="55665-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="55665-115">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="55665-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="55665-116">Matrice di nomi delle classi di consumer logiche supportate dal provider di consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="55665-116">Array of names of the logical consumer classes that the event consumer provider supports.</span></span>

</dd> <dt>

<span data-ttu-id="55665-117">**provider**</span><span class="sxs-lookup"><span data-stu-id="55665-117">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55665-118">Tipo di dati: **\_ \_ provider**</span><span class="sxs-lookup"><span data-stu-id="55665-118">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="55665-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="55665-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55665-120">Percorso dell'oggetto per il provider.</span><span class="sxs-lookup"><span data-stu-id="55665-120">Object path to the provider.</span></span> <span data-ttu-id="55665-121">Questa proprietà viene ereditata da [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="55665-121">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55665-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="55665-122">Remarks</span></span>

<span data-ttu-id="55665-123">La classe **\_ \_ EventConsumerProviderRegistration** deriva da [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="55665-123">The **\_\_EventConsumerProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55665-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55665-124">Requirements</span></span>



| <span data-ttu-id="55665-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="55665-125">Requirement</span></span> | <span data-ttu-id="55665-126">Valore</span><span class="sxs-lookup"><span data-stu-id="55665-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="55665-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55665-127">Minimum supported client</span></span><br/> | <span data-ttu-id="55665-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55665-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="55665-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55665-129">Minimum supported server</span></span><br/> | <span data-ttu-id="55665-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55665-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="55665-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="55665-131">Namespace</span></span><br/>                | <span data-ttu-id="55665-132">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="55665-132">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="55665-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55665-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55665-134">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="55665-134">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="55665-135">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="55665-135">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="55665-136">Registrazione di un provider di consumer di eventi</span><span class="sxs-lookup"><span data-stu-id="55665-136">Registering an Event Consumer Provider</span></span>](registering-an-event-consumer-provider.md)
</dt> <dt>

[<span data-ttu-id="55665-137">Scrittura di un provider di consumer di eventi</span><span class="sxs-lookup"><span data-stu-id="55665-137">Writing an Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)
</dt> </dl>

 


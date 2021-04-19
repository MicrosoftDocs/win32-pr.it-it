---
description: Rappresenta un evento di aggregazione di diversi eventi intrinseci o estrinseci singoli.
ms.assetid: 99afa390-01fe-4a13-ba21-27587470f111
ms.tgt_platform: multiple
title: Classe __AggregateEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AggregateEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f93a962e57452ac555214e42f00af8ac8a4ea3db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317604"
---
# <a name="__aggregateevent-class"></a><span data-ttu-id="2a794-103">\_\_Classe AggregateEvent</span><span class="sxs-lookup"><span data-stu-id="2a794-103">\_\_AggregateEvent class</span></span>

<span data-ttu-id="2a794-104">La classe di sistema **\_ \_ AggregateEvent** rappresenta un evento di aggregazione di più eventi intrinseci o estrinseci singoli.</span><span class="sxs-lookup"><span data-stu-id="2a794-104">The **\_\_AggregateEvent** system class represents an aggregate event of several individual intrinsic or extrinsic events.</span></span> <span data-ttu-id="2a794-105">WMI genera un'istanza di **\_ \_ AggregateEvent** anziché di un [**\_ \_ evento**](--event.md) quando gli utenti effettuano la registrazione con la clausola [Group](group-clause.md) into nella query di eventi.</span><span class="sxs-lookup"><span data-stu-id="2a794-105">WMI generates an instance of **\_\_AggregateEvent** rather than [**\_\_Event**](--event.md) when consumers register with the [GROUP WITHIN](group-clause.md) clause in their event query.</span></span>

<span data-ttu-id="2a794-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2a794-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2a794-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="2a794-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a794-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a794-108">Syntax</span></span>

``` syntax
class __AggregateEvent : __IndicationRelated
{
  uint32 NumberOfEvents;
  object Representative;
};
```

## <a name="members"></a><span data-ttu-id="2a794-109">Members</span><span class="sxs-lookup"><span data-stu-id="2a794-109">Members</span></span>

<span data-ttu-id="2a794-110">La classe **\_ \_ AggregateEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2a794-110">The **\_\_AggregateEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="2a794-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2a794-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a794-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2a794-112">Properties</span></span>

<span data-ttu-id="2a794-113">La classe **\_ \_ AggregateEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2a794-113">The **\_\_AggregateEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a794-114">**NumberOfEvents**</span><span class="sxs-lookup"><span data-stu-id="2a794-114">**NumberOfEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a794-115">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2a794-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2a794-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a794-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a794-117">Numero di eventi combinati per produrre questo evento di riepilogo singolo.</span><span class="sxs-lookup"><span data-stu-id="2a794-117">Number of events combined to produce this single summary event.</span></span>

</dd> <dt>

<span data-ttu-id="2a794-118">**Representative**</span><span class="sxs-lookup"><span data-stu-id="2a794-118">**Representative**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a794-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="2a794-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="2a794-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a794-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a794-121">Copia di uno degli eventi recapitati all'interno dell'intervallo di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="2a794-121">Copy of one of the events delivered within the aggregation interval.</span></span> <span data-ttu-id="2a794-122">Ad esempio, se un consumer ha effettuato la registrazione per gli eventi di modifica della chiave del registro di sistema dal provider di eventi del registro di sistema, il **rappresentante** manterrà un'istanza della classe **RegistryKeyChangeEvent** .</span><span class="sxs-lookup"><span data-stu-id="2a794-122">For example, if a consumer has registered for registry key change events from the Registry Event provider, **Representative** would hold an instance of the **RegistryKeyChangeEvent** class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a794-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a794-123">Remarks</span></span>

<span data-ttu-id="2a794-124">La classe **\_ \_ AggregateEvent** deriva da [**\_ \_ IndicationRelated**](--indicationrelated.md), che non dispone di proprietà.</span><span class="sxs-lookup"><span data-stu-id="2a794-124">The **\_\_AggregateEvent** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

<span data-ttu-id="2a794-125">I provider di eventi non generano mai eventi aggregati.</span><span class="sxs-lookup"><span data-stu-id="2a794-125">Event providers never generate aggregate events.</span></span> <span data-ttu-id="2a794-126">Devono ignorare la clausola GROUP with nell'elaborazione delle query di eventi.</span><span class="sxs-lookup"><span data-stu-id="2a794-126">They must ignore the GROUP WITHIN clause in their processing of event queries.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a794-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a794-127">Requirements</span></span>



| <span data-ttu-id="2a794-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a794-128">Requirement</span></span> | <span data-ttu-id="2a794-129">Valore</span><span class="sxs-lookup"><span data-stu-id="2a794-129">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="2a794-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a794-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2a794-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a794-131">Windows Vista</span></span><br/>       |
| <span data-ttu-id="2a794-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a794-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2a794-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a794-133">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="2a794-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2a794-134">Namespace</span></span><br/>                | <span data-ttu-id="2a794-135">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="2a794-135">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="2a794-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a794-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a794-137">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="2a794-137">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="2a794-138">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="2a794-138">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="2a794-139">Esecuzione di query con WQL</span><span class="sxs-lookup"><span data-stu-id="2a794-139">Querying with WQL</span></span>](querying-with-wql.md)
</dt> </dl>

 


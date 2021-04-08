---
description: È una classe di base astratta utilizzata nella registrazione di un consumer di eventi permanenti.
ms.assetid: c1dc9a91-76f9-4527-ad69-0323a9aef28a
ms.tgt_platform: multiple
title: Classe __EventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumer
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b8478b76aebf293d562129d047330f33e52706b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968648"
---
# <a name="__eventconsumer-class"></a><span data-ttu-id="a5c01-103">\_\_Classe EventConsumer</span><span class="sxs-lookup"><span data-stu-id="a5c01-103">\_\_EventConsumer class</span></span>

<span data-ttu-id="a5c01-104">La classe di sistema **\_ \_ EventConsumer** è una classe di base astratta utilizzata nella registrazione di un consumer di eventi permanenti.</span><span class="sxs-lookup"><span data-stu-id="a5c01-104">The **\_\_EventConsumer** system class is an abstract base class that is used in the registration of a permanent event consumer.</span></span> <span data-ttu-id="a5c01-105">È possibile derivare una nuova classe di consumer di eventi da **\_ \_ EventConsumer**.</span><span class="sxs-lookup"><span data-stu-id="a5c01-105">You can derive a new event consumer class from **\_\_EventConsumer**.</span></span>

<span data-ttu-id="a5c01-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a5c01-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a5c01-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a5c01-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5c01-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5c01-108">Syntax</span></span>

``` syntax
[abstract]
class __EventConsumer : __IndicationRelated
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
};
```

## <a name="members"></a><span data-ttu-id="a5c01-109">Members</span><span class="sxs-lookup"><span data-stu-id="a5c01-109">Members</span></span>

<span data-ttu-id="a5c01-110">La classe **\_ \_ EventConsumer** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a5c01-110">The **\_\_EventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="a5c01-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a5c01-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5c01-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a5c01-112">Properties</span></span>

<span data-ttu-id="a5c01-113">La classe **\_ \_ EventConsumer** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a5c01-113">The **\_\_EventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5c01-114">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="a5c01-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5c01-115">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a5c01-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="a5c01-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5c01-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5c01-117">ID di sicurezza (SID) che identifica in modo univoco l'utente che crea un filtro.</span><span class="sxs-lookup"><span data-stu-id="a5c01-117">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="a5c01-118">WMI archivia il SID dell'utente che crea un'istanza di **\_ \_ EventConsumer** o il SID Administrator, a seconda del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a5c01-118">WMI stores the SID of the user who creates an instance of **\_\_EventConsumer** or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="a5c01-119">Per ulteriori informazioni, vedere [associazione di un filtro eventi a un consumer logico](binding-an-event-filter-with-a-logical-consumer.md) e [monitoraggio e risposta agli eventi con](monitoring-and-responding-to-events-with-standard-consumers.md)consumer standard.</span><span class="sxs-lookup"><span data-stu-id="a5c01-119">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5c01-120">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="a5c01-120">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5c01-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a5c01-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5c01-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5c01-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5c01-123">Nome del computer a cui Strumentazione gestione Windows (WMI) Invia gli eventi.</span><span class="sxs-lookup"><span data-stu-id="a5c01-123">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

</dd> <dt>

<span data-ttu-id="a5c01-124">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="a5c01-124">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5c01-125">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a5c01-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5c01-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a5c01-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5c01-127">Numero massimo di code per un consumer specifico, in byte.</span><span class="sxs-lookup"><span data-stu-id="a5c01-127">Maximum queue for a specific consumer, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5c01-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5c01-128">Remarks</span></span>

<span data-ttu-id="a5c01-129">La classe **\_ \_ EventConsumer** deriva da [**\_ \_ IndicationRelated**](--indicationrelated.md), che non dispone di proprietà.</span><span class="sxs-lookup"><span data-stu-id="a5c01-129">The **\_\_EventConsumer** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which does not have properties.</span></span>

<span data-ttu-id="a5c01-130">I consumer permanenti definiscono nuove classi consumer per descrivere un'azione da eseguire e i dati da elaborare quando i consumer ricevono notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="a5c01-130">Permanent consumers define new consumer classes to describe an action to take and data to be processed when consumers receive event notifications.</span></span> <span data-ttu-id="a5c01-131">I consumer permanenti hanno particolari problemi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a5c01-131">Permanent consumers have special security concerns.</span></span> <span data-ttu-id="a5c01-132">Per ulteriori informazioni, vedere [protezione degli eventi WMI](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="a5c01-132">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5c01-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5c01-133">Requirements</span></span>



| <span data-ttu-id="a5c01-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5c01-134">Requirement</span></span> | <span data-ttu-id="a5c01-135">Valore</span><span class="sxs-lookup"><span data-stu-id="a5c01-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a5c01-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5c01-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a5c01-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5c01-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a5c01-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5c01-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a5c01-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5c01-139">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="a5c01-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a5c01-140">Namespace</span></span><br/>                | <span data-ttu-id="a5c01-141">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="a5c01-141">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="a5c01-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5c01-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5c01-143">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="a5c01-143">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="a5c01-144">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="a5c01-144">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="a5c01-145">Ricezione di eventi in qualsiasi momento</span><span class="sxs-lookup"><span data-stu-id="a5c01-145">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="a5c01-146">Creazione di una nuova classe di consumer di eventi permanenti</span><span class="sxs-lookup"><span data-stu-id="a5c01-146">Creating a New Permanent Event Consumer Class</span></span>](creating-a-new-permanent-event-consumer-class.md)
</dt> <dt>

[<span data-ttu-id="a5c01-147">Creazione di un consumer logico</span><span class="sxs-lookup"><span data-stu-id="a5c01-147">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="a5c01-148">Protezione degli eventi WMI</span><span class="sxs-lookup"><span data-stu-id="a5c01-148">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 


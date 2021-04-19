---
description: Segnala quando un evento viene eliminato in seguito all'overflow della coda di recapito.
ms.assetid: 7cb1ef3b-3b0a-4f72-96de-862022fd6db8
ms.tgt_platform: multiple
title: Classe __EventQueueOverflowEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventQueueOverflowEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 058b03b8a3311aad805f47a04d20e9f1fa8c2477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317600"
---
# <a name="__eventqueueoverflowevent-class"></a><span data-ttu-id="f05e8-103">\_\_Classe EventQueueOverflowEvent</span><span class="sxs-lookup"><span data-stu-id="f05e8-103">\_\_EventQueueOverflowEvent class</span></span>

<span data-ttu-id="f05e8-104">La classe di sistema **\_ \_ EventQueueOverflowEvent** segnala quando viene eliminato un evento in seguito all'overflow della coda di recapito.</span><span class="sxs-lookup"><span data-stu-id="f05e8-104">The **\_\_EventQueueOverflowEvent** system class reports when an event is dropped as a result of delivery queue overflow.</span></span>

<span data-ttu-id="f05e8-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f05e8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f05e8-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f05e8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f05e8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f05e8-107">Syntax</span></span>

``` syntax
class __EventQueueOverflowEvent : __EventDroppedEvent
{
  uint32              CurrentQueueSize;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="f05e8-108">Members</span><span class="sxs-lookup"><span data-stu-id="f05e8-108">Members</span></span>

<span data-ttu-id="f05e8-109">La classe **\_ \_ EventQueueOverflowEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f05e8-109">The **\_\_EventQueueOverflowEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="f05e8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f05e8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f05e8-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f05e8-111">Properties</span></span>

<span data-ttu-id="f05e8-112">La classe **\_ \_ EventQueueOverflowEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f05e8-112">The **\_\_EventQueueOverflowEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f05e8-113">**CurrentQueueSize**</span><span class="sxs-lookup"><span data-stu-id="f05e8-113">**CurrentQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f05e8-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f05e8-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f05e8-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f05e8-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f05e8-116">Dimensioni correnti della coda, in byte.</span><span class="sxs-lookup"><span data-stu-id="f05e8-116">Current queue size, in bytes.</span></span> <span data-ttu-id="f05e8-117">Per impostazione predefinita, questa proprietà è 10 MB per tutte le code combinate.</span><span class="sxs-lookup"><span data-stu-id="f05e8-117">This property defaults to 10 MB for all queues combined.</span></span>

</dd> <dt>

<span data-ttu-id="f05e8-118">**Event**</span><span class="sxs-lookup"><span data-stu-id="f05e8-118">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f05e8-119">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="f05e8-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f05e8-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f05e8-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f05e8-121">Evento di interesse.</span><span class="sxs-lookup"><span data-stu-id="f05e8-121">Event of interest.</span></span> <span data-ttu-id="f05e8-122">Questa proprietà viene ereditata da [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="f05e8-122">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f05e8-123">**IntendedConsumer**</span><span class="sxs-lookup"><span data-stu-id="f05e8-123">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f05e8-124">Tipo di dati: **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="f05e8-124">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="f05e8-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f05e8-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f05e8-126">Riferimento al consumer previsto.</span><span class="sxs-lookup"><span data-stu-id="f05e8-126">Reference to the intended consumer.</span></span> <span data-ttu-id="f05e8-127">Questa proprietà viene ereditata da [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="f05e8-127">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f05e8-128">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="f05e8-128">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f05e8-129">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f05e8-129">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f05e8-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f05e8-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f05e8-131">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="f05e8-131">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="f05e8-132">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="f05e8-132">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="f05e8-133">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="f05e8-133">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f05e8-134">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f05e8-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f05e8-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f05e8-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f05e8-136">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="f05e8-136">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="f05e8-137">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="f05e8-137">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="f05e8-138">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="f05e8-138">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="f05e8-139">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="f05e8-139">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="f05e8-140">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f05e8-140">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f05e8-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="f05e8-141">Remarks</span></span>

<span data-ttu-id="f05e8-142">Solo gli utenti con privilegi di amministratore possono ricevere questo evento.</span><span class="sxs-lookup"><span data-stu-id="f05e8-142">Only users with administrator privileges are able to receive this event.</span></span> <span data-ttu-id="f05e8-143">La classe **\_ \_ EventQueueOverflowEvent** deriva da [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="f05e8-143">The **\_\_EventQueueOverflowEvent** class is derived from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

<span data-ttu-id="f05e8-144">Per ulteriori informazioni, vedere la proprietà [**MaximumQueueSize**](--eventconsumer.md) nella classe [**\_ \_ EventConsumer**](--eventconsumer.md) e la proprietà [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) nella classe **\_ WMISetting di Win32** .</span><span class="sxs-lookup"><span data-stu-id="f05e8-144">For more information, see the [**MaximumQueueSize**](--eventconsumer.md) property in the [**\_\_EventConsumer**](--eventconsumer.md) class and the [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) property in the **Win32\_WMISetting** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="f05e8-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f05e8-145">Requirements</span></span>



| <span data-ttu-id="f05e8-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="f05e8-146">Requirement</span></span> | <span data-ttu-id="f05e8-147">Valore</span><span class="sxs-lookup"><span data-stu-id="f05e8-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f05e8-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f05e8-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f05e8-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f05e8-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f05e8-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f05e8-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f05e8-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f05e8-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="f05e8-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f05e8-152">Namespace</span></span><br/>                | <span data-ttu-id="f05e8-153">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="f05e8-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="f05e8-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f05e8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f05e8-155">**\_\_EventDroppedEvent**</span><span class="sxs-lookup"><span data-stu-id="f05e8-155">**\_\_EventDroppedEvent**</span></span>](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[<span data-ttu-id="f05e8-156">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="f05e8-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 


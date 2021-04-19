---
description: Rappresenta l'occorrenza di un evento che viene eliminato. Un evento eliminato è un evento che non viene recapitato a un consumer di eventi.
ms.assetid: fae267a9-e0ec-43fa-a3c3-d50345775a1d
ms.tgt_platform: multiple
title: Classe __EventDroppedEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventDroppedEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 4e9f68328a3c5c455c98e85a65d53156da6eeada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316001"
---
# <a name="__eventdroppedevent-class"></a><span data-ttu-id="ce0c6-104">\_\_Classe EventDroppedEvent</span><span class="sxs-lookup"><span data-stu-id="ce0c6-104">\_\_EventDroppedEvent class</span></span>

<span data-ttu-id="ce0c6-105">La classe di sistema **\_ \_ EventDroppedEvent** rappresenta l'occorrenza di un evento che viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="ce0c6-105">The **\_\_EventDroppedEvent** system class represents the occurrence of an event that is dropped.</span></span> <span data-ttu-id="ce0c6-106">Un evento eliminato è un evento che non viene recapitato a un consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="ce0c6-106">A dropped event is an event that is not delivered to an event consumer.</span></span>

<span data-ttu-id="ce0c6-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ce0c6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ce0c6-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ce0c6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce0c6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce0c6-109">Syntax</span></span>

``` syntax
class __EventDroppedEvent : __SystemEvent
{
  __Event             Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="ce0c6-110">Members</span><span class="sxs-lookup"><span data-stu-id="ce0c6-110">Members</span></span>

<span data-ttu-id="ce0c6-111">La classe **\_ \_ EventDroppedEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ce0c6-111">The **\_\_EventDroppedEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="ce0c6-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ce0c6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ce0c6-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ce0c6-113">Properties</span></span>

<span data-ttu-id="ce0c6-114">La classe **\_ \_ EventDroppedEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ce0c6-114">The **\_\_EventDroppedEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ce0c6-115">**Event**</span><span class="sxs-lookup"><span data-stu-id="ce0c6-115">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce0c6-116">Tipo di dati: **\_ \_ evento**</span><span class="sxs-lookup"><span data-stu-id="ce0c6-116">Data type: **\_\_Event**</span></span>
</dt> <dt>

<span data-ttu-id="ce0c6-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ce0c6-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce0c6-118">Evento che viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="ce0c6-118">Event that is dropped.</span></span>

</dd> <dt>

<span data-ttu-id="ce0c6-119">**IntendedConsumer**</span><span class="sxs-lookup"><span data-stu-id="ce0c6-119">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce0c6-120">Tipo di dati: **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="ce0c6-120">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="ce0c6-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ce0c6-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce0c6-122">Riferimento a un'istanza di [**\_ \_ EventConsumer**](--eventconsumer.md) che rappresenta l'utente permanente identificato per la ricezione di un evento.</span><span class="sxs-lookup"><span data-stu-id="ce0c6-122">Reference to an instance of [**\_\_EventConsumer**](--eventconsumer.md) that represents the permanent consumer you identify to receive an event.</span></span> <span data-ttu-id="ce0c6-123">Diversi consumer permanenti che sottoscrivono un evento possono continuare a ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="ce0c6-123">Different permanent consumers that subscribe to an event can continue to receive the event.</span></span>

</dd> <dt>

<span data-ttu-id="ce0c6-124">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="ce0c6-124">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce0c6-125">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ce0c6-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ce0c6-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ce0c6-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce0c6-127">Descrittore utilizzato da un provider di eventi per determinare gli utenti che possono ricevere un evento.</span><span class="sxs-lookup"><span data-stu-id="ce0c6-127">Descriptor that an event provider uses to determine the users who can receive an event.</span></span> <span data-ttu-id="ce0c6-128">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="ce0c6-128">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce0c6-129">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="ce0c6-129">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce0c6-130">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ce0c6-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ce0c6-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ce0c6-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce0c6-132">Valore univoco che indica l'ora in cui viene generato un evento.</span><span class="sxs-lookup"><span data-stu-id="ce0c6-132">Unique value that indicates the time when an event is generated.</span></span> <span data-ttu-id="ce0c6-133">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="ce0c6-133">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="ce0c6-134">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="ce0c6-134">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="ce0c6-135">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="ce0c6-135">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="ce0c6-136">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ce0c6-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce0c6-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce0c6-137">Remarks</span></span>

<span data-ttu-id="ce0c6-138">La classe **\_ \_ EventDroppedEvent** deriva da [**\_ \_ SystemEvent**](--systemevent.md).</span><span class="sxs-lookup"><span data-stu-id="ce0c6-138">The **\_\_EventDroppedEvent** class is derived from [**\_\_SystemEvent**](--systemevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce0c6-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce0c6-139">Requirements</span></span>



| <span data-ttu-id="ce0c6-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce0c6-140">Requirement</span></span> | <span data-ttu-id="ce0c6-141">Valore</span><span class="sxs-lookup"><span data-stu-id="ce0c6-141">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ce0c6-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce0c6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ce0c6-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce0c6-143">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ce0c6-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce0c6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ce0c6-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce0c6-145">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="ce0c6-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ce0c6-146">Namespace</span></span><br/>                | <span data-ttu-id="ce0c6-147">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="ce0c6-147">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="ce0c6-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce0c6-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce0c6-149">**\_\_SystemEvent**</span><span class="sxs-lookup"><span data-stu-id="ce0c6-149">**\_\_SystemEvent**</span></span>](/windows/desktop/WmiSdk/--systemevent)
</dt> <dt>

[<span data-ttu-id="ce0c6-150">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="ce0c6-150">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 


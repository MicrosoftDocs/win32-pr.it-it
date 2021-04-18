---
description: Rappresenta l'occorrenza di un altro evento che viene eliminato a causa dell'errore di un consumer di eventi.
ms.assetid: bb6a1ce9-72a2-4528-8bc8-71ac053b6b1d
ms.tgt_platform: multiple
title: Classe __ConsumerFailureEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ConsumerFailureEvent
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 571785245c05d18678c10a65b192a25022fff8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319326"
---
# <a name="__consumerfailureevent-class"></a><span data-ttu-id="1d841-103">\_\_Classe ConsumerFailureEvent</span><span class="sxs-lookup"><span data-stu-id="1d841-103">\_\_ConsumerFailureEvent class</span></span>

<span data-ttu-id="1d841-104">La classe di sistema **\_ \_ ConsumerFailureEvent** rappresenta l'occorrenza di un altro evento che viene eliminato a causa dell'errore di un consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="1d841-104">The **\_\_ConsumerFailureEvent** system class represents the occurrence of some other event that is being dropped because of the failure of an event consumer.</span></span>

<span data-ttu-id="1d841-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1d841-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1d841-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="1d841-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d841-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d841-107">Syntax</span></span>

``` syntax
class __ConsumerFailureEvent : __EventDroppedEvent
{
  uint32              ErrorCode;
  string              ErrorDescription;
  object              ErrorObject;
  object              Event;
  __EventConsumer REF IntendedConsumer;
  uint8               SECURITY_DESCRIPTOR[];
  uint64              TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="1d841-108">Members</span><span class="sxs-lookup"><span data-stu-id="1d841-108">Members</span></span>

<span data-ttu-id="1d841-109">La classe **\_ \_ ConsumerFailureEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1d841-109">The **\_\_ConsumerFailureEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="1d841-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1d841-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d841-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1d841-111">Properties</span></span>

<span data-ttu-id="1d841-112">La classe **\_ \_ ConsumerFailureEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1d841-112">The **\_\_ConsumerFailureEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d841-113">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1d841-113">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d841-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d841-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d841-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d841-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d841-116">Codice di errore restituito dal consumer.</span><span class="sxs-lookup"><span data-stu-id="1d841-116">Error code returned by the consumer.</span></span>

</dd> <dt>

<span data-ttu-id="1d841-117">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1d841-117">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d841-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d841-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d841-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d841-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d841-120">Descrizione del codice di errore esteso, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="1d841-120">Extended error code description, if available.</span></span>

</dd> <dt>

<span data-ttu-id="1d841-121">**ErrorObject**</span><span class="sxs-lookup"><span data-stu-id="1d841-121">**ErrorObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d841-122">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="1d841-122">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="1d841-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d841-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d841-124">Oggetto in errore.</span><span class="sxs-lookup"><span data-stu-id="1d841-124">Object in error.</span></span>

</dd> <dt>

<span data-ttu-id="1d841-125">**Event**</span><span class="sxs-lookup"><span data-stu-id="1d841-125">**Event**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d841-126">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="1d841-126">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="1d841-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d841-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d841-128">Evento in errore.</span><span class="sxs-lookup"><span data-stu-id="1d841-128">Event in error.</span></span> <span data-ttu-id="1d841-129">Questa proprietà viene ereditata da [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="1d841-129">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d841-130">**IntendedConsumer**</span><span class="sxs-lookup"><span data-stu-id="1d841-130">**IntendedConsumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d841-131">Tipo di dati: **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="1d841-131">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="1d841-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d841-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d841-133">Riferimento al consumer previsto.</span><span class="sxs-lookup"><span data-stu-id="1d841-133">Reference to the intended consumer.</span></span> <span data-ttu-id="1d841-134">Questa proprietà viene ereditata da [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="1d841-134">This property is inherited from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d841-135">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="1d841-135">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d841-136">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1d841-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1d841-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d841-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d841-138">Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento.</span><span class="sxs-lookup"><span data-stu-id="1d841-138">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="1d841-139">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="1d841-139">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d841-140">**ORA di \_ creazione**</span><span class="sxs-lookup"><span data-stu-id="1d841-140">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d841-141">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1d841-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1d841-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d841-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d841-143">Valore univoco che indica l'ora in cui è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="1d841-143">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="1d841-144">Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="1d841-144">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="1d841-145">Le informazioni sono nel formato UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="1d841-145">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="1d841-146">Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="1d841-146">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="1d841-147">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1d841-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d841-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d841-148">Remarks</span></span>

<span data-ttu-id="1d841-149">La classe **\_ \_ ConsumerFailureEvent** deriva da [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).</span><span class="sxs-lookup"><span data-stu-id="1d841-149">The **\_\_ConsumerFailureEvent** class is derived from [**\_\_EventDroppedEvent**](--eventdroppedevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d841-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d841-150">Requirements</span></span>



| <span data-ttu-id="1d841-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d841-151">Requirement</span></span> | <span data-ttu-id="1d841-152">Valore</span><span class="sxs-lookup"><span data-stu-id="1d841-152">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1d841-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d841-153">Minimum supported client</span></span><br/> | <span data-ttu-id="1d841-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d841-154">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1d841-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d841-155">Minimum supported server</span></span><br/> | <span data-ttu-id="1d841-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d841-156">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="1d841-157">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1d841-157">Namespace</span></span><br/>                | <span data-ttu-id="1d841-158">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="1d841-158">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="1d841-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d841-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d841-160">**\_\_EventDroppedEvent**</span><span class="sxs-lookup"><span data-stu-id="1d841-160">**\_\_EventDroppedEvent**</span></span>](/windows/desktop/WmiSdk/--eventdroppedevent)
</dt> <dt>

[<span data-ttu-id="1d841-161">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="1d841-161">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 


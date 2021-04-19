---
description: Genera eventi a intervalli, in modo analogo a un \_ messaggio del timer WM nella programmazione Windows.
ms.assetid: 0895a743-a0dd-4833-a2bf-0196369e18b9
ms.tgt_platform: multiple
title: Classe __IntervalTimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __IntervalTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 20dd1c9fb2d009de4d8d957b4d5980cc6d6ff45e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317593"
---
# <a name="__intervaltimerinstruction-class"></a><span data-ttu-id="8c0ea-103">\_\_Classe IntervalTimerInstruction</span><span class="sxs-lookup"><span data-stu-id="8c0ea-103">\_\_IntervalTimerInstruction class</span></span>

<span data-ttu-id="8c0ea-104">La classe di sistema **\_ \_ IntervalTimerInstruction** genera eventi a intervalli, in modo analogo a un \_ messaggio del timer WM nella programmazione Windows.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-104">The **\_\_IntervalTimerInstruction** system class generates events at intervals, similar to a WM\_TIMER message in Windows programming.</span></span> <span data-ttu-id="8c0ea-105">Un consumer di eventi registra per ricevere eventi timer intervallo creando una query di eventi che fa riferimento a questa classe.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-105">An event consumer registers to receive interval timer events by creating an event query that references this class.</span></span> <span data-ttu-id="8c0ea-106">A causa del comportamento del sistema operativo, non vi sono garanzie che gli eventi vengano recapitati esattamente all'intervallo richiesto.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-106">Due to operating system behavior, there are no guarantees that events will be delivered at precisely the requested interval.</span></span>

<span data-ttu-id="8c0ea-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8c0ea-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c0ea-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c0ea-109">Syntax</span></span>

``` syntax
class __IntervalTimerInstruction : __TimerInstruction
{
  uint32  IntervalBetweenEvents;
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a><span data-ttu-id="8c0ea-110">Members</span><span class="sxs-lookup"><span data-stu-id="8c0ea-110">Members</span></span>

<span data-ttu-id="8c0ea-111">La classe **\_ \_ IntervalTimerInstruction** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8c0ea-111">The **\_\_IntervalTimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="8c0ea-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8c0ea-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c0ea-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8c0ea-113">Properties</span></span>

<span data-ttu-id="8c0ea-114">La classe **\_ \_ IntervalTimerInstruction** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-114">The **\_\_IntervalTimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c0ea-115">**IntervalBetweenEvents**</span><span class="sxs-lookup"><span data-stu-id="8c0ea-115">**IntervalBetweenEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c0ea-116">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8c0ea-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8c0ea-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c0ea-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c0ea-118">Qualificatori: [**unità**](standard-qualifiers.md) (millisecondi)</span><span class="sxs-lookup"><span data-stu-id="8c0ea-118">Qualifiers: [**Units**](standard-qualifiers.md) (milliseconds)</span></span>
</dt> </dl>

<span data-ttu-id="8c0ea-119">Numero di millisecondi tra la generazione di eventi.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-119">Number of milliseconds between event firings.</span></span>

</dd> <dt>

<span data-ttu-id="8c0ea-120">**SkipIfPassed**</span><span class="sxs-lookup"><span data-stu-id="8c0ea-120">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c0ea-121">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8c0ea-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8c0ea-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c0ea-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c0ea-123">Se **true**, l'evento deve essere ignorato se l'intervallo è già stato superato.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-123">If **TRUE**, this event is to be skipped if the interval is already passed.</span></span> <span data-ttu-id="8c0ea-124">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-124">The default is **FALSE**.</span></span> <span data-ttu-id="8c0ea-125">Questa proprietà viene ereditata da [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="8c0ea-125">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<dt>

<span data-ttu-id="8c0ea-126">FALSE</span><span class="sxs-lookup"><span data-stu-id="8c0ea-126">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="8c0ea-127">Quando WMI o il consumer diventano nuovamente disponibili, viene generato e ricevuto un evento di notifica.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-127">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="8c0ea-128">true</span><span class="sxs-lookup"><span data-stu-id="8c0ea-128">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="8c0ea-129">L'evento timer non si verifica se WMI non è disponibile per generarlo all'intervallo di tempo appropriato oppure se il consumer che richiede la ricezione dell'evento non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-129">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8c0ea-130">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="8c0ea-130">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c0ea-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8c0ea-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c0ea-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c0ea-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c0ea-133">Qualificatori: [ **chiave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8c0ea-133">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8c0ea-134">Identificatore univoco per questo oggetto **\_ \_ IntervalTimerInstruction** .</span><span class="sxs-lookup"><span data-stu-id="8c0ea-134">Unique identifier for this **\_\_IntervalTimerInstruction** object.</span></span> <span data-ttu-id="8c0ea-135">Questa proprietà viene ereditata da [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="8c0ea-135">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c0ea-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c0ea-136">Remarks</span></span>

<span data-ttu-id="8c0ea-137">La classe **\_ \_ IntervalTimerInstruction** deriva da [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="8c0ea-137">The **\_\_IntervalTimerInstruction** class is derived from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<span data-ttu-id="8c0ea-138">La query di eventi immessa per la registrazione per un evento timer intervallo è in genere basata sulla proprietà **timerId** .</span><span class="sxs-lookup"><span data-stu-id="8c0ea-138">The event query entered to register for an interval timer event is usually based on the **TimerId** property.</span></span> <span data-ttu-id="8c0ea-139">Gli eventi di notifica generati da un evento timer intervallo contengono la proprietà **NumFirings** che contiene i dati che riflettono il numero di eventi generati durante il periodo in cui non è stato possibile ricevere gli eventi.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-139">Notification events generated from an interval timer event contain the property **NumFirings** which contains data reflecting how many events fired during the time the events were unable to be received.</span></span> <span data-ttu-id="8c0ea-140">Se **SkipIfPassed** è impostato su **true**, tali informazioni vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-140">If **SkipIfPassed** is set to **TRUE**, that information is discarded.</span></span>

<span data-ttu-id="8c0ea-141">Il valore della proprietà **IntervalBetweenEvents** deve essere ragionevolmente grande.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-141">The value for the **IntervalBetweenEvents** property should be reasonably large.</span></span> <span data-ttu-id="8c0ea-142">Se è troppo piccolo, WMI potrebbe ignorarlo e non generare l'evento a causa di limitazioni in alcuni sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-142">If it is too small, WMI may ignore it and not generate the event due to limitations in some operating systems.</span></span>

<span data-ttu-id="8c0ea-143">WMI genera l'evento timer interval creando un'istanza della classe [**\_ \_ TimerEvent**](--timerevent.md) .</span><span class="sxs-lookup"><span data-stu-id="8c0ea-143">WMI generates the interval timer event by creating an instance of the [**\_\_TimerEvent**](--timerevent.md) class.</span></span>

<span data-ttu-id="8c0ea-144">Per ricevere questi eventi del timer in un consumer di eventi temporaneo, eseguire [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) con la stringa di query di evento seguente:</span><span class="sxs-lookup"><span data-stu-id="8c0ea-144">To receive these timer events in a temporary event consumer, execute [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) with the following event query string:</span></span>


```sql
SELECT * FROM __TimerEvent WHERE TimerID = "MyEvent"
```



<span data-ttu-id="8c0ea-145">Per ricevere questi eventi timer in un consumer di eventi permanenti, è necessario caricare la query precedente in un filtro eventi, definire un consumer logico e creare un'associazione da filtro a consumer per il filtro e il consumer.</span><span class="sxs-lookup"><span data-stu-id="8c0ea-145">To receive these timer events in a permanent event consumer, you must load the previous query into an event filter, define a logical consumer, and create a filter-to-consumer binding for the filter and consumer.</span></span> <span data-ttu-id="8c0ea-146">Per ulteriori informazioni, vedere [ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md).</span><span class="sxs-lookup"><span data-stu-id="8c0ea-146">For more information, see [Receiving Events at All Times](receiving-events-at-all-times.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8c0ea-147">Esempio</span><span class="sxs-lookup"><span data-stu-id="8c0ea-147">Examples</span></span>

<span data-ttu-id="8c0ea-148">Nella dichiarazione MOF seguente viene illustrato come generare un evento timer intervallo con la proprietà chiave impostata su "" ".</span><span class="sxs-lookup"><span data-stu-id="8c0ea-148">The following MOF declaration shows how to generate an interval timer event with the key property set to "MyEvent" every 10 seconds:</span></span>


```mof
instance of __IntervalTimerInstruction
{
  TimerId = "MyEvent";     // inherited from __TimerInstruction
  SkipIfPassed = FALSE;    // also inherited
  IntervalBetweenEvents = 10000;
};
```



## <a name="requirements"></a><span data-ttu-id="8c0ea-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c0ea-149">Requirements</span></span>



| <span data-ttu-id="8c0ea-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c0ea-150">Requirement</span></span> | <span data-ttu-id="8c0ea-151">Valore</span><span class="sxs-lookup"><span data-stu-id="8c0ea-151">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8c0ea-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c0ea-152">Minimum supported client</span></span><br/> | <span data-ttu-id="8c0ea-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c0ea-153">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8c0ea-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c0ea-154">Minimum supported server</span></span><br/> | <span data-ttu-id="8c0ea-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c0ea-155">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="8c0ea-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8c0ea-156">Namespace</span></span><br/>                | <span data-ttu-id="8c0ea-157">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="8c0ea-157">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="8c0ea-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c0ea-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c0ea-159">**\_\_TimerInstruction**</span><span class="sxs-lookup"><span data-stu-id="8c0ea-159">**\_\_TimerInstruction**</span></span>](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[<span data-ttu-id="8c0ea-160">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="8c0ea-160">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="8c0ea-161">Ricezione di eventi temporizzati o ripetuti</span><span class="sxs-lookup"><span data-stu-id="8c0ea-161">Receiving Timed or Repeating Events</span></span>](receiving-a-timed-or-repeating-event.md)
</dt> </dl>

 


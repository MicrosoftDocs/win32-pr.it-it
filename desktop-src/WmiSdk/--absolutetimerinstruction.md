---
description: Causa la generazione di un evento in una data specifica in un momento specifico.
ms.assetid: bcb64c81-3b40-4665-a880-a100629656e0
ms.tgt_platform: multiple
title: Classe __AbsoluteTimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AbsoluteTimerInstruction
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5f4f55e635e42ec34e9b3558a0784d319e4d91ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319808"
---
# <a name="__absolutetimerinstruction-class"></a><span data-ttu-id="31e0d-103">\_\_Classe AbsoluteTimerInstruction</span><span class="sxs-lookup"><span data-stu-id="31e0d-103">\_\_AbsoluteTimerInstruction class</span></span>

<span data-ttu-id="31e0d-104">La classe di sistema **\_ \_ AbsoluteTimerInstruction** causa la generazione di un evento in una data specifica in un momento specifico.</span><span class="sxs-lookup"><span data-stu-id="31e0d-104">The **\_\_AbsoluteTimerInstruction** system class causes an event to be generated on a specific date at a specific time.</span></span> <span data-ttu-id="31e0d-105">Un consumer di eventi registra per ricevere un evento timer assoluto creando un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="31e0d-105">An event consumer registers to receive an absolute timer event by creating an instance of this class.</span></span> <span data-ttu-id="31e0d-106">L'evento viene generato una sola volta.</span><span class="sxs-lookup"><span data-stu-id="31e0d-106">The event is generated one time.</span></span>

<span data-ttu-id="31e0d-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="31e0d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="31e0d-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="31e0d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="31e0d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31e0d-109">Syntax</span></span>

``` syntax
class __AbsoluteTimerInstruction : __TimerInstruction
{
  datetime EventDateTime;
  boolean  SkipIfPassed = FALSE;
  string   TimerId;
};
```

## <a name="members"></a><span data-ttu-id="31e0d-110">Members</span><span class="sxs-lookup"><span data-stu-id="31e0d-110">Members</span></span>

<span data-ttu-id="31e0d-111">La classe **\_ \_ AbsoluteTimerInstruction** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="31e0d-111">The **\_\_AbsoluteTimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="31e0d-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="31e0d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31e0d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="31e0d-113">Properties</span></span>

<span data-ttu-id="31e0d-114">La classe **\_ \_ AbsoluteTimerInstruction** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="31e0d-114">The **\_\_AbsoluteTimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31e0d-115">**EventDateTime**</span><span class="sxs-lookup"><span data-stu-id="31e0d-115">**EventDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31e0d-116">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="31e0d-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="31e0d-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="31e0d-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="31e0d-118">Stringa a lunghezza fissa nel [formato DMTF](date-and-time-format.md) che specifica quando il timer viene attivato.</span><span class="sxs-lookup"><span data-stu-id="31e0d-118">Fixed-length string in [DMTF format](date-and-time-format.md) that specifies when the timer fires.</span></span>

</dd> <dt>

<span data-ttu-id="31e0d-119">**SkipIfPassed**</span><span class="sxs-lookup"><span data-stu-id="31e0d-119">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31e0d-120">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="31e0d-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31e0d-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31e0d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31e0d-122">Se **true**, l'evento timer si verifica se WMI non è in grado di generarlo all'intervallo di tempo corretto oppure se il consumer che richiede la ricezione dell'evento non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="31e0d-122">If **TRUE**, the timer event occurs if WMI cannot generate it at the correct time interval, or the consumer requesting to receive the event is unavailable.</span></span> <span data-ttu-id="31e0d-123">Se **true**, l'evento non si verificherà.</span><span class="sxs-lookup"><span data-stu-id="31e0d-123">If **TRUE**, the event will not occur.</span></span> <span data-ttu-id="31e0d-124">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="31e0d-124">The default is **FALSE**.</span></span> <span data-ttu-id="31e0d-125">Quando WMI o il consumer diventano disponibili, viene generato e ricevuto un evento di notifica.</span><span class="sxs-lookup"><span data-stu-id="31e0d-125">When WMI or the consumer becomes available, a notification event is generated and received.</span></span> <span data-ttu-id="31e0d-126">Questa proprietà viene ereditata da [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="31e0d-126">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<dt>

<span data-ttu-id="31e0d-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="31e0d-127">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="31e0d-128">Quando WMI o il consumer diventano nuovamente disponibili, viene generato e ricevuto un evento di notifica.</span><span class="sxs-lookup"><span data-stu-id="31e0d-128">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="31e0d-129">true</span><span class="sxs-lookup"><span data-stu-id="31e0d-129">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="31e0d-130">L'evento timer non si verifica se WMI non è disponibile per generarlo all'intervallo di tempo appropriato oppure se il consumer che richiede la ricezione dell'evento non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="31e0d-130">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="31e0d-131">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="31e0d-131">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31e0d-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="31e0d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31e0d-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31e0d-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31e0d-134">Qualificatori: [ **chiave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="31e0d-134">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="31e0d-135">Stringa univoca assegnata dall'utente che identifica un evento timer specifico.</span><span class="sxs-lookup"><span data-stu-id="31e0d-135">Unique user-assigned string that identifies a specific timer event.</span></span> <span data-ttu-id="31e0d-136">Per evitare conflitti di denominazione con altri identificatori del timer, è possibile utilizzare il formato stringa di un GUID di stile dell'ambiente del computer distribuito.</span><span class="sxs-lookup"><span data-stu-id="31e0d-136">To avoid naming conflicts with other timer identifiers, the string form of a distributed computer environment style GUID can be used.</span></span> <span data-ttu-id="31e0d-137">Questa proprietà viene ereditata da [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="31e0d-137">This property is inherited from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31e0d-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="31e0d-138">Remarks</span></span>

<span data-ttu-id="31e0d-139">La classe **\_ \_ AbsoluteTimerInstruction** deriva da [**\_ \_ TimerInstruction**](--timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="31e0d-139">The **\_\_AbsoluteTimerInstruction** class is derived from [**\_\_TimerInstruction**](--timerinstruction.md).</span></span>

<span data-ttu-id="31e0d-140">WMI genera l'evento del timer assoluto creando un'istanza della classe [**\_ \_ TimerEvent**](--timerevent.md) .</span><span class="sxs-lookup"><span data-stu-id="31e0d-140">WMI generates the absolute timer event by creating an instance of the [**\_\_TimerEvent**](--timerevent.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="31e0d-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31e0d-141">Requirements</span></span>



| <span data-ttu-id="31e0d-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="31e0d-142">Requirement</span></span> | <span data-ttu-id="31e0d-143">Valore</span><span class="sxs-lookup"><span data-stu-id="31e0d-143">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="31e0d-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31e0d-144">Minimum supported client</span></span><br/> | <span data-ttu-id="31e0d-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31e0d-145">Windows Vista</span></span><br/>       |
| <span data-ttu-id="31e0d-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31e0d-146">Minimum supported server</span></span><br/> | <span data-ttu-id="31e0d-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31e0d-147">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="31e0d-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="31e0d-148">Namespace</span></span><br/>                | <span data-ttu-id="31e0d-149">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="31e0d-149">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="31e0d-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31e0d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31e0d-151">**\_\_TimerInstruction**</span><span class="sxs-lookup"><span data-stu-id="31e0d-151">**\_\_TimerInstruction**</span></span>](/windows/desktop/WmiSdk/--timerinstruction)
</dt> <dt>

[<span data-ttu-id="31e0d-152">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="31e0d-152">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="31e0d-153">Ricezione di eventi temporizzati o ripetuti</span><span class="sxs-lookup"><span data-stu-id="31e0d-153">Receiving Timed or Repeating Events</span></span>](receiving-a-timed-or-repeating-event.md)
</dt> <dt>

[<span data-ttu-id="31e0d-154">Ricezione di eventi in qualsiasi momento</span><span class="sxs-lookup"><span data-stu-id="31e0d-154">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="31e0d-155">Ricezione di eventi per la durata dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="31e0d-155">Receiving Events for the Duration of Your Application</span></span>](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 


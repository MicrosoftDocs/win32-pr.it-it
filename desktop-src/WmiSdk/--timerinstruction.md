---
description: Specifica le istruzioni per la generazione di eventi timer per i consumer.
ms.assetid: b08edb25-bedf-4014-a835-4050f5749479
ms.tgt_platform: multiple
title: Classe __TimerInstruction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __TimerInstruction
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5c6bbbf905a141fb7e9e3621c78709fd78999393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350096"
---
# <a name="__timerinstruction-class"></a><span data-ttu-id="30696-103">\_\_Classe TimerInstruction</span><span class="sxs-lookup"><span data-stu-id="30696-103">\_\_TimerInstruction class</span></span>

<span data-ttu-id="30696-104">La classe di sistema astratta **\_ \_ TimerInstruction** specifica le istruzioni per la generazione di [eventi timer](receiving-a-timed-or-repeating-event.md) per i consumer.</span><span class="sxs-lookup"><span data-stu-id="30696-104">The **\_\_TimerInstruction** abstract system class specifies instructions on how [timer events](receiving-a-timed-or-repeating-event.md) should be generated for consumers.</span></span>

<span data-ttu-id="30696-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="30696-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="30696-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="30696-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="30696-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30696-107">Syntax</span></span>

``` syntax
[abstract]
class __TimerInstruction : __EventGenerator
{
  boolean SkipIfPassed = FALSE;
  string  TimerId;
};
```

## <a name="members"></a><span data-ttu-id="30696-108">Members</span><span class="sxs-lookup"><span data-stu-id="30696-108">Members</span></span>

<span data-ttu-id="30696-109">La classe **\_ \_ TimerInstruction** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="30696-109">The **\_\_TimerInstruction** class has these types of members:</span></span>

-   [<span data-ttu-id="30696-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="30696-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30696-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="30696-111">Properties</span></span>

<span data-ttu-id="30696-112">La classe **\_ \_ TimerInstruction** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="30696-112">The **\_\_TimerInstruction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30696-113">**SkipIfPassed**</span><span class="sxs-lookup"><span data-stu-id="30696-113">**SkipIfPassed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30696-114">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="30696-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="30696-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="30696-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30696-116">Descrive se verrà generato un evento di notifica e che riceverà quando un consumer diventerà disponibile.</span><span class="sxs-lookup"><span data-stu-id="30696-116">Describes whether a notification event will be generated and receive when a consumer becomes available.</span></span>

<dt>

<span data-ttu-id="30696-117">FALSE</span><span class="sxs-lookup"><span data-stu-id="30696-117">FALSE</span></span>
</dt> <dd>

<span data-ttu-id="30696-118">Quando WMI o il consumer diventano nuovamente disponibili, viene generato e ricevuto un evento di notifica.</span><span class="sxs-lookup"><span data-stu-id="30696-118">When WMI or the consumer becomes available again, a notification event will be generated and received.</span></span>

</dd> <dt>

<span data-ttu-id="30696-119">true</span><span class="sxs-lookup"><span data-stu-id="30696-119">TRUE</span></span>
</dt> <dd>

<span data-ttu-id="30696-120">L'evento timer non si verifica se WMI non è disponibile per generarlo all'intervallo di tempo appropriato oppure se il consumer che richiede la ricezione dell'evento non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="30696-120">The timer event does not occur if WMI is unavailable to generate it at the appropriate time interval, or the consumer requesting to receive the event is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="30696-121">**TimerId**</span><span class="sxs-lookup"><span data-stu-id="30696-121">**TimerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30696-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="30696-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30696-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="30696-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30696-124">Qualificatori: [ **chiave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="30696-124">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="30696-125">Stringa univoca assegnata dall'utente che identifica questo particolare evento del timer.</span><span class="sxs-lookup"><span data-stu-id="30696-125">Unique user-assigned string that identifies this particular timer event.</span></span> <span data-ttu-id="30696-126">Per evitare conflitti di denominazione con altri identificatori del timer, è possibile usare il formato stringa di un GUID di tipo DCE (Distributed computer Environment).</span><span class="sxs-lookup"><span data-stu-id="30696-126">To avoid naming conflicts with other timer identifiers, the string form of a distributed computer environment (DCE)-style GUID can be used.</span></span> <span data-ttu-id="30696-127">Questa proprietà fa parte dell'istanza di [**\_ \_ TimerEvent**](--timerevent.md) che rappresenta l'evento.</span><span class="sxs-lookup"><span data-stu-id="30696-127">This property is part of the [**\_\_TimerEvent**](--timerevent.md) instance that represents the event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30696-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="30696-128">Remarks</span></span>

<span data-ttu-id="30696-129">La classe **\_ \_ TimerInstruction** deriva da [**\_ \_ EventGenerator**](--eventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="30696-129">The **\_\_TimerInstruction** class is derived from [**\_\_EventGenerator**](--eventgenerator.md).</span></span>

<span data-ttu-id="30696-130">Le sottoclassi **\_ \_ TimerInstruction** sono [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md), utilizzate dai consumer per la registrazione per un evento timer assoluto e [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md), utilizzate per la registrazione per un evento timer intervallo.</span><span class="sxs-lookup"><span data-stu-id="30696-130">The **\_\_TimerInstruction** subclasses are [**\_\_AbsoluteTimerInstruction**](--absolutetimerinstruction.md), used by consumers to register for an absolute timer event, and [**\_\_IntervalTimerInstruction**](--intervaltimerinstruction.md), used to register for an interval timer event.</span></span>

## <a name="requirements"></a><span data-ttu-id="30696-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30696-131">Requirements</span></span>



| <span data-ttu-id="30696-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="30696-132">Requirement</span></span> | <span data-ttu-id="30696-133">Valore</span><span class="sxs-lookup"><span data-stu-id="30696-133">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="30696-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30696-134">Minimum supported client</span></span><br/> | <span data-ttu-id="30696-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30696-135">Windows Vista</span></span><br/>       |
| <span data-ttu-id="30696-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30696-136">Minimum supported server</span></span><br/> | <span data-ttu-id="30696-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30696-137">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="30696-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="30696-138">Namespace</span></span><br/>                | <span data-ttu-id="30696-139">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="30696-139">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="30696-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30696-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30696-141">**\_\_EventGenerator**</span><span class="sxs-lookup"><span data-stu-id="30696-141">**\_\_EventGenerator**</span></span>](/windows/desktop/WmiSdk/--eventgenerator)
</dt> <dt>

[<span data-ttu-id="30696-142">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="30696-142">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 


---
description: Questa classe è la classe del tipo di evento per gli eventi DPC (Device rinviated procedure call). La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 46010179-7f0a-47dd-95fd-04d30fc597ba
title: Classe DPC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DPC
- DPC.InitialTime
- DPC.Routine
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0e756c2b41499a6e5b82129d609befc41d5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878733"
---
# <a name="dpc-class"></a><span data-ttu-id="44931-104">Classe DPC</span><span class="sxs-lookup"><span data-stu-id="44931-104">DPC class</span></span>

<span data-ttu-id="44931-105">Questa classe è la classe del tipo di evento per gli eventi DPC (Device rinviated procedure call).</span><span class="sxs-lookup"><span data-stu-id="44931-105">This class is the event type class for device deferred procedure call (DPC) events.</span></span>

<span data-ttu-id="44931-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="44931-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="44931-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44931-107">Syntax</span></span>

``` syntax
[EventType{66, 68, 69}, EventTypeName{"ThreadDPC", "DPC", "TimerDPC"}]
class DPC : PerfInfo
{
  object InitialTime;
  uint32 Routine;
};
```

## <a name="members"></a><span data-ttu-id="44931-108">Members</span><span class="sxs-lookup"><span data-stu-id="44931-108">Members</span></span>

<span data-ttu-id="44931-109">La classe **DPC** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="44931-109">The **DPC** class has these types of members:</span></span>

-   [<span data-ttu-id="44931-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="44931-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44931-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="44931-111">Properties</span></span>

<span data-ttu-id="44931-112">La classe **DPC** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="44931-112">The **DPC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44931-113">**InitialTime**</span><span class="sxs-lookup"><span data-stu-id="44931-113">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44931-114">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="44931-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="44931-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="44931-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44931-116">Qualificatori: WmiDataId (1), Extension ("WmiTime")</span><span class="sxs-lookup"><span data-stu-id="44931-116">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="44931-117">Tempo di immissione DPC.</span><span class="sxs-lookup"><span data-stu-id="44931-117">DPC entry time.</span></span>

</dd> <dt>

<span data-ttu-id="44931-118">**Routine**</span><span class="sxs-lookup"><span data-stu-id="44931-118">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44931-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44931-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44931-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="44931-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44931-121">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="44931-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="44931-122">Indirizzo della routine DPC.</span><span class="sxs-lookup"><span data-stu-id="44931-122">Address of DPC routine.</span></span> <span data-ttu-id="44931-123">Usare l'indirizzo con gli eventi di immagine per individuare l'immagine avviata.</span><span class="sxs-lookup"><span data-stu-id="44931-123">Use the address with the Image events to find which image started.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44931-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="44931-124">Remarks</span></span>

<span data-ttu-id="44931-125">Questi eventi vengono registrati quando viene immesso un DPC.</span><span class="sxs-lookup"><span data-stu-id="44931-125">These events are logged when a DPC is entered.</span></span> <span data-ttu-id="44931-126">Questi eventi vengono utilizzati per monitorare e verificare il comportamento dei driver e dei componenti in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="44931-126">You use these events to monitor and verify the behavior of drivers and kernel-mode components.</span></span> <span data-ttu-id="44931-127">Ad esempio, è possibile usare gli eventi DPC, ISR ed image per determinare i componenti che impiegano troppo tempo a livelli di interrupt elevati.</span><span class="sxs-lookup"><span data-stu-id="44931-127">For example, you can use DPC, ISR, and Image events to determine those components that spend too much time at high interrupt levels.</span></span> <span data-ttu-id="44931-128">Gli eventi DPC e ISR hanno un timestamp di ingresso che viene usato per calcolare la durata delle routine.</span><span class="sxs-lookup"><span data-stu-id="44931-128">DPC and ISR events have an entry time stamp which is used to compute the duration of the routines.</span></span> <span data-ttu-id="44931-129">Gli eventi di immagine vengono letti per costruire le aree di memoria che eseguono il mapping a determinati moduli.</span><span class="sxs-lookup"><span data-stu-id="44931-129">The image events are read to construct the memory regions that map to certain modules.</span></span> <span data-ttu-id="44931-130">È possibile usare il mapping per individuare il modulo che contiene la routine di interrupt.</span><span class="sxs-lookup"><span data-stu-id="44931-130">You can use the mapping to locate the module that contains the interrupt routine.</span></span>

<span data-ttu-id="44931-131">L'evento TimerDPC registra quando un DPC viene attivato in seguito a una scadenza del timer e ai record di evento ThreadDPC quando viene eseguito un DPC a thread.</span><span class="sxs-lookup"><span data-stu-id="44931-131">The TimerDPC event records when a DPC fires as a result of a timer expiration and the ThreadDPC event records when a threaded DPC executes.</span></span>

## <a name="requirements"></a><span data-ttu-id="44931-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44931-132">Requirements</span></span>



| <span data-ttu-id="44931-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="44931-133">Requirement</span></span> | <span data-ttu-id="44931-134">Valore</span><span class="sxs-lookup"><span data-stu-id="44931-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="44931-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44931-135">Minimum supported client</span></span><br/> | <span data-ttu-id="44931-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44931-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="44931-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44931-137">Minimum supported server</span></span><br/> | <span data-ttu-id="44931-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="44931-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





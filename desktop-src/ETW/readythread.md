---
description: Questa classe è la classe del tipo di evento per gli eventi di thread pronti. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 861ab070-5536-4897-b523-9b09a7d59b3e
title: Classe ReadyThread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadyThread
- ReadyThread.TThreadId
- ReadyThread.AdjustReason
- ReadyThread.AdjustIncrement
- ReadyThread.Flag
- ReadyThread.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: e10029c0397c16a5a5eb30be6e3db64c0baec596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879521"
---
# <a name="readythread-class"></a><span data-ttu-id="f6297-104">Classe ReadyThread</span><span class="sxs-lookup"><span data-stu-id="f6297-104">ReadyThread class</span></span>

<span data-ttu-id="f6297-105">Questa classe è la classe del tipo di evento per gli eventi di thread pronti.</span><span class="sxs-lookup"><span data-stu-id="f6297-105">This class is the event type class for ready thread events.</span></span>

<span data-ttu-id="f6297-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="f6297-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6297-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6297-107">Syntax</span></span>

``` syntax
[EventType{50}, EventTypeName{"ReadyThread"}]
class ReadyThread : Thread_V2
{
  uint32 TThreadId;
  sint8  AdjustReason;
  sint8  AdjustIncrement;
  sint8  Flag;
  sint8  Reserved;
};
```

## <a name="members"></a><span data-ttu-id="f6297-108">Members</span><span class="sxs-lookup"><span data-stu-id="f6297-108">Members</span></span>

<span data-ttu-id="f6297-109">La classe **ReadyThread** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f6297-109">The **ReadyThread** class has these types of members:</span></span>

-   [<span data-ttu-id="f6297-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f6297-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6297-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f6297-111">Properties</span></span>

<span data-ttu-id="f6297-112">La classe **ReadyThread** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f6297-112">The **ReadyThread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6297-113">AdjustIncrement</span><span class="sxs-lookup"><span data-stu-id="f6297-113">AdjustIncrement</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6297-114">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="f6297-114">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="f6297-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6297-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6297-116">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="f6297-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="f6297-117">Valore in base al quale viene regolata la priorità.</span><span class="sxs-lookup"><span data-stu-id="f6297-117">The value by which the priority is being adjusted.</span></span>

</dd> <dt>

<span data-ttu-id="f6297-118">AdjustReason</span><span class="sxs-lookup"><span data-stu-id="f6297-118">AdjustReason</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6297-119">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="f6297-119">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="f6297-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6297-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6297-121">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="f6297-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="f6297-122">Motivo del priority boost.</span><span class="sxs-lookup"><span data-stu-id="f6297-122">The reason for the priority boost.</span></span>



| <span data-ttu-id="f6297-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f6297-123">Value</span></span>                                                                        | <span data-ttu-id="f6297-124">Significato</span><span class="sxs-lookup"><span data-stu-id="f6297-124">Meaning</span></span>                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f6297-125"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f6297-125"><dt>0</dt></span></span> </dl> | <span data-ttu-id="f6297-126">Ignorare l'incremento.</span><span class="sxs-lookup"><span data-stu-id="f6297-126">Ignore the increment.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="f6297-127"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f6297-127"><dt>1</dt></span></span> </dl> | <span data-ttu-id="f6297-128">Applicare l'incremento, che decade in modo incrementale alla fine di ogni quantum.</span><span class="sxs-lookup"><span data-stu-id="f6297-128">Apply the increment, which will decay incrementally at the end of each quantum.</span></span><br/>                              |
| <dl> <span data-ttu-id="f6297-129"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f6297-129"><dt>2</dt></span></span> </dl> | <span data-ttu-id="f6297-130">Applicare l'incremento come Boost che dedurrà interamente il suo intero in quantum (in genere per la donazione di priorità).</span><span class="sxs-lookup"><span data-stu-id="f6297-130">Apply the increment as a boost that will decay in its entirety at quantum (typically for priority donation).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f6297-131">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="f6297-131">Flag</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6297-132">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="f6297-132">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="f6297-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6297-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6297-134">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="f6297-134">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="f6297-135">Di seguito sono riportati i flag di stato possibili:</span><span class="sxs-lookup"><span data-stu-id="f6297-135">The following are the possible state flags:</span></span>



| <span data-ttu-id="f6297-136">Valore</span><span class="sxs-lookup"><span data-stu-id="f6297-136">Value</span></span>                                                                          | <span data-ttu-id="f6297-137">Significato</span><span class="sxs-lookup"><span data-stu-id="f6297-137">Meaning</span></span>                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f6297-138"><dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="f6297-138"><dt>0x1</dt></span></span> </dl> | <span data-ttu-id="f6297-139">Il thread è stato preparato da DPC (chiamata di procedura posticipata).</span><span class="sxs-lookup"><span data-stu-id="f6297-139">The thread has been readied from DPC (deferred procedure call).</span></span><br/> |
| <dl> <span data-ttu-id="f6297-140"><dt>0x2</dt></span><span class="sxs-lookup"><span data-stu-id="f6297-140"><dt>0x2</dt></span></span> </dl> | <span data-ttu-id="f6297-141">Lo stack del kernel è attualmente stato scambiato.</span><span class="sxs-lookup"><span data-stu-id="f6297-141">The kernel stack is currently swapped out.</span></span><br/>                      |
| <dl> <span data-ttu-id="f6297-142"><dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="f6297-142"><dt>0x4</dt></span></span> </dl> | <span data-ttu-id="f6297-143">Lo spazio degli indirizzi del processo viene scambiato.</span><span class="sxs-lookup"><span data-stu-id="f6297-143">The process address space is swapped out.</span></span><br/>                       |



 

<span data-ttu-id="f6297-144">Si noti che quando lo stack del kernel o lo spazio degli indirizzi del processo viene sostituito, sarà presente un evento ReadyThread aggiuntivo dopo lo scambio dello stack del kernel o dello spazio degli indirizzi del processo e il thread sarà pronto per l'invio.</span><span class="sxs-lookup"><span data-stu-id="f6297-144">Note that when the kernel stack or the process address space is swapped out, there will be an additional ReadyThread event after the kernel stack or the process address space has been swapped back in and the thread is made ready to be dispatched.</span></span>

</dd> <dt>

<span data-ttu-id="f6297-145">Riservato</span><span class="sxs-lookup"><span data-stu-id="f6297-145">Reserved</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6297-146">Tipo di dati: **sint8**</span><span class="sxs-lookup"><span data-stu-id="f6297-146">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="f6297-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6297-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6297-148">Qualificatori: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="f6297-148">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="f6297-149">Riservato.</span><span class="sxs-lookup"><span data-stu-id="f6297-149">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f6297-150">TThreadId</span><span class="sxs-lookup"><span data-stu-id="f6297-150">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6297-151">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6297-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6297-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f6297-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6297-153">Qualificatori: WmiDataId (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="f6297-153">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="f6297-154">Identificatore del thread di cui è in corso la preparazione per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f6297-154">The thread identifier of the thread being readied for execution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6297-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6297-155">Requirements</span></span>



| <span data-ttu-id="f6297-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6297-156">Requirement</span></span> | <span data-ttu-id="f6297-157">Valore</span><span class="sxs-lookup"><span data-stu-id="f6297-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f6297-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6297-158">Minimum supported client</span></span><br/> | <span data-ttu-id="f6297-159">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f6297-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f6297-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6297-160">Minimum supported server</span></span><br/> | <span data-ttu-id="f6297-161">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f6297-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f6297-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6297-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6297-163">**Thread \_ v2**</span><span class="sxs-lookup"><span data-stu-id="f6297-163">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 





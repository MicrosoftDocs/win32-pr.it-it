---
description: Windows include i nuovi elementi di programmazione seguenti per la sincronizzazione.
ms.assetid: 16cd98d2-adc5-4a14-ad39-a0c5b4cc00cc
title: Novità della sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702ba10126d9c0eeeb85462195680b074918584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231691"
---
# <a name="whats-new-in-synchronization"></a><span data-ttu-id="e9baa-103">Novità della sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="e9baa-103">What's New in Synchronization</span></span>

<span data-ttu-id="e9baa-104">Windows include i nuovi elementi di programmazione seguenti per la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e9baa-104">Windows includes the following new programming elements for synchronization.</span></span>

## <a name="windows-8"></a><span data-ttu-id="e9baa-105">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e9baa-105">Windows 8</span></span>

### <a name="new-functions"></a><span data-ttu-id="e9baa-106">Funzioni nuove</span><span class="sxs-lookup"><span data-stu-id="e9baa-106">New Functions</span></span>

<dl> <dt>

[<span data-ttu-id="e9baa-107">**DeleteSynchronizationBarrier**</span><span class="sxs-lookup"><span data-stu-id="e9baa-107">**DeleteSynchronizationBarrier**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="e9baa-108">Elimina una barriera di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e9baa-108">Deletes a synchronization barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="e9baa-109">**EnterSynchronizationBarrier**</span><span class="sxs-lookup"><span data-stu-id="e9baa-109">**EnterSynchronizationBarrier**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="e9baa-110">Fa in modo che il thread chiamante attenda una barriera di sincronizzazione finché il numero massimo di thread non è entrato nella barriera.</span><span class="sxs-lookup"><span data-stu-id="e9baa-110">Causes the calling thread to wait at a synchronization barrier until the maximum number of threads have entered the barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="e9baa-111">**GetOverlappedResultEx**</span><span class="sxs-lookup"><span data-stu-id="e9baa-111">**GetOverlappedResultEx**</span></span>](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex)
</dt> <dd>

<span data-ttu-id="e9baa-112">Recupera i risultati di un'operazione sovrapposta sul file, named pipe o sul dispositivo di comunicazione specificato entro l'intervallo di timeout specificato.</span><span class="sxs-lookup"><span data-stu-id="e9baa-112">Retrieves the results of an overlapped operation on the specified file, named pipe, or communications device within the specified time-out interval.</span></span> <span data-ttu-id="e9baa-113">Il thread chiamante può eseguire un'attesa di avviso.</span><span class="sxs-lookup"><span data-stu-id="e9baa-113">The calling thread can perform an alertable wait.</span></span>

</dd> <dt>

[<span data-ttu-id="e9baa-114">**InitializeSynchronizationBarrier**</span><span class="sxs-lookup"><span data-stu-id="e9baa-114">**InitializeSynchronizationBarrier**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="e9baa-115">Specifica il numero massimo di thread e il numero di spin per una nuova barriera di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e9baa-115">Specifies the maximum number of threads and spin count for a new synchronization barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="e9baa-116">**WaitOnAddress**</span><span class="sxs-lookup"><span data-stu-id="e9baa-116">**WaitOnAddress**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress)
</dt> <dd>

<span data-ttu-id="e9baa-117">Attende la modifica del valore in corrispondenza dell'indirizzo specificato.</span><span class="sxs-lookup"><span data-stu-id="e9baa-117">Waits for the value at the specified address to change.</span></span>

</dd> <dt>

[<span data-ttu-id="e9baa-118">**WakeByAddressAll**</span><span class="sxs-lookup"><span data-stu-id="e9baa-118">**WakeByAddressAll**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall)
</dt> <dd>

<span data-ttu-id="e9baa-119">Attiva tutti i thread in attesa che il valore di un indirizzo venga modificato.</span><span class="sxs-lookup"><span data-stu-id="e9baa-119">Wakes all threads that are waiting for the value of an address to change.</span></span>

</dd> <dt>

[<span data-ttu-id="e9baa-120">**WakeByAddressSingle**</span><span class="sxs-lookup"><span data-stu-id="e9baa-120">**WakeByAddressSingle**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle)
</dt> <dd>

<span data-ttu-id="e9baa-121">Attiva un thread in attesa della modifica del valore di un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="e9baa-121">Wakes one thread that is waiting for the value of an address to change.</span></span>

</dd> </dl>

### <a name="new-interlocked-functions"></a><span data-ttu-id="e9baa-122">Nuove funzioni Interlocked</span><span class="sxs-lookup"><span data-stu-id="e9baa-122">New Interlocked Functions</span></span>

<dl> <dt>

<span data-ttu-id="e9baa-123">[**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-123">[**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-124">Esegue un'operazione di addizione atomica sui valori **Long** specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-124">Performs an atomic addition operation on the specified **LONG** values.</span></span> <span data-ttu-id="e9baa-125">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-125">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-126">[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-126">[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-127">Esegue un'operazione di addizione atomica sui valori **LONGLONG** specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-127">Performs an atomic addition operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="e9baa-128">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-128">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-129">[**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-129">[**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-130">Esegue un'operazione atomica e sui valori **Long** specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-130">Performs an atomic AND operation on the specified **LONG** values.</span></span> <span data-ttu-id="e9baa-131">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-131">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-132">[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-132">[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-133">Esegue un'operazione atomica e sui valori **char** specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-133">Performs an atomic AND operation on the specified **char** values.</span></span> <span data-ttu-id="e9baa-134">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-134">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-135">[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-135">[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-136">Esegue un'operazione atomica e sui valori **short** specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-136">Performs an atomic AND operation on the specified **SHORT** values.</span></span> <span data-ttu-id="e9baa-137">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-137">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-138">[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-138">[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-139">Esegue un'operazione atomica e sui valori **LONGLONG** specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-139">Performs an atomic AND operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="e9baa-140">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-140">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-141">[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-141">[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-142">Verifica il bit specificato del valore **long64** specificato e lo integra.</span><span class="sxs-lookup"><span data-stu-id="e9baa-142">Tests the specified bit of the specified **LONG64** value and complements it.</span></span> <span data-ttu-id="e9baa-143">L'operazione è atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-143">The operation is atomic.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-144">[**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-144">[**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-145">Verifica il bit specificato del valore **Long** specificato e lo imposta su 0.</span><span class="sxs-lookup"><span data-stu-id="e9baa-145">Tests the specified bit of the specified **LONG** value and sets it to 0.</span></span> <span data-ttu-id="e9baa-146">L'operazione è atomica e viene eseguita con la semantica di acquisizione dell'ordine di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-146">The operation is atomic, and it is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-147">[**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-147">[**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-148">Verifica il bit specificato del valore **Long** specificato e lo imposta su 0.</span><span class="sxs-lookup"><span data-stu-id="e9baa-148">Tests the specified bit of the specified **LONG** value and sets it to 0.</span></span> <span data-ttu-id="e9baa-149">L'operazione è atomica e viene eseguita utilizzando la semantica di rilascio della memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-149">The operation is atomic, and it is performed using memory release semantics.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-150">[**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-150">[**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-151">Verifica il bit specificato del valore **Long** specificato e lo imposta su 1.</span><span class="sxs-lookup"><span data-stu-id="e9baa-151">Tests the specified bit of the specified **LONG** value and sets it to 1.</span></span> <span data-ttu-id="e9baa-152">L'operazione è atomica e viene eseguita con la semantica di acquisizione dell'ordine di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-152">The operation is atomic, and it is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-153">[**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-153">[**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-154">Verifica il bit specificato del valore **Long** specificato e lo imposta su 1.</span><span class="sxs-lookup"><span data-stu-id="e9baa-154">Tests the specified bit of the specified **LONG** value and sets it to 1.</span></span> <span data-ttu-id="e9baa-155">L'operazione è atomica e viene eseguita con la semantica di ordinamento della memoria di rilascio.</span><span class="sxs-lookup"><span data-stu-id="e9baa-155">The operation is atomic, and it is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-156">[**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-156">[**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-157">Esegue un'operazione di confronto e scambio atomica sui valori specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-157">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="e9baa-158">La funzione Confronta due valori a 32 bit specificati e scambia con un altro valore a 32 bit in base al risultato del confronto.</span><span class="sxs-lookup"><span data-stu-id="e9baa-158">The function compares two specified 32-bit values and exchanges with another 32-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="e9baa-159">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-159">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="e9baa-160">**InterlockedCompareExchange16**</span><span class="sxs-lookup"><span data-stu-id="e9baa-160">**InterlockedCompareExchange16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange16)
</dt> <dd>

<span data-ttu-id="e9baa-161">Esegue un'operazione di confronto e scambio atomica sui valori specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-161">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="e9baa-162">La funzione Confronta due valori a 16 bit specificati e scambia con un altro valore a 16 bit in base al risultato del confronto.</span><span class="sxs-lookup"><span data-stu-id="e9baa-162">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-163">[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-163">[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-164">Esegue un'operazione di confronto e scambio atomica sui valori specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-164">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="e9baa-165">La funzione Confronta due valori a 16 bit specificati e scambia con un altro valore a 16 bit in base al risultato del confronto.</span><span class="sxs-lookup"><span data-stu-id="e9baa-165">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="e9baa-166">L'operazione viene eseguita con la semantica di ordinamento della memoria acquisita.</span><span class="sxs-lookup"><span data-stu-id="e9baa-166">The operation is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-167">[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-167">[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-168">Esegue un'operazione di confronto e scambio atomica sui valori specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-168">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="e9baa-169">La funzione Confronta due valori a 16 bit specificati e scambia con un altro valore a 16 bit in base al risultato del confronto.</span><span class="sxs-lookup"><span data-stu-id="e9baa-169">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="e9baa-170">Lo scambio viene eseguito con la semantica di ordinamento della memoria di rilascio.</span><span class="sxs-lookup"><span data-stu-id="e9baa-170">The exchange is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-171">[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-171">[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-172">Esegue un'operazione di confronto e scambio atomica sui valori specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-172">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="e9baa-173">La funzione Confronta due valori a 16 bit specificati e scambia con un altro valore a 16 bit in base al risultato del confronto.</span><span class="sxs-lookup"><span data-stu-id="e9baa-173">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="e9baa-174">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-174">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-175">[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-175">[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-176">Esegue un'operazione di confronto e scambio atomica sui valori specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-176">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="e9baa-177">La funzione Confronta due valori a 64 bit specificati e scambia con un altro valore a 64 bit in base al risultato del confronto.</span><span class="sxs-lookup"><span data-stu-id="e9baa-177">The function compares two specified 64-bit values and exchanges with another 64-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="e9baa-178">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-178">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="e9baa-179">**InterlockedCompareExchange128**</span><span class="sxs-lookup"><span data-stu-id="e9baa-179">**InterlockedCompareExchange128**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange128)
</dt> <dd>

<span data-ttu-id="e9baa-180">Esegue un'operazione di confronto e scambio atomica sui valori specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-180">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="e9baa-181">La funzione Confronta due valori a 128 bit specificati e scambia con un altro valore a 128 bit in base al risultato del confronto.</span><span class="sxs-lookup"><span data-stu-id="e9baa-181">The function compares two specified 128-bit values and exchanges with another 128-bit value based on the outcome of the comparison.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-182">[**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-182">[**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-183">Esegue un'operazione di confronto e scambio atomica sui valori specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-183">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="e9baa-184">La funzione Confronta due valori di puntatore e scambi specificati con un altro valore del puntatore in base al risultato del confronto.</span><span class="sxs-lookup"><span data-stu-id="e9baa-184">The function compares two specified pointer values and exchanges with another pointer value based on the outcome of the comparison.</span></span> <span data-ttu-id="e9baa-185">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-185">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-186">[**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-186">[**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-187">Decrementa (diminuisce di uno) il valore della variabile a 32 bit specificata come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-187">Decrements (decreases by one) the value of the specified 32-bit variable as an atomic operation.</span></span> <span data-ttu-id="e9baa-188">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-188">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="e9baa-189">**InterlockedDecrement16**</span><span class="sxs-lookup"><span data-stu-id="e9baa-189">**InterlockedDecrement16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockeddecrement16)
</dt> <dd>

<span data-ttu-id="e9baa-190">Decrementa (diminuisce di uno) il valore della variabile a 16 bit specificata come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-190">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-191">[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-191">[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-192">Decrementa (diminuisce di uno) il valore della variabile a 16 bit specificata come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-192">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="e9baa-193">L'operazione viene eseguita con la semantica di ordinamento della memoria acquisita.</span><span class="sxs-lookup"><span data-stu-id="e9baa-193">The operation is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-194">[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-194">[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-195">Decrementa (diminuisce di uno) il valore della variabile a 16 bit specificata come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-195">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="e9baa-196">L'operazione viene eseguita con la semantica di ordinamento della memoria di rilascio.</span><span class="sxs-lookup"><span data-stu-id="e9baa-196">The operation is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-197">[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-197">[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-198">Decrementa (diminuisce di uno) il valore della variabile a 16 bit specificata come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-198">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="e9baa-199">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-199">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-200">[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-200">[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-201">Decrementa (diminuisce di uno) il valore della variabile a 64 bit specificata come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-201">Decrements (decreases by one) the value of the specified 64-bit variable as an atomic operation.</span></span> <span data-ttu-id="e9baa-202">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-202">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-203">[**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-203">[**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-204">Imposta una variabile a 64 bit sul valore specificato come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-204">Sets a 64-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="e9baa-205">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-205">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="e9baa-206">**InterlockedExchange8**</span><span class="sxs-lookup"><span data-stu-id="e9baa-206">**InterlockedExchange8**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedexchange8)
</dt> <dd>

<span data-ttu-id="e9baa-207">Imposta una variabile a 8 bit sul valore specificato come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-207">Sets an 8-bit variable to the specified value as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-208">[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-208">[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-209">Imposta una variabile a 16 bit sul valore specificato come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-209">Sets a 16-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="e9baa-210">L'operazione viene eseguita usando la semantica di acquisizione dell'ordine di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-210">The operation is performed using acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-211">[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-211">[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-212">Imposta una variabile a 16 bit sul valore specificato come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-212">Sets a 16-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="e9baa-213">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-213">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-214">[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-214">[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-215">Imposta una variabile a 64 bit sul valore specificato come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-215">Sets a 64-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="e9baa-216">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-216">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-217">[**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-217">[**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-218">Scambia atomicamente una coppia di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="e9baa-218">Atomically exchanges a pair of addresses.</span></span> <span data-ttu-id="e9baa-219">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-219">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-220">[**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-220">[**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-221">Esegue un'aggiunta atomica di valori a 2 32 bit.</span><span class="sxs-lookup"><span data-stu-id="e9baa-221">Performs an atomic addition of two 32-bit values.</span></span> <span data-ttu-id="e9baa-222">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-222">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-223">[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-223">[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-224">Esegue un'aggiunta atomica di valori a 2 64 bit.</span><span class="sxs-lookup"><span data-stu-id="e9baa-224">Performs an atomic addition of two 64-bit values.</span></span> <span data-ttu-id="e9baa-225">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-225">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-226">[**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-226">[**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-227">Incrementa (aumenta di uno) il valore della variabile a 32 bit specificata come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-227">Increments (increases by one) the value of the specified 32-bit variable as an atomic operation.</span></span> <span data-ttu-id="e9baa-228">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-228">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="e9baa-229">**InterlockedIncrement16**</span><span class="sxs-lookup"><span data-stu-id="e9baa-229">**InterlockedIncrement16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedincrement16)
</dt> <dd>

<span data-ttu-id="e9baa-230">Incrementa (aumenta di uno) il valore della variabile a 16 bit specificata come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-230">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-231">[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-231">[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-232">Incrementa (aumenta di uno) il valore della variabile a 16 bit specificata come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-232">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="e9baa-233">L'operazione viene eseguita usando la semantica di acquisizione dell'ordine di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-233">The operation is performed using acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-234">[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-234">[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-235">Incrementa (aumenta di uno) il valore della variabile a 16 bit specificata come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-235">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="e9baa-236">L'operazione viene eseguita usando la semantica di ordinamento della memoria di rilascio.</span><span class="sxs-lookup"><span data-stu-id="e9baa-236">The operation is performed using release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-237">[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-237">[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-238">Incrementa (aumenta di uno) il valore della variabile a 16 bit specificata come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-238">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="e9baa-239">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-239">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-240">[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-240">[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-241">Incrementa (aumenta di uno) il valore della variabile a 64 bit specificata come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="e9baa-241">Increments (increases by one) the value of the specified 64-bit variable as an atomic operation.</span></span> <span data-ttu-id="e9baa-242">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-242">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-243">[**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-243">[**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-244">Esegue un'operazione atomica o sui valori **Long** specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-244">Performs an atomic OR operation on the specified **LONG** values.</span></span> <span data-ttu-id="e9baa-245">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-245">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-246">[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-246">[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-247">Esegue un'operazione atomica o sui valori **char** specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-247">Performs an atomic OR operation on the specified **char** values.</span></span> <span data-ttu-id="e9baa-248">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-248">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-249">[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-249">[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-250">Esegue un'operazione atomica o sui valori **short** specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-250">Performs an atomic OR operation on the specified **SHORT** values.</span></span> <span data-ttu-id="e9baa-251">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-251">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-252">[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-252">[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-253">Esegue un'operazione atomica o sui valori **LONGLONG** specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-253">Performs an atomic OR operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="e9baa-254">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-254">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="e9baa-255">**InterlockedPushListSListEx**</span><span class="sxs-lookup"><span data-stu-id="e9baa-255">**InterlockedPushListSListEx**</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)
</dt> <dd>

<span data-ttu-id="e9baa-256">Inserisce un elenco collegato singolarmente davanti a un altro elenco collegato singolarmente.</span><span class="sxs-lookup"><span data-stu-id="e9baa-256">Inserts a singly-linked list at the front of another singly linked list.</span></span> <span data-ttu-id="e9baa-257">L'accesso agli elenchi è sincronizzato in un sistema multiprocessore.</span><span class="sxs-lookup"><span data-stu-id="e9baa-257">Access to the lists is synchronized on a multiprocessor system.</span></span> <span data-ttu-id="e9baa-258">Questa versione del metodo non usa la convenzione di chiamata [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx) .</span><span class="sxs-lookup"><span data-stu-id="e9baa-258">This version of the method does not use the [\_\_fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx) calling convention.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-259">[**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-259">[**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-260">Esegue un'operazione Atomic XOR sui valori **Long** specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-260">Performs an atomic XOR operation on the specified **LONG** values.</span></span> <span data-ttu-id="e9baa-261">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-261">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-262">[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-262">[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-263">Esegue un'operazione Atomic XOR sui valori **char** specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-263">Performs an atomic XOR operation on the specified **char** values.</span></span> <span data-ttu-id="e9baa-264">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-264">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-265">[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-265">[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-266">Esegue un'operazione Atomic XOR sui valori **short** specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-266">Performs an atomic XOR operation on the specified **SHORT** values.</span></span> <span data-ttu-id="e9baa-267">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-267">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="e9baa-268">[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9baa-268">[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e9baa-269">Esegue un'operazione Atomic XOR sui valori **LONGLONG** specificati.</span><span class="sxs-lookup"><span data-stu-id="e9baa-269">Performs an atomic XOR operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="e9baa-270">L'operazione viene eseguita in modo atomico, ma senza usare barriere di memoria.</span><span class="sxs-lookup"><span data-stu-id="e9baa-270">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> </dl>

## <a name="windows-7"></a><span data-ttu-id="e9baa-271">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e9baa-271">Windows 7</span></span>

### <a name="new-functions"></a><span data-ttu-id="e9baa-272">Funzioni nuove</span><span class="sxs-lookup"><span data-stu-id="e9baa-272">New Functions</span></span>

<dl> <dt>

[<span data-ttu-id="e9baa-273">**SetWaitableTimerEx**</span><span class="sxs-lookup"><span data-stu-id="e9baa-273">**SetWaitableTimerEx**</span></span>](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)
</dt> <dd>

<span data-ttu-id="e9baa-274">Attiva il timer di attesa specificato e fornisce informazioni sul contesto per il timer.</span><span class="sxs-lookup"><span data-stu-id="e9baa-274">Activates the specified waitable timer and provides context information for the timer.</span></span>

</dd> <dt>

[<span data-ttu-id="e9baa-275">**TryAcquireSRWLockExclusive**</span><span class="sxs-lookup"><span data-stu-id="e9baa-275">**TryAcquireSRWLockExclusive**</span></span>](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)
</dt> <dd>

<span data-ttu-id="e9baa-276">Tenta di acquisire un blocco di lettura/scrittura (SRW) Slim in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="e9baa-276">Attempts to acquire a slim reader/writer (SRW) lock in exclusive mode.</span></span> <span data-ttu-id="e9baa-277">Se la chiamata ha esito positivo, il thread chiamante acquisisce la proprietà del blocco.</span><span class="sxs-lookup"><span data-stu-id="e9baa-277">If the call is successful, the calling thread takes ownership of the lock.</span></span>

</dd> <dt>

[<span data-ttu-id="e9baa-278">**TryAcquireSRWLockShared**</span><span class="sxs-lookup"><span data-stu-id="e9baa-278">**TryAcquireSRWLockShared**</span></span>](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)
</dt> <dd>

<span data-ttu-id="e9baa-279">Tenta di acquisire un blocco di lettura/scrittura (SRW) Slim in modalità condivisa.</span><span class="sxs-lookup"><span data-stu-id="e9baa-279">Attempts to acquire a slim reader/writer (SRW) lock in shared mode.</span></span> <span data-ttu-id="e9baa-280">Se la chiamata ha esito positivo, il thread chiamante acquisisce la proprietà del blocco.</span><span class="sxs-lookup"><span data-stu-id="e9baa-280">If the call is successful, the calling thread takes ownership of the lock.</span></span>

</dd> </dl>

### <a name="new-structures"></a><span data-ttu-id="e9baa-281">Nuove strutture</span><span class="sxs-lookup"><span data-stu-id="e9baa-281">New Structures</span></span>

<dl> <dt>

[<span data-ttu-id="e9baa-282">**\_contesto motivo**</span><span class="sxs-lookup"><span data-stu-id="e9baa-282">**REASON\_CONTEXT**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-reason_context)
</dt> <dd>

<span data-ttu-id="e9baa-283">Contiene informazioni di contesto per un timer attivato con [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex).</span><span class="sxs-lookup"><span data-stu-id="e9baa-283">Contains context information for a timer activated with [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex).</span></span>

</dd> </dl>

 

 

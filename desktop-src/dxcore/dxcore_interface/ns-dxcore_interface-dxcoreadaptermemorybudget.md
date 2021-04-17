---
title: DXCoreAdapterMemoryBudget
description: Descrive il budget della memoria per un adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2888b1480e3e394640a10bf0264403cd6c153e3b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474070"
---
# <a name="dxcoreadaptermemorybudget-structure"></a><span data-ttu-id="6c971-103">Struttura DXCoreAdapterMemoryBudget</span><span class="sxs-lookup"><span data-stu-id="6c971-103">DXCoreAdapterMemoryBudget structure</span></span>

<span data-ttu-id="6c971-104">Specifica lo stato dell'adattatore <em>AdapterMemoryBudget</em> , che recupera o richiede il budget di memoria dell'adapter per l'adapter.</span><span class="sxs-lookup"><span data-stu-id="6c971-104">Specifies the <em>AdapterMemoryBudget</em> adapter state, which retrieves or requests the adapter memory budget on the adapter.</span></span> <span data-ttu-id="6c971-105">Impostando (richiedente) un budget rappresenta la memoria fisica minima richiesta da riservare, in byte, sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="6c971-105">Setting (requesting) a budget represents the minimum required physical memory to reserve, in bytes, on the adapter.</span></span> <span data-ttu-id="6c971-106">Si consiglia di impostare una prenotazione per l'adapter per indicare la quantità di memoria fisica che l'applicazione non può usare.</span><span class="sxs-lookup"><span data-stu-id="6c971-106">We recommend that you set an adapter reservation in order to denote the amount of physical memory that your application can't go without.</span></span> <span data-ttu-id="6c971-107">Questo valore consente al sistema operativo di ridurre rapidamente l'effetto di grandi situazioni di pressione della memoria.</span><span class="sxs-lookup"><span data-stu-id="6c971-107">This value helps the operating system (OS) to quickly minimize the impact of large memory-pressure situations.</span></span>

<span data-ttu-id="6c971-108">Quando si chiama [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), lo stato dell'adattatore <em>AdapterMemoryBudget</em> è <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> per *inputStateDetails* e il tipo **DXCoreAdapterMemoryBudget** per *outputBuffer*.</span><span class="sxs-lookup"><span data-stu-id="6c971-108">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type **DXCoreAdapterMemoryBudget** for *outputBuffer*.</span></span>

<span data-ttu-id="6c971-109">Quando si [chiama lo stato,](./nf-dxcore_interface-idxcoreadapter-setstate.md)lo stato dell'adattatore <em>AdapterMemoryBudget</em> è di tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> per *inputStateDetails* e il tipo **uint64_t** per *inputData*.</span><span class="sxs-lookup"><span data-stu-id="6c971-109">When calling [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type **uint64_t** for *inputData*.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c971-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c971-110">Syntax</span></span>

```cpp
struct DXCoreAdapterMemoryBudget
{
  uint64_t budget;
  uint64_t currentUsage;
  uint64_t availableForReservation;
  uint64_t currentReservation;
};
```

## <a name="members"></a><span data-ttu-id="6c971-111">Members</span><span class="sxs-lookup"><span data-stu-id="6c971-111">Members</span></span>

### <a name="budget"></a><span data-ttu-id="6c971-112">budget</span><span class="sxs-lookup"><span data-stu-id="6c971-112">budget</span></span>

<span data-ttu-id="6c971-113">Tipo: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="6c971-113">Type: **uint64_t**</span></span>

<span data-ttu-id="6c971-114">Specifica il budget di memoria dell'adapter fornito dal sistema operativo, in byte, di destinazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c971-114">Specifies the OS-provided adapter memory budget, in bytes, that your application should target.</span></span> <span data-ttu-id="6c971-115">Se il valore di *currentUsage* è maggiore del *budget*, l'applicazione potrebbe comportare un calo o un calo delle prestazioni a causa dell'attività in background da parte del sistema operativo, progettato per fornire ad altre applicazioni un utilizzo corretto della memoria dell'adapter.</span><span class="sxs-lookup"><span data-stu-id="6c971-115">If *currentUsage* is greater than *budget*, then your application may incur stuttering or performance penalties due to background activity by the OS, which is intended to provide other applications with a fair usage of adapter memory.</span></span>

### <a name="currentusage"></a><span data-ttu-id="6c971-116">currentUsage</span><span class="sxs-lookup"><span data-stu-id="6c971-116">currentUsage</span></span>

<span data-ttu-id="6c971-117">Tipo: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="6c971-117">Type: **uint64_t**</span></span>

<span data-ttu-id="6c971-118">Specifica l'utilizzo corrente della memoria dell'adapter Applicaton, in byte.</span><span class="sxs-lookup"><span data-stu-id="6c971-118">Specifies your applicaton's current adapter memory usage, in bytes.</span></span>

### <a name="availableforreservation"></a><span data-ttu-id="6c971-119">availableForReservation</span><span class="sxs-lookup"><span data-stu-id="6c971-119">availableForReservation</span></span>

<span data-ttu-id="6c971-120">Tipo: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="6c971-120">Type: **uint64_t**</span></span>

<span data-ttu-id="6c971-121">Specifica la quantità di memoria dell'adapter, in byte, disponibile per la prenotazione da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c971-121">Specifies the amount of adapter memory, in bytes, that your application has available for reservation.</span></span> <span data-ttu-id="6c971-122">Per riservare la memoria dell'adapter, l'applicazione deve chiamare [IDXCoreAdapter:: sestate](./nf-dxcore_interface-idxcoreadapter-setstate.md) con *stato* impostato su [DXCoreAdapterState:: AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md).</span><span class="sxs-lookup"><span data-stu-id="6c971-122">To reserve this adapter memory, your application should call [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) with *state* set to [DXCoreAdapterState::AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md).</span></span>

### <a name="currentreservation"></a><span data-ttu-id="6c971-123">currentReservation</span><span class="sxs-lookup"><span data-stu-id="6c971-123">currentReservation</span></span>

<span data-ttu-id="6c971-124">Tipo: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="6c971-124">Type: **uint64_t**</span></span>

<span data-ttu-id="6c971-125">Specifica la quantità di memoria dell'adapter, in byte, riservata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c971-125">Specifies the amount of adapter memory, in bytes, that is reserved by your application.</span></span> <span data-ttu-id="6c971-126">Il sistema operativo usa la prenotazione come un suggerimento per determinare la working set minima dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c971-126">The OS uses the reservation as a hint to determine your application's minimum working set.</span></span> <span data-ttu-id="6c971-127">L'applicazione deve tentare di verificare che l'utilizzo della memoria dell'adapter possa essere tagliato per soddisfare questo requisito.</span><span class="sxs-lookup"><span data-stu-id="6c971-127">Your application should attempt to ensure that its adapter memory usage can be trimmed to meet this requirement.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c971-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c971-128">See also</span></span>

<span data-ttu-id="6c971-129">Guida di [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="6c971-129">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
---
description: Gruppo di metodi utilizzato per modificare i blocchi.
ms.assetid: ba4cc37c-bd2f-446f-8b3d-bc2a2e2e4de4
title: Metodi CShareLockNH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b16a979c5d1f111c92a64376c48f4c0ed1a165ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304658"
---
# <a name="csharelocknh-methods"></a><span data-ttu-id="786ef-103">Metodi CShareLockNH</span><span class="sxs-lookup"><span data-stu-id="786ef-103">CShareLockNH Methods</span></span>

<span data-ttu-id="786ef-104">Gruppo di metodi utilizzato per modificare i blocchi.</span><span class="sxs-lookup"><span data-stu-id="786ef-104">A group of methods that is used to manipulate locks.</span></span>

## <a name="methods"></a><span data-ttu-id="786ef-105">Metodi</span><span class="sxs-lookup"><span data-stu-id="786ef-105">Methods</span></span>

<span data-ttu-id="786ef-106">Di seguito sono riportati i metodi esportati da Rwnh.dll.</span><span class="sxs-lookup"><span data-stu-id="786ef-106">The following are methods exported by Rwnh.dll.</span></span>



| <span data-ttu-id="786ef-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="786ef-107">Method</span></span>                                                                   | <span data-ttu-id="786ef-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="786ef-108">Description</span></span>                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="786ef-109">**ExclusiveLock**</span><span class="sxs-lookup"><span data-stu-id="786ef-109">**ExclusiveLock**</span></span>](csharelocknh--exclusivelock.md)                     | <span data-ttu-id="786ef-110">Acquisisce un blocco in lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="786ef-110">Acquires a reader/writer lock.</span></span>                                  |
| [<span data-ttu-id="786ef-111">**ExclusiveToPartial**</span><span class="sxs-lookup"><span data-stu-id="786ef-111">**ExclusiveToPartial**</span></span>](csharelocknh--exclusivetopartial.md)           | <span data-ttu-id="786ef-112">Modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="786ef-112">Changes the state.</span></span>                                              |
| [<span data-ttu-id="786ef-113">**ExclusiveUnlock**</span><span class="sxs-lookup"><span data-stu-id="786ef-113">**ExclusiveUnlock**</span></span>](csharelocknh--exclusiveunlock.md)                 | <span data-ttu-id="786ef-114">Rilascia un blocco.</span><span class="sxs-lookup"><span data-stu-id="786ef-114">Releases a lock.</span></span>                                                |
| [<span data-ttu-id="786ef-115">**FirstPartialToExclusive**</span><span class="sxs-lookup"><span data-stu-id="786ef-115">**FirstPartialToExclusive**</span></span>](csharelocknh--firstpartialtoexclusive.md) | <span data-ttu-id="786ef-116">Utilizzato per la conversione di un blocco parziale in un blocco esclusivo.</span><span class="sxs-lookup"><span data-stu-id="786ef-116">Used in converting a partial lock to an exclusive lock.</span></span>         |
| [<span data-ttu-id="786ef-117">**PartialLock**</span><span class="sxs-lookup"><span data-stu-id="786ef-117">**PartialLock**</span></span>](csharelocknh--partiallock.md)                         | <span data-ttu-id="786ef-118">Impedisce a più di un thread di completare l'acquisizione di un blocco.</span><span class="sxs-lookup"><span data-stu-id="786ef-118">Prevents more than one thread from completing acquiring a lock.</span></span> |
| [<span data-ttu-id="786ef-119">**PartialUnlock**</span><span class="sxs-lookup"><span data-stu-id="786ef-119">**PartialUnlock**</span></span>](csharelocknh--partialunlock.md)                     | <span data-ttu-id="786ef-120">Rilascia un blocco parziale.</span><span class="sxs-lookup"><span data-stu-id="786ef-120">Releases a partial lock.</span></span>                                        |
| [<span data-ttu-id="786ef-121">**ShareLock**</span><span class="sxs-lookup"><span data-stu-id="786ef-121">**ShareLock**</span></span>](csharelocknh--sharelock.md)                             | <span data-ttu-id="786ef-122">Ottiene un blocco per la modalità condivisa.</span><span class="sxs-lookup"><span data-stu-id="786ef-122">Obtains a lock for shared mode.</span></span>                                 |
| [<span data-ttu-id="786ef-123">**ShareUnlock**</span><span class="sxs-lookup"><span data-stu-id="786ef-123">**ShareUnlock**</span></span>](csharelocknh--shareunlock.md)                         | <span data-ttu-id="786ef-124">Rilascia un blocco dalla modalità condivisa.</span><span class="sxs-lookup"><span data-stu-id="786ef-124">Releases a lock from shared mode.</span></span>                               |
| [<span data-ttu-id="786ef-125">**SharedToPartial**</span><span class="sxs-lookup"><span data-stu-id="786ef-125">**SharedToPartial**</span></span>](csharelocknh--sharedtopartial.md)                 | <span data-ttu-id="786ef-126">Ottiene un blocco parziale.</span><span class="sxs-lookup"><span data-stu-id="786ef-126">Obtains a partial lock.</span></span>                                         |
| [<span data-ttu-id="786ef-127">**TryExclusiveLock**</span><span class="sxs-lookup"><span data-stu-id="786ef-127">**TryExclusiveLock**</span></span>](csharelocknh--tryexclusivelock.md)               | <span data-ttu-id="786ef-128">Ottiene un blocco in modo esclusivo.</span><span class="sxs-lookup"><span data-stu-id="786ef-128">Obtains a lock exclusively.</span></span>                                     |



 

 

 




---
description: La classe CCritSec fornisce un blocco thread.
ms.assetid: ecc60afe-15d0-4780-8133-1dfc558c6325
title: Classe CCritSec (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8db0243ecfecd47655f547d40390e602c04d5b88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326829"
---
# <a name="ccritsec-class"></a><span data-ttu-id="445f7-103">Classe CCritSec</span><span class="sxs-lookup"><span data-stu-id="445f7-103">CCritSec class</span></span>

<span data-ttu-id="445f7-104">La classe **CCritSec** fornisce un blocco thread.</span><span class="sxs-lookup"><span data-stu-id="445f7-104">The **CCritSec** class provides a thread lock.</span></span>

<span data-ttu-id="445f7-105">Questa classe è un wrapper sottile per un oggetto **\_ sezione critica** di Windows.</span><span class="sxs-lookup"><span data-stu-id="445f7-105">This class is a thin wrapper for a Windows **CRITICAL\_SECTION** object.</span></span> <span data-ttu-id="445f7-106">È possibile bloccare e sbloccare il thread chiamando il metodo [**CCritSec:: Lock**](ccritsec-lock.md) e [**CCritSec:: Unlock**](ccritsec-unlock.md) .</span><span class="sxs-lookup"><span data-stu-id="445f7-106">You can lock and unlock the thread by calling the [**CCritSec::Lock**](ccritsec-lock.md) and [**CCritSec::Unlock**](ccritsec-unlock.md) methods.</span></span> <span data-ttu-id="445f7-107">Tuttavia, è più sicuro usare questa classe insieme alla classe [**CAutoLock**](cautolock.md) .</span><span class="sxs-lookup"><span data-stu-id="445f7-107">However, it is safer to use this class in conjunction with the [**CAutoLock**](cautolock.md) class.</span></span> <span data-ttu-id="445f7-108">Quando la classe **CAutoLock** esce dall'ambito, sblocca automaticamente l'oggetto **CCritSec** .</span><span class="sxs-lookup"><span data-stu-id="445f7-108">When the **CAutoLock** class goes out of scope, it automatically unlocks the **CCritSec** object.</span></span> <span data-ttu-id="445f7-109">Inoltre, viene compilato in codice inline efficiente.</span><span class="sxs-lookup"><span data-stu-id="445f7-109">Moreover, it compiles to efficient inline code.</span></span>



| <span data-ttu-id="445f7-110">Variabili membro pubblico</span><span class="sxs-lookup"><span data-stu-id="445f7-110">Public Member Variables</span></span>                            | <span data-ttu-id="445f7-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="445f7-111">Description</span></span>                                              |
|----------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="445f7-112">**\_currentOwner m**</span><span class="sxs-lookup"><span data-stu-id="445f7-112">**m\_currentOwner**</span></span>](ccritsec-m-currentowner.md) | <span data-ttu-id="445f7-113">Identificatore del thread proprietario.</span><span class="sxs-lookup"><span data-stu-id="445f7-113">Thread identifier of the owning thread.</span></span>                  |
| [<span data-ttu-id="445f7-114">**\_lockCount m**</span><span class="sxs-lookup"><span data-stu-id="445f7-114">**m\_lockCount**</span></span>](ccritsec-m-lockcount.md)       | <span data-ttu-id="445f7-115">Numero di blocchi in attesa su questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="445f7-115">Number of outstanding locks on this object.</span></span>              |
| [<span data-ttu-id="445f7-116">**\_fTrace m**</span><span class="sxs-lookup"><span data-stu-id="445f7-116">**m\_fTrace**</span></span>](ccritsec-m-ftrace.md)             | <span data-ttu-id="445f7-117">Valore booleano che specifica se tracciare il blocco.</span><span class="sxs-lookup"><span data-stu-id="445f7-117">Boolean value that specifies whether to trace this lock.</span></span> |
| <span data-ttu-id="445f7-118">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="445f7-118">Public Methods</span></span>                                     | <span data-ttu-id="445f7-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="445f7-119">Description</span></span>                                              |
| [<span data-ttu-id="445f7-120">**CCritSec**</span><span class="sxs-lookup"><span data-stu-id="445f7-120">**CCritSec**</span></span>](ccritsec-ccritsec.md)              | <span data-ttu-id="445f7-121">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="445f7-121">Constructor method.</span></span>                                      |
| [<span data-ttu-id="445f7-122">**~ CCritSec**</span><span class="sxs-lookup"><span data-stu-id="445f7-122">**~CCritSec**</span></span>](ccritsec--ccritsec.md)            | <span data-ttu-id="445f7-123">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="445f7-123">Destructor method.</span></span>                                       |
| [<span data-ttu-id="445f7-124">**Lock**</span><span class="sxs-lookup"><span data-stu-id="445f7-124">**Lock**</span></span>](ccritsec-lock.md)                      | <span data-ttu-id="445f7-125">Blocca l'oggetto sezione critica.</span><span class="sxs-lookup"><span data-stu-id="445f7-125">Locks the critical section object.</span></span>                       |
| [<span data-ttu-id="445f7-126">**Sblocca**</span><span class="sxs-lookup"><span data-stu-id="445f7-126">**Unlock**</span></span>](ccritsec-unlock.md)                  | <span data-ttu-id="445f7-127">Sblocca l'oggetto sezione critica.</span><span class="sxs-lookup"><span data-stu-id="445f7-127">Unlocks the critical section object.</span></span>                     |



 

## <a name="requirements"></a><span data-ttu-id="445f7-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="445f7-128">Requirements</span></span>



| <span data-ttu-id="445f7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="445f7-129">Requirement</span></span> | <span data-ttu-id="445f7-130">Valore</span><span class="sxs-lookup"><span data-stu-id="445f7-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="445f7-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="445f7-131">Header</span></span><br/>  | <dl> <span data-ttu-id="445f7-132"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="445f7-132"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="445f7-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="445f7-133">Library</span></span><br/> | <dl> <span data-ttu-id="445f7-134"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="445f7-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="445f7-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="445f7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="445f7-136">Oggetti sezione critica</span><span class="sxs-lookup"><span data-stu-id="445f7-136">Critical Section Objects</span></span>](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[<span data-ttu-id="445f7-137">Riferimento alla classe base DirectShow</span><span class="sxs-lookup"><span data-stu-id="445f7-137">DirectShow Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 


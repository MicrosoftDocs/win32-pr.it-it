---
description: Una transazione è un oggetto che definisce un'unità logica di lavoro.
ms.assetid: 29661a58-ada9-4b7c-8d85-ab65b824c7cd
title: Transazioni (gestione transazioni kernel)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff77ae0d89f5e334319ea0b7b73c27a4b34b57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311126"
---
# <a name="transactions"></a><span data-ttu-id="be4e8-103">Transazioni</span><span class="sxs-lookup"><span data-stu-id="be4e8-103">Transactions</span></span>

<span data-ttu-id="be4e8-104">Una transazione è un oggetto che definisce un'unità logica di lavoro.</span><span class="sxs-lookup"><span data-stu-id="be4e8-104">A transaction is an object that defines a logical unit of work.</span></span> <span data-ttu-id="be4e8-105">La transazione è attiva finché è presente un handle che fa riferimento alla transazione e viene considerato attivo se non è ancora stato eseguito il commit o il rollback della transazione.</span><span class="sxs-lookup"><span data-stu-id="be4e8-105">The transaction is alive as long as there is a handle referencing the transaction and it is considered active if the transaction has not yet been committed or rolled back.</span></span> <span data-ttu-id="be4e8-106">Se viene creata una transazione e tutti gli handle sono stati chiusi prima del commit o del rollback, viene eseguito il rollback della transazione.</span><span class="sxs-lookup"><span data-stu-id="be4e8-106">If a transaction is created and all handles to it have been closed before a commit or rollback occurs, the transaction will be rolled back.</span></span>

<span data-ttu-id="be4e8-107">Si consideri il caso di un client transazionale in modalità utente che crea una transazione per definire l'ambito delle operazioni, quindi esegue gli aggiornamenti in uno o più gestori di risorse.</span><span class="sxs-lookup"><span data-stu-id="be4e8-107">Consider the case of a user-mode transactional client that creates a transaction to scope its operations, then performs updates on one or more resource managers.</span></span> <span data-ttu-id="be4e8-108">Si verifica quanto segue:</span><span class="sxs-lookup"><span data-stu-id="be4e8-108">The following occurs:</span></span>

1.  <span data-ttu-id="be4e8-109">Il client chiama la funzione [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) per creare la transazione e riceve un handle per tale transazione come valore restituito.</span><span class="sxs-lookup"><span data-stu-id="be4e8-109">The client calls the [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) function to create the transaction and receives a handle to that transaction as the return value.</span></span>

    <span data-ttu-id="be4e8-110">La transazione può essere aperta o ereditata da un numero qualsiasi di processi. ogni processo è quindi occupato dalla transazione.</span><span class="sxs-lookup"><span data-stu-id="be4e8-110">The transaction can be opened or inherited by any number of processes; each process is thus involved in the transaction.</span></span> <span data-ttu-id="be4e8-111">L'errore di uno di questi processi causerà l'interruzione della transazione.</span><span class="sxs-lookup"><span data-stu-id="be4e8-111">The failure of any of these processes will cause the transaction to abort.</span></span>

    <span data-ttu-id="be4e8-112">Questa transazione potrebbe non essere ancora persistente.</span><span class="sxs-lookup"><span data-stu-id="be4e8-112">This transaction may not yet be persistent.</span></span> <span data-ttu-id="be4e8-113">Se la transazione utilizza la registrazione presunta-interruzione, è necessario recuperare solo le transazioni che hanno raggiunto lo stato preparato in tutti gli errori di sistema.</span><span class="sxs-lookup"><span data-stu-id="be4e8-113">Only transactions that have reached the prepared state must be recovered across system failures if the transaction uses presumed-abort logging.</span></span>

2.  <span data-ttu-id="be4e8-114">Il client deve passare in modo esplicito una transazione a Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="be4e8-114">The client must pass a transaction to the resource manager explicitly.</span></span>
3.  <span data-ttu-id="be4e8-115">Il client esegue tutte le operazioni transazionali con uno o più RMs, ad esempio i file system transazionali.</span><span class="sxs-lookup"><span data-stu-id="be4e8-115">The client performs all its transactional operations with one or more RMs, such as transacted file systems.</span></span>
4.  <span data-ttu-id="be4e8-116">Il client chiama la funzione [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) .</span><span class="sxs-lookup"><span data-stu-id="be4e8-116">The client calls the [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) function.</span></span>
5.  <span data-ttu-id="be4e8-117">Resource Manager riceve le notifiche da KTM per preparare ed eseguire il commit dei dati.</span><span class="sxs-lookup"><span data-stu-id="be4e8-117">The resource manager receives notifications from KTM to prepare and commit its data.</span></span>

## <a name="transactions-and-threads"></a><span data-ttu-id="be4e8-118">Transazioni e thread</span><span class="sxs-lookup"><span data-stu-id="be4e8-118">Transactions and Threads</span></span>

<span data-ttu-id="be4e8-119">Le transazioni non corrispondono ai thread.</span><span class="sxs-lookup"><span data-stu-id="be4e8-119">Transactions are not the same as threads.</span></span> <span data-ttu-id="be4e8-120">Più thread o processi possono far parte di una singola transazione.</span><span class="sxs-lookup"><span data-stu-id="be4e8-120">Multiple threads or processes can be a part of a single transaction.</span></span> <span data-ttu-id="be4e8-121">Viceversa, un thread può essere parte di diverse transazioni in momenti diversi.</span><span class="sxs-lookup"><span data-stu-id="be4e8-121">Conversely, a thread can be a part of several different transactions at different times.</span></span>

## <a name="transaction-functions"></a><span data-ttu-id="be4e8-122">Funzioni di transazione</span><span class="sxs-lookup"><span data-stu-id="be4e8-122">Transaction Functions</span></span>

<span data-ttu-id="be4e8-123">Le funzioni seguenti vengono utilizzate con le transazioni.</span><span class="sxs-lookup"><span data-stu-id="be4e8-123">The following functions are used with transactions.</span></span>



| <span data-ttu-id="be4e8-124">Funzione</span><span class="sxs-lookup"><span data-stu-id="be4e8-124">Function</span></span>                                                            | <span data-ttu-id="be4e8-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be4e8-125">Description</span></span>                                                                                   |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be4e8-126">**CommitTransaction**</span><span class="sxs-lookup"><span data-stu-id="be4e8-126">**CommitTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | <span data-ttu-id="be4e8-127">Richiede che venga eseguito il commit della transazione specificata.</span><span class="sxs-lookup"><span data-stu-id="be4e8-127">Requests that the specified transaction be committed.</span></span>                                         |
| [<span data-ttu-id="be4e8-128">**CommitTransactionAsync**</span><span class="sxs-lookup"><span data-stu-id="be4e8-128">**CommitTransactionAsync**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | <span data-ttu-id="be4e8-129">Richiede che venga eseguito il commit della transazione specificata.</span><span class="sxs-lookup"><span data-stu-id="be4e8-129">Requests that the specified transaction be committed.</span></span>                                         |
| [<span data-ttu-id="be4e8-130">**CreateTransaction**</span><span class="sxs-lookup"><span data-stu-id="be4e8-130">**CreateTransaction**</span></span>](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | <span data-ttu-id="be4e8-131">Crea un nuovo oggetto transazione.</span><span class="sxs-lookup"><span data-stu-id="be4e8-131">Creates a new transaction object.</span></span>                                                             |
| [<span data-ttu-id="be4e8-132">**GetTransactionInformation**</span><span class="sxs-lookup"><span data-stu-id="be4e8-132">**GetTransactionInformation**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | <span data-ttu-id="be4e8-133">Restituisce le informazioni richieste sulla transazione specificata.</span><span class="sxs-lookup"><span data-stu-id="be4e8-133">Returns the requested information about the specified transaction.</span></span>                            |
| [<span data-ttu-id="be4e8-134">**OpenTransaction**</span><span class="sxs-lookup"><span data-stu-id="be4e8-134">**OpenTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | <span data-ttu-id="be4e8-135">Apre una transazione esistente.</span><span class="sxs-lookup"><span data-stu-id="be4e8-135">Opens an existing transaction.</span></span>                                                                |
| [<span data-ttu-id="be4e8-136">**RollbackTransaction**</span><span class="sxs-lookup"><span data-stu-id="be4e8-136">**RollbackTransaction**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | <span data-ttu-id="be4e8-137">Richiede che venga eseguito il rollback della transazione specificata.</span><span class="sxs-lookup"><span data-stu-id="be4e8-137">Requests that the specified transaction be rolled back.</span></span>                                       |
| [<span data-ttu-id="be4e8-138">**RollbackTransactionAsync**</span><span class="sxs-lookup"><span data-stu-id="be4e8-138">**RollbackTransactionAsync**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | <span data-ttu-id="be4e8-139">Richiede che venga eseguito il rollback della transazione specificata.</span><span class="sxs-lookup"><span data-stu-id="be4e8-139">Requests that the specified transaction be rolled back.</span></span> <span data-ttu-id="be4e8-140">Questa funzione restituisce in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="be4e8-140">This function returns asynchronously.</span></span> |
| [<span data-ttu-id="be4e8-141">**SetTransactionInformation**</span><span class="sxs-lookup"><span data-stu-id="be4e8-141">**SetTransactionInformation**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | <span data-ttu-id="be4e8-142">Imposta le informazioni sulla transazione per la transazione specificata.</span><span class="sxs-lookup"><span data-stu-id="be4e8-142">Sets the transaction information for the specified transaction.</span></span>                               |



 

 

 




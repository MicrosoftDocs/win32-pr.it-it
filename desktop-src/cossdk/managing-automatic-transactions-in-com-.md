---
description: Nel modello di programmazione COM+ è possibile progettare i componenti in modo da eseguire le operazioni migliori&\# 8212, abilitando la logica di business o stabilendo una connessione di database&\# 8212; e basandosi sul Framework di elaborazione delle transazioni di Microsoft Windows per automatizzare le transazioni.
ms.assetid: 50086e6e-024b-4a09-b8be-8f55b6bfadb2
title: Gestione delle transazioni automatiche in COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371730173acd4943f460afbf2feab7ada83078fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524057"
---
# <a name="managing-automatic-transactions-in-com"></a><span data-ttu-id="6d684-103">Gestione delle transazioni automatiche in COM+</span><span class="sxs-lookup"><span data-stu-id="6d684-103">Managing Automatic Transactions in COM+</span></span>

<span data-ttu-id="6d684-104">Nel modello di programmazione COM+ è possibile progettare i componenti per eseguire le operazioni migliori, ovvero abilitare la logica di business o stabilire una connessione al database, e basarsi sul Framework di elaborazione delle transazioni di Microsoft Windows per automatizzare le transazioni.</span><span class="sxs-lookup"><span data-stu-id="6d684-104">In the COM+ programming model, you can design your components to do what they do best—enabling business logic or establishing a database connection—and rely on the transaction processing framework of Microsoft Windows to automate transactions.</span></span>

## <a name="starting-a-transaction"></a><span data-ttu-id="6d684-105">Avvio di una transazione</span><span class="sxs-lookup"><span data-stu-id="6d684-105">Starting a Transaction</span></span>

<span data-ttu-id="6d684-106">COM+ avvia automaticamente una transazione quando si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6d684-106">COM+ automatically begins a transaction when it encounters either of the following conditions:</span></span>

-   <span data-ttu-id="6d684-107">Quando un client non transazionale chiama un componente che richiede una transazione o richiede una nuova transazione.</span><span class="sxs-lookup"><span data-stu-id="6d684-107">When a non-transactional client calls a component that requires a transaction or requires a new transaction.</span></span>
-   <span data-ttu-id="6d684-108">Quando un client transazionale chiama un componente che richiede una nuova transazione.</span><span class="sxs-lookup"><span data-stu-id="6d684-108">When a transactional client calls a component that requires a new transaction.</span></span>

<span data-ttu-id="6d684-109">Se COM+ determina che un oggetto deve disporre di una nuova transazione, avvia prima la transazione e quindi inserisce l'oggetto al suo interno.</span><span class="sxs-lookup"><span data-stu-id="6d684-109">If COM+ determines that an object should have a new transaction, it begins the transaction first and then places the object in it.</span></span> <span data-ttu-id="6d684-110">Il processo include i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6d684-110">The process includes the following steps:</span></span>

1.  <span data-ttu-id="6d684-111">COM+ crea un oggetto context, imposta gli attributi di [attivazione](com--just-in-time-activation.md) e [sincronizzazione](com--synchronization.md) JIT su Required e imposta rispettivamente i [flag coerenti e done](consistent-and-done-flags.md) su true e false.</span><span class="sxs-lookup"><span data-stu-id="6d684-111">COM+ creates a context object, sets both the [JIT activation](com--just-in-time-activation.md) and [Synchronization](com--synchronization.md) attributes to Required, and sets the [consistent and done flags](consistent-and-done-flags.md) to True and False, respectively.</span></span>
2.  <span data-ttu-id="6d684-112">COM+ comunica con il Distributed Transaction Coordinator (DTC) per avviare una transazione.</span><span class="sxs-lookup"><span data-stu-id="6d684-112">COM+ communicates with the Distributed Transaction Coordinator (DTC) to begin a transaction.</span></span> <span data-ttu-id="6d684-113">Il DTC coordina la transazione fisica.</span><span class="sxs-lookup"><span data-stu-id="6d684-113">The DTC coordinates the physical transaction.</span></span>
3.  <span data-ttu-id="6d684-114">Il DTC genera un identificatore di transazione e lo passa nuovamente a COM+.</span><span class="sxs-lookup"><span data-stu-id="6d684-114">The DTC generates a transaction identifier and passes it back to COM+.</span></span> <span data-ttu-id="6d684-115">L'identificatore di transazione stabilisce un limite della transazione.</span><span class="sxs-lookup"><span data-stu-id="6d684-115">The transaction identifier establishes a transaction boundary.</span></span> <span data-ttu-id="6d684-116">Tutti gli oggetti che partecipano alla transazione condividono lo stesso identificatore.</span><span class="sxs-lookup"><span data-stu-id="6d684-116">All objects participating in the transaction share the same identifier.</span></span>
4.  <span data-ttu-id="6d684-117">Quando il client crea l'oggetto, COM+ lo attiva all'interno del limite della transazione.</span><span class="sxs-lookup"><span data-stu-id="6d684-117">When the client creates the object, COM+ activates it within the transaction boundary.</span></span>

## <a name="ending-a-transaction"></a><span data-ttu-id="6d684-118">Fine di una transazione</span><span class="sxs-lookup"><span data-stu-id="6d684-118">Ending a Transaction</span></span>

<span data-ttu-id="6d684-119">COM+ termina una transazione automatica eseguendone il commit o l'interruzione quando si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6d684-119">COM+ ends an automatic transaction by committing or aborting it when one of the following conditions occurs:</span></span>

-   <span data-ttu-id="6d684-120">L'oggetto radice della transazione ne completa il lavoro e COM+ lo rilascia.</span><span class="sxs-lookup"><span data-stu-id="6d684-120">The root object of the transaction completes its work and COM+ releases it.</span></span> <span data-ttu-id="6d684-121">Dopo la disattivazione dell'oggetto radice, la transazione tenta di eseguire il commit.</span><span class="sxs-lookup"><span data-stu-id="6d684-121">After the root object deactivates, the transaction attempts to commit.</span></span>
-   <span data-ttu-id="6d684-122">Il client rilascia l'oggetto radice.</span><span class="sxs-lookup"><span data-stu-id="6d684-122">The client releases the root object.</span></span> <span data-ttu-id="6d684-123">Senza un riferimento, l'oggetto radice viene disattivato e la transazione tenta di eseguire il commit.</span><span class="sxs-lookup"><span data-stu-id="6d684-123">Without a reference, the root object deactivates and the transaction attempts to commit.</span></span>
-   <span data-ttu-id="6d684-124">La transazione supera la soglia di timeout.</span><span class="sxs-lookup"><span data-stu-id="6d684-124">The transaction exceeds its time-out threshold.</span></span> <span data-ttu-id="6d684-125">La transazione viene interrotta automaticamente se non viene eseguito il commit entro il periodo di timeout della transazione, disattivando tutti gli oggetti associati alla transazione.</span><span class="sxs-lookup"><span data-stu-id="6d684-125">The transaction aborts automatically if not committed within the transaction time-out period, deactivating all objects associated with the transaction.</span></span> <span data-ttu-id="6d684-126">Il periodo di timeout predefinito per la transazione è di 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="6d684-126">The default transaction time-out period is 60 seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d684-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6d684-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d684-128">Flag coerenti e done</span><span class="sxs-lookup"><span data-stu-id="6d684-128">Consistent and Done Flags</span></span>](consistent-and-done-flags.md)
</dt> <dt>

[<span data-ttu-id="6d684-129">Velocizzare le transazioni inviando una notifica all'oggetto radice</span><span class="sxs-lookup"><span data-stu-id="6d684-129">Speeding Transactions by Notifying the Root Object</span></span>](speeding-transactions-by-notifying-the-root-object.md)
</dt> <dt>

[<span data-ttu-id="6d684-130">Terminazione di una transazione automatica mediante una chiamata a Tocomplete</span><span class="sxs-lookup"><span data-stu-id="6d684-130">Terminating an Automatic Transaction by Calling SetComplete</span></span>](terminating-an-automatic-transaction-by-calling-setcomplete.md)
</dt> </dl>

 

 




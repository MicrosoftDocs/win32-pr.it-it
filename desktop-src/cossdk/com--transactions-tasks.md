---
description: Attività delle transazioni COM+
ms.assetid: fe4374f1-2452-4316-be57-b866c438404d
title: Attività delle transazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70aaebd3e788e1ff12e86b7831979f055367fea7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127154"
---
# <a name="com-transactions-tasks"></a><span data-ttu-id="9686a-103">Attività delle transazioni COM+</span><span class="sxs-lookup"><span data-stu-id="9686a-103">COM+ Transactions Tasks</span></span>

<span data-ttu-id="9686a-104">Mentre l'elaborazione automatica delle transazioni in COM+ consente di impiegare un tempo di sviluppo più produttivo per la creazione e la configurazione di oggetti che si desidera includere nelle transazioni automatiche, è possibile eseguire alcune attività di programmazione per adattare il comportamento delle transazioni ai requisiti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9686a-104">While automatic transaction processing in COM+ allows you to spend more productive development time in creating and configuring objects that you want to participate in automatic transactions, there are some programming tasks you can perform to tailor transaction behavior to your application requirements.</span></span>

<span data-ttu-id="9686a-105">Negli argomenti seguenti vengono illustrate le opzioni di programmazione specifiche relative all'elaborazione delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="9686a-105">The following topics discuss specific programming options related to transaction processing.</span></span>



| <span data-ttu-id="9686a-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="9686a-106">Topic</span></span>                                                                                             | <span data-ttu-id="9686a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9686a-107">Description</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9686a-108">Impostazione dell'attributo Transaction</span><span class="sxs-lookup"><span data-stu-id="9686a-108">Setting the Transaction Attribute</span></span>](setting-the-transaction-attribute.md)<br/>             | <span data-ttu-id="9686a-109">Viene descritto come impostare i valori degli attributi di transazione per gli oggetti della transazione.</span><span class="sxs-lookup"><span data-stu-id="9686a-109">Describes how to set transaction attribute values for your transaction objects.</span></span><br/>         |
| [<span data-ttu-id="9686a-110">Impostazione del livello di isolamento delle transazioni</span><span class="sxs-lookup"><span data-stu-id="9686a-110">Setting the Transaction Isolation Level</span></span>](setting-the-transaction-isolation-level.md)<br/> | <span data-ttu-id="9686a-111">Viene descritto come impostare i livelli di isolamento delle transazioni per gli oggetti della transazione.</span><span class="sxs-lookup"><span data-stu-id="9686a-111">Describes how to set the transaction isolation levels for your transaction objects.</span></span><br/>     |
| [<span data-ttu-id="9686a-112">Impostazione del timeout della transazione</span><span class="sxs-lookup"><span data-stu-id="9686a-112">Setting the Transaction Time-Out</span></span>](setting-the-transaction-time-out.md)<br/>               | <span data-ttu-id="9686a-113">Viene descritto come impostare gli intervalli di timeout per le transazioni.</span><span class="sxs-lookup"><span data-stu-id="9686a-113">Describes how to set time-out intervals for your transactions.</span></span><br/>                          |
| [<span data-ttu-id="9686a-114">Impostazione dei flag coerenti e done</span><span class="sxs-lookup"><span data-stu-id="9686a-114">Setting the Consistent and Done Flags</span></span>](setting-the-consistent-and-done-flags.md)<br/>     | <span data-ttu-id="9686a-115">Viene illustrato come utilizzare i flag coerenti e done per controllare il risultato di una transazione.</span><span class="sxs-lookup"><span data-stu-id="9686a-115">Shows how to use the consistent and done flags to control the outcome of a transaction.</span></span><br/> |
| [<span data-ttu-id="9686a-116">Creazione di oggetti BYOT</span><span class="sxs-lookup"><span data-stu-id="9686a-116">Creating BYOT Objects</span></span>](creating-byot-objects.md)<br/>                                     | <span data-ttu-id="9686a-117">Viene descritto come creare oggetti in modo che sia possibile eseguire una transazione personalizzata (BYOT).</span><span class="sxs-lookup"><span data-stu-id="9686a-117">Describes how to create objects so you can Bring Your Own Transaction (BYOT).</span></span><br/>           |



 

> [!Note]  
> <span data-ttu-id="9686a-118">Come regola generale, qualsiasi componente che aggiorna lo stato persistente deve supportare le transazioni.</span><span class="sxs-lookup"><span data-stu-id="9686a-118">As a general rule, any component that updates persistent state should support transactions.</span></span> <span data-ttu-id="9686a-119">I componenti che combinano le operazioni di due o più oggetti in una singola attività devono utilizzare le transazioni per semplificare il ripristino degli errori.</span><span class="sxs-lookup"><span data-stu-id="9686a-119">Components that combine the operations of two or more objects into a single task should use transactions to simplify error recovery.</span></span> <span data-ttu-id="9686a-120">Inoltre, per rilasciare le risorse, ad esempio le connessioni al database, le transazioni in COM+ dovrebbero essere le più brevi possibile.</span><span class="sxs-lookup"><span data-stu-id="9686a-120">Also, to release resources, such as database connections, transactions in COM+ should be as short as you can make them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9686a-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9686a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9686a-122">Concetti sulle transazioni COM+</span><span class="sxs-lookup"><span data-stu-id="9686a-122">COM+ Transactions Concepts</span></span>](com--transactions-concepts.md)
</dt> </dl>

 

 





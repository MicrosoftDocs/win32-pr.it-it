---
description: Transazioni COM+
ms.assetid: 40eccce1-a362-4adc-8060-f6923b9162c9
title: Transazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef51f4c8ed5e37101f64d36af385c93ac7e69ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401465"
---
# <a name="com-transactions"></a><span data-ttu-id="2c42d-103">Transazioni COM+</span><span class="sxs-lookup"><span data-stu-id="2c42d-103">COM+ Transactions</span></span>

<span data-ttu-id="2c42d-104">Quando si acquista un libro da una libreria online, si usa una carta di credito per scambiare denaro per un libro.</span><span class="sxs-lookup"><span data-stu-id="2c42d-104">When you purchase a book from an online bookstore, you use a credit card to trade money for a book.</span></span> <span data-ttu-id="2c42d-105">Una volta inviato l'ordine, una serie di operazioni correlate (convalida della carta di credito, verifica della disponibilità dell'inventario e così via) garantisce la disponibilità del libro e l'ottenimento del denaro da parte della libreria.</span><span class="sxs-lookup"><span data-stu-id="2c42d-105">After you submit your order, a series of related operations (validation of your credit card, verification of inventory availability, and so forth) ensures that you get the book and that the bookstore gets your money.</span></span> <span data-ttu-id="2c42d-106">Se una singola operazione della serie ha esito negativo durante lo scambio, l'intero scambio avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2c42d-106">If a single operation in the series fails during the exchange, the entire exchange fails.</span></span> <span data-ttu-id="2c42d-107">Non è possibile ottenere il libro e la libreria non ottiene il denaro.</span><span class="sxs-lookup"><span data-stu-id="2c42d-107">You do not get the book, and the bookstore does not get your money.</span></span>

<span data-ttu-id="2c42d-108">La tecnologia responsabile dell'esecuzione di questo scambio online bilanciato e prevedibile è detta *elaborazione delle transazioni*.</span><span class="sxs-lookup"><span data-stu-id="2c42d-108">The technology responsible for making this online exchange balanced and predictable is called *transaction processing*.</span></span> <span data-ttu-id="2c42d-109">A livello di codice, una *transazione* è un'unità di lavoro in cui si verifica una serie di operazioni.</span><span class="sxs-lookup"><span data-stu-id="2c42d-109">Programmatically, a *transaction* is a unit of work in which a series of operations occur.</span></span> <span data-ttu-id="2c42d-110">COM+ utilizza transazioni programmatiche per garantire che le risorse non vengano aggiornate in modo permanente, a meno che tutte le operazioni all'interno della transazione non vengano completate.</span><span class="sxs-lookup"><span data-stu-id="2c42d-110">COM+ uses programmatic transactions to ensure that resources are not permanently updated unless all operations within the transaction complete successfully.</span></span> <span data-ttu-id="2c42d-111">Associando insieme un set di operazioni correlate in una transazione COM+ che ha esito positivo o negativo completamente, è possibile semplificare notevolmente il ripristino degli errori.</span><span class="sxs-lookup"><span data-stu-id="2c42d-111">By binding a set of related operations together in a COM+ transaction that either completely succeeds or completely fails, you can vastly simplify error recovery.</span></span>

<span data-ttu-id="2c42d-112">Negli argomenti seguenti viene introdotta la teoria generale dell'elaborazione delle transazioni, vengono fornite informazioni dettagliate sulle transazioni in COM+ e vengono presentati suggerimenti pratici per la scrittura di componenti transazionali.</span><span class="sxs-lookup"><span data-stu-id="2c42d-112">The following topics introduce general transaction processing theory, provide a closer look at transactions in COM+, and present practical tips for writing transactional components.</span></span>



| <span data-ttu-id="2c42d-113">Argomento</span><span class="sxs-lookup"><span data-stu-id="2c42d-113">Topic</span></span>                                                                   | <span data-ttu-id="2c42d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c42d-114">Description</span></span>                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="2c42d-115">Concetti sulle transazioni COM+</span><span class="sxs-lookup"><span data-stu-id="2c42d-115">COM+ Transactions Concepts</span></span>](com--transactions-concepts.md)<br/> | <span data-ttu-id="2c42d-116">Vengono presentati termini e concetti di base.</span><span class="sxs-lookup"><span data-stu-id="2c42d-116">Presents basic terms and concepts.</span></span><br/>                                  |
| [<span data-ttu-id="2c42d-117">Attività delle transazioni COM+</span><span class="sxs-lookup"><span data-stu-id="2c42d-117">COM+ Transactions Tasks</span></span>](com--transactions-tasks.md)<br/>       | <span data-ttu-id="2c42d-118">Vengono fornite informazioni pratiche sulla scrittura di componenti transazionali.</span><span class="sxs-lookup"><span data-stu-id="2c42d-118">Provides practical information on writing transactional components.</span></span><br/> |



 

 

 





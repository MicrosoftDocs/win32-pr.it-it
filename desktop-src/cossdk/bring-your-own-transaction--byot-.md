---
description: Bring Your Own Transaction (BYOT)
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: Bring Your Own Transaction (BYOT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ca6f7f12babbf3ad183c4695a68591d9e181a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305019"
---
# <a name="bring-your-own-transaction-byot"></a><span data-ttu-id="a2c85-103">Bring Your Own Transaction (BYOT)</span><span class="sxs-lookup"><span data-stu-id="a2c85-103">Bring Your Own Transaction (BYOT)</span></span>

<span data-ttu-id="a2c85-104">BYOT consente la creazione di un componente con o per ereditare una transazione esterna.</span><span class="sxs-lookup"><span data-stu-id="a2c85-104">BYOT allows a component to be created with or to inherit an external transaction.</span></span> <span data-ttu-id="a2c85-105">Ovvero, un componente che non dispone già di una transazione associata può acquisire una transazione.</span><span class="sxs-lookup"><span data-stu-id="a2c85-105">That is, a component that does not already have an associated transaction can acquire a transaction.</span></span> <span data-ttu-id="a2c85-106">Attualmente, le transazioni MTS sono automatiche; la presenza di un'istanza del componente in una transazione viene determinata al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="a2c85-106">Currently, MTS transactions are automatic; whether a component instance lives in a transaction is determined at creation time.</span></span> <span data-ttu-id="a2c85-107">Gli attributi transazionali di un componente e il relativo autore determinano la transazione associata a una determinata istanza.</span><span class="sxs-lookup"><span data-stu-id="a2c85-107">The transactional attributes of a component and its creator determine what transaction is associated with a given instance.</span></span> <span data-ttu-id="a2c85-108">In tutti i casi, MTS controlla la durata delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="a2c85-108">In all cases, MTS controls transaction lifetimes.</span></span> <span data-ttu-id="a2c85-109">COM+ estende questo per consentire l'impostazione di una transazione DTC o TIP preesistente arbitraria come proprietà di transazione del contesto di un nuovo componente.</span><span class="sxs-lookup"><span data-stu-id="a2c85-109">COM+ extends this to allow setting an arbitrary pre-existing DTC or TIP transaction as the transaction property of a new component's context.</span></span> <span data-ttu-id="a2c85-110">Ciò consente di associare i componenti configurati alle transazioni la cui durata è controllata da un monitor TP, un OTS o un sistema DBMS.</span><span class="sxs-lookup"><span data-stu-id="a2c85-110">This allows configured components to be associated with transactions whose lifetimes are controlled by a TP monitor, OTS, or DBMS.</span></span>

> [!Note]  
> <span data-ttu-id="a2c85-111">È necessario usare le transazioni BYOT con cautela.</span><span class="sxs-lookup"><span data-stu-id="a2c85-111">BYOT transactions must be used with caution.</span></span> <span data-ttu-id="a2c85-112">In alcune situazioni, possono causare una transazione che si estende su più domini di sincronizzazione, ovvero consentono il parallelismo con una transazione, causando una condizione di deadlock.</span><span class="sxs-lookup"><span data-stu-id="a2c85-112">In certain situations, they can result in a transaction spanning multiple synchronization domains—that is, they allow parallelism with a transaction, causing a deadlock condition.</span></span> <span data-ttu-id="a2c85-113">Le transazioni automatiche, anziché le transazioni BYOT, rappresentano il modello di programmazione preferito per i writer di componenti aziendali.</span><span class="sxs-lookup"><span data-stu-id="a2c85-113">Automatic transactions, rather than BYOT transactions, are the preferred programming model for writers of business components.</span></span>

 

<span data-ttu-id="a2c85-114">Le interfacce per le transazioni BYOT includono l'interfaccia [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) e l'interfaccia [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) .</span><span class="sxs-lookup"><span data-stu-id="a2c85-114">The interfaces for BYOT transactions include the [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) interface and the [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) interface.</span></span> <span data-ttu-id="a2c85-115">L'interfaccia **ICreateWithTransactionEx** crea un oggetto che è integrato in una transazione manuale.</span><span class="sxs-lookup"><span data-stu-id="a2c85-115">The **ICreateWithTransactionEx** interface creates an object that is enlisted within a manual transaction.</span></span> <span data-ttu-id="a2c85-116">L'interfaccia **ICreateWithTipTransactionEx** crea un oggetto che è integrato in una transazione manuale utilizzando il protocollo di transazione Internet (tip).</span><span class="sxs-lookup"><span data-stu-id="a2c85-116">The **ICreateWithTipTransactionEx** interface creates an object that is enlisted within a manual transaction using the Transaction Internet Protocol (TIP).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2c85-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a2c85-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2c85-118">Eredità di transazioni manuali</span><span class="sxs-lookup"><span data-stu-id="a2c85-118">Inheriting Manual Transactions</span></span>](inheriting-manual-transactions.md)
</dt> </dl>

 

 




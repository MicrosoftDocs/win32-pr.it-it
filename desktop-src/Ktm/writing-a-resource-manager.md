---
description: Se si sta scrivendo un servizio o un componente ed è necessario usare i servizi transazionali o se è necessario monitorare lo stato di una transazione kernel, è necessario creare un gestore di risorse (RM).
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: Scrittura di un Gestione risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c47f9a0704f6edaea02d752fe39f01fce61c0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311125"
---
# <a name="writing-a-resource-manager"></a><span data-ttu-id="cf83b-103">Scrittura di un Gestione risorse</span><span class="sxs-lookup"><span data-stu-id="cf83b-103">Writing a Resource Manager</span></span>

<span data-ttu-id="cf83b-104">Se si sta scrivendo un servizio o un componente ed è necessario usare i servizi transazionali o se è necessario monitorare lo stato di una transazione kernel, è necessario creare un gestore di risorse (RM).</span><span class="sxs-lookup"><span data-stu-id="cf83b-104">If you are writing a service or component and need to use transactional services or if you need to monitor the state of a kernel transaction, you need to create a resource manager (RM).</span></span>

<span data-ttu-id="cf83b-105">Per scrivere un gestore di risorse, è necessario creare più oggetti kernel.</span><span class="sxs-lookup"><span data-stu-id="cf83b-105">To write a resource manager, you must create multiple kernel objects.</span></span> <span data-ttu-id="cf83b-106">Gli oggetti utilizzati da un RM sono:</span><span class="sxs-lookup"><span data-stu-id="cf83b-106">The objects that an RM uses are:</span></span>

-   <span data-ttu-id="cf83b-107">Oggetti di gestione transazioni (TM)</span><span class="sxs-lookup"><span data-stu-id="cf83b-107">Transaction Manager (TM) objects</span></span>
-   <span data-ttu-id="cf83b-108">Oggetti Gestione risorse</span><span class="sxs-lookup"><span data-stu-id="cf83b-108">Resource Manager objects</span></span>
-   <span data-ttu-id="cf83b-109">Oggetti di integrazione</span><span class="sxs-lookup"><span data-stu-id="cf83b-109">Enlistment objects</span></span>

<span data-ttu-id="cf83b-110">Per prima cosa, creare un oggetto TM.</span><span class="sxs-lookup"><span data-stu-id="cf83b-110">First, create a TM object.</span></span> <span data-ttu-id="cf83b-111">Esistono due tipi di TMs:</span><span class="sxs-lookup"><span data-stu-id="cf83b-111">There are two types of TMs:</span></span>

-   <span data-ttu-id="cf83b-112">Volatile: le TMs non dispongono di un log e non possono recuperare il proprio stato</span><span class="sxs-lookup"><span data-stu-id="cf83b-112">Volatile – these TMs do not have a log and cannot recover their state</span></span>
-   <span data-ttu-id="cf83b-113">Durevole: le TM hanno un log</span><span class="sxs-lookup"><span data-stu-id="cf83b-113">Durable – these TMs have a log</span></span>

<span data-ttu-id="cf83b-114">Per creare una TM durevole, è necessario creare un log CLFS e chiamare [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) o fare in modo che KTM lo crei per l'utente.</span><span class="sxs-lookup"><span data-stu-id="cf83b-114">To create a durable TM, you must either create a CLFS log and call [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) or have KTM create it for you.</span></span> <span data-ttu-id="cf83b-115">Dopo la creazione di una TM durevole, è necessario innanzitutto ripristinare la TM chiamando [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager).</span><span class="sxs-lookup"><span data-stu-id="cf83b-115">After a durable TM is created, you must first recover the TM by calling [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager).</span></span> <span data-ttu-id="cf83b-116">Una volta recuperato, il TM sarà disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="cf83b-116">After the TM is recovered, it is available for use.</span></span>

<span data-ttu-id="cf83b-117">Se è stata ripristinata una TM esistente, tutte le RMs associate a questa TM inizieranno a ricevere i messaggi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="cf83b-117">If you recovered an existing TM, all RMs associated with this TM will start receiving recovery messages.</span></span> <span data-ttu-id="cf83b-118">Per ulteriori informazioni, vedere [elaborazione del ripristino](recovery-processing.md).</span><span class="sxs-lookup"><span data-stu-id="cf83b-118">For more information, see [Recovery Processing](recovery-processing.md).</span></span>

<span data-ttu-id="cf83b-119">Successivamente, creare un gestore di risorse chiamando [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) con l'handle TM.</span><span class="sxs-lookup"><span data-stu-id="cf83b-119">Next, you create a resource manager by calling [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) with the TM handle.</span></span> <span data-ttu-id="cf83b-120">Il RM può essere volatile o durevole.</span><span class="sxs-lookup"><span data-stu-id="cf83b-120">The RM can be volatile or durable.</span></span> <span data-ttu-id="cf83b-121">Con RMs durevole è possibile usare solo TMs durevoli.</span><span class="sxs-lookup"><span data-stu-id="cf83b-121">Only durable TMs can be used with durable RMs.</span></span>

<span data-ttu-id="cf83b-122">Quando si lavora in modo transazionale, si integra la transazione chiamando [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)e specificando quali notifiche ricevere.</span><span class="sxs-lookup"><span data-stu-id="cf83b-122">When working transactionally, you enlist in the transaction by calling [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)and specifying which notifications to receive.</span></span>

<span data-ttu-id="cf83b-123">**Nota**  È possibile iniziare a ricevere le notifiche prima del completamento della chiamata a [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) .</span><span class="sxs-lookup"><span data-stu-id="cf83b-123">**Note**  You can start receiving notifications before the call to [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) is completed.</span></span>

<span data-ttu-id="cf83b-124">Quando si riceve una notifica, chiamare la funzione "completa \* " appropriata quando viene completata qualsiasi lavoro associato all'elaborazione della notifica.</span><span class="sxs-lookup"><span data-stu-id="cf83b-124">When you receive a notification, call the appropriate "Complete\*" function when any work associated with processing the notification is completed.</span></span> <span data-ttu-id="cf83b-125">Le funzioni complete sono:</span><span class="sxs-lookup"><span data-stu-id="cf83b-125">The complete functions are:</span></span>

-   [<span data-ttu-id="cf83b-126">**CommitComplete**</span><span class="sxs-lookup"><span data-stu-id="cf83b-126">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [<span data-ttu-id="cf83b-127">**PrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="cf83b-127">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [<span data-ttu-id="cf83b-128">**PreprepareComplete**</span><span class="sxs-lookup"><span data-stu-id="cf83b-128">**PreprepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

<span data-ttu-id="cf83b-129">Se in qualsiasi momento un gestore di risorse non è in grado di completare il lavoro della transazione o se continuare, il rendering dell'applicazione non è in grado di annullare le operazioni eseguite all'interno della transazione, è necessario eseguire il rollback della transazione chiamando [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).</span><span class="sxs-lookup"><span data-stu-id="cf83b-129">If at any time a resource manager is unable to complete the work of the transaction, or if continuing would render your application unable to undo the work done within the transaction, you must roll back the transaction by calling [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).</span></span>

 

 




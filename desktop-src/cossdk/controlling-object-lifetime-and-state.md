---
description: Controllo della durata e dello stato degli oggetti
ms.assetid: 172e07a2-1711-4353-9099-ff9d31a564c6
title: Controllo della durata e dello stato degli oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cc1d582d85bc84ef2b1749a427711d1fe26fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305013"
---
# <a name="controlling-object-lifetime-and-state"></a><span data-ttu-id="e01b3-103">Controllo della durata e dello stato degli oggetti</span><span class="sxs-lookup"><span data-stu-id="e01b3-103">Controlling Object Lifetime and State</span></span>

<span data-ttu-id="e01b3-104">Un oggetto in pool può partecipare al modo in cui COM+ gestisce l'attività nel pool implementando [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span><span class="sxs-lookup"><span data-stu-id="e01b3-104">A pooled object can participate in how COM+ manages its activity in the pool by implementing [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol).</span></span> <span data-ttu-id="e01b3-105">Quando viene creato un oggetto in pool, questo viene aggregato in un oggetto più grande che gestirà l'oggetto chiamando i metodi seguenti su **IObjectControl** nei punti regolari del ciclo di vita dell'oggetto:</span><span class="sxs-lookup"><span data-stu-id="e01b3-105">When a pooled object is created, it is aggregated into a larger object that will manage the object by calling the following methods on **IObjectControl** at regular points in the object's lifecycle:</span></span>

-   <span data-ttu-id="e01b3-106">[**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate): viene chiamato ogni volta che l'oggetto viene restituito a un client, attivato in un contesto specifico.</span><span class="sxs-lookup"><span data-stu-id="e01b3-106">[**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)—Called whenever the object is returned to a client, activated in a specific context.</span></span>
-   <span data-ttu-id="e01b3-107">[**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate): viene chiamato ogni volta che un oggetto viene rilasciato dal client o, nel caso di un oggetto attivato da JIT, quando viene disattivato.</span><span class="sxs-lookup"><span data-stu-id="e01b3-107">[**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)—Called whenever an object is released by the client or, in the case of a JIT-activated object, when it is deactivated.</span></span>
-   <span data-ttu-id="e01b3-108">[**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled): viene chiamato ogni volta che un oggetto deve essere restituito al pool generale.</span><span class="sxs-lookup"><span data-stu-id="e01b3-108">[**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)—Called whenever an object is to be returned to the general pool.</span></span>

<span data-ttu-id="e01b3-109">L'implementazione di [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) è facoltativa, ad eccezione degli oggetti transazionali, che devono sempre implementare [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) per monitorare lo stato delle risorse che contengono.</span><span class="sxs-lookup"><span data-stu-id="e01b3-109">Implementing [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) is optional, except for transactional objects, which should always implement [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) to monitor the state of the resources they hold.</span></span> <span data-ttu-id="e01b3-110">Tuttavia, è consigliabile implementare **IObjectControl** nella maggior parte dei casi perché fornisce un modo efficiente per gestire il comportamento di un oggetto in pool, come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="e01b3-110">However, it is advisable to implement **IObjectControl** in most cases because it provides an efficient way to manage the behavior of a pooled object, as described below.</span></span>

## <a name="performing-context-specific-initialization"></a><span data-ttu-id="e01b3-111">Esecuzione dell'inizializzazione Context-Specific</span><span class="sxs-lookup"><span data-stu-id="e01b3-111">Performing Context-Specific Initialization</span></span>

<span data-ttu-id="e01b3-112">Utilizzando [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate), è possibile inizializzare l'oggetto nel contesto in cui viene attivato per un determinato client.</span><span class="sxs-lookup"><span data-stu-id="e01b3-112">Using [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate), you can initialize the object in the context in which it is activated for a given client.</span></span> <span data-ttu-id="e01b3-113">Per determinare, ad esempio, se l'oggetto ha affinità di transazione (le relative risorse potrebbero essere già integrate), è possibile ottenere l'ID di transazione associato al contesto.</span><span class="sxs-lookup"><span data-stu-id="e01b3-113">For example, to determine whether the object has transaction affinity (its resources may already be enlisted), you might get the transaction ID associated with the context.</span></span>

<span data-ttu-id="e01b3-114">In genere si usa [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)per eseguire l'inizializzazione coerente in tutti i metodi esposti dall'oggetto, considerandola come parte specifica del contesto del costruttore dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e01b3-114">Typically you would use [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)to perform initialization that is consistent across any methods exposed by the object, treating it as the context-specific portion of the object's constructor.</span></span>

## <a name="cleaning-up-any-client-state"></a><span data-ttu-id="e01b3-115">Pulizia di qualsiasi stato del client</span><span class="sxs-lookup"><span data-stu-id="e01b3-115">Cleaning Up Any Client State</span></span>

<span data-ttu-id="e01b3-116">Utilizzando [**Disattiva**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), è possibile eliminare qualsiasi stato specifico del client che potrebbe esistere in modo che l'oggetto torni al pool in uno stato completamente generico e possa quindi essere utilizzato da qualsiasi client senza compromettere la sicurezza o l'isolamento.</span><span class="sxs-lookup"><span data-stu-id="e01b3-116">Using [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), you can get rid of any client-specific state that might exist so that your object returns to the pool in a completely generic state and can then be used by any client without compromising security or isolation.</span></span>

## <a name="controlling-reuse-of-the-object"></a><span data-ttu-id="e01b3-117">Controllo del riutilizzo dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="e01b3-117">Controlling Reuse of the Object</span></span>

<span data-ttu-id="e01b3-118">Utilizzando [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), è possibile monitorare lo stato interno dell'oggetto e segnalare se è adatto per il riutilizzo.</span><span class="sxs-lookup"><span data-stu-id="e01b3-118">Using [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), you can monitor the internal state of your object and report on whether it is fit for its reuse.</span></span> <span data-ttu-id="e01b3-119">Se **CanBePooled** restituisce true e non è stato raggiunto il numero massimo di pool, l'oggetto viene inserito nuovamente nel pool generale.</span><span class="sxs-lookup"><span data-stu-id="e01b3-119">If **CanBePooled** returns True and the pool maximum has not been reached, the object is placed back in the general pool.</span></span> <span data-ttu-id="e01b3-120">Se **CanBePooled** restituisce false, l'oggetto viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="e01b3-120">If **CanBePooled** returns False, the object is discarded.</span></span> <span data-ttu-id="e01b3-121">Nel caso di componenti transazionali, la restituzione di false causerà la distruzione della transazione corrente.</span><span class="sxs-lookup"><span data-stu-id="e01b3-121">In the case of transactional components, returning False will doom the current transaction.</span></span>

<span data-ttu-id="e01b3-122">In genere, si conservano alcuni membri dati globali per l'oggetto e se si rileva una connessione non valida o una risorsa di qualche tipo è in uno stato non valido, impostare questo valore in modo che corrisponda alla situazione corrente e restituirlo tramite [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span><span class="sxs-lookup"><span data-stu-id="e01b3-122">Typically, you would keep some global data member for the object, and if you detect a connection to be bad or a resource of some kind to be in a bad state, set this to reflect the current situation and return it through [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span>

<span data-ttu-id="e01b3-123">Se un oggetto non implementa [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), le istanze continueranno a essere riutilizzate fino a quando non viene raggiunto il livello massimo del pool.</span><span class="sxs-lookup"><span data-stu-id="e01b3-123">If an object does not implement [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), instances will continue to be reused until the pool maximum level is reached.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e01b3-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e01b3-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e01b3-125">Stringhe del costruttore di oggetti COM+</span><span class="sxs-lookup"><span data-stu-id="e01b3-125">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="e01b3-126">Funzionamento del pool di oggetti</span><span class="sxs-lookup"><span data-stu-id="e01b3-126">How Object Pooling Works</span></span>](how-object-pooling-works.md)
</dt> <dt>

[<span data-ttu-id="e01b3-127">Miglioramento delle prestazioni con il pool di oggetti</span><span class="sxs-lookup"><span data-stu-id="e01b3-127">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="e01b3-128">Raggruppamento di oggetti transazionali</span><span class="sxs-lookup"><span data-stu-id="e01b3-128">Pooling Transactional Objects</span></span>](pooling-transactional-objects.md)
</dt> <dt>

[<span data-ttu-id="e01b3-129">Requisiti per gli oggetti pool</span><span class="sxs-lookup"><span data-stu-id="e01b3-129">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 




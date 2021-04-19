---
description: I componenti transazionali che devono essere raggruppati hanno requisiti particolari.
ms.assetid: 32e2f830-c30a-4dbc-8e69-dd2038851998
title: Raggruppamento di oggetti transazionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 006ba32ad2ac550be4fa4418dde322ded26c64c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304945"
---
# <a name="pooling-transactional-objects"></a><span data-ttu-id="f549d-103">Raggruppamento di oggetti transazionali</span><span class="sxs-lookup"><span data-stu-id="f549d-103">Pooling Transactional Objects</span></span>

<span data-ttu-id="f549d-104">I componenti transazionali che devono essere raggruppati hanno requisiti particolari.</span><span class="sxs-lookup"><span data-stu-id="f549d-104">Transactional components that are to be pooled have special requirements.</span></span>

## <a name="manually-enlisting-resources"></a><span data-ttu-id="f549d-105">Integrazione manuale delle risorse</span><span class="sxs-lookup"><span data-stu-id="f549d-105">Manually Enlisting Resources</span></span>

<span data-ttu-id="f549d-106">Gli oggetti pool che fanno parte delle transazioni devono integrare manualmente le risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="f549d-106">Poolable objects that participate in transactions must manually enlist managed resources.</span></span> <span data-ttu-id="f549d-107">Se un oggetto contiene risorse gestite tra client, non sarà possibile eseguire automaticamente l'integrazione di Resource Manager in una transazione quando l'oggetto viene attivato in un determinato contesto.</span><span class="sxs-lookup"><span data-stu-id="f549d-107">If an object holds managed resources between clients, there will be no way for the resource manager to automatically enlist in a transaction when the object is activated in a given context.</span></span>

<span data-ttu-id="f549d-108">L'oggetto stesso deve gestire la logica di rilevamento della transazione, la disattivazione dell'integrazione automatica di Resource Manager e l'integrazione manuale di tutte le risorse che possiede.</span><span class="sxs-lookup"><span data-stu-id="f549d-108">The object itself must handle the logic of detecting the transaction, turning off the resource manager's auto-enlistment, and manually enlisting any resources that it holds.</span></span> <span data-ttu-id="f549d-109">I passaggi per eseguire questa operazione sono specifici del gestore di risorse in uso.</span><span class="sxs-lookup"><span data-stu-id="f549d-109">The steps for doing this are specific to the resource manager that you are using.</span></span> <span data-ttu-id="f549d-110">Se è necessario eseguire l'integrazione manuale, consultare la documentazione relativa a Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="f549d-110">If you need to do manual enlistment, consult the documentation for your resource manager.</span></span>

<span data-ttu-id="f549d-111">Come descritto di seguito, gli oggetti possono essere raggruppati con affinità di transazione mentre una transazione è attiva e può essere attivata con affinità di transazione se viene chiamata da un client associato a tale transazione.</span><span class="sxs-lookup"><span data-stu-id="f549d-111">As described below, objects can be pooled with transaction affinity while a transaction is active and can be activated with transaction affinity if called by a client associated with that transaction.</span></span> <span data-ttu-id="f549d-112">Prima di eseguire l'integrazione delle risorse, è innanzitutto necessario controllare l'affinità di transazione.</span><span class="sxs-lookup"><span data-stu-id="f549d-112">Before enlisting resources, you should first check for transaction affinity.</span></span> <span data-ttu-id="f549d-113">Se l'oggetto è stato ricavato dal pool specifico di tale transazione, è già stato eseguito il lavoro in tale transazione ed è stata integrata la relativa risorsa.</span><span class="sxs-lookup"><span data-stu-id="f549d-113">If the object has been taken from the pool specific to that transaction, it has already done work in that transaction and enlisted its resources.</span></span>

## <a name="turning-off-automatic-enlistment"></a><span data-ttu-id="f549d-114">Disattivazione dell'integrazione automatica</span><span class="sxs-lookup"><span data-stu-id="f549d-114">Turning Off Automatic Enlistment</span></span>

<span data-ttu-id="f549d-115">L'integrazione automatica deve essere disattivata dopo l'acquisizione della risorsa, in genere nel costruttore dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f549d-115">Automatic enlistment should be turned off after the resource is acquired, usually in the object's constructor.</span></span> <span data-ttu-id="f549d-116">Ovvero si disabilita l'integrazione automatica e quindi si effettua la connessione.</span><span class="sxs-lookup"><span data-stu-id="f549d-116">That is, you disable automatic enlistment and then connect.</span></span>

<span data-ttu-id="f549d-117">La disabilitazione dell'integrazione automatica può talvolta essere una procedura delicata, in particolare nel caso di provider di accesso ai dati a più livelli.</span><span class="sxs-lookup"><span data-stu-id="f549d-117">Disabling auto-enlistment can sometimes be a subtle procedure, particularly in the case of layered data access providers.</span></span> <span data-ttu-id="f549d-118">L'integrazione automatica viene talvolta abbinata al pool di connessioni, come con ODBC e talvolta non come con OLE DB.</span><span class="sxs-lookup"><span data-stu-id="f549d-118">Auto-enlistment is sometimes coupled with connection pooling, as with ODBC, and sometimes not, as with OLE DB.</span></span> <span data-ttu-id="f549d-119">Potrebbe essere necessario assicurarsi che l'inserimento automatico sia disattivato a diversi livelli di provider.</span><span class="sxs-lookup"><span data-stu-id="f549d-119">You might need to ensure that auto-enlistment is off at several levels of providers.</span></span>

## <a name="implementing-iobjectcontrol"></a><span data-ttu-id="f549d-120">Implementazione di IObjectControl</span><span class="sxs-lookup"><span data-stu-id="f549d-120">Implementing IObjectControl</span></span>

<span data-ttu-id="f549d-121">Gli oggetti che fanno parte di un pool che partecipano alle transazioni devono monitorare lo stato corrente delle risorse che contengono.</span><span class="sxs-lookup"><span data-stu-id="f549d-121">Poolable objects that participate in transactions must monitor the current state of resources they are holding.</span></span> <span data-ttu-id="f549d-122">Se l'oggetto rileva che si trova in uno stato non riutilizzabile, ad esempio se una connessione non è valida, deve restituire false per [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span><span class="sxs-lookup"><span data-stu-id="f549d-122">If the object detects that it is in a non-reusable state—for example, if a connection is bad—it should return False for [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).</span></span> <span data-ttu-id="f549d-123">Questo avrà l'effetto di rimuovere l'istanza dell'oggetto e di destinarla alla transazione corrente.</span><span class="sxs-lookup"><span data-stu-id="f549d-123">This will have the effect of both discarding the object instance and dooming the current transaction.</span></span>

## <a name="transaction-specific-pools"></a><span data-ttu-id="f549d-124">Pool di Transaction-Specific</span><span class="sxs-lookup"><span data-stu-id="f549d-124">Transaction-Specific Pools</span></span>

<span data-ttu-id="f549d-125">Un pool di oggetti è in genere omogeneo e qualsiasi oggetto in pool non attualmente in uso è utile per tornare a qualsiasi client.</span><span class="sxs-lookup"><span data-stu-id="f549d-125">A pool of objects is generally homogenous, and any pooled object not currently in use is good to return to any client.</span></span> <span data-ttu-id="f549d-126">L'unica eccezione a questa regola è nel caso degli oggetti transazionali, per cui è ottimizzato il pool di oggetti.</span><span class="sxs-lookup"><span data-stu-id="f549d-126">The only exception to this rule is in the case of transactional objects, for which object pooling is optimized.</span></span> <span data-ttu-id="f549d-127">Quando il client che richiede un oggetto ha una transazione associata, COM+ analizzerà il pool per un oggetto disponibile già associato a tale transazione.</span><span class="sxs-lookup"><span data-stu-id="f549d-127">When the client requesting an object has an associated transaction, COM+ will scan the pool for an available object that is already associated with that transaction.</span></span> <span data-ttu-id="f549d-128">Se viene trovato un oggetto con affinità di transazione, quest'operazione viene restituita al client. in caso contrario, viene restituito un oggetto dal pool generale.</span><span class="sxs-lookup"><span data-stu-id="f549d-128">If an object with transaction affinity is found, it is returned to the client; otherwise, an object from the general pool is returned.</span></span>

<span data-ttu-id="f549d-129">In questo modo, i pool speciali vengono mantenuti contenenti oggetti con affinità per una determinata transazione.</span><span class="sxs-lookup"><span data-stu-id="f549d-129">In this manner, special subpools are maintained containing objects with affinity for a particular transaction.</span></span> <span data-ttu-id="f549d-130">Quando viene eseguito il commit o l'interruzione della transazione, questi oggetti vengono restituiti al pool generale senza affinità di transazione, pronti per l'utilizzo da parte di qualsiasi client.</span><span class="sxs-lookup"><span data-stu-id="f549d-130">When the transaction commits or aborts, these objects are returned to the general pool with no transaction affinity, ready to be used by any client.</span></span>

<span data-ttu-id="f549d-131">Per questo motivo, quando il componente integra manualmente le risorse gestite in una transazione, deve prima verificare se sono già integrate.</span><span class="sxs-lookup"><span data-stu-id="f549d-131">For this reason, when your component manually enlists its managed resources in a transaction, it should first check to see whether they are already enlisted.</span></span> <span data-ttu-id="f549d-132">In tal caso, non è necessario eseguire l'integrazione.</span><span class="sxs-lookup"><span data-stu-id="f549d-132">If so, there is no need to enlist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f549d-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f549d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f549d-134">Stringhe del costruttore di oggetti COM+</span><span class="sxs-lookup"><span data-stu-id="f549d-134">COM+ Object Constructor Strings</span></span>](com--object-constructor-strings.md)
</dt> <dt>

[<span data-ttu-id="f549d-135">Controllo della durata e dello stato degli oggetti</span><span class="sxs-lookup"><span data-stu-id="f549d-135">Controlling Object Lifetime and State</span></span>](controlling-object-lifetime-and-state.md)
</dt> <dt>

[<span data-ttu-id="f549d-136">Funzionamento del pool di oggetti</span><span class="sxs-lookup"><span data-stu-id="f549d-136">How Object Pooling Works</span></span>](how-object-pooling-works.md)
</dt> <dt>

[<span data-ttu-id="f549d-137">Miglioramento delle prestazioni con il pool di oggetti</span><span class="sxs-lookup"><span data-stu-id="f549d-137">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)
</dt> <dt>

[<span data-ttu-id="f549d-138">Requisiti per gli oggetti pool</span><span class="sxs-lookup"><span data-stu-id="f549d-138">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)
</dt> </dl>

 

 




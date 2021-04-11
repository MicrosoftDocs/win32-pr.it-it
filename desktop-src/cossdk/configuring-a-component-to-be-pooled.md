---
description: È possibile configurare un componente da raggruppare solo quando viene scritto correttamente per supportare il pool. Per informazioni dettagliate su questi requisiti, vedere Requisiti per gli oggetti pool.
ms.assetid: ffd812cc-811e-4f2a-8736-d1cb22d5abb7
title: Configurazione di un componente da raggruppare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780f7e1d9128b213b138e63b9dfa7e0f40642681
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127563"
---
# <a name="configuring-a-component-to-be-pooled"></a><span data-ttu-id="8fd89-104">Configurazione di un componente da raggruppare</span><span class="sxs-lookup"><span data-stu-id="8fd89-104">Configuring a Component to Be Pooled</span></span>

<span data-ttu-id="8fd89-105">È possibile configurare un componente da raggruppare solo quando viene scritto correttamente per supportare il pool.</span><span class="sxs-lookup"><span data-stu-id="8fd89-105">You can configure a component to be pooled only when it is correctly written to support being pooled.</span></span> <span data-ttu-id="8fd89-106">Per informazioni dettagliate su questi requisiti, vedere [requisiti per gli oggetti pool](requirements-for-poolable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8fd89-106">For details of these requirements, see [Requirements for Poolable Objects](requirements-for-poolable-objects.md).</span></span>

> [!Note]  
> <span data-ttu-id="8fd89-107">Per impostazione predefinita, un componente non è configurato per essere in pool.</span><span class="sxs-lookup"><span data-stu-id="8fd89-107">By default, a component is not configured to be pooled.</span></span>

 

<span data-ttu-id="8fd89-108">Quando si configura un componente da raggruppare, è possibile specificare le proprietà seguenti per determinare il modo in cui COM+ gestisce il pool:</span><span class="sxs-lookup"><span data-stu-id="8fd89-108">When you configure a component to be pooled, you can specify the following properties to determine how COM+ maintains the pool:</span></span>

-   <span data-ttu-id="8fd89-109">**Dimensioni minime del pool.**</span><span class="sxs-lookup"><span data-stu-id="8fd89-109">**Minimum pool size.**</span></span> <span data-ttu-id="8fd89-110">Rappresenta il numero di oggetti creati all'avvio dell'applicazione e il numero minimo di oggetti conservati nel pool mentre l'applicazione è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8fd89-110">Represents the number of objects that are created when the application starts and the minimum number of objects that are maintained in the pool while the application is running.</span></span> <span data-ttu-id="8fd89-111">Se il numero di oggetti disponibili nel pool scende al di sotto del valore minimo specificato, vengono creati nuovi oggetti per soddisfare le richieste di oggetti in attesa e riempire il pool.</span><span class="sxs-lookup"><span data-stu-id="8fd89-111">If the number of available objects in the pool drops below the specified minimum, new objects are created to meet any outstanding object requests and refill the pool.</span></span> <span data-ttu-id="8fd89-112">Se il numero di oggetti disponibili nel pool è maggiore del numero minimo, questi oggetti surplus vengono eliminati durante un ciclo di pulizia.</span><span class="sxs-lookup"><span data-stu-id="8fd89-112">If the number of available objects in the pool is greater than the minimum number, those surplus objects are destroyed during a clean-up cycle.</span></span>
-   <span data-ttu-id="8fd89-113">**Dimensioni massime del pool.**</span><span class="sxs-lookup"><span data-stu-id="8fd89-113">**Maximum pool size.**</span></span> <span data-ttu-id="8fd89-114">Rappresenta il numero massimo di oggetti in pool che la gestione pool creerà, sia attivamente utilizzato dai client che inattivo nel pool.</span><span class="sxs-lookup"><span data-stu-id="8fd89-114">Represents the maximum number of pooled objects that the pooling manager will create, both actively used by clients and inactive in the pool.</span></span> <span data-ttu-id="8fd89-115">Quando si creano oggetti, gestione pool verifica se la dimensione massima del pool non è stata raggiunta e, in caso contrario, il gestore del pool crea una nuova istanza dell'oggetto da distribuire al client.</span><span class="sxs-lookup"><span data-stu-id="8fd89-115">When creating objects, the pooling manager checks to verify that the maximum pool size has not been reached and, if it hasn't, the pool manager creates a new instance of the object to dispense to the client.</span></span> <span data-ttu-id="8fd89-116">Se è stata raggiunta la dimensione massima del pool, le richieste client verranno accodate e riceveranno il primo oggetto disponibile dal pool in base a una prima funzione.</span><span class="sxs-lookup"><span data-stu-id="8fd89-116">If the maximum pool size has been reached, client requests will be queued and will receive the first available object from the pool on a first-come first-served basis.</span></span> <span data-ttu-id="8fd89-117">Il timeout delle richieste di creazione di oggetti avverrà dopo un periodo specificato.</span><span class="sxs-lookup"><span data-stu-id="8fd89-117">Object creation requests will time-out after a specified period.</span></span>
-   <span data-ttu-id="8fd89-118">**Timeout creazione (MS).**</span><span class="sxs-lookup"><span data-stu-id="8fd89-118">**Creation timeout (ms).**</span></span> <span data-ttu-id="8fd89-119">Specifica il tempo di attesa di un client, in millisecondi, per la restituzione di un oggetto dal pool dopo una chiamata a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="8fd89-119">Specifies how long a client will wait, in milliseconds, for an object to be returned from the pool after a call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="8fd89-120">Se la chiamata del client ha esito negativo, viene restituito l'errore E il \_ timeout.</span><span class="sxs-lookup"><span data-stu-id="8fd89-120">If the client call is unsuccessful, the error E\_TIMEOUT is returned.</span></span>

<span data-ttu-id="8fd89-121">**Per impostare le proprietà correlate al pool**</span><span class="sxs-lookup"><span data-stu-id="8fd89-121">**To set pooling-related properties**</span></span>

1.  <span data-ttu-id="8fd89-122">Nel riquadro dei dettagli dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sul componente che si desidera configurare, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="8fd89-122">In the details pane of the Component Services administrative tool, right-click the component that you want to configure, and then click **Properties**.</span></span>

2.  <span data-ttu-id="8fd89-123">Nella finestra di dialogo Proprietà componente fare clic sulla scheda **attivazione** .</span><span class="sxs-lookup"><span data-stu-id="8fd89-123">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="8fd89-124">Per abilitare il pool di oggetti per il componente, selezionare la casella di controllo **Abilita pool di oggetti** .</span><span class="sxs-lookup"><span data-stu-id="8fd89-124">To enable object pooling for the component, select the **Enable object pooling** check box.</span></span>

4.  <span data-ttu-id="8fd89-125">Nella casella **dimensioni minime pool** immettere il numero minimo di oggetti di questo tipo nel pool.</span><span class="sxs-lookup"><span data-stu-id="8fd89-125">In the **Minimum pool size** box, enter the minimum number of objects of this type in the pool.</span></span> <span data-ttu-id="8fd89-126">Il pool verrà mantenuto per avere almeno questo numero di oggetti.</span><span class="sxs-lookup"><span data-stu-id="8fd89-126">The pool will be maintained to have at least this many objects.</span></span>

5.  <span data-ttu-id="8fd89-127">Nella casella u immettere il numero massimo di oggetti di questo tipo nel pool.</span><span class="sxs-lookup"><span data-stu-id="8fd89-127">In the u box, enter the maximum number of objects of this type in the pool.</span></span> <span data-ttu-id="8fd89-128">Il numero di oggetti, sia attivato che disattivato, non supererà mai questo valore.</span><span class="sxs-lookup"><span data-stu-id="8fd89-128">The number of objects, both activated and deactivated, will never exceed this value.</span></span>

6.  <span data-ttu-id="8fd89-129">Nella casella **timeout creazione (MS)** immettere il periodo di tempo, in millisecondi, in cui un client attenderà un oggetto in pool, se non è immediatamente disponibile.</span><span class="sxs-lookup"><span data-stu-id="8fd89-129">In the **Creation timeout (ms)** box, enter the amount of time, in milliseconds, a client will wait for a pooled object if one is not immediately available.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fd89-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8fd89-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fd89-131">Monitoraggio delle statistiche degli oggetti</span><span class="sxs-lookup"><span data-stu-id="8fd89-131">Monitoring Object Statistics</span></span>](monitoring-object-statistics.md)
</dt> </dl>

 

 

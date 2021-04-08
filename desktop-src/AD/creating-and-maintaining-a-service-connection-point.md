---
title: Creazione e gestione di un punto di connessione del servizio
description: Quando si esegue la pubblicazione con un SCP, tenere presente che deve contenere dati correnti sull'istanza del servizio.
ms.assetid: 2350cb65-3439-4a5f-adc5-b71476793247
ms.tgt_platform: multiple
keywords:
- Creazione e gestione di un punto di connessione del servizio AD
- AD, creazione e gestione del punto di connessione del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c4ad02b92fa6567fc3b709e45f2f64ce66318
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046533"
---
# <a name="creating-and-maintaining-a-service-connection-point"></a><span data-ttu-id="71fd1-105">Creazione e gestione di un punto di connessione del servizio</span><span class="sxs-lookup"><span data-stu-id="71fd1-105">Creating and Maintaining a Service Connection Point</span></span>

<span data-ttu-id="71fd1-106">Quando si esegue la pubblicazione con un SCP, tenere presente che deve contenere dati correnti sull'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="71fd1-106">When publishing with an SCP, remember that it must contain current data about the service instance.</span></span> <span data-ttu-id="71fd1-107">In caso contrario, i client che si associano al SCP recuperano i dati obsoleti.</span><span class="sxs-lookup"><span data-stu-id="71fd1-107">Otherwise, clients that bind to the SCP retrieve outdated data.</span></span> <span data-ttu-id="71fd1-108">Il programma di installazione del servizio, che crea un SCP, specifica i valori iniziali per gli attributi convergenza.</span><span class="sxs-lookup"><span data-stu-id="71fd1-108">Your service installer, that creates an SCP, specifies the initial values for the SCPs attributes.</span></span> <span data-ttu-id="71fd1-109">Quindi, quando l'istanza del servizio viene avviata, deve individuare SCP e aggiornare i valori di attributo, se necessario.</span><span class="sxs-lookup"><span data-stu-id="71fd1-109">Then, when the service instance starts, it must locate the SCP and update the attribute values, if necessary.</span></span> <span data-ttu-id="71fd1-110">In questo modo, i client sono in grado di garantire i dati più recenti.</span><span class="sxs-lookup"><span data-stu-id="71fd1-110">In this way, clients are assured the most current data.</span></span>

<span data-ttu-id="71fd1-111">Dopo la creazione del SCP, il programma di installazione del servizio esegue due passaggi aggiuntivi che consentono al servizio di aggiornare SCP:</span><span class="sxs-lookup"><span data-stu-id="71fd1-111">After creating the SCP, your service installer performs two additional steps that enable your service to update the SCP:</span></span>

-   <span data-ttu-id="71fd1-112">Impostare le voci ACE nel descrittore di sicurezza dell'oggetto SCP per consentire al servizio di modificare gli attributi SCP in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="71fd1-112">Set ACEs in the security descriptor of the SCP object to enable the service to modify SCP attributes at run time.</span></span> <span data-ttu-id="71fd1-113">Per ulteriori informazioni e un esempio di codice, vedere [Abilitazione dell'account del servizio per l'accesso alle proprietà SCP](enabling-service-account-to-access-scp-properties.md).</span><span class="sxs-lookup"><span data-stu-id="71fd1-113">For more information and a code example, see [Enabling Service Account to Access SCP Properties](enabling-service-account-to-access-scp-properties.md).</span></span>
-   <span data-ttu-id="71fd1-114">Memorizzare nella cache il **objectGUID** del SCP nel registro di sistema del computer host del servizio.</span><span class="sxs-lookup"><span data-stu-id="71fd1-114">Cache the **objectGUID** of the SCP in the registry on the service host computer.</span></span> <span data-ttu-id="71fd1-115">Il servizio recupera il GUID memorizzato nella cache per l'associazione all'SCP per verificare e aggiornare i relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="71fd1-115">The service retrieves the cached GUID to bind to the SCP to verify and update its attributes.</span></span>

<span data-ttu-id="71fd1-116">Il programma di installazione del servizio memorizza nella cache il **OBJECTGUID** SCP anziché il DN.</span><span class="sxs-lookup"><span data-stu-id="71fd1-116">The service installer caches the SCP's **objectGUID** rather than its DN.</span></span> <span data-ttu-id="71fd1-117">Il **objectGUID** non cambia mai, indipendentemente dal fatto che SCP venga spostato o rinominato.</span><span class="sxs-lookup"><span data-stu-id="71fd1-117">The **objectGUID** never changes, regardless of whether the SCP is moved or renamed.</span></span> <span data-ttu-id="71fd1-118">Il DN può cambiare se un amministratore sposta o Rinomina SCP.</span><span class="sxs-lookup"><span data-stu-id="71fd1-118">The DN can change if an administrator moves or renames the SCP.</span></span> <span data-ttu-id="71fd1-119">Se, ad esempio, si crea un SCP come figlio di un oggetto computer, il nome distinto del SCP viene modificato se il computer viene rinominato o spostato in un dominio o in un'unità organizzativa diversa.</span><span class="sxs-lookup"><span data-stu-id="71fd1-119">For example, if you create an SCP as a child of a computer object, the distinguished name of the SCP changes if the computer is renamed or moved to a different domain or organizational unit.</span></span>

<span data-ttu-id="71fd1-120">Quando un programma di installazione del servizio crea un SCP, deve leggere il **objectGUID** dell'oggetto appena creato e memorizzarlo nella cache nel registro di sistema del computer host del servizio.</span><span class="sxs-lookup"><span data-stu-id="71fd1-120">When a service installer creates an SCP, it must read the **objectGUID** of the newly created object and cache it in the registry of the service host computer.</span></span> <span data-ttu-id="71fd1-121">Usare il metodo [**IADs:: Get \_ GUID**](/windows/desktop/ADSI/iads-property-methods) per ottenere il valore **objectGUID** in formato stringa adatto per l'associazione.</span><span class="sxs-lookup"><span data-stu-id="71fd1-121">Use the [**IADs::get\_GUID**](/windows/desktop/ADSI/iads-property-methods) method to get the **objectGUID** value in string format suitable for binding.</span></span> <span data-ttu-id="71fd1-122">Memorizzare nella cache la stringa GUID come valore nella seguente chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="71fd1-122">Cache the GUID string as a value under the following registry key.</span></span>

```
HKEY_LOCAL_MACHINE
   vendor name
      product name
```

<span data-ttu-id="71fd1-123">Dove "nome fornitore" e "nome prodotto" identificano il fornitore e il prodotto.</span><span class="sxs-lookup"><span data-stu-id="71fd1-123">Where "vendor name" and "product name" identify the vendor and product.</span></span>

<span data-ttu-id="71fd1-124">Quando il servizio viene avviato, recupera la stringa GUID memorizzata nella cache dal registro di sistema e la usa per l'associazione al SCP.</span><span class="sxs-lookup"><span data-stu-id="71fd1-124">When the service starts, it retrieves the cached GUID string from the registry and uses it to bind to the SCP.</span></span> <span data-ttu-id="71fd1-125">Il servizio legge gli attributi SCP importanti e li confronta con i valori correnti.</span><span class="sxs-lookup"><span data-stu-id="71fd1-125">The service reads the important SCP attributes and compares them to current values.</span></span> <span data-ttu-id="71fd1-126">Se i valori SCP sono obsoleti, il servizio li aggiorna.</span><span class="sxs-lookup"><span data-stu-id="71fd1-126">If the SCP values are outdated, the service updates them.</span></span> <span data-ttu-id="71fd1-127">I valori che possono essere richiesti dal servizio per l'aggiornamento includono **Keywords**, **serviceBindingInformation**, **serviceDNSName** e **serviceDNSNameType**.</span><span class="sxs-lookup"><span data-stu-id="71fd1-127">Values that the service might require to update include **keywords**, **serviceBindingInformation**, **serviceDNSName**, and **serviceDNSNameType**.</span></span>

## <a name="examples"></a><span data-ttu-id="71fd1-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="71fd1-128">Examples</span></span>

-   [<span data-ttu-id="71fd1-129">Esempi di script</span><span class="sxs-lookup"><span data-stu-id="71fd1-129">Script samples</span></span>](script-samples-for-managing-service-connection-points.md)
-   [<span data-ttu-id="71fd1-130">Esempi di codice (C/C++)</span><span class="sxs-lookup"><span data-stu-id="71fd1-130">Code (C/C++) samples</span></span>](code-samples-for-managing-service-connection-points.md)

 

 
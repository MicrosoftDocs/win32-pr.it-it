---
description: Una delle prime attività che è necessario scrivere per un provider è il processo di inizializzazione, che include tutte le attività che il provider deve eseguire, che consente di inviare e ricevere informazioni da WMI, controllare un oggetto gestito ed eseguire altre attività.
ms.assetid: 3dc145b8-1ce4-4caa-b2ac-31a3681e76f1
ms.tgt_platform: multiple
title: Inizializzazione di un provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14a724d72d5e5c58eff30f2fa61da64d77a493f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885394"
---
# <a name="initializing-a-provider"></a><span data-ttu-id="cfcc7-103">Inizializzazione di un provider</span><span class="sxs-lookup"><span data-stu-id="cfcc7-103">Initializing a Provider</span></span>

<span data-ttu-id="cfcc7-104">Una delle prime attività che è necessario scrivere per un provider è il processo di inizializzazione, che include tutte le attività che il provider deve eseguire, che consente di inviare e ricevere informazioni da WMI, controllare un oggetto gestito ed eseguire altre attività.</span><span class="sxs-lookup"><span data-stu-id="cfcc7-104">One of the first tasks you must code for a provider is the initialization process, which covers any tasks your provider must perform that allows it to send and receive information from WMI, control a managed object, and perform other tasks.</span></span> <span data-ttu-id="cfcc7-105">Ogni tipo di provider dispone di un set diverso di attività che deve eseguire e dispone di un set di interfacce univoche associato.</span><span class="sxs-lookup"><span data-stu-id="cfcc7-105">Each type of provider has a different set of tasks that it must perform and has an accompanying set of unique interfaces.</span></span>

<span data-ttu-id="cfcc7-106">Tuttavia, tutti i provider vengono inizializzati tramite l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e indicano a WMI lo stato di inizializzazione tramite l'interfaccia [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) .</span><span class="sxs-lookup"><span data-stu-id="cfcc7-106">However, all providers initialize through the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, and inform WMI of their initialization status through the [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) interface.</span></span>

<span data-ttu-id="cfcc7-107">Nella procedura riportata di seguito viene descritto come inizializzare un provider.</span><span class="sxs-lookup"><span data-stu-id="cfcc7-107">The following procedure describes how to initialize a provider.</span></span>

<span data-ttu-id="cfcc7-108">**Per inizializzare un provider**</span><span class="sxs-lookup"><span data-stu-id="cfcc7-108">**To initialize a provider**</span></span>

1.  <span data-ttu-id="cfcc7-109">Implementare [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) per il provider.</span><span class="sxs-lookup"><span data-stu-id="cfcc7-109">Implement [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) for your provider.</span></span>

    <span data-ttu-id="cfcc7-110">Quando WMI stabilisce che un client richiede i servizi di un provider, WMI carica il provider chiamando il metodo [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) .</span><span class="sxs-lookup"><span data-stu-id="cfcc7-110">When WMI determines that a client requires the services of a provider, WMI loads the provider by calling the [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) method.</span></span>

2.  <span data-ttu-id="cfcc7-111">Implementare qualsiasi interfaccia univoca per il tipo di provider.</span><span class="sxs-lookup"><span data-stu-id="cfcc7-111">Implement any interfaces unique to your type of provider.</span></span>
3.  <span data-ttu-id="cfcc7-112">Informare WMI che il provider è terminato con l'inizializzazione chiamando [**IWbemProviderInitSink:: sestato**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).</span><span class="sxs-lookup"><span data-stu-id="cfcc7-112">Inform WMI that your provider is finished with initialization by calling [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).</span></span>

    <span data-ttu-id="cfcc7-113">Tutte le implementazioni di [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) devono chiamare [**IWbemProviderInitSink:: sestatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) per segnalare lo stato di inizializzazione a WMI.</span><span class="sxs-lookup"><span data-stu-id="cfcc7-113">All implementations of [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) must call [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to report initialization status to WMI.</span></span> <span data-ttu-id="cfcc7-114">Il metodo **sestatus** consente a WMI di determinare se un provider è pronto a ricevere le richieste e il tipo di richieste che il provider è pronto a ricevere.</span><span class="sxs-lookup"><span data-stu-id="cfcc7-114">The **SetStatus** method allows WMI to determine if a provider is ready to receive requests and the type of requests that the provider is ready to receive.</span></span>

<span data-ttu-id="cfcc7-115">Nella procedura riportata di seguito viene descritto come segnalare un'inizializzazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="cfcc7-115">The following procedure describes how to report a successful initialization.</span></span>

<span data-ttu-id="cfcc7-116">**Per segnalare una corretta inizializzazione**</span><span class="sxs-lookup"><span data-stu-id="cfcc7-116">**To report a successful initialization**</span></span>

-   <span data-ttu-id="cfcc7-117">Impostare il parametro *istatus* di [**sestatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) su **WBEM \_ S \_ Initialized**.</span><span class="sxs-lookup"><span data-stu-id="cfcc7-117">Set the *IStatus* parameter of [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to **WBEM\_S\_INITIALIZED**.</span></span>

    <span data-ttu-id="cfcc7-118">Restituendo **l' \_ \_ inizializzazione di WBEM**, un provider indica una preparazione per la gestione delle richieste provenienti da applicazioni, WMI e altri provider.</span><span class="sxs-lookup"><span data-stu-id="cfcc7-118">By returning **WBEM\_S\_INITIALIZED**, a provider indicates a readiness to handle requests from applications, WMI, and other providers.</span></span> <span data-ttu-id="cfcc7-119">Dopo la ricezione \_ di WBEM S \_ Initialized, WMI effettua una chiamata al metodo [**IWbemProviderInit:: QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) nel provider.</span><span class="sxs-lookup"><span data-stu-id="cfcc7-119">After receiving WBEM\_S\_INITIALIZED, WMI makes a call to the [**IWbemProviderInit::QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) method on the provider.</span></span> <span data-ttu-id="cfcc7-120">Questa query recupera un puntatore all'interfaccia principale del provider.</span><span class="sxs-lookup"><span data-stu-id="cfcc7-120">This query retrieves a pointer to the primary interface of the provider.</span></span>

<span data-ttu-id="cfcc7-121">Nella procedura riportata di seguito viene descritto come segnalare un errore durante l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="cfcc7-121">The following procedure describes how to report an error during initialization.</span></span>

<span data-ttu-id="cfcc7-122">**Per segnalare un errore durante l'inizializzazione**</span><span class="sxs-lookup"><span data-stu-id="cfcc7-122">**To report an error during initialization**</span></span>

-   <span data-ttu-id="cfcc7-123">Impostare il parametro *istatus* di [**sestatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) su **WBEM \_ E \_ failed**.</span><span class="sxs-lookup"><span data-stu-id="cfcc7-123">Set the *IStatus* parameter of [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to **WBEM\_E\_FAILED**.</span></span> <span data-ttu-id="cfcc7-124">I provider di viste WMI che restituiscono **WBEM E non sono \_ \_ riusciti** a funzionare.</span><span class="sxs-lookup"><span data-stu-id="cfcc7-124">WMI views providers that return **WBEM\_E\_FAILED** as not functional.</span></span>

    <span data-ttu-id="cfcc7-125">WMI rilascia il puntatore [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) dopo che WMI ha ottenuto un puntatore all'interfaccia principale del provider o dopo che l'inizializzazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="cfcc7-125">WMI releases the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pointer either after WMI has obtained a pointer to the primary interface of the provider or after initialization has failed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfcc7-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cfcc7-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfcc7-127">Sviluppo di un provider WMI</span><span class="sxs-lookup"><span data-stu-id="cfcc7-127">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="cfcc7-128">Impostazione di descrittori di sicurezza spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cfcc7-128">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="cfcc7-129">Sicurezza del provider</span><span class="sxs-lookup"><span data-stu-id="cfcc7-129">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 




---
title: Nome servizio
description: In questo argomento viene illustrato il modo in cui la libreria di gestione Dynamic Data Exchange rende possibile a un'applicazione server di registrare i nomi di servizio supportati.
ms.assetid: 4b7e7f43-18aa-4c2e-aa2b-5ce7bb18048f
keywords:
- Interfaccia utente di Windows, Dynamic Data Exchange (DDE)
- Dynamic Data Exchange (DDE), servizio nome
- DDE (Dynamic Data Exchange), servizio nome
- scambio di dati, Dynamic Data Exchange (DDE)
- Interfaccia utente di Windows, libreria di gestione Dynamic Data Exchange (DDEML)
- Libreria di gestione Dynamic Data Exchange (DDEML), servizio nome
- DDEML (libreria di gestione Dynamic Data Exchange), servizio nome
- scambio di dati, libreria di gestione Dynamic Data Exchange (DDEML)
- Dynamic Data Exchange (DDE), registrazione del nome del servizio
- DDE (Dynamic Data Exchange), registrazione del nome del servizio
- Libreria di gestione Dynamic Data Exchange (DDEML), registrazione del nome del servizio
- DDEML (libreria di gestione Dynamic Data Exchange), registrazione del nome del servizio
- Dynamic Data Exchange (DDE), filtro nome servizio
- DDE (Dynamic Data Exchange), filtro nome servizio
- Libreria di gestione Dynamic Data Exchange (DDEML), filtro nome servizio
- DDEML (libreria di gestione Dynamic Data Exchange), filtro nome servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f958ab73164e70177cb5deeb5f400f44695015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332628"
---
# <a name="name-service"></a><span data-ttu-id="43bd8-119">Nome servizio</span><span class="sxs-lookup"><span data-stu-id="43bd8-119">Name Service</span></span>

<span data-ttu-id="43bd8-120">La libreria di gestione Dynamic Data Exchange (DDEML) consente a un'applicazione server di registrare i nomi di servizio supportati e di impedire al DDEML di inviare transazioni di [**\_ connessione XTYP**](xtyp-connect.md) per i nomi di servizio non supportati alla funzione di callback di Dynamic Data Exchange (DDE) del server.</span><span class="sxs-lookup"><span data-stu-id="43bd8-120">The Dynamic Data Exchange Management Library (DDEML) makes it possible for a server application to register the service names that it supports and to prevent the DDEML from sending [**XTYP\_CONNECT**](xtyp-connect.md) transactions for unsupported service names to the server's Dynamic Data Exchange (DDE) callback function.</span></span>

<span data-ttu-id="43bd8-121">Negli argomenti seguenti viene descritto il nome Service.</span><span class="sxs-lookup"><span data-stu-id="43bd8-121">The following topics describe the name service.</span></span>

-   [<span data-ttu-id="43bd8-122">Registrazione del nome del servizio</span><span class="sxs-lookup"><span data-stu-id="43bd8-122">Service Name Registration</span></span>](#service-name-registration)
-   [<span data-ttu-id="43bd8-123">Filtro nome servizio</span><span class="sxs-lookup"><span data-stu-id="43bd8-123">Service Name Filter</span></span>](#service-name-filter)

## <a name="service-name-registration"></a><span data-ttu-id="43bd8-124">Registrazione del nome del servizio</span><span class="sxs-lookup"><span data-stu-id="43bd8-124">Service Name Registration</span></span>

<span data-ttu-id="43bd8-125">Registrando i nomi di servizio con DDEML, un server informa altre applicazioni DDE nel sistema che è disponibile un nuovo server.</span><span class="sxs-lookup"><span data-stu-id="43bd8-125">By registering its service names with the DDEML, a server informs other DDE applications in the system that a new server is available.</span></span> <span data-ttu-id="43bd8-126">Un server registra un nome di servizio chiamando la funzione [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) e specificando un handle di stringa che identifica il nome.</span><span class="sxs-lookup"><span data-stu-id="43bd8-126">A server registers a service name by calling the [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) function and specifying a string handle that identifies the name.</span></span> <span data-ttu-id="43bd8-127">In risposta, il DDEML invia una transazione di [**\_ registrazione XTYP**](xtyp-register.md) alla funzione di callback di ogni applicazione DDEML nel sistema, ad eccezione di quelle che hanno specificato il \_ \_ flag di filtro di CBF Skip registrations nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="43bd8-127">In response, the DDEML sends an [**XTYP\_REGISTER**](xtyp-register.md) transaction to the callback function of each DDEML application in the system (except those that specified the CBF\_SKIP\_REGISTRATIONS filter flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function).</span></span> <span data-ttu-id="43bd8-128">La **transazione \_ Register XTYP** passa due handle di stringa a una funzione di callback: il primo identifica la stringa che specifica il nome del servizio di base e la seconda identifica la stringa che specifica il servizio specifico dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="43bd8-128">The **XTYP\_REGISTER** transaction passes two string handles to a callback function: the first identifies the string specifying the base service name, and the second identifies the string specifying the instance-specific service.</span></span> <span data-ttu-id="43bd8-129">Un client utilizza in genere il nome del servizio di base in un elenco di server disponibili, in modo che l'utente possa selezionare un server dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="43bd8-129">A client typically uses the base service name in a list of available servers, so the user can select a server from the list.</span></span> <span data-ttu-id="43bd8-130">Il client utilizza il nome del servizio specifico dell'istanza per stabilire una conversazione con un'istanza specifica di un'applicazione server, se è in esecuzione più di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="43bd8-130">The client uses the instance-specific service name to establish a conversation with a specific instance of a server application, if more than one instance is running.</span></span>

<span data-ttu-id="43bd8-131">Un server può utilizzare [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) per annullare la registrazione di un nome di servizio.</span><span class="sxs-lookup"><span data-stu-id="43bd8-131">A server can use [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) to unregister a service name.</span></span> <span data-ttu-id="43bd8-132">Questa funzione fa in modo che DDEML invii [**XTYP \_ Annulla la registrazione**](xtyp-unregister.md) delle transazioni alle altre applicazioni DDE nel sistema, indicando che non possono più usare il nome per stabilire conversazioni.</span><span class="sxs-lookup"><span data-stu-id="43bd8-132">This function causes the DDEML to send [**XTYP\_UNREGISTER**](xtyp-unregister.md) transactions to the other DDE applications in the system, informing them that they can no longer use the name to establish conversations.</span></span>

<span data-ttu-id="43bd8-133">Un server deve chiamare [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) per registrare i nomi di servizio subito dopo la chiamata di [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea).</span><span class="sxs-lookup"><span data-stu-id="43bd8-133">A server must call [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) to register its service names soon after calling [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea).</span></span> <span data-ttu-id="43bd8-134">Un server deve annullare la registrazione dei nomi di servizio usando **DdeNameService** appena prima di chiamare la funzione [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) .</span><span class="sxs-lookup"><span data-stu-id="43bd8-134">A server must unregister its service names by using **DdeNameService** just before calling the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function.</span></span>

## <a name="service-name-filter"></a><span data-ttu-id="43bd8-135">Filtro nome servizio</span><span class="sxs-lookup"><span data-stu-id="43bd8-135">Service Name Filter</span></span>

<span data-ttu-id="43bd8-136">Oltre a registrare i nomi dei servizi, [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) consente a un server di attivare o disattivare il filtro del nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="43bd8-136">In addition to registering service names, [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) enables a server to turn its service name filter on or off.</span></span> <span data-ttu-id="43bd8-137">Quando un server disattiva il filtro del nome del servizio, DDEML invia la transazione di [**\_ connessione XTYP**](xtyp-connect.md) alla funzione di callback DDE del server ogni volta che un client chiama la funzione [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) , indipendentemente dal nome del servizio specificato nella funzione.</span><span class="sxs-lookup"><span data-stu-id="43bd8-137">When a server turns off its service name filter, the DDEML sends the [**XTYP\_CONNECT**](xtyp-connect.md) transaction to the server's DDE callback function whenever any client calls the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function, regardless of the service name specified in the function.</span></span> <span data-ttu-id="43bd8-138">Quando un server attiva il filtro del nome del servizio, DDEML invia la transazione di **\_ connessione XTYP** al server solo quando **DdeConnect** specifica un nome di servizio specificato dal server in una chiamata a **DdeNameService**.</span><span class="sxs-lookup"><span data-stu-id="43bd8-138">When a server turns on its service name filter, the DDEML sends the **XTYP\_CONNECT** transaction to the server only when **DdeConnect** specifies a service name the server has specified in a call to **DdeNameService**.</span></span>

<span data-ttu-id="43bd8-139">Per impostazione predefinita, il filtro del nome del servizio è acceso quando un'applicazione chiama [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea).</span><span class="sxs-lookup"><span data-stu-id="43bd8-139">By default, the service name filter is on when an application calls [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea).</span></span> <span data-ttu-id="43bd8-140">Questa impostazione predefinita impedisce al DDEML di inviare la transazione di [**\_ connessione XTYP**](xtyp-connect.md) a un server prima che il server abbia creato la stringa di gestione necessaria.</span><span class="sxs-lookup"><span data-stu-id="43bd8-140">This default prevents the DDEML from sending the [**XTYP\_CONNECT**](xtyp-connect.md) transaction to a server before the server has created the string handles it needs.</span></span> <span data-ttu-id="43bd8-141">Un server può disabilitare il filtro del nome del servizio specificando il \_ flag FILTEROFF DNS in una chiamata a [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span><span class="sxs-lookup"><span data-stu-id="43bd8-141">A server can turn off its service name filter by specifying the DNS\_FILTEROFF flag in a call to [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span></span> <span data-ttu-id="43bd8-142">Il \_ flag FILTERON DNS attiva il filtro.</span><span class="sxs-lookup"><span data-stu-id="43bd8-142">The DNS\_FILTERON flag turns on the filter.</span></span>

 

 





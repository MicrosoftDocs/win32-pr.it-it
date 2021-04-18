---
description: L'API DRT (Distributed routing table) utilizza le funzioni seguenti.
ms.assetid: 1ceff217-d410-47fa-99a2-8588f001859e
title: Funzioni della tabella di routing distribuita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd48c3a60f458285ce5f607f9ab6bcf7a557cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312286"
---
# <a name="distributed-routing-table-functions"></a><span data-ttu-id="128de-103">Funzioni della tabella di routing distribuita</span><span class="sxs-lookup"><span data-stu-id="128de-103">Distributed Routing Table Functions</span></span>

<span data-ttu-id="128de-104">L'API DRT (Distributed routing table) utilizza le funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="128de-104">The Distributed Routing Table (DRT) API utilizes the following functions.</span></span>

## <a name="lifetime-management-functions"></a><span data-ttu-id="128de-105">Funzioni di gestione della durata</span><span class="sxs-lookup"><span data-stu-id="128de-105">Lifetime Management Functions</span></span>



| <span data-ttu-id="128de-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="128de-106">Function</span></span>                                           | <span data-ttu-id="128de-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="128de-107">Description</span></span>                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="128de-108">**DrtOpen**</span><span class="sxs-lookup"><span data-stu-id="128de-108">**DrtOpen**</span></span>](/windows/desktop/api/drt/nf-drt-drtopen)                         | <span data-ttu-id="128de-109">Crea un'istanza di DRT locale usando i criteri specificati dalla struttura [**\_ delle impostazioni di DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .</span><span class="sxs-lookup"><span data-stu-id="128de-109">Creates a local DRT instance using criteria specified by the [**DRT\_SETTINGS**](/windows/desktop/api/drt/ns-drt-drt_settings) structure.</span></span>  |
| [<span data-ttu-id="128de-110">**DrtClose**</span><span class="sxs-lookup"><span data-stu-id="128de-110">**DrtClose**</span></span>](/windows/desktop/api/drt/nf-drt-drtclose)                       | <span data-ttu-id="128de-111">Chiude e rimuove l'istanza locale di DRT.</span><span class="sxs-lookup"><span data-stu-id="128de-111">Closes and removes the local instance of the DRT.</span></span>                                                              |
| [<span data-ttu-id="128de-112">**DrtGetEventData**</span><span class="sxs-lookup"><span data-stu-id="128de-112">**DrtGetEventData**</span></span>](/windows/desktop/api/drt/nf-drt-drtgeteventdata)         | <span data-ttu-id="128de-113">Recupera i dati dell'evento associati a un evento segnalato.</span><span class="sxs-lookup"><span data-stu-id="128de-113">Retrieves event data associated with a signaled event.</span></span>                                                         |
| [<span data-ttu-id="128de-114">**DrtGetEventDataSize**</span><span class="sxs-lookup"><span data-stu-id="128de-114">**DrtGetEventDataSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgeteventdatasize) | <span data-ttu-id="128de-115">Restituisce la dimensione della struttura [**di \_ \_ dati dell'evento DRT**](/windows/desktop/api/drt/ns-drt-drt_event_data) associata a un evento segnalato.</span><span class="sxs-lookup"><span data-stu-id="128de-115">Returns the size of the [**DRT\_EVENT\_DATA**](/windows/desktop/api/drt/ns-drt-drt_event_data) structure associated with a signaled event.</span></span> |



 

## <a name="module-management-functions"></a><span data-ttu-id="128de-116">Funzioni di gestione dei moduli</span><span class="sxs-lookup"><span data-stu-id="128de-116">Module Management Functions</span></span>



| <span data-ttu-id="128de-117">Funzione</span><span class="sxs-lookup"><span data-stu-id="128de-117">Function</span></span>                                                                           | <span data-ttu-id="128de-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="128de-118">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="128de-119">**DrtCreatePnrpBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="128de-119">**DrtCreatePnrpBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver)           | <span data-ttu-id="128de-120">Crea un resolver bootstrap basato sul protocollo PNRP.</span><span class="sxs-lookup"><span data-stu-id="128de-120">Creates a bootstrap resolver based on the PNRP protocol.</span></span>                                                                              |
| [<span data-ttu-id="128de-121">**DrtDeletePnrpBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="128de-121">**DrtDeletePnrpBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletepnrpbootstrapresolver)           | <span data-ttu-id="128de-122">Elimina un resolver bootstrap basato sul protocollo PNRP.</span><span class="sxs-lookup"><span data-stu-id="128de-122">Deletes a bootstrap resolver based on the PNRP protocol.</span></span>                                                                              |
| [<span data-ttu-id="128de-123">**DrtCreateDnsBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="128de-123">**DrtCreateDnsBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver)             | <span data-ttu-id="128de-124">Crea un provider bootstrap che contatterà un host noto in base al nome.</span><span class="sxs-lookup"><span data-stu-id="128de-124">Creates a bootstrap provider that will contact a well known host by name.</span></span>                                                             |
| [<span data-ttu-id="128de-125">**DrtDeleteDnsBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="128de-125">**DrtDeleteDnsBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver)             | <span data-ttu-id="128de-126">Elimina un provider bootstrap che contatterà un host noto in base al nome.</span><span class="sxs-lookup"><span data-stu-id="128de-126">Deletes a bootstrap provider that will contact a well known host by name.</span></span>                                                             |
| [<span data-ttu-id="128de-127">**DrtCreateIpv6UdpTransport**</span><span class="sxs-lookup"><span data-stu-id="128de-127">**DrtCreateIpv6UdpTransport**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)                     | <span data-ttu-id="128de-128">Crea un trasporto basato sul protocollo UDP IPv6.</span><span class="sxs-lookup"><span data-stu-id="128de-128">Creates a transport based on the IPv6 UDP protocol.</span></span>                                                                                   |
| [<span data-ttu-id="128de-129">**DrtDeleteIpv6UdpTransport**</span><span class="sxs-lookup"><span data-stu-id="128de-129">**DrtDeleteIpv6UdpTransport**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport)                     | <span data-ttu-id="128de-130">Elimina un trasporto basato sul protocollo UDP IPv6.</span><span class="sxs-lookup"><span data-stu-id="128de-130">Deletes a transport based on the IPv6 UDP protocol.</span></span>                                                                                   |
| [<span data-ttu-id="128de-131">**DrtCreateDerivedKeySecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="128de-131">**DrtCreateDerivedKeySecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) | <span data-ttu-id="128de-132">Crea un provider di sicurezza delle chiavi derivato per DRT.</span><span class="sxs-lookup"><span data-stu-id="128de-132">Creates a derived key security provider for the DRT.</span></span>                                                                                  |
| [<span data-ttu-id="128de-133">**DrtCreateDerivedKey**</span><span class="sxs-lookup"><span data-stu-id="128de-133">**DrtCreateDerivedKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatederivedkey)                                 | <span data-ttu-id="128de-134">Crea una chiave che può essere utilizzata da [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) quando DRT utilizza un provider di sicurezza della chiave derivata.</span><span class="sxs-lookup"><span data-stu-id="128de-134">Creates a key that can be utilized by [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) when the DRT is using a derived key security provider.</span></span> |
| [<span data-ttu-id="128de-135">**DrtDeleteDerivedKeySecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="128de-135">**DrtDeleteDerivedKeySecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider) | <span data-ttu-id="128de-136">Elimina un provider di sicurezza della chiave derivata per DRT.</span><span class="sxs-lookup"><span data-stu-id="128de-136">Deletes a derived key security provider for the DRT.</span></span>                                                                                  |
| [<span data-ttu-id="128de-137">**DrtCreateNullSecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="128de-137">**DrtCreateNullSecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider)             | <span data-ttu-id="128de-138">Crea un provider di sicurezza null.</span><span class="sxs-lookup"><span data-stu-id="128de-138">Creates a null security provider.</span></span> <span data-ttu-id="128de-139">Questo provider di sicurezza non richiede nodi per l'autenticazione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="128de-139">This security provider does not require nodes to authenticate keys.</span></span>                                 |
| [<span data-ttu-id="128de-140">**DrtDeleteNullSecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="128de-140">**DrtDeleteNullSecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider)             | <span data-ttu-id="128de-141">Elimina un provider di sicurezza null.</span><span class="sxs-lookup"><span data-stu-id="128de-141">Deletes a null security provider.</span></span>                                                                                                     |



 

## <a name="registration-functions"></a><span data-ttu-id="128de-142">Funzioni di registrazione</span><span class="sxs-lookup"><span data-stu-id="128de-142">Registration Functions</span></span>



| <span data-ttu-id="128de-143">Funzione</span><span class="sxs-lookup"><span data-stu-id="128de-143">Function</span></span>                                     | <span data-ttu-id="128de-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="128de-144">Description</span></span>                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="128de-145">**DrtRegisterKey**</span><span class="sxs-lookup"><span data-stu-id="128de-145">**DrtRegisterKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtregisterkey)     | <span data-ttu-id="128de-146">Registra una chiave in DRT.</span><span class="sxs-lookup"><span data-stu-id="128de-146">Registers a key in the DRT.</span></span>                                    |
| [<span data-ttu-id="128de-147">**DrtUpdateKey**</span><span class="sxs-lookup"><span data-stu-id="128de-147">**DrtUpdateKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtupdatekey)         | <span data-ttu-id="128de-148">Aggiorna i dati dell'applicazione associati a una chiave registrata.</span><span class="sxs-lookup"><span data-stu-id="128de-148">Updates the application data associated with a registered key.</span></span> |
| [<span data-ttu-id="128de-149">**DrtUnregisterKey**</span><span class="sxs-lookup"><span data-stu-id="128de-149">**DrtUnregisterKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtunregisterkey) | <span data-ttu-id="128de-150">Annulla la registrazione di una chiave dal DRT.</span><span class="sxs-lookup"><span data-stu-id="128de-150">Deregisters a key from the DRT.</span></span>                                |



 

## <a name="search-functions"></a><span data-ttu-id="128de-151">Funzioni di ricerca</span><span class="sxs-lookup"><span data-stu-id="128de-151">Search Functions</span></span>



| <span data-ttu-id="128de-152">Funzione</span><span class="sxs-lookup"><span data-stu-id="128de-152">Function</span></span>                                                 | <span data-ttu-id="128de-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="128de-153">Description</span></span>                                                                                                                                                                                                             |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="128de-154">**DrtStartSearch**</span><span class="sxs-lookup"><span data-stu-id="128de-154">**DrtStartSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtstartsearch)                 | <span data-ttu-id="128de-155">Cerca una chiave in DRT usando i criteri specificati nella struttura [**delle \_ \_ informazioni di ricerca DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) .</span><span class="sxs-lookup"><span data-stu-id="128de-155">Searches the DRT for a key using criteria specified in the [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) structure.</span></span>                                                                                                      |
| [<span data-ttu-id="128de-156">**DrtContinueSearch**</span><span class="sxs-lookup"><span data-stu-id="128de-156">**DrtContinueSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtcontinuesearch)           | <span data-ttu-id="128de-157">Continua una ricerca \_ \_ \_ di un percorso di DRT di ricerca di una chiave in DRT.</span><span class="sxs-lookup"><span data-stu-id="128de-157">Continues a DRT\_SEARCH\_RETURN\_PATH search for a key in the DRT.</span></span> <span data-ttu-id="128de-158">Questa funzione viene usata solo quando il flag **fIterative** è impostato su **true** nella struttura associata [**di \_ \_ informazioni di ricerca DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) .</span><span class="sxs-lookup"><span data-stu-id="128de-158">This function is used only when the **fIterative** flag is set to **TRUE** in the associated [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) structure.</span></span> |
| [<span data-ttu-id="128de-159">**DrtGetSearchResult**</span><span class="sxs-lookup"><span data-stu-id="128de-159">**DrtGetSearchResult**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)         | <span data-ttu-id="128de-160">Recupera i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="128de-160">Retrieves the search result(s).</span></span>                                                                                                                                                                                         |
| [<span data-ttu-id="128de-161">**DrtGetSearchResultSize**</span><span class="sxs-lookup"><span data-stu-id="128de-161">**DrtGetSearchResultSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchresultsize) | <span data-ttu-id="128de-162">Restituisce la dimensione del successivo risultato della ricerca disponibile.</span><span class="sxs-lookup"><span data-stu-id="128de-162">Returns the size of the next available search result.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="128de-163">**DrtGetSearchPath**</span><span class="sxs-lookup"><span data-stu-id="128de-163">**DrtGetSearchPath**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchpath)             | <span data-ttu-id="128de-164">Restituisce un elenco di nodi contattati durante l'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="128de-164">Returns a list of nodes contacted during the search operation.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="128de-165">**DrtGetSearchPathSize**</span><span class="sxs-lookup"><span data-stu-id="128de-165">**DrtGetSearchPathSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize)     | <span data-ttu-id="128de-166">Restituisce la dimensione del percorso di ricerca che rappresenta il numero di nodi utilizzati nell'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="128de-166">Returns the size of the search path, which represents the number of nodes utilized in the search operation.</span></span>                                                                                                             |
| [<span data-ttu-id="128de-167">**DrtEndSearch**</span><span class="sxs-lookup"><span data-stu-id="128de-167">**DrtEndSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtendsearch)                     | <span data-ttu-id="128de-168">Annulla la ricerca di una chiave in un DRT e, di conseguenza, la restituzione dei risultati tramite il [**\_ \_ risultato della ricerca DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="128de-168">Cancels a search for a key in a DRT, and as a result, the return of results via [**DRT\_SEARCH\_RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) is stopped.</span></span> <span data-ttu-id="128de-169">Questa API può essere chiamata in qualsiasi momento dopo l'emissione di una ricerca.</span><span class="sxs-lookup"><span data-stu-id="128de-169">This API can be called at any point after a search is issued.</span></span>              |



 

## <a name="instance-name-functions"></a><span data-ttu-id="128de-170">Funzioni nome istanza</span><span class="sxs-lookup"><span data-stu-id="128de-170">Instance Name Functions</span></span>



| <span data-ttu-id="128de-171">Funzione</span><span class="sxs-lookup"><span data-stu-id="128de-171">Function</span></span>                                                 | <span data-ttu-id="128de-172">Descrizione</span><span class="sxs-lookup"><span data-stu-id="128de-172">Description</span></span>                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="128de-173">**DrtGetInstanceName**</span><span class="sxs-lookup"><span data-stu-id="128de-173">**DrtGetInstanceName**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetinstancename)         | <span data-ttu-id="128de-174">Ottiene il nome associato a un'istanza di DRT.</span><span class="sxs-lookup"><span data-stu-id="128de-174">Gets the name associated with a DRT instance.</span></span>                    |
| [<span data-ttu-id="128de-175">**DrtGetInstanceNameSize**</span><span class="sxs-lookup"><span data-stu-id="128de-175">**DrtGetInstanceNameSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetinstancenamesize) | <span data-ttu-id="128de-176">Restituisce le dimensioni del nome dell'istanza della tabella di routing distribuita.</span><span class="sxs-lookup"><span data-stu-id="128de-176">Returns the size of the Distributed Routing Table instance name.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="128de-177">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="128de-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="128de-178">Enumerazioni tabella di routing distribuita</span><span class="sxs-lookup"><span data-stu-id="128de-178">Distributed Routing Table Enumerations</span></span>](distributed-routing-table-enumerations.md)
</dt> <dt>

[<span data-ttu-id="128de-179">Strutture della tabella di routing distribuita</span><span class="sxs-lookup"><span data-stu-id="128de-179">Distributed Routing Table Structures</span></span>](distributed-routing-table-structures.md)
</dt> <dt>

[<span data-ttu-id="128de-180">Riferimento API Tabella routing distribuito</span><span class="sxs-lookup"><span data-stu-id="128de-180">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 




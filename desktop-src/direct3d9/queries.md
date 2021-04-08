---
description: Sono disponibili diversi tipi di query progettati per eseguire query sullo stato delle risorse.
ms.assetid: 2c65d199-141d-43a7-b513-4cb4459d7c27
title: Query (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f450aa7015d4b66ad28b6c4d0632b2995bedd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875961"
---
# <a name="queries-direct3d-9"></a><span data-ttu-id="57925-103">Query (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="57925-103">Queries (Direct3D 9)</span></span>

<span data-ttu-id="57925-104">Sono disponibili diversi tipi di query progettati per eseguire query sullo stato delle risorse.</span><span class="sxs-lookup"><span data-stu-id="57925-104">There are several types of queries which are designed to query the status of resources.</span></span> <span data-ttu-id="57925-105">Lo stato di una determinata risorsa include lo stato della GPU (Graphics Processing Unit), lo stato del driver o lo stato di Runtime.</span><span class="sxs-lookup"><span data-stu-id="57925-105">The status of a given resource includes graphics processing unit (GPU) status, driver status, or runtime status.</span></span> <span data-ttu-id="57925-106">Per comprendere la differenza tra i diversi tipi di query, è necessario comprendere gli Stati della query.</span><span class="sxs-lookup"><span data-stu-id="57925-106">To understand the difference between the different query types, you need to understand the query states.</span></span> <span data-ttu-id="57925-107">Il diagramma di transizione di stato seguente illustra ogni stato della query.</span><span class="sxs-lookup"><span data-stu-id="57925-107">The following state transition diagram explains each of the query states.</span></span>

![diagramma che mostra le transizioni tra gli Stati di query](images/queries.png)

<span data-ttu-id="57925-109">Il diagramma mostra tre stati, ognuno definito da cerchi.</span><span class="sxs-lookup"><span data-stu-id="57925-109">The diagram shows three states, each defined by circles.</span></span> <span data-ttu-id="57925-110">Ognuna delle linee continue è costituita da eventi basati su applicazioni che provocano una transizione di stato.</span><span class="sxs-lookup"><span data-stu-id="57925-110">Each of the solid lines are application-driven events that cause a state transition.</span></span> <span data-ttu-id="57925-111">La linea tratteggiata è un evento basato sulle risorse che passa una query dallo stato emesso allo stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="57925-111">The dashed line is a resource-driven event that switches a query from the issued state to the signaled state.</span></span> <span data-ttu-id="57925-112">Ognuno di questi Stati ha uno scopo diverso:</span><span class="sxs-lookup"><span data-stu-id="57925-112">Each of these states has a different purpose:</span></span>

-   <span data-ttu-id="57925-113">Lo stato segnalato è come uno stato inattivo.</span><span class="sxs-lookup"><span data-stu-id="57925-113">The signaled state is like an idle state.</span></span> <span data-ttu-id="57925-114">L'oggetto query è stato generato ed è in attesa del rilascio della query da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="57925-114">The query object has been generated and is waiting for the application to issue the query.</span></span> <span data-ttu-id="57925-115">Una volta completata la query e la transizione allo stato segnalato, è possibile recuperare la risposta alla query.</span><span class="sxs-lookup"><span data-stu-id="57925-115">Once a query has completed and transitioned back to the signaled state, the answer to the query can be retrieved.</span></span>
-   <span data-ttu-id="57925-116">Lo stato di compilazione è analogo a un'area di gestione temporanea di una query.</span><span class="sxs-lookup"><span data-stu-id="57925-116">The building state is like a staging area for a query.</span></span> <span data-ttu-id="57925-117">Dallo stato di compilazione è stata eseguita una query (chiamando [**\_ Begin D3DISSUE**](d3dissue-begin.md)) ma non è ancora stata eseguita la transizione allo stato emesso.</span><span class="sxs-lookup"><span data-stu-id="57925-117">From the building state, a query has been issued (by calling [**D3DISSUE\_BEGIN**](d3dissue-begin.md)) but has not yet transitioned to the issued state.</span></span> <span data-ttu-id="57925-118">Quando un'applicazione invia una query end (chiamando [**D3DISSUE \_ end**](d3dissue-end.md)), la query esegue la transizione allo stato emesso.</span><span class="sxs-lookup"><span data-stu-id="57925-118">When an application issues a query end (by calling [**D3DISSUE\_END**](d3dissue-end.md)), the query transitions to the issued state.</span></span>
-   <span data-ttu-id="57925-119">Lo stato emesso indica che la risorsa sottoposta a query ha il controllo della query.</span><span class="sxs-lookup"><span data-stu-id="57925-119">The issued state means that the resource being queried has control of the query.</span></span> <span data-ttu-id="57925-120">Al termine del lavoro della risorsa, la risorsa esegue la transizione della macchina a stati verso lo stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="57925-120">Once the resource finishes its work, the resource transitions the state machine to the signaled state.</span></span> <span data-ttu-id="57925-121">Durante lo stato emesso, l'applicazione deve eseguire il polling per rilevare la transizione allo stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="57925-121">During the issued state, the application must poll to detect the transition to the signaled state.</span></span> <span data-ttu-id="57925-122">Una volta eseguita la transizione allo stato segnalato, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) restituisce il risultato della query (tramite un argomento) all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="57925-122">Once the transition to the signaled state occurs, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) returns the query result (through an argument) to the application.</span></span>

<span data-ttu-id="57925-123">Nella tabella seguente sono elencati i tipi di query disponibili.</span><span class="sxs-lookup"><span data-stu-id="57925-123">The following table lists the available query types.</span></span>



| <span data-ttu-id="57925-124">Tipo di query</span><span class="sxs-lookup"><span data-stu-id="57925-124">Query Type</span></span>        | <span data-ttu-id="57925-125">Evento Issue</span><span class="sxs-lookup"><span data-stu-id="57925-125">Issue Event</span></span>                                                                      | <span data-ttu-id="57925-126">Buffer GetData</span><span class="sxs-lookup"><span data-stu-id="57925-126">GetData buffer</span></span>                                                              | <span data-ttu-id="57925-127">Runtime</span><span class="sxs-lookup"><span data-stu-id="57925-127">Runtime</span></span>      | <span data-ttu-id="57925-128">Inizio implicito della query</span><span class="sxs-lookup"><span data-stu-id="57925-128">Implicit beginning of query</span></span>                      |
|-------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------|--------------------------------------------------|
| <span data-ttu-id="57925-129">BANDWIDTHTIMINGS</span><span class="sxs-lookup"><span data-stu-id="57925-129">BANDWIDTHTIMINGS</span></span>  | <span data-ttu-id="57925-130">[**D3DISSUE \_ Begin**](d3dissue-begin.md), [ **D3DISSUE \_ end**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="57925-130">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="57925-131">**\_D3D9BANDWIDTHTIMINGS D3DDEVINFO**</span><span class="sxs-lookup"><span data-stu-id="57925-131">**D3DDEVINFO\_D3D9BANDWIDTHTIMINGS**</span></span>](d3ddevinfo-d3d9bandwidthtimings.md) | <span data-ttu-id="57925-132">Vendita al dettaglio/debug</span><span class="sxs-lookup"><span data-stu-id="57925-132">Retail/Debug</span></span> | <span data-ttu-id="57925-133">N/D</span><span class="sxs-lookup"><span data-stu-id="57925-133">N/A</span></span>                                              |
| <span data-ttu-id="57925-134">CACHEUTILIZATION</span><span class="sxs-lookup"><span data-stu-id="57925-134">CACHEUTILIZATION</span></span>  | <span data-ttu-id="57925-135">[**D3DISSUE \_ Begin**](d3dissue-begin.md), [ **D3DISSUE \_ end**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="57925-135">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="57925-136">**\_D3D9CACHEUTILIZATION D3DDEVINFO**</span><span class="sxs-lookup"><span data-stu-id="57925-136">**D3DDEVINFO\_D3D9CACHEUTILIZATION**</span></span>](d3ddevinfo-d3d9cacheutilization.md) | <span data-ttu-id="57925-137">Vendita al dettaglio/debug</span><span class="sxs-lookup"><span data-stu-id="57925-137">Retail/Debug</span></span> | <span data-ttu-id="57925-138">N/D</span><span class="sxs-lookup"><span data-stu-id="57925-138">N/A</span></span>                                              |
| <span data-ttu-id="57925-139">EVENTO</span><span class="sxs-lookup"><span data-stu-id="57925-139">EVENT</span></span>             | [<span data-ttu-id="57925-140">**\_Fine D3DISSUE**</span><span class="sxs-lookup"><span data-stu-id="57925-140">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="57925-141">BOOL</span><span class="sxs-lookup"><span data-stu-id="57925-141">BOOL</span></span>                                                                        | <span data-ttu-id="57925-142">Vendita al dettaglio/debug</span><span class="sxs-lookup"><span data-stu-id="57925-142">Retail/Debug</span></span> | [<span data-ttu-id="57925-143">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="57925-143">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| <span data-ttu-id="57925-144">INTERFACETIMINGS</span><span class="sxs-lookup"><span data-stu-id="57925-144">INTERFACETIMINGS</span></span>  | <span data-ttu-id="57925-145">[**D3DISSUE \_ Begin**](d3dissue-begin.md), [ **D3DISSUE \_ end**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="57925-145">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="57925-146">**\_D3D9INTERFACETIMINGS D3DDEVINFO**</span><span class="sxs-lookup"><span data-stu-id="57925-146">**D3DDEVINFO\_D3D9INTERFACETIMINGS**</span></span>](d3ddevinfo-d3d9interfacetimings.md) | <span data-ttu-id="57925-147">Vendita al dettaglio/debug</span><span class="sxs-lookup"><span data-stu-id="57925-147">Retail/Debug</span></span> | <span data-ttu-id="57925-148">N/D</span><span class="sxs-lookup"><span data-stu-id="57925-148">N/A</span></span>                                              |
| <span data-ttu-id="57925-149">OCCLUSIONE</span><span class="sxs-lookup"><span data-stu-id="57925-149">OCCLUSION</span></span>         | <span data-ttu-id="57925-150">[**D3DISSUE \_ Begin**](d3dissue-begin.md), [ **D3DISSUE \_ end**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="57925-150">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | <span data-ttu-id="57925-151">DWORD</span><span class="sxs-lookup"><span data-stu-id="57925-151">DWORD</span></span>                                                                       | <span data-ttu-id="57925-152">Vendita al dettaglio/debug</span><span class="sxs-lookup"><span data-stu-id="57925-152">Retail/Debug</span></span> | <span data-ttu-id="57925-153">N/D</span><span class="sxs-lookup"><span data-stu-id="57925-153">N/A</span></span>                                              |
| <span data-ttu-id="57925-154">PIPELINETIMINGS</span><span class="sxs-lookup"><span data-stu-id="57925-154">PIPELINETIMINGS</span></span>   | <span data-ttu-id="57925-155">[**D3DISSUE \_ Begin**](d3dissue-begin.md), [ **D3DISSUE \_ end**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="57925-155">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="57925-156">**\_D3D9PIPELINETIMINGS D3DDEVINFO**</span><span class="sxs-lookup"><span data-stu-id="57925-156">**D3DDEVINFO\_D3D9PIPELINETIMINGS**</span></span>](d3ddevinfo-d3d9pipelinetimings.md)   | <span data-ttu-id="57925-157">Vendita al dettaglio/debug</span><span class="sxs-lookup"><span data-stu-id="57925-157">Retail/Debug</span></span> | <span data-ttu-id="57925-158">N/D</span><span class="sxs-lookup"><span data-stu-id="57925-158">N/A</span></span>                                              |
| <span data-ttu-id="57925-159">RESOURCEMANAGER</span><span class="sxs-lookup"><span data-stu-id="57925-159">RESOURCEMANAGER</span></span>   | [<span data-ttu-id="57925-160">**\_Fine D3DISSUE**</span><span class="sxs-lookup"><span data-stu-id="57925-160">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="57925-161">**\_RESOURCEMANAGER D3DDEVINFO**</span><span class="sxs-lookup"><span data-stu-id="57925-161">**D3DDEVINFO\_ResourceManager**</span></span>](d3ddevinfo-resourcemanager.md)           | <span data-ttu-id="57925-162">Solo debug</span><span class="sxs-lookup"><span data-stu-id="57925-162">Debug only</span></span>   | [<span data-ttu-id="57925-163">**Presente**</span><span class="sxs-lookup"><span data-stu-id="57925-163">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| <span data-ttu-id="57925-164">timestamp</span><span class="sxs-lookup"><span data-stu-id="57925-164">TIMESTAMP</span></span>         | [<span data-ttu-id="57925-165">**\_Fine D3DISSUE**</span><span class="sxs-lookup"><span data-stu-id="57925-165">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="57925-166">UINT64</span><span class="sxs-lookup"><span data-stu-id="57925-166">UINT64</span></span>                                                                      | <span data-ttu-id="57925-167">Vendita al dettaglio/debug</span><span class="sxs-lookup"><span data-stu-id="57925-167">Retail/Debug</span></span> | <span data-ttu-id="57925-168">N/D</span><span class="sxs-lookup"><span data-stu-id="57925-168">N/A</span></span>                                              |
| <span data-ttu-id="57925-169">TIMESTAMPDISJOINT</span><span class="sxs-lookup"><span data-stu-id="57925-169">TIMESTAMPDISJOINT</span></span> | <span data-ttu-id="57925-170">[**D3DISSUE \_ Begin**](d3dissue-begin.md), [ **D3DISSUE \_ end**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="57925-170">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | <span data-ttu-id="57925-171">BOOL</span><span class="sxs-lookup"><span data-stu-id="57925-171">BOOL</span></span>                                                                        | <span data-ttu-id="57925-172">Vendita al dettaglio/debug</span><span class="sxs-lookup"><span data-stu-id="57925-172">Retail/Debug</span></span> | <span data-ttu-id="57925-173">N/D</span><span class="sxs-lookup"><span data-stu-id="57925-173">N/A</span></span>                                              |
| <span data-ttu-id="57925-174">TIMESTAMPFREQ</span><span class="sxs-lookup"><span data-stu-id="57925-174">TIMESTAMPFREQ</span></span>     | [<span data-ttu-id="57925-175">**\_Fine D3DISSUE**</span><span class="sxs-lookup"><span data-stu-id="57925-175">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="57925-176">UINT64</span><span class="sxs-lookup"><span data-stu-id="57925-176">UINT64</span></span>                                                                      | <span data-ttu-id="57925-177">Vendita al dettaglio/debug</span><span class="sxs-lookup"><span data-stu-id="57925-177">Retail/Debug</span></span> | <span data-ttu-id="57925-178">N/D</span><span class="sxs-lookup"><span data-stu-id="57925-178">N/A</span></span>                                              |
| <span data-ttu-id="57925-179">VCACHE</span><span class="sxs-lookup"><span data-stu-id="57925-179">VCACHE</span></span>            | [<span data-ttu-id="57925-180">**\_Fine D3DISSUE**</span><span class="sxs-lookup"><span data-stu-id="57925-180">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="57925-181">**\_VCACHE D3DDEVINFO**</span><span class="sxs-lookup"><span data-stu-id="57925-181">**D3DDEVINFO\_VCACHE**</span></span>](d3ddevinfo-vcache.md)                             | <span data-ttu-id="57925-182">Vendita al dettaglio/debug</span><span class="sxs-lookup"><span data-stu-id="57925-182">Retail/Debug</span></span> | [<span data-ttu-id="57925-183">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="57925-183">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| <span data-ttu-id="57925-184">VERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="57925-184">VERTEXSTATS</span></span>       | [<span data-ttu-id="57925-185">**\_Fine D3DISSUE**</span><span class="sxs-lookup"><span data-stu-id="57925-185">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="57925-186">**\_D3DVERTEXSTATS D3DDEVINFO**</span><span class="sxs-lookup"><span data-stu-id="57925-186">**D3DDEVINFO\_D3DVERTEXSTATS**</span></span>](d3ddevinfo-d3dvertexstats.md)             | <span data-ttu-id="57925-187">Solo debug</span><span class="sxs-lookup"><span data-stu-id="57925-187">Debug only</span></span>   | [<span data-ttu-id="57925-188">**Presente**</span><span class="sxs-lookup"><span data-stu-id="57925-188">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| <span data-ttu-id="57925-189">VERTEXTIMINGS</span><span class="sxs-lookup"><span data-stu-id="57925-189">VERTEXTIMINGS</span></span>     | <span data-ttu-id="57925-190">[**D3DISSUE \_ Begin**](d3dissue-begin.md), [ **D3DISSUE \_ end**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="57925-190">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="57925-191">**\_D3D9STAGETIMINGS D3DDEVINFO**</span><span class="sxs-lookup"><span data-stu-id="57925-191">**D3DDEVINFO\_D3D9STAGETIMINGS**</span></span>](d3ddevinfo-d3d9stagetimings.md)         | <span data-ttu-id="57925-192">Vendita al dettaglio/debug</span><span class="sxs-lookup"><span data-stu-id="57925-192">Retail/Debug</span></span> | <span data-ttu-id="57925-193">N/D</span><span class="sxs-lookup"><span data-stu-id="57925-193">N/A</span></span>                                              |



 

<span data-ttu-id="57925-194">Alcune query richiedono un evento Begin e end, mentre altre richiedono solo un evento End.</span><span class="sxs-lookup"><span data-stu-id="57925-194">Some of the queries require a begin and end event, while others only require an end event.</span></span> <span data-ttu-id="57925-195">Le query che richiedono solo un evento End iniziano quando si verifica un altro evento implicito, elencato nella tabella.</span><span class="sxs-lookup"><span data-stu-id="57925-195">The queries that only require an end event begin when another implicit event occurs (which is listed in the table).</span></span> <span data-ttu-id="57925-196">Tutte le query restituiscono una risposta, ad eccezione della query di eventi la cui risposta è sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="57925-196">All queries return an answer, except the event query whose answer is always **TRUE**.</span></span> <span data-ttu-id="57925-197">Un'applicazione utilizza lo stato della query o il codice restituito di [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="57925-197">An application uses either the state of the query or the return code of [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span>

## <a name="create-a-query"></a><span data-ttu-id="57925-198">Creare una query</span><span class="sxs-lookup"><span data-stu-id="57925-198">Create a Query</span></span>

<span data-ttu-id="57925-199">Prima di creare una query, è possibile verificare se il runtime supporta le query chiamando [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) con un puntatore **null** analogo al seguente:</span><span class="sxs-lookup"><span data-stu-id="57925-199">Before you create a query, you can check to see if the runtime supports queries by calling [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) with a **NULL** pointer like this:</span></span>


```
IDirect3DQuery9* pEventQuery;

// Create a device pointer m_pd3dDevice

// Create a query object
HRESULT hr = m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, NULL);
```



<span data-ttu-id="57925-200">Questo metodo restituisce un codice di esito positivo se è possibile creare una query. in caso contrario, restituisce un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="57925-200">This method returns a success code if a query can be created; otherwise it returns an error code.</span></span> <span data-ttu-id="57925-201">Quando [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) ha esito positivo, è possibile creare un oggetto query analogo al seguente:</span><span class="sxs-lookup"><span data-stu-id="57925-201">Once [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) succeeds, you can create a query object like this:</span></span>


```
IDirect3DQuery9* pEventQuery;
m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);
```



<span data-ttu-id="57925-202">Se la chiamata ha esito positivo, viene creato un oggetto query.</span><span class="sxs-lookup"><span data-stu-id="57925-202">If this call succeeds, a query object is created.</span></span> <span data-ttu-id="57925-203">La query è essenzialmente inattiva nello stato segnalato (con una risposta non inizializzata) in attesa di essere rilasciata.</span><span class="sxs-lookup"><span data-stu-id="57925-203">The query is essentially idle in the signaled state (with an uninitialized answer) waiting to be issued.</span></span> <span data-ttu-id="57925-204">Una volta completata la query, rilasciarla come qualsiasi altra interfaccia.</span><span class="sxs-lookup"><span data-stu-id="57925-204">When you are finished with the query, release it like any other interface.</span></span>

## <a name="issue-a-query"></a><span data-ttu-id="57925-205">Eseguire una query</span><span class="sxs-lookup"><span data-stu-id="57925-205">Issue a Query</span></span>

<span data-ttu-id="57925-206">Un'applicazione modifica lo stato di una query eseguendo una query.</span><span class="sxs-lookup"><span data-stu-id="57925-206">An application changes a query state by issuing a query.</span></span> <span data-ttu-id="57925-207">Di seguito è riportato un esempio di esecuzione di una query:</span><span class="sxs-lookup"><span data-stu-id="57925-207">Here is an example of issuing a query:</span></span>


```
IDirect3DQuery9* pEventQuery;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Issue a Begin event
pEventQuery->Issue(D3DISSUE_BEGIN);

or

// Issue an End event
pEventQuery->Issue(D3DISSUE_END);
```



<span data-ttu-id="57925-208">Una query nello stato segnalato verrà transizione come questa quando viene eseguita:</span><span class="sxs-lookup"><span data-stu-id="57925-208">A query in the signaled state will transition like this when issued:</span></span>



| <span data-ttu-id="57925-209">Tipo di problema</span><span class="sxs-lookup"><span data-stu-id="57925-209">Issue Type</span></span>                                | <span data-ttu-id="57925-210">Esegue una query sulle transizioni a.</span><span class="sxs-lookup"><span data-stu-id="57925-210">Query Transitions to the .</span></span> <span data-ttu-id="57925-211">.</span><span class="sxs-lookup"><span data-stu-id="57925-211">.</span></span> <span data-ttu-id="57925-212">.</span><span class="sxs-lookup"><span data-stu-id="57925-212">.</span></span> |
|-------------------------------------------|--------------------------------|
| [<span data-ttu-id="57925-213">**\_Inizio D3DISSUE**</span><span class="sxs-lookup"><span data-stu-id="57925-213">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="57925-214">Stato di compilazione.</span><span class="sxs-lookup"><span data-stu-id="57925-214">Building state.</span></span>                |
| [<span data-ttu-id="57925-215">**\_Fine D3DISSUE**</span><span class="sxs-lookup"><span data-stu-id="57925-215">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="57925-216">Stato emesso.</span><span class="sxs-lookup"><span data-stu-id="57925-216">Issued state.</span></span>                  |



 

<span data-ttu-id="57925-217">Una query nello stato di compilazione eseguirà la transizione come questa quando viene eseguita:</span><span class="sxs-lookup"><span data-stu-id="57925-217">A query in the building state will transition like this when issued:</span></span>



| <span data-ttu-id="57925-218">Tipo di problema</span><span class="sxs-lookup"><span data-stu-id="57925-218">Issue Type</span></span>                                | <span data-ttu-id="57925-219">Esegue una query sulle transizioni a.</span><span class="sxs-lookup"><span data-stu-id="57925-219">Query Transitions to the .</span></span> <span data-ttu-id="57925-220">.</span><span class="sxs-lookup"><span data-stu-id="57925-220">.</span></span> <span data-ttu-id="57925-221">.</span><span class="sxs-lookup"><span data-stu-id="57925-221">.</span></span>                                            |
|-------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="57925-222">**\_Inizio D3DISSUE**</span><span class="sxs-lookup"><span data-stu-id="57925-222">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="57925-223">(Nessuna transizione, rimane nello stato di compilazione.</span><span class="sxs-lookup"><span data-stu-id="57925-223">(No transition, stays in the building state.</span></span> <span data-ttu-id="57925-224">Riavvia la parentesi della query.</span><span class="sxs-lookup"><span data-stu-id="57925-224">Restarts the query bracket.)</span></span> |
| [<span data-ttu-id="57925-225">**\_Fine D3DISSUE**</span><span class="sxs-lookup"><span data-stu-id="57925-225">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="57925-226">Stato emesso.</span><span class="sxs-lookup"><span data-stu-id="57925-226">Issued state.</span></span>                                                             |



 

<span data-ttu-id="57925-227">Una query nello stato emesso verrà transizione come questa quando viene eseguita:</span><span class="sxs-lookup"><span data-stu-id="57925-227">A query in the issued state will transition like this when issued:</span></span>



| <span data-ttu-id="57925-228">Tipo di problema</span><span class="sxs-lookup"><span data-stu-id="57925-228">Issue Type</span></span>                                | <span data-ttu-id="57925-229">Esegue una query sulle transizioni a.</span><span class="sxs-lookup"><span data-stu-id="57925-229">Query Transitions to the .</span></span> <span data-ttu-id="57925-230">.</span><span class="sxs-lookup"><span data-stu-id="57925-230">.</span></span> <span data-ttu-id="57925-231">.</span><span class="sxs-lookup"><span data-stu-id="57925-231">.</span></span>                    |
|-------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="57925-232">**\_Inizio D3DISSUE**</span><span class="sxs-lookup"><span data-stu-id="57925-232">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="57925-233">Compilazione dello stato e riavvio della parentesi di query.</span><span class="sxs-lookup"><span data-stu-id="57925-233">Building state and restarts the query bracket.</span></span>    |
| [<span data-ttu-id="57925-234">**\_Fine D3DISSUE**</span><span class="sxs-lookup"><span data-stu-id="57925-234">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="57925-235">Stato emesso dopo l'abbandono della query esistente.</span><span class="sxs-lookup"><span data-stu-id="57925-235">Issued state after abandoning the existing query.</span></span> |



 

## <a name="check-the-query-state-and-get-the-answer-to-the-query"></a><span data-ttu-id="57925-236">Controllare lo stato della query e ottenere la risposta alla query</span><span class="sxs-lookup"><span data-stu-id="57925-236">Check the Query State and Get the Answer to the Query</span></span>

<span data-ttu-id="57925-237">[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) esegue due operazioni:</span><span class="sxs-lookup"><span data-stu-id="57925-237">[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) does two things:</span></span>

1.  <span data-ttu-id="57925-238">Restituisce lo stato della query nel codice restituito.</span><span class="sxs-lookup"><span data-stu-id="57925-238">Returns the query state in the return code.</span></span>
2.  <span data-ttu-id="57925-239">Restituisce la risposta alla query in *pData*.</span><span class="sxs-lookup"><span data-stu-id="57925-239">Returns the answer to the query in *pData*.</span></span>

<span data-ttu-id="57925-240">Da ognuno dei tre stati di query, di seguito sono riportati i codici restituiti [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) :</span><span class="sxs-lookup"><span data-stu-id="57925-240">From each of the three query states, here are the [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) return codes:</span></span>



| <span data-ttu-id="57925-241">Stato delle query</span><span class="sxs-lookup"><span data-stu-id="57925-241">Query State</span></span> | <span data-ttu-id="57925-242">Codice restituito GetData</span><span class="sxs-lookup"><span data-stu-id="57925-242">GetData return code</span></span> |
|-------------|---------------------|
| <span data-ttu-id="57925-243">Segnalato</span><span class="sxs-lookup"><span data-stu-id="57925-243">Signaled</span></span>    | <span data-ttu-id="57925-244">\_OK</span><span class="sxs-lookup"><span data-stu-id="57925-244">S\_OK</span></span>               |
| <span data-ttu-id="57925-245">Compilazione</span><span class="sxs-lookup"><span data-stu-id="57925-245">Building</span></span>    | <span data-ttu-id="57925-246">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="57925-246">Error code</span></span>          |
| <span data-ttu-id="57925-247">Rilasciato</span><span class="sxs-lookup"><span data-stu-id="57925-247">Issued</span></span>      | <span data-ttu-id="57925-248">S \_ false</span><span class="sxs-lookup"><span data-stu-id="57925-248">S\_FALSE</span></span>            |



 

<span data-ttu-id="57925-249">Ad esempio, quando una query è nello stato emesso e la risposta alla query non è disponibile, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) restituisce S \_ false.</span><span class="sxs-lookup"><span data-stu-id="57925-249">For example, when a query is in the issued state and the answer to the query is not available, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) returns S\_FALSE.</span></span> <span data-ttu-id="57925-250">Quando la risorsa termina il lavoro e l'applicazione ha emesso una query end, la risorsa esegue la transizione della query allo stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="57925-250">When the resource finishes its work and the application has issued a query end, the resource transitions the query to the signaled state.</span></span> <span data-ttu-id="57925-251">Dallo stato segnalato, **GetData** restituisce S OK, \_ il che significa che la risposta alla query viene restituita anche in *pData*.</span><span class="sxs-lookup"><span data-stu-id="57925-251">From the signaled state, **GetData** returns S\_OK which means that the answer to the query is also returned in *pData*.</span></span> <span data-ttu-id="57925-252">Ad esempio, di seguito è illustrata la sequenza di eventi per restituire il numero di pixel disegnati in una sequenza di rendering:</span><span class="sxs-lookup"><span data-stu-id="57925-252">For instance, here is the sequence of events to return the number of pixels drawn in a render sequence:</span></span>

-   <span data-ttu-id="57925-253">Creare la query.</span><span class="sxs-lookup"><span data-stu-id="57925-253">Create the query.</span></span>
-   <span data-ttu-id="57925-254">Rilascia un evento Begin.</span><span class="sxs-lookup"><span data-stu-id="57925-254">Issue a begin event.</span></span>
-   <span data-ttu-id="57925-255">Creare qualcosa.</span><span class="sxs-lookup"><span data-stu-id="57925-255">Draw something.</span></span>
-   <span data-ttu-id="57925-256">Eseguire un evento di fine.</span><span class="sxs-lookup"><span data-stu-id="57925-256">Issue an end event.</span></span>

<span data-ttu-id="57925-257">Di seguito è riportata la sequenza di codice corrispondente:</span><span class="sxs-lookup"><span data-stu-id="57925-257">The following is the corresponding sequence of code:</span></span>


```
IDirect3DQuery9* pOcclusionQuery;
DWORD numberOfPixelsDrawn;

m_pD3DDevice->CreateQuery(D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery);

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_BEGIN);

// API render loop
...
Draw(...)
...

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pOcclusionQuery->GetData( &numberOfPixelsDrawn, 
                                  sizeof(DWORD), D3DGETDATA_FLUSH ))
    ;
```



<span data-ttu-id="57925-258">Queste righe di codice eseguono diverse operazioni:</span><span class="sxs-lookup"><span data-stu-id="57925-258">These lines of code do several things:</span></span>

-   <span data-ttu-id="57925-259">Chiamare [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) per restituire il numero di pixel disegnati.</span><span class="sxs-lookup"><span data-stu-id="57925-259">Call [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) to return the number of pixels drawn.</span></span>
-   <span data-ttu-id="57925-260">Specificare [**D3DGETDATA \_ Flush**](d3dgetdata-flush.md) per consentire alla risorsa di eseguire la transizione della query allo stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="57925-260">Specify [**D3DGETDATA\_FLUSH**](d3dgetdata-flush.md) to enable the resource to transition the query to the signaled state.</span></span>
-   <span data-ttu-id="57925-261">Eseguire il polling della risorsa di query chiamando [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) da un ciclo.</span><span class="sxs-lookup"><span data-stu-id="57925-261">Poll the query resource by calling [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) from a loop.</span></span> <span data-ttu-id="57925-262">Fino a quando **GetData** restituisce \_ false, significa che la risorsa non ha ancora restituito la risposta.</span><span class="sxs-lookup"><span data-stu-id="57925-262">As long as **GetData** returns S\_FALSE, this means the resource has not returned the answer yet.</span></span>

<span data-ttu-id="57925-263">Il valore restituito da [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) indica essenzialmente lo stato della query.</span><span class="sxs-lookup"><span data-stu-id="57925-263">The return value of [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) essentially tells you in what state the query is.</span></span> <span data-ttu-id="57925-264">I valori possibili sono S \_ OK, s \_ false e un errore.</span><span class="sxs-lookup"><span data-stu-id="57925-264">Possible values are S\_OK, S\_FALSE, and an error.</span></span> <span data-ttu-id="57925-265">Non chiamare **GetData** per una query che si trova nello stato di compilazione.</span><span class="sxs-lookup"><span data-stu-id="57925-265">Do not call **GetData** on a query that is in the building state.</span></span>

-   <span data-ttu-id="57925-266">S \_ OK indica che la risorsa (GPU, driver o Runtime) è stata completata.</span><span class="sxs-lookup"><span data-stu-id="57925-266">S\_OK means the resource (GPU or driver, or runtime) is finished.</span></span> <span data-ttu-id="57925-267">La query viene restituita allo stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="57925-267">The query is returning to the signaled state.</span></span> <span data-ttu-id="57925-268">La risposta, se presente, viene restituita da [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="57925-268">The answer (if any) is being returned by [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span>
-   <span data-ttu-id="57925-269">S \_ false significa che la risorsa (GPU, driver o Runtime) non può restituire ancora una risposta.</span><span class="sxs-lookup"><span data-stu-id="57925-269">S\_FALSE means the resource (GPU or driver, or runtime) cannot return an answer yet.</span></span> <span data-ttu-id="57925-270">Il problema potrebbe essere dovuto al fatto che la GPU non è stata completata o non ha ancora visto il lavoro.</span><span class="sxs-lookup"><span data-stu-id="57925-270">This could be because the GPU is not finished or has not seen the work yet.</span></span>
-   <span data-ttu-id="57925-271">Un errore indica che la query ha generato un errore dal quale non è possibile eseguire il ripristino.</span><span class="sxs-lookup"><span data-stu-id="57925-271">An error means that the query has generated an error from which it cannot recover.</span></span> <span data-ttu-id="57925-272">Questa situazione può verificarsi se il dispositivo viene perso durante una query.</span><span class="sxs-lookup"><span data-stu-id="57925-272">This could be the case if the device is lost during a query.</span></span> <span data-ttu-id="57925-273">Una volta che una query ha generato un errore \_ , ad eccezione di false, è necessario ricreare la query che riavvierà la sequenza di query dallo stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="57925-273">Once a query has generated an error (other than S\_FALSE), the query must be recreated which will restart the query sequence from the signaled state.</span></span>

<span data-ttu-id="57925-274">Anziché specificare [**D3DGETDATA \_ Flush**](d3dgetdata-flush.md), che fornisce informazioni più aggiornate, è possibile fornire zero, ovvero un controllo più leggero se la query è nello stato emesso.</span><span class="sxs-lookup"><span data-stu-id="57925-274">Instead of specifying [**D3DGETDATA\_FLUSH**](d3dgetdata-flush.md), which provides more up-to-date information, you could supply zero which is a more light-weight check if the query is in the issued state.</span></span> <span data-ttu-id="57925-275">Se si specifica zero, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) non Scarica il buffer dei comandi.</span><span class="sxs-lookup"><span data-stu-id="57925-275">Supplying zero will cause [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) to not flush the command buffer.</span></span> <span data-ttu-id="57925-276">Per questo motivo, è necessario prestare attenzione per evitare i cicli infinate (vedere **GetData** per informazioni dettagliate).</span><span class="sxs-lookup"><span data-stu-id="57925-276">For this reason, care must be taken to avoid infinate loops (see **GetData** for details).</span></span> <span data-ttu-id="57925-277">Poiché il runtime Accoda il lavoro nel buffer dei comandi, lo **\_ scaricamento di D3DGETDATA** è un meccanismo per scaricare il buffer dei comandi al driver e, di conseguenza, la GPU; vedere [profilatura accurata delle chiamate API Direct3D (Direct3D 9)](accurately-profiling-direct3d-api-calls.md).</span><span class="sxs-lookup"><span data-stu-id="57925-277">Since the runtime queues up work in the command buffer, **D3DGETDATA\_FLUSH** is a mechanism for flushing the command buffer to the driver (and hence the GPU; see [Accurately Profiling Direct3D API Calls (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="57925-278">Durante lo scaricamento del buffer dei comandi, una query può passare allo stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="57925-278">During the command buffer flush, a query may transition to the signaled state.</span></span>

## <a name="example-an-event-query"></a><span data-ttu-id="57925-279">Esempio: una query di eventi</span><span class="sxs-lookup"><span data-stu-id="57925-279">Example: An Event Query</span></span>

<span data-ttu-id="57925-280">Una query di eventi non supporta un evento Begin.</span><span class="sxs-lookup"><span data-stu-id="57925-280">An event query does not support a begin event.</span></span>

-   <span data-ttu-id="57925-281">Creare la query.</span><span class="sxs-lookup"><span data-stu-id="57925-281">Create the query.</span></span>
-   <span data-ttu-id="57925-282">Eseguire un evento di fine.</span><span class="sxs-lookup"><span data-stu-id="57925-282">Issue an end event.</span></span>
-   <span data-ttu-id="57925-283">Eseguire il polling finché la GPU non è inattiva.</span><span class="sxs-lookup"><span data-stu-id="57925-283">Poll until the GPU is idle.</span></span>
-   <span data-ttu-id="57925-284">Eseguire un evento di fine.</span><span class="sxs-lookup"><span data-stu-id="57925-284">Issue an end event.</span></span>


```
IDirect3DQuery9* pEventQuery = NULL;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

... // API calls

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
```



<span data-ttu-id="57925-285">Questa è la sequenza dei comandi usati da una query di eventi per profilare le chiamate di Application Programming Interface (API) (vedere [profilatura accurata delle chiamate API Direct3D (Direct3D 9)](accurately-profiling-direct3d-api-calls.md).</span><span class="sxs-lookup"><span data-stu-id="57925-285">This is the sequence of commands an event query uses to profile application programming interface (API) calls (see [Accurately Profiling Direct3D API Calls (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="57925-286">Questa sequenza usa i marcatori per controllare la quantità di lavoro nel buffer dei comandi.</span><span class="sxs-lookup"><span data-stu-id="57925-286">This sequence uses markers to help control the amount of work in the command buffer.</span></span>

<span data-ttu-id="57925-287">Si noti che le applicazioni devono prestare particolare attenzione al costo elevato associato allo scaricamento del buffer dei comandi, in quanto in questo modo il sistema operativo passa alla modalità kernel, causando così una notevole riduzione delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="57925-287">Note that applications should pay special attention to the large cost associated with flushing the command buffer because this causes the operating system to switch into kernel mode, thus incurring a sizeable performance penalty.</span></span> <span data-ttu-id="57925-288">Le applicazioni devono inoltre tenere presente che gli sprechi di cicli della CPU attendono il completamento delle query.</span><span class="sxs-lookup"><span data-stu-id="57925-288">Applications should also be aware of wasting CPU cycles by waiting for queries to complete.</span></span>

<span data-ttu-id="57925-289">Le query sono un'ottimizzazione da utilizzare durante il rendering per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="57925-289">Queries are an optimization to be used during rendering to increase performance.</span></span> <span data-ttu-id="57925-290">Pertanto, non è vantaggioso dedicare tempo in attesa del completamento di una query.</span><span class="sxs-lookup"><span data-stu-id="57925-290">Therefore, it is not beneficial to spend time waiting for a query to finish.</span></span> <span data-ttu-id="57925-291">Se viene eseguita una query e se i risultati non sono ancora pronti nel momento in cui l'applicazione li controlla, il tentativo di ottimizzazione non riesce e il rendering dovrebbe continuare normalmente.</span><span class="sxs-lookup"><span data-stu-id="57925-291">If a query is issued and if the results are not yet ready by the time the application checks for them, the attempt at optimizing did not succeed and rendering should continue as normal.</span></span>

<span data-ttu-id="57925-292">L'esempio classico è l'abbattimento dell'occlusione.</span><span class="sxs-lookup"><span data-stu-id="57925-292">The classic example of this is during Occlusion Culling.</span></span> <span data-ttu-id="57925-293">Anziché il ciclo **while** precedente, un'applicazione che usa le query può implementare l'abbattimento dell'occlusione per verificare se una query è stata completata in base al tempo necessario per il risultato.</span><span class="sxs-lookup"><span data-stu-id="57925-293">Instead of the **while** loop above, an application using queries can implement occlusion culling to check to see if a query had finished by the time it needs the result.</span></span> <span data-ttu-id="57925-294">Se la query non è stata completata, continuare (come scenario peggiore) come se l'oggetto sottoposto a test non fosse nascosto (ovvero è visibile) ed eseguirne il rendering.</span><span class="sxs-lookup"><span data-stu-id="57925-294">If the query has not finished, continue (as a worst-case scenario) as if the object being tested against is not occluded (i.e. it is visible) and render it.</span></span> <span data-ttu-id="57925-295">Il codice avrà un aspetto simile al seguente.</span><span class="sxs-lookup"><span data-stu-id="57925-295">The code would look similar to the following.</span></span>


```
IDirect3DQuery9* pOcclusionQuery = NULL;
m_pD3DDevice->CreateQuery( D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery );

// Add a begin marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_BEGIN );

... // API calls

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_END );

// Avoid flushing and letting the CPU go idle by not using a while loop.
// Check if queries are finished:
DWORD dwOccluded = 0;
if( S_FALSE == pOcclusionQuery->GetData( &dwOccluded, sizeof(DWORD), 0 ) )
{
    // Query is not done yet or object not occluded; avoid flushing/wait by continuing with worst-case scenario
    pSomeComplexMesh->Render();
}
else if( dwOccluded != 0 )
{
    // Query is done and object is not occluded.
    pSomeComplexMesh->Render();
}
```



## <a name="related-topics"></a><span data-ttu-id="57925-296">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="57925-296">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57925-297">Argomenti avanzati</span><span class="sxs-lookup"><span data-stu-id="57925-297">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 

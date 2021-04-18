---
description: Sono disponibili numerose query interessanti su un driver che un'applicazione può eseguire se non si verifica alcun costo in termini di prestazioni.
ms.assetid: 81e1c5c5-03bc-4598-814e-14e56513e221
title: Notifica asincrona (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aee8acb791e2e1e2de7eb305cc19df4e7711e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304882"
---
# <a name="asynchronous-notification-direct3d-9"></a><span data-ttu-id="e061b-103">Notifica asincrona (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e061b-103">Asynchronous Notification (Direct3D 9)</span></span>

<span data-ttu-id="e061b-104">Sono disponibili numerose query interessanti su un driver che un'applicazione può eseguire se non si verifica alcun costo in termini di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e061b-104">There are number of interesting queries on a driver that an application can make if there is no performance cost.</span></span> <span data-ttu-id="e061b-105">In Direct3D 7 e Direct3D 8, un meccanismo di query sincrono, GetInfo, funziona bene per elementi come le statistiche, ma non sono state aggiunte query critiche per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e061b-105">In Direct3D 7 and Direct3D 8, a synchronous query mechanism, GetInfo, worked well for things like statistics, but no performance-critical queries were added.</span></span> <span data-ttu-id="e061b-106">Sono presenti altri elementi, come le barriere, intrinsecamente asincroni.</span><span class="sxs-lookup"><span data-stu-id="e061b-106">There are other things (like fences) that are inherently asynchronous.</span></span> <span data-ttu-id="e061b-107">Si tratta di un'API semplice per eseguire query sia sincrone che asincrone.</span><span class="sxs-lookup"><span data-stu-id="e061b-107">This is a simple API to make both synchronous and asynchronous queries.</span></span> <span data-ttu-id="e061b-108">GetInfo verrà ritirato in Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="e061b-108">GetInfo will be retired in Direct3D 9.</span></span>

<span data-ttu-id="e061b-109">Creare una query usando [**IDirect3DDevice9:: CreateQuery**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="e061b-109">Create a query using [**IDirect3DDevice9::CreateQuery**](/windows/desktop/api).</span></span> <span data-ttu-id="e061b-110">Questo metodo accetta D3DQUERYTYPE, che definisce il tipo di query da creare e restituisce un puntatore a un oggetto [**IDirect3DQuery9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="e061b-110">This method takes a D3DQUERYTYPE, which defines what kind of query to make and returns a pointer to an [**IDirect3DQuery9**](/windows/desktop/api) object.</span></span> <span data-ttu-id="e061b-111">Se il tipo di query non è supportato, la chiamata restituisce un errore D3DERR \_ NOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="e061b-111">If the query type is not supported, the call returns an error D3DERR\_NOTAVAILABLE.</span></span> <span data-ttu-id="e061b-112">Utilizzando l'oggetto query, l'applicazione invia la query al runtime utilizzando [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)ed esegue il polling dello stato della query utilizzando [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="e061b-112">Using the query object, the application submits the query to the runtime using [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue), and polls the query status using [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span> <span data-ttu-id="e061b-113">Se il risultato della query è disponibile, viene \_ restituito s OK. in caso contrario, \_ viene restituito s false.</span><span class="sxs-lookup"><span data-stu-id="e061b-113">If the query result is available, S\_OK is returned; otherwise, S\_FALSE is returned.</span></span> <span data-ttu-id="e061b-114">Si prevede che l'applicazione passi un buffer di dimensioni appropriate per i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="e061b-114">The application is expected to pass an appropriately sized buffer for the query results.</span></span>

<span data-ttu-id="e061b-115">L'applicazione ha un'opzione che consente di forzare il runtime a scaricare la query fino al driver usando D3DGETDATA \_ Flush con [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="e061b-115">The application has an option to force the runtime to flush the query down to the driver by using D3DGETDATA\_FLUSH with [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span> <span data-ttu-id="e061b-116">Causa uno scaricamento, forzando il driver a visualizzare la query.</span><span class="sxs-lookup"><span data-stu-id="e061b-116">It causes a flush, forcing the driver to see the query.</span></span> <span data-ttu-id="e061b-117">In questo caso, \_ viene restituito D3DERR DEVICELOST se il dispositivo viene perso.</span><span class="sxs-lookup"><span data-stu-id="e061b-117">In this case, D3DERR\_DEVICELOST is returned if the device becomes lost.</span></span>

<span data-ttu-id="e061b-118">Tutte le query vengono perse quando il dispositivo viene perso, l'applicazione deve crearle nuovamente.</span><span class="sxs-lookup"><span data-stu-id="e061b-118">All queries are lost when the device is lost, the application has to re-create them.</span></span> <span data-ttu-id="e061b-119">Se il dispositivo non supporta la query e pQueryID è **null**, la creazione della query avrà esito negativo con D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e061b-119">If the device does not support the query and the pQueryID is **NULL**, the query creation will fail with D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="e061b-120">Nella tabella seguente vengono riepilogate informazioni importanti su ogni tipo di query.</span><span class="sxs-lookup"><span data-stu-id="e061b-120">The following table summaries important information about each query type.</span></span>



| <span data-ttu-id="e061b-121">QuertyType</span><span class="sxs-lookup"><span data-stu-id="e061b-121">QuertyType</span></span>                    | <span data-ttu-id="e061b-122">Flag di problema valido</span><span class="sxs-lookup"><span data-stu-id="e061b-122">Valid issue flag</span></span>              | <span data-ttu-id="e061b-123">Buffer GetData</span><span class="sxs-lookup"><span data-stu-id="e061b-123">GetData buffer</span></span>              | <span data-ttu-id="e061b-124">Runtime</span><span class="sxs-lookup"><span data-stu-id="e061b-124">Runtime</span></span>      | <span data-ttu-id="e061b-125">Inizio implicito della query</span><span class="sxs-lookup"><span data-stu-id="e061b-125">Implicit beginning of query</span></span> |
|-------------------------------|-------------------------------|-----------------------------|--------------|-----------------------------|
| <span data-ttu-id="e061b-126">\_VCACHE D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="e061b-126">D3DQUERYTYPE\_VCACHE</span></span>          | <span data-ttu-id="e061b-127">\_Fine D3DISSUE</span><span class="sxs-lookup"><span data-stu-id="e061b-127">D3DISSUE\_END</span></span>                 | <span data-ttu-id="e061b-128">\_VCACHE D3DDEVINFO</span><span class="sxs-lookup"><span data-stu-id="e061b-128">D3DDEVINFO\_VCACHE</span></span>          | <span data-ttu-id="e061b-129">Vendita al dettaglio/debug</span><span class="sxs-lookup"><span data-stu-id="e061b-129">Retail/Debug</span></span> | <span data-ttu-id="e061b-130">CreateDevice</span><span class="sxs-lookup"><span data-stu-id="e061b-130">CreateDevice</span></span>                |
| <span data-ttu-id="e061b-131">\_RESOURCEMANAGER D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="e061b-131">D3DQUERYTYPE\_ResourceManager</span></span> | <span data-ttu-id="e061b-132">\_Fine D3DISSUE</span><span class="sxs-lookup"><span data-stu-id="e061b-132">D3DISSUE\_END</span></span>                 | <span data-ttu-id="e061b-133">\_RESOURCEMANAGER D3DDEVINFO</span><span class="sxs-lookup"><span data-stu-id="e061b-133">D3DDEVINFO\_ResourceManager</span></span> | <span data-ttu-id="e061b-134">Solo debug</span><span class="sxs-lookup"><span data-stu-id="e061b-134">Debug only</span></span>   | <span data-ttu-id="e061b-135">Presente</span><span class="sxs-lookup"><span data-stu-id="e061b-135">Present</span></span>                     |
| <span data-ttu-id="e061b-136">\_VERTEXSTATS D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="e061b-136">D3DQUERYTYPE\_VERTEXSTATS</span></span>     | <span data-ttu-id="e061b-137">\_Fine D3DISSUE</span><span class="sxs-lookup"><span data-stu-id="e061b-137">D3DISSUE\_END</span></span>                 | <span data-ttu-id="e061b-138">\_D3DVERTEXSTATS D3DDEVINFO</span><span class="sxs-lookup"><span data-stu-id="e061b-138">D3DDEVINFO\_D3DVERTEXSTATS</span></span>  | <span data-ttu-id="e061b-139">Solo debug</span><span class="sxs-lookup"><span data-stu-id="e061b-139">Debug only</span></span>   | <span data-ttu-id="e061b-140">Presente</span><span class="sxs-lookup"><span data-stu-id="e061b-140">Present</span></span>                     |
| <span data-ttu-id="e061b-141">\_Evento D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="e061b-141">D3DQUERYTYPE\_EVENT</span></span>           | <span data-ttu-id="e061b-142">\_Fine D3DISSUE</span><span class="sxs-lookup"><span data-stu-id="e061b-142">D3DISSUE\_END</span></span>                 | <span data-ttu-id="e061b-143">BOOL</span><span class="sxs-lookup"><span data-stu-id="e061b-143">BOOL</span></span>                        | <span data-ttu-id="e061b-144">Vendita al dettaglio/debug</span><span class="sxs-lookup"><span data-stu-id="e061b-144">Retail/Debug</span></span> | <span data-ttu-id="e061b-145">CreateDevice</span><span class="sxs-lookup"><span data-stu-id="e061b-145">CreateDevice</span></span>                |
| <span data-ttu-id="e061b-146">\_Occlusione D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="e061b-146">D3DQUERYTYPE\_OCCLUSION</span></span>       | <span data-ttu-id="e061b-147">D3DISSUE \_ Begin, D3DISSUE \_ end</span><span class="sxs-lookup"><span data-stu-id="e061b-147">D3DISSUE\_BEGIN,D3DISSUE\_END</span></span> | <span data-ttu-id="e061b-148">DWORD</span><span class="sxs-lookup"><span data-stu-id="e061b-148">DWORD</span></span>                       | <span data-ttu-id="e061b-149">Vendita al dettaglio/debug</span><span class="sxs-lookup"><span data-stu-id="e061b-149">Retail/Debug</span></span> | <span data-ttu-id="e061b-150">N/D</span><span class="sxs-lookup"><span data-stu-id="e061b-150">N/A</span></span>                         |



 

<span data-ttu-id="e061b-151">Campo Flags per [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):</span><span class="sxs-lookup"><span data-stu-id="e061b-151">Flags field for [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):</span></span>


```
#define D3DISSUE_END (1 << 0) 
// Tells the runtime to issue the end of a query, changing its state to 
//   "non-signaled" 
```




```
 
#define D3DISSUE_BEGIN (1 << 1) // Tells the runtime to issue the 
// beginning of a query. 
```



<span data-ttu-id="e061b-152">Campo Flags per [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):</span><span class="sxs-lookup"><span data-stu-id="e061b-152">Flags field for [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):</span></span>


```
 
#define D3DGETDATA_FLUSH (1 << 0) // Tells the runtime to flush 
// if the query is outstanding.
```



## <a name="related-topics"></a><span data-ttu-id="e061b-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e061b-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e061b-154">Suggerimenti per la programmazione</span><span class="sxs-lookup"><span data-stu-id="e061b-154">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 

---
title: Modello a oggetti
description: Nella tabella seguente sono elencati i tipi di oggetto che possono essere modificati tramite i vari set di API forniti da Windows Filtering Platform (PAM).
ms.assetid: 6931583f-785c-4e27-b5e4-d185d23a54ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa90b4757a39617616c6f83b6b79fe322b2e64c8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104046352"
---
# <a name="object-model"></a><span data-ttu-id="22746-103">Modello a oggetti</span><span class="sxs-lookup"><span data-stu-id="22746-103">Object Model</span></span>

<span data-ttu-id="22746-104">Nella tabella seguente sono elencati i tipi di oggetto che possono essere modificati tramite i vari set di API forniti da Windows Filtering Platform (PAM).</span><span class="sxs-lookup"><span data-stu-id="22746-104">The following table lists the object types that can be manipulated through the various API sets supplied by the Windows Filtering Platform (WFP).</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22746-105">Tipo di oggetto</span><span class="sxs-lookup"><span data-stu-id="22746-105">Object Type</span></span></th>
<th><span data-ttu-id="22746-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22746-106">Description</span></span></th>
<th><span data-ttu-id="22746-107">Proprietà di esempio</span><span class="sxs-lookup"><span data-stu-id="22746-107">Sample Properties</span></span></th>
<th><span data-ttu-id="22746-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="22746-108">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22746-109">Filtra</span><span class="sxs-lookup"><span data-stu-id="22746-109">Filter</span></span></td>
<td><span data-ttu-id="22746-110">Regola che governa la classificazione.</span><span class="sxs-lookup"><span data-stu-id="22746-110">A rule that governs classification.</span></span> <span data-ttu-id="22746-111">Se le condizioni vengono soddisfatte, viene richiamata l'azione.</span><span class="sxs-lookup"><span data-stu-id="22746-111">If the conditions are met, the action is invoked.</span></span> <br/> <span data-ttu-id="22746-112">Si tratta dell'oggetto più complesso esposto da WFP, poiché unisce tutti gli altri tipi di oggetto.</span><span class="sxs-lookup"><span data-stu-id="22746-112">This is the most complex object exposed by WFP since it ties together all the other object types.</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="22746-113">Matrice di condizioni</span><span class="sxs-lookup"><span data-stu-id="22746-113">Array of conditions</span></span></li>
<li><span data-ttu-id="22746-114">Azione (Consenti, blocca, callout)</span><span class="sxs-lookup"><span data-stu-id="22746-114">Action (Permit, Block, Callout)</span></span></li>
<li><span data-ttu-id="22746-115"><a href="filter-weight-assignment.md">Weight</a></span><span class="sxs-lookup"><span data-stu-id="22746-115"><a href="filter-weight-assignment.md">Weight</a></span></span></li>
<li><span data-ttu-id="22746-116">Context</span><span class="sxs-lookup"><span data-stu-id="22746-116">Context</span></span></li>
</ul></td>
<td><span data-ttu-id="22746-117">&quot;Blocca il traffico con una porta TCP maggiore di 1024.&quot;</span><span class="sxs-lookup"><span data-stu-id="22746-117">&quot;Block traffic with a TCP port greater than 1024.&quot;</span></span> <br/> <span data-ttu-id="22746-118">&quot;Callout agli ID per tutto il traffico non protetto.&quot;</span><span class="sxs-lookup"><span data-stu-id="22746-118">&quot;Callout to IDS for all traffic that is not secured.&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22746-119">Callout</span><span class="sxs-lookup"><span data-stu-id="22746-119">Callout</span></span></td>
<td><span data-ttu-id="22746-120">Set di funzioni che partecipano al processo di classificazione.</span><span class="sxs-lookup"><span data-stu-id="22746-120">A set of functions that participate in the classification process.</span></span><br/> <span data-ttu-id="22746-121">Consente di eseguire l'elaborazione di pacchetti personalizzati quando vengono soddisfatte determinate condizioni.</span><span class="sxs-lookup"><span data-stu-id="22746-121">It allows for custom packet processing to be done when certain conditions are met.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="22746-122">ID</span><span class="sxs-lookup"><span data-stu-id="22746-122">ID</span></span></li>
<li><span data-ttu-id="22746-123">Livello applicabile</span><span class="sxs-lookup"><span data-stu-id="22746-123">Applicable layer</span></span></li>
</ul></td>
<td><span data-ttu-id="22746-124">Driver NAT</span><span class="sxs-lookup"><span data-stu-id="22746-124">The NAT driver</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22746-125">Livello</span><span class="sxs-lookup"><span data-stu-id="22746-125">Layer</span></span></td>
<td><span data-ttu-id="22746-126">Contenitore di filtri nel motore di filtro.</span><span class="sxs-lookup"><span data-stu-id="22746-126">A filter container in the filter engine.</span></span> <br/> <span data-ttu-id="22746-127">Rappresenta un punto specifico nell'elaborazione del traffico di rete in cui viene richiamato il motore di filtro.</span><span class="sxs-lookup"><span data-stu-id="22746-127">Represents a specific point in network traffic processing where the filter engine is invoked.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="22746-128">Schema per i filtri che è possibile aggiungere al livello</span><span class="sxs-lookup"><span data-stu-id="22746-128">Schema for filters that can be added to the layer</span></span></li>
</ul></td>
<td><span data-ttu-id="22746-129">Livello trasporto in ingresso</span><span class="sxs-lookup"><span data-stu-id="22746-129">The Inbound Transport Layer</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22746-130">Sottolivello</span><span class="sxs-lookup"><span data-stu-id="22746-130">Sub-layer</span></span></td>
<td><span data-ttu-id="22746-131">Sottocomponente di un livello, utilizzato nell' <a href="filter-arbitration.md">arbitro di filtro</a>.</span><span class="sxs-lookup"><span data-stu-id="22746-131">A sub-component of a layer, used in <a href="filter-arbitration.md">filter arbitration</a>.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="22746-132">Peso</span><span class="sxs-lookup"><span data-stu-id="22746-132">Weight</span></span></li>
</ul></td>
<td><span data-ttu-id="22746-133">Sottolivello del tunnel IPsec</span><span class="sxs-lookup"><span data-stu-id="22746-133">The IPsec Tunnel sub-layer</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22746-134">Provider</span><span class="sxs-lookup"><span data-stu-id="22746-134">Provider</span></span></td>
<td><span data-ttu-id="22746-135">Provider di criteri in cui è stata compilata una soluzione in WFP.</span><span class="sxs-lookup"><span data-stu-id="22746-135">A policy provider that has built a solution on WFP.</span></span><br/> <span data-ttu-id="22746-136">Viene utilizzato esclusivamente per la gestione; non influisce sull'elaborazione dei pacchetti in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="22746-136">It is used solely for management; it does not affect run-time packet processing.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="22746-137">ID</span><span class="sxs-lookup"><span data-stu-id="22746-137">ID</span></span></li>
<li><span data-ttu-id="22746-138">Nome del servizio</span><span class="sxs-lookup"><span data-stu-id="22746-138">Service name</span></span></li>
</ul></td>
<td><span data-ttu-id="22746-139">Windows Firewall con sicurezza avanzata</span><span class="sxs-lookup"><span data-stu-id="22746-139">Windows Firewall with Advanced Security</span></span><br/> <span data-ttu-id="22746-140">Applicazione di filtro URL di terze parti</span><span class="sxs-lookup"><span data-stu-id="22746-140">A 3rd-party URL filtering application</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22746-141">Contesto del provider</span><span class="sxs-lookup"><span data-stu-id="22746-141">Provider Context</span></span></td>
<td><span data-ttu-id="22746-142">BLOB di dati utilizzato da un provider di criteri per archiviare informazioni di contesto arbitrarie.</span><span class="sxs-lookup"><span data-stu-id="22746-142">A data blob used by a policy provider to store arbitrary context information.</span></span> <br/> <span data-ttu-id="22746-143">Viene usato per passare le informazioni di configurazione personalizzate a un callout.</span><span class="sxs-lookup"><span data-stu-id="22746-143">It is used to pass custom configuration information to a callout.</span></span><br/> <span data-ttu-id="22746-144">Il modo più comune per usare le informazioni sul contesto consiste nel fare in modo che i filtri facciano riferimento a un contesto del provider.</span><span class="sxs-lookup"><span data-stu-id="22746-144">The most common way to use the context information is to have filters reference a provider context.</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="22746-145">ID</span><span class="sxs-lookup"><span data-stu-id="22746-145">ID</span></span></li>
<li><span data-ttu-id="22746-146">BLOB di dati</span><span class="sxs-lookup"><span data-stu-id="22746-146">Data blob</span></span></li>
</ul></td>
<td><span data-ttu-id="22746-147">IPsec archivia le impostazioni di autenticazione nel motore di filtro di base (BFE).</span><span class="sxs-lookup"><span data-stu-id="22746-147">IPsec stores authentication settings in the Base Filtering Engine ( BFE).</span></span> <span data-ttu-id="22746-148">La &quot; &quot; proprietà di contesto di un filtro indica le impostazioni di autenticazione da usare per il traffico descritto dal filtro.</span><span class="sxs-lookup"><span data-stu-id="22746-148">The &quot;Context&quot; property of a filter indicates the authentication settings to use for the traffic that the filter describes.</span></span><br/> <span data-ttu-id="22746-149">Lo shim di selezione della certificazione SSL archivia le informazioni di certificazione in un contesto del provider.</span><span class="sxs-lookup"><span data-stu-id="22746-149">The SSL certification selection shim will store certification information in a provider context.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="22746-150">I tipi di oggetti esposti dall'API PAM hanno una semantica coerente.</span><span class="sxs-lookup"><span data-stu-id="22746-150">The object types exposed by WFP API have consistent semantics.</span></span> <span data-ttu-id="22746-151">Le azioni di aggiunta, enumerazione, sottoscrizione e così via sono simili per tutti i tipi di oggetto.</span><span class="sxs-lookup"><span data-stu-id="22746-151">The actions of add, enumerate, subscribe, and so on are similar for all object types.</span></span>

<span data-ttu-id="22746-152">Ogni tipo di oggetto è rappresentato da una struttura di dati (ad esempio, [**FWPM \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)).</span><span class="sxs-lookup"><span data-stu-id="22746-152">Each object type is represented by a data structure (for example, [**FWPM\_FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)).</span></span> <span data-ttu-id="22746-153">Per ridurre al minimo il numero di strutture di dati diverse esposte dall'API Pam, viene utilizzata la stessa struttura di dati per l'aggiunta di nuovi oggetti e il recupero di quelli esistenti.</span><span class="sxs-lookup"><span data-stu-id="22746-153">In order to minimize the number of different data structures exposed by the WFP API, the same data structure is used for both adding new objects and retrieving existing ones.</span></span> <span data-ttu-id="22746-154">In questo modo, possono essere presenti campi in ogni struttura di dati che vengono ignorati quando si aggiunge un nuovo oggetto perché questi campi sono compilati dal motore di filtro di base (BFE) e non dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="22746-154">Thus, there may be fields in each data structure that are ignored when adding a new object since these fields are filled in by the Base Filtering Engine (BFE), and not by the caller.</span></span> <span data-ttu-id="22746-155">Ad esempio, una struttura di dati **FWPM \_ FILTER0** ha un campo **FilterId** che contiene il **LUID** **del FWPS FILTER0 \_ corrispondente.**</span><span class="sxs-lookup"><span data-stu-id="22746-155">For example, an **FWPM\_FILTER0** data structure has a **filterId** field that contains the **LUID** of the corresponding **FWPS\_FILTER0**.</span></span> <span data-ttu-id="22746-156">Questo **LUID** viene assegnato da BFE e pertanto questo campo viene ignorato nella chiamata a [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).</span><span class="sxs-lookup"><span data-stu-id="22746-156">This **LUID** is assigned by BFE, and thus, this field is ignored in the call to [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).</span></span>

## <a name="related-topics"></a><span data-ttu-id="22746-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22746-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22746-158">Gestione degli oggetti</span><span class="sxs-lookup"><span data-stu-id="22746-158">Object Management</span></span>](object-management.md)
</dt> </dl>

 

 






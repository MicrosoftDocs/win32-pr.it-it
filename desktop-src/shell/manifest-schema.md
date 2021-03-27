---
description: Questi elementi costituiscono i XML Schema utilizzati nelle procedure guidate per il trasferimento dei manifesti di pubblicazione sul Web e degli ordini di stampa online.
title: Trasferimento dello schema del manifesto
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 488b6fc9-ff85-4860-9cd5-61d5de7e15e8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d0b57f1eb81169674c6c8d36e66c8a3cd21cf0e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994941"
---
# <a name="transfer-manifest-schema"></a><span data-ttu-id="1a962-103">Trasferimento dello schema del manifesto</span><span class="sxs-lookup"><span data-stu-id="1a962-103">Transfer Manifest Schema</span></span>

<span data-ttu-id="1a962-104">Questi elementi costituiscono i XML Schema utilizzati nelle procedure guidate per il trasferimento dei manifesti di pubblicazione sul Web e degli ordini di stampa online.</span><span class="sxs-lookup"><span data-stu-id="1a962-104">These elements make up the XML schema used in the Web Publishing and Online Print Ordering wizards' transfer manifest.</span></span>

<span data-ttu-id="1a962-105">Gli elementi seguenti sono definiti per il manifesto di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="1a962-105">The following elements are defined for the transfer manifest.</span></span>

-   [<span data-ttu-id="1a962-106">cancelledpage</span><span class="sxs-lookup"><span data-stu-id="1a962-106">cancelledpage</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-107">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-108">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-108">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a962-110">failurepage</span><span class="sxs-lookup"><span data-stu-id="1a962-110">failurepage</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-111">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-112">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-112">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-113">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a962-114">preferito</span><span class="sxs-lookup"><span data-stu-id="1a962-114">favorite</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-115">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-116">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-116">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-117">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-117">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a962-118">file</span><span class="sxs-lookup"><span data-stu-id="1a962-118">file</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-119">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-120">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-120">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-121">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-121">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a962-122">filelist</span><span class="sxs-lookup"><span data-stu-id="1a962-122">filelist</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-123">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-124">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-124">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-125">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-125">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a962-126">cartella</span><span class="sxs-lookup"><span data-stu-id="1a962-126">folder</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-127">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-128">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-128">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-129">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-129">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a962-130">cartella</span><span class="sxs-lookup"><span data-stu-id="1a962-130">folderlist</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-131">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-131">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-132">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-132">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-133">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-133">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a962-134">FormData</span><span class="sxs-lookup"><span data-stu-id="1a962-134">formdata</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-135">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-135">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-136">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-136">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-137">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-137">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a962-138">htmlui</span><span class="sxs-lookup"><span data-stu-id="1a962-138">htmlui</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-139">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-139">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-140">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-140">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-141">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-141">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a962-142">imageproperty</span><span class="sxs-lookup"><span data-stu-id="1a962-142">imageproperty</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-143">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-143">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-144">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-144">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-145">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-145">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a962-146">metadati</span><span class="sxs-lookup"><span data-stu-id="1a962-146">metadata</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-147">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-147">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-148">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-148">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-149">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-149">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a962-150">netplace</span><span class="sxs-lookup"><span data-stu-id="1a962-150">netplace</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-151">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-151">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-152">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-152">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-153">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-153">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a962-154">Inserisci</span><span class="sxs-lookup"><span data-stu-id="1a962-154">post</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-155">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-155">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-156">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-156">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-157">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-157">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a962-158">ridimensionare</span><span class="sxs-lookup"><span data-stu-id="1a962-158">resize</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-159">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-159">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-160">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-160">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-161">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-161">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a962-162">successpage</span><span class="sxs-lookup"><span data-stu-id="1a962-162">successpage</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-163">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-163">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-164">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-164">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-165">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-165">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a962-166">target</span><span class="sxs-lookup"><span data-stu-id="1a962-166">target</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-167">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-167">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-168">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-168">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-169">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-169">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a962-170">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="1a962-170">transfermanifest</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-171">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-171">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-172">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-172">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-173">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-173">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a962-174">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="1a962-174">uploadinfo</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-175">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-175">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="1a962-176">Attributes (Attributi)</span><span class="sxs-lookup"><span data-stu-id="1a962-176">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="1a962-177">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-177">Element Information</span></span>](#element-information)

## <a name="cancelledpage"></a><span data-ttu-id="1a962-178">cancelledpage</span><span class="sxs-lookup"><span data-stu-id="1a962-178">cancelledpage</span></span>

<span data-ttu-id="1a962-179">Consente di specificare la pagina HTML sul lato server da visualizzare prima della chiusura della procedura guidata quando l'utente fa clic sul pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="1a962-179">Specifies the server-side HTML page to display before the wizard is closed when the user clicks the **Cancel** button.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-180">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-180">Syntax</span></span>


```
<cancelledpage
    href = "string"
>
<!-- child elements -->
</cancelledpage>                  
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-181">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-181">Attributes</span></span>



| <span data-ttu-id="1a962-182">Attributo</span><span class="sxs-lookup"><span data-stu-id="1a962-182">Attribute</span></span> | <span data-ttu-id="1a962-183">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a962-183">Description</span></span>                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a962-184">href</span><span class="sxs-lookup"><span data-stu-id="1a962-184">href</span></span>      | <span data-ttu-id="1a962-185">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-185">Required.</span></span> <span data-ttu-id="1a962-186">URL della pagina HTML sul lato server da visualizzare quando l'utente fa clic sul pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="1a962-186">The URL of the server-side HTML page to display when the user clicks the **Cancel** button.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1a962-187">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-187">Element Information</span></span>



| <span data-ttu-id="1a962-188">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-188">Parent Element</span></span>        | <span data-ttu-id="1a962-189">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-189">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="1a962-190">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="1a962-190">uploadinfo</span></span>](#syntax) | <span data-ttu-id="1a962-191">nessuno</span><span class="sxs-lookup"><span data-stu-id="1a962-191">None</span></span>           |



 

## <a name="failurepage"></a><span data-ttu-id="1a962-192">failurepage</span><span class="sxs-lookup"><span data-stu-id="1a962-192">failurepage</span></span>

<span data-ttu-id="1a962-193">Specifica la pagina HTML sul lato server da visualizzare se il caricamento non riesce.</span><span class="sxs-lookup"><span data-stu-id="1a962-193">Specifies the server-side HTML page to display if the upload is not successful.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-194">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-194">Syntax</span></span>


```
<failurepage
    href = "string"
>
<!-- child elements -->
</failurepage>                    
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-195">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-195">Attributes</span></span>



| <span data-ttu-id="1a962-196">Attributo</span><span class="sxs-lookup"><span data-stu-id="1a962-196">Attribute</span></span> | <span data-ttu-id="1a962-197">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a962-197">Description</span></span>                                                                                |
|-----------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a962-198">href</span><span class="sxs-lookup"><span data-stu-id="1a962-198">href</span></span>      | <span data-ttu-id="1a962-199">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-199">Required.</span></span> <span data-ttu-id="1a962-200">URL della pagina HTML sul lato server da visualizzare se il caricamento non riesce.</span><span class="sxs-lookup"><span data-stu-id="1a962-200">The URL of the server-side HTML page to display if the upload is not successful.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1a962-201">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-201">Element Information</span></span>



| <span data-ttu-id="1a962-202">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-202">Parent Element</span></span>        | <span data-ttu-id="1a962-203">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-203">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="1a962-204">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="1a962-204">uploadinfo</span></span>](#syntax) | <span data-ttu-id="1a962-205">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="1a962-205">None.</span></span> <span data-ttu-id="1a962-206">Testo consentito.</span><span class="sxs-lookup"><span data-stu-id="1a962-206">Text is allowed.</span></span> |



 

## <a name="favorite"></a><span data-ttu-id="1a962-207">preferito</span><span class="sxs-lookup"><span data-stu-id="1a962-207">favorite</span></span>

<span data-ttu-id="1a962-208">Indica alla procedura guidata di creare una voce di sito Web preferita dal menu **Preferiti** per l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="1a962-208">Instructs the wizard to create a favorite website entry in the **Favorites** menu for the given URL.</span></span> <span data-ttu-id="1a962-209">Se questo elemento non viene specificato, l'elemento [htmlui](#syntax) viene usato al suo posto.</span><span class="sxs-lookup"><span data-stu-id="1a962-209">If this element is not specified, then the [htmlui](#syntax) element is used in its place.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-210">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-210">Syntax</span></span>


```
<favorite
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</favorite>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-211">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-211">Attributes</span></span>



| <span data-ttu-id="1a962-212">Attributo</span><span class="sxs-lookup"><span data-stu-id="1a962-212">Attribute</span></span> | <span data-ttu-id="1a962-213">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a962-213">Description</span></span>                                                            |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="1a962-214">comment</span><span class="sxs-lookup"><span data-stu-id="1a962-214">comment</span></span>   | <span data-ttu-id="1a962-215">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-215">Required.</span></span> <span data-ttu-id="1a962-216">Commento associato alla voce **Preferiti** .</span><span class="sxs-lookup"><span data-stu-id="1a962-216">The comment associated with the **Favorites** entry.</span></span>         |
| <span data-ttu-id="1a962-217">href</span><span class="sxs-lookup"><span data-stu-id="1a962-217">href</span></span>      | <span data-ttu-id="1a962-218">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-218">Required.</span></span> <span data-ttu-id="1a962-219">URL della voce **Preferiti** .</span><span class="sxs-lookup"><span data-stu-id="1a962-219">The URL of the **Favorites** entry.</span></span>                          |
| <span data-ttu-id="1a962-220">name</span><span class="sxs-lookup"><span data-stu-id="1a962-220">name</span></span>      | <span data-ttu-id="1a962-221">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-221">Required.</span></span> <span data-ttu-id="1a962-222">Nome dell'URL visualizzato nel menu **Preferiti** .</span><span class="sxs-lookup"><span data-stu-id="1a962-222">The name for the URL that appears in the **Favorites** menu.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1a962-223">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-223">Element Information</span></span>



| <span data-ttu-id="1a962-224">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-224">Parent Element</span></span>        | <span data-ttu-id="1a962-225">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-225">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="1a962-226">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="1a962-226">uploadinfo</span></span>](#syntax) | <span data-ttu-id="1a962-227">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="1a962-227">None.</span></span> <span data-ttu-id="1a962-228">Testo consentito.</span><span class="sxs-lookup"><span data-stu-id="1a962-228">Text is allowed.</span></span> |



 

## <a name="file"></a><span data-ttu-id="1a962-229">file</span><span class="sxs-lookup"><span data-stu-id="1a962-229">file</span></span>

<span data-ttu-id="1a962-230">Descrive un singolo file da copiare.</span><span class="sxs-lookup"><span data-stu-id="1a962-230">Describes a single file to be copied.</span></span> <span data-ttu-id="1a962-231">È possibile che più elementi [file](#syntax) siano contenuti in un singolo nodo di [file](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="1a962-231">Multiple [file](#syntax) elements may be contained under a single [filelist](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-232">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-232">Syntax</span></span>


```
<file
    contenttype = "string"
    destination = "string"
    extension = "string"
    id = "string"
    size = "string"
    source = "string"
>
<!-- child elements -->
</file>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-233">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-233">Attributes</span></span>



| <span data-ttu-id="1a962-234">Attributo</span><span class="sxs-lookup"><span data-stu-id="1a962-234">Attribute</span></span>   | <span data-ttu-id="1a962-235">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a962-235">Description</span></span>                                                                                                                                                                  |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a962-236">ContentType</span><span class="sxs-lookup"><span data-stu-id="1a962-236">contenttype</span></span> | <span data-ttu-id="1a962-237">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1a962-237">Optional.</span></span> <span data-ttu-id="1a962-238">Tipo MIME del file.</span><span class="sxs-lookup"><span data-stu-id="1a962-238">The MIME type of the file.</span></span>                                                                                                                                         |
| <span data-ttu-id="1a962-239">destination</span><span class="sxs-lookup"><span data-stu-id="1a962-239">destination</span></span> | <span data-ttu-id="1a962-240">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-240">Required.</span></span> <span data-ttu-id="1a962-241">Percorso suggerito per il file dopo che è stato caricato.</span><span class="sxs-lookup"><span data-stu-id="1a962-241">A suggested path for the file once it is uploaded.</span></span> <span data-ttu-id="1a962-242">Questo percorso è relativo all'URL di destinazione del sito di caricamento.</span><span class="sxs-lookup"><span data-stu-id="1a962-242">This path is relative to the upload site's destination URL.</span></span> <span data-ttu-id="1a962-243">Il sito di caricamento può modificare questo valore se necessario.</span><span class="sxs-lookup"><span data-stu-id="1a962-243">The upload site can modify this value as necessary.</span></span> |
| <span data-ttu-id="1a962-244">estensione</span><span class="sxs-lookup"><span data-stu-id="1a962-244">extension</span></span>   | <span data-ttu-id="1a962-245">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1a962-245">Optional.</span></span> <span data-ttu-id="1a962-246">Estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="1a962-246">The file name extension of the file.</span></span>                                                                                                                               |
| <span data-ttu-id="1a962-247">id</span><span class="sxs-lookup"><span data-stu-id="1a962-247">id</span></span>          | <span data-ttu-id="1a962-248">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-248">Required.</span></span> <span data-ttu-id="1a962-249">Indice numerico del file.</span><span class="sxs-lookup"><span data-stu-id="1a962-249">The numerical index of the file.</span></span>                                                                                                                                   |
| <span data-ttu-id="1a962-250">size</span><span class="sxs-lookup"><span data-stu-id="1a962-250">size</span></span>        | <span data-ttu-id="1a962-251">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1a962-251">Optional.</span></span> <span data-ttu-id="1a962-252">Dimensioni, in byte, del file.</span><span class="sxs-lookup"><span data-stu-id="1a962-252">The size of the file, in bytes.</span></span>                                                                                                                                    |
| <span data-ttu-id="1a962-253">source</span><span class="sxs-lookup"><span data-stu-id="1a962-253">source</span></span>      | <span data-ttu-id="1a962-254">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-254">Required.</span></span> <span data-ttu-id="1a962-255">Percorso file system completo per il file.</span><span class="sxs-lookup"><span data-stu-id="1a962-255">The full file system path for the file.</span></span>                                                                                                                            |



 

### <a name="element-information"></a><span data-ttu-id="1a962-256">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-256">Element Information</span></span>



| <span data-ttu-id="1a962-257">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-257">Parent Element</span></span>      | <span data-ttu-id="1a962-258">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-258">Child Elements</span></span>                                          |
|---------------------|---------------------------------------------------------|
| [<span data-ttu-id="1a962-259">filelist</span><span class="sxs-lookup"><span data-stu-id="1a962-259">filelist</span></span>](#syntax) | <span data-ttu-id="1a962-260">[metadati](#syntax), [post](#syntax), [ridimensionamento](#syntax)</span><span class="sxs-lookup"><span data-stu-id="1a962-260">[metadata](#syntax), [post](#syntax), [resize](#syntax)</span></span> |



 

## <a name="filelist"></a><span data-ttu-id="1a962-261">filelist</span><span class="sxs-lookup"><span data-stu-id="1a962-261">filelist</span></span>

<span data-ttu-id="1a962-262">Contenitore per gli elementi che descrivono i file da copiare.</span><span class="sxs-lookup"><span data-stu-id="1a962-262">A container for elements describing the files to be copied.</span></span> <span data-ttu-id="1a962-263">È possibile [che più elementi](#syntax) FileDirectory siano contenuti in un singolo nodo [transfermanifest](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="1a962-263">Multiple [filelist](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-264">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-264">Syntax</span></span>


```
<filelist
    usesfolders = "1"
>
<!-- child elements -->
</filelist>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-265">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-265">Attributes</span></span>



| <span data-ttu-id="1a962-266">Attributo</span><span class="sxs-lookup"><span data-stu-id="1a962-266">Attribute</span></span>   | <span data-ttu-id="1a962-267">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a962-267">Description</span></span>      |
|-------------|------------------|
| <span data-ttu-id="1a962-268">usesfolders</span><span class="sxs-lookup"><span data-stu-id="1a962-268">usesfolders</span></span> | <span data-ttu-id="1a962-269">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="1a962-269">Not implemented.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1a962-270">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-270">Element Information</span></span>



| <span data-ttu-id="1a962-271">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-271">Parent Element</span></span>              | <span data-ttu-id="1a962-272">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-272">Child Elements</span></span>  |
|-----------------------------|-----------------|
| [<span data-ttu-id="1a962-273">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="1a962-273">transfermanifest</span></span>](#syntax) | [<span data-ttu-id="1a962-274">file</span><span class="sxs-lookup"><span data-stu-id="1a962-274">file</span></span>](#syntax) |



 

## <a name="folder"></a><span data-ttu-id="1a962-275">folder</span><span class="sxs-lookup"><span data-stu-id="1a962-275">folder</span></span>

<span data-ttu-id="1a962-276">Descrive la cartella in cui sono archiviati i file.</span><span class="sxs-lookup"><span data-stu-id="1a962-276">Describes a folder in which files are stored.</span></span> <span data-ttu-id="1a962-277">È possibile che più elementi [cartella](#syntax) siano contenuti in un singolo nodo di [cartelle](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="1a962-277">Multiple [folder](#syntax) elements may be contained under a single [folderlist](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-278">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-278">Syntax</span></span>


```
<folder
    destination = "string"
>
<!-- child elements -->
</folder>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-279">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-279">Attributes</span></span>



| <span data-ttu-id="1a962-280">Attributo</span><span class="sxs-lookup"><span data-stu-id="1a962-280">Attribute</span></span>   | <span data-ttu-id="1a962-281">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a962-281">Description</span></span>                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a962-282">destination</span><span class="sxs-lookup"><span data-stu-id="1a962-282">destination</span></span> | <span data-ttu-id="1a962-283">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-283">Required.</span></span> <span data-ttu-id="1a962-284">Percorso suggerito per la cartella dopo il caricamento.</span><span class="sxs-lookup"><span data-stu-id="1a962-284">A suggested path for the folder once it is uploaded.</span></span> <span data-ttu-id="1a962-285">Questo percorso è relativo all'URL di destinazione del sito di caricamento.</span><span class="sxs-lookup"><span data-stu-id="1a962-285">This path is relative to the upload site's destination URL.</span></span> <span data-ttu-id="1a962-286">Il sito di caricamento può modificare questo valore se necessario.</span><span class="sxs-lookup"><span data-stu-id="1a962-286">The upload site can modify this value as necessary.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1a962-287">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-287">Element Information</span></span>



| <span data-ttu-id="1a962-288">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-288">Parent Element</span></span>        | <span data-ttu-id="1a962-289">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-289">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="1a962-290">cartella</span><span class="sxs-lookup"><span data-stu-id="1a962-290">folderlist</span></span>](#syntax) | <span data-ttu-id="1a962-291">nessuno</span><span class="sxs-lookup"><span data-stu-id="1a962-291">None</span></span>           |



 

## <a name="folderlist"></a><span data-ttu-id="1a962-292">cartella</span><span class="sxs-lookup"><span data-stu-id="1a962-292">folderlist</span></span>

<span data-ttu-id="1a962-293">Contenitore per gli elementi che descrivono i file da copiare.</span><span class="sxs-lookup"><span data-stu-id="1a962-293">A container for elements describing the files to be copied.</span></span> <span data-ttu-id="1a962-294">Più elementi [cartella](#syntax) possono essere contenuti in un singolo nodo [transfermanifest](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="1a962-294">Multiple [folderlist](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-295">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-295">Syntax</span></span>


```
<folderlist>
<!-- child elements -->
</folderlist>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-296">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-296">Attributes</span></span>

<span data-ttu-id="1a962-297">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="1a962-297">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="1a962-298">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-298">Element Information</span></span>



| <span data-ttu-id="1a962-299">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-299">Parent Element</span></span>              | <span data-ttu-id="1a962-300">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-300">Child Elements</span></span>    |
|-----------------------------|-------------------|
| [<span data-ttu-id="1a962-301">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="1a962-301">transfermanifest</span></span>](#syntax) | [<span data-ttu-id="1a962-302">cartella</span><span class="sxs-lookup"><span data-stu-id="1a962-302">folder</span></span>](#syntax) |



 

## <a name="formdata"></a><span data-ttu-id="1a962-303">FormData</span><span class="sxs-lookup"><span data-stu-id="1a962-303">formdata</span></span>

<span data-ttu-id="1a962-304">Descrive i dati facoltativi del modulo codificato HTML che possono essere trasferiti con i file.</span><span class="sxs-lookup"><span data-stu-id="1a962-304">Describes optional HTML encoded form data that may be transferred with the files.</span></span> <span data-ttu-id="1a962-305">Questo elemento viene aggiunto dal servizio se sceglie di caricare i file come post multiparte.</span><span class="sxs-lookup"><span data-stu-id="1a962-305">This element is added by the service if it elects to upload the files as a multi-part post.</span></span> <span data-ttu-id="1a962-306">I dati del form, insieme alle informazioni dell'elemento [post](#syntax) , vengono usati per creare l'intestazione post.</span><span class="sxs-lookup"><span data-stu-id="1a962-306">The form data, together with information from the [post](#syntax) element, is used to create the post header.</span></span>

<span data-ttu-id="1a962-307">Più elementi [FormData](#syntax) possono essere contenuti in un singolo nodo [uploadinfo](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="1a962-307">Multiple [formdata](#syntax) elements may be contained under a single [uploadinfo](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-308">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-308">Syntax</span></span>


```
<formdata
    name = "string"
>
<!-- child elements -->
</formdata>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-309">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-309">Attributes</span></span>



| <span data-ttu-id="1a962-310">Attributo</span><span class="sxs-lookup"><span data-stu-id="1a962-310">Attribute</span></span> | <span data-ttu-id="1a962-311">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a962-311">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1a962-312">name</span><span class="sxs-lookup"><span data-stu-id="1a962-312">name</span></span>      | <span data-ttu-id="1a962-313">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-313">Required.</span></span> <span data-ttu-id="1a962-314">Definisce il nome dati del modulo associato a questa sezione del caricamento.</span><span class="sxs-lookup"><span data-stu-id="1a962-314">Defines the form data name associated with this section of the upload.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1a962-315">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-315">Element Information</span></span>



| <span data-ttu-id="1a962-316">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-316">Parent Element</span></span>        | <span data-ttu-id="1a962-317">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-317">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="1a962-318">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="1a962-318">uploadinfo</span></span>](#syntax) | <span data-ttu-id="1a962-319">nessuno</span><span class="sxs-lookup"><span data-stu-id="1a962-319">None</span></span>           |



 

## <a name="htmlui"></a><span data-ttu-id="1a962-320">htmlui</span><span class="sxs-lookup"><span data-stu-id="1a962-320">htmlui</span></span>

<span data-ttu-id="1a962-321">URL della pagina HTML sul lato server da visualizzare quando la procedura guidata viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="1a962-321">The URL of the server-side HTML page to display when the wizard is closed.</span></span> <span data-ttu-id="1a962-322">Questo elemento crea una voce di pagina Web preferita nel menu **Preferiti** se l'elemento [preferito](#syntax) è assente e viene specificato il nome descrittivo del sito di caricamento.</span><span class="sxs-lookup"><span data-stu-id="1a962-322">This element creates a favorite webpage entry in the **Favorites** menu if the [favorite](#syntax) element is absent and the upload site's friendly name is specified.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-323">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-323">Syntax</span></span>


```
<htmlui
    href = "string"
>
<!-- child elements -->
</htmlui>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-324">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-324">Attributes</span></span>



| <span data-ttu-id="1a962-325">Attributo</span><span class="sxs-lookup"><span data-stu-id="1a962-325">Attribute</span></span> | <span data-ttu-id="1a962-326">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a962-326">Description</span></span>                                                                          |
|-----------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1a962-327">href</span><span class="sxs-lookup"><span data-stu-id="1a962-327">href</span></span>      | <span data-ttu-id="1a962-328">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-328">Required.</span></span> <span data-ttu-id="1a962-329">URL della pagina HTML sul lato server da visualizzare quando la procedura guidata viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="1a962-329">The URL of the server-side HTML page to display when the wizard is closed.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1a962-330">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-330">Element Information</span></span>



| <span data-ttu-id="1a962-331">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-331">Parent Element</span></span>        | <span data-ttu-id="1a962-332">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-332">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="1a962-333">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="1a962-333">uploadinfo</span></span>](#syntax) | <span data-ttu-id="1a962-334">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="1a962-334">None.</span></span> <span data-ttu-id="1a962-335">Testo consentito.</span><span class="sxs-lookup"><span data-stu-id="1a962-335">Text is allowed.</span></span> |



 

## <a name="imageproperty"></a><span data-ttu-id="1a962-336">imageproperty</span><span class="sxs-lookup"><span data-stu-id="1a962-336">imageproperty</span></span>

<span data-ttu-id="1a962-337">Specifica una proprietà di immagine correlata al file.</span><span class="sxs-lookup"><span data-stu-id="1a962-337">Specifies an image property relating to the file.</span></span> <span data-ttu-id="1a962-338">Più elementi [ImageProperty](#syntax) possono essere contenuti in un singolo nodo di [metadati](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="1a962-338">Multiple [imageproperty](#syntax) elements may be contained under a single [metadata](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-339">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-339">Syntax</span></span>


```
<imageproperty
    id = "string"
>
<!-- child elements -->
</imageproperty>                  
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-340">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-340">Attributes</span></span>



| <span data-ttu-id="1a962-341">Attributo</span><span class="sxs-lookup"><span data-stu-id="1a962-341">Attribute</span></span> | <span data-ttu-id="1a962-342">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a962-342">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="1a962-343">id</span><span class="sxs-lookup"><span data-stu-id="1a962-343">id</span></span>        | <span data-ttu-id="1a962-344">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-344">Required.</span></span> <span data-ttu-id="1a962-345">ID della proprietà specifica.</span><span class="sxs-lookup"><span data-stu-id="1a962-345">The ID of the particular property.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1a962-346">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-346">Element Information</span></span>



| <span data-ttu-id="1a962-347">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-347">Parent Element</span></span>      | <span data-ttu-id="1a962-348">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-348">Child Elements</span></span>         |
|---------------------|------------------------|
| [<span data-ttu-id="1a962-349">metadati</span><span class="sxs-lookup"><span data-stu-id="1a962-349">metadata</span></span>](#syntax) | <span data-ttu-id="1a962-350">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="1a962-350">None.</span></span> <span data-ttu-id="1a962-351">Testo consentito.</span><span class="sxs-lookup"><span data-stu-id="1a962-351">Text is allowed.</span></span> |



 

## <a name="metadata"></a><span data-ttu-id="1a962-352">metadata</span><span class="sxs-lookup"><span data-stu-id="1a962-352">metadata</span></span>

<span data-ttu-id="1a962-353">Contenitore per elementi e testo che definisce i metadati per il file specifico.</span><span class="sxs-lookup"><span data-stu-id="1a962-353">A container for elements and text defining metadata for the particular file.</span></span> <span data-ttu-id="1a962-354">Più elementi di [metadati](#syntax) possono essere contenuti in un singolo nodo di [file](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="1a962-354">Multiple [metadata](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-355">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-355">Syntax</span></span>


```
<metadata>
<!-- child elements -->
</metadata>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-356">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-356">Attributes</span></span>

<span data-ttu-id="1a962-357">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="1a962-357">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="1a962-358">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-358">Element Information</span></span>



| <span data-ttu-id="1a962-359">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-359">Parent Element</span></span>  | <span data-ttu-id="1a962-360">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-360">Child Elements</span></span>           |
|-----------------|--------------------------|
| [<span data-ttu-id="1a962-361">file</span><span class="sxs-lookup"><span data-stu-id="1a962-361">file</span></span>](#syntax) | [<span data-ttu-id="1a962-362">imageproperty</span><span class="sxs-lookup"><span data-stu-id="1a962-362">imageproperty</span></span>](#syntax) |



 

## <a name="netplace"></a><span data-ttu-id="1a962-363">netplace</span><span class="sxs-lookup"><span data-stu-id="1a962-363">netplace</span></span>

<span data-ttu-id="1a962-364">Definisce la destinazione di una posizione di rete creata nella **rete** quando il caricamento è completo.</span><span class="sxs-lookup"><span data-stu-id="1a962-364">Defines the target for a network place that is created in **My Network Places** when the upload is complete.</span></span> <span data-ttu-id="1a962-365">La creazione di una posizione di rete può essere impedita tramite il metodo [**IPublishingWizard:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) .</span><span class="sxs-lookup"><span data-stu-id="1a962-365">Creation of a network place can be prevented through the [**IPublishingWizard::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) method.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-366">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-366">Syntax</span></span>


```
<netplace
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</netplace>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-367">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-367">Attributes</span></span>



| <span data-ttu-id="1a962-368">Attributo</span><span class="sxs-lookup"><span data-stu-id="1a962-368">Attribute</span></span> | <span data-ttu-id="1a962-369">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a962-369">Description</span></span>                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a962-370">comment</span><span class="sxs-lookup"><span data-stu-id="1a962-370">comment</span></span>   | <span data-ttu-id="1a962-371">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-371">Required.</span></span> <span data-ttu-id="1a962-372">Commento visualizzato per l'icona del punto di rete quando il cursore si trova su di esso.</span><span class="sxs-lookup"><span data-stu-id="1a962-372">The comment displayed for the network place icon when the cursor rests on it.</span></span>         |
| <span data-ttu-id="1a962-373">href</span><span class="sxs-lookup"><span data-stu-id="1a962-373">href</span></span>      | <span data-ttu-id="1a962-374">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-374">Required.</span></span> <span data-ttu-id="1a962-375">URL della voce del punto di rete.</span><span class="sxs-lookup"><span data-stu-id="1a962-375">The URL of the network place entry.</span></span>                                                   |
| <span data-ttu-id="1a962-376">name</span><span class="sxs-lookup"><span data-stu-id="1a962-376">name</span></span>      | <span data-ttu-id="1a962-377">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-377">Required.</span></span> <span data-ttu-id="1a962-378">Nome dell'icona del punto di rete visualizzato nella cartella **risorse di rete** .</span><span class="sxs-lookup"><span data-stu-id="1a962-378">The name for the network place icon that appears in the **My Network Places** folder.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1a962-379">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-379">Element Information</span></span>



| <span data-ttu-id="1a962-380">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-380">Parent Element</span></span>        | <span data-ttu-id="1a962-381">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-381">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="1a962-382">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="1a962-382">uploadinfo</span></span>](#syntax) | <span data-ttu-id="1a962-383">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="1a962-383">None.</span></span> <span data-ttu-id="1a962-384">Testo consentito.</span><span class="sxs-lookup"><span data-stu-id="1a962-384">Text is allowed.</span></span> |



 

## <a name="post"></a><span data-ttu-id="1a962-385">post</span><span class="sxs-lookup"><span data-stu-id="1a962-385">post</span></span>

<span data-ttu-id="1a962-386">URL a cui deve essere inviato il file.</span><span class="sxs-lookup"><span data-stu-id="1a962-386">URL to which the file should be posted.</span></span> <span data-ttu-id="1a962-387">Questo elemento viene aggiunto dal servizio quando il trasferimento viene eseguito come post multiparte e, con [FormData](#syntax), viene usato per compilare l'intestazione post.</span><span class="sxs-lookup"><span data-stu-id="1a962-387">This element is added by the service when the transfer is done as a multi-part post and, with [formdata](#syntax), is used to build the post header.</span></span> <span data-ttu-id="1a962-388">Se il servizio sceglie di eseguire il trasferimento di file utilizzando World Wide Web Distributed Authoring and Versioning (WebDAV), non dovrebbe aggiungere questo elemento.</span><span class="sxs-lookup"><span data-stu-id="1a962-388">If the service chooses to perform the file transfer using World Wide Web Distributed Authoring and Versioning (WebDAV), it should not add this element.</span></span> <span data-ttu-id="1a962-389">È possibile che più elementi [post](#syntax) siano contenuti in un singolo nodo di [file](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="1a962-389">Multiple [post](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-390">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-390">Syntax</span></span>


```
<post
    filename = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</post>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-391">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-391">Attributes</span></span>



| <span data-ttu-id="1a962-392">Attributo</span><span class="sxs-lookup"><span data-stu-id="1a962-392">Attribute</span></span> | <span data-ttu-id="1a962-393">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a962-393">Description</span></span>                                                                    |
|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1a962-394">nomefile</span><span class="sxs-lookup"><span data-stu-id="1a962-394">filename</span></span>  | <span data-ttu-id="1a962-395">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1a962-395">Optional.</span></span> <span data-ttu-id="1a962-396">Nome del file inviato.</span><span class="sxs-lookup"><span data-stu-id="1a962-396">The file name for the posted file.</span></span>                                   |
| <span data-ttu-id="1a962-397">href</span><span class="sxs-lookup"><span data-stu-id="1a962-397">href</span></span>      | <span data-ttu-id="1a962-398">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-398">Required.</span></span> <span data-ttu-id="1a962-399">URL della cartella di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1a962-399">The URL of the destination folder.</span></span>                                   |
| <span data-ttu-id="1a962-400">name</span><span class="sxs-lookup"><span data-stu-id="1a962-400">name</span></span>      | <span data-ttu-id="1a962-401">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-401">Required.</span></span> <span data-ttu-id="1a962-402">Definisce il nome dati del modulo associato a questa sezione del post.</span><span class="sxs-lookup"><span data-stu-id="1a962-402">Defines the form data name associated with this section of the post.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1a962-403">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-403">Element Information</span></span>



| <span data-ttu-id="1a962-404">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-404">Parent Element</span></span>  | <span data-ttu-id="1a962-405">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-405">Child Elements</span></span>      |
|-----------------|---------------------|
| [<span data-ttu-id="1a962-406">file</span><span class="sxs-lookup"><span data-stu-id="1a962-406">file</span></span>](#syntax) | [<span data-ttu-id="1a962-407">FormData</span><span class="sxs-lookup"><span data-stu-id="1a962-407">formdata</span></span>](#syntax) |



 

## <a name="resize"></a><span data-ttu-id="1a962-408">resize</span><span class="sxs-lookup"><span data-stu-id="1a962-408">resize</span></span>

<span data-ttu-id="1a962-409">Definisce il ridimensionamento e la ricompressione di un file di immagine nel formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="1a962-409">Defines the scaling and recompression of an image file into JPEG format.</span></span> <span data-ttu-id="1a962-410">Se il file di origine è già in formato JPEG ed è minore o uguale alla larghezza e all'altezza specificate, non viene ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="1a962-410">If the source file is already in JPEG format and is less than or equal to the specified width and height, it is not sized.</span></span> <span data-ttu-id="1a962-411">Se il file di origine non è un file JPEG, viene convertito.</span><span class="sxs-lookup"><span data-stu-id="1a962-411">If the source file is not a JPEG file, it is converted.</span></span> <span data-ttu-id="1a962-412">È possibile impedire il ridimensionamento, la ricompressione e la conversione del file tramite il metodo [**IPublishingWizard:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) .</span><span class="sxs-lookup"><span data-stu-id="1a962-412">Scaling, recompression, and conversion of the file can be prevented through the [**IPublishingWizard::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) method.</span></span> <span data-ttu-id="1a962-413">Più elementi di [ridimensionamento](#syntax) possono essere contenuti in un singolo nodo di [file](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="1a962-413">Multiple [resize](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-414">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-414">Syntax</span></span>


```
<resize
    cx = "string"
    cy = "string"
    quality = "string"
>
<!-- child elements -->
</resize>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-415">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-415">Attributes</span></span>



| <span data-ttu-id="1a962-416">Attributo</span><span class="sxs-lookup"><span data-stu-id="1a962-416">Attribute</span></span> | <span data-ttu-id="1a962-417">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a962-417">Description</span></span>                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a962-418">CX</span><span class="sxs-lookup"><span data-stu-id="1a962-418">cx</span></span>        | <span data-ttu-id="1a962-419">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-419">Required.</span></span> <span data-ttu-id="1a962-420">Larghezza dell'immagine, in pixel, dopo il caricamento.</span><span class="sxs-lookup"><span data-stu-id="1a962-420">The width of the image, in pixels, after uploading.</span></span> <span data-ttu-id="1a962-421">Se questo valore è 0, **CX** viene calcolato dal valore **CY** per mantenere le dimensioni relative.</span><span class="sxs-lookup"><span data-stu-id="1a962-421">If this value is 0, then **cx** is calculated from the **cy** value to preserve relative dimensions.</span></span>  |
| <span data-ttu-id="1a962-422">cy</span><span class="sxs-lookup"><span data-stu-id="1a962-422">cy</span></span>        | <span data-ttu-id="1a962-423">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-423">Required.</span></span> <span data-ttu-id="1a962-424">Altezza dell'immagine, in pixel, dopo il caricamento.</span><span class="sxs-lookup"><span data-stu-id="1a962-424">The height of the image, in pixels, after uploading.</span></span> <span data-ttu-id="1a962-425">Se questo valore è 0, **CY** viene calcolato dal valore **CX** per mantenere le dimensioni relative.</span><span class="sxs-lookup"><span data-stu-id="1a962-425">If this value is 0, then **cy** is calculated from the **cx** value to preserve relative dimensions.</span></span> |
| <span data-ttu-id="1a962-426">qualità</span><span class="sxs-lookup"><span data-stu-id="1a962-426">quality</span></span>   | <span data-ttu-id="1a962-427">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-427">Required.</span></span> <span data-ttu-id="1a962-428">Il valore di qualità JPEG, compreso tra 0 e 100, 100 è la qualità più elevata.</span><span class="sxs-lookup"><span data-stu-id="1a962-428">The JPEG quality value, between 0 and 100, with 100 being the highest quality.</span></span>                                                                            |



 

### <a name="element-information"></a><span data-ttu-id="1a962-429">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-429">Element Information</span></span>



| <span data-ttu-id="1a962-430">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-430">Parent Element</span></span>  | <span data-ttu-id="1a962-431">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-431">Child Elements</span></span> |
|-----------------|----------------|
| [<span data-ttu-id="1a962-432">file</span><span class="sxs-lookup"><span data-stu-id="1a962-432">file</span></span>](#syntax) | <span data-ttu-id="1a962-433">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="1a962-433">None.</span></span>          |



 

## <a name="successpage"></a><span data-ttu-id="1a962-434">successpage</span><span class="sxs-lookup"><span data-stu-id="1a962-434">successpage</span></span>

<span data-ttu-id="1a962-435">Specifica la pagina HTML sul lato server da visualizzare se il caricamento ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1a962-435">Specifies the server-side HTML page to display if the upload is successful.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-436">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-436">Syntax</span></span>


```
<successpage
    href = "string"
>
<!-- child elements -->
</successpage>                    
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-437">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-437">Attributes</span></span>



| <span data-ttu-id="1a962-438">Attributo</span><span class="sxs-lookup"><span data-stu-id="1a962-438">Attribute</span></span> | <span data-ttu-id="1a962-439">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a962-439">Description</span></span>                                                                            |
|-----------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a962-440">href</span><span class="sxs-lookup"><span data-stu-id="1a962-440">href</span></span>      | <span data-ttu-id="1a962-441">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-441">Required.</span></span> <span data-ttu-id="1a962-442">URL della pagina HTML sul lato server da visualizzare se il caricamento ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1a962-442">The URL of the server-side HTML page to display if the upload is successful.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1a962-443">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-443">Element Information</span></span>



| <span data-ttu-id="1a962-444">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-444">Parent Element</span></span>        | <span data-ttu-id="1a962-445">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-445">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="1a962-446">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="1a962-446">uploadinfo</span></span>](#syntax) | <span data-ttu-id="1a962-447">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="1a962-447">None.</span></span> <span data-ttu-id="1a962-448">Testo consentito.</span><span class="sxs-lookup"><span data-stu-id="1a962-448">Text is allowed.</span></span> |



 

## <a name="target"></a><span data-ttu-id="1a962-449">target</span><span class="sxs-lookup"><span data-stu-id="1a962-449">target</span></span>

<span data-ttu-id="1a962-450">Cartella di destinazione specificata in formato Universal Naming Convention (UNC) o come server WebDAV.</span><span class="sxs-lookup"><span data-stu-id="1a962-450">A destination folder specified in Universal Naming Convention (UNC) format or as a WebDAV server.</span></span> <span data-ttu-id="1a962-451">Il servizio aggiunge questa destinazione per specificare una cartella di destinazione se il trasferimento usa un protocollo WebDAV o file system.</span><span class="sxs-lookup"><span data-stu-id="1a962-451">The service adds this target to specify a destination folder if the transfer uses a WebDAV or file system protocol.</span></span> <span data-ttu-id="1a962-452">Se il servizio sceglie di eseguire il trasferimento di file come post multiparte, non dovrebbe aggiungere questo elemento.</span><span class="sxs-lookup"><span data-stu-id="1a962-452">If the service chooses to perform the file transfer as a multi-part post, it should not add this element.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-453">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-453">Syntax</span></span>


```
<target
    href = "string"
>
<!-- child elements -->
</target>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-454">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-454">Attributes</span></span>



| <span data-ttu-id="1a962-455">Attributo</span><span class="sxs-lookup"><span data-stu-id="1a962-455">Attribute</span></span> | <span data-ttu-id="1a962-456">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a962-456">Description</span></span>                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a962-457">href</span><span class="sxs-lookup"><span data-stu-id="1a962-457">href</span></span>      | <span data-ttu-id="1a962-458">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-458">Required.</span></span> <span data-ttu-id="1a962-459">URL della cartella di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1a962-459">The URL of the destination folder.</span></span> <span data-ttu-id="1a962-460">Usare il modulo **https://** per WebDAV o il modulo **\\ \\ \\ condivisione server** per UNC.</span><span class="sxs-lookup"><span data-stu-id="1a962-460">Use the **https://** form for WebDAV or the **\\\\server\\share** form for UNC.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1a962-461">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-461">Element Information</span></span>



| <span data-ttu-id="1a962-462">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-462">Parent Element</span></span>        | <span data-ttu-id="1a962-463">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-463">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="1a962-464">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="1a962-464">uploadinfo</span></span>](#syntax) | <span data-ttu-id="1a962-465">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="1a962-465">None.</span></span> <span data-ttu-id="1a962-466">Testo consentito.</span><span class="sxs-lookup"><span data-stu-id="1a962-466">Text is allowed.</span></span> |



 

## <a name="transfermanifest"></a><span data-ttu-id="1a962-467">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="1a962-467">transfermanifest</span></span>

<span data-ttu-id="1a962-468">Nodo padre del file manifesto di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="1a962-468">The parent node of the transfer manifest file.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-469">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-469">Syntax</span></span>


```
<transfermanifest>
<!-- child elements -->
</transfermanifest>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-470">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-470">Attributes</span></span>

<span data-ttu-id="1a962-471">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="1a962-471">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="1a962-472">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-472">Element Information</span></span>



| <span data-ttu-id="1a962-473">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-473">Parent Element</span></span> | <span data-ttu-id="1a962-474">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-474">Child Elements</span></span>                                                    |
|----------------|-------------------------------------------------------------------|
| <span data-ttu-id="1a962-475">nessuno</span><span class="sxs-lookup"><span data-stu-id="1a962-475">None</span></span>           | <span data-ttu-id="1a962-476">[filefile](#syntax), [](#syntax) [fileuploadinfo](#syntax)</span><span class="sxs-lookup"><span data-stu-id="1a962-476">[filelist](#syntax), [folderlist](#syntax), [uploadinfo](#syntax)</span></span> |



 

## <a name="uploadinfo"></a><span data-ttu-id="1a962-477">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="1a962-477">uploadinfo</span></span>

<span data-ttu-id="1a962-478">Contenitore per gli elementi che forniscono informazioni dal sito di caricamento utilizzato nella transazione.</span><span class="sxs-lookup"><span data-stu-id="1a962-478">A container for elements providing information from the upload site used in the transaction.</span></span> <span data-ttu-id="1a962-479">Più elementi [uploadinfo](#syntax) possono essere contenuti in un singolo nodo [transfermanifest](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="1a962-479">Multiple [uploadinfo](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="1a962-480">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a962-480">Syntax</span></span>


```
<uploadinfo
    friendlyname = "string"
>
<!-- child elements -->
</uploadinfo>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="1a962-481">Attributi</span><span class="sxs-lookup"><span data-stu-id="1a962-481">Attributes</span></span>



| <span data-ttu-id="1a962-482">Attributo</span><span class="sxs-lookup"><span data-stu-id="1a962-482">Attribute</span></span>    | <span data-ttu-id="1a962-483">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a962-483">Description</span></span>                                                                 |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="1a962-484">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1a962-484">friendlyname</span></span> | <span data-ttu-id="1a962-485">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a962-485">Required.</span></span> <span data-ttu-id="1a962-486">Nome descrittivo per il sito Web visualizzato nella procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="1a962-486">A friendly name for the website which is displayed in the wizard.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="1a962-487">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1a962-487">Element Information</span></span>



| <span data-ttu-id="1a962-488">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1a962-488">Parent Element</span></span>              | <span data-ttu-id="1a962-489">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1a962-489">Child Elements</span></span>                                                                                                                                           |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a962-490">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="1a962-490">transfermanifest</span></span>](#syntax) | <span data-ttu-id="1a962-491">[cancelledpage](#syntax), [failurepage](#syntax), [Preferiti](#syntax), [htmlui](#syntax), [netplace](#syntax), [successpage](#syntax), [target](#syntax)</span><span class="sxs-lookup"><span data-stu-id="1a962-491">[cancelledpage](#syntax), [failurepage](#syntax), [favorite](#syntax), [htmlui](#syntax), [netplace](#syntax), [successpage](#syntax), [target](#syntax)</span></span> |



 

 

 




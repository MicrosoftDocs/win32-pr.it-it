---
description: Modifiche all'ordinamento NLS
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: Modifiche all'ordinamento NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57cfaf2a9891c2d952637429786729670fc103c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088059"
---
# <a name="nls-sorting-changes"></a><span data-ttu-id="ebc4f-103">Modifiche all'ordinamento NLS</span><span class="sxs-lookup"><span data-stu-id="ebc4f-103">NLS Sorting Changes</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="ebc4f-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="ebc4f-104">Affected Platforms</span></span>

 <span data-ttu-id="ebc4f-105">**Client** - Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="ebc4f-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="ebc4f-106">**Server** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ebc4f-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="ebc4f-107">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="ebc4f-107">Feature Impact</span></span>

 <span data-ttu-id="ebc4f-108">**Gravità** - Alta</span><span class="sxs-lookup"><span data-stu-id="ebc4f-108">**Severity** - High</span></span>  
<span data-ttu-id="ebc4f-109">**Frequenza** - Bassa (poche app sono influenzate, ma in caso di impatto, sempre interrotte)</span><span class="sxs-lookup"><span data-stu-id="ebc4f-109">**Frequency** - Low (few apps impacted, but if impacted, always broken)</span></span>  


## <a name="description"></a><span data-ttu-id="ebc4f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebc4f-110">Description</span></span>

<span data-ttu-id="ebc4f-111">Le funzioni NLS (National Language Support) consentono alle applicazioni di supportare le diverse esigenze specifiche della lingua e delle impostazioni locali degli utenti in tutto il mondo.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-111">The National Language Support (NLS) functions help applications support the different language- and locale-specific needs of users around the world.</span></span> <span data-ttu-id="ebc4f-112">Le nuove versioni di Windows includono quasi sempre modifiche NLS.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-112">New Windows versions almost invariably include NLS changes.</span></span> <span data-ttu-id="ebc4f-113">Questa modifica influisce sulle regole di confronto e sull'ordinamento e pertanto sulle applicazioni con indici persistenti.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-113">This change affects collation and sorting, and therefore applications that have persistent indexes.</span></span>

<span data-ttu-id="ebc4f-114">Una tabella delle regole di confronto include due numeri che ne identificano la versione (revisione): la versione definita e la versione NLS.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-114">A collation table has two numbers that identify its version (revision): the defined version and the NLS version.</span></span> <span data-ttu-id="ebc4f-115">Entrambe le versioni sono valori DWORD, costituiti da una versione principale e una versione secondaria.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-115">Both versions are DWORD values, composed of a major version and a minor version.</span></span> <span data-ttu-id="ebc4f-116">Il primo byte di un valore è riservato, i due byte successivi rappresentano la versione principale e l'ultimo byte rappresenta la versione secondaria.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-116">The first byte of a value is reserved, the next two bytes represent the major version, and the last byte represents the minor version.</span></span> <span data-ttu-id="ebc4f-117">In termini esadecimali, il modello è 0xRRMMMMmm, dove R è uguale a Reserved, M è uguale a major e m è uguale a minor.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-117">In hexadecimal terms, the pattern is 0xRRMMMMmm, where R equals Reserved, M equals major, and m equals minor.</span></span> <span data-ttu-id="ebc4f-118">Ad esempio, una versione principale di 3 con una versione secondaria di 4 è rappresentata come 0x304.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-118">For example, a major version of 3 with a minor version of 4 is represented as 0x304.</span></span>

<span data-ttu-id="ebc4f-119">Per una versione principale, uno o più punti di codice cambiano in modo che l'applicazione deve indicizzare nuovamente tutti i dati affinché i confronti siano validi.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-119">For a major version, one or more code points change so that the application must re-index all data for comparisons to be valid.</span></span> <span data-ttu-id="ebc4f-120">Per una versione secondaria, non viene spostato nulla, ma vengono aggiunti punti di codice.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-120">For a minor version, nothing moves, but code points are added.</span></span> <span data-ttu-id="ebc4f-121">Per questo tipo di versione, l'applicazione deve solo indicizzare nuovamente le stringhe con valori precedentemente non ordinabili.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-121">For this type of version, the application only has to re-index strings with previously unsortable values.</span></span> <span data-ttu-id="ebc4f-122">Di seguito è riepilogato il significato dei numeri di versione in relazione alle modifiche dei dati nelle tabelle delle eccezioni specifiche delle impostazioni locali e nelle tabelle predefinite:</span><span class="sxs-lookup"><span data-stu-id="ebc4f-122">In summary, here is what the version numbers mean in relation to the data changes in the locale-specific exception tables and default tables:</span></span>

<span data-ttu-id="ebc4f-123">**NLSVersion Major:** modifica dei punti di codice nelle tabelle 'exception' o specifiche delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="ebc4f-123">**NLSVersion Major** – Changed code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="ebc4f-124">**NLSVersion Minor:** sono stati aggiunti nuovi punti di codice nelle tabelle 'exception' o specifiche delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="ebc4f-124">**NLSVersion Minor** – Added new code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="ebc4f-125">**DefinedVersion Major:** modifica dei punti di codice nella tabella predefinita</span><span class="sxs-lookup"><span data-stu-id="ebc4f-125">**DefinedVersion Major** – Changed code points in the default table</span></span>  
<span data-ttu-id="ebc4f-126">**DefinedVersion Minor:** sono stati aggiunti nuovi punti di codice nella tabella predefinita</span><span class="sxs-lookup"><span data-stu-id="ebc4f-126">**DefinedVersion Minor** – Added new code points in the default table</span></span>  


<span data-ttu-id="ebc4f-127">**Ordinamento dei numeri di versione per le versioni rilasciate:**</span><span class="sxs-lookup"><span data-stu-id="ebc4f-127">**Sorting version numbers for released versions:**</span></span>



| <span data-ttu-id="ebc4f-128">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="ebc4f-128">Operating System</span></span>    | <span data-ttu-id="ebc4f-129">Versione</span><span class="sxs-lookup"><span data-stu-id="ebc4f-129">Release</span></span>           | <span data-ttu-id="ebc4f-130">Versione (0xRRMMMMmm)</span><span class="sxs-lookup"><span data-stu-id="ebc4f-130">Version (0xRRMMMMmm)</span></span>         |
|---------------------|-------------------|------------------------------|
| <span data-ttu-id="ebc4f-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ebc4f-131">Windows XP</span></span>          | <span data-ttu-id="ebc4f-132">RTM/SP1/SP2/SP3/...</span><span class="sxs-lookup"><span data-stu-id="ebc4f-132">RTM/SP1/SP2/SP3/…</span></span> | <span data-ttu-id="ebc4f-133">N/D : nessuna API GetNLSVersion()</span><span class="sxs-lookup"><span data-stu-id="ebc4f-133">N/A - no GetNLSVersion() API</span></span> |
| <span data-ttu-id="ebc4f-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ebc4f-134">Windows Server 2003</span></span> | <span data-ttu-id="ebc4f-135">RTM/SP1</span><span class="sxs-lookup"><span data-stu-id="ebc4f-135">RTM/SP1</span></span>           | <span data-ttu-id="ebc4f-136">0x00 0000 01</span><span class="sxs-lookup"><span data-stu-id="ebc4f-136">0x00 0000 01</span></span>                 |
| <span data-ttu-id="ebc4f-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebc4f-137">Windows Vista</span></span>       | <span data-ttu-id="ebc4f-138">RTM/SP1</span><span class="sxs-lookup"><span data-stu-id="ebc4f-138">RTM/SP1</span></span>           | <span data-ttu-id="ebc4f-139">0x00 0405 00</span><span class="sxs-lookup"><span data-stu-id="ebc4f-139">0x00 0405 00</span></span>                 |
| <span data-ttu-id="ebc4f-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebc4f-140">Windows Server 2008</span></span> | <span data-ttu-id="ebc4f-141">RTM</span><span class="sxs-lookup"><span data-stu-id="ebc4f-141">RTM</span></span>               | <span data-ttu-id="ebc4f-142">0x00 0501 00/0x00 5001 00</span><span class="sxs-lookup"><span data-stu-id="ebc4f-142">0x00 0501 00 / 0x00 5001 00</span></span>  |
| <span data-ttu-id="ebc4f-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ebc4f-143">Windows 7</span></span>           | <span data-ttu-id="ebc4f-144">RTM</span><span class="sxs-lookup"><span data-stu-id="ebc4f-144">RTM</span></span>               | <span data-ttu-id="ebc4f-145">0x00060100</span><span class="sxs-lookup"><span data-stu-id="ebc4f-145">0x00060100</span></span>                   |



 

## <a name="manifestation"></a><span data-ttu-id="ebc4f-146">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="ebc4f-146">Manifestation</span></span>

<span data-ttu-id="ebc4f-147">Le applicazioni (ad esempio i database) con indici permanenti che non controllano la versione NLS e ri-indicizzano in caso di modifica della versione non riusciranno a ordinare correttamente o potrebbero non fornire i risultati richiesti.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-147">Applications (such as databases) with persistent indexes that do not check the NLS version and re-index upon version change will fail to sort correctly or may fail to provide requested results.</span></span>

<span data-ttu-id="ebc4f-148">Nel caso delle interfacce utente, gli elenchi (ad esempio, alfabetico, numerico, alfanumerico, simboli e così via) possono essere ordinati in modo non corretto.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-148">In the case of user interfaces, lists (for example, alphabetical, numeric, alphanumeric, symbols, and so on) may sort incorrectly.</span></span>

## <a name="solution"></a><span data-ttu-id="ebc4f-149">Soluzione</span><span class="sxs-lookup"><span data-stu-id="ebc4f-149">Solution</span></span>

<span data-ttu-id="ebc4f-150">L'applicazione può chiamare **GetNLSVersionEx** (Windows Vista o versioni successive) o **GetNLSVersion** (prima di Windows Vista) per recuperare sia la versione definita che la versione NLS per una tabella delle regole di confronto.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-150">Your application can call either **GetNLSVersionEx** (Windows Vista or later) or **GetNLSVersion** (prior to Windows Vista) to retrieve both the defined version and the NLS version for a collation table.</span></span>

-   <span data-ttu-id="ebc4f-151">GetNLSVersionEx:</span><span class="sxs-lookup"><span data-stu-id="ebc4f-151">GetNLSVersionEx:</span></span>

<span data-ttu-id="ebc4f-152">*Recupera informazioni sulla versione corrente di una funzionalità NLS specificata per le impostazioni locali specificate in base al nome*</span><span class="sxs-lookup"><span data-stu-id="ebc4f-152">*Retrieves information about the current version of a specified NLS capability for a locale specified by name*</span></span>  
<span data-ttu-id="ebc4f-153">Questa funzione consente a un'applicazione come Active Directory di determinare se una modifica NLS influisce sulle impostazioni locali usate per una particolare tabella di indice.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-153">This function allows an application such as Active Directory to determine whether an NLS change affects the locale used for a particular index table.</span></span> <span data-ttu-id="ebc4f-154">In caso contrario, non è necessario indicizzare nuovamente la tabella.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-154">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="ebc4f-155">Per altre informazioni, vedere Gestione delle informazioni sulle impostazioni locali e sulla lingua.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-155">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="ebc4f-156">Questa funzione supporta impostazioni locali personalizzate.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-156">This function supports custom locales.</span></span> <span data-ttu-id="ebc4f-157">Se *lpLocaleName* specifica impostazioni locali supplementari, i dati recuperati sono i dati corretti per l'ordine delle regole di confronto associato alle impostazioni locali supplementari.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-157">If *lpLocaleName* specifies a supplemental locale, the data retrieved is the correct data for the collation order associated with that supplemental locale.</span></span>  

<span data-ttu-id="ebc4f-158">**Nota:** Le versioni di Windows precedenti a Windows Vista non **supportano GetNLSVersionEx.**</span><span class="sxs-lookup"><span data-stu-id="ebc4f-158">**Note:** Versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  


-   <span data-ttu-id="ebc4f-159">GetNLSVersion (da usare per le applicazioni in esecuzione in versioni di Windows precedenti a Windows Vista):</span><span class="sxs-lookup"><span data-stu-id="ebc4f-159">GetNLSVersion (use for applications running on versions of Windows prior to Windows Vista):</span></span>

<span data-ttu-id="ebc4f-160">*Recupera informazioni sulla versione corrente di una funzionalità NLS specificata per le impostazioni locali specificate dall'identificatore*</span><span class="sxs-lookup"><span data-stu-id="ebc4f-160">*Retrieves information about the current version of a specified NLS capability for a locale specified by identifier*</span></span>  
<span data-ttu-id="ebc4f-161">Questa funzione consente a un'applicazione come Active Directory di determinare se una modifica NLS influisce sull'identificatore delle impostazioni locali usato per una particolare tabella di indice.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-161">This function allows an application such as Active Directory to determine if an NLS change affects the locale identifier used for a particular index table.</span></span> <span data-ttu-id="ebc4f-162">In caso contrario, non è necessario indicizzare nuovamente la tabella.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-162">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="ebc4f-163">Per altre informazioni, vedere Gestione delle informazioni sulle impostazioni locali e sulla lingua.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-163">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="ebc4f-164">**Nota:** Questa funzione recupera informazioni solo sulle impostazioni locali specificate dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-164">**Note:** This function retrieves information only about a locale specified by identifier.</span></span> <span data-ttu-id="ebc4f-165">La **funzione GetNLSVersionEx** supporta impostazioni locali, funzionalità e nomi RFC 4646 aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-165">The **GetNLSVersionEx** function supports additional locales, features, and RFC 4646 names.</span></span> <span data-ttu-id="ebc4f-166">Tuttavia, le versioni di Windows precedenti a Windows Vista non **supportano GetNLSVersionEx.**</span><span class="sxs-lookup"><span data-stu-id="ebc4f-166">However, versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  
<span data-ttu-id="ebc4f-167">Le applicazioni destinate a essere eseguite solo in Windows Vista e versioni successive devono **usare GetNLSVersionEx** in preferenza per questa funzione.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-167">Applications meant to run only on Windows Vista and later should use **GetNLSVersionEx** in preference to this function.</span></span> <span data-ttu-id="ebc4f-168">**GetNLSVersionEx** offre un buon supporto per le impostazioni locali supplementari.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-168">**GetNLSVersionEx** provides good support for supplemental locales.</span></span>  


## <a name="compatibility-test"></a><span data-ttu-id="ebc4f-169">Test di compatibilità</span><span class="sxs-lookup"><span data-stu-id="ebc4f-169">Compatibility Test</span></span>

<span data-ttu-id="ebc4f-170">**Passaggi per determinare se una versione delle regole di confronto è stata modificata, ovvero se è necessario eseguire di nuovo l'indicizzazione:**</span><span class="sxs-lookup"><span data-stu-id="ebc4f-170">**Steps to tell if a collation version changed (that is, you need to re-index):**</span></span>

-   <span data-ttu-id="ebc4f-171">**Usare GetNLSVersionEx() per** recuperare una **struttura NLSVERSIONINFOEX** durante l'indicizzazione originale dei dati.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-171">**Use GetNLSVersionEx()** to retrieve an **NLSVERSIONINFOEX** structure when doing the original indexing of your data.</span></span>
-   <span data-ttu-id="ebc4f-172">Archiviare le proprietà seguenti con l'indice per identificare la versione:  **NLSVERSIONINFOEX.dwNLSVersion** e **NLSVERSIONINFOEX.dwDefinedVersion:** queste due proprietà insieme specificano la versione della tabella di ordinamento in uso.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-172">Store the following properties with your index to identify the version:  **NLSVERSIONINFOEX.dwNLSVersion** and **NLSVERSIONINFOEX.dwDefinedVersion** – These two properties together specify the version of the sorting table you are using.</span></span>  
    <span data-ttu-id="ebc4f-173">**NLSVERSIONINFOEX.dwEffectiveId:** specifica le impostazioni locali valide dell'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-173">**NLSVERSIONINFOEX.dwEffectiveId** - This specifies the effective locale of your sort.</span></span> <span data-ttu-id="ebc4f-174">Le impostazioni locali personalizzate puntano all'ordinamento delle impostazioni locali predefinite.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-174">A custom locale will point to an in-box locale's sort.</span></span>  
    
-   <span data-ttu-id="ebc4f-175">Quando si usa l'indice, **usare GetNlsVersionEx()** per individuare la versione dei dati.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-175">When using the index use **GetNlsVersionEx()** to discover the version of your data.</span></span>
-   <span data-ttu-id="ebc4f-176">Se una delle tre proprietà è stata modificata, i dati di ordinamento in uso potrebbero restituire risultati diversi e qualsiasi indicizzazione potrebbe non riuscire a trovare i record.</span><span class="sxs-lookup"><span data-stu-id="ebc4f-176">If any of the three properties has changed, the sorting data you are using could return different results and any indexing you have may fail to find records.</span></span>
-   <span data-ttu-id="ebc4f-177">Se si sa che i dati non contengono punti di codice Unicode non validi, ovvero tutte le stringhe hanno restituito **TRUE** da una chiamata a **IsNLSDefinedString(),** è possibile considerarli uguali se solo il byte basso di **dwNLSVersion** e **dwDefinedVersion** è stato modificato (le versioni secondarie descritte in precedenza).</span><span class="sxs-lookup"><span data-stu-id="ebc4f-177">If you KNOW that your data does not contain invalid Unicode code points (that is, all of your strings returned **TRUE** from a call to **IsNLSDefinedString()**), then you may consider them the same if ONLY the low byte of **dwNLSVersion** and **dwDefinedVersion** changed (the minor versions described above).</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="ebc4f-178">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="ebc4f-178">Links to Other Resources</span></span>

-   [<span data-ttu-id="ebc4f-179">Internazionalizzazione per le applicazioni di Windows</span><span class="sxs-lookup"><span data-stu-id="ebc4f-179">Internationalization for Windows Applications</span></span>](../intl/international-support.md)
-   [<span data-ttu-id="ebc4f-180">Funzione GetNLSVersionEx</span><span class="sxs-lookup"><span data-stu-id="ebc4f-180">GetNLSVersionEx Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [<span data-ttu-id="ebc4f-181">Funzione GetNLSVersion</span><span class="sxs-lookup"><span data-stu-id="ebc4f-181">GetNLSVersion Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [<span data-ttu-id="ebc4f-182">Come determinare se la versione delle regole di confronto è stata modificata</span><span class="sxs-lookup"><span data-stu-id="ebc4f-182">How to tell if the collation version changed</span></span>](/archive/blogs/shawnste/)

 

 

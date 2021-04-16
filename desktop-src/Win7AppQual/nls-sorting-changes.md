---
description: .
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: Modifiche di ordinamento NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0805eae753c1e312d26f8c84e13d19041458cf26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530145"
---
# <a name="nls-sorting-changes"></a><span data-ttu-id="fb15c-103">Modifiche di ordinamento NLS</span><span class="sxs-lookup"><span data-stu-id="fb15c-103">NLS Sorting Changes</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="fb15c-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="fb15c-104">Affected Platforms</span></span>

 <span data-ttu-id="fb15c-105">**Client** -Windows XP Windows \| Vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="fb15c-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="fb15c-106">**Server** -windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fb15c-106">**Servers** - Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="fb15c-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="fb15c-107">Feature Impact</span></span>

 <span data-ttu-id="fb15c-108">**Gravità** -alta</span><span class="sxs-lookup"><span data-stu-id="fb15c-108">**Severity** - High</span></span>  
<span data-ttu-id="fb15c-109">**Frequenza** -bassa (poche app interessate, ma se interessate, sempre interrotte)</span><span class="sxs-lookup"><span data-stu-id="fb15c-109">**Frequency** - Low (few apps impacted, but if impacted, always broken)</span></span>  


## <a name="description"></a><span data-ttu-id="fb15c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb15c-110">Description</span></span>

<span data-ttu-id="fb15c-111">Le funzioni NLS (National Language Support) aiutano le applicazioni a supportare le diverse esigenze specifiche per la lingua e le impostazioni locali degli utenti in tutto il mondo.</span><span class="sxs-lookup"><span data-stu-id="fb15c-111">The National Language Support (NLS) functions help applications support the different language- and locale-specific needs of users around the world.</span></span> <span data-ttu-id="fb15c-112">Le nuove versioni di Windows includono quasi sempre le modifiche NLS.</span><span class="sxs-lookup"><span data-stu-id="fb15c-112">New Windows versions almost invariably include NLS changes.</span></span> <span data-ttu-id="fb15c-113">Questa modifica influiscono sulle regole di confronto e l'ordinamento, quindi sulle applicazioni con indici permanenti.</span><span class="sxs-lookup"><span data-stu-id="fb15c-113">This change affects collation and sorting, and therefore applications that have persistent indexes.</span></span>

<span data-ttu-id="fb15c-114">Una tabella delle regole di confronto contiene due numeri che ne identificano la versione (revisione), ovvero la versione definita e la versione NLS.</span><span class="sxs-lookup"><span data-stu-id="fb15c-114">A collation table has two numbers that identify its version (revision): the defined version and the NLS version.</span></span> <span data-ttu-id="fb15c-115">Entrambe le versioni sono valori DWORD, composti da una versione principale e una versione secondaria.</span><span class="sxs-lookup"><span data-stu-id="fb15c-115">Both versions are DWORD values, composed of a major version and a minor version.</span></span> <span data-ttu-id="fb15c-116">Il primo byte di un valore è riservato, i due byte successivi rappresentano la versione principale e l'ultimo byte rappresenta la versione secondaria.</span><span class="sxs-lookup"><span data-stu-id="fb15c-116">The first byte of a value is reserved, the next two bytes represent the major version, and the last byte represents the minor version.</span></span> <span data-ttu-id="fb15c-117">In termini esadecimali, il modello è 0xRRMMMMmm, dove R è uguale a reserved, M è uguale a Major e m è uguale a minor.</span><span class="sxs-lookup"><span data-stu-id="fb15c-117">In hexadecimal terms, the pattern is 0xRRMMMMmm, where R equals Reserved, M equals major, and m equals minor.</span></span> <span data-ttu-id="fb15c-118">Ad esempio, una versione principale di 3 con una versione secondaria di 4 viene rappresentata come 0x304.</span><span class="sxs-lookup"><span data-stu-id="fb15c-118">For example, a major version of 3 with a minor version of 4 is represented as 0x304.</span></span>

<span data-ttu-id="fb15c-119">Per una versione principale, uno o più punti di codice cambiano in modo che l'applicazione debba reindicizzare tutti i dati affinché i confronti siano validi.</span><span class="sxs-lookup"><span data-stu-id="fb15c-119">For a major version, one or more code points change so that the application must re-index all data for comparisons to be valid.</span></span> <span data-ttu-id="fb15c-120">Per una versione secondaria, nulla viene spostato, ma vengono aggiunti punti di codice.</span><span class="sxs-lookup"><span data-stu-id="fb15c-120">For a minor version, nothing moves, but code points are added.</span></span> <span data-ttu-id="fb15c-121">Per questo tipo di versione, l'applicazione deve solo reindicizzare le stringhe con valori precedentemente non ordinabili.</span><span class="sxs-lookup"><span data-stu-id="fb15c-121">For this type of version, the application only has to re-index strings with previously unsortable values.</span></span> <span data-ttu-id="fb15c-122">In sintesi, di seguito sono riportati i numeri di versione in relazione alle modifiche dei dati nelle tabelle delle eccezioni specifiche delle impostazioni locali e nelle tabelle predefinite:</span><span class="sxs-lookup"><span data-stu-id="fb15c-122">In summary, here is what the version numbers mean in relation to the data changes in the locale-specific exception tables and default tables:</span></span>

<span data-ttu-id="fb15c-123">**NLSVersion Major** : punti di codice modificati nelle tabelle ' Exception ' o specifiche delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="fb15c-123">**NLSVersion Major** – Changed code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="fb15c-124">**NLSVersion minor** -aggiunta di nuovi punti di codice nelle tabelle ' Exception ' o specifiche delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="fb15c-124">**NLSVersion Minor** – Added new code points in the 'exception,' or locale-specific tables</span></span>  
<span data-ttu-id="fb15c-125">**DefinedVersion Major** : punti di codice modificati nella tabella predefinita</span><span class="sxs-lookup"><span data-stu-id="fb15c-125">**DefinedVersion Major** – Changed code points in the default table</span></span>  
<span data-ttu-id="fb15c-126">**DefinedVersion minor** -aggiunta di nuovi punti di codice nella tabella predefinita</span><span class="sxs-lookup"><span data-stu-id="fb15c-126">**DefinedVersion Minor** – Added new code points in the default table</span></span>  


<span data-ttu-id="fb15c-127">**Ordinamento dei numeri di versione per le versioni rilasciate:**</span><span class="sxs-lookup"><span data-stu-id="fb15c-127">**Sorting version numbers for released versions:**</span></span>



| <span data-ttu-id="fb15c-128">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="fb15c-128">Operating System</span></span>    | <span data-ttu-id="fb15c-129">Versione</span><span class="sxs-lookup"><span data-stu-id="fb15c-129">Release</span></span>           | <span data-ttu-id="fb15c-130">Versione (0xRRMMMMmm)</span><span class="sxs-lookup"><span data-stu-id="fb15c-130">Version (0xRRMMMMmm)</span></span>         |
|---------------------|-------------------|------------------------------|
| <span data-ttu-id="fb15c-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fb15c-131">Windows XP</span></span>          | <span data-ttu-id="fb15c-132">RTM/SP1/SP2/SP3/...</span><span class="sxs-lookup"><span data-stu-id="fb15c-132">RTM/SP1/SP2/SP3/…</span></span> | <span data-ttu-id="fb15c-133">N/A-nessuna API GetNLSVersion ()</span><span class="sxs-lookup"><span data-stu-id="fb15c-133">N/A - no GetNLSVersion() API</span></span> |
| <span data-ttu-id="fb15c-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fb15c-134">Windows Server 2003</span></span> | <span data-ttu-id="fb15c-135">RTM/SP1</span><span class="sxs-lookup"><span data-stu-id="fb15c-135">RTM/SP1</span></span>           | <span data-ttu-id="fb15c-136">0x00 0000 01</span><span class="sxs-lookup"><span data-stu-id="fb15c-136">0x00 0000 01</span></span>                 |
| <span data-ttu-id="fb15c-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb15c-137">Windows Vista</span></span>       | <span data-ttu-id="fb15c-138">RTM/SP1</span><span class="sxs-lookup"><span data-stu-id="fb15c-138">RTM/SP1</span></span>           | <span data-ttu-id="fb15c-139">0x00 0405 00</span><span class="sxs-lookup"><span data-stu-id="fb15c-139">0x00 0405 00</span></span>                 |
| <span data-ttu-id="fb15c-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb15c-140">Windows Server 2008</span></span> | <span data-ttu-id="fb15c-141">RTM</span><span class="sxs-lookup"><span data-stu-id="fb15c-141">RTM</span></span>               | <span data-ttu-id="fb15c-142">0x00 0501 00/0x00 5001 00</span><span class="sxs-lookup"><span data-stu-id="fb15c-142">0x00 0501 00 / 0x00 5001 00</span></span>  |
| <span data-ttu-id="fb15c-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fb15c-143">Windows 7</span></span>           | <span data-ttu-id="fb15c-144">RTM</span><span class="sxs-lookup"><span data-stu-id="fb15c-144">RTM</span></span>               | <span data-ttu-id="fb15c-145">0x00060100</span><span class="sxs-lookup"><span data-stu-id="fb15c-145">0x00060100</span></span>                   |



 

## <a name="manifestation"></a><span data-ttu-id="fb15c-146">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="fb15c-146">Manifestation</span></span>

<span data-ttu-id="fb15c-147">Le applicazioni, ad esempio i database, con indici permanenti che non controllano la versione NLS e reindicizzano in caso di modifica della versione non verranno ordinate correttamente o potrebbero non riuscire a fornire i risultati richiesti.</span><span class="sxs-lookup"><span data-stu-id="fb15c-147">Applications (such as databases) with persistent indexes that do not check the NLS version and re-index upon version change will fail to sort correctly or may fail to provide requested results.</span></span>

<span data-ttu-id="fb15c-148">Nel caso di interfacce utente, gli elenchi (ad esempio, alfabetico, numerico, alfanumerico, simboli e così via) potrebbero essere ordinati in modo errato.</span><span class="sxs-lookup"><span data-stu-id="fb15c-148">In the case of user interfaces, lists (for example, alphabetical, numeric, alphanumeric, symbols, and so on) may sort incorrectly.</span></span>

## <a name="solution"></a><span data-ttu-id="fb15c-149">Soluzione</span><span class="sxs-lookup"><span data-stu-id="fb15c-149">Solution</span></span>

<span data-ttu-id="fb15c-150">L'applicazione può chiamare **GetNLSVersionEx** (Windows Vista o versione successiva) o **GetNLSVersion** (prima di Windows Vista) per recuperare sia la versione definita che la versione NLS per una tabella delle regole di confronto.</span><span class="sxs-lookup"><span data-stu-id="fb15c-150">Your application can call either **GetNLSVersionEx** (Windows Vista or later) or **GetNLSVersion** (prior to Windows Vista) to retrieve both the defined version and the NLS version for a collation table.</span></span>

-   <span data-ttu-id="fb15c-151">GetNLSVersionEx:</span><span class="sxs-lookup"><span data-stu-id="fb15c-151">GetNLSVersionEx:</span></span>

<span data-ttu-id="fb15c-152">*Recupera le informazioni sulla versione corrente di una funzionalità NLS specificata per le impostazioni locali specificate dal nome*</span><span class="sxs-lookup"><span data-stu-id="fb15c-152">*Retrieves information about the current version of a specified NLS capability for a locale specified by name*</span></span>  
<span data-ttu-id="fb15c-153">Questa funzione consente a un'applicazione, ad esempio Active Directory di determinare se una modifica NLS influisca sulle impostazioni locali utilizzate per una determinata tabella dell'indice.</span><span class="sxs-lookup"><span data-stu-id="fb15c-153">This function allows an application such as Active Directory to determine whether an NLS change affects the locale used for a particular index table.</span></span> <span data-ttu-id="fb15c-154">In caso contrario, non è necessario reindicizzare la tabella.</span><span class="sxs-lookup"><span data-stu-id="fb15c-154">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="fb15c-155">Per ulteriori informazioni, vedere Gestione delle impostazioni locali e delle informazioni sulla lingua.</span><span class="sxs-lookup"><span data-stu-id="fb15c-155">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="fb15c-156">Questa funzione supporta impostazioni locali personalizzate.</span><span class="sxs-lookup"><span data-stu-id="fb15c-156">This function supports custom locales.</span></span> <span data-ttu-id="fb15c-157">Se *lpLocaleName* specifica un'impostazione locale supplementare, i dati recuperati sono i dati corretti per l'ordine delle regole di confronto associato alle impostazioni locali supplementari.</span><span class="sxs-lookup"><span data-stu-id="fb15c-157">If *lpLocaleName* specifies a supplemental locale, the data retrieved is the correct data for the collation order associated with that supplemental locale.</span></span>  

<span data-ttu-id="fb15c-158">**Nota:** Le versioni di Windows precedenti a Windows Vista non supportano **GetNLSVersionEx**.</span><span class="sxs-lookup"><span data-stu-id="fb15c-158">**Note:** Versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  


-   <span data-ttu-id="fb15c-159">GetNLSVersion (utilizzare per le applicazioni in esecuzione nelle versioni di Windows precedenti a Windows Vista):</span><span class="sxs-lookup"><span data-stu-id="fb15c-159">GetNLSVersion (use for applications running on versions of Windows prior to Windows Vista):</span></span>

<span data-ttu-id="fb15c-160">*Recupera le informazioni sulla versione corrente di una funzionalità NLS specificata per le impostazioni locali specificate dall'identificatore*</span><span class="sxs-lookup"><span data-stu-id="fb15c-160">*Retrieves information about the current version of a specified NLS capability for a locale specified by identifier*</span></span>  
<span data-ttu-id="fb15c-161">Questa funzione consente a un'applicazione, ad esempio Active Directory di determinare se una modifica NLS influisca sull'identificatore delle impostazioni locali utilizzato per una determinata tabella dell'indice.</span><span class="sxs-lookup"><span data-stu-id="fb15c-161">This function allows an application such as Active Directory to determine if an NLS change affects the locale identifier used for a particular index table.</span></span> <span data-ttu-id="fb15c-162">In caso contrario, non è necessario reindicizzare la tabella.</span><span class="sxs-lookup"><span data-stu-id="fb15c-162">If it does not, there is no need to re-index the table.</span></span> <span data-ttu-id="fb15c-163">Per ulteriori informazioni, vedere Gestione delle impostazioni locali e delle informazioni sulla lingua.</span><span class="sxs-lookup"><span data-stu-id="fb15c-163">For more information, see Handling Locale and Language Information.</span></span>  
<span data-ttu-id="fb15c-164">**Nota:** Questa funzione recupera informazioni solo sulle impostazioni locali specificate dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="fb15c-164">**Note:** This function retrieves information only about a locale specified by identifier.</span></span> <span data-ttu-id="fb15c-165">La funzione **GetNLSVersionEx** supporta impostazioni locali, funzionalità e nomi RFC 4646 aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="fb15c-165">The **GetNLSVersionEx** function supports additional locales, features, and RFC 4646 names.</span></span> <span data-ttu-id="fb15c-166">Tuttavia, le versioni di Windows precedenti a Windows Vista non supportano **GetNLSVersionEx**.</span><span class="sxs-lookup"><span data-stu-id="fb15c-166">However, versions of Windows prior to Windows Vista do not support **GetNLSVersionEx**.</span></span>  
<span data-ttu-id="fb15c-167">Le applicazioni destinate a essere eseguite solo in Windows Vista e versioni successive devono utilizzare **GetNLSVersionEx** in preferenza a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="fb15c-167">Applications meant to run only on Windows Vista and later should use **GetNLSVersionEx** in preference to this function.</span></span> <span data-ttu-id="fb15c-168">**GetNLSVersionEx** offre un supporto efficace per le impostazioni locali aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="fb15c-168">**GetNLSVersionEx** provides good support for supplemental locales.</span></span>  


## <a name="compatibility-test"></a><span data-ttu-id="fb15c-169">Test di compatibilità</span><span class="sxs-lookup"><span data-stu-id="fb15c-169">Compatibility Test</span></span>

<span data-ttu-id="fb15c-170">**Viene descritta la procedura per stabilire se una versione delle regole di confronto è cambiata (ovvero è necessario reindicizzare):**</span><span class="sxs-lookup"><span data-stu-id="fb15c-170">**Steps to tell if a collation version changed (that is, you need to re-index):**</span></span>

-   <span data-ttu-id="fb15c-171">**Utilizzare GetNLSVersionEx ()** per recuperare una struttura **NLSVERSIONINFOEX** quando si esegue l'indicizzazione originale dei dati.</span><span class="sxs-lookup"><span data-stu-id="fb15c-171">**Use GetNLSVersionEx()** to retrieve an **NLSVERSIONINFOEX** structure when doing the original indexing of your data.</span></span>
-   <span data-ttu-id="fb15c-172">Archiviare le proprietà seguenti con l'indice per identificare la versione:  **NLSVERSIONINFOEX. dwNLSVersion** e **NLSVERSIONINFOEX. dwDefinedVersion** : queste due proprietà insieme specificano la versione della tabella di ordinamento in uso.</span><span class="sxs-lookup"><span data-stu-id="fb15c-172">Store the following properties with your index to identify the version:  **NLSVERSIONINFOEX.dwNLSVersion** and **NLSVERSIONINFOEX.dwDefinedVersion** – These two properties together specify the version of the sorting table you are using.</span></span>  
    <span data-ttu-id="fb15c-173">**NLSVERSIONINFOEX. dwEffectiveId** : specifica le impostazioni locali effettive dell'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="fb15c-173">**NLSVERSIONINFOEX.dwEffectiveId** - This specifies the effective locale of your sort.</span></span> <span data-ttu-id="fb15c-174">Le impostazioni locali personalizzate punteranno a un ordinamento delle impostazioni locali nella casella.</span><span class="sxs-lookup"><span data-stu-id="fb15c-174">A custom locale will point to an in-box locale's sort.</span></span>  
    
-   <span data-ttu-id="fb15c-175">Quando si utilizza l'indice, utilizzare **GetNlsVersionEx ()** per individuare la versione dei dati.</span><span class="sxs-lookup"><span data-stu-id="fb15c-175">When using the index use **GetNlsVersionEx()** to discover the version of your data.</span></span>
-   <span data-ttu-id="fb15c-176">Se una delle tre proprietà è stata modificata, i dati di ordinamento utilizzati potrebbero restituire risultati diversi e qualsiasi indicizzazione potrebbe non riuscire a trovare i record.</span><span class="sxs-lookup"><span data-stu-id="fb15c-176">If any of the three properties has changed, the sorting data you are using could return different results and any indexing you have may fail to find records.</span></span>
-   <span data-ttu-id="fb15c-177">Se si è certi che i dati non contengono punti di codice Unicode non validi (ovvero, tutte le stringhe restituiscono **true** da una chiamata a **IsNLSDefinedString ()**), è possibile considerare le stesse se solo il byte minimo di **dwNLSVersion** e **dwDefinedVersion** è cambiato (le versioni secondarie descritte in precedenza).</span><span class="sxs-lookup"><span data-stu-id="fb15c-177">If you KNOW that your data does not contain invalid Unicode code points (that is, all of your strings returned **TRUE** from a call to **IsNLSDefinedString()**), then you may consider them the same if ONLY the low byte of **dwNLSVersion** and **dwDefinedVersion** changed (the minor versions described above).</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="fb15c-178">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="fb15c-178">Links to Other Resources</span></span>

-   [<span data-ttu-id="fb15c-179">Internazionalizzazione per le applicazioni di Windows</span><span class="sxs-lookup"><span data-stu-id="fb15c-179">Internationalization for Windows Applications</span></span>](../intl/international-support.md)
-   [<span data-ttu-id="fb15c-180">GetNLSVersionEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="fb15c-180">GetNLSVersionEx Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [<span data-ttu-id="fb15c-181">GetNLSVersion (funzione)</span><span class="sxs-lookup"><span data-stu-id="fb15c-181">GetNLSVersion Function</span></span>](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [<span data-ttu-id="fb15c-182">Come stabilire se la versione delle regole di confronto è stata modificata</span><span class="sxs-lookup"><span data-stu-id="fb15c-182">How to tell if the collation version changed</span></span>](/archive/blogs/shawnste/)

 

 

---
title: Test di convalida per i negozi online di tipo 2 di onboarding
description: Questo argomento descrive i test che verranno eseguiti da Microsoft per convalidare l'archivio online di tipo 2. Microsoft richiede di eseguire questi test prima di inviare una versione finale candidata. È necessario che l'archivio online passi i test da pubblicare.
ms.assetid: 1da51772-9711-4913-b05d-830fabe49da2
keywords:
- Windows Media Player Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beefd0945f9d1a9ae61e61f8be74beada1695baf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396086"
---
# <a name="validation-tests-for-on-boarding-type-2-online-stores"></a><span data-ttu-id="9108c-106">Test di convalida per i negozi online di tipo 2 di onboarding</span><span class="sxs-lookup"><span data-stu-id="9108c-106">Validation Tests for On-boarding Type 2 Online Stores</span></span>

<span data-ttu-id="9108c-107">Questo argomento descrive i test che verranno eseguiti da Microsoft per convalidare l'archivio online di tipo 2.</span><span class="sxs-lookup"><span data-stu-id="9108c-107">This topic describes tests that Microsoft will perform to validate your Type 2 online store.</span></span> <span data-ttu-id="9108c-108">Microsoft richiede di eseguire questi test prima di inviare una versione finale candidata.</span><span class="sxs-lookup"><span data-stu-id="9108c-108">Microsoft requires that you run these tests before you submit a release candidate.</span></span> <span data-ttu-id="9108c-109">È necessario che l'archivio online passi i test da pubblicare.</span><span class="sxs-lookup"><span data-stu-id="9108c-109">Your online store must successfully pass these tests to be published.</span></span>

> [!Note]  
> <span data-ttu-id="9108c-110">Se l'archivio è di tipo 1 anziché di tipo 2, è possibile usare questo argomento come linea guida per comprendere l'ambito del test di certificazione trattato per gli archivi di tipo 1.</span><span class="sxs-lookup"><span data-stu-id="9108c-110">If your store is Type 1 rather than Type 2, you can use this topic as a guideline to understand the scope of the certification testing that is covered for Type 1 stores.</span></span> <span data-ttu-id="9108c-111">Per il set completo di test per i negozi di tipo 1, contattare [supporto tecnico Microsoft](https://support.microsoft.com/ph/7763#tab0).</span><span class="sxs-lookup"><span data-stu-id="9108c-111">For the complete set of tests for Type 1 stores, contact [Microsoft Support](https://support.microsoft.com/ph/7763#tab0).</span></span>

 

<span data-ttu-id="9108c-112">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="9108c-112">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9108c-113">Elenco di controllo test</span><span class="sxs-lookup"><span data-stu-id="9108c-113">Test Checklist</span></span>](#test-checklist)
    -   [<span data-ttu-id="9108c-114">Preparazione superamento test</span><span class="sxs-lookup"><span data-stu-id="9108c-114">Test Pass Preparation</span></span>](#test-pass-preparation)
-   [<span data-ttu-id="9108c-115">Ambiente di test</span><span class="sxs-lookup"><span data-stu-id="9108c-115">Test Environment</span></span>](#test-environment)
-   [<span data-ttu-id="9108c-116">Installazione e configurazione</span><span class="sxs-lookup"><span data-stu-id="9108c-116">Configuration and Setup</span></span>](#configuration-and-setup)
    -   [<span data-ttu-id="9108c-117">Configurazione di un computer di test</span><span class="sxs-lookup"><span data-stu-id="9108c-117">Setting Up a Test Machine</span></span>](#setting-up-a-test-machine)
    -   [<span data-ttu-id="9108c-118">Configurazione di un archivio</span><span class="sxs-lookup"><span data-stu-id="9108c-118">Setting Up a Store</span></span>](#setting-up-a-store)
    -   [<span data-ttu-id="9108c-119">Creazione di un account</span><span class="sxs-lookup"><span data-stu-id="9108c-119">Creating an Account</span></span>](#creating-an-account)
    -   [<span data-ttu-id="9108c-120">Impostazione della memorizzazione delle credenziali nella cache</span><span class="sxs-lookup"><span data-stu-id="9108c-120">Setting Up Credential Caching</span></span>](#setting-up-credential-caching)
-   [<span data-ttu-id="9108c-121">Acquisizione contenuto</span><span class="sxs-lookup"><span data-stu-id="9108c-121">Content Acquisition</span></span>](#content-acquisition)
    -   [<span data-ttu-id="9108c-122">Flusso di contenuti</span><span class="sxs-lookup"><span data-stu-id="9108c-122">Streaming Content</span></span>](#streaming-content)
    -   [<span data-ttu-id="9108c-123">Recupero del contenuto</span><span class="sxs-lookup"><span data-stu-id="9108c-123">Obtaining Content</span></span>](#obtaining-content)
    -   [<span data-ttu-id="9108c-124">Burning del contenuto</span><span class="sxs-lookup"><span data-stu-id="9108c-124">Burning Content</span></span>](#burning-content)
    -   [<span data-ttu-id="9108c-125">Trasferimento di contenuto</span><span class="sxs-lookup"><span data-stu-id="9108c-125">Transferring Content</span></span>](#transferring-content)
-   [<span data-ttu-id="9108c-126">Funzionalità di archiviazione</span><span class="sxs-lookup"><span data-stu-id="9108c-126">Store Features</span></span>](#store-features)
    -   [<span data-ttu-id="9108c-127">Gestione di un account</span><span class="sxs-lookup"><span data-stu-id="9108c-127">Managing an Account</span></span>](#managing-an-account)
    -   [<span data-ttu-id="9108c-128">Gestione del centro informazioni</span><span class="sxs-lookup"><span data-stu-id="9108c-128">Managing the Info Center</span></span>](#managing-the-info-center)
-   [<span data-ttu-id="9108c-129">Interazione archivio</span><span class="sxs-lookup"><span data-stu-id="9108c-129">Store Interaction</span></span>](#store-interaction)
    -   [<span data-ttu-id="9108c-130">Cedendo all'archivio attivo</span><span class="sxs-lookup"><span data-stu-id="9108c-130">Yielding to the Active Store</span></span>](#yielding-to-the-active-store)
    -   [<span data-ttu-id="9108c-131">Impedire all'archivio testato di assumere l'archivio attivo</span><span class="sxs-lookup"><span data-stu-id="9108c-131">Preventing the Tested Store From Taking Over the Active Store</span></span>](#preventing-the-tested-store-from-taking-over-the-active-store)
    -   [<span data-ttu-id="9108c-132">Accesso a un archivio in modalità High-Contrast</span><span class="sxs-lookup"><span data-stu-id="9108c-132">Accessing a Store in High-Contrast Mode</span></span>](#accessing-a-store-in-high-contrast-mode)
    -   [<span data-ttu-id="9108c-133">Protezione di un archivio</span><span class="sxs-lookup"><span data-stu-id="9108c-133">Securing a Store</span></span>](#securing-a-store)

## <a name="test-checklist"></a><span data-ttu-id="9108c-134">Elenco di controllo test</span><span class="sxs-lookup"><span data-stu-id="9108c-134">Test Checklist</span></span>

<span data-ttu-id="9108c-135">Usare l'elenco di controllo nella tabella seguente per convalidare il negozio online di tipo 2 che si vuole portare a bordo.</span><span class="sxs-lookup"><span data-stu-id="9108c-135">Use the checklist in the following table to validate your Type 2 online store that you wish to bring on board.</span></span>



<span data-ttu-id="9108c-136">Test</span><span class="sxs-lookup"><span data-stu-id="9108c-136">Test</span></span>

<span data-ttu-id="9108c-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9108c-137">Windows XP</span></span>

<span data-ttu-id="9108c-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9108c-138">Windows Vista</span></span>

<span data-ttu-id="9108c-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9108c-139">Windows 7</span></span>

<span data-ttu-id="9108c-140">Risultato (superato/non superato/non applicabile)</span><span class="sxs-lookup"><span data-stu-id="9108c-140">Result (pass/fail/not applicable)</span></span>

<span data-ttu-id="9108c-141">32</span><span class="sxs-lookup"><span data-stu-id="9108c-141">32</span></span>

<span data-ttu-id="9108c-142">64</span><span class="sxs-lookup"><span data-stu-id="9108c-142">64</span></span>

<span data-ttu-id="9108c-143">32</span><span class="sxs-lookup"><span data-stu-id="9108c-143">32</span></span>

<span data-ttu-id="9108c-144">64</span><span class="sxs-lookup"><span data-stu-id="9108c-144">64</span></span>

<span data-ttu-id="9108c-145">32</span><span class="sxs-lookup"><span data-stu-id="9108c-145">32</span></span>

<span data-ttu-id="9108c-146">64</span><span class="sxs-lookup"><span data-stu-id="9108c-146">64</span></span>

1. <span data-ttu-id="9108c-147">Verificare che il software sia installato.</span><span class="sxs-lookup"><span data-stu-id="9108c-147">Verify that software installs.</span></span>

2. <span data-ttu-id="9108c-148">Verificare la disinstallazione del software.</span><span class="sxs-lookup"><span data-stu-id="9108c-148">Verify that software uninstalls.</span></span>

3. <span data-ttu-id="9108c-149">Verificare che il software non venga eseguito nell'area di notifica.</span><span class="sxs-lookup"><span data-stu-id="9108c-149">Verify that software does not run in the tray.</span></span>

4. <span data-ttu-id="9108c-150">Verificare che la scheda Store funzioni.</span><span class="sxs-lookup"><span data-stu-id="9108c-150">Verify that the store tab operates.</span></span>

5. <span data-ttu-id="9108c-151">Verificare che l'archivio disponga di un'opzione per creare un nuovo account.</span><span class="sxs-lookup"><span data-stu-id="9108c-151">Verify that the store has an option to create a new account.</span></span>

6. <span data-ttu-id="9108c-152">Verificare che l'account creato possa effettuare l'accesso.</span><span class="sxs-lookup"><span data-stu-id="9108c-152">Verify that the created account can sign in.</span></span>

7. <span data-ttu-id="9108c-153">Verificare che l'archivio disponga di un'opzione per salvare le informazioni utente.</span><span class="sxs-lookup"><span data-stu-id="9108c-153">Verify that the store has an option to save user information.</span></span>

8. <span data-ttu-id="9108c-154">Verificare che la memorizzazione nella cache delle credenziali sia presente e funzionante.</span><span class="sxs-lookup"><span data-stu-id="9108c-154">Verify that credential caching is present and working.</span></span>

9. <span data-ttu-id="9108c-155">Verificare che all'utente vengano richieste le credenziali se non sono memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="9108c-155">Verify that the user is prompted for credentials if they are not cached.</span></span>

10. <span data-ttu-id="9108c-156">Verificare che tutti i tipi di flusso di contenuto disponibili.</span><span class="sxs-lookup"><span data-stu-id="9108c-156">Verify that all available types of content stream.</span></span>

11. <span data-ttu-id="9108c-157">Verificare che il contenuto riproduca in Microsoft Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9108c-157">Verify that content plays in Microsoft Windows Media Player.</span></span>

12. <span data-ttu-id="9108c-158">Verificare che il prezzo calcolato sia corretto.</span><span class="sxs-lookup"><span data-stu-id="9108c-158">Verify that a calculated price is correct.</span></span>

13. <span data-ttu-id="9108c-159">Verificare che il contenuto acquistato venga scaricato nella libreria.</span><span class="sxs-lookup"><span data-stu-id="9108c-159">Verify that purchased content is downloaded to the library.</span></span>

14. <span data-ttu-id="9108c-160">Verificare che i metadati vengano scaricati per l'acquisto.</span><span class="sxs-lookup"><span data-stu-id="9108c-160">Verify that metadata is downloaded for the purchase.</span></span>

15. <span data-ttu-id="9108c-161">Verificare che i diritti di utilizzo del supporto siano corretti per l'acquisto.</span><span class="sxs-lookup"><span data-stu-id="9108c-161">Verify that media usage rights are correct for the purchase.</span></span>

16. <span data-ttu-id="9108c-162">Verificare che il contenuto acquistato possa essere riprodotto.</span><span class="sxs-lookup"><span data-stu-id="9108c-162">Verify that the purchased content can play.</span></span>

17. <span data-ttu-id="9108c-163">Verificare che facendo clic sul pulsante **Acquista** **o acquista sia** possibile passare allo Store.</span><span class="sxs-lookup"><span data-stu-id="9108c-163">Verify that clicking the **Buy** or **Shop** button switches to the store.</span></span>

18. <span data-ttu-id="9108c-164">Verificare che il contenuto acquistato sia stato scaricato.</span><span class="sxs-lookup"><span data-stu-id="9108c-164">Verify that purchased content downloaded.</span></span>

19. <span data-ttu-id="9108c-165">Verificare che il contenuto acquistato possa essere bruciato.</span><span class="sxs-lookup"><span data-stu-id="9108c-165">Verify that purchased content can be burned.</span></span>

20. <span data-ttu-id="9108c-166">Verificare che il numero di masterizzazioni venga decrementato.</span><span class="sxs-lookup"><span data-stu-id="9108c-166">Verify that the burn count is decremented.</span></span>

21. <span data-ttu-id="9108c-167">Verificare che il contenuto possa essere trasferito a un altro computer.</span><span class="sxs-lookup"><span data-stu-id="9108c-167">Verify that content can be transferred to another computer.</span></span>

22. <span data-ttu-id="9108c-168">Verificare che il contenuto venga trasferito a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9108c-168">Verify that content transfers to a device.</span></span>

23. <span data-ttu-id="9108c-169">Verificare che il numero di sincronizzazioni venga decrementato.</span><span class="sxs-lookup"><span data-stu-id="9108c-169">Verify that the sync count is decremented.</span></span>

24. <span data-ttu-id="9108c-170">Verificare che la cronologia degli acquisti tenga traccia degli acquisti precedenti.</span><span class="sxs-lookup"><span data-stu-id="9108c-170">Verify that the purchase history tracks prior purchases.</span></span>

25. <span data-ttu-id="9108c-171">Verificare che sia possibile ripristinare un acquisto precedente.</span><span class="sxs-lookup"><span data-stu-id="9108c-171">Verify that a prior purchase can be restored.</span></span>

26. <span data-ttu-id="9108c-172">Verificare la funzionalità di un archivio per gestire più computer.</span><span class="sxs-lookup"><span data-stu-id="9108c-172">Verify a store's functionality to manage multiple computers.</span></span>

27. <span data-ttu-id="9108c-173">Verificare che il centro informazioni sia disattivato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="9108c-173">Verify that the Info Center is off by default.</span></span>

28. <span data-ttu-id="9108c-174">Verificare che il centro informazioni includa informazioni multimediali nell'area Now-Playing.</span><span class="sxs-lookup"><span data-stu-id="9108c-174">Verify that the Info Center has media information in the now-playing area.</span></span>

29. <span data-ttu-id="9108c-175">Verificare che i collegamenti accedano all'archivio.</span><span class="sxs-lookup"><span data-stu-id="9108c-175">Verify that links navigate to the store.</span></span>

30. <span data-ttu-id="9108c-176">Verificare che l'archivio testato venga restituito nell'archivio attivo.</span><span class="sxs-lookup"><span data-stu-id="9108c-176">Verify that the tested store yields to the active store.</span></span>

31. <span data-ttu-id="9108c-177">Verificare che l'archivio testato non occupi l'archivio corrente.</span><span class="sxs-lookup"><span data-stu-id="9108c-177">Verify that the tested store does not take over the current store.</span></span>

32. <span data-ttu-id="9108c-178">Verificare che l'archivio sia accessibile in modalità a contrasto elevato.</span><span class="sxs-lookup"><span data-stu-id="9108c-178">Verify that the store is accessible in high-contrast mode.</span></span>

33. <span data-ttu-id="9108c-179">Verificare che l'archivio sia protetto.</span><span class="sxs-lookup"><span data-stu-id="9108c-179">Verify that the store is secure.</span></span>



 

### <a name="test-pass-preparation"></a><span data-ttu-id="9108c-180">Preparazione superamento test</span><span class="sxs-lookup"><span data-stu-id="9108c-180">Test Pass Preparation</span></span>

<span data-ttu-id="9108c-181">Prima di eseguire un test superato, è necessario assicurarsi che l'archivio e gli account di test siano pronti per il test.</span><span class="sxs-lookup"><span data-stu-id="9108c-181">Before you run a test pass, you should ensure that the store and the test accounts are ready for testing.</span></span> <span data-ttu-id="9108c-182">Prima dell'avvio del passaggio, è necessario determinare le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="9108c-182">You should determine the following information before the pass starts.</span></span> <span data-ttu-id="9108c-183">Se è possibile determinare le informazioni per alcuni giorni prima del superamento del test, il passaggio viene eseguito in modo più efficiente.</span><span class="sxs-lookup"><span data-stu-id="9108c-183">If you can determine the information some days in advance of the test pass, the pass will run more efficiently.</span></span>

-   <span data-ttu-id="9108c-184">Determinare le seguenti informazioni sugli account di test forniti dall'archivio:</span><span class="sxs-lookup"><span data-stu-id="9108c-184">Determine the following information about test accounts that are supplied by the store:</span></span>
    -   <span data-ttu-id="9108c-185">Account e password funzionano per consentire a un utente di eseguire l'accesso</span><span class="sxs-lookup"><span data-stu-id="9108c-185">Accounts and passwords work to allow a user to sign in</span></span>
    -   <span data-ttu-id="9108c-186">Gli account sono finanziati correttamente e adeguatamente per ogni tipo di modalità aziendale offerta dallo Store</span><span class="sxs-lookup"><span data-stu-id="9108c-186">Accounts are correctly and adequately funded for each type of business mode the store offers</span></span>
    -   <span data-ttu-id="9108c-187">Gli account sono validi per tutte le impostazioni locali da testare oppure sono presenti account per ogni impostazione locale se gli account non possono superare le impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="9108c-187">Accounts are valid for all locales to be tested, or accounts exist for each locale if accounts cannot cross locales</span></span>
-   <span data-ttu-id="9108c-188">Determinare le impostazioni locali da testare.</span><span class="sxs-lookup"><span data-stu-id="9108c-188">Determine which locales to test.</span></span>
-   <span data-ttu-id="9108c-189">Determinare le lingue da testare.</span><span class="sxs-lookup"><span data-stu-id="9108c-189">Determine which languages to test.</span></span>
-   <span data-ttu-id="9108c-190">Determinare le seguenti informazioni sull'ambiente di testing:</span><span class="sxs-lookup"><span data-stu-id="9108c-190">Determine the following information about the test environment:</span></span>

    -   <span data-ttu-id="9108c-191">Archivi Live compatibili con Windows XP, Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="9108c-191">Live stores that work with Windows XP, Windows Vista, and Windows 7</span></span>
    -   <span data-ttu-id="9108c-192">Archivio non Live da testare</span><span class="sxs-lookup"><span data-stu-id="9108c-192">The non-live store to test</span></span>
    -   <span data-ttu-id="9108c-193">Verificare che l'archivio non Live da testare sia visibile in tutte le versioni del sistema operativo e in tutte le versioni della piattaforma Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9108c-193">Verify that the non-live store to test is visible in all versions of the operating system and all versions of the Windows Media Player platform.</span></span>

-   <span data-ttu-id="9108c-194">Determinare le informazioni seguenti sull'archivio da testare:</span><span class="sxs-lookup"><span data-stu-id="9108c-194">Determine the following information about the store to test:</span></span>

    -   <span data-ttu-id="9108c-195">Nome archivio</span><span class="sxs-lookup"><span data-stu-id="9108c-195">Store name</span></span>
    -   <span data-ttu-id="9108c-196">Grafica e etichetta del logo della scheda Store prevista</span><span class="sxs-lookup"><span data-stu-id="9108c-196">Expected store tab logo graphics and label</span></span>
    -   <span data-ttu-id="9108c-197">Lo Store è attivo per tutte le versioni del sistema operativo?</span><span class="sxs-lookup"><span data-stu-id="9108c-197">Is the store live for all operating system versions?</span></span>
    -   <span data-ttu-id="9108c-198">Si tratta di una nuova versione dell'archivio sottoposta a test?</span><span class="sxs-lookup"><span data-stu-id="9108c-198">Is this is a new version of the store under test?</span></span>
    -   <span data-ttu-id="9108c-199">L'archivio è sottoposto a test di tipo 1 o di tipo 2?</span><span class="sxs-lookup"><span data-stu-id="9108c-199">Is the store under test a Type 1 or Type 2 store?</span></span>
    -   <span data-ttu-id="9108c-200">Il tipo di archivio è stato modificato?</span><span class="sxs-lookup"><span data-stu-id="9108c-200">Has the store type changed?</span></span>

-   <span data-ttu-id="9108c-201">Determinare in quali versioni e piattaforme del sistema operativo si prevede di testare l'archivio.</span><span class="sxs-lookup"><span data-stu-id="9108c-201">Determine on which operating system versions and platforms you plan to test the store.</span></span>
-   <span data-ttu-id="9108c-202">Determinare che il programma di installazione e il plug-in funzionano su tutte le versioni e le piattaforme del sistema operativo da testare.</span><span class="sxs-lookup"><span data-stu-id="9108c-202">Determine that the installer and plug-in works on all operating system versions and platforms to be tested.</span></span>
-   <span data-ttu-id="9108c-203">Determinare se è necessario un documento di navigazione.</span><span class="sxs-lookup"><span data-stu-id="9108c-203">Determine if a navigation document is required.</span></span>
-   <span data-ttu-id="9108c-204">Determinare le informazioni seguenti sui supporti offerti dal negozio:</span><span class="sxs-lookup"><span data-stu-id="9108c-204">Determine the following information about the media that the store offers:</span></span>

    -   <span data-ttu-id="9108c-205">Formati</span><span class="sxs-lookup"><span data-stu-id="9108c-205">Formats</span></span>
    -   <span data-ttu-id="9108c-206">È necessario un software proprietario?</span><span class="sxs-lookup"><span data-stu-id="9108c-206">Is any proprietary software required?</span></span>
    -   <span data-ttu-id="9108c-207">È necessario testare tutti i tipi di supporto o solo un subset di tipi di supporti?</span><span class="sxs-lookup"><span data-stu-id="9108c-207">Must you test all media types, or only a subset of media types?</span></span>

-   <span data-ttu-id="9108c-208">Determinare le seguenti informazioni sui diritti di utilizzo del supporto:</span><span class="sxs-lookup"><span data-stu-id="9108c-208">Determine the following information about media usage rights:</span></span>

    -   <span data-ttu-id="9108c-209">I supporti di archiviazione hanno la protezione del contenuto?</span><span class="sxs-lookup"><span data-stu-id="9108c-209">Does the store media have content protection?</span></span>
    -   <span data-ttu-id="9108c-210">In tal caso, determinare il tipo di protezione del contenuto del supporto.</span><span class="sxs-lookup"><span data-stu-id="9108c-210">If so, determine the type of content protection that the media have.</span></span>
    -   <span data-ttu-id="9108c-211">In tal caso, determinare il comportamento protetto previsto.</span><span class="sxs-lookup"><span data-stu-id="9108c-211">If so, determine the expected protected behavior.</span></span>
    -   <span data-ttu-id="9108c-212">I diritti di utilizzo dei supporti includono la condivisione da computer a computer?</span><span class="sxs-lookup"><span data-stu-id="9108c-212">Do the media usage rights include computer-to-computer sharing?</span></span>
    -   <span data-ttu-id="9108c-213">Diritti di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="9108c-213">The sync rights</span></span>
    -   <span data-ttu-id="9108c-214">Diritti di masterizzazione</span><span class="sxs-lookup"><span data-stu-id="9108c-214">The burn rights</span></span>
    -   <span data-ttu-id="9108c-215">Diritti di riproduzione</span><span class="sxs-lookup"><span data-stu-id="9108c-215">The play rights</span></span>
    -   <span data-ttu-id="9108c-216">Date di scadenza, se presenti</span><span class="sxs-lookup"><span data-stu-id="9108c-216">The expiration dates, if any</span></span>

-   <span data-ttu-id="9108c-217">Determinare se sono presenti supporti sufficienti (un catalogo sufficientemente grande) per fornire un campione significativo.</span><span class="sxs-lookup"><span data-stu-id="9108c-217">Determine if you have sufficient media (a large enough catalog) to provide a meaningful sample.</span></span>
-   <span data-ttu-id="9108c-218">Determinare quale passaggio della fase è: RC 0, conformità e così via.</span><span class="sxs-lookup"><span data-stu-id="9108c-218">Determine what the stage pass is: RC 0, compliance, and so on.</span></span>
-   <span data-ttu-id="9108c-219">Determinare se il superamento del test è un tipo specifico: regressione, fumo e così via.</span><span class="sxs-lookup"><span data-stu-id="9108c-219">Determine if the test pass is a certain type: regression, smoke, and so on.</span></span>

## <a name="test-environment"></a><span data-ttu-id="9108c-220">Ambiente di test</span><span class="sxs-lookup"><span data-stu-id="9108c-220">Test Environment</span></span>

<span data-ttu-id="9108c-221">È necessario eseguire il test delle configurazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9108c-221">You must conduct testing on the following configurations:</span></span>

-   <span data-ttu-id="9108c-222">Microsoft Windows Media Player 11 nei sistemi operativi Windows XP con Service Pack 3 (SP3) a 32 bit e a 64 bit</span><span class="sxs-lookup"><span data-stu-id="9108c-222">Microsoft Windows Media Player 11 on Windows XP with Service Pack 3 (SP3) 32-bit and 64-bit operating systems</span></span>
-   <span data-ttu-id="9108c-223">Windows Media Player 11 nei sistemi operativi Windows Vista a 32 bit e a 64 bit (Windows Media Player a 32 bit)</span><span class="sxs-lookup"><span data-stu-id="9108c-223">Windows Media Player 11 on Windows Vista 32-bit and 64-bit (32-bit Windows Media Player) operating systems</span></span>
-   <span data-ttu-id="9108c-224">Microsoft Windows Media Player 12 nei sistemi operativi Windows a 7 32 bit e a 64 bit (Windows Media Player a 32 bit)</span><span class="sxs-lookup"><span data-stu-id="9108c-224">Microsoft Windows Media Player 12 on Windows 7 32-bit and 64-bit (32-bit Windows Media Player) operating systems</span></span>

<span data-ttu-id="9108c-225">Sebbene sia necessario eseguire test su tutte le versioni e le piattaforme del sistema operativo elencate, le versioni a 32 bit di Windows Vista e Windows 7 sono le versioni del sistema operativo prioritarie.</span><span class="sxs-lookup"><span data-stu-id="9108c-225">Although you must perform testing on all the operating system versions and platforms listed, 32-bit versions of Windows Vista and Windows 7 are the priority targeted operating system versions.</span></span> <span data-ttu-id="9108c-226">È necessario testare l'installazione di qualsiasi software su tutte le piattaforme.</span><span class="sxs-lookup"><span data-stu-id="9108c-226">You must test the installation of any software on all platforms.</span></span>

<span data-ttu-id="9108c-227">Le schermate in questo argomento usano un archivio fittizio, Proseware, per illustrare l'uso dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="9108c-227">Screen shots in this topic use a fictitious store, Proseware, to demonstrate the usage of the user interface.</span></span>

## <a name="configuration-and-setup"></a><span data-ttu-id="9108c-228">Installazione e configurazione</span><span class="sxs-lookup"><span data-stu-id="9108c-228">Configuration and Setup</span></span>

<span data-ttu-id="9108c-229">Le sezioni seguenti descrivono come configurare e configurare i test di convalida per il caricamento in un archivio online di tipo 2.</span><span class="sxs-lookup"><span data-stu-id="9108c-229">The following sections describe how to configure and set up validation testing to on-board a Type 2 online store.</span></span>

### <a name="setting-up-a-test-machine"></a><span data-ttu-id="9108c-230">Configurazione di un computer di test</span><span class="sxs-lookup"><span data-stu-id="9108c-230">Setting Up a Test Machine</span></span>

<span data-ttu-id="9108c-231">Per configurare un computer di test, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="9108c-231">Perform the following steps to set up a test machine:</span></span>

1.  <span data-ttu-id="9108c-232">Puntare il computer di test ai server di test del contenuto aggiungendo una chiave del registro di sistema specifica dell'archivio.</span><span class="sxs-lookup"><span data-stu-id="9108c-232">Point the test computer to content test servers by adding a store-specific registry key.</span></span>
2.  <span data-ttu-id="9108c-233">Impostare i valori nella finestra di dialogo **Opzioni internazionali e della lingua** sulla lingua e le impostazioni locali appropriate.</span><span class="sxs-lookup"><span data-stu-id="9108c-233">Set values in the **Regional and Language Options** dialog box to the proper language and locale settings.</span></span> <span data-ttu-id="9108c-234">Per impostare la lingua, selezionare la scheda **formati** , quindi selezionare la lingua nella casella combinata **formato corrente** .</span><span class="sxs-lookup"><span data-stu-id="9108c-234">To set the language, select the **Formats** tab and then select the language from the **Current format** combo box.</span></span> <span data-ttu-id="9108c-235">Per impostare l'area, selezionare la scheda **località** , quindi selezionare l'area nella casella combinata **percorso corrente** .</span><span class="sxs-lookup"><span data-stu-id="9108c-235">To set the region, select the **Location** tab and then select the region from the **Current location** combo box.</span></span> <span data-ttu-id="9108c-236">Inoltre, per gli archivi che richiedono l'installazione di un plug-in o di un software personalizzato specifico dell'archivio, potrebbe essere necessario modificare le impostazioni locali del sistema in base alla lingua delle impostazioni locali del negozio per facilitare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="9108c-236">Additionally, for stores that require installation of a plug-in or store-specific custom software, you might need to change the system locale to the language of the store's locale to facilitate installation.</span></span> <span data-ttu-id="9108c-237">Il programma di installazione software deve supportare sia caratteri a byte singolo che doppi e deve essere eseguito in qualsiasi impostazione locale.</span><span class="sxs-lookup"><span data-stu-id="9108c-237">The software installer must support both single and double byte characters and must run on any locale.</span></span> <span data-ttu-id="9108c-238">È necessario eseguire il test nelle impostazioni locali native.</span><span class="sxs-lookup"><span data-stu-id="9108c-238">You must test in the native locale.</span></span> <span data-ttu-id="9108c-239">Per impostare le impostazioni locali native, aprire la finestra di dialogo **regione e lingua** , selezionare la scheda **amministrativa** , quindi fare clic sul pulsante **Modifica impostazioni locali del sistema** , come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="9108c-239">To set the native locale, open the **Region and Language** dialog box, select the **Administrative** tab, and then click the **Change system locale** button as shown in the following screen shot.</span></span> <span data-ttu-id="9108c-240">Quando si fa clic su questo pulsante viene visualizzata la finestra **di dialogo Impostazioni area e lingua** .</span><span class="sxs-lookup"><span data-stu-id="9108c-240">Clicking this button displays the **Region and Language Settings** dialog box.</span></span> <span data-ttu-id="9108c-241">Nella casella combinata **impostazioni locali del sistema corrente** della finestra di dialogo vengono modificate le impostazioni locali del sistema.</span><span class="sxs-lookup"><span data-stu-id="9108c-241">The **Current system locale** combo box in that dialog box changes the system locale.</span></span>

    <span data-ttu-id="9108c-242">Le schermate seguenti mostrano le schede in cui è possibile impostare l'area e la lingua:</span><span class="sxs-lookup"><span data-stu-id="9108c-242">The following screen shots show the tabs on which you can set region and language:</span></span>

    ![screenshot della finestra di dialogo Opzioni internazionali e della lingua](images/reg-lang-opt.png)

    ![screenshot che Mostra come modificare le impostazioni locali correnti del sistema](images/reg-lang-settings.png)

3.  <span data-ttu-id="9108c-245">Disattivare la visualizzazione del centro informazioni di un negozio impostando Windows Media Player per riprodurre una visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9108c-245">Turn off the view of a store's Info Center by setting Windows Media Player to play a visualization.</span></span> <span data-ttu-id="9108c-246">La differenza principale tra le piattaforme è che in Windows Media Player 11, si inizia facendo clic su **Now Playing**, mentre in Windows Media Player 12 si inizia facendo clic con il pulsante destro del mouse sulla finestra principale.</span><span class="sxs-lookup"><span data-stu-id="9108c-246">The main difference between the platforms is that in Windows Media Player 11, you start by clicking **Now Playing**, whereas in Windows Media Player 12, you start by right-clicking the main window.</span></span>

    <span data-ttu-id="9108c-247">Lo screenshot seguente mostra la sequenza di opzioni di menu che riproduce una visualizzazione in Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="9108c-247">The following screen shot shows the sequence of menu options that plays a visualization in Windows Media Player 11:</span></span>

    ![screenshot che illustra come riprodurre una visualizzazione in Windows Media Player 11](images/wmp11-visual.png)

    <span data-ttu-id="9108c-249">Lo screenshot seguente mostra la sequenza di opzioni di menu che riproduce una visualizzazione in Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="9108c-249">The following screen shot shows the sequence of menu options that plays a visualization in Windows Media Player 12:</span></span>

    ![screenshot che illustra come riprodurre una visualizzazione in Windows Media Player 12](images/wmp12-visual.png)

### <a name="setting-up-a-store"></a><span data-ttu-id="9108c-251">Configurazione di un archivio</span><span class="sxs-lookup"><span data-stu-id="9108c-251">Setting Up a Store</span></span>

<span data-ttu-id="9108c-252">Eseguire prima di tutto i passaggi seguenti per configurare un archivio e quindi eseguire i passaggi che seguono i passaggi iniziali per verificare l'installazione del negozio:</span><span class="sxs-lookup"><span data-stu-id="9108c-252">First perform the following steps to set up a store, and then perform the steps that follow the initial steps to verify the store setup:</span></span>

1.  <span data-ttu-id="9108c-253">Avviare Windows Media Player e attendere alcuni secondi per acquisire il file di AllServices.xml più recente.</span><span class="sxs-lookup"><span data-stu-id="9108c-253">Launch Windows Media Player and wait several seconds to acquire the latest AllServices.xml file.</span></span>
2.  <span data-ttu-id="9108c-254">Per Windows XP e Windows Vista, per selezionare uno Store online, fare prima clic sulla scheda che divide tra la visualizzazione della guida multimediale e la visualizzazione negozi online.</span><span class="sxs-lookup"><span data-stu-id="9108c-254">For Windows XP and Windows Vista, to select an online store, first click the tab that splits between the Media Guide view and the Online Stores view.</span></span> <span data-ttu-id="9108c-255">Quindi, dal menu fare clic su **Sfoglia tutti gli archivi online** e selezionare l'archivio facendo clic sull'icona nell'elenco di archivi.</span><span class="sxs-lookup"><span data-stu-id="9108c-255">Then, from the menu click **Browse all Online Stores**, and select the store by clicking its icon in the list of stores.</span></span> <span data-ttu-id="9108c-256">Per Windows 7, fare clic sul pulsante nel riquadro di spostamento della libreria che divide tra il pulsante della **Guida multimediale** e il pulsante **online stores** .</span><span class="sxs-lookup"><span data-stu-id="9108c-256">For Windows 7, click the button in the library-navigation pane that splits between the **Media Guide** button and the **Online Stores** button.</span></span> <span data-ttu-id="9108c-257">Quindi, dal menu fare clic su **Sfoglia tutti gli archivi online** e selezionare l'archivio facendo clic sull'icona nell'elenco di archivi.</span><span class="sxs-lookup"><span data-stu-id="9108c-257">Then, from the menu click **Browse all online stores**, and select the store by clicking its icon in the list of stores.</span></span>

    <span data-ttu-id="9108c-258">Lo screenshot seguente mostra come selezionare uno Store online in Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="9108c-258">The following screen shot shows how to select an online store in Windows Media Player 11:</span></span>

    ![screenshot che illustra come selezionare uno Store online in Windows Media Player 11](images/wmp11-set-store.png)

    <span data-ttu-id="9108c-260">Lo screenshot seguente mostra come selezionare uno Store online in Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="9108c-260">The following screen shot shows how to select an Online Store in Windows Media Player 12:</span></span>

    ![screenshot che illustra come selezionare uno Store online in Windows Media Player 12](images/wmp12-set-store.png)

3.  <span data-ttu-id="9108c-262">Seguire le istruzioni dello Store per installare eventuali software aggiuntivi necessari per usare lo Store.</span><span class="sxs-lookup"><span data-stu-id="9108c-262">Follow instructions from the store to install any additional software that is needed to use the store.</span></span>

<span data-ttu-id="9108c-263">**Per verificare l'installazione dell'archivio**</span><span class="sxs-lookup"><span data-stu-id="9108c-263">**To verify store setup**</span></span>

1.  <span data-ttu-id="9108c-264">Verificare che il software venga installato.</span><span class="sxs-lookup"><span data-stu-id="9108c-264">Verify that the software installs.</span></span>

    <span data-ttu-id="9108c-265">Verificare che il plug-in OCX o qualsiasi altro software dallo Store venga scaricato e installato senza errori.</span><span class="sxs-lookup"><span data-stu-id="9108c-265">Verify that the OCX plug-in or any other software from the store downloads and installs without error.</span></span>

2.  <span data-ttu-id="9108c-266">Verificare la disinstallazione del software.</span><span class="sxs-lookup"><span data-stu-id="9108c-266">Verify that the software uninstalls.</span></span>

    <span data-ttu-id="9108c-267">Verificare che nel pannello di controllo, nell'elemento **programmi e funzionalità** , il software installato dall'archivio venga visualizzato nell'elenco **Disinstalla o modifica programma** e verificare che sia possibile disinstallarlo da questo elenco senza errori.</span><span class="sxs-lookup"><span data-stu-id="9108c-267">Verify that in Control Panel, in the **Programs and Features** item, the software that the store installs appears in the **Uninstall or change a program** list, and verify that you can uninstall it from this list without error.</span></span>

3.  <span data-ttu-id="9108c-268">Verificare che il software non venga eseguito nella barra di sistema.</span><span class="sxs-lookup"><span data-stu-id="9108c-268">Verify that software does not run in the system tray.</span></span>

    <span data-ttu-id="9108c-269">Verificare che nessuno dei software dello Store aggiunga icone all'area di notifica del programma (sulla barra delle applicazioni a sinistra del clock) prima del consenso del cliente per scaricare il software dello Store.</span><span class="sxs-lookup"><span data-stu-id="9108c-269">Verify that none of the software from the store adds icons to the program notification area (on the Taskbar to the left of the clock) prior to customer consent to download store software.</span></span>

    <span data-ttu-id="9108c-270">L'esperienza di archiviazione di base non richiede l'installazione di software aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="9108c-270">The basic store experience should not require installation of additional software.</span></span> <span data-ttu-id="9108c-271">Dovrebbe essere disponibile un'esperienza di supporto di base, ad esempio flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="9108c-271">A basic media experience, such as streaming media, should be available.</span></span> <span data-ttu-id="9108c-272">Alcuni negozi installano software aggiuntivo, ad esempio Download Manager, per un'esperienza di supporto Premier. questi archivi possono avere icone nella barra di sistema se le icone rappresentano applicazioni separate da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9108c-272">Some stores install additional software such as download managers for a premier media experience; these stores can have icons in the system tray if the icons represent applications that are separate from Windows Media Player.</span></span>

4.  <span data-ttu-id="9108c-273">Verificare che la scheda Store funzioni.</span><span class="sxs-lookup"><span data-stu-id="9108c-273">Verify that the store tab operates.</span></span>

    <span data-ttu-id="9108c-274">Verificare che la scheda archivia cambi per indicare l'archivio selezionato.</span><span class="sxs-lookup"><span data-stu-id="9108c-274">Verify that the store tab changes to indicate the selected store.</span></span>

    <span data-ttu-id="9108c-275">Per Windows XP e Windows Vista con Windows Media Player 11, verificare che il nome e l'icona del negozio siano visibili sullo sfondo di Windows Media Player 11 scuro.</span><span class="sxs-lookup"><span data-stu-id="9108c-275">For Windows XP and Windows Vista with Windows Media Player 11, verify that the store name and icon are visible against the dark Windows Media Player 11 background.</span></span>

    <span data-ttu-id="9108c-276">Per Windows 7 con Windows Media Player 12, verificare che il nome e l'icona dell'archivio siano visibili nel riquadro di spostamento della libreria, nel menu di scelta rapida del selettore del servizio.</span><span class="sxs-lookup"><span data-stu-id="9108c-276">For Windows 7 with Windows Media Player 12, verify the store name and icon are visible in the library-navigation pane, in the service-selector context menu.</span></span>

    <span data-ttu-id="9108c-277">Verificare che l'archivio sia elencato nella parte superiore dell'elenco dei selettori del negozio nel menu.</span><span class="sxs-lookup"><span data-stu-id="9108c-277">Verify that the store is listed at the top of the store selector list in the menu.</span></span>

    > [!Note]  
    > <span data-ttu-id="9108c-278">Non verrà aggiunta l'opzione **di menu Aggiungi servizio corrente** se l'archivio di tipo 2 è l'archivio in primo piano (impostazione predefinita) per l'area.</span><span class="sxs-lookup"><span data-stu-id="9108c-278">There will be no **Add current service to menu** option if the Type 2 store is the featured (default) store for the region.</span></span>

     

    <span data-ttu-id="9108c-279">Lo screenshot seguente mostra il menu visualizzato quando si fa clic sulla scheda nell'angolo superiore destro di Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="9108c-279">The following screen shot shows the menu that appears when you click the tab at the top right corner of Windows Media Player 11:</span></span>

    ![screenshot che mostra la scheda Store in Windows Media Player 11](images/wmp11-verify-store.png)

    <span data-ttu-id="9108c-281">Lo screenshot seguente mostra il menu visualizzato quando si fa clic sul pulsante di menu combinato nell'angolo inferiore sinistro di Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="9108c-281">The following screen shot shows the menu that appears when you click the split button at the lower left corner of Windows Media Player 12:</span></span>

    ![screenshot che mostra la scheda Store in Windows Media Player 12](images/wmp12-verify-store.png)

### <a name="creating-an-account"></a><span data-ttu-id="9108c-283">Creazione di un account</span><span class="sxs-lookup"><span data-stu-id="9108c-283">Creating an Account</span></span>

<span data-ttu-id="9108c-284">**Per verificare la configurazione dell'account**</span><span class="sxs-lookup"><span data-stu-id="9108c-284">**To verify account setup**</span></span>

1.  <span data-ttu-id="9108c-285">Verificare che l'archivio disponga di un'opzione per creare un nuovo account e quindi seguire le istruzioni per la creazione di un nuovo account.</span><span class="sxs-lookup"><span data-stu-id="9108c-285">Verify that the store has an option to create a new account, and then follow the store instructions to create a new account.</span></span>

    <span data-ttu-id="9108c-286">Lo screenshot seguente evidenzia un pulsante **Crea nuovo account** come potrebbe essere visualizzato in Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="9108c-286">The following screen shot highlights a **Create New Account** button as it might appear in Windows Media Player 11:</span></span>

    ![screenshot che illustra come verificare la configurazione dell'account per Windows Media Player 11](images/wmp11-verify-account.png)

    <span data-ttu-id="9108c-288">Lo screenshot seguente evidenzia un pulsante **Crea nuovo account** come potrebbe essere visualizzato in Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="9108c-288">The following screen shot highlights a **Create New Account** button as it might appear in Windows Media Player 12:</span></span>

    ![screenshot che illustra come verificare la configurazione dell'account per Windows Media Player 12](images/wmp12-verify-account.png)

2.  <span data-ttu-id="9108c-290">Verificare che sia possibile accedere all'account creato.</span><span class="sxs-lookup"><span data-stu-id="9108c-290">Verify that you can sign in to the account that you created.</span></span>

### <a name="setting-up-credential-caching"></a><span data-ttu-id="9108c-291">Impostazione della memorizzazione delle credenziali nella cache</span><span class="sxs-lookup"><span data-stu-id="9108c-291">Setting Up Credential Caching</span></span>

<span data-ttu-id="9108c-292">Eseguire prima di tutto i passaggi seguenti per configurare la memorizzazione delle credenziali nella cache, quindi eseguire i passaggi che seguono i passaggi iniziali per verificare la configurazione della memorizzazione nella cache delle credenziali:</span><span class="sxs-lookup"><span data-stu-id="9108c-292">First perform the following steps to set up credential caching, and then perform the steps that follow the initial steps to verify the credential-caching setup:</span></span>

1.  <span data-ttu-id="9108c-293">Nella pagina di accesso immettere le credenziali e selezionare l'opzione per salvare le informazioni utente.</span><span class="sxs-lookup"><span data-stu-id="9108c-293">At the sign-in page, enter credentials and select the option to save user information.</span></span>
2.  <span data-ttu-id="9108c-294">Verificare che nella pagina di accesso sia presente una casella di controllo che consente all'utente di memorizzare nella cache le credenziali.</span><span class="sxs-lookup"><span data-stu-id="9108c-294">Verify that the sign-in page has a check box that allows the user to cache credentials.</span></span>
3.  <span data-ttu-id="9108c-295">La memorizzazione nella cache delle credenziali facoltativa è un punto di sicurezza importante.</span><span class="sxs-lookup"><span data-stu-id="9108c-295">Optional credential caching is an important security point.</span></span> <span data-ttu-id="9108c-296">Il caching automatico delle credenziali può esporre informazioni personali degli utenti che effettuano l'accesso a un computer condiviso o pubblico.</span><span class="sxs-lookup"><span data-stu-id="9108c-296">Automatic credential caching can expose personally identifiable information of users who sign into a shared or public computer.</span></span> <span data-ttu-id="9108c-297">È consigliabile proteggere le informazioni dei clienti offrendo una casella di controllo che consente di eseguire il rendering facoltativo della memorizzazione nella cache.</span><span class="sxs-lookup"><span data-stu-id="9108c-297">You should protect customer information by offering a check box that renders the caching optional.</span></span>

<span data-ttu-id="9108c-298">**Per verificare la memorizzazione delle credenziali nella cache**</span><span class="sxs-lookup"><span data-stu-id="9108c-298">**To verify credential caching**</span></span>

1.  <span data-ttu-id="9108c-299">Verificare che nell'archivio sia presente una casella di controllo per l'opzione **Salva le informazioni utente** .</span><span class="sxs-lookup"><span data-stu-id="9108c-299">Verify that the store has a check box for a **Save my user information** option.</span></span>

    1.  <span data-ttu-id="9108c-300">Chiudere Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="9108c-300">Close Windows Media Player.</span></span>
    2.  <span data-ttu-id="9108c-301">Riaprire Media Player di Windows e provare a scaricare contenuto.</span><span class="sxs-lookup"><span data-stu-id="9108c-301">Reopen Windows Media Player and attempt to download some content.</span></span>

2.  <span data-ttu-id="9108c-302">Verificare che la memorizzazione nella cache delle credenziali sia presente e funzionante.</span><span class="sxs-lookup"><span data-stu-id="9108c-302">Verify that credential caching is present and working.</span></span>

    1.  <span data-ttu-id="9108c-303">Disconnettersi dallo Store.</span><span class="sxs-lookup"><span data-stu-id="9108c-303">Sign out of the store.</span></span>
    2.  <span data-ttu-id="9108c-304">Chiudere Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="9108c-304">Close Windows Media Player.</span></span>
    3.  <span data-ttu-id="9108c-305">Riaprire Media Player di Windows e provare a scaricare contenuto.</span><span class="sxs-lookup"><span data-stu-id="9108c-305">Reopen Windows Media Player and attempt to download some content.</span></span>

3.  <span data-ttu-id="9108c-306">Verificare che all'utente vengano richieste le credenziali se non sono memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="9108c-306">Verify that the user is prompted for credentials if they are not cached.</span></span>

    <span data-ttu-id="9108c-307">Dopo la disconnessione e il tentativo di usare lo Store, al cliente verranno richieste le credenziali.</span><span class="sxs-lookup"><span data-stu-id="9108c-307">After signing out and then trying to use the store, the customer should be prompted for credentials.</span></span>

## <a name="content-acquisition"></a><span data-ttu-id="9108c-308">Acquisizione contenuto</span><span class="sxs-lookup"><span data-stu-id="9108c-308">Content Acquisition</span></span>

<span data-ttu-id="9108c-309">In questa sezione vengono descritti i vari modi per acquisire contenuto e come verificare che il contenuto sia stato acquisito.</span><span class="sxs-lookup"><span data-stu-id="9108c-309">This section describes the various ways to acquire content and how to verify that that content was acquired.</span></span>

### <a name="streaming-content"></a><span data-ttu-id="9108c-310">Flusso di contenuti</span><span class="sxs-lookup"><span data-stu-id="9108c-310">Streaming Content</span></span>

<span data-ttu-id="9108c-311">Trasmettere tutti i tipi di contenuto disponibili dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="9108c-311">Stream all available types of content from the store.</span></span> <span data-ttu-id="9108c-312">Ad esempio, flusso di contenuto Radio, video, audio e anteprime.</span><span class="sxs-lookup"><span data-stu-id="9108c-312">For example, stream radio, video, audio, and previews content.</span></span>

<span data-ttu-id="9108c-313">**Per verificare il contenuto di streaming**</span><span class="sxs-lookup"><span data-stu-id="9108c-313">**To verify streaming content**</span></span>

1.  <span data-ttu-id="9108c-314">Verificare che tutti i tipi di flusso di contenuto disponibili.</span><span class="sxs-lookup"><span data-stu-id="9108c-314">Verify that all available types of content stream.</span></span>

2.  <span data-ttu-id="9108c-315">Verificare che il contenuto riproduca in Windows Media Player e non in un altro lettore o controllo.</span><span class="sxs-lookup"><span data-stu-id="9108c-315">Verify that content plays in Windows Media Player and not some other player or control.</span></span>

### <a name="obtaining-content"></a><span data-ttu-id="9108c-316">Recupero del contenuto</span><span class="sxs-lookup"><span data-stu-id="9108c-316">Obtaining Content</span></span>

<span data-ttu-id="9108c-317">Eseguire prima di tutto i passaggi seguenti per acquistare il contenuto, quindi eseguire i passaggi che seguono i passaggi iniziali per verificare l'acquisto e verificare che il contenuto sia stato scaricato:</span><span class="sxs-lookup"><span data-stu-id="9108c-317">First perform the following steps to purchase content, and then perform the steps that follow the initial steps to verify the purchase and verify that the content downloaded:</span></span>

1.  <span data-ttu-id="9108c-318">Avviare Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9108c-318">Launch Windows Media Player.</span></span>
2.  <span data-ttu-id="9108c-319">Accedere all'account di test.</span><span class="sxs-lookup"><span data-stu-id="9108c-319">Sign in to the test account.</span></span>
3.  <span data-ttu-id="9108c-320">Passare al contenuto da acquistare.</span><span class="sxs-lookup"><span data-stu-id="9108c-320">Navigate to the content to purchase.</span></span>
4.  <span data-ttu-id="9108c-321">Seguire la procedura specifica dell'archivio per acquistare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="9108c-321">Follow the store-specific procedure to purchase content.</span></span>

<span data-ttu-id="9108c-322">**Per verificare il contenuto acquistato e scaricato**</span><span class="sxs-lookup"><span data-stu-id="9108c-322">**To verify purchased and downloaded content**</span></span>

1.  <span data-ttu-id="9108c-323">Verificare che il prezzo calcolato sia corretto.</span><span class="sxs-lookup"><span data-stu-id="9108c-323">Verify that the calculated price is correct.</span></span>

    <span data-ttu-id="9108c-324">Verificare che il prezzo sia corretto, in particolare quando si acquistano più parti di contenuto contemporaneamente e si verifica che le informazioni di saldo del conto siano aggiornate correttamente dopo l'acquisto.</span><span class="sxs-lookup"><span data-stu-id="9108c-324">Verify that the price is correct, especially when purchasing multiple pieces of content at once, and verify that any account balance information is updated correctly after purchase.</span></span> <span data-ttu-id="9108c-325">Alcuni contenuti possono essere acquistati come singole tracce e solo alcuni come album.</span><span class="sxs-lookup"><span data-stu-id="9108c-325">Some content can be purchased as single tracks and some as albums only.</span></span> <span data-ttu-id="9108c-326">Verificare che il prezzo dell'album non sia maggiore della somma delle singole tracce.</span><span class="sxs-lookup"><span data-stu-id="9108c-326">Verify that the album price is not larger than the sum of the individual tracks.</span></span>

2.  <span data-ttu-id="9108c-327">Verificare che il contenuto acquistato venga scaricato nella libreria.</span><span class="sxs-lookup"><span data-stu-id="9108c-327">Verify that the purchased content downloads to the library.</span></span>

    <span data-ttu-id="9108c-328">Al termine del download, passare al contenuto scaricato nella libreria Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="9108c-328">When the download completes, navigate to the downloaded content in the Windows Media Player library.</span></span> <span data-ttu-id="9108c-329">Il contenuto scaricato si trova nella libreria dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="9108c-329">The downloaded content is located in the current user's library.</span></span>

    -   <span data-ttu-id="9108c-330">Per Windows XP e Windows Vista con Windows Media Player 11, il contenuto scaricato viene visualizzato nel riquadro di spostamento della libreria, in pivot **libreria** , quindi in **canzoni**.</span><span class="sxs-lookup"><span data-stu-id="9108c-330">For Windows XP and Windows Vista with Windows Media Player 11, downloaded content appears in the library navigation pane, under **Library** pivot, and then under **Songs**.</span></span>
    -   <span data-ttu-id="9108c-331">Per Windows 7 con Windows Media Player 12, il contenuto scaricato nella libreria di Windows Media Player viene visualizzato nel riquadro di spostamento Media Player Windows in **musica**.</span><span class="sxs-lookup"><span data-stu-id="9108c-331">For Windows 7 with Windows Media Player 12, content that is downloaded to the Windows Media Player library appears in the Windows Media Player navigation pane under **Music**.</span></span>

3.  <span data-ttu-id="9108c-332">Verificare che vengano scaricati i metadati per l'acquisto.</span><span class="sxs-lookup"><span data-stu-id="9108c-332">Verify that metadata downloads for the purchase.</span></span>

    <span data-ttu-id="9108c-333">Verificare che le colonne seguenti siano visualizzate nella libreria Media Player di Windows (aggiungere in caso contrario):</span><span class="sxs-lookup"><span data-stu-id="9108c-333">Ensure that the following columns appear in the Windows Media Player library (add them if not):</span></span>

    -   <span data-ttu-id="9108c-334">Artista album</span><span class="sxs-lookup"><span data-stu-id="9108c-334">Album Artist</span></span>
    -   <span data-ttu-id="9108c-335">Titolo</span><span class="sxs-lookup"><span data-stu-id="9108c-335">Title</span></span>
    -   <span data-ttu-id="9108c-336">Titolo album</span><span class="sxs-lookup"><span data-stu-id="9108c-336">Album Title</span></span>
    -   <span data-ttu-id="9108c-337">Provider di contenuti</span><span class="sxs-lookup"><span data-stu-id="9108c-337">Content Provider</span></span>
    -   <span data-ttu-id="9108c-338">Genre</span><span class="sxs-lookup"><span data-stu-id="9108c-338">Genre</span></span>

    <span data-ttu-id="9108c-339">È necessario popolare le colonne precedenti.</span><span class="sxs-lookup"><span data-stu-id="9108c-339">The preceding columns must be populated.</span></span> <span data-ttu-id="9108c-340">Il contenuto deve avere album art.</span><span class="sxs-lookup"><span data-stu-id="9108c-340">Content should have album art.</span></span> <span data-ttu-id="9108c-341">Tuttavia, non è necessario che l'Art album superi i test di convalida.</span><span class="sxs-lookup"><span data-stu-id="9108c-341">However, album art is not required to pass validation testing.</span></span>

4.  <span data-ttu-id="9108c-342">Verificare che i diritti di utilizzo del supporto siano corretti per l'acquisto.</span><span class="sxs-lookup"><span data-stu-id="9108c-342">Verify that media usage rights are correct for the purchase.</span></span>

    <span data-ttu-id="9108c-343">Per ogni traccia scaricata, fare clic con il pulsante destro del mouse sulla traccia e selezionare **Proprietà**, quindi selezionare la scheda **diritti di utilizzo del supporto** .</span><span class="sxs-lookup"><span data-stu-id="9108c-343">For each downloaded track, right-click the track and select **Properties**, and then select the **Media Usage Rights** tab.</span></span>

    <span data-ttu-id="9108c-344">L'archivio può scegliere di proteggere il contenuto con i diritti di utilizzo dei supporti oppure può scegliere di non proteggere il contenuto.</span><span class="sxs-lookup"><span data-stu-id="9108c-344">The store can choose to protect its content with media usage rights, or can choose to not protect the content.</span></span> <span data-ttu-id="9108c-345">La scheda **diritti di utilizzo del supporto** riflette tale stato elencando le restrizioni oppure indicando che il contenuto non è protetto.</span><span class="sxs-lookup"><span data-stu-id="9108c-345">The **Media Usage Rights** tab reflects that status either by listing the restrictions, or by stating that the content is not protected.</span></span> <span data-ttu-id="9108c-346">L'archivio deve comunicare il piano più recente per i diritti di utilizzo dei supporti.</span><span class="sxs-lookup"><span data-stu-id="9108c-346">The store must communicate its most current plan for media usage rights.</span></span> <span data-ttu-id="9108c-347">È necessario verificare i risultati effettivi rispetto a questo comportamento previsto.</span><span class="sxs-lookup"><span data-stu-id="9108c-347">You must verify actual results against this expected behavior.</span></span>

    <span data-ttu-id="9108c-348">Le licenze per i diritti multimediali devono essere pre-recapitate.</span><span class="sxs-lookup"><span data-stu-id="9108c-348">Media rights licenses must be pre-delivered.</span></span> <span data-ttu-id="9108c-349">Il cliente non deve necessariamente riprodurre il contenuto o eseguire altre procedure per ottenere la licenza.</span><span class="sxs-lookup"><span data-stu-id="9108c-349">The customer must not be required to play the content or go through some other process to get the license.</span></span> <span data-ttu-id="9108c-350">È necessario confrontare i diritti di utilizzo di supporti specifici per le comunicazioni tra il negozio e il cliente in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="9108c-350">You must compare the specific media usage rights to what the store has communicated to the customer as appropriate.</span></span> <span data-ttu-id="9108c-351">I diritti devono essere trasferibili ad almeno altri due computer.</span><span class="sxs-lookup"><span data-stu-id="9108c-351">Rights must be transferable to at least two other computers.</span></span> <span data-ttu-id="9108c-352">I clienti devono poter masterizzare e sincronizzare i propri supporti.</span><span class="sxs-lookup"><span data-stu-id="9108c-352">Customers must be able to burn and synchronize their media.</span></span>

    <span data-ttu-id="9108c-353">Lo screenshot seguente illustra i diritti di utilizzo del supporto di un file protetto:</span><span class="sxs-lookup"><span data-stu-id="9108c-353">The following screen shot shows the media usage rights of a protected file:</span></span>

    ![screenshot che mostra i diritti di utilizzo dei supporti per un file protetto](images/media-rights-protected.png)

    <span data-ttu-id="9108c-355">Se il contenuto non è protetto, la scheda **Rights Usage media** indicherà questo fatto.</span><span class="sxs-lookup"><span data-stu-id="9108c-355">If the content is not protected, the **Media Usage Rights** tab indicates this fact.</span></span>

    <span data-ttu-id="9108c-356">Lo screenshot seguente illustra i diritti di utilizzo del supporto di un file non protetto:</span><span class="sxs-lookup"><span data-stu-id="9108c-356">The following screen shot shows the media usage rights of an unprotected file:</span></span>

    ![screenshot che mostra i diritti di utilizzo dei supporti per un file non protetto](images/media-rights-not-protected.png)

5.  <span data-ttu-id="9108c-358">Verificare che il contenuto acquistato venga riprodotto.</span><span class="sxs-lookup"><span data-stu-id="9108c-358">Verify that the purchased content plays.</span></span>

    <span data-ttu-id="9108c-359">Verificare che il contenuto scaricato venga riprodotto in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9108c-359">Verify that downloaded content plays in Windows Media Player.</span></span>

    <span data-ttu-id="9108c-360">Riprodurre qualsiasi contenuto acquistato dallo Store e che risiede nella libreria locale oppure trasmettere un'anteprima.</span><span class="sxs-lookup"><span data-stu-id="9108c-360">Play any content that was purchased from the store and that resides in the local library, or stream a preview.</span></span>

    <span data-ttu-id="9108c-361">Per acquistare contenuto in Windows XP e Windows Vista con Windows Media Player 11, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="9108c-361">Perform the following steps to purchase content in Windows XP and Windows Vista with Windows Media Player 11:</span></span>

    1.  <span data-ttu-id="9108c-362">Fare clic sulla scheda **Now Playing** .</span><span class="sxs-lookup"><span data-stu-id="9108c-362">Click the **Now Playing** tab.</span></span>
    2.  <span data-ttu-id="9108c-363">Nel riquadro dell'elenco posizionare il puntatore del mouse sul passaggio del mouse su album art per visualizzare il collegamento **Acquista** .</span><span class="sxs-lookup"><span data-stu-id="9108c-363">In the list pane, position the mouse pointer to hover over album art in order to show the **Buy** link.</span></span>
    3.  <span data-ttu-id="9108c-364">Fare clic su **Acquista**.</span><span class="sxs-lookup"><span data-stu-id="9108c-364">Click **Buy**.</span></span>

    <span data-ttu-id="9108c-365">Lo screenshot seguente mostra il percorso del collegamento **buy** in Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="9108c-365">The following screen shot shows the location of the **Buy** link in Windows Media Player 11:</span></span>

    ![screenshot che illustra come acquistare contenuto in Windows Media Player 11](images/wmp11-verify-buy-play.png)

    <span data-ttu-id="9108c-367">Per acquistare contenuto in Windows 7 con Windows Media Player 12, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="9108c-367">Perform the following steps to purchase content in Windows 7 with Windows Media Player 12:</span></span>

    1.  <span data-ttu-id="9108c-368">In modalità libreria fare clic sulla scheda **Riproduci** .</span><span class="sxs-lookup"><span data-stu-id="9108c-368">In library mode, click the **Play** tab.</span></span>
    2.  <span data-ttu-id="9108c-369">Nella playlist, in album Art, fare clic su **Shop**</span><span class="sxs-lookup"><span data-stu-id="9108c-369">In the playlist, under the album art, click **Shop**</span></span>

    <span data-ttu-id="9108c-370">Lo screenshot seguente mostra come acquistare contenuto in Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="9108c-370">The following screen shot shows how to buy content in Windows Media Player 12:</span></span>

    ![screenshot che illustra come acquistare contenuto in Windows Media Player 12](images/wmp12-verify-buy-play.png)

6.  <span data-ttu-id="9108c-372">Verificare **che fare clic** su **Acquista** o acquista opzioni per lo Store.</span><span class="sxs-lookup"><span data-stu-id="9108c-372">Verify that clicking **Buy** or **Shop** switches to the store.</span></span>

    <span data-ttu-id="9108c-373">Il Media Player di Windows dovrebbe passare allo Store nella visualizzazione libreria e caricare l'esperienza di acquisto dello Store.</span><span class="sxs-lookup"><span data-stu-id="9108c-373">The Windows Media Player should switch to the store in library view and load the purchasing experience of the store.</span></span>

    <span data-ttu-id="9108c-374">È quindi necessario continuare a acquistare la traccia.</span><span class="sxs-lookup"><span data-stu-id="9108c-374">You must then continue to purchase the track.</span></span>

7.  <span data-ttu-id="9108c-375">Verificare che dopo aver fatto clic su **acquista o acquista** , il contenuto viene scaricato.</span><span class="sxs-lookup"><span data-stu-id="9108c-375">Verify that after clicking **Buy** or **Shop**, the content downloads.</span></span>

    <span data-ttu-id="9108c-376">Verificare che i diritti di utilizzo del supporto siano appropriati per il contenuto acquistato e i relativi metadati e verificare che la traccia riproduca.</span><span class="sxs-lookup"><span data-stu-id="9108c-376">Verify that the media usage rights are appropriate for the purchased content and its metadata, and verify that the track plays.</span></span> <span data-ttu-id="9108c-377">In generale, questo metodo di acquisto deve avere gli stessi risultati di altri metodi.</span><span class="sxs-lookup"><span data-stu-id="9108c-377">In general, this method of purchase should have the same results as other methods.</span></span>

### <a name="burning-content"></a><span data-ttu-id="9108c-378">Burning del contenuto</span><span class="sxs-lookup"><span data-stu-id="9108c-378">Burning Content</span></span>

<span data-ttu-id="9108c-379">Eseguire prima di tutto i passaggi seguenti per masterizzare il contenuto acquistato (copiare il contenuto acquistato in un CD o DVD scrivibile), quindi eseguire i passaggi che seguono i passaggi iniziali per verificare che il contenuto bruci:</span><span class="sxs-lookup"><span data-stu-id="9108c-379">First perform the following steps to burn purchased content (copy purchased content to a writeable CD or DVD), and then perform the steps that follow the initial steps to verify that the content burns:</span></span>

> [!Note]  
> <span data-ttu-id="9108c-380">Prima di masterizzare una traccia acquistata, annotare il numero di Burn, in modo da poter verificare in seguito se il conteggio diminuisce dopo aver bruciato la traccia.</span><span class="sxs-lookup"><span data-stu-id="9108c-380">Before you burn a purchased track, note its burn count so you can later verify whether the count decrements after you burn the track.</span></span>

 

1.  <span data-ttu-id="9108c-381">Fare clic sulla scheda **Burn**</span><span class="sxs-lookup"><span data-stu-id="9108c-381">Click the **Burn** tab</span></span>
2.  <span data-ttu-id="9108c-382">Trascinare le tracce acquistate nell' **elenco di masterizzazioni**.</span><span class="sxs-lookup"><span data-stu-id="9108c-382">Drag purchased tracks to the **Burn List**.</span></span>
3.  <span data-ttu-id="9108c-383">Fare clic sul pulsante **Avvia Burn** .</span><span class="sxs-lookup"><span data-stu-id="9108c-383">Click the **Start Burn** button.</span></span>

<span data-ttu-id="9108c-384">Lo screenshot seguente mostra l' **elenco di masterizzazioni** sul lato destro dello schermo e il pulsante **Avvia Burn** sotto l' **elenco di masterizzazione** in Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="9108c-384">The following screen shot shows the **Burn List** on the right side of the screen and the **Start Burn** button below the **Burn List** in Windows Media Player 11:</span></span>

![screenshot che illustra come masterizzare contenuto in Windows Media Player 11](images/wmp11-verify-burn.png)

<span data-ttu-id="9108c-386">Lo screenshot seguente mostra come viene visualizzato l'elenco di masterizzazione in Windows Media Player 12 dopo aver trascinato una traccia nell'elenco di masterizzazione e viene visualizzato il pulsante **Avvia Burn** nella parte superiore della scheda **Burn** :</span><span class="sxs-lookup"><span data-stu-id="9108c-386">The following screen shot shows how the burn list appears in Windows Media Player 12 after you drag a track to the burn list, and it shows the **Start Burn** button at the top of the **Burn** tab:</span></span>

![screenshot che illustra come masterizzare contenuto in Windows Media Player 12](images/wmp12-verify-burn.png)

<span data-ttu-id="9108c-388">**Per verificare che il contenuto acquistato possa essere bruciato**</span><span class="sxs-lookup"><span data-stu-id="9108c-388">**To verify that purchased content can be burned**</span></span>

1.  <span data-ttu-id="9108c-389">Verificare che il contenuto acquistato venga bruciato giocando il CD o il DVD dopo il completamento della masterizzazione.</span><span class="sxs-lookup"><span data-stu-id="9108c-389">Verify that the purchased content burns by playing the CD or DVD after burning completes.</span></span>

2.  <span data-ttu-id="9108c-390">Verificare che il numero di masterizzazioni venga decrementato.</span><span class="sxs-lookup"><span data-stu-id="9108c-390">Verify that the burn count is decremented.</span></span>

    <span data-ttu-id="9108c-391">Passare alla raccolta e aprire i diritti di utilizzo del supporto per una traccia acquistata che è stata bruciata.</span><span class="sxs-lookup"><span data-stu-id="9108c-391">Navigate to the library and open the media usage rights for a purchased track that was burned.</span></span>

    <span data-ttu-id="9108c-392">Se il numero di volte in cui è possibile masterizzare una traccia è limitato, verificare che questo numero venga diminuito dopo che la traccia è stata bruciata.</span><span class="sxs-lookup"><span data-stu-id="9108c-392">If the number of times a track can be burned is limited, verify that this number decreases after the track is burned.</span></span>

### <a name="transferring-content"></a><span data-ttu-id="9108c-393">Trasferimento di contenuto</span><span class="sxs-lookup"><span data-stu-id="9108c-393">Transferring Content</span></span>

<span data-ttu-id="9108c-394">Trasferire il contenuto a un altro computer.</span><span class="sxs-lookup"><span data-stu-id="9108c-394">Transfer content to another computer.</span></span>

<span data-ttu-id="9108c-395">**Per verificare che il contenuto acquistato possa essere trasferito a un altro computer**</span><span class="sxs-lookup"><span data-stu-id="9108c-395">**To verify that purchased content can be transferred to another computer**</span></span>

-   <span data-ttu-id="9108c-396">Se l'archivio consente il trasferimento di contenuto a un altro computer, trasferire il contenuto ad almeno due computer.</span><span class="sxs-lookup"><span data-stu-id="9108c-396">If the store allows transferring content to another computer, transfer the content to at least two computers.</span></span>

<span data-ttu-id="9108c-397">Eseguire prima di tutto i passaggi seguenti per sincronizzare un dispositivo e trasferire il contenuto acquistato al dispositivo, quindi eseguire i passaggi che seguono i passaggi iniziali per verificare che il contenuto venga trasferito:</span><span class="sxs-lookup"><span data-stu-id="9108c-397">First perform the following steps to sync to a device and transfer purchased content to that device, and then perform the steps that follow the initial steps to verify that the content is transferred:</span></span>

> [!Note]  
> <span data-ttu-id="9108c-398">Prima di trasferire una traccia acquistata, annotare il numero di sincronizzazioni, in modo da poter verificare in seguito se il conteggio diminuisce dopo il trasferimento della traccia.</span><span class="sxs-lookup"><span data-stu-id="9108c-398">Before you transfer a purchased track, note its sync count so you can later verify whether the count decrements after you transfer the track.</span></span>

 

1.  <span data-ttu-id="9108c-399">Connettere un dispositivo con un clock protetto.</span><span class="sxs-lookup"><span data-stu-id="9108c-399">Connect a device with a secure clock.</span></span> <span data-ttu-id="9108c-400">Alcuni esempi includono i dispositivi che usano Windows Media DRM per i dispositivi portatili, ad esempio un centro multimediale portatile come iRiver H10, Creative Zen e così via.</span><span class="sxs-lookup"><span data-stu-id="9108c-400">Examples include devices that use Windows Media DRM for Portable Devices, such as a Portable Media Center like the iRiver H10, the Creative Zen, and so on.</span></span>
2.  <span data-ttu-id="9108c-401">In Windows Media Player fare clic sulla scheda **Sincronizza** .</span><span class="sxs-lookup"><span data-stu-id="9108c-401">In Windows Media Player, click the **Sync** tab.</span></span>
3.  <span data-ttu-id="9108c-402">Trascinare il contenuto dalla libreria all'area **elenco sincronizzazione** nella scheda **Sincronizza** .</span><span class="sxs-lookup"><span data-stu-id="9108c-402">Drag content from the library to the **Sync list** area on the **Sync** tab.</span></span>
4.  <span data-ttu-id="9108c-403">Fare clic sul pulsante **Avvia sincronizzazione** .</span><span class="sxs-lookup"><span data-stu-id="9108c-403">Click the **Start Sync** button.</span></span>

<span data-ttu-id="9108c-404">Lo screenshot seguente mostra la traccia 1 nell'area **elenco sincronizzazione** e Mostra il pulsante **Avvia sincronizzazione** in Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="9108c-404">The following screen shot shows Track 1 in the **Sync list** area and shows the **Start Sync** button in Windows Media Player 11:</span></span>

![screenshot che Mostra come trasferire il contenuto in Windows Media Player 11](images/wmp11-verify-transfer.png)

<span data-ttu-id="9108c-406">Lo screenshot seguente mostra la traccia 1 nell'area **elenco sincronizzazione** e Mostra il pulsante **Avvia sincronizzazione** in Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="9108c-406">The following screen shot shows Track 1 in the **Sync list** area and shows the **Start Sync** button in Windows Media Player 12:</span></span>

![screenshot che Mostra come trasferire il contenuto in Windows Media Player 12](images/wmp12-verify-transfer.png)

<span data-ttu-id="9108c-408">**Per verificare che il contenuto acquistato possa essere trasferito a un altro dispositivo**</span><span class="sxs-lookup"><span data-stu-id="9108c-408">**To verify that purchased content can be transferred to another device**</span></span>

1.  <span data-ttu-id="9108c-409">Verificare che il contenuto acquistato venga trasferito al dispositivo giocando al contenuto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9108c-409">Verify that the purchased content is transferred to the device by playing the content on the device.</span></span> <span data-ttu-id="9108c-410">Anche il contenuto trasferito deve avere metadati appropriati.</span><span class="sxs-lookup"><span data-stu-id="9108c-410">The transferred content must also have appropriate metadata.</span></span>

2.  <span data-ttu-id="9108c-411">Verificare che il numero di sincronizzazioni venga decrementato.</span><span class="sxs-lookup"><span data-stu-id="9108c-411">Verify that the sync count is decremented.</span></span>

    <span data-ttu-id="9108c-412">Passare alla raccolta e aprire i diritti di utilizzo del supporto per una traccia trasferita.</span><span class="sxs-lookup"><span data-stu-id="9108c-412">Navigate to the library and open the media usage rights for a transferred track.</span></span>

    <span data-ttu-id="9108c-413">Se il numero di volte in cui è possibile sincronizzare una traccia è limitato, verificare che questo numero diminuisca quando viene trasferita la traccia.</span><span class="sxs-lookup"><span data-stu-id="9108c-413">If the number of times a track can sync is limited, verify that this number decreases when the track is transferred.</span></span>

## <a name="store-features"></a><span data-ttu-id="9108c-414">Funzionalità di archiviazione</span><span class="sxs-lookup"><span data-stu-id="9108c-414">Store Features</span></span>

<span data-ttu-id="9108c-415">Le sezioni seguenti descrivono come testare le varie funzionalità di un negozio online caricato.</span><span class="sxs-lookup"><span data-stu-id="9108c-415">The following sections describe how to test various features of an on-boarded online store.</span></span>

### <a name="managing-an-account"></a><span data-ttu-id="9108c-416">Gestione di un account</span><span class="sxs-lookup"><span data-stu-id="9108c-416">Managing an Account</span></span>

<span data-ttu-id="9108c-417">Accedere con un account che ha effettuato alcuni acquisti e aprire la cronologia degli acquisti.</span><span class="sxs-lookup"><span data-stu-id="9108c-417">Sign in with an account that has made some purchases and open the purchase history.</span></span>

<span data-ttu-id="9108c-418">**Per verificare la cronologia degli acquisti**</span><span class="sxs-lookup"><span data-stu-id="9108c-418">**To verify purchase history**</span></span>

-   <span data-ttu-id="9108c-419">Verificare che la cronologia degli acquisti tenga traccia degli acquisti precedenti.</span><span class="sxs-lookup"><span data-stu-id="9108c-419">Verify that the purchase history tracks prior purchases.</span></span>

<span data-ttu-id="9108c-420">Se il tipo di account o archivio supporta questa funzionalità, provare a ripristinare un acquisto eliminato.</span><span class="sxs-lookup"><span data-stu-id="9108c-420">If the store or account type supports this feature, attempt to restore a deleted purchase.</span></span>

<span data-ttu-id="9108c-421">**Per verificare che gli acquisti precedenti possano essere riacquisiti**</span><span class="sxs-lookup"><span data-stu-id="9108c-421">**To verify that prior purchases can be reacquired**</span></span>

-   <span data-ttu-id="9108c-422">Verificare che sia possibile ripristinare un acquisto precedente.</span><span class="sxs-lookup"><span data-stu-id="9108c-422">Verify that a prior purchase can be restored.</span></span>

<span data-ttu-id="9108c-423">Se l'archivio supporta l'utilizzo di più computer con l'account, verificare le funzionalità fornite da questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="9108c-423">If the store supports using multiple computers with the account, verify any functionality that this feature provides.</span></span>

<span data-ttu-id="9108c-424">**Per verificare la gestione di più computer con un singolo account**</span><span class="sxs-lookup"><span data-stu-id="9108c-424">**To verify multiple computer management with a single account**</span></span>

-   <span data-ttu-id="9108c-425">Verificare la funzionalità dell'archivio per gestire più computer.</span><span class="sxs-lookup"><span data-stu-id="9108c-425">Verify the store's functionality to manage multiple computers.</span></span>

### <a name="managing-a-store-specific-account"></a><span data-ttu-id="9108c-426">Gestione di un account Store-Specific</span><span class="sxs-lookup"><span data-stu-id="9108c-426">Managing a Store-Specific Account</span></span>

<span data-ttu-id="9108c-427">L'archivio potrebbe non avere tipi di account, restrizioni o contenuti tipici.</span><span class="sxs-lookup"><span data-stu-id="9108c-427">The store might not have typical account types, restrictions, or content.</span></span> <span data-ttu-id="9108c-428">Ad esempio, un archivio che affitta il video di streaming potrebbe richiedere un'interfaccia utente per visualizzare i noleggi attivi e l'interfaccia utente deve essere testata.</span><span class="sxs-lookup"><span data-stu-id="9108c-428">For example, a store that rents streaming video would need some user interface to display active rentals and that user interface would need to be tested.</span></span>

> [!Note]  
> <span data-ttu-id="9108c-429">Sebbene Microsoft non sia in grado di certificare le funzionalità degli account specifici dell'archivio, per garantire una migliore esperienza con i clienti, è consigliabile testare tale funzionalità.</span><span class="sxs-lookup"><span data-stu-id="9108c-429">Although Microsoft cannot certify store-specific account functionality, to ensure a good customer experience, you should test that functionality.</span></span>

 

### <a name="managing-the-info-center"></a><span data-ttu-id="9108c-430">Gestione del centro informazioni</span><span class="sxs-lookup"><span data-stu-id="9108c-430">Managing the Info Center</span></span>

<span data-ttu-id="9108c-431">Eseguire prima di tutto i passaggi seguenti per preparare il test dello stato predefinito, quindi eseguire il passaggio successivo che segue i passaggi iniziali per verificare che il centro informazioni sia disattivato per impostazione predefinita:</span><span class="sxs-lookup"><span data-stu-id="9108c-431">First perform the following steps to prepare for testing the default state, and then perform the next step that follows the initial steps to verify that the Info Center is off by default:</span></span>

1.  <span data-ttu-id="9108c-432">Riprodurre contenuto dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="9108c-432">Play some content from the store.</span></span>
2.  <span data-ttu-id="9108c-433">Passa alla modalità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="9108c-433">Switch to Now Playing mode.</span></span> <span data-ttu-id="9108c-434">In Windows XP o Windows Vista con Windows Media Player 11, fare clic sulla scheda **Now Playing** . In Windows 7 con Windows Media Player 12 fare clic sul pulsante **passa a ora di riproduzione** nell'angolo in basso a destra.</span><span class="sxs-lookup"><span data-stu-id="9108c-434">In Windows XP or Windows Vista with Windows Media Player 11, click the **Now Playing** tab. In Windows 7 with Windows Media Player 12, click the **Switch to Now Playing** button at the lower right corner.</span></span>

<span data-ttu-id="9108c-435">**Per verificare che il centro informazioni sia disattivato per impostazione predefinita**</span><span class="sxs-lookup"><span data-stu-id="9108c-435">**To verify that the Info Center is off by default**</span></span>

-   <span data-ttu-id="9108c-436">Verificare che il centro informazioni sia disattivato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="9108c-436">Verify that the Info Center is off by default.</span></span>

<span data-ttu-id="9108c-437">Se l'archivio offre una visualizzazione del centro informazioni, Riproduci contenuto dallo Store e durante la riproduzione del contenuto passa alla modalità di riproduzione e attiva il centro informazioni.</span><span class="sxs-lookup"><span data-stu-id="9108c-437">If the store offers an Info Center view, play some content from the store, and while the content is playing, switch to Now Playing mode and turn Info Center on.</span></span>

<span data-ttu-id="9108c-438">In Windows XP o Windows Vista con Windows Media Player 11, fare clic con il pulsante destro del mouse sulla finestra Now-playing, quindi scegliere **visualizzazione centro informazioni** dal menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="9108c-438">In Windows XP or Windows Vista with Windows Media Player 11, right-click the now-playing window, and then from the context menu select **Info Center View**.</span></span>

<span data-ttu-id="9108c-439">Lo screenshot seguente mostra il menu di scelta rapida in Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="9108c-439">The following screen shot shows the context menu in Windows Media Player 11:</span></span>

![screenshot che illustra come accedere al centro informazioni di un negozio in Windows Media Player 11](images/wmp11-info-center.png)

<span data-ttu-id="9108c-441">In Windows 7 con Windows Media Player 12, fare clic con il pulsante destro del mouse sulla finestra Now-playing, scegliere **visualizzazioni** dal menu di scelta rapida e quindi fare clic su **visualizzazione centro informazioni**.</span><span class="sxs-lookup"><span data-stu-id="9108c-441">In Windows 7 with Windows Media Player 12, right-click the now-playing window, on the context menu select **Visualizations**, and then click **Info Center View**.</span></span>

<span data-ttu-id="9108c-442">Lo screenshot seguente mostra il menu di scelta rapida in Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="9108c-442">The following screen shot shows the context menu in Windows Media Player 12:</span></span>

![screenshot che illustra come accedere al centro informazioni di un negozio in Windows Media Player 12](images/wmp12-info-center.png)

<span data-ttu-id="9108c-444">**Per verificare che il centro informazioni funzioni**</span><span class="sxs-lookup"><span data-stu-id="9108c-444">**To verify that the Info Center is functional**</span></span>

-   <span data-ttu-id="9108c-445">Verificare che il centro informazioni mostri informazioni sui supporti nell'area di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="9108c-445">Verify that the Info Center shows media information in the now-playing area.</span></span> <span data-ttu-id="9108c-446">Lo screenshot seguente mostra un esempio di tali informazioni sui supporti:</span><span class="sxs-lookup"><span data-stu-id="9108c-446">The following screen shot shows an example of such media information:</span></span>

    ![screenshot che mostra la funzionalità del centro informazioni di un negozio](images/media-information.png)

<span data-ttu-id="9108c-448">Se nella pagina vengono visualizzati collegamenti di acquisto o altri collegamenti, fare clic sui collegamenti.</span><span class="sxs-lookup"><span data-stu-id="9108c-448">If any buy links or other links appear on the page, click the links.</span></span>

<span data-ttu-id="9108c-449">**Per verificare i collegamenti nella visualizzazione del centro informazioni**</span><span class="sxs-lookup"><span data-stu-id="9108c-449">**To verify links in the Info Center view**</span></span>

-   <span data-ttu-id="9108c-450">Verificare che i collegamenti visualizzino l'archivio.</span><span class="sxs-lookup"><span data-stu-id="9108c-450">Verify that the links show the store.</span></span>

    <span data-ttu-id="9108c-451">Il Media Player di Windows dovrebbe passare all'archivio nella propria libreria.</span><span class="sxs-lookup"><span data-stu-id="9108c-451">The Windows Media Player should switch to the store in its library.</span></span>

## <a name="store-interaction"></a><span data-ttu-id="9108c-452">Interazione archivio</span><span class="sxs-lookup"><span data-stu-id="9108c-452">Store Interaction</span></span>

<span data-ttu-id="9108c-453">Le sezioni seguenti descrivono come testare l'interazione tra gli altri archivi e l'archivio che si sta testando.</span><span class="sxs-lookup"><span data-stu-id="9108c-453">The following sections describe how to test interaction between the other stores and the store that you are testing.</span></span>

### <a name="yielding-to-the-active-store"></a><span data-ttu-id="9108c-454">Cedendo all'archivio attivo</span><span class="sxs-lookup"><span data-stu-id="9108c-454">Yielding to the Active Store</span></span>

<span data-ttu-id="9108c-455">Passa a un archivio diverso da quello testato.</span><span class="sxs-lookup"><span data-stu-id="9108c-455">Switch to a store other than the store being tested.</span></span>

<span data-ttu-id="9108c-456">**Per verificare il cedimento all'archivio attivo**</span><span class="sxs-lookup"><span data-stu-id="9108c-456">**To verify yielding to the active store**</span></span>

-   <span data-ttu-id="9108c-457">Verificare che l'archivio testato venga restituito nell'archivio attivo.</span><span class="sxs-lookup"><span data-stu-id="9108c-457">Verify that the tested store yields to the active store.</span></span>

### <a name="preventing-the-tested-store-from-taking-over-the-active-store"></a><span data-ttu-id="9108c-458">Impedire all'archivio testato di assumere l'archivio attivo</span><span class="sxs-lookup"><span data-stu-id="9108c-458">Preventing the Tested Store From Taking Over the Active Store</span></span>

-   <span data-ttu-id="9108c-459">Con un altro archivio selezionato, chiudere Windows Media Player e riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="9108c-459">With another store selected, close Windows Media Player and restart the computer.</span></span>
-   <span data-ttu-id="9108c-460">Avviare Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9108c-460">Launch Windows Media Player.</span></span>

<span data-ttu-id="9108c-461">**Per verificare che l'archivio testato non riprenda**</span><span class="sxs-lookup"><span data-stu-id="9108c-461">**To verify that the tested store does not take over**</span></span>

-   <span data-ttu-id="9108c-462">Verificare che venga visualizzato l'archivio attivo più di recente e che l'archivio testato non venga visualizzato.</span><span class="sxs-lookup"><span data-stu-id="9108c-462">Verify that the most recently active store appears and that the tested store does not appear.</span></span>

### <a name="accessing-a-store-in-high-contrast-mode"></a><span data-ttu-id="9108c-463">Accesso a un archivio in modalità High-Contrast</span><span class="sxs-lookup"><span data-stu-id="9108c-463">Accessing a Store in High-Contrast Mode</span></span>

<span data-ttu-id="9108c-464">Per prima cosa abilitare la modalità a contrasto elevato premendo MAIUSC a sinistra + ALT di sinistra + STAMP, quindi eseguire i passaggi seguenti per verificare l'accessibilità a contrasto elevato:</span><span class="sxs-lookup"><span data-stu-id="9108c-464">First enable high-contrast mode by pressing LEFT SHIFT+LEFT ALT+PRINT SCREEN, and then perform the following steps to verify high-contrast accessibility:</span></span>

<span data-ttu-id="9108c-465">**Per verificare che l'archivio sia accessibile in modalità a contrasto elevato**</span><span class="sxs-lookup"><span data-stu-id="9108c-465">**To verify that the store is accessible in high-contrast mode**</span></span>

1.  <span data-ttu-id="9108c-466">Verificare che l'interfaccia utente di accesso sia intatta e funzionante.</span><span class="sxs-lookup"><span data-stu-id="9108c-466">Verify that the log-in user interface is intact and functional.</span></span>
2.  <span data-ttu-id="9108c-467">Verificare che tutte le finestre e le finestre di dialogo vengano visualizzate correttamente.</span><span class="sxs-lookup"><span data-stu-id="9108c-467">Verify that all windows and dialog boxes appear correctly.</span></span>
3.  <span data-ttu-id="9108c-468">Acquistare supporti.</span><span class="sxs-lookup"><span data-stu-id="9108c-468">Purchase media.</span></span> <span data-ttu-id="9108c-469">Verificare che i pulsanti per l'acquisto e il download, i manager di download, le informazioni sui prezzi e così via siano visibili.</span><span class="sxs-lookup"><span data-stu-id="9108c-469">Verify that purchase and download buttons, download managers, price information, and so on is visible.</span></span>
4.  <span data-ttu-id="9108c-470">Verificare che sia possibile trasmettere, masterizzare e sincronizzare.</span><span class="sxs-lookup"><span data-stu-id="9108c-470">Verify that you can stream, burn, and synchronize.</span></span>
5.  <span data-ttu-id="9108c-471">Cercare elementi di testo e interfaccia utente ritagliati, testo non leggibile e altri difetti visibili.</span><span class="sxs-lookup"><span data-stu-id="9108c-471">Look for clipped text and user-interface elements, text that is not legible, and other visible defects.</span></span>

### <a name="securing-a-store"></a><span data-ttu-id="9108c-472">Protezione di un archivio</span><span class="sxs-lookup"><span data-stu-id="9108c-472">Securing a Store</span></span>

<span data-ttu-id="9108c-473">Per verificare la sicurezza dell'account, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="9108c-473">Perform the following steps to verify account security:</span></span>

<span data-ttu-id="9108c-474">**Per verificare la sicurezza dell'account**</span><span class="sxs-lookup"><span data-stu-id="9108c-474">**To verify account security**</span></span>

1.  <span data-ttu-id="9108c-475">Immettere le informazioni relative all'account con formato non valido nella pagina e nella finestra di dialogo di accesso e verificare che l'archivio la rifiuti.</span><span class="sxs-lookup"><span data-stu-id="9108c-475">Enter malformed account information into the log-in page and dialog box and verify that the store rejects it.</span></span>
2.  <span data-ttu-id="9108c-476">Accedere, visualizzare la pagina dell'account e disconnettersi.</span><span class="sxs-lookup"><span data-stu-id="9108c-476">Sign in, view the account page, and sign out.</span></span>
3.  <span data-ttu-id="9108c-477">Fare clic sul pulsante indietro in Windows Media Player e verificare di non visualizzare le informazioni sull'account utente precedente.</span><span class="sxs-lookup"><span data-stu-id="9108c-477">Click the back button in Windows Media Player, and verify that you do not see the previous user account information.</span></span>

 

 





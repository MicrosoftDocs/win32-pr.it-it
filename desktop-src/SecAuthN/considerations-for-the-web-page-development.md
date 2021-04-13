---
description: Il broker di autenticazione Web si basa sulle stesse tecnologie di Internet Explorer in Windows.
ms.assetid: 4BBAE30F-63AB-4AB0-9C99-016EF05220E8
title: Considerazioni relative allo sviluppo di pagine Web
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbe7e738616589afc4f7ba4f03d92a12207d189c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346006"
---
# <a name="considerations-for-the-web-page-development"></a><span data-ttu-id="99547-103">Considerazioni relative allo sviluppo di pagine Web</span><span class="sxs-lookup"><span data-stu-id="99547-103">Considerations for the web page development</span></span>

<span data-ttu-id="99547-104">Il broker di autenticazione Web si basa sulle stesse tecnologie di Internet Explorer in Windows.</span><span class="sxs-lookup"><span data-stu-id="99547-104">Web Authentication Broker is built on the top of the same technologies that power Internet Explorer in Windows.</span></span> <span data-ttu-id="99547-105">Tuttavia, a causa di uno scopo speciale di questo componente alcune funzionalità di Internet Explorer sono state disabilitate o bloccate a una configurazione specifica.</span><span class="sxs-lookup"><span data-stu-id="99547-105">However, due to a very special purpose of this component some features of the Internet Explorer were disabled or locked to specific configuration.</span></span> <span data-ttu-id="99547-106">Inoltre, il broker di autenticazione Web fornisce un canale di registrazione eventi dedicato per facilitare la risoluzione dei problemi relativi alle pagine elaborate.</span><span class="sxs-lookup"><span data-stu-id="99547-106">Also, Web Authentication Broker provides a dedicated event logging channel to help troubleshoot issues with pages that it processes.</span></span>

## <a name="internet-explorer-10-standard-document-mode"></a><span data-ttu-id="99547-107">Modalità documento standard di Internet Explorer 10</span><span class="sxs-lookup"><span data-stu-id="99547-107">Internet Explorer 10 standard document mode</span></span>

<span data-ttu-id="99547-108">Il broker di autenticazione Web Visualizza tutte le pagine in "modalità standard IE10".</span><span class="sxs-lookup"><span data-stu-id="99547-108">The Web Authentication Broker displays all pages in the "IE10 Standards Mode".</span></span> <span data-ttu-id="99547-109">È possibile utilizzare gli strumenti di sviluppo di Internet Explorer per vedere il funzionamento della pagina in modalità documento diverse.</span><span class="sxs-lookup"><span data-stu-id="99547-109">You can use the developer tools in Internet Explorer to see how your page works under different document modes.</span></span> <span data-ttu-id="99547-110">Per ulteriori informazioni sulla compatibilità con Internet Explorer 10, vedere gli argomenti MSDN per [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="99547-110">For more information on Internet Explorer 10 compatibility, see the MSDN topics for [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).</span></span>

## <a name="disabled-and-locked-down-features"></a><span data-ttu-id="99547-111">Funzionalità disabilitate e bloccate</span><span class="sxs-lookup"><span data-stu-id="99547-111">Disabled and locked down features</span></span>

<span data-ttu-id="99547-112">Diverse funzionalità di Internet Explorer sono completamente disabilitate o bloccate in base a valori specifici che non possono essere modificati nelle opzioni Internet del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="99547-112">Several features of Internet Explorer are either completely disabled or locked down to specific values that can’t be changed in the Internet Options of the operating system.</span></span>



| <span data-ttu-id="99547-113">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="99547-113">Feature</span></span>                            | <span data-ttu-id="99547-114">Stato</span><span class="sxs-lookup"><span data-stu-id="99547-114">Status</span></span>                                                                                                                                                                                                          |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99547-115">API della cache dell'applicazione ("AppCache")</span><span class="sxs-lookup"><span data-stu-id="99547-115">Application Cache API ("AppCache")</span></span> | <span data-ttu-id="99547-116">Disabled</span><span class="sxs-lookup"><span data-stu-id="99547-116">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="99547-117">Cronologia collegamenti</span><span class="sxs-lookup"><span data-stu-id="99547-117">Link history</span></span>                       | <span data-ttu-id="99547-118">Disabled</span><span class="sxs-lookup"><span data-stu-id="99547-118">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="99547-119">File temporanei</span><span class="sxs-lookup"><span data-stu-id="99547-119">Temporary files</span></span>                    | <span data-ttu-id="99547-120">Abilitato</span><span class="sxs-lookup"><span data-stu-id="99547-120">Enabled</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="99547-121">Cookie</span><span class="sxs-lookup"><span data-stu-id="99547-121">Cookies</span></span>                            | <span data-ttu-id="99547-122">I cookie di sessione sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="99547-122">Session cookies are enabled.</span></span> <span data-ttu-id="99547-123">I cookie salvati in modo permanente sono consentiti, ma sono soggetti a pulizia automatica, a meno che il broker di autenticazione Web non sia in modalità SSO.</span><span class="sxs-lookup"><span data-stu-id="99547-123">Persisted cookies are allowed, but are subject to automatic cleanup unless the Web Authentication Broker is in the SSO mode.</span></span> <span data-ttu-id="99547-124">Per ulteriori informazioni, vedere la sezione Single Sign-on.</span><span class="sxs-lookup"><span data-stu-id="99547-124">For more information, see the Single Sign On section.</span></span> |
| <span data-ttu-id="99547-125">DATABASE di indice</span><span class="sxs-lookup"><span data-stu-id="99547-125">Index DB</span></span>                           | <span data-ttu-id="99547-126">Disabled</span><span class="sxs-lookup"><span data-stu-id="99547-126">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="99547-127">Archiviazione DOM</span><span class="sxs-lookup"><span data-stu-id="99547-127">DOM storage</span></span>                        | <span data-ttu-id="99547-128">Disabled</span><span class="sxs-lookup"><span data-stu-id="99547-128">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="99547-129">ActiveX</span><span class="sxs-lookup"><span data-stu-id="99547-129">ActiveX</span></span>                            | <span data-ttu-id="99547-130">Disabled</span><span class="sxs-lookup"><span data-stu-id="99547-130">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="99547-131">Download di file</span><span class="sxs-lookup"><span data-stu-id="99547-131">File downloads</span></span>                     | <span data-ttu-id="99547-132">Disabled</span><span class="sxs-lookup"><span data-stu-id="99547-132">Disabled</span></span>                                                                                                                                                                                                        |



 

## <a name="https-requirement"></a><span data-ttu-id="99547-133">Requisito HTTPS</span><span class="sxs-lookup"><span data-stu-id="99547-133">HTTPS requirement</span></span>

<span data-ttu-id="99547-134">Il primo URL che un'applicazione userà per comunicare con il provider online deve essere HTTPS.</span><span class="sxs-lookup"><span data-stu-id="99547-134">The first URL that an application will use to communicate with the online provider is required to be HTTPS.</span></span>

## <a name="dimension-for-different-window-sizes"></a><span data-ttu-id="99547-135">Dimensione per diverse dimensioni della finestra</span><span class="sxs-lookup"><span data-stu-id="99547-135">Dimension for different window sizes</span></span>

<span data-ttu-id="99547-136">Un'app di Windows 8 può essere visualizzata in diverse dimensioni, ad esempio a schermo intero, a una finestra ridimensionata o all'interno di un fascino, ad esempio l'accesso alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="99547-136">A Windows 8 app may appear in several different sizes such as full screen, a resized window, or within a Charm such as Share Charm.</span></span> <span data-ttu-id="99547-137">A seconda del layout della finestra in cui viene visualizzato il broker di autenticazione Web, le dimensioni con cui le pagine Web devono funzionare potrebbero essere diverse.</span><span class="sxs-lookup"><span data-stu-id="99547-137">Depending in which window layout the Web Authentication Broker appears, the size with which the web pages have to work could be different.</span></span> <span data-ttu-id="99547-138">Per ulteriori informazioni, vedere l'argomento [linee guida per il ridimensionamento in layout ristretti](/previous-versions/windows/hh465371(v=win.10)) e le [linee guida per la condivisione del contenuto](/previous-versions/windows/hh465251(v=win.10)) .</span><span class="sxs-lookup"><span data-stu-id="99547-138">For more information, see the [Guidelines for resizing to narrow layouts](/previous-versions/windows/hh465371(v=win.10)) topic and the [Guidelines for sharing content](/previous-versions/windows/hh465251(v=win.10)) topic.</span></span>

<span data-ttu-id="99547-139">La pagina Web deve usare le query per supporti CSS per verificare le dimensioni necessarie per l'uso e il lay-out di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="99547-139">The web page should use CSS media queries to check the size it has to work with and lay itself out accordingly.</span></span> <span data-ttu-id="99547-140">La pagina, tuttavia, non deve essere progettata in base ai pixel esatti documentati in questo articolo e deve essere in grado di ridimensionare le diverse dimensioni.</span><span class="sxs-lookup"><span data-stu-id="99547-140">However, the page should not be designed based on the exact pixels documented here and should be able to scale to different sizes.</span></span> <span data-ttu-id="99547-141">Le dimensioni specificate in questo documento sono soggette a modifiche nelle versioni future del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="99547-141">The sizes specified in this document are subject to change in future OS versions.</span></span>

<span data-ttu-id="99547-142">Se una pagina non può contenere tutte le informazioni nello spazio assegnato, ad esempio un lungo elenco di autorizzazioni richieste da un'applicazione, il broker di autenticazione Web fornirà barre di scorrimento per consentire all'utente di scorrere la pagina in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="99547-142">If a page can’t fit all of the information in the allotted space (for example, a long list of permissions that an application is requesting), the Web Authentication Broker will provide scroll bars to allow the user to scroll the page as needed.</span></span> <span data-ttu-id="99547-143">Lo zoom è fornito anche da Pinch zoom per i dispositivi basati su tocco e CTRL + rotellina del mouse per PC desktop e portatili.</span><span class="sxs-lookup"><span data-stu-id="99547-143">Zooming is also provided by pinch zoom for touch-based devices and Ctrl + mouse wheel for desktop and laptop PCs.</span></span>

<span data-ttu-id="99547-144">Per testare diversi fattori di scalabilità, usare l' [app di esempio Web Authentication broker SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) caricata in Microsoft Visual Studio Professional 2012, che consente di simulare lo schermo intero e gli stati ridimensionati.</span><span class="sxs-lookup"><span data-stu-id="99547-144">To test different scaling factors use the [Web Authentication Broker SDK sample app](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) loaded in Microsoft Visual Studio Professional 2012 which allows simulating the full screen and resized states.</span></span>

<span data-ttu-id="99547-145">Oltre ai diversi layout documentati in precedenza, assicurarsi di testare la pagina in modo diverso, ad esempio verticale e orizzontale, con diverse impostazioni locali e lingue, nonché con funzionalità di accessibilità come l'opzione "Rendi tutto più grande" attivata.</span><span class="sxs-lookup"><span data-stu-id="99547-145">In addition to different layouts documented above, make sure to test your page in different screen orientation (for example, portrait and landscape), and different locales and languages as well as with accessibility features such as the "Make everything bigger" option turned on.</span></span>

<span data-ttu-id="99547-146">I layout disponibili sono:</span><span class="sxs-lookup"><span data-stu-id="99547-146">The available layouts are:</span></span>

-   [<span data-ttu-id="99547-147">Schermo intero</span><span class="sxs-lookup"><span data-stu-id="99547-147">Full screen</span></span>](#full-screen)
-   [<span data-ttu-id="99547-148">Finestra ridimensionata</span><span class="sxs-lookup"><span data-stu-id="99547-148">Resized window</span></span>](#resized)
-   [<span data-ttu-id="99547-149">Visualizzazione Charm</span><span class="sxs-lookup"><span data-stu-id="99547-149">Charm view</span></span>](#charm-view)
-   [<span data-ttu-id="99547-150">Visualizzazione selezione file</span><span class="sxs-lookup"><span data-stu-id="99547-150">File picker view</span></span>](#file-picker-view)

### <a name="full-screen"></a><span data-ttu-id="99547-151">Schermo intero</span><span class="sxs-lookup"><span data-stu-id="99547-151">Full screen</span></span>

<span data-ttu-id="99547-152">Per il layout a schermo intero, le dimensioni della pagina Web sono:</span><span class="sxs-lookup"><span data-stu-id="99547-152">For the full screen layout, the web page dimensions are:</span></span>

-   <span data-ttu-id="99547-153">Larghezza: 566 pixel</span><span class="sxs-lookup"><span data-stu-id="99547-153">Width: 566 pixels</span></span>
-   <span data-ttu-id="99547-154">Height: altezza dello schermo (dipende dalla risoluzione dello schermo)</span><span class="sxs-lookup"><span data-stu-id="99547-154">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="99547-155">Nell'esempio seguente viene illustrata l'interfaccia utente di broker di autenticazione Web nel layout a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="99547-155">The following example shows the web authentication broker UI in full screen layout.</span></span>

![esempio di interfaccia utente di broker di autenticazione Web nel layout a schermo intero](images/wab-figure2.png)

### <a name="resized"></a><span data-ttu-id="99547-157">Ridimensionata</span><span class="sxs-lookup"><span data-stu-id="99547-157">Resized</span></span>

<span data-ttu-id="99547-158">Per una finestra ridimensionata, le dimensioni della pagina Web possono essere:</span><span class="sxs-lookup"><span data-stu-id="99547-158">For a resized window, the web page dimensions can be:</span></span>

-   <span data-ttu-id="99547-159">Larghezza: 260 pixel</span><span class="sxs-lookup"><span data-stu-id="99547-159">Width: 260 pixels</span></span>
-   <span data-ttu-id="99547-160">Height: altezza dello schermo (dipende dalla risoluzione dello schermo)</span><span class="sxs-lookup"><span data-stu-id="99547-160">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="99547-161">Nell'esempio seguente viene illustrata l'interfaccia utente di broker di autenticazione Web in una finestra ridimensionata nella pagina Web XBox.</span><span class="sxs-lookup"><span data-stu-id="99547-161">The following example shows the Web Authentication Broker UI in a resized window on the XBox web page.</span></span> <span data-ttu-id="99547-162">Si noti che l'interfaccia utente di broker di autenticazione Web si trova solo sul lato destro dell'acquisizione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="99547-162">Note that the Web Authentication Broker UI is only on the right side of the screen capture.</span></span>

![esempio di interfaccia utente di broker di autenticazione Web in una finestra ridimensionata](images/wab-figure3.png)

### <a name="charm-view"></a><span data-ttu-id="99547-164">Visualizzazione Charm</span><span class="sxs-lookup"><span data-stu-id="99547-164">Charm view</span></span>

<span data-ttu-id="99547-165">Per la visualizzazione Charm, le dimensioni della pagina Web sono:</span><span class="sxs-lookup"><span data-stu-id="99547-165">For the Charm view, the web page dimensions are:</span></span>

-   <span data-ttu-id="99547-166">Larghezza: 566 pixel</span><span class="sxs-lookup"><span data-stu-id="99547-166">Width: 566 pixels</span></span>
-   <span data-ttu-id="99547-167">Height: altezza dello schermo (dipende dalla risoluzione dello schermo)</span><span class="sxs-lookup"><span data-stu-id="99547-167">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="99547-168">Nell'esempio seguente viene illustrata l'interfaccia utente di broker di autenticazione Web nella visualizzazione Charm.</span><span class="sxs-lookup"><span data-stu-id="99547-168">The following example shows the Web Authentication Broker UI in Charm view.</span></span>

![un esempio mostra l'interfaccia utente di broker di autenticazione Web nella visualizzazione Charm](images/wab-figure4.png)

### <a name="file-picker-view"></a><span data-ttu-id="99547-170">Visualizzazione selezione file</span><span class="sxs-lookup"><span data-stu-id="99547-170">File picker view</span></span>

<span data-ttu-id="99547-171">Per la visualizzazione selezione file, le dimensioni della pagina Web sono:</span><span class="sxs-lookup"><span data-stu-id="99547-171">For the file picker view, the web page dimensions are:</span></span>

-   <span data-ttu-id="99547-172">Larghezza: 566 pixel</span><span class="sxs-lookup"><span data-stu-id="99547-172">Width: 566 pixels</span></span>
-   <span data-ttu-id="99547-173">Height: altezza dello schermo (dipende dalla risoluzione dello schermo)</span><span class="sxs-lookup"><span data-stu-id="99547-173">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="99547-174">Nell'esempio seguente viene illustrata l'interfaccia utente di broker di autenticazione Web nella visualizzazione di selezione file.</span><span class="sxs-lookup"><span data-stu-id="99547-174">The following example shows the Web Authentication Broker UI in file picker view.</span></span>

![un esempio mostra l'interfaccia utente di broker di autenticazione Web nella visualizzazione selezione file](images/wab-figure5.png)

## <a name="no-new-windows-by-default"></a><span data-ttu-id="99547-176">Nessuna nuova finestra per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="99547-176">No new windows by default</span></span>

<span data-ttu-id="99547-177">Per impostazione predefinita, nessun URL provocherà l'apertura di una nuova finestra, ma verrà invece visualizzata nella finestra gestore di autenticazione Web.</span><span class="sxs-lookup"><span data-stu-id="99547-177">By default, no URLs will result in a new window being opened but will instead be displayed within the Web Authentication Broker window.</span></span> <span data-ttu-id="99547-178">Questo include il metodo JavaScript Window. Open, l'attributo "target" dei collegamenti ipertestuali oppure quando l'utente usa il meccanismo CTRL + clic per forzare l'apertura di una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="99547-178">This includes window.open JavaScript method, "target" attribute of the hyperlinks, or when the user uses the Ctrl+Click mechanism to force a new window to open.</span></span> <span data-ttu-id="99547-179">L'eccezione a questa regola si verifica quando una pagina Web dichiara un collegamento come sicuro per spostarsi in un browser, come descritto nella pagina relativa alla personalizzazione della destinazione dei collegamenti ipertestuali.</span><span class="sxs-lookup"><span data-stu-id="99547-179">The exception to this rule is when a web page declares a link as safe to be navigated in a browser as described in the Customizing Target of the Hyperlinks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99547-180">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99547-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99547-181">App di esempio SDK Web Authentication broker</span><span class="sxs-lookup"><span data-stu-id="99547-181">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="99547-182">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="99547-182">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 

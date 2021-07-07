---
description: In questo argomento vengono descritte le procedure consigliate per la progettazione di pagine Web che utilizzano Gestore autenticazione Web per l'accesso.
ms.assetid: 271EC68B-5E58-4C1C-B631-DED6A694E98F
title: Procedure consigliate per la progettazione di pagine Web di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdd6ab5dc067c23cfb29d21d2ff4780cee0ef1c
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353674"
---
# <a name="best-practices-for-designing-authentication-web-pages"></a><span data-ttu-id="47923-103">Procedure consigliate per la progettazione di pagine Web di autenticazione</span><span class="sxs-lookup"><span data-stu-id="47923-103">Best Practices for designing authentication web pages</span></span>

<span data-ttu-id="47923-104">In questo argomento vengono descritte le procedure consigliate per la progettazione di pagine Web che utilizzano Gestore autenticazione Web per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="47923-104">This topic describes best practices for designing web pages that use Web Authentication Broker for logging on.</span></span>

-   [<span data-ttu-id="47923-105">Uso di metatag</span><span class="sxs-lookup"><span data-stu-id="47923-105">Use of metatags</span></span>](#use-of-metatags)
-   [<span data-ttu-id="47923-106">Uso di stili WINDOWS 8 CSS</span><span class="sxs-lookup"><span data-stu-id="47923-106">Use of Windows 8 CSS styling</span></span>](#use-of-windows-8-css-styling)
-   [<span data-ttu-id="47923-107">Uso di colori e temi</span><span class="sxs-lookup"><span data-stu-id="47923-107">Use of color and themes</span></span>](#use-of-color-and-themes)
-   [<span data-ttu-id="47923-108">Allineamento</span><span class="sxs-lookup"><span data-stu-id="47923-108">Alignment</span></span>](#alignment)
-   [<span data-ttu-id="47923-109">Progettazione per Snap</span><span class="sxs-lookup"><span data-stu-id="47923-109">Designing for snap</span></span>](#designing-for-snap)
-   [<span data-ttu-id="47923-110">Progettazione per un'esperienza di accesso veloce e fluida</span><span class="sxs-lookup"><span data-stu-id="47923-110">Designing for a fast and fluid login experience</span></span>](#designing-for-a-fast-and-fluid-login-experience)
-   [<span data-ttu-id="47923-111">Security Considerations</span><span class="sxs-lookup"><span data-stu-id="47923-111">Security Considerations</span></span>](#security-considerations)
-   [<span data-ttu-id="47923-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="47923-112">Related topics</span></span>](#related-topics)

## <a name="use-of-metatags"></a><span data-ttu-id="47923-113">Uso di metatag</span><span class="sxs-lookup"><span data-stu-id="47923-113">Use of metatags</span></span>

<span data-ttu-id="47923-114">Usando i metatag, il provider "Contoso Social" può specificare il titolo, l'icona e il colore dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="47923-114">Using metatags, the provider "Contoso Social" can specify the title, the icon and the color of the header.</span></span> <span data-ttu-id="47923-115">Nel file HTML di esempio (WebAuthLogin.html), questa operazione viene eseguita usando il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="47923-115">In the sample HTML file (WebAuthLogin.html), this is done by using the following code.</span></span>


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



<span data-ttu-id="47923-116">Ciò consente Windows integrare la presenza del provider in modo evidente nell'intestazione dell'interfaccia utente, come evidenziato dalla casella rossa nello screenshot seguente.</span><span class="sxs-lookup"><span data-stu-id="47923-116">This allows Windows to integrate the presence of the provider in a prominent way in the header of the UI as highlighted by the red box in the following screenshot.</span></span> ![Pagina di accesso che mostra l'intestazione contoso nell'interfaccia utente](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a><span data-ttu-id="47923-118">Uso di stili WINDOWS 8 CSS</span><span class="sxs-lookup"><span data-stu-id="47923-118">Use of Windows 8 CSS styling</span></span>

<span data-ttu-id="47923-119">Il foglio di stile ui-light.css fornito è il foglio Windows 8 stile usato dalle app Windows Store.</span><span class="sxs-lookup"><span data-stu-id="47923-119">The provided ui-light.css stylesheet is the Windows 8 stylesheet used by Windows Store apps.</span></span> <span data-ttu-id="47923-120">Definisce lo stile Windows app dello Store per la tipografia e i controlli standard, ad esempio pulsanti, caselle di testo, collegamenti ipertestuali e caselle di controllo per assicurarsi che siano simili al tocco.</span><span class="sxs-lookup"><span data-stu-id="47923-120">It defines Windows Store app styling for typography and standard controls, like buttons, text boxes, hyperlinks, and check boxes to make sure they are touch friendly.</span></span> <span data-ttu-id="47923-121">Quando si progettano e si personalizzano le pagine di autorizzazione Web per Windows 8, si consiglia di usare questo foglio di stile così come è e aggiornarlo in base alle esigenze, purché la pagina Web segua comunque le procedure consigliate a sé stante.</span><span class="sxs-lookup"><span data-stu-id="47923-121">When designing and tailoring web authorization pages for Windows 8, we encourage you to use this stylesheet as is and update it as needed as long as your web page still follows best-practices in its own way.</span></span>

<span data-ttu-id="47923-122">Ad esempio, se si dispone di un foglio di stile speciale per l'aspetto dei collegamenti ipertestuali nella pagina Web, è consigliabile assicurarsi che lo stile fornito sia touch friendly allo stesso modo dei collegamenti ipertestuali Windows 8 standard.</span><span class="sxs-lookup"><span data-stu-id="47923-122">For example, if you have a special stylesheet for what hyperlinks should look and feel like on your web page, it's good to be thoughtful to make sure that the styling you provide is touch friendly in the same way as standard Windows 8 hyperlinks.</span></span> <span data-ttu-id="47923-123">Questo è essenziale per la base di consumer che usa Windows 8 dispositivi touch.</span><span class="sxs-lookup"><span data-stu-id="47923-123">This is essential for the consumer base using Windows 8 on their touch devices.</span></span>

## <a name="use-of-color-and-themes"></a><span data-ttu-id="47923-124">Uso di colori e temi</span><span class="sxs-lookup"><span data-stu-id="47923-124">Use of color and themes</span></span>

<span data-ttu-id="47923-125">In questo esempio viene illustrato un uso riflessivo del colore in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="47923-125">This sample demonstrates a thoughtful use of color in a few different ways.</span></span>

-   <span data-ttu-id="47923-126">Sfondo bianco per la pagina Web.</span><span class="sxs-lookup"><span data-stu-id="47923-126">White background for the web page.</span></span> <span data-ttu-id="47923-127">Come si può vedere dallo screenshot precedente, la pagina Web è ospitata all'interno di una superficie bianca che si estende sulla larghezza dello schermo.</span><span class="sxs-lookup"><span data-stu-id="47923-127">As you can tell from the previous screenshot, the web page is hosted within a white surface that spans the width of the screen.</span></span> <span data-ttu-id="47923-128">Per assicurarsi che la pagina Web si integri con la superficie, è consigliabile che la pagina Web abbia uno sfondo bianco.</span><span class="sxs-lookup"><span data-stu-id="47923-128">To make sure that the web page integrates with the surface, it is advised that the web page should have a white background.</span></span>
-   <span data-ttu-id="47923-129">Colorazione dei controlli in base al colore del marchio.</span><span class="sxs-lookup"><span data-stu-id="47923-129">Colorizing controls based on your brand color.</span></span> <span data-ttu-id="47923-130">Il file CSS theme-colors.css fornisce lo stile per eseguire l'override dei colori standard dei controlli nel foglio di stile dell'interfaccia utente in modo da associare i temi dei controlli al colore dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="47923-130">The CSS file theme-colors.css provides styling to override the standard colors of controls in the ui-light stylesheet to match the theming of the controls to the color of the header.</span></span> <span data-ttu-id="47923-131">Nello screenshot seguente, ad esempio, i pulsanti e i collegamenti ipertestuali accettano i colori derivati dal colore dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="47923-131">For example, in the following screenshot, the buttons and hyperlinks take on colors derived from the header color.</span></span> ![screenshot dei pulsanti e del testo con lo stesso colore dell'intestazione](images/wab-figure11.png)
-   <span data-ttu-id="47923-133">Colore dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="47923-133">Header color.</span></span> <span data-ttu-id="47923-134">L'uso del colore del marchio di Contoso nell'intestazione crea una personalità unificata per il marchio del provider all'interno dell'interfaccia utente del sistema.</span><span class="sxs-lookup"><span data-stu-id="47923-134">The use of Contoso's brand color in the header creates a unified personality for the provider's brand within the system UI.</span></span>

## <a name="alignment"></a><span data-ttu-id="47923-135">Allineamento</span><span class="sxs-lookup"><span data-stu-id="47923-135">Alignment</span></span>

<span data-ttu-id="47923-136">La pagina Web stessa non ha spaziatura interna a sinistra o a destra per consentire l'allineamento tipografico con il titolo nell'intestazione a sinistra e l'icona nell'intestazione a destra.</span><span class="sxs-lookup"><span data-stu-id="47923-136">The web page itself has no padding on the left or the right to allow for typographic alignment with the title in the header on the left and the icon in the header on the right.</span></span>

<span data-ttu-id="47923-137">Si noterà anche che i pulsanti sono sempre allineati in basso a destra nella pagina Web (e a destra con l'icona nell'intestazione).</span><span class="sxs-lookup"><span data-stu-id="47923-137">You will also notice that buttons are always bottom-right aligned in the web page (and right aligned with the icon in the header).</span></span> <span data-ttu-id="47923-138">Si tratta di una procedura consigliata perché Windows 8 utenti saranno abituati a flussi di dialogo simili con pulsanti in basso a destra.</span><span class="sxs-lookup"><span data-stu-id="47923-138">This is best-practice as Windows 8 users will be accustomed to similar dialog flows having buttons in the bottom-right.</span></span>

## <a name="designing-for-snap"></a><span data-ttu-id="47923-139">Progettazione per Snap</span><span class="sxs-lookup"><span data-stu-id="47923-139">Designing for snap</span></span>

<span data-ttu-id="47923-140">Nell'immagine seguente è possibile visualizzare le pagine di accesso e autorizzazioni in stato snap.</span><span class="sxs-lookup"><span data-stu-id="47923-140">In the following image, you can see the login and permissions pages in snap state.</span></span>

![<span data-ttu-id="47923-141">visualizzazione agganciata della schermata di accesso</span><span class="sxs-lookup"><span data-stu-id="47923-141">snap view of the login screen</span></span> ](images/wab-figure12.png) <span data-ttu-id="47923-142">.</span><span class="sxs-lookup"><span data-stu-id="47923-142">.</span></span> ![<span data-ttu-id="47923-143">visualizzazione agganciata della pagina delle autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="47923-143">snap view of the permissions page</span></span> ](images/wab-figure13.png)

<span data-ttu-id="47923-144">Nel file di esempio ui-webauth.css è possibile vedere l'uso di query multimediali che ottimizzano il layout della pagina per lo stato di blocco in base alla larghezza disponibile per la pagina Web.</span><span class="sxs-lookup"><span data-stu-id="47923-144">In the sample file ui-webauth.css, you can see the use of media queries that optimize the layout of the page for snap state based on width available for the web page.</span></span> <span data-ttu-id="47923-145">Il frammento di codice racchiuso nell'ambito seguente implementa CSS personalizzato per lo stato di allineamento.</span><span class="sxs-lookup"><span data-stu-id="47923-145">The code snippet enclosed in the following scope implements CSS tailored for snap state.</span></span>


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



<span data-ttu-id="47923-146">In Windows 8, la larghezza dello stato di allineamento è di 320 pixel.</span><span class="sxs-lookup"><span data-stu-id="47923-146">In Windows 8, the width of the snap state is 320 pixels.</span></span> <span data-ttu-id="47923-147">La pagina di autenticazione Web occupa 260 pixel nell'interfaccia utente precedente.</span><span class="sxs-lookup"><span data-stu-id="47923-147">The web-auth page occupies 260 pixels in the UI above.</span></span> <span data-ttu-id="47923-148">Si sta usando un valore di larghezza massima con un margine sufficiente, quindi il codice media query del provider non è associato alla larghezza esatta dello stato di allineamento.</span><span class="sxs-lookup"><span data-stu-id="47923-148">We're using a max-width value with enough margin, so the media query code of the provider is not bound to the exact width of the snap state.</span></span>

<span data-ttu-id="47923-149">Per personalizzare l'app per la visualizzazione agganciata, è importante che l'utente non perda alcun contesto presente nelle altre visualizzazioni dell'esperienza di autenticazione Web (visualizzazioni complete, di riempimento o di accesso), ma è utile ri strutturare il layout e la gerarchia degli elementi nella pagina in modo che le informazioni necessarie per mantenere il contesto siano visibili e interattive.</span><span class="sxs-lookup"><span data-stu-id="47923-149">In tailoring your app for the snap view, it's important that user does not lose any context that they have in the other views of web auth experience (full, fill or charm views), but it's valuable to re-structure the layout and hierarchy of the elements in the page so that the information needed to retain context is visible and interactive.</span></span> <span data-ttu-id="47923-150">Sono stati illustrati alcuni esempi di come l'esempio personalizza la pagina Web per lo stato di allineamento.</span><span class="sxs-lookup"><span data-stu-id="47923-150">We've called out some examples of how the sample tailors the web page for the snap state.</span></span>

-   <span data-ttu-id="47923-151">Ad esempio, per la pagina di accesso in stato di agganciamento, la proprietà width del campo di testo di input (come specificato in ui-light.css) è stata sottoposta a override ed è stata impostata come valore numerico più piccolo, in modo che il campo di testo non venga ritagliato orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="47923-151">As an example, for the login page in snap state, the width property of the input text field (as specified in ui-light.css) has been overridden and been set as smaller numerical value, so that the text field is not horizontally clipped.</span></span>
-   <span data-ttu-id="47923-152">Come altro esempio, nello stato di allineamento, le dimensioni del carattere delle intestazioni h1 e h2 vengono ridotte rispettivamente a 20 pt e 11 pt da 42 pt e 20 pt.</span><span class="sxs-lookup"><span data-stu-id="47923-152">As another example, in snap state, the font size of the h1 and h2 headers is reduced to 20 pt and 11 pt from 42 pt and 20 pt respectively.</span></span> <span data-ttu-id="47923-153">Questa operazione viene eseguita in base alla Windows 8 e ottimizza il testo in modo che sia più compatto nel viewport modificato.</span><span class="sxs-lookup"><span data-stu-id="47923-153">This is done in accordance with the Windows 8 type ramp, and optimizes text to be more compact in the changed viewport.</span></span>
-   <span data-ttu-id="47923-154">Come altro esempio, si noti che le dimensioni delle icone nella pagina delle autorizzazioni sono inferiori (confrontare con la pagina di visualizzazione completa precedente).</span><span class="sxs-lookup"><span data-stu-id="47923-154">As another example, notice the sizes of the icons in the permissions page are smaller (compare to the full view page above).</span></span> <span data-ttu-id="47923-155">Anche in questo caso, questa operazione viene eseguita per mantenere il contesto, scambiando gli asset di progettazione per quelli più ottimali per il viewport modificato.</span><span class="sxs-lookup"><span data-stu-id="47923-155">Again, this is done to retain context, while swapping design assets for those more optimal for the changed viewport.</span></span>

## <a name="designing-for-a-fast-and-fluid-login-experience"></a><span data-ttu-id="47923-156">Progettazione per un'esperienza di accesso veloce e fluida</span><span class="sxs-lookup"><span data-stu-id="47923-156">Designing for a fast and fluid login experience</span></span>

<span data-ttu-id="47923-157">Nelle prime fasi della progettazione di questa pagina Web è stato preso in gioco il fatto che una delle cose migliori per questa pagina è un'esperienza di accesso veloce e fluida.</span><span class="sxs-lookup"><span data-stu-id="47923-157">Early in the designing of this web page, we made a stake in the ground that one thing that this page is best at is a fast and fluid login experience.</span></span> <span data-ttu-id="47923-158">Di conseguenza, l'interfaccia utente più importante nel flusso è il campo nome utente e password nella pagina di accesso per un'esperienza di immissione rapida delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="47923-158">Thus, the UI that is most prominent in the flow is the username and password field in the login page for a quick credential entry experience.</span></span> <span data-ttu-id="47923-159">Anche se è stato identificato che esistono altri scenari comuni, ad esempio il recupero delle password e il riferimento alle informative sulla privacy, l'esperienza del Web è una posizione migliore per tali esperienze.</span><span class="sxs-lookup"><span data-stu-id="47923-159">While we identified that there are other common scenarios such as password retrieval, and referencing privacy statements, the rich experience of the web is a better place for those experiences.</span></span> <span data-ttu-id="47923-160">Per tutti i flussi non correlati all'esperienza di autenticazione Web sicura, è consigliabile passare l'utente al browser.</span><span class="sxs-lookup"><span data-stu-id="47923-160">For all flows not related to secure web auth experience, we recommend navigating the user to the browser.</span></span> <span data-ttu-id="47923-161">Come illustrato nel file HTML di esempio (WebAuthLogin.html), vengono visualizzate tutte le pagine Web collegate dalla pagina di accesso o delle autorizzazioni nel browser predefinito dell'utente, in cui l'utente può completare questi flussi e quindi tornare `<meta name="mswebdialog-newwindowurl" content="*" />` all'app per accedere.</span><span class="sxs-lookup"><span data-stu-id="47923-161">This is shown in the sample HTML file (WebAuthLogin.html) as follows: `<meta name="mswebdialog-newwindowurl" content="*" />` This opens all web pages linked to from the login or permissions page in the user's default browser where the user can complete these flows and then return to the app to log in.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="47923-162">Considerazioni relative alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="47923-162">Security Considerations</span></span>

<span data-ttu-id="47923-163">Gli articoli seguenti forniscono indicazioni per la scrittura di codice C++ sicuro.</span><span class="sxs-lookup"><span data-stu-id="47923-163">The following articles provide guidance for writing secure C++ code.</span></span>

-   [<span data-ttu-id="47923-164">Procedure di sicurezza consigliate per C++</span><span class="sxs-lookup"><span data-stu-id="47923-164">Security Best Practices for C++</span></span>](/cpp/security/security-best-practices-for-cpp)
-   <span data-ttu-id="47923-165">[Patterns & Practices Security Guidance for Applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="47923-165">[Patterns & Practices Security Guidance for Applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span></span>

## <a name="related-topics"></a><span data-ttu-id="47923-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="47923-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47923-167">Considerazioni relative allo sviluppo di pagine Web</span><span class="sxs-lookup"><span data-stu-id="47923-167">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="47923-168">Domande frequenti su Web Authentication Broker</span><span class="sxs-lookup"><span data-stu-id="47923-168">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.yml)
</dt> <dt>

[<span data-ttu-id="47923-169">App di esempio Web Authentication Broker SDK</span><span class="sxs-lookup"><span data-stu-id="47923-169">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="47923-170">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="47923-170">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 

---
description: Questo argomento descrive le procedure consigliate per la progettazione di pagine Web che usano il broker di autenticazione Web per l'accesso.
ms.assetid: 271EC68B-5E58-4C1C-B631-DED6A694E98F
title: Procedure consigliate per la progettazione di pagine Web di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6360e313b49a69c16aebf532911bcdf562f9a4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344366"
---
# <a name="best-practices-for-designing-authentication-web-pages"></a><span data-ttu-id="4ee5f-103">Procedure consigliate per la progettazione di pagine Web di autenticazione</span><span class="sxs-lookup"><span data-stu-id="4ee5f-103">Best Practices for designing authentication web pages</span></span>

<span data-ttu-id="4ee5f-104">Questo argomento descrive le procedure consigliate per la progettazione di pagine Web che usano il broker di autenticazione Web per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-104">This topic describes best practices for designing web pages that use Web Authentication Broker for logging on.</span></span>

-   [<span data-ttu-id="4ee5f-105">Uso dei metatag</span><span class="sxs-lookup"><span data-stu-id="4ee5f-105">Use of metatags</span></span>](#use-of-metatags)
-   [<span data-ttu-id="4ee5f-106">Uso dello stile CSS di Windows 8</span><span class="sxs-lookup"><span data-stu-id="4ee5f-106">Use of Windows 8 CSS styling</span></span>](#use-of-windows-8-css-styling)
-   [<span data-ttu-id="4ee5f-107">Uso di colori e temi</span><span class="sxs-lookup"><span data-stu-id="4ee5f-107">Use of color and themes</span></span>](#use-of-color-and-themes)
-   [<span data-ttu-id="4ee5f-108">Allineamento</span><span class="sxs-lookup"><span data-stu-id="4ee5f-108">Alignment</span></span>](#alignment)
-   [<span data-ttu-id="4ee5f-109">Progettazione per snap</span><span class="sxs-lookup"><span data-stu-id="4ee5f-109">Designing for snap</span></span>](#designing-for-snap)
-   [<span data-ttu-id="4ee5f-110">Progettazione per un'esperienza di accesso rapida e fluida</span><span class="sxs-lookup"><span data-stu-id="4ee5f-110">Designing for a fast and fluid login experience</span></span>](#designing-for-a-fast-and-fluid-login-experience)
-   [<span data-ttu-id="4ee5f-111">Security Considerations</span><span class="sxs-lookup"><span data-stu-id="4ee5f-111">Security Considerations</span></span>](#security-considerations)
-   [<span data-ttu-id="4ee5f-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ee5f-112">Related topics</span></span>](#related-topics)

## <a name="use-of-metatags"></a><span data-ttu-id="4ee5f-113">Uso dei metatag</span><span class="sxs-lookup"><span data-stu-id="4ee5f-113">Use of metatags</span></span>

<span data-ttu-id="4ee5f-114">Utilizzando i metatag, il provider "contoso social" può specificare il titolo, l'icona e il colore dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-114">Using metatags, the provider "Contoso Social" can specify the title, the icon and the color of the header.</span></span> <span data-ttu-id="4ee5f-115">Nel file HTML di esempio (WebAuthLogin.html), questa operazione viene eseguita usando il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-115">In the sample HTML file (WebAuthLogin.html), this is done by using the following code.</span></span>


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



<span data-ttu-id="4ee5f-116">Questo consente a Windows di integrare la presenza del provider in modo significativo nell'intestazione dell'interfaccia utente evidenziata dalla casella rossa nello screenshot seguente.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-116">This allows Windows to integrate the presence of the provider in a prominent way in the header of the UI as highlighted by the red box in the following screenshot.</span></span> ![pagina di accesso che mostra l'intestazione Contoso nell'interfaccia utente](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a><span data-ttu-id="4ee5f-118">Uso dello stile CSS di Windows 8</span><span class="sxs-lookup"><span data-stu-id="4ee5f-118">Use of Windows 8 CSS styling</span></span>

<span data-ttu-id="4ee5f-119">Il foglio di stile UI-Light. CSS fornito è il foglio di stile di Windows 8 usato dalle app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-119">The provided ui-light.css stylesheet is the Windows 8 stylesheet used by Windows Store apps.</span></span> <span data-ttu-id="4ee5f-120">Definisce lo stile delle app di Windows Store per la tipografia e i controlli standard, ad esempio pulsanti, caselle di testo, collegamenti ipertestuali e caselle di controllo per assicurarsi che siano compatibili con il tocco.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-120">It defines Windows Store app styling for typography and standard controls, like buttons, text boxes, hyperlinks, and check boxes to make sure they are touch friendly.</span></span> <span data-ttu-id="4ee5f-121">Quando si progettano e si personalizzano le pagine di autorizzazione Web per Windows 8, si consiglia di usare questo foglio di stile e di aggiornarlo in base alle esigenze, purché la pagina Web segua le procedure consigliate in modo specifico.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-121">When designing and tailoring web authorization pages for Windows 8, we encourage you to use this stylesheet as is and update it as needed as long as your web page still follows best-practices in its own way.</span></span>

<span data-ttu-id="4ee5f-122">Se, ad esempio, si dispone di un foglio di stile speciale per i collegamenti ipertestuali che dovrebbero avere un aspetto analogo a quello della pagina Web, è opportuno prestare attenzione a garantire che lo stile fornito sia semplice da usare in modo analogo ai collegamenti ipertestuali standard di Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-122">For example, if you have a special stylesheet for what hyperlinks should look and feel like on your web page, it's good to be thoughtful to make sure that the styling you provide is touch friendly in the same way as standard Windows 8 hyperlinks.</span></span> <span data-ttu-id="4ee5f-123">Questa operazione è essenziale per la base di utenti che usa Windows 8 sui dispositivi touch.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-123">This is essential for the consumer base using Windows 8 on their touch devices.</span></span>

## <a name="use-of-color-and-themes"></a><span data-ttu-id="4ee5f-124">Uso di colori e temi</span><span class="sxs-lookup"><span data-stu-id="4ee5f-124">Use of color and themes</span></span>

<span data-ttu-id="4ee5f-125">In questo esempio viene illustrato un utilizzo ponderato del colore in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-125">This sample demonstrates a thoughtful use of color in a few different ways.</span></span>

-   <span data-ttu-id="4ee5f-126">Sfondo bianco per la pagina Web.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-126">White background for the web page.</span></span> <span data-ttu-id="4ee5f-127">Come si può vedere dallo screenshot precedente, la pagina Web è ospitata all'interno di una superficie bianca che copre la larghezza dello schermo.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-127">As you can tell from the previous screenshot, the web page is hosted within a white surface that spans the width of the screen.</span></span> <span data-ttu-id="4ee5f-128">Per assicurarsi che la pagina Web si integri con la superficie, è consigliabile che la pagina Web disponga di uno sfondo bianco.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-128">To make sure that the web page integrates with the surface, it is advised that the web page should have a white background.</span></span>
-   <span data-ttu-id="4ee5f-129">Colorazione dei controlli in base al colore del marchio.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-129">Colorizing controls based on your brand color.</span></span> <span data-ttu-id="4ee5f-130">Il file CSS Theme-Colors. CSS fornisce lo stile per eseguire l'override dei colori standard dei controlli nel foglio di stile della luce dell'interfaccia utente in modo che corrisponda a quello dei controlli al colore dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-130">The CSS file theme-colors.css provides styling to override the standard colors of controls in the ui-light stylesheet to match the theming of the controls to the color of the header.</span></span> <span data-ttu-id="4ee5f-131">Nello screenshot seguente, ad esempio, i pulsanti e i collegamenti ipertestuali accettano i colori derivati dal colore dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-131">For example, in the following screenshot, the buttons and hyperlinks take on colors derived from the header color.</span></span> ![screenshot dei pulsanti e del testo con lo stesso colore dell'intestazione](images/wab-figure11.png)
-   <span data-ttu-id="4ee5f-133">Colore dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-133">Header color.</span></span> <span data-ttu-id="4ee5f-134">L'uso del colore del marchio di Contoso nell'intestazione crea una personalità unificata per il marchio del provider nell'interfaccia utente del sistema.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-134">The use of Contoso's brand color in the header creates a unified personality for the provider's brand within the system UI.</span></span>

## <a name="alignment"></a><span data-ttu-id="4ee5f-135">Allineamento</span><span class="sxs-lookup"><span data-stu-id="4ee5f-135">Alignment</span></span>

<span data-ttu-id="4ee5f-136">La pagina Web non ha spaziatura interna a sinistra o a destra per consentire l'allineamento tipografico con il titolo nell'intestazione a sinistra e l'icona nell'intestazione a destra.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-136">The web page itself has no padding on the left or the right to allow for typographic alignment with the title in the header on the left and the icon in the header on the right.</span></span>

<span data-ttu-id="4ee5f-137">Si noterà anche che i pulsanti sono sempre allineati in basso a destra nella pagina Web ed è allineato a destra con l'icona nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-137">You will also notice that buttons are always bottom-right aligned in the web page (and right aligned with the icon in the header).</span></span> <span data-ttu-id="4ee5f-138">Si tratta di una procedura consigliata poiché gli utenti di Windows 8 saranno abituati a flussi di finestre di dialogo simili con pulsanti in basso a destra.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-138">This is best-practice as Windows 8 users will be accustomed to similar dialog flows having buttons in the bottom-right.</span></span>

## <a name="designing-for-snap"></a><span data-ttu-id="4ee5f-139">Progettazione per snap</span><span class="sxs-lookup"><span data-stu-id="4ee5f-139">Designing for snap</span></span>

<span data-ttu-id="4ee5f-140">Nell'immagine seguente è possibile visualizzare le pagine account di accesso e autorizzazioni in stato di snap-in.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-140">In the following image, you can see the login and permissions pages in snap state.</span></span>

![<span data-ttu-id="4ee5f-141">visualizzazione snap della schermata di accesso</span><span class="sxs-lookup"><span data-stu-id="4ee5f-141">snap view of the login screen</span></span> ](images/wab-figure12.png) <span data-ttu-id="4ee5f-142">.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-142">.</span></span> ![<span data-ttu-id="4ee5f-143">visualizzazione snap della pagina autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="4ee5f-143">snap view of the permissions page</span></span> ](images/wab-figure13.png)

<span data-ttu-id="4ee5f-144">Nel file di esempio UI-WebAuth. CSS è possibile vedere l'uso di query multimediali per ottimizzare il layout della pagina per lo stato di snap in base alla larghezza disponibile per la pagina Web.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-144">In the sample file ui-webauth.css, you can see the use of media queries that optimize the layout of the page for snap state based on width available for the web page.</span></span> <span data-ttu-id="4ee5f-145">Il frammento di codice incluso nell'ambito seguente implementa il CSS personalizzato per lo stato di snap.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-145">The code snippet enclosed in the following scope implements CSS tailored for snap state.</span></span>


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



<span data-ttu-id="4ee5f-146">In Windows 8, la larghezza dello stato di allineamento è 320 pixel.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-146">In Windows 8, the width of the snap state is 320 pixels.</span></span> <span data-ttu-id="4ee5f-147">La pagina autenticazione Web occupa 260 pixel nell'interfaccia utente precedente.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-147">The web-auth page occupies 260 pixels in the UI above.</span></span> <span data-ttu-id="4ee5f-148">Si sta usando un valore di larghezza massima con un margine sufficiente, quindi il codice di query del supporto del provider non è associato alla larghezza esatta dello stato di allineamento.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-148">We're using a max-width value with enough margin, so the media query code of the provider is not bound to the exact width of the snap state.</span></span>

<span data-ttu-id="4ee5f-149">Per personalizzare l'app per la visualizzazione snap, è importante che l'utente non perda alcun contesto presente nelle altre visualizzazioni dell'esperienza di autenticazione Web (viste Full, Fill o charm), ma è utile ristrutturare il layout e la gerarchia degli elementi nella pagina in modo che le informazioni necessarie per mantenere il contesto siano visibili e interattive.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-149">In tailoring your app for the snap view, it's important that user does not lose any context that they have in the other views of web auth experience (full, fill or charm views), but it's valuable to re-structure the layout and hierarchy of the elements in the page so that the information needed to retain context is visible and interactive.</span></span> <span data-ttu-id="4ee5f-150">Sono stati illustrati alcuni esempi del modo in cui l'esempio segue la pagina Web per lo stato di allineamento.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-150">We've called out some examples of how the sample tailors the web page for the snap state.</span></span>

-   <span data-ttu-id="4ee5f-151">Per la pagina di accesso nello stato di allineamento, ad esempio, la proprietà Width del campo di testo di input (come specificato in UI-Light. CSS) è stata sottoposta a override ed è stata impostata come valore numerico più piccolo, in modo che il campo di testo non venga troncato orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-151">As an example, for the login page in snap state, the width property of the input text field (as specified in ui-light.css) has been overridden and been set as smaller numerical value, so that the text field is not horizontally clipped.</span></span>
-   <span data-ttu-id="4ee5f-152">Come altro esempio, nello stato di snap, le dimensioni del carattere delle intestazioni H1 e H2 vengono ridotte rispettivamente a 20 PT e 11 PT da 42 PT e 20 PT.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-152">As another example, in snap state, the font size of the h1 and h2 headers is reduced to 20 pt and 11 pt from 42 pt and 20 pt respectively.</span></span> <span data-ttu-id="4ee5f-153">Questa operazione viene eseguita in base alla rampa di tipo Windows 8 e ottimizza il testo in modo da essere più compatto nel viewport modificato.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-153">This is done in accordance with the Windows 8 type ramp, and optimizes text to be more compact in the changed viewport.</span></span>
-   <span data-ttu-id="4ee5f-154">Per un altro esempio, si noti che le dimensioni delle icone nella pagina autorizzazioni sono inferiori (confrontare la pagina di visualizzazione completa precedente).</span><span class="sxs-lookup"><span data-stu-id="4ee5f-154">As another example, notice the sizes of the icons in the permissions page are smaller (compare to the full view page above).</span></span> <span data-ttu-id="4ee5f-155">Anche in questo caso, questa operazione viene eseguita per mantenere il contesto, scambiando le risorse di progettazione per quelle più ottimali per il viewport modificato.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-155">Again, this is done to retain context, while swapping design assets for those more optimal for the changed viewport.</span></span>

## <a name="designing-for-a-fast-and-fluid-login-experience"></a><span data-ttu-id="4ee5f-156">Progettazione per un'esperienza di accesso rapida e fluida</span><span class="sxs-lookup"><span data-stu-id="4ee5f-156">Designing for a fast and fluid login experience</span></span>

<span data-ttu-id="4ee5f-157">Nella fase iniziale della progettazione di questa pagina Web, abbiamo creato un punto di interesse per l'accesso rapido e fluido a questa pagina.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-157">Early in the designing of this web page, we made a stake in the ground that one thing that this page is best at is a fast and fluid login experience.</span></span> <span data-ttu-id="4ee5f-158">Di conseguenza, l'interfaccia utente più importante nel flusso è il campo nome utente e password nella pagina di accesso per una rapida esperienza di immissione delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-158">Thus, the UI that is most prominent in the flow is the username and password field in the login page for a quick credential entry experience.</span></span> <span data-ttu-id="4ee5f-159">Sebbene sia stato rilevato che esistono altri scenari comuni, ad esempio il recupero delle password e il riferimento a informative sulla privacy, l'esperienza avanzata del Web è una posizione migliore per tali esperienze.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-159">While we identified that there are other common scenarios such as password retrieval, and referencing privacy statements, the rich experience of the web is a better place for those experiences.</span></span> <span data-ttu-id="4ee5f-160">Per tutti i flussi non correlati all'esperienza di autenticazione Web sicura, è consigliabile passare all'utente nel browser.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-160">For all flows not related to secure web auth experience, we recommend navigating the user to the browser.</span></span> <span data-ttu-id="4ee5f-161">Questa operazione viene mostrata nel file HTML di esempio (WebAuthLogin.html) come indicato di seguito: `<meta name="mswebdialog-newwindowurl" content="*" />` consente di aprire tutte le pagine Web collegate a dalla pagina account di accesso o autorizzazioni nel browser predefinito dell'utente, in cui l'utente può completare questi flussi e tornare all'app per accedere.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-161">This is shown in the sample HTML file (WebAuthLogin.html) as follows: `<meta name="mswebdialog-newwindowurl" content="*" />` This opens all web pages linked to from the login or permissions page in the user's default browser where the user can complete these flows and then return to the app to log in.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="4ee5f-162">Considerazioni relative alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="4ee5f-162">Security Considerations</span></span>

<span data-ttu-id="4ee5f-163">Gli articoli seguenti forniscono indicazioni per la scrittura di codice C++ sicuro.</span><span class="sxs-lookup"><span data-stu-id="4ee5f-163">The following articles provide guidance for writing secure C++ code.</span></span>

-   [<span data-ttu-id="4ee5f-164">Procedure di protezione ottimali per C++</span><span class="sxs-lookup"><span data-stu-id="4ee5f-164">Security Best Practices for C++</span></span>](/cpp/security/security-best-practices-for-cpp)
-   <span data-ttu-id="4ee5f-165">[Modelli & procedure consigliate per la sicurezza delle applicazioni](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="4ee5f-165">[Patterns & Practices Security Guidance for Applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ee5f-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ee5f-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ee5f-167">Considerazioni relative allo sviluppo di pagine Web</span><span class="sxs-lookup"><span data-stu-id="4ee5f-167">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="4ee5f-168">Domande frequenti sul broker di autenticazione Web</span><span class="sxs-lookup"><span data-stu-id="4ee5f-168">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)
</dt> <dt>

[<span data-ttu-id="4ee5f-169">App di esempio SDK Web Authentication broker</span><span class="sxs-lookup"><span data-stu-id="4ee5f-169">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="4ee5f-170">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="4ee5f-170">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 

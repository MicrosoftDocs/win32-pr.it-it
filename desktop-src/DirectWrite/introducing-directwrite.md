---
title: Introduzione a DirectWrite
description: Le persone comunicano con il testo sempre nella loro vita quotidiana.
ms.assetid: ec7cc4a3-b925-48dc-920f-fd293b4c69f0
keywords:
- DirectWrite, informazioni
- DirectWrite, funzionalità tipografiche
- tipografia
- DirectWrite, testo internazionale
- DirectWrite, tipi di carattere OpenType
- Tipi di carattere OpenType
- DirectWrite, ClearType
- ClearType
- DirectWrite, panoramica delle API
- DirectWrite, IDWriteFontFace
- IDWriteFontFace
- DirectWrite, rendering del testo
- DirectWrite, modalità di rendering
- DirectWrite, interoperatività GDI
- DirectWrite, interoperabilità
- interoperabilità, DirectWrite
- interoperabilità, Graphics Device Interface (GDI)
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4064feccbdbc03f4b2e4d0118e5ab704013d314e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872906"
---
# <a name="introducing-directwrite"></a><span data-ttu-id="fb704-122">Introduzione a DirectWrite</span><span class="sxs-lookup"><span data-stu-id="fb704-122">Introducing DirectWrite</span></span>

<span data-ttu-id="fb704-123">Le persone comunicano con il testo sempre nella loro vita quotidiana.</span><span class="sxs-lookup"><span data-stu-id="fb704-123">People communicate with text all the time in their daily lives.</span></span> <span data-ttu-id="fb704-124">È il modo principale in cui le persone utilizzano un volume di informazioni sempre maggiore.</span><span class="sxs-lookup"><span data-stu-id="fb704-124">It is the primary way for people to consume an increasing volume of information.</span></span> <span data-ttu-id="fb704-125">In passato, veniva usato per stampare contenuto, principalmente documenti, giornali, libri e così via.</span><span class="sxs-lookup"><span data-stu-id="fb704-125">In the past, it used to be through printed content, primarily documents, newspapers, books, and so on.</span></span> <span data-ttu-id="fb704-126">Sempre più, si tratta di contenuto online nel proprio PC Windows.</span><span class="sxs-lookup"><span data-stu-id="fb704-126">Increasingly, it is online content on their Windows PC.</span></span> <span data-ttu-id="fb704-127">Un tipico utente di Windows dedica molto tempo alla lettura dallo schermo del computer.</span><span class="sxs-lookup"><span data-stu-id="fb704-127">A typical Windows user spends a lot of time reading from their computer screen.</span></span> <span data-ttu-id="fb704-128">Potrebbero navigare sul Web, analizzare la posta elettronica, comporre un report, compilare un foglio di calcolo o scrivere software, ma ciò che realmente stanno leggendo.</span><span class="sxs-lookup"><span data-stu-id="fb704-128">They might be surfing the Web, scanning e-mail, composing a report, filling in a spreadsheet, or writing software, but what they're really doing is reading.</span></span> <span data-ttu-id="fb704-129">Anche se il testo e i tipi di carattere comportano quasi tutte le parti dell'esperienza utente in Windows, per la maggior parte degli utenti la lettura sullo schermo non è piacevole come la lettura dell'output stampato.</span><span class="sxs-lookup"><span data-stu-id="fb704-129">Even though text and fonts permeate nearly every part of the user experience in Windows, for most users, reading on the screen is not as enjoyable as reading printed output.</span></span>

<span data-ttu-id="fb704-130">Per gli sviluppatori di applicazioni Windows la scrittura di codice di gestione del testo è una sfida a causa dei maggiori requisiti per una migliore leggibilità, una formattazione sofisticata e un controllo del layout e il supporto per più linguaggi che l'applicazione deve visualizzare.</span><span class="sxs-lookup"><span data-stu-id="fb704-130">For Windows application developers, writing text-handling code is a challenge because of the increased requirements for better readability, sophisticated formatting and layout control, and support for the multiple languages the application must display.</span></span> <span data-ttu-id="fb704-131">Anche il sistema di gestione del testo più semplice deve consentire l'input di testo, il layout, la visualizzazione, la modifica e la copia e incolla.</span><span class="sxs-lookup"><span data-stu-id="fb704-131">Even the most basic text-handling system must allow for text input, layout, display, editing, and copying and pasting.</span></span> <span data-ttu-id="fb704-132">Gli utenti di Windows in genere prevedono ancora più di queste funzionalità di base, richiedendo anche semplici editor per supportare più tipi di carattere, diversi stili di paragrafo, immagini incorporate, controllo ortografico e altre funzionalità.</span><span class="sxs-lookup"><span data-stu-id="fb704-132">Windows users commonly expect even more than these basic features, requiring even simple editors to support multiple fonts, various paragraph styles, embedded images, spell checking, and other features.</span></span> <span data-ttu-id="fb704-133">La moderna progettazione dell'interfaccia utente non è più conforme al formato singolo, al testo normale, ma deve presentare un'esperienza migliore con i tipi di carattere e i layout di testo avanzati.</span><span class="sxs-lookup"><span data-stu-id="fb704-133">Modern UI design is also no longer confined to single format, plain text, but needs to present a better experience with rich fonts and text layouts.</span></span>

<span data-ttu-id="fb704-134">Questa è un'introduzione al modo in cui [DirectWrite](direct-write-portal.md) consente alle applicazioni Windows di migliorare l'esperienza di testo per l'interfaccia utente e i documenti.</span><span class="sxs-lookup"><span data-stu-id="fb704-134">This is an introduction to how [DirectWrite](direct-write-portal.md) enables Windows applications to enhance the text experience for UI and documents.</span></span>

## <a name="improving-the-text-experience"></a><span data-ttu-id="fb704-135">Miglioramento dell'esperienza di testo</span><span class="sxs-lookup"><span data-stu-id="fb704-135">Improving the Text Experience</span></span>

<span data-ttu-id="fb704-136">Le applicazioni Windows moderne hanno requisiti sofisticati per il testo nell'interfaccia utente e nei documenti.</span><span class="sxs-lookup"><span data-stu-id="fb704-136">Modern Windows applications have sophisticated requirements for text in their UI and documents.</span></span> <span data-ttu-id="fb704-137">Sono incluse una migliore leggibilità, il supporto per una vasta gamma di linguaggi e script e prestazioni di rendering superiori.</span><span class="sxs-lookup"><span data-stu-id="fb704-137">These include better readability, support for a large variety of languages and scripts, and superior rendering performance.</span></span> <span data-ttu-id="fb704-138">Inoltre, la maggior parte delle applicazioni esistenti richiede un modo per portare avanti gli investimenti esistenti nella codebase di WindowsWin32.</span><span class="sxs-lookup"><span data-stu-id="fb704-138">In addition, most existing applications require a way to carry forward existing investments in the WindowsWin32 code base.</span></span>

<span data-ttu-id="fb704-139">[DirectWrite](direct-write-portal.md) fornisce le tre funzionalità seguenti che consentono agli sviluppatori di applicazioni Windows di migliorare l'esperienza di testo all'interno delle applicazioni: indipendenza dal sistema di rendering, tipografia di alta qualità e più livelli di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="fb704-139">[DirectWrite](direct-write-portal.md) provides the following three features that enable Windows application developers to improve the text experience within their applications: independence from the rendering system, high-quality typography, and multiple layers of functionality.</span></span>

## <a name="rendering-system-independence"></a><span data-ttu-id="fb704-140">Indipendenza Rendering-System</span><span class="sxs-lookup"><span data-stu-id="fb704-140">Rendering-System Independence</span></span>

<span data-ttu-id="fb704-141">[DirectWrite](direct-write-portal.md) è indipendente da qualsiasi tecnologia grafica specifica.</span><span class="sxs-lookup"><span data-stu-id="fb704-141">[DirectWrite](direct-write-portal.md) is independent of any particular graphics technology.</span></span> <span data-ttu-id="fb704-142">Le applicazioni sono gratuite per l'utilizzo della tecnologia di rendering più adatta alle proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="fb704-142">Applications are free to use the rendering technology best suited to their needs.</span></span> <span data-ttu-id="fb704-143">Ciò offre alle applicazioni la flessibilità di continuare a eseguire il rendering di alcune parti dell'applicazione tramite GDI e altre parti tramite Direct3D o [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="fb704-143">This gives applications the flexibility to continue rendering some parts of their application through GDI and other parts through Direct3D or [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="fb704-144">Infatti, un'applicazione può scegliere di eseguire il rendering di DirectWrite tramite uno stack di rendering proprietario.</span><span class="sxs-lookup"><span data-stu-id="fb704-144">In fact, an application could choose to render DirectWrite through a proprietary rendering stack.</span></span>

## <a name="high-quality-typography"></a><span data-ttu-id="fb704-145">Tipografia High-Quality</span><span class="sxs-lookup"><span data-stu-id="fb704-145">High-Quality Typography</span></span>

<span data-ttu-id="fb704-146">[DirectWrite](direct-write-portal.md) sfrutta i vantaggi offerti dalla tecnologia dei tipi di carattere [OpenType](../intl/opentype-font-format.md) per abilitare la tipografia di qualità elevata in un'applicazione Windows.</span><span class="sxs-lookup"><span data-stu-id="fb704-146">[DirectWrite](direct-write-portal.md) takes advantage of the advances in [OpenType](../intl/opentype-font-format.md) Font technology to enable high quality typography within a Windows application.</span></span> <span data-ttu-id="fb704-147">Il sistema dei tipi di carattere DirectWrite fornisce servizi per la gestione dell'enumerazione dei tipi di carattere, del fallback del tipo di carattere e della memorizzazione nella cache del tipo di carattere, tutti necessari per le applicazioni per la gestione di</span><span class="sxs-lookup"><span data-stu-id="fb704-147">The DirectWrite font system provides services for dealing with font enumeration, font fallback, and font caching, which are all needed by applications for handling fonts.</span></span>

<span data-ttu-id="fb704-148">Il supporto [OpenType](../intl/opentype-font-format.md) fornito da [DirectWrite](direct-write-portal.md) consente agli sviluppatori di aggiungere alle proprie applicazioni funzionalità tipografiche avanzate e supporto per testo internazionale.</span><span class="sxs-lookup"><span data-stu-id="fb704-148">The [OpenType](../intl/opentype-font-format.md) support provided by [DirectWrite](direct-write-portal.md) enables developers to add to their applications advanced typographic features and support for international text.</span></span>

## <a name="support-for-advanced-typographic-features"></a><span data-ttu-id="fb704-149">Supporto per funzionalità tipografiche avanzate</span><span class="sxs-lookup"><span data-stu-id="fb704-149">Support for Advanced Typographic Features</span></span>

<span data-ttu-id="fb704-150">[DirectWrite](direct-write-portal.md) consente agli sviluppatori di applicazioni di sbloccare le funzionalità dei tipi di carattere OpenType che non possono essere utilizzati in WINFORMS o GDI.</span><span class="sxs-lookup"><span data-stu-id="fb704-150">[DirectWrite](direct-write-portal.md) enables application developers to unlock the features of OpenType fonts that they couldn't use in WinForms or GDI.</span></span> <span data-ttu-id="fb704-151">L'oggetto DirectWrite [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) espone molte delle funzionalità avanzate dei tipi di carattere OpenType, ad esempio alternative stilistiche e ornati.</span><span class="sxs-lookup"><span data-stu-id="fb704-151">The DirectWrite [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) object exposes many of the advanced features of OpenType fonts, such as stylistic alternates and swashes.</span></span> <span data-ttu-id="fb704-152">Microsoft Windows Software Development Kit (SDK) fornisce un set di tipi di carattere [OpenType](../intl/opentype-font-format.md) di esempio progettati con funzionalità avanzate, ad esempio i tipi di carattere Pericle e Pescadero.</span><span class="sxs-lookup"><span data-stu-id="fb704-152">The Microsoft Windows Software Development Kit (SDK) provides a set of sample [OpenType](../intl/opentype-font-format.md) fonts that are designed with rich features, such as the Pericles and Pescadero fonts.</span></span> <span data-ttu-id="fb704-153">Per ulteriori informazioni sulle funzionalità OpenType, vedere [funzionalità dei tipi di carattere OpenType](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fb704-153">For more details on OpenType features, see [OpenType Font Features](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).</span></span>

## <a name="support-for-international-text"></a><span data-ttu-id="fb704-154">Supporto per testo internazionale</span><span class="sxs-lookup"><span data-stu-id="fb704-154">Support for International Text</span></span>

<span data-ttu-id="fb704-155">[DirectWrite](direct-write-portal.md) utilizza i tipi di carattere [OpenType](../intl/opentype-font-format.md) per consentire un ampio supporto per il testo internazionale.</span><span class="sxs-lookup"><span data-stu-id="fb704-155">[DirectWrite](direct-write-portal.md) uses [OpenType](../intl/opentype-font-format.md) fonts to enable broad support for international text.</span></span> <span data-ttu-id="fb704-156">Sono supportate funzionalità Unicode quali surrogati, BIDI, interruzioni di riga e UV.</span><span class="sxs-lookup"><span data-stu-id="fb704-156">Unicode features such as surrogates, BIDI, line breaking, and UVS are supported.</span></span> <span data-ttu-id="fb704-157">La creazione di elementi, la sostituzione e la definizione di un glifo di script basati sul linguaggio garantiscono che il layout e il rendering del testo in qualsiasi script siano corretti.</span><span class="sxs-lookup"><span data-stu-id="fb704-157">Language-guided script itemization, number substitution, and glyph shaping ensure that text in any script has the correct layout and rendering.</span></span>

<span data-ttu-id="fb704-158">Sono attualmente supportati gli script seguenti:</span><span class="sxs-lookup"><span data-stu-id="fb704-158">The following scripts are currently supported:</span></span>

> [!Note]  
> <span data-ttu-id="fb704-159">Per gli script contrassegnati con un \* , non sono disponibili tipi di carattere di sistema predefiniti.</span><span class="sxs-lookup"><span data-stu-id="fb704-159">For scripts marked with an \*, there are no default system fonts.</span></span> <span data-ttu-id="fb704-160">Le applicazioni devono installare i tipi di carattere che supportano questi script.</span><span class="sxs-lookup"><span data-stu-id="fb704-160">Applications must install fonts that support these scripts.</span></span>

 

-   <span data-ttu-id="fb704-161">Arabo</span><span class="sxs-lookup"><span data-stu-id="fb704-161">Arabic</span></span>
-   <span data-ttu-id="fb704-162">Armeno</span><span class="sxs-lookup"><span data-stu-id="fb704-162">Armenian</span></span>
-   <span data-ttu-id="fb704-163">Bengala</span><span class="sxs-lookup"><span data-stu-id="fb704-163">Bengala</span></span>
-   <span data-ttu-id="fb704-164">Bopomofo</span><span class="sxs-lookup"><span data-stu-id="fb704-164">Bopomofo</span></span>
-   <span data-ttu-id="fb704-165">Braille\*</span><span class="sxs-lookup"><span data-stu-id="fb704-165">Braille\*</span></span>
-   <span data-ttu-id="fb704-166">Sillabico aborigeno canadese</span><span class="sxs-lookup"><span data-stu-id="fb704-166">Canadian aboriginal syllabics</span></span>
-   <span data-ttu-id="fb704-167">Cherokee</span><span class="sxs-lookup"><span data-stu-id="fb704-167">Cherokee</span></span>
-   <span data-ttu-id="fb704-168">Cinese (semplificato & tradizionale)</span><span class="sxs-lookup"><span data-stu-id="fb704-168">Chinese (Simplified & Traditional)</span></span>
-   <span data-ttu-id="fb704-169">Cirillico</span><span class="sxs-lookup"><span data-stu-id="fb704-169">Cyrillic</span></span>
-   <span data-ttu-id="fb704-170">Copto\*</span><span class="sxs-lookup"><span data-stu-id="fb704-170">Coptic\*</span></span>
-   <span data-ttu-id="fb704-171">Devanagari</span><span class="sxs-lookup"><span data-stu-id="fb704-171">Devanagari</span></span>
-   <span data-ttu-id="fb704-172">Etiope</span><span class="sxs-lookup"><span data-stu-id="fb704-172">Ethiopic</span></span>
-   <span data-ttu-id="fb704-173">Georgiano</span><span class="sxs-lookup"><span data-stu-id="fb704-173">Georgian</span></span>
-   <span data-ttu-id="fb704-174">Glagolitico\*</span><span class="sxs-lookup"><span data-stu-id="fb704-174">Glagolitic\*</span></span>
-   <span data-ttu-id="fb704-175">Greco</span><span class="sxs-lookup"><span data-stu-id="fb704-175">Greek</span></span>
-   <span data-ttu-id="fb704-176">Gujarati</span><span class="sxs-lookup"><span data-stu-id="fb704-176">Gujarati</span></span>
-   <span data-ttu-id="fb704-177">Gurmukhi</span><span class="sxs-lookup"><span data-stu-id="fb704-177">Gurmukhi</span></span>
-   <span data-ttu-id="fb704-178">Ebraico</span><span class="sxs-lookup"><span data-stu-id="fb704-178">Hebrew</span></span>
-   <span data-ttu-id="fb704-179">Giapponese</span><span class="sxs-lookup"><span data-stu-id="fb704-179">Japanese</span></span>
-   <span data-ttu-id="fb704-180">Kannada</span><span class="sxs-lookup"><span data-stu-id="fb704-180">Kannada</span></span>
-   <span data-ttu-id="fb704-181">Khmer</span><span class="sxs-lookup"><span data-stu-id="fb704-181">Khmer</span></span>
-   <span data-ttu-id="fb704-182">Coreano</span><span class="sxs-lookup"><span data-stu-id="fb704-182">Korean</span></span>
-   <span data-ttu-id="fb704-183">Lao</span><span class="sxs-lookup"><span data-stu-id="fb704-183">Lao</span></span>
-   <span data-ttu-id="fb704-184">Latino</span><span class="sxs-lookup"><span data-stu-id="fb704-184">Latin</span></span>
-   <span data-ttu-id="fb704-185">Malayalam</span><span class="sxs-lookup"><span data-stu-id="fb704-185">Malayalam</span></span>
-   <span data-ttu-id="fb704-186">Mongolo</span><span class="sxs-lookup"><span data-stu-id="fb704-186">Mongolian</span></span>
-   <span data-ttu-id="fb704-187">Myanmar</span><span class="sxs-lookup"><span data-stu-id="fb704-187">Myanmar</span></span>
-   <span data-ttu-id="fb704-188">Nuovo tai lue</span><span class="sxs-lookup"><span data-stu-id="fb704-188">New Tai Lue</span></span>
-   <span data-ttu-id="fb704-189">Ogamico\*</span><span class="sxs-lookup"><span data-stu-id="fb704-189">Ogham\*</span></span>
-   <span data-ttu-id="fb704-190">Odia</span><span class="sxs-lookup"><span data-stu-id="fb704-190">Odia</span></span>
-   <span data-ttu-id="fb704-191">' Carattere phags-pa</span><span class="sxs-lookup"><span data-stu-id="fb704-191">'Phags-pa</span></span>
-   <span data-ttu-id="fb704-192">Runico\*</span><span class="sxs-lookup"><span data-stu-id="fb704-192">Runic\*</span></span>
-   <span data-ttu-id="fb704-193">Singalese</span><span class="sxs-lookup"><span data-stu-id="fb704-193">Sinhala</span></span>
-   <span data-ttu-id="fb704-194">Siriaco</span><span class="sxs-lookup"><span data-stu-id="fb704-194">Syriac</span></span>
-   <span data-ttu-id="fb704-195">Tai le</span><span class="sxs-lookup"><span data-stu-id="fb704-195">Tai Le</span></span>
-   <span data-ttu-id="fb704-196">Tamil</span><span class="sxs-lookup"><span data-stu-id="fb704-196">Tamil</span></span>
-   <span data-ttu-id="fb704-197">Telugu</span><span class="sxs-lookup"><span data-stu-id="fb704-197">Telugu</span></span>
-   <span data-ttu-id="fb704-198">Thaana</span><span class="sxs-lookup"><span data-stu-id="fb704-198">Thaana</span></span>
-   <span data-ttu-id="fb704-199">Thai</span><span class="sxs-lookup"><span data-stu-id="fb704-199">Thai</span></span>
-   <span data-ttu-id="fb704-200">Tibetano</span><span class="sxs-lookup"><span data-stu-id="fb704-200">Tibetan</span></span>
-   <span data-ttu-id="fb704-201">Yi</span><span class="sxs-lookup"><span data-stu-id="fb704-201">Yi</span></span>

## <a name="multiple-layers-of-functionality"></a><span data-ttu-id="fb704-202">Più livelli di funzionalità</span><span class="sxs-lookup"><span data-stu-id="fb704-202">Multiple Layers of Functionality</span></span>

<span data-ttu-id="fb704-203">[DirectWrite](direct-write-portal.md) fornisce livelli di funzionalità con factoring, in cui ogni livello interagisce senza interruzioni con il successivo.</span><span class="sxs-lookup"><span data-stu-id="fb704-203">[DirectWrite](direct-write-portal.md) provides factored layers of functionality, with each layer interacting seamlessly with the next.</span></span> <span data-ttu-id="fb704-204">Il progetto API offre agli sviluppatori di applicazioni la libertà e la flessibilità di adottare singoli livelli, a seconda delle esigenze e della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="fb704-204">The API design gives application developers the freedom and flexibility to adopt individual layers depending on their needs and schedule.</span></span> <span data-ttu-id="fb704-205">Nel diagramma seguente viene illustrata la relazione tra questi livelli.</span><span class="sxs-lookup"><span data-stu-id="fb704-205">The following diagram shows the relationship between these layers.</span></span>

![diagramma dei livelli DirectWrite e del modo in cui comunicano con un'applicazione o un Framework dell'interfaccia utente e l'API grafica](images/intro-01.png)

<span data-ttu-id="fb704-207">L'API di layout del testo fornisce la funzionalità di livello più alto disponibile in [DirectWrite](direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="fb704-207">The text layout API provides the highest level functionality available from [DirectWrite](direct-write-portal.md).</span></span> <span data-ttu-id="fb704-208">Fornisce servizi per l'applicazione per misurare, visualizzare e interagire con stringhe di testo formattate in modo completo.</span><span class="sxs-lookup"><span data-stu-id="fb704-208">It provides services for the application to measure, display, and interact with richly formatted text strings.</span></span> <span data-ttu-id="fb704-209">Questa API di testo può essere usata nelle applicazioni che attualmente usano Win32 DrawText per creare un'interfaccia utente moderna con testo formattato in modo completo.</span><span class="sxs-lookup"><span data-stu-id="fb704-209">This text API can be used in applications that currently use Win32's DrawText to build a modern UI with richly formatted text.</span></span>

<span data-ttu-id="fb704-210">Le applicazioni con utilizzo intensivo del testo che implementano il proprio motore di layout possono utilizzare il livello successivo, ovvero il processore di script.</span><span class="sxs-lookup"><span data-stu-id="fb704-210">Text-intensive applications that implement their own layout engine may use the next layer down: the script processor.</span></span> <span data-ttu-id="fb704-211">Il processore di script suddivide un blocco di testo in blocchi di script e gestisce il mapping tra le rappresentazioni Unicode e la rappresentazione del glifo appropriata nel tipo di carattere, in modo che il testo dello script possa essere visualizzato correttamente nella lingua corretta.</span><span class="sxs-lookup"><span data-stu-id="fb704-211">The script processor breaks down a chunk of text into script blocks and handles the mapping between Unicode representations to the appropriate glyph representation in the font so the text of the script can be correctly displayed in the correct language.</span></span> <span data-ttu-id="fb704-212">Il sistema di layout utilizzato dal livello API del layout del testo è basato sul sistema di elaborazione di tipi di carattere e script.</span><span class="sxs-lookup"><span data-stu-id="fb704-212">The layout system used by the text layout API layer is built upon the font and script processing system.</span></span>

<span data-ttu-id="fb704-213">Il livello di rendering del glifo è il livello più basso di funzionalità e fornisce funzionalità di rendering dei glifi per le applicazioni che implementano il proprio motore di layout di testo.</span><span class="sxs-lookup"><span data-stu-id="fb704-213">The glyph-rendering layer is the lowest layer of functionality and provides glyph-rendering functionality for applications that implement their own text layout engine.</span></span> <span data-ttu-id="fb704-214">Il livello di rendering del glifo è utile anche per le applicazioni che implementano un renderer personalizzato per modificare il comportamento di disegno del glifo tramite la funzione di callback nell'API di formattazione del testo [DirectWrite](direct-write-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="fb704-214">The glyph rendering layer is also useful for applications that implement a custom renderer to modify the glyph-drawing behavior through the callback function in the [DirectWrite](direct-write-portal.md) text-formatting API.</span></span>

<span data-ttu-id="fb704-215">Il sistema dei tipi di carattere [DirectWrite](direct-write-portal.md) è disponibile per tutti i livelli funzionali di DirectWrite e consente a un'applicazione di accedere alle informazioni sul tipo di carattere e sul glifo.</span><span class="sxs-lookup"><span data-stu-id="fb704-215">The [DirectWrite](direct-write-portal.md) font system is available to all the DirectWrite functional layers and enables an application to access font and glyph information.</span></span> <span data-ttu-id="fb704-216">È progettato per gestire le tecnologie dei tipi di carattere e i formati di dati comuni.</span><span class="sxs-lookup"><span data-stu-id="fb704-216">It is designed to handle common font technologies and data formats.</span></span> <span data-ttu-id="fb704-217">Il modello di tipo di carattere DirectWrite segue la pratica tipografica comune di supportare un numero qualsiasi di pesi, stili e estendezioni nella stessa famiglia di caratteri.</span><span class="sxs-lookup"><span data-stu-id="fb704-217">The DirectWrite font model follows the common typographic practice of supporting any number of weights, styles, and stretches in the same font family.</span></span> <span data-ttu-id="fb704-218">Questo modello, lo stesso modello seguito da WPF e CSS, specifica che i tipi di carattere che differiscono solo per il peso (grassetto, chiaro e così via), lo stile (verticale, corsivo o obliquo) o l'estensione (stretta, ridotta, ampia e così via) vengono considerati membri di una singola famiglia di caratteri.</span><span class="sxs-lookup"><span data-stu-id="fb704-218">This model, the same model followed by WPF and CSS, specifies that fonts differing only in weight (bold, light, and so on), style (upright, italic, or oblique) or stretch (narrow, condensed, wide, and so on) are considered to be members of a single font family.</span></span>

### <a name="improved-text-rendering-with-cleartype"></a><span data-ttu-id="fb704-219">Rendering del testo migliorato con ClearType</span><span class="sxs-lookup"><span data-stu-id="fb704-219">Improved Text Rendering with ClearType</span></span>

<span data-ttu-id="fb704-220">Migliorare la leggibilità sullo schermo è un requisito fondamentale per tutte le applicazioni Windows.</span><span class="sxs-lookup"><span data-stu-id="fb704-220">Improving readability on the screen is a key requirement for all Windows applications.</span></span> <span data-ttu-id="fb704-221">L'evidenza della ricerca nella psicologia cognitiva indica che è necessario essere in grado di riconoscere accuratamente ogni lettera e che la spaziatura tra le lettere è fondamentale per l'elaborazione rapida.</span><span class="sxs-lookup"><span data-stu-id="fb704-221">The evidence from research in cognitive psychology indicates that we need to be able to recognize every letter accurately and that even spacing between letters is critical for fast processing.</span></span> <span data-ttu-id="fb704-222">Le lettere e le parole che non sono simmetriche vengono percepite come orribili e peggiorano l'esperienza di lettura.</span><span class="sxs-lookup"><span data-stu-id="fb704-222">Letters and words that are not symmetrical are perceived as ugly and degrade the reading experience.</span></span> <span data-ttu-id="fb704-223">Kevin Larson, Microsoft Advanced Reading Technologies Group, ha scritto un articolo sull'argomento pubblicato in Spectrum IEEE.</span><span class="sxs-lookup"><span data-stu-id="fb704-223">Kevin Larson, Microsoft Advanced Reading Technologies group, wrote an article on the subject that was published in Spectrum IEEE.</span></span> <span data-ttu-id="fb704-224">L'articolo è denominato "tecnologia del testo" ( https://www.spectrum.ieee.org/print/5049) .</span><span class="sxs-lookup"><span data-stu-id="fb704-224">The article is called "The Technology of Text" (https://www.spectrum.ieee.org/print/5049).</span></span>

<span data-ttu-id="fb704-225">Il rendering del testo in [DirectWrite](direct-write-portal.md) viene eseguito utilizzando Microsoft ClearType, che migliora la chiarezza e la leggibilità del testo.</span><span class="sxs-lookup"><span data-stu-id="fb704-225">Text in [DirectWrite](direct-write-portal.md) is rendered using Microsoft ClearType, which enhances the clarity and readability of text.</span></span> <span data-ttu-id="fb704-226">ClearType sfrutta il fatto che gli schermi LCD moderni hanno striping RGB per ogni pixel che possono essere controllati singolarmente.</span><span class="sxs-lookup"><span data-stu-id="fb704-226">ClearType takes advantage of the fact that modern LCD displays have RGB stripes for each pixel that can be controlled individually.</span></span> <span data-ttu-id="fb704-227">DirectWrite utilizza i miglioramenti più recenti per ClearType, incluso prima con Windows Vista con Windows Presentation Foundation, che consente di valutare non solo le singole lettere, ma anche la spaziatura tra le lettere.</span><span class="sxs-lookup"><span data-stu-id="fb704-227">DirectWrite uses the latest enhancements to ClearType, first included with Windows Vista with Windows Presentation Foundation, that enables it to evaluate not just the individual letters but also the spacing between letters.</span></span> <span data-ttu-id="fb704-228">Prima di questi miglioramenti di ClearType, il testo con una dimensione di "lettura" di 10 o 12 punti era difficile da visualizzare: è possibile posizionare un pixel tra le lettere, che era spesso troppo piccolo o 2 pixel, che era spesso troppo grande.</span><span class="sxs-lookup"><span data-stu-id="fb704-228">Before these ClearType enhancements, text with a "reading" size of 10 or 12 points was difficult to display: we could place either 1 pixel in between letters, which was often too little, or 2 pixels, which was often too much.</span></span> <span data-ttu-id="fb704-229">L'uso della risoluzione aggiuntiva nei subpixel fornisce la spaziatura frazionaria, che migliora l'uniformità e la simmetria dell'intera pagina.</span><span class="sxs-lookup"><span data-stu-id="fb704-229">Using the extra resolution in the subpixels provides us with fractional spacing, which improves the evenness and symmetry of the entire page.</span></span>

<span data-ttu-id="fb704-230">Nell'illustrazione seguente viene illustrato il modo in cui i glifi possono iniziare su qualsiasi limite dei sottopixel quando si utilizza il posizionamento dei sottopixel.</span><span class="sxs-lookup"><span data-stu-id="fb704-230">The following two illustration show how glyphs may begin on any sub-pixel boundary when sub-pixel positioning is used.</span></span>

<span data-ttu-id="fb704-231">Viene eseguito il rendering della figura seguente utilizzando la versione GDI del renderer ClearType, che non utilizza il posizionamento dei subpixel.</span><span class="sxs-lookup"><span data-stu-id="fb704-231">The following illustration is rendered using the GDI version of the ClearType renderer, which did not employ sub-pixel positioning.</span></span>

![illustrazione della "tecnologia" di cui è stato eseguito il rendering senza posizionamento dei subpixel](images/intro-03.png)

<span data-ttu-id="fb704-233">Viene eseguito il rendering della figura seguente usando la versione [DirectWrite](direct-write-portal.md) del renderer ClearType, che usa il posizionamento dei subpixel.</span><span class="sxs-lookup"><span data-stu-id="fb704-233">The following illustration is rendered using the [DirectWrite](direct-write-portal.md) version of the ClearType renderer, which uses sub-pixel positioning.</span></span>

![illustrazione della "tecnologia" di cui è stato eseguito il rendering con il posizionamento dei subpixel](images/intro-04.png)

<span data-ttu-id="fb704-235">Si noti che la spaziatura tra le lettere h e n è più uniforme nella seconda immagine e la lettera o è distanziata ulteriormente dalla lettera n, più anche con la lettera l.</span><span class="sxs-lookup"><span data-stu-id="fb704-235">Note that the spacing between the letters h and n is more even in the second image and the letter o is spaced further from the letter n, more even with the letter l.</span></span> <span data-ttu-id="fb704-236">Si noti inoltre che le steli sulle lettere l sono più naturali.</span><span class="sxs-lookup"><span data-stu-id="fb704-236">Also note how the stems on the letters l are more natural looking.</span></span>

<span data-ttu-id="fb704-237">Il posizionamento ClearType del sottopixel offre la spaziatura più accurata dei caratteri sullo schermo, soprattutto in dimensioni ridotte, in cui la differenza tra un subpixel e un pixel intero rappresenta una percentuale significativa della larghezza del glifo.</span><span class="sxs-lookup"><span data-stu-id="fb704-237">The subpixel ClearType positioning offers the most accurate spacing of characters on screen, especially at small sizes where the difference between a sub-pixel and a whole pixel represents a significant proportion of glyph width.</span></span> <span data-ttu-id="fb704-238">Consente di misurare il testo in uno spazio di risoluzione ideale e di eseguirne il rendering in corrispondenza della relativa posizione naturale, con la granularità del sottopixel.</span><span class="sxs-lookup"><span data-stu-id="fb704-238">It enables text to be measured in ideal resolution space and rendered at its natural position at the LCD color stripe, with subpixel granularity.</span></span> <span data-ttu-id="fb704-239">Il testo misurato e sottoposto a rendering mediante questa tecnologia è, per definizione, indipendente dalla risoluzione, vale a dire che lo stesso layout del testo viene effettuato attraverso la gamma di diverse risoluzioni di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="fb704-239">Text measured and rendered using this technology is, by definition, resolution-independent, meaning that the exact same layout of text is achieved across the range of various display resolutions.</span></span>

<span data-ttu-id="fb704-240">A differenza di entrambi i tipi di rendering GDI ClearType, il sottopixel ClearType offre la larghezza più accurata dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="fb704-240">Unlike either type of GDI ClearType rendering, sub-pixel ClearType offers the most accurate width of characters.</span></span>

<span data-ttu-id="fb704-241">Per impostazione predefinita, l'API della stringa di testo adotta il rendering del testo dei sottopixel, il che significa che il testo viene misurato in base alla risoluzione ideale indipendentemente dalla risoluzione dello schermo corrente e produce il risultato del posizionamento del glifo in base alle larghezze di avanzamento e al posizionamento dei glifi effettivamente ridimensionati.</span><span class="sxs-lookup"><span data-stu-id="fb704-241">The Text String API adopts sub-pixel text rendering by default, which means it measures text at its ideal resolution independent of the current display resolution, and produces the glyph positioning result based on the truly scaled glyph advance widths and positioning offsets.</span></span>

<span data-ttu-id="fb704-242">Per il testo di grandi dimensioni, [DirectWrite](direct-write-portal.md) Abilita anche l'anti-aliasing lungo l'asse y per rendere i bordi più uniformi ed eseguire il rendering delle lettere come la finestra di progettazione del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="fb704-242">For large-sized text, [DirectWrite](direct-write-portal.md) also enables anti-aliasing along the y-axis to make the edges smoother and render letters as the font designer intended.</span></span> <span data-ttu-id="fb704-243">La figura seguente mostra l'anti-aliasing della direzione y.</span><span class="sxs-lookup"><span data-stu-id="fb704-243">The following illustration shows y-direction anti-aliasing.</span></span>

![illustrazione di "ClearType" di cui è stato eseguito il rendering come testo GDI e come testo DirectWrite con l'anti-aliasing della direzione y](images/intro-05.png)

<span data-ttu-id="fb704-245">Sebbene il testo di [DirectWrite](direct-write-portal.md) sia posizionato e sottoposto a rendering utilizzando il sottopixel ClearType per impostazione predefinita, sono disponibili altre opzioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="fb704-245">Although [DirectWrite](direct-write-portal.md) text is positioned and rendered using sub-pixel ClearType by default, other rendering options are available.</span></span> <span data-ttu-id="fb704-246">Molte applicazioni esistenti utilizzano GDI per eseguire il rendering della maggior parte dell'interfaccia utente e alcune applicazioni utilizzano i controlli di modifica del sistema che continuano a utilizzare GDI per il rendering del testo.</span><span class="sxs-lookup"><span data-stu-id="fb704-246">Many existing applications use GDI to render most of their UI, and some applications use system editing controls that continue to use GDI for text rendering.</span></span> <span data-ttu-id="fb704-247">Quando si aggiunge il testo di DirectWrite a queste applicazioni, potrebbe essere necessario sacrificare i miglioramenti dell'esperienza di lettura forniti da ClearType in subpixel, in modo che il testo abbia un aspetto coerente all'interno dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fb704-247">When adding DirectWrite text to these applications, it may be necessary to sacrifice the reading experience improvements provided by sub-pixel ClearType so that text has a consistent appearance across the application.</span></span>

<span data-ttu-id="fb704-248">Per soddisfare questi requisiti, [DirectWrite](direct-write-portal.md) supporta anche le seguenti opzioni di rendering:</span><span class="sxs-lookup"><span data-stu-id="fb704-248">To meet these requirements, [DirectWrite](direct-write-portal.md) also supports the following rendering options:</span></span>

-   <span data-ttu-id="fb704-249">ClearType del sottopixel (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="fb704-249">Sub-pixel ClearType (default).</span></span>
-   <span data-ttu-id="fb704-250">ClearType dei sottopixel con anti-aliasing in dimensioni orizzontali e verticali.</span><span class="sxs-lookup"><span data-stu-id="fb704-250">Sub-pixel ClearType with anti-aliasing in both horizontal and vertical dimensions.</span></span>
-   <span data-ttu-id="fb704-251">Testo con alias.</span><span class="sxs-lookup"><span data-stu-id="fb704-251">Aliased text.</span></span>
-   <span data-ttu-id="fb704-252">GDI naturale a larghezza (usato da Microsoft Word visualizzazione di lettura, ad esempio).</span><span class="sxs-lookup"><span data-stu-id="fb704-252">GDI natural-width (used by Microsoft Word Reading View, for example).</span></span>
-   <span data-ttu-id="fb704-253">Compatibile con GDI: larghezza (inclusa la bitmap incorporata dell'Asia orientale).</span><span class="sxs-lookup"><span data-stu-id="fb704-253">GDI compatible-width (including East Asian embedded bitmap).</span></span>

<span data-ttu-id="fb704-254">Ognuna di queste modalità di rendering può essere ottimizzata tramite l'API DirectWrite e tramite il nuovo sintonizzatore ClearType della posta in arrivo di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fb704-254">Each of these rendering modes can be fine-tuned through the DirectWrite API and through the new Windows 7 inbox ClearType tuner.</span></span>

> [!Note]  
> <span data-ttu-id="fb704-255">A partire da Windows 8, è consigliabile usare l'anti-aliasing del testo in scala di grigi nella maggior parte dei casi.</span><span class="sxs-lookup"><span data-stu-id="fb704-255">Starting with Windows 8, you should use greyscale text antialiasing in most cases.</span></span> <span data-ttu-id="fb704-256">Per altre informazioni, vedere la sezione seguente.</span><span class="sxs-lookup"><span data-stu-id="fb704-256">See the next section for more information.</span></span>

 

### <a name="support-for-natural-layout"></a><span data-ttu-id="fb704-257">Supporto per il layout naturale</span><span class="sxs-lookup"><span data-stu-id="fb704-257">Support for Natural Layout</span></span>

<span data-ttu-id="fb704-258">Il layout naturale è indipendente dalla risoluzione, quindi la spaziatura dei caratteri non cambia quando si esegue lo zoom avanti o indietro o a seconda del valore DPI dello schermo.</span><span class="sxs-lookup"><span data-stu-id="fb704-258">Natural layout is resolution-independent, so the spacing of characters doesn't change as you zoom in or out, or depending on the DPI of the display.</span></span> <span data-ttu-id="fb704-259">Un vantaggio secondario è che la spaziatura è vera per la progettazione del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="fb704-259">A secondary advantage is that spacing is true to the design of the font.</span></span> <span data-ttu-id="fb704-260">Il layout naturale è reso possibile dal supporto di DirectWrite per il rendering naturale, il che significa che i singoli glifi possono essere posizionati in una frazione di pixel.</span><span class="sxs-lookup"><span data-stu-id="fb704-260">Natural layout is made possible by DirectWrite's support for natural rendering, which means individual glyphs can be positioned to a fraction of a pixel.</span></span>

<span data-ttu-id="fb704-261">Sebbene il layout naturale sia quello predefinito, alcune applicazioni devono eseguire il rendering del testo con la stessa spaziatura e l'aspetto di GDI.</span><span class="sxs-lookup"><span data-stu-id="fb704-261">While natural layout is the default, some applications need to render text with the same spacing and appearance as GDI.</span></span> <span data-ttu-id="fb704-262">Per tali applicazioni, DirectWrite fornisce le modalità di misurazione naturale GDI classico e GDI e le modalità di rendering corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="fb704-262">For such applications, DirectWrite provides GDI classic and GDI natural measuring modes and corresponding rendering modes.</span></span>

<span data-ttu-id="fb704-263">Una delle modalità di rendering sopra elencate può essere combinata con una delle due modalità di anti-aliasing: ClearType o scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="fb704-263">Any of the above rendering modes can be combined with either of the two antialiasing modes: ClearType or grayscale.</span></span> <span data-ttu-id="fb704-264">L'anti-aliasing ClearType simula una risoluzione più elevata modificando singolarmente i valori di colore rosso, verde e blu di ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="fb704-264">ClearType antialiasing simulations a higher resolution by individually manipulating the red, green, and blue color values of each pixel.</span></span> <span data-ttu-id="fb704-265">L'anti-aliasing in scala di grigi calcola un solo valore di code coverage (o Alpha) per ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="fb704-265">Grayscale antialiasing computes only one coverage (or alpha) value for each pixel.</span></span> <span data-ttu-id="fb704-266">ClearType è l'impostazione predefinita, ma l'anti-aliasing in scala di grigi è consigliato per le app di Windows Store perché è più veloce ed è compatibile con l'anti-aliasing standard, pur continuando a essere estremamente leggibile.</span><span class="sxs-lookup"><span data-stu-id="fb704-266">ClearType is the default, but grayscale antialiasing is recommended for Windows Store apps because it is faster and is compatible with standard antialiasing, while still being highly readable.</span></span>

## <a name="api-overview"></a><span data-ttu-id="fb704-267">Panoramica API</span><span class="sxs-lookup"><span data-stu-id="fb704-267">API Overview</span></span>

<span data-ttu-id="fb704-268">L'interfaccia [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) è il punto di partenza per l'uso della funzionalità DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="fb704-268">The [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface is the starting point for using DirectWrite functionality.</span></span> <span data-ttu-id="fb704-269">La Factory è l'oggetto radice che crea un set di oggetti che possono essere usati insieme.</span><span class="sxs-lookup"><span data-stu-id="fb704-269">The factory is the root object that creates a set of objects that can be used together.</span></span>

<span data-ttu-id="fb704-270">L'operazione di formattazione e layout è un prerequisito per le operazioni, in quanto il testo deve essere formattato correttamente e disposto a un set di vincoli specificato prima di poter essere disegnato o sottoposto a hit test.</span><span class="sxs-lookup"><span data-stu-id="fb704-270">The formatting and layout operation is a prerequisite to the operations, as text needs to be properly formatted and laid out to a specified set of constraints before it can be drawn or hit-tested.</span></span> <span data-ttu-id="fb704-271">Due oggetti chiave che è possibile creare con un [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) a questo scopo sono [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span><span class="sxs-lookup"><span data-stu-id="fb704-271">Two key objects that you can create with an [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) for this purpose are [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="fb704-272">Un oggetto **IDWriteTextFormat** rappresenta le informazioni di formattazione per un paragrafo di testo.</span><span class="sxs-lookup"><span data-stu-id="fb704-272">An **IDWriteTextFormat** object represents the formatting information for a paragraph of text.</span></span> <span data-ttu-id="fb704-273">La funzione [**IDWriteFactory archiviata nei:: CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) accetta la stringa di input, i vincoli associati, ad esempio la dimensione dello spazio da compilare e l'oggetto **IDWriteTextFormat** , e inserisce il risultato completamente analizzato e formattato in **IDWriteTextLayout** da usare nelle operazioni successive.</span><span class="sxs-lookup"><span data-stu-id="fb704-273">The [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) function takes the input string, the associated constraints such as the dimension of the space to be filled, and the **IDWriteTextFormat** object, and puts the fully analyzed and formatted result into **IDWriteTextLayout** to use in subsequent operations.</span></span>

<span data-ttu-id="fb704-274">L'applicazione può quindi eseguire il rendering del testo utilizzando la funzione [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) fornita da [Direct2D](../direct2d/direct2d-portal.md) o implementando una funzione di callback che può utilizzare GDI, Direct2D o altri sistemi grafici per eseguire il rendering dei glifi.</span><span class="sxs-lookup"><span data-stu-id="fb704-274">The application can then render the text using the [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) function provided by [Direct2D](../direct2d/direct2d-portal.md) or by implementing a callback function that can use GDI, Direct2D, or other graphics systems to render the glyphs.</span></span> <span data-ttu-id="fb704-275">Per un singolo testo di formato, la funzione [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) su Direct2D fornisce un modo più semplice per creare testo senza dover prima creare un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="fb704-275">For a single format text, the [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) function on Direct2D provides a simpler way to draw text without having to first create a [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

## <a name="formatting-and-drawing-hello-world-using-directwrite"></a><span data-ttu-id="fb704-276">Formattazione e disegno di "Hello World" con DirectWrite</span><span class="sxs-lookup"><span data-stu-id="fb704-276">Formatting and Drawing "Hello World" Using DirectWrite</span></span>

<span data-ttu-id="fb704-277">Nell'esempio di codice riportato di seguito viene illustrato come un'applicazione può formattare un singolo paragrafo utilizzando [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e come utilizzarla per creare la funzione di [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="fb704-277">The following code example shows how an application can format a single paragraph using [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and draw it using the [Direct2D](../direct2d/direct2d-portal.md)[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) function.</span></span>


```C++
HRESULT DemoApp::DrawHelloWorld(
    ID2D1HwndRenderTarget* pIRenderTarget
    )
{
    HRESULT hr = S_OK;
    ID2D1SolidColorBrush* pIRedBrush = NULL;
    IDWriteTextFormat* pITextFormat = NULL;
    IDWriteFactory* pIDWriteFactory = NULL;

    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED,
                __uuidof(IDWriteFactory),
                reinterpret_cast<IUnknown**>(&pIDWriteFactory));
    }

    if(SUCCEEDED(hr))
    {
        hr = pIDWriteFactory->CreateTextFormat(
            L"Arial", 
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL, 
            DWRITE_FONT_STYLE_NORMAL, 
            DWRITE_FONT_STRETCH_NORMAL, 
            10.0f * 96.0f/72.0f, 
            L"en-US", 
            &pITextFormat
        );
    }

    if(SUCCEEDED(hr))
    {
        hr = pIRenderTarget->CreateSolidColorBrush(
            D2D1:: ColorF(D2D1::ColorF::Red),
            &pIRedBrush
        );
    }
    
   D2D1_RECT_F layoutRect = D2D1::RectF(0.f, 0.f, 100.f, 100.f);

    // Actually draw the text at the origin.
    if(SUCCEEDED(hr))
    {
        pIRenderTarget->DrawText(
            L"Hello World",
            wcslen(L"Hello World"),
            pITextFormat,
            layoutRect, 
            pIRedBrush
        );
    }

    // Clean up.
    SafeRelease(&pIRedBrush);
    SafeRelease(&pITextFormat);
    SafeRelease(&pIDWriteFactory);

    return hr;
}
```



## <a name="accessing-the-font-system"></a><span data-ttu-id="fb704-278">Accesso al sistema di tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="fb704-278">Accessing the Font System</span></span>

<span data-ttu-id="fb704-279">Oltre a specificare un nome della famiglia di caratteri per la stringa di testo usando l'interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) nell'esempio precedente, [DirectWrite](direct-write-portal.md) offre alle applicazioni un maggiore controllo sulla selezione dei tipi di carattere tramite l'enumerazione dei tipi di carattere e la possibilità di creare una raccolta di tipi di carattere personalizzata basata su tipi di carattere incorporati.</span><span class="sxs-lookup"><span data-stu-id="fb704-279">In addition to specifying a font family name for the text string by using the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface in the example above, [DirectWrite](direct-write-portal.md) provides applications more control over font selection through font enumeration and the ability to create custom font collection based on embedded document fonts.</span></span>

<span data-ttu-id="fb704-280">L'oggetto [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) è una raccolta di famiglie di caratteri.</span><span class="sxs-lookup"><span data-stu-id="fb704-280">The [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) object is a collection of font families.</span></span> <span data-ttu-id="fb704-281">DirectWrite consente di accedere al set di tipi di carattere installati nel sistema tramite una raccolta di tipi di carattere speciale denominata raccolta di tipi di carattere di sistema.</span><span class="sxs-lookup"><span data-stu-id="fb704-281">DirectWrite provides access to the set of fonts installed on the system through a special font collection called the system font collection.</span></span> <span data-ttu-id="fb704-282">Questa operazione viene ottenuta chiamando il metodo [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) dell'oggetto [**IDWriteFactory archiviata nei**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="fb704-282">This is obtained by calling the [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) method of the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) object.</span></span> <span data-ttu-id="fb704-283">Un'applicazione può inoltre creare una raccolta di tipi di carattere personalizzata da un set di tipi di carattere enumerati da un callback definito dall'applicazione, ovvero tipi di carattere privati installati da un'applicazione o tipi di carattere incorporati in un documento.</span><span class="sxs-lookup"><span data-stu-id="fb704-283">An application can also create a custom font collection from a set of fonts enumerated by an application-defined callback, that is, private fonts installed by an application, or fonts embedded in a document.</span></span>

<span data-ttu-id="fb704-284">L'applicazione può quindi chiamare [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) per ottenere un oggetto FontFamily specifico all'interno della raccolta e quindi chiamare [**IDWriteFontFamily:: GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) per ottenere un oggetto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) specifico.</span><span class="sxs-lookup"><span data-stu-id="fb704-284">The application can then call [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) to get to a specific FontFamily object within the collection, and then call [**IDWriteFontFamily::GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) to get to a specific [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object.</span></span> <span data-ttu-id="fb704-285">L'oggetto **IDWriteFont** rappresenta un tipo di carattere in una raccolta di tipi di carattere ed espone le proprietà e alcune metriche dei tipi di carattere di base.</span><span class="sxs-lookup"><span data-stu-id="fb704-285">The **IDWriteFont** object represents a font in a font collection and exposes properties and a few basic font metrics.</span></span>

<span data-ttu-id="fb704-286">[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) è un altro oggetto che rappresenta un tipo di carattere ed espone un set completo di metriche su un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="fb704-286">The [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) is another object that represents a font and exposes a full set of metrics on a font.</span></span> <span data-ttu-id="fb704-287">**IDWriteFontFace** può essere creato direttamente da un nome di tipo di carattere; per accedere a un'applicazione non è necessario ottenere una raccolta di tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="fb704-287">The **IDWriteFontFace** can be created directly from a font name; an application does not have to get a font collection to access it.</span></span> <span data-ttu-id="fb704-288">È utile per un'applicazione di layout di testo, ad esempio Microsoft Word, che deve eseguire una query sui dettagli per un tipo di carattere specifico.</span><span class="sxs-lookup"><span data-stu-id="fb704-288">It is useful for a text layout application such as Microsoft Word that needs to query the details for a specific font.</span></span>

<span data-ttu-id="fb704-289">Nel diagramma seguente viene illustrata la relazione tra questi oggetti.</span><span class="sxs-lookup"><span data-stu-id="fb704-289">The following diagram illustrates the relationship between these objects.</span></span>

![diagramma della relazione tra una raccolta di tipi di carattere, una famiglia di caratteri e un tipo di carattere](images/fontcollection.png)

### <a name="idwritefontface"></a><span data-ttu-id="fb704-291">IDWriteFontFace</span><span class="sxs-lookup"><span data-stu-id="fb704-291">IDWriteFontFace</span></span>

<span data-ttu-id="fb704-292">L'oggetto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) rappresenta un tipo di carattere e fornisce informazioni più dettagliate sul tipo di carattere rispetto all'oggetto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) .</span><span class="sxs-lookup"><span data-stu-id="fb704-292">The [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object represents a font and provides more detailed information about the font than the [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object does.</span></span> <span data-ttu-id="fb704-293">Le metriche relative al tipo di carattere e al glifo della **IDWriteFontFace** sono utili per le applicazioni che implementano il layout del testo.</span><span class="sxs-lookup"><span data-stu-id="fb704-293">The font and glyph metrics from the **IDWriteFontFace** are useful for applications that implement text layout.</span></span>

<span data-ttu-id="fb704-294">La maggior parte delle applicazioni mainstream non utilizzerà queste API direttamente e utilizzerà invece [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) o specifica direttamente il nome della famiglia di caratteri.</span><span class="sxs-lookup"><span data-stu-id="fb704-294">Most mainstream applications will not use these APIs directly, and instead will use [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) or specify the font family name directly.</span></span>

<span data-ttu-id="fb704-295">Nella tabella seguente sono riepilogati gli scenari di utilizzo per i due oggetti.</span><span class="sxs-lookup"><span data-stu-id="fb704-295">The following table summarizes the usage scenarios for the two objects.</span></span>



| <span data-ttu-id="fb704-296">Category</span><span class="sxs-lookup"><span data-stu-id="fb704-296">Category</span></span>                                                                                                         | [<span data-ttu-id="fb704-297">**IDWriteFont**</span><span class="sxs-lookup"><span data-stu-id="fb704-297">**IDWriteFont**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | [<span data-ttu-id="fb704-298">**IDWriteFontFace**</span><span class="sxs-lookup"><span data-stu-id="fb704-298">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="fb704-299">API per supportare l'interazione dell'utente, ad esempio un'interfaccia utente di selezione dei tipi di carattere: Descrizione e altre API informative</span><span class="sxs-lookup"><span data-stu-id="fb704-299">APIs to support user interaction such as a font-chooser user interface: description and other informational APIs</span></span> | <span data-ttu-id="fb704-300">Sì</span><span class="sxs-lookup"><span data-stu-id="fb704-300">Yes</span></span>                                        | <span data-ttu-id="fb704-301">No</span><span class="sxs-lookup"><span data-stu-id="fb704-301">No</span></span>                                                 |
| <span data-ttu-id="fb704-302">API per supportare il mapping dei tipi di carattere: famiglia, stile, peso, estensione, code coverage dei caratteri</span><span class="sxs-lookup"><span data-stu-id="fb704-302">APIs to support font mapping: family, style, weight, stretch, character coverage</span></span>                                 | <span data-ttu-id="fb704-303">Sì</span><span class="sxs-lookup"><span data-stu-id="fb704-303">Yes</span></span>                                        | <span data-ttu-id="fb704-304">No</span><span class="sxs-lookup"><span data-stu-id="fb704-304">No</span></span>                                                 |
| <span data-ttu-id="fb704-305">API DrawText</span><span class="sxs-lookup"><span data-stu-id="fb704-305">DrawText API</span></span>                                                                                                     | <span data-ttu-id="fb704-306">Sì</span><span class="sxs-lookup"><span data-stu-id="fb704-306">Yes</span></span>                                        | <span data-ttu-id="fb704-307">No</span><span class="sxs-lookup"><span data-stu-id="fb704-307">No</span></span>                                                 |
| <span data-ttu-id="fb704-308">API usate per il rendering</span><span class="sxs-lookup"><span data-stu-id="fb704-308">APIs used for rendering</span></span>                                                                                          | <span data-ttu-id="fb704-309">No</span><span class="sxs-lookup"><span data-stu-id="fb704-309">No</span></span>                                         | <span data-ttu-id="fb704-310">Sì</span><span class="sxs-lookup"><span data-stu-id="fb704-310">Yes</span></span>                                                |
| <span data-ttu-id="fb704-311">API usate per il layout del testo: metriche del glifo e così via</span><span class="sxs-lookup"><span data-stu-id="fb704-311">APIs used for text layout: glyph metrics, and so on</span></span>                                                              | <span data-ttu-id="fb704-312">No</span><span class="sxs-lookup"><span data-stu-id="fb704-312">No</span></span>                                         | <span data-ttu-id="fb704-313">Sì</span><span class="sxs-lookup"><span data-stu-id="fb704-313">Yes</span></span>                                                |
| <span data-ttu-id="fb704-314">API per il controllo dell'interfaccia utente e il layout del testo: metriche a livello di carattere</span><span class="sxs-lookup"><span data-stu-id="fb704-314">APIs for UI control and text layout: font-wide metrics</span></span>                                                           | <span data-ttu-id="fb704-315">Sì</span><span class="sxs-lookup"><span data-stu-id="fb704-315">Yes</span></span>                                        | <span data-ttu-id="fb704-316">Sì</span><span class="sxs-lookup"><span data-stu-id="fb704-316">Yes</span></span>                                                |



 

<span data-ttu-id="fb704-317">Di seguito è riportato un esempio di applicazione che enumera i tipi di carattere nella raccolta di tipi di carattere di sistema.</span><span class="sxs-lookup"><span data-stu-id="fb704-317">The following is an example application that enumerates the fonts in the system font collection.</span></span>


```C++
#include <dwrite.h>
#include <string.h>
#include <stdio.h>
#include <new>

// SafeRelease inline function.
template <class T> inline void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

void wmain()
{
    IDWriteFactory* pDWriteFactory = NULL;

    HRESULT hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory)
            );

    IDWriteFontCollection* pFontCollection = NULL;

    // Get the system font collection.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
    }

    UINT32 familyCount = 0;

    // Get the number of font families in the collection.
    if (SUCCEEDED(hr))
    {
        familyCount = pFontCollection->GetFontFamilyCount();
    }

    for (UINT32 i = 0; i < familyCount; ++i)
    {
        IDWriteFontFamily* pFontFamily = NULL;

        // Get the font family.
        if (SUCCEEDED(hr))
        {
            hr = pFontCollection->GetFontFamily(i, &pFontFamily);
        }

        IDWriteLocalizedStrings* pFamilyNames = NULL;
        
        // Get a list of localized strings for the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFontFamily->GetFamilyNames(&pFamilyNames);
        }

        UINT32 index = 0;
        BOOL exists = false;
        
        wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

        if (SUCCEEDED(hr))
        {
            // Get the default locale for this user.
            int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

            // If the default locale is returned, find that locale name, otherwise use "en-us".
            if (defaultLocaleSuccess)
            {
                hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
            }
            if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
            {
                hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
            }
        }
        
        // If the specified locale doesn't exist, select the first on the list.
        if (!exists)
            index = 0;

        UINT32 length = 0;

        // Get the string length.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetStringLength(index, &length);
        }

        // Allocate a string big enough to hold the name.
        wchar_t* name = new (std::nothrow) wchar_t[length+1];
        if (name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Get the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetString(index, name, length+1);
        }
        if (SUCCEEDED(hr))
        {
            // Print out the family name.
            wprintf(L"%s\n", name);
        }

        SafeRelease(&pFontFamily);
        SafeRelease(&pFamilyNames);

        delete [] name;
    }

    SafeRelease(&pFontCollection);
    SafeRelease(&pDWriteFactory);
}

```



## <a name="text-rendering"></a><span data-ttu-id="fb704-318">Rendering del testo</span><span class="sxs-lookup"><span data-stu-id="fb704-318">Text rendering</span></span>

<span data-ttu-id="fb704-319">Le API per il rendering del testo consentono di eseguire il rendering dei glifi in un tipo di carattere [DirectWrite](direct-write-portal.md) in una superficie [Direct2D](../direct2d/direct2d-portal.md) o in una bitmap indipendente dal dispositivo GDI oppure di essere convertiti in strutture o bitmap.</span><span class="sxs-lookup"><span data-stu-id="fb704-319">The text rendering APIs enable glyphs in a [DirectWrite](direct-write-portal.md) font to be rendered to a [Direct2D](../direct2d/direct2d-portal.md) surface or to a GDI device independent bitmap, or to be converted to outlines or bitmaps.</span></span> <span data-ttu-id="fb704-320">Il rendering ClearType in DirectWrite supporta il posizionamento dei subpixel con maggiore nitidezza e contrasto rispetto alle implementazioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="fb704-320">The ClearType rendering in DirectWrite supports sub-pixel positioning with improved sharpness and contrast compared to previous implementations on Windows.</span></span> <span data-ttu-id="fb704-321">DirectWrite supporta anche testo in bianco e nero con alias per supportare scenari che coinvolgono caratteri asiatici orientali con bitmap incorporate o in cui l'utente ha disabilitato la smussatura dei caratteri di qualsiasi tipo.</span><span class="sxs-lookup"><span data-stu-id="fb704-321">DirectWrite also supports aliased black-and-white text to support scenarios involving East Asian fonts with embedded bitmaps, or where the user has disabled font smoothing of any type.</span></span>

<span data-ttu-id="fb704-322">Tutte le opzioni sono regolabili da tutte le manopole ClearType disponibili accessibili tramite le API [DirectWrite](direct-write-portal.md) ed esposte anche tramite la nuova applet del pannello di controllo del sintonizzatore ClearType di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fb704-322">All the options are adjustable by all the available ClearType knobs accessible through the [DirectWrite](direct-write-portal.md) APIs, and also exposed via the new Windows 7 ClearType tuner control panel applet.</span></span>

<span data-ttu-id="fb704-323">Sono disponibili due API per il rendering dei glifi, una che fornisce il rendering con accelerazione hardware tramite [Direct2D](../direct2d/direct2d-portal.md) e l'altra che fornisce il rendering del software a una bitmap GDI.</span><span class="sxs-lookup"><span data-stu-id="fb704-323">There are two APIs available for rendering glyphs, one providing hardware-accelerated rendering through [Direct2D](../direct2d/direct2d-portal.md) and the other providing software rendering to a GDI bitmap.</span></span> <span data-ttu-id="fb704-324">Un'applicazione che usa [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e l'implementazione del callback [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) può chiamare una di queste funzioni in risposta a un callback [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) .</span><span class="sxs-lookup"><span data-stu-id="fb704-324">An application using [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) and implementing the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) callback can call either of these functions in response to a [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) callback.</span></span> <span data-ttu-id="fb704-325">Inoltre, le applicazioni che implementano il proprio layout o gestiscono i dati a livello di glifo possono usare queste API.</span><span class="sxs-lookup"><span data-stu-id="fb704-325">Also, applications that implement their own layout or deal with glyph-level data can use these APIs.</span></span>

1.  [<span data-ttu-id="fb704-326">**ID2DRenderTarget::D rawGlyphRun**</span><span class="sxs-lookup"><span data-stu-id="fb704-326">**ID2DRenderTarget::DrawGlyphRun**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)

    <span data-ttu-id="fb704-327">Le applicazioni possono usare l'API [Direct2D](../direct2d/direct2d-portal.md) [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) per fornire l'accelerazione hardware per il rendering del testo con la GPU.</span><span class="sxs-lookup"><span data-stu-id="fb704-327">Applications can use the [Direct2D](../direct2d/direct2d-portal.md) API [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) to provide hardware acceleration for text rendering using the GPU.</span></span> <span data-ttu-id="fb704-328">L'accelerazione hardware ha effetto su tutte le fasi della pipeline di rendering del testo, dall'Unione di glifi alle esecuzioni di glifi e dall'applicazione di filtri alla bitmap di esecuzione del glifo, all'applicazione dell'algoritmo di Blend ClearType all'output visualizzato finale.</span><span class="sxs-lookup"><span data-stu-id="fb704-328">Hardware acceleration affects all phases of the text rendering pipeline—from merging glyphs into glyph runs and filtering the glyph-run bitmap, to applying the ClearType blending algorithm to the final displayed output.</span></span> <span data-ttu-id="fb704-329">Si tratta dell'API consigliata per ottenere le migliori prestazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="fb704-329">This is the recommended API for getting the best rendering performance.</span></span>

2.  [<span data-ttu-id="fb704-330">**IDWriteBitmapRenderTarget::D rawGlyphRun**</span><span class="sxs-lookup"><span data-stu-id="fb704-330">**IDWriteBitmapRenderTarget::DrawGlyphRun**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)

    <span data-ttu-id="fb704-331">Le applicazioni possono usare il metodo [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) per eseguire il rendering del software di un'esecuzione di glifi in una bitmap da 32 BPP.</span><span class="sxs-lookup"><span data-stu-id="fb704-331">Applications can use the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to perform a software-rendering of a run of glyphs to a 32-bpp bitmap.</span></span> <span data-ttu-id="fb704-332">L'oggetto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) incapsula una bitmap e un contesto di dispositivo di memoria che può essere usato per il rendering dei glifi.</span><span class="sxs-lookup"><span data-stu-id="fb704-332">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object encapsulates a bitmap and a memory device context that can be used for rendering glyphs.</span></span> <span data-ttu-id="fb704-333">Questa API è utile se si desidera rimanere con GDI perché si dispone di una codebase esistente che esegue il rendering in GDI.</span><span class="sxs-lookup"><span data-stu-id="fb704-333">This API is useful if you want to stay with GDI because you have an existing code base that renders in GDI.</span></span>

<span data-ttu-id="fb704-334">Se si dispone di un'applicazione che dispone di codice di layout di testo che utilizza GDI e si desidera mantenere il codice di layout esistente ma si utilizza [DirectWrite](direct-write-portal.md) solo per il passaggio finale dei glifi di rendering, [**IDWriteGdiInterop:: CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) fornisce il Bridge tra le due API.</span><span class="sxs-lookup"><span data-stu-id="fb704-334">If you have an application that has existing text layout code that uses GDI, and you want to preserve its existing layout code but use [DirectWrite](direct-write-portal.md) just for the final step of rendering glyphs, [**IDWriteGdiInterop::CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) provides the bridge between the two APIs.</span></span> <span data-ttu-id="fb704-335">Prima di chiamare questa funzione, l'applicazione userà la funzione **IDWriteGdiInterop:: CreateFontFaceFromHdc** per ottenere un riferimento del tipo di carattere da un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb704-335">Before calling this function, the application will use the **IDWriteGdiInterop::CreateFontFaceFromHdc** function to get a font-face reference from a device context.</span></span>

> [!Note]  
> <span data-ttu-id="fb704-336">Per la maggior parte degli scenari, è possibile che le applicazioni non debbano usare queste API per il rendering di glifi.</span><span class="sxs-lookup"><span data-stu-id="fb704-336">For most scenarios, applications may not need to use these glyph-rendering APIs.</span></span> <span data-ttu-id="fb704-337">Dopo che un'applicazione ha creato un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , può usare il metodo [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) per eseguire il rendering del testo.</span><span class="sxs-lookup"><span data-stu-id="fb704-337">After an application has created an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object, it can use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method to render the text.</span></span>

 

## <a name="custom-rendering-modes"></a><span data-ttu-id="fb704-338">Modalità di rendering personalizzate</span><span class="sxs-lookup"><span data-stu-id="fb704-338">Custom Rendering Modes</span></span>

<span data-ttu-id="fb704-339">Un numero di parametri influisce sul rendering del testo, ad esempio gamma, livello ClearType, geometria pixel e contrasto migliorato.</span><span class="sxs-lookup"><span data-stu-id="fb704-339">A number of parameters affect text rendering, such as gamma, ClearType level, pixel geometry, and enhanced contrast.</span></span> <span data-ttu-id="fb704-340">I parametri di rendering sono incapsulati da un oggetto che implementa l'interfaccia [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) pubblica.</span><span class="sxs-lookup"><span data-stu-id="fb704-340">Rendering parameters are encapsulated by an object, which implements the public [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) interface.</span></span> <span data-ttu-id="fb704-341">L'oggetto parametri di rendering viene inizializzato automaticamente in base alle proprietà hardware e/o alle preferenze utente specificate tramite l'applet del pannello di controllo ClearType in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fb704-341">The rendering parameters object is automatically initialized based on hardware properties and/or user preferences specified through the ClearType control panel applet in Windows 7.</span></span> <span data-ttu-id="fb704-342">In genere, se un client usa l'API di layout [DirectWrite](direct-write-portal.md) , DirectWrite seleziona automaticamente una modalità di rendering che corrisponde alla modalità di misurazione specificata.</span><span class="sxs-lookup"><span data-stu-id="fb704-342">Generally, if a client uses the [DirectWrite](direct-write-portal.md) layout API, DirectWrite will automatically select a rendering mode that corresponds to the specified measuring mode.</span></span>

<span data-ttu-id="fb704-343">Le applicazioni che vogliono un maggiore controllo possono usare [**IDWriteFactory archiviata nei:: CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) per implementare le diverse opzioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="fb704-343">Applications that want more control can use [**IDWriteFactory::CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) to implement the different rendering options.</span></span> <span data-ttu-id="fb704-344">Questa funzione può essere usata anche per impostare la gamma, la geometria dei pixel e il contrasto migliorato.</span><span class="sxs-lookup"><span data-stu-id="fb704-344">This function can also be used to set the gamma, pixel geometry, and enhanced contrast.</span></span>

<span data-ttu-id="fb704-345">Di seguito sono riportate le varie opzioni di rendering disponibili:</span><span class="sxs-lookup"><span data-stu-id="fb704-345">The following are the various rendering options available:</span></span>

-   <span data-ttu-id="fb704-346">Anti-aliasing sub-pixel</span><span class="sxs-lookup"><span data-stu-id="fb704-346">Sub-pixel anti-aliasing</span></span>

    <span data-ttu-id="fb704-347">L'applicazione imposta il parametro *renderingMode* sulla \_ modalità di rendering DWrite \_ \_ Natural per specificare il rendering con anti-aliasing solo nella dimensione orizzontale.</span><span class="sxs-lookup"><span data-stu-id="fb704-347">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_NATURAL to specify rendering with anti-aliasing in the horizontal dimension only.</span></span>

-   <span data-ttu-id="fb704-348">Anti-aliasing di sottopixel in dimensioni orizzontali e verticali.</span><span class="sxs-lookup"><span data-stu-id="fb704-348">Sub-pixel anti-aliasing in both horizontal and vertical dimensions.</span></span>

    <span data-ttu-id="fb704-349">L'applicazione imposta il parametro *renderingMode* sulla \_ modalità di rendering DWrite \_ \_ Natural \_ simmetrica per specificare il rendering con anti-aliasing nelle dimensioni orizzontale e verticale.</span><span class="sxs-lookup"><span data-stu-id="fb704-349">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_NATURAL\_SYMMETRIC to specify rendering with anti-aliasing in both horizontal and vertical dimensions.</span></span> <span data-ttu-id="fb704-350">In questo modo, le curve e le linee diagonali sembrano più smussate a scapito della morbidezza e vengono in genere usate in dimensioni superiori a 16 ppem.</span><span class="sxs-lookup"><span data-stu-id="fb704-350">This makes curves and diagonal lines look smoother at the expense of some softness, and is typically used at sizes above 16 ppem.</span></span>

-   <span data-ttu-id="fb704-351">Testo con alias</span><span class="sxs-lookup"><span data-stu-id="fb704-351">Aliased Text</span></span>

    <span data-ttu-id="fb704-352">L'applicazione imposta il parametro *renderingMode* su \_ modalità di rendering DWrite \_ \_ con alias per specificare il testo con alias.</span><span class="sxs-lookup"><span data-stu-id="fb704-352">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_ALIASED to specify aliased text.</span></span>

-   <span data-ttu-id="fb704-353">Testo in scala di grigi</span><span class="sxs-lookup"><span data-stu-id="fb704-353">Grayscale Text</span></span>

    <span data-ttu-id="fb704-354">L'applicazione imposta il parametro *pixelGeometry* su DWrite \_ pixel \_ Geometry \_ flat per specificare il testo in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="fb704-354">The application sets the *pixelGeometry* parameter to DWRITE\_PIXEL\_GEOMETRY\_FLAT to specify grayscale text.</span></span>

-   <span data-ttu-id="fb704-355">Compatibile con GDI: larghezza (inclusa la bitmap incorporata dell'Asia orientale)</span><span class="sxs-lookup"><span data-stu-id="fb704-355">GDI compatible-width (including East Asian embedded bitmap)</span></span>

    <span data-ttu-id="fb704-356">L'applicazione imposta il parametro *renderingMode* sulla \_ modalità di rendering DWrite \_ \_ GDI \_ classico per specificare l'anti-aliasing a larghezza compatibile con GDI.</span><span class="sxs-lookup"><span data-stu-id="fb704-356">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_GDI\_CLASSIC to specify GDI compatible-width anti-aliasing.</span></span>

-   <span data-ttu-id="fb704-357">GDI naturale-larghezza</span><span class="sxs-lookup"><span data-stu-id="fb704-357">GDI natural-width</span></span>

    <span data-ttu-id="fb704-358">L'applicazione imposta il parametro *renderingMode* sulla \_ modalità di rendering DWrite \_ \_ GDI \_ Natural per specificare l'anti-aliasing compatibile con larghezza naturale GDI.</span><span class="sxs-lookup"><span data-stu-id="fb704-358">The application sets the *renderingMode* parameter to DWRITE\_RENDERING\_MODE\_GDI\_NATURAL to specify GDI natural-width compatible anti-aliasing.</span></span>

-   <span data-ttu-id="fb704-359">Testo struttura</span><span class="sxs-lookup"><span data-stu-id="fb704-359">Outline text</span></span>

    <span data-ttu-id="fb704-360">Per il rendering di grandi dimensioni, uno sviluppatore di applicazioni potrebbe preferire il rendering usando il contorno dei tipi di carattere anziché eseguendo la rasterizzazione in una bitmap.</span><span class="sxs-lookup"><span data-stu-id="fb704-360">For rendering at large sizes, an application developer might prefer to render by using the font outline rather than by rasterizing into a bitmap.</span></span> <span data-ttu-id="fb704-361">L'applicazione imposta il parametro *renderingMode* sulla **\_ \_ \_ struttura della modalità di rendering DWrite** per specificare che il rendering deve ignorare il rasterizzatore e utilizzare direttamente le strutture.</span><span class="sxs-lookup"><span data-stu-id="fb704-361">The application sets the *renderingMode* parameter to **DWRITE\_RENDERING\_MODE\_OUTLINE** to specify that rendering should bypass the rasterizer and use the outlines directly.</span></span>

## <a name="gdi-interoperability"></a><span data-ttu-id="fb704-362">Interoperabilità GDI</span><span class="sxs-lookup"><span data-stu-id="fb704-362">GDI Interoperability</span></span>

<span data-ttu-id="fb704-363">L'interfaccia [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) fornisce l'interoperabilità con GDI.</span><span class="sxs-lookup"><span data-stu-id="fb704-363">The [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) interface provides interoperability with GDI.</span></span> <span data-ttu-id="fb704-364">Questo consente alle applicazioni di continuare l'investimento esistente nelle basi di codice GDI e di usare selettivamente [DirectWrite](direct-write-portal.md) per il rendering o il layout.</span><span class="sxs-lookup"><span data-stu-id="fb704-364">This enables applications to continue their existing investment in GDI code bases and selectively use [DirectWrite](direct-write-portal.md) for either rendering or layout.</span></span>

<span data-ttu-id="fb704-365">Di seguito sono riportate le API che consentono a un'applicazione di eseguire la migrazione da o verso il sistema di tipi di carattere GDI:</span><span class="sxs-lookup"><span data-stu-id="fb704-365">The following are the APIs that enable an application to migrate to or from the GDI font system:</span></span>

-   [<span data-ttu-id="fb704-366">**CreateFontFromLOGFONT**</span><span class="sxs-lookup"><span data-stu-id="fb704-366">**CreateFontFromLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)

    <span data-ttu-id="fb704-367">Crea un oggetto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) che corrisponde alle proprietà specificate dalla struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="fb704-367">Creates an [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object that matches the properties specified by the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

-   [<span data-ttu-id="fb704-368">**ConvertFontToLOGFONT**</span><span class="sxs-lookup"><span data-stu-id="fb704-368">**ConvertFontToLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)

    <span data-ttu-id="fb704-369">Inizializza una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) basata sulle proprietà compatibili con GDI del [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)specificato.</span><span class="sxs-lookup"><span data-stu-id="fb704-369">Initializes a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure based on the GDI-compatible properties of the specified [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont).</span></span>

-   [<span data-ttu-id="fb704-370">**ConvertFontFaceToLOGFONT**</span><span class="sxs-lookup"><span data-stu-id="fb704-370">**ConvertFontFaceToLOGFONT**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)

    <span data-ttu-id="fb704-371">Inizializza una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) basata sulle proprietà compatibili con GDI del [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)specificato.</span><span class="sxs-lookup"><span data-stu-id="fb704-371">Initializes a [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure based on the GDI-compatible properties of the specified [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface).</span></span>

-   [<span data-ttu-id="fb704-372">**CreateFontFaceFromHdc**</span><span class="sxs-lookup"><span data-stu-id="fb704-372">**CreateFontFaceFromHdc**</span></span>](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc)

    <span data-ttu-id="fb704-373">Crea un oggetto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) che corrisponde al **Hfont** attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="fb704-373">Creates an [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) object that corresponds to the currently selected **HFONT**.</span></span>

## <a name="conclusion"></a><span data-ttu-id="fb704-374">Conclusione</span><span class="sxs-lookup"><span data-stu-id="fb704-374">Conclusion</span></span>

<span data-ttu-id="fb704-375">Il miglioramento dell'esperienza di lettura è di grande importanza per gli utenti che si trovino sullo schermo o su carta.</span><span class="sxs-lookup"><span data-stu-id="fb704-375">Improving the reading experience is of great value to users whether it is on the screen or on paper.</span></span> <span data-ttu-id="fb704-376">[DirectWrite](direct-write-portal.md) offre la facilità d'uso e il modello di programmazione a più livelli per gli sviluppatori di applicazioni per migliorare l'esperienza di testo per le applicazioni Windows.</span><span class="sxs-lookup"><span data-stu-id="fb704-376">[DirectWrite](direct-write-portal.md) provides the ease of use and the layered programming model for application developers to improve the text experience for their Windows applications.</span></span> <span data-ttu-id="fb704-377">Le applicazioni possono usare DirectWrite per eseguire il rendering del testo formattato in modo RTF per l'interfaccia utente e i documenti con l'API layout.</span><span class="sxs-lookup"><span data-stu-id="fb704-377">Applications can use DirectWrite to render richly formatted text for their UI and documents with the layout API.</span></span> <span data-ttu-id="fb704-378">Per scenari più complessi, un'applicazione può lavorare direttamente con glifi, accedere a tipi di carattere e così via e sfruttare la potenza di DirectWrite per offrire funzionalità tipografiche di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="fb704-378">For more complex scenarios, an application can work directly with glyphs, access fonts, and so on, and harness the power of DirectWrite to deliver high-quality typography.</span></span>

<span data-ttu-id="fb704-379">Le funzionalità di interoperabilità di [DirectWrite](direct-write-portal.md) consentono agli sviluppatori di applicazioni di portare avanti le codebase Win32 esistenti e di adottare DirectWrite in modo selettivo all'interno delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="fb704-379">The interoperability capabilities of [DirectWrite](direct-write-portal.md) enable application developers to carry forward their existing Win32 codebases and adopt DirectWrite selectively within their applications.</span></span>

 

 
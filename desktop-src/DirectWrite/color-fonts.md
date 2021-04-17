---
title: Caratteri a colori
description: Questo argomento descrive i tipi di carattere di colore, il relativo supporto in DirectWrite e Direct2D e come usarli nell'app.
ms.assetid: 74e096c4-9d1c-8854-e9ee-f8b11ac1c71a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6774089cc1f0bed1349edc940c6a1ae715d052c7
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "104562652"
---
# <a name="color-fonts"></a><span data-ttu-id="0b08c-103">Caratteri a colori</span><span class="sxs-lookup"><span data-stu-id="0b08c-103">Color Fonts</span></span>

<span data-ttu-id="0b08c-104">Questo argomento descrive i tipi di carattere di colore, il relativo supporto in DirectWrite e Direct2D e come usarli nell'app.</span><span class="sxs-lookup"><span data-stu-id="0b08c-104">This topic describes color fonts, their support in DirectWrite and Direct2D, and how to use them in your app.</span></span>

<span data-ttu-id="0b08c-105">Questo documento contiene le parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b08c-105">This document contains the following parts:</span></span>

-   [<span data-ttu-id="0b08c-106">Che cosa sono i tipi di carattere colore?</span><span class="sxs-lookup"><span data-stu-id="0b08c-106">What are color fonts?</span></span>](#what-are-color-fonts)
-   [<span data-ttu-id="0b08c-107">Perché usare i tipi di carattere colore?</span><span class="sxs-lookup"><span data-stu-id="0b08c-107">Why use color fonts?</span></span>](#why-use-color-fonts)
-   [<span data-ttu-id="0b08c-108">Quali tipi di tipi di carattere colori supporta Windows?</span><span class="sxs-lookup"><span data-stu-id="0b08c-108">What kinds of color fonts does Windows support?</span></span>](#what-kinds-of-color-fonts-does-windows-support)
-   [<span data-ttu-id="0b08c-109">Uso di tipi di carattere colori</span><span class="sxs-lookup"><span data-stu-id="0b08c-109">Using color fonts</span></span>](#using-color-fonts)
    -   [<span data-ttu-id="0b08c-110">Uso di tipi di carattere a colori in un'app XAML</span><span class="sxs-lookup"><span data-stu-id="0b08c-110">Using color fonts in a XAML app</span></span>](#using-color-fonts-in-a-xaml-app)
    -   [<span data-ttu-id="0b08c-111">Uso di tipi di carattere a colori in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0b08c-111">Using color fonts in Microsoft Edge</span></span>](#using-color-fonts-in-microsoft-edge)
    -   [<span data-ttu-id="0b08c-112">Uso dei tipi di carattere colori con DirectWrite e Direct2D</span><span class="sxs-lookup"><span data-stu-id="0b08c-112">Using color fonts with DirectWrite and Direct2D</span></span>](#using-color-fonts-with-directwrite-and-direct2d)
    -   [<span data-ttu-id="0b08c-113">Uso dei tipi di carattere colore con Win2D</span><span class="sxs-lookup"><span data-stu-id="0b08c-113">Using color fonts with Win2D</span></span>](#using-color-fonts-with-win2d)
-   [<span data-ttu-id="0b08c-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0b08c-114">Related topics</span></span>](#related-topics)

## <a name="what-are-color-fonts"></a><span data-ttu-id="0b08c-115">Che cosa sono i tipi di carattere colore?</span><span class="sxs-lookup"><span data-stu-id="0b08c-115">What are color fonts?</span></span>

<span data-ttu-id="0b08c-116">I tipi di carattere colori, detti anche tipi di carattere a colori o tipi di carattere cromatici, rappresentano una tecnologia per i tipi di carattere che consente ai progettisti di utilizzare più colori all'interno di ogni glifo.</span><span class="sxs-lookup"><span data-stu-id="0b08c-116">Color fonts, also referred to as  multicolored fonts  or  chromatic fonts,  are a font technology that allows font designers to use multiple colors within each glyph.</span></span> <span data-ttu-id="0b08c-117">I tipi di carattere colori consentono scenari di testo multicolore in app e siti Web con meno codice e un supporto più affidabile del sistema operativo rispetto alle tecniche ad hoc implementate sopra il sistema di rendering del testo.</span><span class="sxs-lookup"><span data-stu-id="0b08c-117">Color fonts enable multicolored text scenarios in apps and websites with less code and more robust operating system support than ad-hoc techniques implemented above the text rendering system.</span></span>

<span data-ttu-id="0b08c-118">I tipi di carattere con cui si conosce probabilmente non sono tipi di carattere colore.</span><span class="sxs-lookup"><span data-stu-id="0b08c-118">The fonts you are probably most familiar with are not color fonts.</span></span> <span data-ttu-id="0b08c-119">Questi tipi di carattere definiscono solo la forma dei glifi che contengono, sia con le linee di vettore sia con le bitmap monocromatiche.</span><span class="sxs-lookup"><span data-stu-id="0b08c-119">These fonts define only the shape of the glyphs they contain, either with vector outlines or monochromatic bitmaps.</span></span> <span data-ttu-id="0b08c-120">In fase di disegnare, un renderer di testo riempie la forma del glifo usando un solo colore (il colore del carattere) specificato dall'app o dal documento sottoposto a rendering.</span><span class="sxs-lookup"><span data-stu-id="0b08c-120">At draw time, a text renderer fills the glyph shape using a single color (the  font color ) specified by the app or document being rendered.</span></span> <span data-ttu-id="0b08c-121">I tipi di carattere colore, d'altra parte, contengono informazioni sui colori, oltre alle informazioni sulla forma.</span><span class="sxs-lookup"><span data-stu-id="0b08c-121">Color fonts, on the other hand, contain color information in addition to shape information.</span></span> <span data-ttu-id="0b08c-122">Alcuni approcci consentono ai progettisti di tipi di carattere di offrire più tavolozze dei colori, offrendo la flessibilità artistica del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="0b08c-122">Some approaches allow font designers to offer multiple color palettes, giving the color font artistic flexibility.</span></span>

<span data-ttu-id="0b08c-123">Nell'esempio seguente viene illustrato un glifo del tipo di carattere del colore Segoe UI emoji.</span><span class="sxs-lookup"><span data-stu-id="0b08c-123">The following example shows a glyph from the Segoe UI Emoji color font.</span></span> <span data-ttu-id="0b08c-124">Il rendering del glifo viene eseguito in monocromia a sinistra e in colore a destra.</span><span class="sxs-lookup"><span data-stu-id="0b08c-124">The glyph is rendered in monochrome on the left, and in color on the right.</span></span>

![Mostra i glifi affiancati, il glifo di sinistra di cui è stato eseguito il rendering in monocromatico, il diritto nel tipo di carattere colore Segoe U I emoji.](images/color-font-cat.png)

<span data-ttu-id="0b08c-126">I tipi di carattere dei colori includono in genere informazioni di fallback per le piattaforme che non supportano i tipi di carattere colori o per scenari in cui la funzionalità dei colori è stata disabilitata</span><span class="sxs-lookup"><span data-stu-id="0b08c-126">Color fonts typically include fallback information for platforms that do not support color fonts or for scenarios in which color functionality has been disabled.</span></span> <span data-ttu-id="0b08c-127">Su queste piattaforme, i tipi di carattere colore vengono visualizzati come tipi di carattere monocromatici regolari.</span><span class="sxs-lookup"><span data-stu-id="0b08c-127">On those platforms, color fonts are rendered as regular monochromatic fonts.</span></span>

## <a name="why-use-color-fonts"></a><span data-ttu-id="0b08c-128">Perché usare i tipi di carattere colore?</span><span class="sxs-lookup"><span data-stu-id="0b08c-128">Why use color fonts?</span></span>

<span data-ttu-id="0b08c-129">Storicamente, i progettisti e gli sviluppatori hanno usato diverse tecniche per ottenere testo multicolore.</span><span class="sxs-lookup"><span data-stu-id="0b08c-129">Historically, designers and developers have used a variety of techniques to achieve multicolored text.</span></span> <span data-ttu-id="0b08c-130">Ad esempio, i siti web usano spesso immagini raster anziché testo per visualizzare intestazioni avanzate.</span><span class="sxs-lookup"><span data-stu-id="0b08c-130">For example, websites often use raster images instead of text in order to display rich headers.</span></span> <span data-ttu-id="0b08c-131">Questo approccio consente la flessibilità artistica, ma la grafica raster non è scalabile correttamente per tutte le dimensioni di visualizzazione, né fornisce le stesse funzionalità di accessibilità del testo reale.</span><span class="sxs-lookup"><span data-stu-id="0b08c-131">This approach enables artistic flexibility, but raster graphics do not scale well to all display sizes, nor do they provide the same accessibility features as real text.</span></span> <span data-ttu-id="0b08c-132">Un'altra tecnica comune è quella di sovrapporre più tipi di carattere monocromatici con diversi colori dei tipi di carattere, ma questo in genere richiede un codice di layout aggiuntivo da gestire.</span><span class="sxs-lookup"><span data-stu-id="0b08c-132">Another common technique is to overlay multiple monochromatic fonts in different font colors, but this typically requires extra layout code to manage.</span></span>

<span data-ttu-id="0b08c-133">I tipi di carattere colore offrono un modo per ottenere questi effetti visivi con tutta la semplicità e la funzionalità dei tipi di carattere normali.</span><span class="sxs-lookup"><span data-stu-id="0b08c-133">Color fonts offer a way to achieve these visual effects with all the simplicity and functionality of regular fonts.</span></span> <span data-ttu-id="0b08c-134">Il testo di cui è stato eseguito il rendering in un tipo di carattere è identico a quello di un altro testo: può essere copiato e incollato, può essere analizzato dagli strumenti di accessibilità e così via.</span><span class="sxs-lookup"><span data-stu-id="0b08c-134">Text rendered in a color font is the same as other text: it can be copied and pasted, it can be parsed by accessibility tools, and so forth.</span></span>

## <a name="what-kinds-of-color-fonts-does-windows-support"></a><span data-ttu-id="0b08c-135">Quali tipi di tipi di carattere colori supporta Windows?</span><span class="sxs-lookup"><span data-stu-id="0b08c-135">What kinds of color fonts does Windows support?</span></span>

<span data-ttu-id="0b08c-136">La [specifica OpenType](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) definisce diversi modi per incorporare le informazioni sui colori in un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="0b08c-136">The [OpenType specification](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) defines several ways to embed color information in a font.</span></span> <span data-ttu-id="0b08c-137">A partire dall'aggiornamento dell'anniversario di Windows 10, DirectWrite e Direct2D (e i Framework Windows basati su di essi) supportano tutti questi approcci.</span><span class="sxs-lookup"><span data-stu-id="0b08c-137">Starting in Windows 10 Anniversary Update, DirectWrite and Direct2D (and the Windows frameworks built on them) support all of these approaches.</span></span> <span data-ttu-id="0b08c-138">Sono riepilogati nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="0b08c-138">They are summarized in the table below:</span></span>



| <span data-ttu-id="0b08c-139">Tecnica</span><span class="sxs-lookup"><span data-stu-id="0b08c-139">Technique</span></span>                                                                                                                        | <span data-ttu-id="0b08c-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b08c-140">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b08c-141">[Colr](/typography/opentype/spec/colr) / Tabelle [CPAL](/typography/opentype/spec/cpal)</span><span class="sxs-lookup"><span data-stu-id="0b08c-141">[COLR](/typography/opentype/spec/colr)/[CPAL](/typography/opentype/spec/cpal) tables</span></span> | <span data-ttu-id="0b08c-142">USA i livelli di vettori colorati, le cui forme sono definite nello stesso modo dei profili di glifo a colore singolo.</span><span class="sxs-lookup"><span data-stu-id="0b08c-142">Uses layers of colored vectors, whose shapes are defined in the same way as single-color glyph outlines.</span></span> <span data-ttu-id="0b08c-143">**Nota:** Supportato a partire da Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="0b08c-143">**Note:** Supported starting in Windows 8.1.</span></span> <br/>                                                                                                                                                 |
| <span data-ttu-id="0b08c-144">Tabella [SVG](/typography/opentype/spec/svg)</span><span class="sxs-lookup"><span data-stu-id="0b08c-144">[SVG](/typography/opentype/spec/svg) table</span></span>                                                                 | <span data-ttu-id="0b08c-145">Usa immagini vettoriali create nel formato di grafica vettoriale scalabile.</span><span class="sxs-lookup"><span data-stu-id="0b08c-145">Uses vector images authored in the Scalable Vector Graphics format.</span></span> <span data-ttu-id="0b08c-146">**Nota:** A partire dall'aggiornamento dell'anniversario di Windows 10, DirectWrite supporta un subset della specifica SVG completa. Non tutto il contenuto SVG è garantito per il rendering in un tipo di carattere SVG OpenType.</span><span class="sxs-lookup"><span data-stu-id="0b08c-146">**Note:** As of Windows 10 Anniversary Update, DirectWrite supports a subset of the full SVG spec. Not all SVG content is guaranteed to render in an OpenType SVG font.</span></span> <span data-ttu-id="0b08c-147">Per altri dettagli, vedere [supporto per SVG](../direct2d/svg-support.md) .</span><span class="sxs-lookup"><span data-stu-id="0b08c-147">See [SVG Support](../direct2d/svg-support.md) for more details.</span></span> <br/> |
| <span data-ttu-id="0b08c-148">[CBDT](/typography/opentype/spec/cbdt) / Tabelle [cblC](/typography/opentype/spec/cblc)</span><span class="sxs-lookup"><span data-stu-id="0b08c-148">[CBDT](/typography/opentype/spec/cbdt)/[CBLC](/typography/opentype/spec/cblc) tables</span></span> | <span data-ttu-id="0b08c-149">Usa immagini bitmap a colori incorporati.</span><span class="sxs-lookup"><span data-stu-id="0b08c-149">Uses embedded color bitmap images.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="0b08c-150">tabella [sbix](/typography/opentype/spec/sbix)</span><span class="sxs-lookup"><span data-stu-id="0b08c-150">[sbix](/typography/opentype/spec/sbix) table</span></span>                                                               | <span data-ttu-id="0b08c-151">Usa immagini bitmap a colori incorporati.</span><span class="sxs-lookup"><span data-stu-id="0b08c-151">Uses embedded color bitmap images.</span></span>                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a><span data-ttu-id="0b08c-152">Uso di tipi di carattere colori</span><span class="sxs-lookup"><span data-stu-id="0b08c-152">Using color fonts</span></span>

<span data-ttu-id="0b08c-153">Dal punto di vista dell'utente, i tipi di carattere dei colori sono solo tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="0b08c-153">From the user s perspective, color fonts are  just fonts .</span></span> <span data-ttu-id="0b08c-154">Ad esempio, possono in genere essere installate e disinstallate dal sistema in modo analogo ai tipi di carattere monocromatici e vengono visualizzate come testo normale e selezionabile.</span><span class="sxs-lookup"><span data-stu-id="0b08c-154">For example, they can usually be installed and uninstalled from the system in the same way as monochromatic fonts, and they are rendered as regular, selectable text.</span></span>

<span data-ttu-id="0b08c-155">Dal punto di vista dello sviluppatore, i tipi di carattere colorati vengono in genere utilizzati allo stesso modo dei tipi di carattere monocromatici.</span><span class="sxs-lookup"><span data-stu-id="0b08c-155">From the developer s perspective too, color fonts are usually used the same way as monochromatic fonts.</span></span> <span data-ttu-id="0b08c-156">Nei framework XAML e Microsoft Edge è possibile applicare uno stile al testo con i tipi di carattere di colore nello stesso modo dei tipi di carattere normali e, per impostazione predefinita, il rendering del testo verrà eseguito in colore.</span><span class="sxs-lookup"><span data-stu-id="0b08c-156">In the XAML and Microsoft Edge frameworks, you can style your text with color fonts the same way as regular fonts, and by default your text will be rendered in color.</span></span> <span data-ttu-id="0b08c-157">Tuttavia, se l'app chiama direttamente le API Direct2D (o API Win2D) per eseguire il rendering del testo, deve richiedere esplicitamente il rendering del tipo di carattere colore.</span><span class="sxs-lookup"><span data-stu-id="0b08c-157">However, if your app directly calls Direct2D APIs (or Win2D APIs) to render text, it must explicitly request color font rendering.</span></span>

### <a name="using-color-fonts-in-a-xaml-app"></a><span data-ttu-id="0b08c-158">Uso di tipi di carattere a colori in un'app XAML</span><span class="sxs-lookup"><span data-stu-id="0b08c-158">Using color fonts in a XAML app</span></span>

<span data-ttu-id="0b08c-159">Gli elementi di testo della piattaforma XAML, ad esempio [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [RichEditBox](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)e [FontIcon](/uwp/api/windows.ui.xaml.controls.fonticon), supportano i tipi di carattere colore per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0b08c-159">The XAML platform s text elements (such as [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [RichEditBox](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396), and [FontIcon](/uwp/api/windows.ui.xaml.controls.fonticon)) support color fonts by default.</span></span> <span data-ttu-id="0b08c-160">È sufficiente applicare uno stile al testo con un tipo di carattere colore. verrà eseguito il rendering di qualsiasi glifo di colore a colori.</span><span class="sxs-lookup"><span data-stu-id="0b08c-160">Simply style your text with a color font, and any color glyphs will be rendered in color.</span></span> <span data-ttu-id="0b08c-161">L'esempio di codice seguente illustra un modo per applicare uno stile a un TextBlock con un tipo di carattere di colore incluso nell'app.</span><span class="sxs-lookup"><span data-stu-id="0b08c-161">The following code example shows one way to style a TextBlock with a color font packaged with your app.</span></span> <span data-ttu-id="0b08c-162">La stessa tecnica si applica ai normali tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="0b08c-162">The same technique applies to regular fonts.</span></span>


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



<span data-ttu-id="0b08c-163">Se non si vuole mai che l'elemento di testo XAML esegua il rendering del testo multicolore, impostare la relativa proprietà [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) su false.</span><span class="sxs-lookup"><span data-stu-id="0b08c-163">If you never want your XAML text element to render multicolored text, set its [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) property to false.</span></span>

### <a name="using-color-fonts-in-microsoft-edge"></a><span data-ttu-id="0b08c-164">Uso di tipi di carattere a colori in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0b08c-164">Using color fonts in Microsoft Edge</span></span>

<span data-ttu-id="0b08c-165">Per impostazione predefinita, il rendering dei tipi di carattere di colore viene eseguito in siti Web e app Web in esecuzione su Microsoft Edge, incluso il controllo [WebView](/uwp/api/windows.ui.xaml.controls.webview) XAML.</span><span class="sxs-lookup"><span data-stu-id="0b08c-165">Color fonts are rendered by default in websites and web apps running on Microsoft Edge, including the XAML [WebView](/uwp/api/windows.ui.xaml.controls.webview) control.</span></span> <span data-ttu-id="0b08c-166">È sufficiente usare HTML e CSS per applicare uno stile al testo con un tipo di carattere colore e qualsiasi glifo di colore verrà sottoposto a rendering in colore.</span><span class="sxs-lookup"><span data-stu-id="0b08c-166">Simply use HTML and CSS to style your text with a color font, and any color glyphs will be rendered in color.</span></span>

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a><span data-ttu-id="0b08c-167">Uso dei tipi di carattere colori con DirectWrite e Direct2D</span><span class="sxs-lookup"><span data-stu-id="0b08c-167">Using color fonts with DirectWrite and Direct2D</span></span>

<span data-ttu-id="0b08c-168">L'app può usare i metodi di disegno del testo di livello superiore di Direct2D ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) e [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) oppure può usare tecniche di basso livello per disegnare direttamente le esecuzioni di glifi.</span><span class="sxs-lookup"><span data-stu-id="0b08c-168">Your app can use Direct2D s higher-level text drawing methods ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) and [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) or it can use lower-level techniques to draw glyph runs directly.</span></span> <span data-ttu-id="0b08c-169">In entrambi i casi, l'app richiede modifiche al codice per gestire correttamente i glifi dei colori.</span><span class="sxs-lookup"><span data-stu-id="0b08c-169">In either case, your app requires code changes in order to handle color glyphs correctly.</span></span> <span data-ttu-id="0b08c-170">Se l'app usa le API **DrawText** e **DrawTextLayout** di Direct2D, si noti che per impostazione predefinita non viene eseguito il rendering delle icone dei colori.</span><span class="sxs-lookup"><span data-stu-id="0b08c-170">If your app uses Direct2D s **DrawText** and **DrawTextLayout** APIs, note that these do not render color glyphs by default.</span></span> <span data-ttu-id="0b08c-171">In questo modo si evitano modifiche impreviste del comportamento nelle app per il rendering del testo progettate prima del supporto dei tipi di carattere colori.</span><span class="sxs-lookup"><span data-stu-id="0b08c-171">This is to avoid unexpected behavior changes in text rendering apps that were designed prior to color font support.</span></span>

<span data-ttu-id="0b08c-172">Per acconsentire esplicitamente al rendering del glifo dei colori, passare le opzioni di testo di disegno d2d1 Abilita il flag opzioni del [**\_ tipo di \_ \_ \_ \_ \_ carattere colore**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) al metodo di disegno.</span><span class="sxs-lookup"><span data-stu-id="0b08c-172">To opt in to color glyph rendering, pass the [**D2D1\_DRAW\_TEXT\_OPTIONS\_ENABLE\_COLOR\_FONT**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) options flag to the drawing method.</span></span> <span data-ttu-id="0b08c-173">Nell'esempio di codice seguente viene illustrato come chiamare il metodo DrawText di Direct2D per eseguire il rendering di una stringa in un tipo di carattere di colore:</span><span class="sxs-lookup"><span data-stu-id="0b08c-173">The following code example shows how to call Direct2D s DrawText method to render a string in a color font:</span></span>


```C++
// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_defaultFillBrush. 
m_deviceContext->DrawText( 
    m_string->Data(), 
    m_string->Length(), 
    m_textFormat.Get(), 
    m_layoutRect, 
    m_defaultFillBrush.Get(), 
    D2D1_DRAW_TEXT_OPTIONS_ENABLE_COLOR_FONT 
    );  
    
```



<span data-ttu-id="0b08c-174">Se l'app usa le API di livello inferiore per gestire le esecuzioni di glifi direttamente, continuerà a funzionare in presenza di tipi di carattere di colore, ma non sarà in grado di creare icone dei colori senza logica aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="0b08c-174">If your app uses lower-level APIs to handle glyph runs directly, then it will continue to function in the presence of color fonts, but it will not be able to draw color glyphs without additional logic.</span></span>

<span data-ttu-id="0b08c-175">Per gestire correttamente i glifi dei colori, l'app deve:</span><span class="sxs-lookup"><span data-stu-id="0b08c-175">To correctly handle color glyphs, your app should:</span></span>

1.  <span data-ttu-id="0b08c-176">Passare le informazioni di esecuzione del glifo a [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), insieme a un parametro dei [**formati di \_ \_ immagine \_ del glifo DWrite**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) che indica i tipi di glifo del colore che l'app è preparata a gestire.</span><span class="sxs-lookup"><span data-stu-id="0b08c-176">Pass the glyph run information to [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), along with a [**DWRITE\_GLYPH\_IMAGE\_FORMATS**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) parameter that indicates which type(s) of color glyph the app is prepared to handle.</span></span> <span data-ttu-id="0b08c-177">Se sono presenti glifi di colore (in base al tipo di carattere e ai **\_ formati di \_ immagine \_ del glifo DWrite** richiesti), DirectWrite suddividerà il glifo primario in esecuzioni di glifi di colore individuali a cui è possibile accedere tramite l'oggetto [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) restituito nel passaggio 4.</span><span class="sxs-lookup"><span data-stu-id="0b08c-177">If any color glyphs are present (based on the font and the requested **DWRITE\_GLYPH\_IMAGE\_FORMATS**), then DirectWrite will split the primary glyph run into individual  color glyph runs  which can be accessed through the returned [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) object in Step 4.</span></span>
2.  <span data-ttu-id="0b08c-178">Controllare HRESULT restituito da [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) per determinare se sono state rilevate esecuzioni di glifi di colore.</span><span class="sxs-lookup"><span data-stu-id="0b08c-178">Check the HRESULT returned by [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) to determine whether any color glyph runs were detected.</span></span> <span data-ttu-id="0b08c-179">Un valore **HRESULT** di **DWrite \_ E \_ nocolor** indica che non è stata eseguita alcuna icona dei colori applicabile.</span><span class="sxs-lookup"><span data-stu-id="0b08c-179">An **HRESULT** of **DWRITE\_E\_NOCOLOR** indicates no applicable color glyph run.</span></span>
3.  <span data-ttu-id="0b08c-180">Se [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) non ha segnalato l'esecuzione di un glifo dei colori (restituendo **DWrite \_ E \_ nocolor**), l'intera esecuzione del glifo viene considerata come monocromatico e l'app deve essere disegnato come desiderato (ad esempio, usando [**ID2D1DeviceContext::D rawglyphrun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).</span><span class="sxs-lookup"><span data-stu-id="0b08c-180">If [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) reported no color glyph runs (by returning **DWRITE\_E\_NOCOLOR**), then the whole glyph run is treated as monochromatic, and your app should draw it as desired (for example, using [**ID2D1DeviceContext::DrawGlyphRun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).</span></span>
4.  <span data-ttu-id="0b08c-181">Se [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) segnala la presenza delle esecuzioni del glifo dei colori, l'app deve ignorare l'esecuzione del glifo principale e usare invece le esecuzioni del glifo dei colori restituite da TranslateColorGlyphRun.</span><span class="sxs-lookup"><span data-stu-id="0b08c-181">If [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) does report the presence of color glyph runs, then your app should ignore the primary glyph run and instead use the color glyph run(s) returned by TranslateColorGlyphRun.</span></span> <span data-ttu-id="0b08c-182">A tale scopo, eseguire l'iterazione dell'oggetto [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) restituito, recuperare ogni icona del colore e disegnarla come appropriato per il formato dell'immagine del glifo. ad esempio, è possibile usare [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) e [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) per disegnare rispettivamente i glifi di bitmap di colore e i glifi svg.</span><span class="sxs-lookup"><span data-stu-id="0b08c-182">To do so, iterate through the returned [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) object, retrieving each color glyph run and drawing it as appropriate for its glyph image format (for example, you can use [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) and [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) to draw color bitmap glyphs and SVG glyphs, respectively).</span></span>

<span data-ttu-id="0b08c-183">Nell'esempio di codice seguente viene illustrata la struttura generale di questa procedura:</span><span class="sxs-lookup"><span data-stu-id="0b08c-183">The following code example shows the general structure of this procedure:</span></span>


```C++
// An example code snippet demonstrating how to use TranslateColorGlyphRun 
// to handle different kinds of color glyphs. This code does not make any 
// actual drawing calls. 
HRESULT DrawGlyphRun( 
    FLOAT baselineOriginX, 
    FLOAT baselineOriginY, 
    DWRITE_MEASURING_MODE measuringMode, 
    _In_ DWRITE_GLYPH_RUN const* glyphRun, 
    _In_ DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription, 
) 
{ 
    // Specify the color glyph formats your app supports. In this example, 
    // the app requests only glyphs defined with PNG or SVG. 
    DWRITE_GLYPH_IMAGE_FORMATS requestedFormats = 
        DWRITE_GLYPH_IMAGE_FORMATS_PNG | DWRITE_GLYPH_IMAGE_FORMATS_SVG; 

    ComPtr<IDWriteColorGlyphRunEnumerator1> glyphRunEnumerator; 
    HRESULT hr = m_dwriteFactory->TranslateColorGlyphRun( 
        D2D1::Point2F(baselineOriginX, baselineOriginY), 
        glyphRun, 
        glyphRunDescription, 
        requestedFormats, // the glyph formats supported by this renderer 
        measuringMode, 
        nullptr, 
        0, 
        &glyphRunEnumerator // on return, may contain color glyph runs 
        ); 

    if (hr == DWRITE_E_NOCOLOR) 
    { 
        // The glyph run has no color glyphs. Draw it as a monochrome glyph 
        // run, for example using the DrawGlyphRun method on a Direct2D 
        // device context. 
    } 
    else 
    { 
        // The glyph run has one or more color glyphs. 
        DX::ThrowIfFailed(hr); 

        // Iterate through the color glyph runs and draw them. 
        for (;;) 
        { 
            BOOL haveRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->MoveNext(&haveRun)); 
            if (!haveRun) 
            { 
                break; 
            } 

            // Retrieve the color glyph run. 
            DWRITE_COLOR_GLYPH_RUN1 const* colorRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->GetCurrentRun(&colorRun)); 

            // Draw the color glyph run depending on its format. 
            switch (colorRun->glyphImageFormat) 
            { 
            case DWRITE_GLYPH_IMAGE_FORMATS_PNG: 
                // Draw the PNG glyph, for example with 
                // ID2D1DeviceContext4::DrawColorBitmapGlyphRun. 
                break; 

            case DWRITE_GLYPH_IMAGE_FORMATS_SVG: 
                // Draw the SVG glyph, for example with 
                // ID2D1DeviceContext4::DrawSvgGlyphRun. 
                break; 

                // ...etc. 
            } 
        } 
    } 

    return hr; 
} 
```



### <a name="using-color-fonts-with-win2d"></a><span data-ttu-id="0b08c-184">Uso dei tipi di carattere colore con Win2D</span><span class="sxs-lookup"><span data-stu-id="0b08c-184">Using color fonts with Win2D</span></span>

<span data-ttu-id="0b08c-185">Analogamente a Direct2D, le API di disegno del testo di Win2D non eseguono il rendering delle icone dei colori per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0b08c-185">Similar to Direct2D, Win2D s text drawing APIs do not render color glyphs by default.</span></span> <span data-ttu-id="0b08c-186">Per acconsentire esplicitamente al rendering del glifo dei colori, impostare il flag delle opzioni [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) nell'oggetto formato testo che l'app passa al metodo di disegno del testo.</span><span class="sxs-lookup"><span data-stu-id="0b08c-186">To opt in to color glyph rendering, set the [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) options flag in the text format object your app passes to the text drawing method.</span></span> <span data-ttu-id="0b08c-187">Nell'esempio di codice seguente viene illustrato come eseguire il rendering di una stringa in un tipo di carattere colore utilizzando Win2D:</span><span class="sxs-lookup"><span data-stu-id="0b08c-187">The following code example shows how to render a string in a color font using Win2D:</span></span>


```C++
// The text format that will be used to draw the text. (Declared elsewhere 
// and initialized elsewhere by the app to point to a color font.) 
CanvasTextFormat m_textFormat; 

// Set the EnableColorFont option. 
m_textFormat.Options = CanvasDrawTextOptions.EnableColorFont; 

// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_color. 
args.DrawingSession.DrawText( 
    m_string, 
    m_point, 
    m_color, 
    m_textFormat 
    ); 
```

## <a name="related-topics"></a><span data-ttu-id="0b08c-188">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0b08c-188">Related topics</span></span>

[<span data-ttu-id="0b08c-189">Esempio di glifo colorato DirectWrite</span><span class="sxs-lookup"><span data-stu-id="0b08c-189">DirectWrite colored glyph sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[<span data-ttu-id="0b08c-190">**Interfaccia IDWriteFontFace4**</span><span class="sxs-lookup"><span data-stu-id="0b08c-190">**IDWriteFontFace4 interface**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[<span data-ttu-id="0b08c-191">**Metodo IDWriteFactory4:: TranslateColorGlyphRun**</span><span class="sxs-lookup"><span data-stu-id="0b08c-191">**IDWriteFactory4::TranslateColorGlyphRun method**</span></span>](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[<span data-ttu-id="0b08c-192">**ID2D1DeviceContext4::D Metodo rawText**</span><span class="sxs-lookup"><span data-stu-id="0b08c-192">**ID2D1DeviceContext4::DrawText method**</span></span>](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 


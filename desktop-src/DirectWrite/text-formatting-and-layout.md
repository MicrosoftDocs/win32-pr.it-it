---
title: Formattazione e layout del testo
description: DirectWrite fornisce due interfacce per la formattazione del testo IDWriteTextFormat e IDWriteTextLayout.
ms.assetid: a68963a6-e486-4881-8ad6-873173396fca
keywords:
- DirectWrite, formattazione del testo
- DirectWrite, layout
- Interfaccia DirectWrite,IDWriteTextFormat
- Interfaccia DirectWrite,IDWriteTextLayout
- Interfaccia IDWriteTextFormat
- Interfaccia IDWriteTextLayout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e5790742a3d3caf7f962a6b5e2b3111c626f28
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380755"
---
# <a name="text-formatting-and-layout"></a><span data-ttu-id="99002-109">Formattazione e layout del testo</span><span class="sxs-lookup"><span data-stu-id="99002-109">Text Formatting and Layout</span></span>

<span data-ttu-id="99002-110">[DirectWrite](direct-write-portal.md) offre due interfacce per la formattazione del testo: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)</span><span class="sxs-lookup"><span data-stu-id="99002-110">[DirectWrite](direct-write-portal.md) provides two interfaces for formatting text: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="99002-111">**IDWriteTextFormat** descrive solo il formato del testo e viene usato nei casi in cui un'intera stringa deve avere le stesse dimensioni del carattere, lo stesso stile, lo stesso spessore e così via.</span><span class="sxs-lookup"><span data-stu-id="99002-111">**IDWriteTextFormat** describes only the format for text and is used in cases when an entire string is to be the same font size, style, weight and so on.</span></span> <span data-ttu-id="99002-112">D'altra parte, **IDWriteTextLayout** incapsula sia una stringa di testo che la formattazione per gli intervalli specificati della stringa.</span><span class="sxs-lookup"><span data-stu-id="99002-112">On the other hand, **IDWriteTextLayout** encapsulates both a text string and the formatting for specified ranges of the string.</span></span> <span data-ttu-id="99002-113">Questo documento descrive ogni interfaccia e i relativi usi.</span><span class="sxs-lookup"><span data-stu-id="99002-113">This document describes each interface and their uses.</span></span> <span data-ttu-id="99002-114">Per altre informazioni sulla creazione e sui metodi di queste interfacce, vedere le pagine di riferimento [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)</span><span class="sxs-lookup"><span data-stu-id="99002-114">For more information about the creation and methods of these interfaces, see the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference pages.</span></span>

<span data-ttu-id="99002-115">Questo documento contiene le parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="99002-115">This document contains the following parts:</span></span>

-   [<span data-ttu-id="99002-116">IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="99002-116">IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
    -   [<span data-ttu-id="99002-117">Modifica di un oggetto IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="99002-117">Modifying an IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
-   [<span data-ttu-id="99002-118">IDWriteTextLayout</span><span class="sxs-lookup"><span data-stu-id="99002-118">IDWriteTextLayout</span></span>](#idwritetextlayout)
    -   [<span data-ttu-id="99002-119">Formattazione di un intervallo di testo</span><span class="sxs-lookup"><span data-stu-id="99002-119">Formatting a range of text</span></span>](#formatting-a-range-of-text)
    -   [<span data-ttu-id="99002-120">Opzioni di rendering</span><span class="sxs-lookup"><span data-stu-id="99002-120">Rendering Options</span></span>](#rendering-options)

## <a name="idwritetextformat"></a><span data-ttu-id="99002-121">IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="99002-121">IDWriteTextFormat</span></span>

<span data-ttu-id="99002-122">Un [**oggetto IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) viene usato per:</span><span class="sxs-lookup"><span data-stu-id="99002-122">An [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object is used to:</span></span>

-   <span data-ttu-id="99002-123">Descrivere il formato di un'intera stringa durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="99002-123">Describe the format for an entire string when rendering.</span></span> <span data-ttu-id="99002-124">Per eseguire il rendering di una stringa con più formati, usare un [**oggetto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)</span><span class="sxs-lookup"><span data-stu-id="99002-124">To render a string with multiple formats, use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>
-   <span data-ttu-id="99002-125">Specificare il formato di testo predefinito quando si crea un [**oggetto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)</span><span class="sxs-lookup"><span data-stu-id="99002-125">Specify the default text format when creating an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="99002-126">Per creare un [**oggetto IDWriteTextFormat,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) usare il metodo [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) e specificare la famiglia di caratteri, la raccolta di caratteri, lo spessore del carattere, le dimensioni del carattere (in DIP), il nome delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="99002-126">To create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object, you use the [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) method and specify the font family, font collection, font weight, font size (in DIPs), locale name.</span></span>

### <a name="modifying-an-idwritetextformat"></a><span data-ttu-id="99002-127">Modifica di un oggetto IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="99002-127">Modifying an IDWriteTextFormat</span></span>

<span data-ttu-id="99002-128">Dopo aver [**creato un'interfaccia IDWriteTextFormat,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) alcuni valori non possono essere modificati: la famiglia di caratteri, la raccolta, lo spessore e le dimensioni, nonché il nome delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="99002-128">Once an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface is created, some values cannot be changed: the font family, collection, weight, and size, as well the locale name.</span></span> <span data-ttu-id="99002-129">Per modificare questi valori, è necessario creare un nuovo **oggetto IDWriteTextFormat.**</span><span class="sxs-lookup"><span data-stu-id="99002-129">To change these values, a new **IDWriteTextFormat** object must be created.</span></span>

<span data-ttu-id="99002-130">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) consente di modificare le proprietà precedenti senza ricreare alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="99002-130">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) enables you to change the properties above without recreating anything.</span></span> <span data-ttu-id="99002-131">[**IDWriteTextFormat consente**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) di apportare modifiche al formato che si applicano all'intero testo, ad esempio l'allineamento del testo.</span><span class="sxs-lookup"><span data-stu-id="99002-131">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) enables you to make format changes that apply to the entire text, such as text alignment.</span></span> <span data-ttu-id="99002-132">Se si vuole applicare la formattazione a intervalli di caratteri specifici, è consigliabile usare **IDWriteTextLayout**.</span><span class="sxs-lookup"><span data-stu-id="99002-132">If you want to apply formatting to specific character ranges, you should do so by using a **IDWriteTextLayout**.</span></span>

<span data-ttu-id="99002-133">[**IDWriteTextFormat fornisce**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) metodi per impostare l'allineamento del testo, la direzione del flusso, la tabulazione incrementale, l'interlinea, l'allineamento del paragrafo, il trimming e il ritorno a capo automatico.</span><span class="sxs-lookup"><span data-stu-id="99002-133">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) provides methods to set the text alignment, flow direction, incremental tab stop, line spacing, paragraph alignment, trimming, and word wrapping.</span></span> <span data-ttu-id="99002-134">Queste proprietà possono essere modificate in qualsiasi momento dopo la creazione **dell'oggetto IDWriteTextFormat.**</span><span class="sxs-lookup"><span data-stu-id="99002-134">These properties can be changed at any time after the creation of the **IDWriteTextFormat** object.</span></span>

## <a name="idwritetextlayout"></a><span data-ttu-id="99002-135">IDWriteTextLayout</span><span class="sxs-lookup"><span data-stu-id="99002-135">IDWriteTextLayout</span></span>

<span data-ttu-id="99002-136">[**L'interfaccia IDWriteTextLayout,**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) a differenza [**di IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), rappresenta sia un blocco di testo che la formattazione associata.</span><span class="sxs-lookup"><span data-stu-id="99002-136">The [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface, unlike [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), represents both a block of text and the associated formatting.</span></span> <span data-ttu-id="99002-137">**IDWriteTextFormat rappresenta le** informazioni di formattazione iniziali.</span><span class="sxs-lookup"><span data-stu-id="99002-137">**IDWriteTextFormat** represents initial formatting information.</span></span> <span data-ttu-id="99002-138">L'esempio seguente illustra come creare un **oggetto IDWriteTextLayout** usando [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).</span><span class="sxs-lookup"><span data-stu-id="99002-138">The following example shows how to create an **IDWriteTextLayout** object using [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).</span></span>


```C++
// Create a text layout using the text format.
if (SUCCEEDED(hr))
{
    RECT rect;
    GetClientRect(hwnd_, &rect); 
    float width  = rect.right  / dpiScaleX_;
    float height = rect.bottom / dpiScaleY_;

    hr = pDWriteFactory_->CreateTextLayout(
        wszText_,      // The string to be laid out and formatted.
        cTextLength_,  // The length of the string.
        pTextFormat_,  // The text format to apply to the string (contains font information, etc).
        width,         // The width of the layout box.
        height,        // The height of the layout box.
        &pTextLayout_  // The IDWriteTextLayout interface pointer.
        );
}

```



<span data-ttu-id="99002-139">Il testo in un [**oggetto IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) non può essere modificato dopo la creazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="99002-139">The text in an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object cannot be changed once the object is created.</span></span> <span data-ttu-id="99002-140">Per modificare il testo, è necessario eliminare l'oggetto esistente e creare un nuovo **oggetto IDWriteTextLayout.**</span><span class="sxs-lookup"><span data-stu-id="99002-140">To change the text you must delete the existing object and create a new **IDWriteTextLayout** object.</span></span>

<span data-ttu-id="99002-141">È possibile usare [**idWriteTextLayout per**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) formattare intervalli di testo specificati.</span><span class="sxs-lookup"><span data-stu-id="99002-141">You can use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) to format specified ranges of text.</span></span> <span data-ttu-id="99002-142">**IDWriteTextLayout fornisce** anche metodi per modificare lo stile e lo spessore del carattere e aggiungere funzionalità del tipo di carattere OpenType e hit testing.</span><span class="sxs-lookup"><span data-stu-id="99002-142">**IDWriteTextLayout** also provides methods for changing font style and weight, and adding OpenType font features and hit testing.</span></span> <span data-ttu-id="99002-143">Per altre informazioni e un elenco completo dei metodi, vedere la pagina di riferimento [**di IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)</span><span class="sxs-lookup"><span data-stu-id="99002-143">For more information and a complete list of methods see the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference page.</span></span>

### <a name="formatting-a-range-of-text"></a><span data-ttu-id="99002-144">Formattazione di un intervallo di testo</span><span class="sxs-lookup"><span data-stu-id="99002-144">Formatting a range of text</span></span>

<span data-ttu-id="99002-145">[**IDWriteTextLayout fornisce**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) diversi metodi per formattare intervalli di testo.</span><span class="sxs-lookup"><span data-stu-id="99002-145">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) provides several methods to format ranges of text.</span></span> <span data-ttu-id="99002-146">Ognuno di questi metodi accetta una [**struttura DWRITE \_ TEXT \_ RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) come parametro per specificare la posizione iniziale del testo all'interno della stringa e la lunghezza dell'intervallo da formattare.</span><span class="sxs-lookup"><span data-stu-id="99002-146">Each of these methods takes a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) structure as a parameter to specify the starting text position within the string and the length of the range to format.</span></span> <span data-ttu-id="99002-147">Nell'esempio seguente viene illustrato come impostare lo spessore del carattere di un intervallo di testo su grassetto.</span><span class="sxs-lookup"><span data-stu-id="99002-147">The following example shows how to set the font weight of a range of text to bold.</span></span>


```C++
// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 5};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

```



### <a name="rendering-options"></a><span data-ttu-id="99002-148">Opzioni di rendering</span><span class="sxs-lookup"><span data-stu-id="99002-148">Rendering Options</span></span>

<span data-ttu-id="99002-149">Il rendering del testo con formattazione descritta solo da un oggetto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) può essere eseguito con [Direct2D,](../direct2d/direct2d-portal.md)tuttavia sono disponibili altre opzioni per il rendering di un [**oggetto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)</span><span class="sxs-lookup"><span data-stu-id="99002-149">Text with formatting described by only a [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object can be rendered with [Direct2D](../direct2d/direct2d-portal.md), however, there are a few more options for rendering an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="99002-150">È possibile eseguire il rendering della stringa descritta da un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usando i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="99002-150">The string described by an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object can be rendered using the methods below.</span></span>

1.  <span data-ttu-id="99002-151">[Eseguire il rendering con Direct2D.](rendering-by-using-direct2d.md)</span><span class="sxs-lookup"><span data-stu-id="99002-151">[Render using Direct2D](rendering-by-using-direct2d.md).</span></span>
2.  <span data-ttu-id="99002-152">[Eseguire il rendering usando un renderer di testo personalizzato.](how-to-implement-a-custom-text-renderer.md)</span><span class="sxs-lookup"><span data-stu-id="99002-152">[Render using a custom text renderer](how-to-implement-a-custom-text-renderer.md).</span></span>
3.  <span data-ttu-id="99002-153">[Eseguire il rendering su una superficie GDI.](render-to-a-gdi-surface.md)</span><span class="sxs-lookup"><span data-stu-id="99002-153">[Render to a GDI surface](render-to-a-gdi-surface.md).</span></span>

 

 

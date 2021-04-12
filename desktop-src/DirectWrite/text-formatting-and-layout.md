---
title: Formattazione e layout del testo
description: DirectWrite fornisce due interfacce per la formattazione di testo IDWriteTextFormat e IDWriteTextLayout.
ms.assetid: a68963a6-e486-4881-8ad6-873173396fca
keywords:
- DirectWrite, formattazione del testo
- DirectWrite, layout
- DirectWrite, interfaccia IDWriteTextFormat
- DirectWrite, interfaccia IDWriteTextLayout
- Interfaccia IDWriteTextFormat
- Interfaccia IDWriteTextLayout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30fcf884c15015af2645c32e217d3b4a6b433554
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104224002"
---
# <a name="text-formatting-and-layout"></a><span data-ttu-id="30c33-109">Formattazione e layout del testo</span><span class="sxs-lookup"><span data-stu-id="30c33-109">Text Formatting and Layout</span></span>

<span data-ttu-id="30c33-110">[DirectWrite](direct-write-portal.md) fornisce due interfacce per la formattazione del testo: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span><span class="sxs-lookup"><span data-stu-id="30c33-110">[DirectWrite](direct-write-portal.md) provides two interfaces for formatting text: [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout).</span></span> <span data-ttu-id="30c33-111">**IDWriteTextFormat** descrive solo il formato per il testo e viene usato nei casi in cui un'intera stringa deve avere le stesse dimensioni del carattere, stile, spessore e così via.</span><span class="sxs-lookup"><span data-stu-id="30c33-111">**IDWriteTextFormat** describes only the format for text and is used in cases when an entire string is to be the same font size, style, weight and so on.</span></span> <span data-ttu-id="30c33-112">D'altra parte, **IDWriteTextLayout** incapsula sia una stringa di testo che la formattazione per gli intervalli specificati della stringa.</span><span class="sxs-lookup"><span data-stu-id="30c33-112">On the other hand, **IDWriteTextLayout** encapsulates both a text string and the formatting for specified ranges of the string.</span></span> <span data-ttu-id="30c33-113">In questo documento vengono descritte le singole interfacce e i relativi utilizzi.</span><span class="sxs-lookup"><span data-stu-id="30c33-113">This document describes each interface and their uses.</span></span> <span data-ttu-id="30c33-114">Per ulteriori informazioni sulla creazione e sui metodi di queste interfacce, vedere le pagine di riferimento [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="30c33-114">For more information about the creation and methods of these interfaces, see the [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference pages.</span></span>

<span data-ttu-id="30c33-115">Questo documento contiene le parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="30c33-115">This document contains the following parts:</span></span>

-   [<span data-ttu-id="30c33-116">IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="30c33-116">IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
    -   [<span data-ttu-id="30c33-117">Modifica di un IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="30c33-117">Modifying an IDWriteTextFormat</span></span>](#modifying-an-idwritetextformat)
-   [<span data-ttu-id="30c33-118">IDWriteTextLayout</span><span class="sxs-lookup"><span data-stu-id="30c33-118">IDWriteTextLayout</span></span>](#idwritetextlayout)
    -   [<span data-ttu-id="30c33-119">Formattazione di un intervallo di testo</span><span class="sxs-lookup"><span data-stu-id="30c33-119">Formatting a range of text</span></span>](#formatting-a-range-of-text)
    -   [<span data-ttu-id="30c33-120">Opzioni di rendering</span><span class="sxs-lookup"><span data-stu-id="30c33-120">Rendering Options</span></span>](#rendering-options)

## <a name="idwritetextformat"></a><span data-ttu-id="30c33-121">IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="30c33-121">IDWriteTextFormat</span></span>

<span data-ttu-id="30c33-122">Un oggetto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) viene usato per:</span><span class="sxs-lookup"><span data-stu-id="30c33-122">An [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object is used to:</span></span>

-   <span data-ttu-id="30c33-123">Descrive il formato per un'intera stringa durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="30c33-123">Describe the format for an entire string when rendering.</span></span> <span data-ttu-id="30c33-124">Per eseguire il rendering di una stringa con più formati, usare un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="30c33-124">To render a string with multiple formats, use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>
-   <span data-ttu-id="30c33-125">Consente di specificare il formato di testo predefinito durante la creazione di un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="30c33-125">Specify the default text format when creating an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="30c33-126">Per creare un oggetto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , usare il metodo [**IDWriteFactory archiviata nei:: CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) e specificare la famiglia di caratteri, la raccolta di caratteri, il peso del carattere, le dimensioni del carattere (in DIP), il nome delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="30c33-126">To create an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object, you use the [**IDWriteFactory::CreateTextFormat**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat) method and specify the font family, font collection, font weight, font size (in DIPs), locale name.</span></span>

### <a name="modifying-an-idwritetextformat"></a><span data-ttu-id="30c33-127">Modifica di un IDWriteTextFormat</span><span class="sxs-lookup"><span data-stu-id="30c33-127">Modifying an IDWriteTextFormat</span></span>

<span data-ttu-id="30c33-128">Una volta creata un'interfaccia [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , alcuni valori non possono essere modificati: la famiglia di caratteri, la raccolta, il peso e le dimensioni, nonché il nome delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="30c33-128">Once an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) interface is created, some values cannot be changed: the font family, collection, weight, and size, as well the locale name.</span></span> <span data-ttu-id="30c33-129">Per modificare questi valori, è necessario creare un nuovo oggetto **IDWriteTextFormat** .</span><span class="sxs-lookup"><span data-stu-id="30c33-129">To change these values, a new **IDWriteTextFormat** object must be created.</span></span>

<span data-ttu-id="30c33-130">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) consente di modificare le proprietà precedenti senza ricreare l'elemento.</span><span class="sxs-lookup"><span data-stu-id="30c33-130">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) enables you to change the properties above without recreating anthing.</span></span> <span data-ttu-id="30c33-131">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) consente di apportare modifiche al formato applicabili all'intero testo, ad esempio l'allineamento del testo.</span><span class="sxs-lookup"><span data-stu-id="30c33-131">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) enables you to make format changes that apply to the entire text, such as text alignment.</span></span> <span data-ttu-id="30c33-132">Se si desidera applicare la formattazione a intervalli di caratteri specifici, è necessario utilizzare un **IDWriteTextLayout**.</span><span class="sxs-lookup"><span data-stu-id="30c33-132">If you want to apply formatting to specific character ranges, you should do so by using a **IDWriteTextLayout**.</span></span>

<span data-ttu-id="30c33-133">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) fornisce metodi per impostare l'allineamento del testo, la direzione del flusso, l'arresto della tabulazione incrementale, l'interlinea, l'allineamento del paragrafo, il taglio e il ritorno a capo delle parole</span><span class="sxs-lookup"><span data-stu-id="30c33-133">[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) provides methods to set the text alignment, flow direction, incremental tab stop, line spacing, paragraph alignment, trimming, and word wrapping.</span></span> <span data-ttu-id="30c33-134">Queste proprietà possono essere modificate in qualsiasi momento dopo la creazione dell'oggetto **IDWriteTextFormat** .</span><span class="sxs-lookup"><span data-stu-id="30c33-134">These properties can be changed at any time after the creation of the **IDWriteTextFormat** object.</span></span>

## <a name="idwritetextlayout"></a><span data-ttu-id="30c33-135">IDWriteTextLayout</span><span class="sxs-lookup"><span data-stu-id="30c33-135">IDWriteTextLayout</span></span>

<span data-ttu-id="30c33-136">L'interfaccia [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , a differenza di [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), rappresenta un blocco di testo e la formattazione associata.</span><span class="sxs-lookup"><span data-stu-id="30c33-136">The [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) interface, unlike [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), represents both a block of text and the associated formatting.</span></span> <span data-ttu-id="30c33-137">**IDWriteTextFormat** rappresenta le informazioni di formattazione iniziali.</span><span class="sxs-lookup"><span data-stu-id="30c33-137">**IDWriteTextFormat** represents initial formatting information.</span></span> <span data-ttu-id="30c33-138">Nell'esempio seguente viene illustrato come creare un oggetto **IDWriteTextLayout** usando [**IDWriteFactory archiviata nei:: CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).</span><span class="sxs-lookup"><span data-stu-id="30c33-138">The following example shows how to create an **IDWriteTextLayout** object using [**IDWriteFactory::CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout).</span></span>


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



<span data-ttu-id="30c33-139">Il testo in un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) non può essere modificato dopo la creazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="30c33-139">The text in an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object cannot be changed once the object is created.</span></span> <span data-ttu-id="30c33-140">Per modificare il testo, è necessario eliminare l'oggetto esistente e creare un nuovo oggetto **IDWriteTextLayout** .</span><span class="sxs-lookup"><span data-stu-id="30c33-140">To change the text you must delete the existing object and create a new **IDWriteTextLayout** object.</span></span>

<span data-ttu-id="30c33-141">È possibile usare un [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) per formattare gli intervalli di testo specificati.</span><span class="sxs-lookup"><span data-stu-id="30c33-141">You can use an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) to format specified ranges of text.</span></span> <span data-ttu-id="30c33-142">**IDWriteTextLayout** fornisce anche metodi per modificare lo stile e il peso del carattere e aggiungere le funzionalità del tipo di carattere OpenType e l'hit testing.</span><span class="sxs-lookup"><span data-stu-id="30c33-142">**IDWriteTextLayout** also provides methods for changing font style and weight, and adding OpenType font features and hit testing.</span></span> <span data-ttu-id="30c33-143">Per ulteriori informazioni e per un elenco completo dei metodi, vedere la pagina di riferimento di [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="30c33-143">For more information and a complete list of methods see the [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) reference page.</span></span>

### <a name="formatting-a-range-of-text"></a><span data-ttu-id="30c33-144">Formattazione di un intervallo di testo</span><span class="sxs-lookup"><span data-stu-id="30c33-144">Formatting a range of text</span></span>

<span data-ttu-id="30c33-145">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) fornisce diversi metodi per formattare gli intervalli di testo.</span><span class="sxs-lookup"><span data-stu-id="30c33-145">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) provides several methods to format ranges of text.</span></span> <span data-ttu-id="30c33-146">Ognuno di questi metodi accetta la struttura di un [**\_ \_ intervallo di testo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) come parametro per specificare la posizione iniziale del testo all'interno della stringa e la lunghezza dell'intervallo da formattare.</span><span class="sxs-lookup"><span data-stu-id="30c33-146">Each of these methods takes a [**DWRITE\_TEXT\_RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) structure as a parameter to specify the starting text position within the string and the length of the range to format.</span></span> <span data-ttu-id="30c33-147">Nell'esempio seguente viene illustrato come impostare lo spessore del carattere di un intervallo di testo in grassetto.</span><span class="sxs-lookup"><span data-stu-id="30c33-147">The following example shows how to set the font weight of a range of text to bold.</span></span>


```C++
// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 5};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}

```



### <a name="rendering-options"></a><span data-ttu-id="30c33-148">Opzioni di rendering</span><span class="sxs-lookup"><span data-stu-id="30c33-148">Rendering Options</span></span>

<span data-ttu-id="30c33-149">Il rendering del testo con la formattazione descritta solo da un oggetto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) può essere eseguito con [Direct2D](../direct2d/direct2d-portal.md), tuttavia sono disponibili altre opzioni per il rendering di un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="30c33-149">Text with formatting described by only a [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object can be rendered with [Direct2D](../direct2d/direct2d-portal.md), however, there are a few more options for rendering an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="30c33-150">La stringa descritta da un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) può essere sottoposta a rendering usando i metodi riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="30c33-150">The string described by an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object can be rendered using the methods below.</span></span>

1.  <span data-ttu-id="30c33-151">[Eseguire il rendering tramite Direct2D](rendering-by-using-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="30c33-151">[Render using Direct2D](rendering-by-using-direct2d.md).</span></span>
2.  <span data-ttu-id="30c33-152">[Eseguire il rendering usando un renderer di testo personalizzato](how-to-implement-a-custom-text-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="30c33-152">[Render using a custom text renderer](how-to-implement-a-custom-text-renderer.md).</span></span>
3.  <span data-ttu-id="30c33-153">[Eseguire il rendering in una superficie GDI](render-to-a-gdi-surface.md).</span><span class="sxs-lookup"><span data-stu-id="30c33-153">[Render to a GDI surface](render-to-a-gdi-surface.md).</span></span>

 

 
---
title: Interoperabilità con GDI
description: DirectWrite fornisce un percorso di migrazione da e alcune interoperabilità con il modello del tipo di carattere di GDI, oltre a interfacce per il rendering del testo in una bitmap che può essere disegnata in una finestra.
ms.assetid: fb73e07b-60fb-4726-bd5b-c14d61ace186
keywords:
- DirectWrite, interoperatività GDI
- DirectWrite, interoperabilità
- interoperabilità
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41c7c99e6bfac0aabddd4a1568b64cd425ccb25b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046786"
---
# <a name="interoperating-with-gdi"></a><span data-ttu-id="ac501-108">Interoperabilità con GDI</span><span class="sxs-lookup"><span data-stu-id="ac501-108">Interoperating with GDI</span></span>

<span data-ttu-id="ac501-109">[DirectWrite](direct-write-portal.md) fornisce un percorso di migrazione da e alcune interoperabilità con il modello del tipo di carattere di GDI, oltre a interfacce per il rendering del testo in una bitmap che può essere disegnata in una finestra.</span><span class="sxs-lookup"><span data-stu-id="ac501-109">[DirectWrite](direct-write-portal.md) provides a migration path from, and some interoperability with, GDI's font model, as well as interfaces for rendering text to a bitmap that can then be drawn on a window.</span></span>

<span data-ttu-id="ac501-110">Questa panoramica include le parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ac501-110">This overview contains the following parts:</span></span>

-   [<span data-ttu-id="ac501-111">Introduzione</span><span class="sxs-lookup"><span data-stu-id="ac501-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="ac501-112">Parte 1: IDWriteGdiInterop</span><span class="sxs-lookup"><span data-stu-id="ac501-112">Part 1: IDWriteGdiInterop</span></span>](#part-1-idwritegdiinterop)
-   [<span data-ttu-id="ac501-113">Parte 2: oggetti Font</span><span class="sxs-lookup"><span data-stu-id="ac501-113">Part 2: Font Objects</span></span>](#part-2-font-objects)
-   [<span data-ttu-id="ac501-114">Parte 3: rendering</span><span class="sxs-lookup"><span data-stu-id="ac501-114">Part 3: Rendering</span></span>](#part-3-rendering)

## <a name="introduction"></a><span data-ttu-id="ac501-115">Introduzione</span><span class="sxs-lookup"><span data-stu-id="ac501-115">Introduction</span></span>

<span data-ttu-id="ac501-116">[DirectWrite](direct-write-portal.md) fornisce metodi per la conversione tra la struttura LOGFONT di GDI e le interfacce del tipo di carattere DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="ac501-116">[DirectWrite](direct-write-portal.md) provides methods for converting between GDI's LOGFONT structure and DirectWrite font interfaces.</span></span> <span data-ttu-id="ac501-117">In questo modo è possibile utilizzare GDI per alcune o tutte le enumerazioni e la selezione dei tipi di carattere, sfruttando al contempo le funzionalità e le prestazioni migliorate di DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="ac501-117">This allows you to use GDI for some or all of the font enumeration and selection, while taking advantage of the improved functionality and performance of DirectWrite.</span></span> <span data-ttu-id="ac501-118">DirectWrite dispone inoltre di interfacce per il rendering in una bitmap se si desidera visualizzare il testo su una superficie GDI.</span><span class="sxs-lookup"><span data-stu-id="ac501-118">DirectWrite also has interfaces for rendering to a bitmap if you want to display text on a GDI surface.</span></span>

## <a name="part-1-idwritegdiinterop"></a><span data-ttu-id="ac501-119">Parte 1: IDWriteGdiInterop</span><span class="sxs-lookup"><span data-stu-id="ac501-119">Part 1: IDWriteGdiInterop</span></span>

<span data-ttu-id="ac501-120">L'interfaccia [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) viene utilizzata per eseguire la conversione tra le strutture del tipo di carattere GDI e le interfacce del tipo di carattere [DirectWrite](direct-write-portal.md) e per creare un oggetto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) .</span><span class="sxs-lookup"><span data-stu-id="ac501-120">The [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) interface is used to convert between GDI font structures and [DirectWrite](direct-write-portal.md) font interfaces, and also to create an [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object.</span></span> <span data-ttu-id="ac501-121">Ottenere un oggetto **IDWriteGdiInterop** usando il metodo [**IDWriteFactory archiviata nei:: GetGdiInterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) , come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="ac501-121">Get an **IDWriteGdiInterop** object by using the [**IDWriteFactory::GetGdiInterop**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getgdiinterop) method, as shown in the following code.</span></span>


```C++
// Create a GDI interop interface.
if (SUCCEEDED(hr))
{
    hr = g_pDWriteFactory->GetGdiInterop(&g_pGdiInterop);
}
```



## <a name="part-2-font-objects"></a><span data-ttu-id="ac501-122">Parte 2: oggetti Font</span><span class="sxs-lookup"><span data-stu-id="ac501-122">Part 2: Font Objects</span></span>

<span data-ttu-id="ac501-123">GDI utilizza la struttura LOGFONT per archiviare le informazioni sul tipo di carattere e lo stile del testo.</span><span class="sxs-lookup"><span data-stu-id="ac501-123">GDI uses the LOGFONT structure to store information about the font and style of text.</span></span> <span data-ttu-id="ac501-124">Il metodo [**IDWriteGdiInterop:: CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) converte una struttura LOGFONT in un oggetto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) , come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="ac501-124">The [**IDWriteGdiInterop::CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont) method will convert a LOGFONT structure to an [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) object, as seen in the following code.</span></span>


```C++
// Convert to a DirectWrite font.
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateFontFromLOGFONT(&lf, &pFont);
}
```



<span data-ttu-id="ac501-125">Tuttavia, [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) non incapsula tutte le informazioni che un LOGFONT esegue.</span><span class="sxs-lookup"><span data-stu-id="ac501-125">However, [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) does not encapsulate all of the same information that a LOGFONT does.</span></span> <span data-ttu-id="ac501-126">Una struttura LOGFONT contiene le dimensioni del carattere, il peso, lo stile, la sottolineatura, l'attacco, il nome del tipo di carattere e altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ac501-126">A LOGFONT structure contains the font size, weight, style, underline, strikeout, font face name, and some other information.</span></span> <span data-ttu-id="ac501-127">Gli oggetti **IDWriteFont** contengono informazioni su un tipo di carattere e il relativo spessore e stile, ma non le dimensioni del carattere, la sottolineatura e così via.</span><span class="sxs-lookup"><span data-stu-id="ac501-127">**IDWriteFont** objects contain information about a font and its weight and style, but not the font size, underline, and so on.</span></span> <span data-ttu-id="ac501-128">Con [DirectWrite](direct-write-portal.md), gli elementi di informazioni di formattazione, ad esempio, sono incapsulati da un oggetto [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) o, per intervalli specifici di testo, un oggetto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .</span><span class="sxs-lookup"><span data-stu-id="ac501-128">With [DirectWrite](direct-write-portal.md), formatting information elements such as these are encapsulated by an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object or, for specific ranges of text, an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="ac501-129">È possibile eseguire la conversione di un [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) in un LOGFONT usando [**IDWriteGdiInterop:: ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).</span><span class="sxs-lookup"><span data-stu-id="ac501-129">You do have the option to convert a [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) to a LOGFONT by using the [**IDWriteGdiInterop::ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont).</span></span>

## <a name="part-3-rendering"></a><span data-ttu-id="ac501-130">Parte 3: rendering</span><span class="sxs-lookup"><span data-stu-id="ac501-130">Part 3: Rendering</span></span>

<span data-ttu-id="ac501-131">Per eseguire il rendering del testo DirectWrite in una superficie GDI si utilizza un renderer di testo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ac501-131">To render DirectWrite text to a GDI surface you use a custom text renderer.</span></span> <span data-ttu-id="ac501-132">Vedere l'argomento [eseguire il rendering in una superficie GDI](render-to-a-gdi-surface.md) .</span><span class="sxs-lookup"><span data-stu-id="ac501-132">See the [Render to a GDI Surface](render-to-a-gdi-surface.md) topic.</span></span>

 

 
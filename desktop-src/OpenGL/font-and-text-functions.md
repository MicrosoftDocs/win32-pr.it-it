---
title: Funzioni per il tipo di carattere e il testo (OpenGL)
description: Le funzioni seguenti possono essere utilizzate per gestire i tipi di carattere e il testo.
ms.assetid: 42e16967-1eeb-4d37-bbd6-33c473eb2757
keywords:
- Funzioni WGL, testo
- Funzioni WGL, carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e205549346cccc2c44b7670db91530cfbc24017d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400128"
---
# <a name="font-and-text-functions-opengl"></a><span data-ttu-id="6b02f-105">Funzioni per il tipo di carattere e il testo (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="6b02f-105">Font and Text Functions (OpenGL)</span></span>

<span data-ttu-id="6b02f-106">Le funzioni seguenti possono essere utilizzate per gestire i tipi di carattere e il testo.</span><span class="sxs-lookup"><span data-stu-id="6b02f-106">The following functions can be used to manage fonts and text.</span></span>



| <span data-ttu-id="6b02f-107">Funzione Windows</span><span class="sxs-lookup"><span data-stu-id="6b02f-107">Windows Function</span></span>                                 | <span data-ttu-id="6b02f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b02f-108">Description</span></span>                                                                                                                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b02f-109">**wglUseFontBitmaps**</span><span class="sxs-lookup"><span data-stu-id="6b02f-109">**wglUseFontBitmaps**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)   | <span data-ttu-id="6b02f-110">Crea un set di elenchi di visualizzazione bitmap di caratteri.</span><span class="sxs-lookup"><span data-stu-id="6b02f-110">Creates a set of character bitmap display lists.</span></span> <span data-ttu-id="6b02f-111">I caratteri provengono dal tipo di carattere corrente del contesto di dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="6b02f-111">Characters come from a specified device context's current font.</span></span> <span data-ttu-id="6b02f-112">I caratteri vengono specificati come esecuzione consecutiva all'interno del set di glifi del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="6b02f-112">Characters are specified as a consecutive run within the font's glyph set.</span></span>                                      |
| [<span data-ttu-id="6b02f-113">**wglUseFontOutlines**</span><span class="sxs-lookup"><span data-stu-id="6b02f-113">**wglUseFontOutlines**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) | <span data-ttu-id="6b02f-114">Crea un set di elenchi di visualizzazione, in base ai glifi del tipo di carattere del contorno attualmente selezionato di un contesto di dispositivo, da utilizzare con il contesto di rendering corrente.</span><span class="sxs-lookup"><span data-stu-id="6b02f-114">Creates a set of display lists, based on the glyphs of the currently selected outline font of a device context, for use with the current rendering context.</span></span> <span data-ttu-id="6b02f-115">Gli elenchi di visualizzazione vengono utilizzati per creare caratteri 3D di tipi di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="6b02f-115">The display lists are used to draw 3-D characters of TrueType fonts.</span></span> |



 

<span data-ttu-id="6b02f-116">Le funzioni **wglUseFontBitmaps** e **wglUseFontOutlines** accettano un handle per un contesto di dispositivo e usano il tipo di carattere corrente del contesto di dispositivo come origine per le bitmap.</span><span class="sxs-lookup"><span data-stu-id="6b02f-116">The **wglUseFontBitmaps** and **wglUseFontOutlines** functions take a handle to a device context, and use that device context's current font as a source for the bitmaps.</span></span> <span data-ttu-id="6b02f-117">È pertanto necessario impostare il tipo di carattere del contesto di dispositivo e le proprietà del tipo di carattere prima di chiamare **wglUseFontBitmaps** o **wglUseFontOutlines**.</span><span class="sxs-lookup"><span data-stu-id="6b02f-117">It is therefore necessary to set the device context's font and the font's properties before calling **wglUseFontBitmaps** or **wglUseFontOutlines**.</span></span>

<span data-ttu-id="6b02f-118">Le funzioni [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) e [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) accettano anche un parametro che trasforma il primo glifo del tipo di carattere in un elenco di visualizzazione bitmap e un parametro che specifica il numero di glifi da trasformare negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="6b02f-118">The [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) and [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) functions also take a parameter that turns the first glyph in the font into a bitmap display list, and a parameter that specifies how many glyphs to turn into display lists.</span></span> <span data-ttu-id="6b02f-119">La funzione crea quindi gli elenchi di visualizzazione per l'esecuzione consecutiva specificata di glifi.</span><span class="sxs-lookup"><span data-stu-id="6b02f-119">The function then creates display lists for the specified consecutive run of glyphs.</span></span> <span data-ttu-id="6b02f-120">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="6b02f-120">For example:</span></span>

-   <span data-ttu-id="6b02f-121">Per creare un set di elenchi di visualizzazione bitmap 224 per tutti i glifi del set di caratteri di Windows, impostare questi due parametri rispettivamente su 32 e 224.</span><span class="sxs-lookup"><span data-stu-id="6b02f-121">To create a set of 224 bitmap display lists for all of the Windows character set glyphs, set these two parameters to 32 and 224, respectively.</span></span>
-   <span data-ttu-id="6b02f-122">Per creare un set di elenchi di visualizzazione bitmap 256 per tutte le icone del set di caratteri OEM, impostare questi due parametri rispettivamente su 0 e 256.</span><span class="sxs-lookup"><span data-stu-id="6b02f-122">To create a set of 256 bitmap display lists for all of the OEM character set glyphs, set these two parameters to 0 and 256, respectively.</span></span>
-   <span data-ttu-id="6b02f-123">Per creare un elenco di visualizzazione bitmap singolo per qualsiasi glifo del set di caratteri singolo, impostare il secondo di questi parametri su 1.</span><span class="sxs-lookup"><span data-stu-id="6b02f-123">To create a single bitmap display list for any single character set glyph, set the second of these parameters to 1.</span></span>

<span data-ttu-id="6b02f-124">Le funzioni **wglUseFontBitmaps** e **wglUseFontOutlines** rappresentano un glifo null in un tipo di carattere con un elenco di visualizzazione vuoto.</span><span class="sxs-lookup"><span data-stu-id="6b02f-124">The **wglUseFontBitmaps** and **wglUseFontOutlines** functions represent a null glyph in a font with an empty display list.</span></span>

<span data-ttu-id="6b02f-125">Gli elenchi di visualizzazione creati da una chiamata a **wglUseFontBitmaps** o **wglUseFontOutlines** vengono numerati automaticamente consecutivamente.</span><span class="sxs-lookup"><span data-stu-id="6b02f-125">The display lists created by a call to **wglUseFontBitmaps** or **wglUseFontOutlines** are automatically numbered consecutively.</span></span>

<span data-ttu-id="6b02f-126">Dopo aver chiamato la funzione [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) o [**WglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) , chiamare [**glCallLists**](glcalllists.md) per creare una stringa di caratteri.</span><span class="sxs-lookup"><span data-stu-id="6b02f-126">After calling the [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) or [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) function, call [**glCallLists**](glcalllists.md) to draw a string of characters.</span></span> <span data-ttu-id="6b02f-127">Per il codice di esempio, vedere [disegno di testo in una finestra Double-Buffered OpenGL](drawing-text-in-a-double-buffered-opengl-window.md) .</span><span class="sxs-lookup"><span data-stu-id="6b02f-127">See [Drawing Text in a Double-Buffered OpenGL Window](drawing-text-in-a-double-buffered-opengl-window.md) for sample code.</span></span> <span data-ttu-id="6b02f-128">In questo contesto, **glCallLists** USA ogni carattere in una stringa come indice nella matrice di elenchi di visualizzazione numerati consecutivamente creati da **wglUseFontBitmaps** o **wglUseFontOutlines**.</span><span class="sxs-lookup"><span data-stu-id="6b02f-128">In this context, **glCallLists** uses each character in a string as an index into the array of consecutively numbered display lists created by **wglUseFontBitmaps** or **wglUseFontOutlines**.</span></span>

<span data-ttu-id="6b02f-129">Al termine della creazione del testo, chiamare la funzione [**glDeleteLists**](gldeletelists.md) per rilasciare il set contiguo di elenchi di visualizzazione creati da **wglUseFontBitmaps** e **wglUseFontOutlines**.</span><span class="sxs-lookup"><span data-stu-id="6b02f-129">When you finish drawing text, call the [**glDeleteLists**](gldeletelists.md) function to release the contiguous set of display lists created by **wglUseFontBitmaps** and **wglUseFontOutlines**.</span></span>

 

 





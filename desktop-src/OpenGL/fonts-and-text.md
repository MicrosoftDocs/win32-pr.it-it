---
title: Tipi di carattere e testo (OpenGL)
description: L'implementazione Microsoft di OpenGL in Windows supporta la grafica GDI in una finestra OpenGL con singolo buffer.
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- OpenGL per Windows, tipi di carattere
- OpenGL per Windows, testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fba4ffe996bd88a6285f615ddacb31e57fc311
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400127"
---
# <a name="fonts-and-text-opengl"></a><span data-ttu-id="5792e-105">Tipi di carattere e testo (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="5792e-105">Fonts and Text (OpenGL)</span></span>

<span data-ttu-id="5792e-106">L'implementazione Microsoft di OpenGL in Windows supporta la grafica GDI in una finestra OpenGL con singolo buffer.</span><span class="sxs-lookup"><span data-stu-id="5792e-106">Microsoft's implementation of OpenGL in Windows supports GDI graphics in a single-buffered OpenGL window.</span></span> <span data-ttu-id="5792e-107">Non supporta la grafica GDI in una finestra OpenGL con doppio buffer.</span><span class="sxs-lookup"><span data-stu-id="5792e-107">It does not support GDI graphics in a double-buffered OpenGL window.</span></span> <span data-ttu-id="5792e-108">Pertanto, è possibile chiamare solo le funzioni standard GDI font e Text per creare testo in una finestra OpenGL con buffer singolo; non è possibile chiamare queste funzioni per creare testo in una finestra OpenGL con doppio buffer.</span><span class="sxs-lookup"><span data-stu-id="5792e-108">Thus, you can call only the standard GDI font and text functions to draw text in a single-buffered OpenGL window; you cannot call those functions to draw text in a double-buffered OpenGL window.</span></span>

<span data-ttu-id="5792e-109">Esiste una soluzione alternativa per questa restrizione sul testo nelle finestre con doppio buffer: compila gli elenchi di visualizzazione OpenGL per le immagini bitmap di caratteri, quindi Esegui gli elenchi di visualizzazione per creare caratteri.</span><span class="sxs-lookup"><span data-stu-id="5792e-109">There is a workaround for this restriction on text in double-buffered windows: build OpenGL display lists for bitmap images of characters, and then execute those display lists to draw characters.</span></span> <span data-ttu-id="5792e-110">Questo processo prevede tre passaggi principali:</span><span class="sxs-lookup"><span data-stu-id="5792e-110">There are three main steps in this process:</span></span>

1.  <span data-ttu-id="5792e-111">Selezionare un tipo di carattere per un contesto di dispositivo, impostando le proprietà del tipo di carattere come desiderato.</span><span class="sxs-lookup"><span data-stu-id="5792e-111">Select a font for a device context, setting the font's properties as desired.</span></span>
2.  <span data-ttu-id="5792e-112">Creare un set di elenchi di visualizzazione bitmap basati sui glifi nel tipo di carattere del contesto di dispositivo, un elenco di visualizzazione per ogni glifo che l'applicazione trarrà.</span><span class="sxs-lookup"><span data-stu-id="5792e-112">Create a set of bitmap display lists based on the glyphs in the device context's font, one display list for each glyph that the application will draw.</span></span>
3.  <span data-ttu-id="5792e-113">Creare ogni glifo in una stringa usando gli elenchi di visualizzazione bitmap.</span><span class="sxs-lookup"><span data-stu-id="5792e-113">Draw each glyph in a string, using those bitmap display lists.</span></span>

<span data-ttu-id="5792e-114">Per creare gli elenchi di visualizzazione, chiamare le funzioni [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) e [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) .</span><span class="sxs-lookup"><span data-stu-id="5792e-114">To create the display lists, call the [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) and [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) functions.</span></span> <span data-ttu-id="5792e-115">Per creare caratteri in una stringa usando gli elenchi di visualizzazione, chiamare [**glCallLists**](glcalllists.md).</span><span class="sxs-lookup"><span data-stu-id="5792e-115">To draw characters in a string using those display lists, call [**glCallLists**](glcalllists.md).</span></span>

<span data-ttu-id="5792e-116">Per creare applicazioni facili da localizzare e che usano le risorse in modo sporadico, è necessario gestire con attenzione la creazione e l'archiviazione degli elenchi di visualizzazione delle immagini del glifo.</span><span class="sxs-lookup"><span data-stu-id="5792e-116">To create applications that are easy to localize and that use resources sparingly, the creation and storage of these glyph image display lists must be managed carefully.</span></span> <span data-ttu-id="5792e-117">Molti linguaggi, a differenza della lingua inglese, presentano alfabeti i cui codici di caratteri sono compresi in un set di valori relativamente grande.</span><span class="sxs-lookup"><span data-stu-id="5792e-117">Many languages, unlike English, have alphabets whose character codes range over a relatively large set of values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5792e-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5792e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5792e-119">Funzioni di tipo carattere e testo</span><span class="sxs-lookup"><span data-stu-id="5792e-119">Font and Text Functions</span></span>](font-and-text-functions.md)
</dt> </dl>

 

 





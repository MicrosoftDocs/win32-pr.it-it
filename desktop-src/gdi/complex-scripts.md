---
description: Sebbene le funzioni descritte nella precedente funzionino correttamente per molti linguaggi, potrebbero non occuparsi delle esigenze di alfabeti non latini.
ms.assetid: a60b50c8-13e8-4c61-989f-187bb67cf929
title: Script complessi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c149aa1d9a6f5caf78fec5227f25aa30146fc273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880326"
---
# <a name="complex-scripts"></a><span data-ttu-id="3e202-103">Script complessi</span><span class="sxs-lookup"><span data-stu-id="3e202-103">Complex Scripts</span></span>

<span data-ttu-id="3e202-104">Sebbene le funzioni descritte nella precedente funzionino correttamente per molti linguaggi, potrebbero non occuparsi delle esigenze di alfabeti non latini.</span><span class="sxs-lookup"><span data-stu-id="3e202-104">While the functions discussed in the preceding work well for many languages, they may not deal with the needs of complex scripts.</span></span> <span data-ttu-id="3e202-105">Gli *alfabeti non latini* sono linguaggi il cui modulo stampato non viene sottoposto a rendering in modo semplice.</span><span class="sxs-lookup"><span data-stu-id="3e202-105">*Complex scripts* are languages whose printed form is not rendered in a simple way.</span></span> <span data-ttu-id="3e202-106">Uno script complesso, ad esempio, può consentire il rendering bidirezionale, il Shaping contestuale dei glifi o la combinazione di caratteri.</span><span class="sxs-lookup"><span data-stu-id="3e202-106">For example, a complex script may allow bidirectional rendering, contextual shaping of glyphs, or combining characters.</span></span> <span data-ttu-id="3e202-107">A causa di questi requisiti speciali, il controllo dell'output di testo deve essere molto flessibile.</span><span class="sxs-lookup"><span data-stu-id="3e202-107">Due to these special requirements, the control of text output must be very flexible.</span></span>

<span data-ttu-id="3e202-108">Le funzioni che visualizzano [**testo text**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)out, [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)e [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) sono state estese per supportare script complessi.</span><span class="sxs-lookup"><span data-stu-id="3e202-108">Functions that display text [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext), and [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) have been extended to support complex scripts.</span></span> <span data-ttu-id="3e202-109">In generale, questo supporto è trasparente per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3e202-109">In general, this support is transparent to the application.</span></span> <span data-ttu-id="3e202-110">Tuttavia, le applicazioni devono salvare i caratteri in un buffer e visualizzare un'intera riga di testo in una sola volta, in modo che i moduli di definizione degli script complessi possano usare il contesto per riordinare e generare correttamente i glifi.</span><span class="sxs-lookup"><span data-stu-id="3e202-110">However, applications should save characters in a buffer and display a whole line of text at one time, so that the complex script shaping modules can use context to reorder and generate glyphs correctly.</span></span> <span data-ttu-id="3e202-111">Inoltre, poiché la larghezza di un glifo può variare in base al contesto, le applicazioni devono usare [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) per determinare la lunghezza della riga invece di usare la larghezza dei caratteri memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="3e202-111">In addition, because the width of a glyph can vary by context, applications should use [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) to determine line length rather than using cached character widths.</span></span>

<span data-ttu-id="3e202-112">Inoltre, le applicazioni complesse compatibili con gli script devono considerare l'aggiunta del supporto per l'ordine di lettura da destra a sinistra e l'allineamento a destra per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3e202-112">In addition, complex script-aware applications should consider adding support for right-to-left reading order and right alignment to their applications.</span></span> <span data-ttu-id="3e202-113">È possibile alternare l'ordine di lettura o l'allineamento tra Left e Right con il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="3e202-113">You can toggle the reading order or alignment between left and right with the following code:</span></span>


```C++
// Save lAlign (this example uses static variables) 
static LONG lAlign = TA_LEFT;

// When user toggles alignment (assuming TA_CENTER is not supported). 

lAlign = TA_RIGHT;

// When the user toggles reading order. 

lAlign = TA_RTLREADING;

// Before calling ExtTextOut, for example, when processing WM_PAINT  

SetTextAlign (hDc, lAlign);
```



<span data-ttu-id="3e202-114">Per impostare entrambi gli attributi contemporaneamente, eseguire l'istruzione seguente e quindi chiamare [**setTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) e [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), come illustrato in precedenza:</span><span class="sxs-lookup"><span data-stu-id="3e202-114">To toggle both attributes at once, execute the following statement and then call [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) and [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), as shown previously:</span></span>


```C++
lAlign = TA_RIGHT^TA_RTLREADING;  //pre-inline !
```



<span data-ttu-id="3e202-115">È anche possibile elaborare script complessi con Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="3e202-115">You can also process complex scripts with Uniscribe.</span></span> <span data-ttu-id="3e202-116">Uniscribe è un set di funzioni che consentono un elevato livello di controllo per gli script complessi.</span><span class="sxs-lookup"><span data-stu-id="3e202-116">Uniscribe is a set of functions that allow a fine degree of control for complex scripts.</span></span> <span data-ttu-id="3e202-117">Per altre informazioni, vedere [Uniscribe](../intl/uniscribe.md) ed [elaborazione di script complessi](../intl/processing-complex-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="3e202-117">For more information, see [Uniscribe](../intl/uniscribe.md) and [Processing Complex Scripts](../intl/processing-complex-scripts.md).</span></span>

 

 

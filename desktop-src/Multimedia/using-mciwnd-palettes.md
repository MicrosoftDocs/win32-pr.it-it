---
title: Uso di tavolozze MCIWnd
description: Uso di tavolozze MCIWnd
ms.assetid: 2b99ca57-f321-4286-8ebf-ae3344d8d2c9
keywords:
- MCIWndGetPalette (macro)
- MCIWndSetPalette (macro)
- MCIWndRealize (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970e0e33c9dd03c7f1133576f371b713f7174df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963051"
---
# <a name="using-mciwnd-palettes"></a><span data-ttu-id="3c8bc-106">Uso di tavolozze MCIWnd</span><span class="sxs-lookup"><span data-stu-id="3c8bc-106">Using MCIWnd Palettes</span></span>

<span data-ttu-id="3c8bc-107">La riproduzione di clip video con una profondità di colore a 8 bit (capacità di 256 colori) richiede una tavolozza per definire i colori utilizzati.</span><span class="sxs-lookup"><span data-stu-id="3c8bc-107">Playing video clips with 8-bit color depth (256-color capacity) requires a palette to define the colors being used.</span></span> <span data-ttu-id="3c8bc-108">In alcuni casi, la tavolozza inclusa in un clip video non è la tavolozza più appropriata da usare durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="3c8bc-108">Sometimes, the palette included with a video clip is not the most appropriate palette to use during playback.</span></span> <span data-ttu-id="3c8bc-109">In questo caso, MCIWnd offre tre modi per gestire le tavolozze per la riproduzione:</span><span class="sxs-lookup"><span data-stu-id="3c8bc-109">In this case, MCIWnd provides three ways to manage palettes for playback:</span></span>

-   <span data-ttu-id="3c8bc-110">Recuperare un handle per la tavolozza associata a una finestra MCIWnd usando la macro [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="3c8bc-110">Retrieve a handle to the palette associated with an MCIWnd window by using the [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) macro.</span></span> <span data-ttu-id="3c8bc-111">La tavolozza non è necessariamente associata esclusivamente alla finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="3c8bc-111">The palette is not necessarily associated exclusively with the MCIWnd window.</span></span> <span data-ttu-id="3c8bc-112">Altre applicazioni possono accedere e persino invalidare l'handle della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="3c8bc-112">Other applications can access, and even invalidate, the palette handle.</span></span> <span data-ttu-id="3c8bc-113">Di conseguenza, l'applicazione deve prevedere l'utilizzo globale della tavolozza e, al termine della tavolozza, non dovrebbe liberarlo.</span><span class="sxs-lookup"><span data-stu-id="3c8bc-113">Consequently, your application should anticipate the global use of the palette and, when finished with the palette, should not free it.</span></span>
-   <span data-ttu-id="3c8bc-114">Specificare una nuova tavolozza da usare con il clip video associato a una finestra MCIWnd usando la macro [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) .</span><span class="sxs-lookup"><span data-stu-id="3c8bc-114">Specify a new palette to use with the video clip associated with an MCIWnd window by using the [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) macro.</span></span>
-   <span data-ttu-id="3c8bc-115">Realizzare la tavolozza associata a una finestra MCIWnd nella tavolozza di sistema usando la macro [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) .</span><span class="sxs-lookup"><span data-stu-id="3c8bc-115">Realize the palette associated with an MCIWnd window to the system palette by using the [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) macro.</span></span> <span data-ttu-id="3c8bc-116">Questa macro chiama la funzione [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) con la tavolozza associata alla finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="3c8bc-116">This macro calls the [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) function with the palette associated with the MCIWnd window.</span></span> <span data-ttu-id="3c8bc-117">Se i gestori di messaggi dell'applicazione [**per \_ WM PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) e [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) chiamano solo **RealizePalette** o **MCIWndRealize**, è necessario inviare tali messaggi a MCIWnd se non vengono gestiti da soli.</span><span class="sxs-lookup"><span data-stu-id="3c8bc-117">If your application message handlers for [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) call only **RealizePalette** or **MCIWndRealize**, you must forward these messages to MCIWnd if you do not handle them yourself.</span></span>

> [!Note]  
> <span data-ttu-id="3c8bc-118">Quando un clip video con profondità di colore a 8 bit viene caricato nella finestra MCIWnd, la tavolozza inclusa con tale clip sostituisce la tavolozza associata alla finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="3c8bc-118">When a video clip with 8-bit color depth is loaded into the MCIWnd window, the palette included with that clip replaces the palette associated with the MCIWnd window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3c8bc-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c8bc-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c8bc-120">Miglioramenti della riproduzione</span><span class="sxs-lookup"><span data-stu-id="3c8bc-120">Playback Enhancements</span></span>](playback-enhancements.md)
</dt> </dl>

 

 
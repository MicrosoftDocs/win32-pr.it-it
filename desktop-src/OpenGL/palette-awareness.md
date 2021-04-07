---
title: Riconoscimento della tavolozza
description: È necessario che l'applicazione risponda ai \_ messaggi WM PALETTECHANGED, WM \_ QUERYNEWPALETTE e WM \_ Activate per essere consapevoli e utilizzare le tavolozze. Progettare l'applicazione per selezionare e realizzare le tavolozze in risposta a questi messaggi.
ms.assetid: 0670e929-dfdb-44d2-bda2-c532d1739d8e
keywords:
- OpenGL per Windows, riconoscimento della tavolozza
- compatibilità della tavolozza OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ceab4c27f63c12977d072f84e789d1800b6557
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872902"
---
# <a name="palette-awareness"></a><span data-ttu-id="f3230-106">Riconoscimento della tavolozza</span><span class="sxs-lookup"><span data-stu-id="f3230-106">Palette Awareness</span></span>

<span data-ttu-id="f3230-107">È necessario che l'applicazione risponda ai messaggi [WM \_ PALETTECHANGED](/windows/desktop/gdi/wm-palettechanged), [WM \_ QUERYNEWPALETTE](/windows/desktop/gdi/wm-querynewpalette)e [WM \_ Activate](../inputdev/wm-activate.md) per essere consapevoli e utilizzare le tavolozze.</span><span class="sxs-lookup"><span data-stu-id="f3230-107">Your application must respond to the [WM\_PALETTECHANGED](/windows/desktop/gdi/wm-palettechanged), [WM\_QUERYNEWPALETTE](/windows/desktop/gdi/wm-querynewpalette), and [WM\_ACTIVATE](../inputdev/wm-activate.md) messages to be aware of and use palettes.</span></span> <span data-ttu-id="f3230-108">Progettare l'applicazione per selezionare e realizzare le tavolozze in risposta a questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="f3230-108">Design your application to select and realize palettes in response to these messages.</span></span>

<span data-ttu-id="f3230-109">Per ulteriori informazioni sulle tavolozze e sulla consapevolezza della tavolozza, vedere gli articoli "riconoscimento della tavolozza" e "gestione tavolozze: come e perché" nella libreria di sviluppo Microsoft per sviluppatori Microsoft Compact Disks.</span><span class="sxs-lookup"><span data-stu-id="f3230-109">For more information on palettes and palette awareness, see the articles "Palette Awareness," and "The Palette Manager: How and Why" on the Microsoft Developer Network Development Library compact discs.</span></span>

 

 
---
title: Formati pixel
description: Formati pixel
ms.assetid: 2e179340-c487-4b72-a22e-078b800af11d
keywords:
- OpenGL per Windows, pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16f9f78edc0cf935fb602de8d88792091588ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298889"
---
# <a name="pixel-formats"></a><span data-ttu-id="487fd-104">Formati pixel</span><span class="sxs-lookup"><span data-stu-id="487fd-104">Pixel Formats</span></span>

<span data-ttu-id="487fd-105">Un *formato pixel* specifica diverse proprietà di una superficie di disegno OpenGL.</span><span class="sxs-lookup"><span data-stu-id="487fd-105">A *pixel format* specifies several properties of an OpenGL drawing surface.</span></span> <span data-ttu-id="487fd-106">Di seguito sono riportate alcune delle proprietà specificate da un formato pixel:</span><span class="sxs-lookup"><span data-stu-id="487fd-106">Some of the properties specified by a pixel format are:</span></span>

-   <span data-ttu-id="487fd-107">Indica se il buffer pixel è a buffer singolo o doppio.</span><span class="sxs-lookup"><span data-stu-id="487fd-107">Whether the pixel buffer is single- or double-buffered.</span></span>
-   <span data-ttu-id="487fd-108">Indica se i dati pixel sono in formato RGBA o di indice colore.</span><span class="sxs-lookup"><span data-stu-id="487fd-108">Whether the pixel data is in RGBA or color-index form.</span></span>
-   <span data-ttu-id="487fd-109">Numero di bit usati per archiviare i dati di colore.</span><span class="sxs-lookup"><span data-stu-id="487fd-109">The number of bits used to store color data.</span></span>
-   <span data-ttu-id="487fd-110">Numero di bit utilizzati per il buffer di profondità (asse z).</span><span class="sxs-lookup"><span data-stu-id="487fd-110">The number of bits used for the depth (z-axis) buffer.</span></span>
-   <span data-ttu-id="487fd-111">Numero di bit utilizzati per il buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="487fd-111">The number of bits used for the stencil buffer.</span></span>
-   <span data-ttu-id="487fd-112">Numero di piani sovrapposti e sottoposti a sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="487fd-112">The number of overlay and underlay planes.</span></span>
-   <span data-ttu-id="487fd-113">Diverse maschere di visibilità.</span><span class="sxs-lookup"><span data-stu-id="487fd-113">Various visibility masks.</span></span>

<span data-ttu-id="487fd-114">L'implementazione Microsoft di OpenGL per Windows usa la struttura dei dati [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) per trasferire i dati in formato pixel.</span><span class="sxs-lookup"><span data-stu-id="487fd-114">Microsoft's implementation of OpenGL for Windows uses the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure to convey pixel format data.</span></span> <span data-ttu-id="487fd-115">I membri della struttura specificano le proprietà precedenti e altre ancora.</span><span class="sxs-lookup"><span data-stu-id="487fd-115">The structure's members specify the preceding properties and several others.</span></span>

<span data-ttu-id="487fd-116">Un determinato contesto di dispositivo può supportare diversi formati pixel.</span><span class="sxs-lookup"><span data-stu-id="487fd-116">A given device context can support several pixel formats.</span></span> <span data-ttu-id="487fd-117">Windows identifica i formati pixel supportati da un contesto di dispositivo con valori di indice consecutivi in base uno (1, 2, 3, 4 e così via).</span><span class="sxs-lookup"><span data-stu-id="487fd-117">Windows identifies the pixel formats that a device context supports with consecutive one-based index values (1, 2, 3, 4, and so on).</span></span> <span data-ttu-id="487fd-118">Un contesto di dispositivo può avere un solo formato pixel corrente, scelto dal set di formati pixel supportati.</span><span class="sxs-lookup"><span data-stu-id="487fd-118">A device context can have just one current pixel format, chosen from the set of pixel formats it supports.</span></span>

<span data-ttu-id="487fd-119">Ogni finestra ha il proprio formato pixel corrente in OpenGL in Windows.</span><span class="sxs-lookup"><span data-stu-id="487fd-119">Each window has its own current pixel format in OpenGL in Windows.</span></span> <span data-ttu-id="487fd-120">Ciò significa, ad esempio, che un'applicazione può visualizzare contemporaneamente RGBA e le finestre OpenGL con indicizzazione dei colori, o finestre OpenGL con buffer singolo e doppio.</span><span class="sxs-lookup"><span data-stu-id="487fd-120">This means, for example, that an application can simultaneously display RGBA and color-index OpenGL windows, or single- and double-buffered OpenGL windows.</span></span> <span data-ttu-id="487fd-121">Questa funzionalità di formato pixel per finestra è limitata alle finestre OpenGL.</span><span class="sxs-lookup"><span data-stu-id="487fd-121">This per-window pixel format capability is limited to OpenGL windows.</span></span>

<span data-ttu-id="487fd-122">In genere si ottiene un contesto di dispositivo, si imposta il formato pixel del contesto di dispositivo e quindi si crea un contesto di rendering OpenGL adatto per tale dispositivo.</span><span class="sxs-lookup"><span data-stu-id="487fd-122">Typically, you obtain a device context, set the device context's pixel format, and then create an OpenGL rendering context suitable for that device.</span></span>

> [!Note]  
> <span data-ttu-id="487fd-123">È possibile impostare il formato pixel prima di creare un contesto di rendering perché il contesto di rendering eredita il formato pixel del contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="487fd-123">You set the pixel format before creating a rendering context because the rendering context inherits the device context's pixel format.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="487fd-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="487fd-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="487fd-125">Funzioni in formato pixel</span><span class="sxs-lookup"><span data-stu-id="487fd-125">Pixel Format Functions</span></span>](pixel-format-functions.md)
</dt> </dl>

 

 





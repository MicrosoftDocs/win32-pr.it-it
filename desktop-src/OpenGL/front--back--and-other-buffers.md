---
title: Front, back e altri buffer
description: OpenGL archivia e modifica i dati pixel in un framebuffer.
ms.assetid: 4af6a5e4-cc62-49e5-a4d5-e54b1348e8fe
keywords:
- OpenGL per Windows, buffer
- framebuffer OpenGL
- buffer dei colori OpenGL
- buffer di profondità OpenGL
- buffer di accumulo OpenGL
- buffer di stencil OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea487b73af356853bee2054db292cdfe740bd16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396250"
---
# <a name="front-back-and-other-buffers"></a><span data-ttu-id="2c14e-109">Front, back e altri buffer</span><span class="sxs-lookup"><span data-stu-id="2c14e-109">Front, Back, and Other Buffers</span></span>

<span data-ttu-id="2c14e-110">OpenGL archivia e modifica i dati pixel in un framebuffer.</span><span class="sxs-lookup"><span data-stu-id="2c14e-110">OpenGL stores and manipulates pixel data in a framebuffer.</span></span> <span data-ttu-id="2c14e-111">Il framebuffer è costituito da un set di buffer logici: i buffer di colore, profondità, accumulo e stencil.</span><span class="sxs-lookup"><span data-stu-id="2c14e-111">The framebuffer consists of a set of logical buffers: color, depth, accumulation, and stencil buffers.</span></span> <span data-ttu-id="2c14e-112">Il buffer dei colori è costituito da un set di buffer logici; Questo set può includere un front-left, un front-right, un back-left, un back-right e un certo numero di buffer ausiliari.</span><span class="sxs-lookup"><span data-stu-id="2c14e-112">The color buffer itself consists of a set of logical buffers; this set can include a front-left, a front-right, a back-left, a back-right, and some number of auxiliary buffers.</span></span> <span data-ttu-id="2c14e-113">Un particolare formato pixel o un'implementazione OpenGL non può fornire tutti questi buffer.</span><span class="sxs-lookup"><span data-stu-id="2c14e-113">A particular pixel format or OpenGL implementation may not supply all of these buffers.</span></span> <span data-ttu-id="2c14e-114">La versione corrente dell'implementazione di Microsoft OpenGL in Windows, ad esempio, non supporta le immagini stereoscopiche, quindi un formato pixel non può avere buffer di colore sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="2c14e-114">For example, the current version of Microsoft's implementation of OpenGL in Windows does not support stereoscopic images, so a pixel format cannot have left and right color buffers.</span></span> <span data-ttu-id="2c14e-115">Inoltre, la versione corrente non supporta i buffer ausiliari.</span><span class="sxs-lookup"><span data-stu-id="2c14e-115">In addition, the current version does not support auxiliary buffers.</span></span> <span data-ttu-id="2c14e-116">Per altre informazioni sui buffer OpenGL e sulle funzioni OpenGL che operano su di essi, vedere il *Manuale di riferimento per OpenGL* e la guida per *programmatori OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="2c14e-116">For more information on OpenGL buffers and the OpenGL functions that operate on them, see the *OpenGL Reference Manual* and the *OpenGL Programming Guide*.</span></span>

<span data-ttu-id="2c14e-117">L'implementazione Microsoft di OpenGL in Windows supporta il doppio buffering delle immagini.</span><span class="sxs-lookup"><span data-stu-id="2c14e-117">Microsoft's implementation of OpenGL in Windows supports double buffering of images.</span></span> <span data-ttu-id="2c14e-118">Si tratta di una tecnica in cui un'applicazione disegna i pixel in un buffer fuori schermo, quindi, quando l'immagine è pronta per la visualizzazione, copia il contenuto del buffer fuori schermo in un buffer a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="2c14e-118">This is a technique in which an application draws pixels to an off-screen buffer, and then, when that image is ready for display, copies the contents of the off-screen buffer to an on-screen buffer.</span></span> <span data-ttu-id="2c14e-119">Il doppio buffer consente di apportare modifiche alle immagini, che sono particolarmente importanti per le immagini animate.</span><span class="sxs-lookup"><span data-stu-id="2c14e-119">Double buffering enables smooth image changes, which are especially important for animated images.</span></span>

<span data-ttu-id="2c14e-120">Due buffer a colori sono disponibili per le applicazioni che usano il doppio buffer: un buffer anteriore e un buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="2c14e-120">Two color buffers are available to applications that use double buffering: a front buffer and a back buffer.</span></span> <span data-ttu-id="2c14e-121">Per impostazione predefinita, i comandi di disegno vengono indirizzati al buffer nascosto (il buffer fuori schermo), mentre il buffer anteriore viene visualizzato sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="2c14e-121">By default, drawing commands are directed to the back buffer (the off-screen buffer), while the front buffer is displayed on the screen.</span></span> <span data-ttu-id="2c14e-122">Quando il buffer fuori schermo è pronto per la visualizzazione, si chiama [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)e Windows copia il contenuto del buffer fuori schermo nel buffer sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="2c14e-122">When the off-screen buffer is ready for display, you call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers), and Windows copies the contents of the off-screen buffer to the on-screen buffer.</span></span>

<span data-ttu-id="2c14e-123">L'implementazione generica usa una bitmap indipendente dal dispositivo (DIB) come buffer nascosto e lo schermo viene visualizzato come buffer anteriore.</span><span class="sxs-lookup"><span data-stu-id="2c14e-123">The generic implementation uses a device-independent bitmap (DIB) as the back buffer and the screen display as the front buffer.</span></span> <span data-ttu-id="2c14e-124">I dispositivi hardware e i relativi driver possono utilizzare approcci diversi.</span><span class="sxs-lookup"><span data-stu-id="2c14e-124">Hardware devices and their drivers may use different approaches.</span></span>

<span data-ttu-id="2c14e-125">Il doppio buffer è una proprietà in formato pixel.</span><span class="sxs-lookup"><span data-stu-id="2c14e-125">Double buffering is a pixel-format property.</span></span> <span data-ttu-id="2c14e-126">Per richiedere il doppio buffering per un formato pixel, impostare il \_ flag PFD DOUBLEBUFFER nella struttura dei dati [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) in una chiamata a [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span><span class="sxs-lookup"><span data-stu-id="2c14e-126">To request double buffering for a pixel format, set the PFD\_DOUBLEBUFFER flag in the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure in a call to [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span></span>

<span data-ttu-id="2c14e-127">La funzione di base OpenGL, [**glDrawBuffer**](gldrawbuffer.md), seleziona i buffer per la scrittura e la cancellazione.</span><span class="sxs-lookup"><span data-stu-id="2c14e-127">The OpenGL core function, [**glDrawBuffer**](gldrawbuffer.md), selects buffers for writing and clearing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c14e-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2c14e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c14e-129">Funzioni buffer</span><span class="sxs-lookup"><span data-stu-id="2c14e-129">Buffer Functions</span></span>](buffer-functions.md)
</dt> </dl>

 

 





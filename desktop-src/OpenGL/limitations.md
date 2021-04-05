---
title: Limitazioni
description: Limitazioni
ms.assetid: 5f41620d-dde0-4e82-92f0-ada9d4acf127
keywords:
- OpenGL per Windows, limitazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478a139326f74c236ca0109fddbbc3d4ffb46e1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709724"
---
# <a name="limitations"></a><span data-ttu-id="3aa6e-104">Limitazioni</span><span class="sxs-lookup"><span data-stu-id="3aa6e-104">Limitations</span></span>

<span data-ttu-id="3aa6e-105">L'implementazione generica presenta le limitazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3aa6e-105">The generic implementation has the following limitations:</span></span>

-   <span data-ttu-id="3aa6e-106">Stampa.</span><span class="sxs-lookup"><span data-stu-id="3aa6e-106">Printing.</span></span>

    <span data-ttu-id="3aa6e-107">È possibile stampare un'immagine OpenGL direttamente in una stampante usando solo i metafile.</span><span class="sxs-lookup"><span data-stu-id="3aa6e-107">You can print an OpenGL image directly to a printer using metafiles only.</span></span> <span data-ttu-id="3aa6e-108">Per altre informazioni, vedere [stampa di un'immagine OpenGL](printing-an-opengl-image.md).</span><span class="sxs-lookup"><span data-stu-id="3aa6e-108">For more information, see [Printing an OpenGL Image](printing-an-opengl-image.md).</span></span>

-   <span data-ttu-id="3aa6e-109">Non è possibile combinare grafica OpenGL e GDI in una finestra con doppio buffer.</span><span class="sxs-lookup"><span data-stu-id="3aa6e-109">OpenGL and GDI graphics cannot be mixed in a double-buffered window.</span></span>

    <span data-ttu-id="3aa6e-110">Un'applicazione può creare direttamente grafica OpenGL e grafica GDI in una finestra con singolo buffer, ma non in una finestra con doppio buffer.</span><span class="sxs-lookup"><span data-stu-id="3aa6e-110">An application can directly draw both OpenGL graphics and GDI graphics into a single-buffered window, but not into a double-buffered window.</span></span>

-   <span data-ttu-id="3aa6e-111">Non sono disponibili tavolozze dei colori hardware per ogni finestra.</span><span class="sxs-lookup"><span data-stu-id="3aa6e-111">There are no per-window hardware color palettes.</span></span>

    <span data-ttu-id="3aa6e-112">Windows ha una singola tavolozza dei colori hardware del sistema, applicabile all'intero schermo.</span><span class="sxs-lookup"><span data-stu-id="3aa6e-112">Windows has a single system hardware color palette, which applies to the whole screen.</span></span> <span data-ttu-id="3aa6e-113">Una finestra OpenGL non può avere una propria tavolozza hardware, ma può avere una propria tavolozza logica.</span><span class="sxs-lookup"><span data-stu-id="3aa6e-113">An OpenGL window cannot have its own hardware palette, but can have its own logical palette.</span></span> <span data-ttu-id="3aa6e-114">A tale scopo, deve diventare un'applicazione in grado di riconoscere la tavolozza.</span><span class="sxs-lookup"><span data-stu-id="3aa6e-114">To do so, it must become a palette-aware application.</span></span> <span data-ttu-id="3aa6e-115">Per ulteriori informazioni, vedere [modalità colori OpenGL e gestione tavolozza di Windows](opengl-color-modes-and-windows-palette-management.md).</span><span class="sxs-lookup"><span data-stu-id="3aa6e-115">For more information, see [OpenGL Color Modes and Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).</span></span>

-   <span data-ttu-id="3aa6e-116">Non è disponibile alcun supporto diretto per gli appunti, DDE (Dynamic Data Exchange) o OLE.</span><span class="sxs-lookup"><span data-stu-id="3aa6e-116">There is no direct support for the Clipboard, dynamic data exchange (DDE), or OLE.</span></span>

    <span data-ttu-id="3aa6e-117">Una finestra con grafica OpenGL non supporta direttamente queste funzionalità di Windows.</span><span class="sxs-lookup"><span data-stu-id="3aa6e-117">A window with OpenGL graphics does not directly support these Windows capabilities.</span></span> <span data-ttu-id="3aa6e-118">Tuttavia, esistono soluzioni alternative per l'utilizzo degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="3aa6e-118">There are workarounds, however, for using the Clipboard.</span></span> <span data-ttu-id="3aa6e-119">Per altre informazioni, vedere [copia di un'immagine OpenGL negli Appunti](copying-an-opengl-image-to-the-clipboard.md).</span><span class="sxs-lookup"><span data-stu-id="3aa6e-119">For more information, see [Copying an OpenGL Image to the Clipboard](copying-an-opengl-image-to-the-clipboard.md).</span></span>

-   <span data-ttu-id="3aa6e-120">La libreria di classi di Inventory 2,0 C++ non è inclusa.</span><span class="sxs-lookup"><span data-stu-id="3aa6e-120">The Inventor 2.0 C++ class library is not included.</span></span>

    <span data-ttu-id="3aa6e-121">La libreria di classi Inventory basata su OpenGL fornisce costrutti di livello superiore per la programmazione di grafica 3D.</span><span class="sxs-lookup"><span data-stu-id="3aa6e-121">The Inventor class library, built on top of OpenGL, provides higher-level constructs for programming 3-D graphics.</span></span> <span data-ttu-id="3aa6e-122">Non è incluso nella versione corrente dell'implementazione di Microsoft OpenGL per Windows.</span><span class="sxs-lookup"><span data-stu-id="3aa6e-122">It is not included in the current version of Microsoft's implementation of OpenGL for Windows.</span></span>

-   <span data-ttu-id="3aa6e-123">Non è disponibile alcun supporto per le funzionalità di formato pixel seguenti: immagini stereoscopiche, alfa bitplane e buffer ausiliari.</span><span class="sxs-lookup"><span data-stu-id="3aa6e-123">There is no support for the following pixel format features: stereoscopic images, alpha bitplanes, and auxiliary buffers.</span></span>

    <span data-ttu-id="3aa6e-124">È tuttavia disponibile il supporto per diversi buffer ausiliari, tra cui il buffer dello stencil, il buffer di accumulo, il buffer nascosto (doppio buffer), il buffer del piano sottoposto a sovrapposizione e il buffer di profondità (asse z).</span><span class="sxs-lookup"><span data-stu-id="3aa6e-124">There is, however, support for several ancillary buffers including: stencil buffer, accumulation buffer, back buffer (double buffering), overlay and underlay plane buffer, and depth (z-axis) buffer.</span></span>

 

 





---
title: Stampa di un'immagine OpenGL
description: È possibile stampare le immagini OpenGL sottoposte a rendering nei metafile avanzati.
ms.assetid: 6099cbe2-82f9-46ec-a3ca-74486c111639
keywords:
- OpenGL per Windows, stampa
- stampa di immagini OpenGL OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca0c5260a084796915a7564f793f0e252b5228c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300335"
---
# <a name="printing-an-opengl-image"></a><span data-ttu-id="1a39b-105">Stampa di un'immagine OpenGL</span><span class="sxs-lookup"><span data-stu-id="1a39b-105">Printing an OpenGL Image</span></span>

<span data-ttu-id="1a39b-106">È possibile stampare le immagini OpenGL sottoposte a rendering nei metafile avanzati.</span><span class="sxs-lookup"><span data-stu-id="1a39b-106">You can print OpenGL images rendered in enhanced metafiles.</span></span> <span data-ttu-id="1a39b-107">Quando si esegue il rendering in un dispositivo di stampa (HDC), questo deve essere supportato da uno spooler del metafile.</span><span class="sxs-lookup"><span data-stu-id="1a39b-107">When you render to a printer device (HDC) it must be backed by a metafile spooler.</span></span> <span data-ttu-id="1a39b-108">OpenGL usa memoria per la profondità, il colore e altri buffer per archiviare l'output grafico in una stampante.</span><span class="sxs-lookup"><span data-stu-id="1a39b-108">OpenGL uses memory for depth, color, and other buffers to store graphics output to a printer.</span></span> <span data-ttu-id="1a39b-109">Poiché la risoluzione tipica della stampante richiede una quantità significativa di memoria per archiviare l'output della grafica, la stampa di un'immagine OpenGL potrebbe richiedere una quantità di memoria maggiore di quella disponibile nel sistema.</span><span class="sxs-lookup"><span data-stu-id="1a39b-109">Because typical printer resolution requires a significant amount of memory to store the graphics output, printing an OpenGL image might require more memory than is available in the system.</span></span> <span data-ttu-id="1a39b-110">Per ovviare a questa limitazione, l'implementazione corrente di OpenGL stampa le immagini OpenGL in bande.</span><span class="sxs-lookup"><span data-stu-id="1a39b-110">To overcome this limitation, the current implementation of OpenGL prints OpenGL graphics in bands.</span></span> <span data-ttu-id="1a39b-111">Tuttavia, questo aumenta il tempo necessario per stampare le immagini OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1a39b-111">However, this increases the time it takes to print OpenGL images.</span></span>

<span data-ttu-id="1a39b-112">Prima di stampare un'immagine OpenGL, è necessario chiamare la funzione [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) per completare l'inizializzazione di un contesto di dispositivo stampante (DC).</span><span class="sxs-lookup"><span data-stu-id="1a39b-112">Before you print an OpenGL image, you must call the [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) function to complete the initialization of a printer device context (DC).</span></span> <span data-ttu-id="1a39b-113">Dopo aver chiamato **StartDoc**, è possibile creare contesti di rendering (HGLRC) per eseguire il rendering sul dispositivo di stampa.</span><span class="sxs-lookup"><span data-stu-id="1a39b-113">After calling **StartDoc**, you can create rendering contexts (HGLRC) to render to the printer device.</span></span> <span data-ttu-id="1a39b-114">Se si creano contesti di rendering prima di chiamare **StartDoc**, non è possibile determinare se è stato eseguito lo spooling di un metafile.</span><span class="sxs-lookup"><span data-stu-id="1a39b-114">If you create rendering contexts before calling **StartDoc**, there is no way to determine whether a metafile is spooled.</span></span>

<span data-ttu-id="1a39b-115">Nell'esempio di codice seguente viene illustrato come stampare un'immagine OpenGL:</span><span class="sxs-lookup"><span data-stu-id="1a39b-115">The following code sample shows how to print an OpenGL image:</span></span>

``` syntax
HDC            hDC;
DOCINFO        di;
HGLRC          hglrc;

// Call StartDoc to start the document 
StartDoc( hDC, &di );

// Prepare the printer driver to accept data 
StartPage(hDC);

// Create a rendering context using the metafile DC 
hglrc = wglCreateContext ( hDCmetafile );

// Do OpenGL rendering operations here 
    . . .
wglMakeCurrent(NULL, NULL); // Get rid of rendering context 
    . . .
EndPage(hDC); // Finish writing to the page 
EndDoc(hDC); // End the print job
```

<span data-ttu-id="1a39b-116">Per altre informazioni sull'uso dei metafile, vedere [operazioni Metafile avanzate](/windows/desktop/gdi/enhanced-metafile-operations).</span><span class="sxs-lookup"><span data-stu-id="1a39b-116">For more information on using metafiles, see [Enhanced Metafile Operations](/windows/desktop/gdi/enhanced-metafile-operations).</span></span>

 

 
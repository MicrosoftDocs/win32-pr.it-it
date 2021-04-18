---
title: Porting di contesti di dispositivo e formati pixel
description: Porting di contesti di dispositivo e formati pixel
ms.assetid: b60cac27-1e2e-4da5-81c4-69446b92f820
keywords:
- porting in OpenGL, pixel
- Porting OpenGL, pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d793c139c6d7a0a0fc85b2e2c36f30176ce9ab6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297857"
---
# <a name="porting-device-contexts-and-pixel-formats"></a><span data-ttu-id="9a2b7-105">Porting di contesti di dispositivo e formati pixel</span><span class="sxs-lookup"><span data-stu-id="9a2b7-105">Porting Device Contexts and Pixel Formats</span></span>

<span data-ttu-id="9a2b7-106">Ogni finestra nell'implementazione Microsoft di OpenGL per Windows ha il proprio formato pixel corrente.</span><span class="sxs-lookup"><span data-stu-id="9a2b7-106">Each window in the Microsoft implementation of OpenGL for Windows has its own current pixel format.</span></span> <span data-ttu-id="9a2b7-107">Un formato pixel è definito da una struttura di dati [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="9a2b7-107">A pixel format is defined by a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure.</span></span> <span data-ttu-id="9a2b7-108">Poiché ogni finestra ha il proprio formato pixel, si ottiene un contesto di dispositivo, si imposta il formato pixel del contesto di dispositivo e quindi si crea un contesto di rendering OpenGL per il contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9a2b7-108">Because each window has its own pixel format, you obtain a device context, set the pixel format of the device context, and then create an OpenGL rendering context for the device context.</span></span> <span data-ttu-id="9a2b7-109">Il contesto di rendering usa automaticamente il formato pixel del relativo contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9a2b7-109">The rendering context automatically uses the pixel format of its device context.</span></span>

<span data-ttu-id="9a2b7-110">Il sistema X Window usa anche una struttura di dati, **XVisualInfo**, per specificare le proprietà dei pixel in una finestra.</span><span class="sxs-lookup"><span data-stu-id="9a2b7-110">The X Window System also uses a data structure, **XVisualInfo**, to specify the properties of pixels in a window.</span></span> <span data-ttu-id="9a2b7-111">Le strutture **XVisualInfo** contengono una struttura di dati **visiva** che descrive il modo in cui vengono usate le risorse di colore in una schermata specifica.</span><span class="sxs-lookup"><span data-stu-id="9a2b7-111">**XVisualInfo** structures contain a **Visual** data structure that describes how color resources are used in a specific screen.</span></span>

<span data-ttu-id="9a2b7-112">Nel sistema X Window, **XVisualInfo** viene usato per creare una finestra impostando la finestra sul formato pixel desiderato.</span><span class="sxs-lookup"><span data-stu-id="9a2b7-112">In the X Window System, **XVisualInfo** is used to create a window by setting the window to the pixel format you want.</span></span> <span data-ttu-id="9a2b7-113">La struttura restituita viene utilizzata per creare la finestra e un contesto di rendering.</span><span class="sxs-lookup"><span data-stu-id="9a2b7-113">The returned structure is used to create the window and a rendering context.</span></span> <span data-ttu-id="9a2b7-114">In Windows si crea prima una finestra e si ottiene un handle per un contesto di dispositivo (HDC) della finestra.</span><span class="sxs-lookup"><span data-stu-id="9a2b7-114">In Windows, you first create a window and get a handle to a device context (HDC) of the window.</span></span> <span data-ttu-id="9a2b7-115">HDC viene quindi usato per impostare il formato pixel per la finestra.</span><span class="sxs-lookup"><span data-stu-id="9a2b7-115">The HDC is then used to set the pixel format for the window.</span></span> <span data-ttu-id="9a2b7-116">Il contesto di rendering usa il formato pixel della finestra.</span><span class="sxs-lookup"><span data-stu-id="9a2b7-116">The rendering context uses the pixel format of the window.</span></span>

<span data-ttu-id="9a2b7-117">Nella tabella seguente vengono confrontate le funzioni visive di sistema X e GLX con le funzioni di formato pixel Windows equivalenti.</span><span class="sxs-lookup"><span data-stu-id="9a2b7-117">The following table compares the X Window System and GLX visual functions with their equivalent Windows pixel format functions.</span></span>



| <span data-ttu-id="9a2b7-118">Funzione visiva X/GLX</span><span class="sxs-lookup"><span data-stu-id="9a2b7-118">X window/GLX visual function</span></span>                                                                                     | <span data-ttu-id="9a2b7-119">Funzione formato pixel Windows</span><span class="sxs-lookup"><span data-stu-id="9a2b7-119">Windows pixel format function</span></span>                                                                                                      |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a2b7-120">XVisualInfo \* **glXChooseVisual**(display *\* DPY*, int *Screen*, int *\* attrib*)</span><span class="sxs-lookup"><span data-stu-id="9a2b7-120">XVisualInfo\***glXChooseVisual**( Display *\*dpy*,int *screen*,int *\*attribList*)</span></span>                               | <span data-ttu-id="9a2b7-121">int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)(HDC *HDC*, PIXELFORMATDESCRIPTOR *\* PPFD*)</span><span class="sxs-lookup"><span data-stu-id="9a2b7-121">int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)( HDC *hdc*,PIXELFORMATDESCRIPTOR *\*ppfd*)</span></span>                                      |
| <span data-ttu-id="9a2b7-122">int **glXGetConfig**(display *\* DPY*, XVisualInfo *\* Vis*, int *\* attrib*, int *\* value*)</span><span class="sxs-lookup"><span data-stu-id="9a2b7-122">int **glXGetConfig**( Display *\*dpy*,XVisualInfo *\*vis*,int *\*attribList*,int *\*value*)</span></span>                      | <span data-ttu-id="9a2b7-123">int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)(HDC *HDC*, int *iPixelFormat*, uint *nBytes*, LPPIXELFORMATDESCRIPTOR *PPFD*)</span><span class="sxs-lookup"><span data-stu-id="9a2b7-123">int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)( HDC *hdc*,int *iPixelFormat*,UINT *nBytes*,LPPIXELFORMATDESCRIPTOR *ppfd*)</span></span> |
| <span data-ttu-id="9a2b7-124">XVisualInfo \* **XGetVisualInfo**(display *\* DPY*, Long *vinfo \_ mask*, XVisualInfo *\* vinfo \_ Templ*, int *\* nItems*)</span><span class="sxs-lookup"><span data-stu-id="9a2b7-124">XVisualInfo\***XGetVisualInfo**( Display *\*dpy*,long *vinfo\_mask*,XVisualInfo *\*vinfo\_templ*,int *\*nitems*)</span></span> | <span data-ttu-id="9a2b7-125">int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)(HDC *HDC*)</span><span class="sxs-lookup"><span data-stu-id="9a2b7-125">int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)( HDC *hdc*)</span></span>                                                                           |
| <span data-ttu-id="9a2b7-126">Quando viene creata una finestra, viene usato l'oggetto *visivo* restituito da **glxChooseVisual** .</span><span class="sxs-lookup"><span data-stu-id="9a2b7-126">The *visual* returned by **glxChooseVisual** is used when a window is created.</span></span>                                   | <span data-ttu-id="9a2b7-127">BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)(HDC *HDC*, int *iPixelFormat*, PIXELFORMATDESCRIPTOR *\* PPFD*)</span><span class="sxs-lookup"><span data-stu-id="9a2b7-127">BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)( HDC *hdc*,int *iPixelFormat*,PIXELFORMATDESCRIPTOR *\*ppfd*)</span></span>                        |



 

<span data-ttu-id="9a2b7-128">Nelle sezioni seguenti vengono illustrati esempi di frammenti di codice in formato pixel per un programma di sistema Windows X e lo stesso codice dopo che è stato trasferito a Windows.</span><span class="sxs-lookup"><span data-stu-id="9a2b7-128">The following sections give examples of pixel format code fragments for an X Window System program, and the same code after it has been ported to Windows.</span></span>

-   [<span data-ttu-id="9a2b7-129">Esempio di codice in formato pixel GLX</span><span class="sxs-lookup"><span data-stu-id="9a2b7-129">GLX Pixel Format Code Sample</span></span>](glx-pixel-format-code-sample.md)
-   [<span data-ttu-id="9a2b7-130">Esempio di codice in formato pixel Windows</span><span class="sxs-lookup"><span data-stu-id="9a2b7-130">Windows Pixel Format Code Sample</span></span>](win32-pixel-format-code-sample.md)

<span data-ttu-id="9a2b7-131">Per ulteriori informazioni sui formati pixel, vedere [formati pixel](pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="9a2b7-131">For more information on pixel formats, see [Pixel Formats](pixel-formats.md).</span></span>

 

 





---
title: Porting di contesti di rendering
description: Porting di contesti di rendering
ms.assetid: 8655a81b-9f13-4ee5-ba0d-9aa9da1bfd09
keywords:
- rendering di contesti OpenGL, portabilità
- OpenGL per Windows, contesti di rendering
- porting in OpenGL, contesti di rendering
- Porting di OpenGL, contesti di rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e72839d04838b3173d772fbbf29a903a295cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396327"
---
# <a name="porting-rendering-contexts"></a><span data-ttu-id="e25ba-107">Porting di contesti di rendering</span><span class="sxs-lookup"><span data-stu-id="e25ba-107">Porting Rendering Contexts</span></span>

<span data-ttu-id="e25ba-108">Il sistema X Window e Windows eseguono il rendering dei contesti di rendering.</span><span class="sxs-lookup"><span data-stu-id="e25ba-108">The X Window System and Windows render through rendering contexts.</span></span> <span data-ttu-id="e25ba-109">Sei funzioni GLX gestiscono i contesti di rendering e cinque di essi hanno una funzione di Windows equivalente.</span><span class="sxs-lookup"><span data-stu-id="e25ba-109">Six GLX functions manage rendering contexts and five of them have an equivalent Windows function.</span></span>

<span data-ttu-id="e25ba-110">Nella tabella seguente sono elencate le funzioni di rendering di GLX e le relative funzioni Windows equivalenti.</span><span class="sxs-lookup"><span data-stu-id="e25ba-110">The following table lists the GLX rendering functions and their equivalent Windows functions.</span></span>



| <span data-ttu-id="e25ba-111">Funzione del contesto di rendering GLX</span><span class="sxs-lookup"><span data-stu-id="e25ba-111">GLX rendering context function</span></span>                                                                            | <span data-ttu-id="e25ba-112">Funzione del contesto di rendering Windows</span><span class="sxs-lookup"><span data-stu-id="e25ba-112">Windows rendering context function</span></span>                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e25ba-113">GLXContext **glXCopyContext**(display *\* DPY*, GLXContext *src*, GLXContext *DST*, Gluint *mask*)</span><span class="sxs-lookup"><span data-stu-id="e25ba-113">GLXContext **glXCopyContext**( Display *\*dpy*,GLXContext *src*,GLXContext *dst*,GLuint *mask*)</span></span>            | <span data-ttu-id="e25ba-114">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="e25ba-114">Not applicable.</span></span>                                                         |
| <span data-ttu-id="e25ba-115">GLXContext **glXCreateContext**(display *\* DPY*, XVisualInfo *\* Vis*, GLXContext *shares*, bool *Direct*)</span><span class="sxs-lookup"><span data-stu-id="e25ba-115">GLXContext **glXCreateContext**( Display *\*dpy*,XVisualInfo *\*vis*,GLXContext *shareList*,Bool *direct*)</span></span> | <span data-ttu-id="e25ba-116">HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)(HDC *HDC*)</span><span class="sxs-lookup"><span data-stu-id="e25ba-116">HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)( HDC *hdc*)</span></span>          |
| <span data-ttu-id="e25ba-117">void **glXDeleteContext**(display *\* DPY*, GLXContext *ctx*)</span><span class="sxs-lookup"><span data-stu-id="e25ba-117">void **glXDeleteContext**( Display *\*dpy*,GLXContext *ctx*)</span></span>                                              | <span data-ttu-id="e25ba-118">BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)(HGLRC *HGLRC*)</span><span class="sxs-lookup"><span data-stu-id="e25ba-118">BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)( HGLRC *hglrc*)</span></span>       |
| <span data-ttu-id="e25ba-119">GLXContext **glXGetCurrentContext**(*void*)</span><span class="sxs-lookup"><span data-stu-id="e25ba-119">GLXContext **glXGetCurrentContext**(*void*)</span></span>                                                               | <span data-ttu-id="e25ba-120">HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*void*)</span><span class="sxs-lookup"><span data-stu-id="e25ba-120">HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*VOID*)</span></span>      |
| <span data-ttu-id="e25ba-121">GLXDrawable **glXGetCurrentDrawable**(*void*)</span><span class="sxs-lookup"><span data-stu-id="e25ba-121">GLXDrawable **glXGetCurrentDrawable**(*void*)</span></span>                                                             | <span data-ttu-id="e25ba-122">HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*void*)</span><span class="sxs-lookup"><span data-stu-id="e25ba-122">HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*VOID*)</span></span>                  |
| <span data-ttu-id="e25ba-123">Bool **glXMakeCurrent**(display *\* DPY*, GLXDrawable *disegnato*, GLXContext *ctx*)</span><span class="sxs-lookup"><span data-stu-id="e25ba-123">Bool **glXMakeCurrent**( Display *\*dpy*,GLXDrawable *draw*,GLXContext *ctx*)</span></span>                              | <span data-ttu-id="e25ba-124">BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)(HDC *HDC*, HGLRC *HGLRC*)</span><span class="sxs-lookup"><span data-stu-id="e25ba-124">BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)( HDC *hdc*,HGLRC *hglrc*)</span></span> |



 

<span data-ttu-id="e25ba-125">I tipi restituiti e altri tipi hanno nomi diversi nel sistema X Window rispetto a Windows.</span><span class="sxs-lookup"><span data-stu-id="e25ba-125">Return types and other types have different names in the X Window System than in Windows.</span></span> <span data-ttu-id="e25ba-126">È possibile cercare le occorrenze di GLXContext per trovare le parti del codice che devono essere trasferite.</span><span class="sxs-lookup"><span data-stu-id="e25ba-126">You can search for occurrences of GLXContext to help find parts of your code that need to be ported.</span></span>

<span data-ttu-id="e25ba-127">Nelle sezioni seguenti vengono confrontati gli esempi di codice del contesto di rendering in un programma di sistema finestra X e lo stesso codice dopo che è stato trasferito a Windows.</span><span class="sxs-lookup"><span data-stu-id="e25ba-127">The following sections compare rendering context code samples in an X Window System program and the same code after it has been ported to Windows.</span></span>

<span data-ttu-id="e25ba-128">Per ulteriori informazioni sui contesti di rendering, vedere [contesti di rendering](rendering-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="e25ba-128">For more information on rendering contexts, see [Rendering Contexts](rendering-contexts.md).</span></span>

 

 





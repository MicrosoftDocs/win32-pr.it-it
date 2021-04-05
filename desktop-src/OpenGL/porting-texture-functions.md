---
title: Porting di funzioni di trama
description: Porting di funzioni di trama
ms.assetid: 03e0b0fc-3812-4744-a0f1-3dcb466d679d
keywords:
- Porting di IRIS GL, trama
- porting da IRIS GL, trama
- porting in OpenGL da IRIS GL, trama
- Porting OpenGL da IRIS GL, trama
- trama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cba8b105089553084a93f997517d19cf371e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044940"
---
# <a name="porting-texture-functions"></a><span data-ttu-id="ac51b-108">Porting di funzioni di trama</span><span class="sxs-lookup"><span data-stu-id="ac51b-108">Porting Texture Functions</span></span>

<span data-ttu-id="ac51b-109">Quando si esegue il porting delle funzioni di trama di IRIS GL in OpenGL, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="ac51b-109">When porting IRIS GL texture functions to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="ac51b-110">OpenGL non mantiene le tabelle di trame; USA solo la trama a una D e la trama 2D.</span><span class="sxs-lookup"><span data-stu-id="ac51b-110">OpenGL doesn't maintain tables of textures; it uses either 1-D texture and 2-D texture only.</span></span> <span data-ttu-id="ac51b-111">Per riutilizzare le trame dal codice di IRIS GL, inserirle in un elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ac51b-111">To reuse the textures from your IRIS GL code, put them in a display list.</span></span>
-   <span data-ttu-id="ac51b-112">OpenGL non genera automaticamente mipmap.</span><span class="sxs-lookup"><span data-stu-id="ac51b-112">OpenGL doesn't automatically generate mipmaps.</span></span> <span data-ttu-id="ac51b-113">Se si usa mipmap, è necessario chiamare prima la funzione [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) .</span><span class="sxs-lookup"><span data-stu-id="ac51b-113">If you're using mipmaps, you must first call the [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) function.</span></span>
-   <span data-ttu-id="ac51b-114">In OpenGL si usano [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) per attivare e disattivare le funzionalità di texturing.</span><span class="sxs-lookup"><span data-stu-id="ac51b-114">In OpenGL, you use [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) to turn texturing capabilities on and off.</span></span>
-   <span data-ttu-id="ac51b-115">In OpenGL, le dimensioni della trama sono più rigorosamente regolate rispetto a IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="ac51b-115">In OpenGL, texture size is more strictly regulated than in IRIS GL.</span></span> <span data-ttu-id="ac51b-116">Le dimensioni di una trama OpenGL devono essere le seguenti:</span><span class="sxs-lookup"><span data-stu-id="ac51b-116">The size of an OpenGL texture must be:</span></span>

    <span data-ttu-id="ac51b-117">2 *n* + 2 *b*</span><span class="sxs-lookup"><span data-stu-id="ac51b-117">2 *n* + 2 *b*</span></span>

    <span data-ttu-id="ac51b-118">dove *n* è un numero intero e *b* è:</span><span class="sxs-lookup"><span data-stu-id="ac51b-118">where *n* is an integer and *b* is:</span></span>

    -   <span data-ttu-id="ac51b-119">0, se la trama non ha bordo</span><span class="sxs-lookup"><span data-stu-id="ac51b-119">0, if the texture has no border</span></span>
    -   <span data-ttu-id="ac51b-120">1, se la trama ha un pixel del bordo, le trame OpenGL possono avere bordi di 1 pixel.</span><span class="sxs-lookup"><span data-stu-id="ac51b-120">1, if the texture has a border pixel (OpenGL textures can have 1-pixel borders.)</span></span>

<span data-ttu-id="ac51b-121">La tabella seguente elenca le funzioni di trama di IRIS GL e i rispettivi equivalenti OpenGL generali.</span><span class="sxs-lookup"><span data-stu-id="ac51b-121">The following table lists IRIS GL texture functions and their general OpenGL equivalents.</span></span>



| <span data-ttu-id="ac51b-122">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="ac51b-122">IRIS GL function</span></span> | <span data-ttu-id="ac51b-123">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="ac51b-123">OpenGL function</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="ac51b-124">Significato</span><span class="sxs-lookup"><span data-stu-id="ac51b-124">Meaning</span></span>                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac51b-125">**textdef2d**</span><span class="sxs-lookup"><span data-stu-id="ac51b-125">**textdef2d**</span></span>    | <span data-ttu-id="ac51b-126">[](glteximage2d.md)[**glTexParameter** glTexImage2D](gltexparameter-functions.md)</span><span class="sxs-lookup"><span data-stu-id="ac51b-126">[**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)</span></span><br/> [<span data-ttu-id="ac51b-127">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="ac51b-127">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)<br/>                                                                                                           | <span data-ttu-id="ac51b-128">Specifica un'immagine di trama 2D.</span><span class="sxs-lookup"><span data-stu-id="ac51b-128">Specifies a 2-D texture image.</span></span>                                                              |
| <span data-ttu-id="ac51b-129">**textbind**</span><span class="sxs-lookup"><span data-stu-id="ac51b-129">**textbind**</span></span>     | <span data-ttu-id="ac51b-130">**glTexImage2DglTexParameter**</span><span class="sxs-lookup"><span data-stu-id="ac51b-130">**glTexImage2DglTexParameter**</span></span><br/> <span data-ttu-id="ac51b-131">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="ac51b-131">**gluBuild2DMipmaps**</span></span><br/>                                                                                                                                                                                            | <span data-ttu-id="ac51b-132">Seleziona una funzione di trama.</span><span class="sxs-lookup"><span data-stu-id="ac51b-132">Selects a texture function.</span></span>                                                                 |
| <span data-ttu-id="ac51b-133">**tevdef**</span><span class="sxs-lookup"><span data-stu-id="ac51b-133">**tevdef**</span></span>       | [<span data-ttu-id="ac51b-134">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="ac51b-134">**glTexEnv**</span></span>](gltexenv-functions.md)                                                                                                                                                                                                                                | <span data-ttu-id="ac51b-135">Definisce un ambiente di mapping di trame.</span><span class="sxs-lookup"><span data-stu-id="ac51b-135">Defines a texture-mapping environment.</span></span>                                                      |
| <span data-ttu-id="ac51b-136">**tevbind**</span><span class="sxs-lookup"><span data-stu-id="ac51b-136">**tevbind**</span></span>      | <span data-ttu-id="ac51b-137">[**glTexImage1D** glTexEnv](glteximage1d.md)</span><span class="sxs-lookup"><span data-stu-id="ac51b-137">**glTexEnv**[**glTexImage1D**](glteximage1d.md)</span></span><br/>                                                                                                                                                                                                           | <span data-ttu-id="ac51b-138">Seleziona un ambiente di trama.</span><span class="sxs-lookup"><span data-stu-id="ac51b-138">Selects a texture environment.</span></span>                                                              |
| <span data-ttu-id="ac51b-139">**T2**</span><span class="sxs-lookup"><span data-stu-id="ac51b-139">**t2**</span></span>           | [<span data-ttu-id="ac51b-140">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="ac51b-140">**glTexCoord**</span></span>](gltexcoord-functions.md)                                                                                                                                                                                                                            | <span data-ttu-id="ac51b-141">Imposta le coordinate di trama correnti.</span><span class="sxs-lookup"><span data-stu-id="ac51b-141">Sets the current texture coordinates.</span></span>                                                       |
| <span data-ttu-id="ac51b-142">**texgen**</span><span class="sxs-lookup"><span data-stu-id="ac51b-142">**texgen**</span></span>       | <span data-ttu-id="ac51b-143">[](gltexgen-functions.md)[**glGetTexParameter** glTexGen](glgettexparameter.md)</span><span class="sxs-lookup"><span data-stu-id="ac51b-143">[**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)</span></span><br/> [<span data-ttu-id="ac51b-144">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="ac51b-144">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)<br/> [<span data-ttu-id="ac51b-145">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="ac51b-145">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)<br/> [<span data-ttu-id="ac51b-146">**gluScaleImage**</span><span class="sxs-lookup"><span data-stu-id="ac51b-146">**gluScaleImage**</span></span>](gluscaleimage.md)<br/> | <span data-ttu-id="ac51b-147">Controlla la generazione delle coordinate di trama. Ridimensiona un'immagine a una dimensione arbitraria.</span><span class="sxs-lookup"><span data-stu-id="ac51b-147">Controls generation of texture coordinates.Scales an image to an arbitrary size.</span></span><br/> |



 

<span data-ttu-id="ac51b-148">Per ulteriori informazioni sul texturing, vedere la *Guida alla programmazione di OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="ac51b-148">For more information on texturing, see the *OpenGL Programming Guide*.</span></span>

<span data-ttu-id="ac51b-149">Questo argomento include informazioni sui seguenti elementi.</span><span class="sxs-lookup"><span data-stu-id="ac51b-149">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="ac51b-150">Conversione di tevdef</span><span class="sxs-lookup"><span data-stu-id="ac51b-150">Translating tevdef</span></span>](translating-tevdef.md)
-   [<span data-ttu-id="ac51b-151">Conversione di texdef</span><span class="sxs-lookup"><span data-stu-id="ac51b-151">Translating texdef</span></span>](translating-texdef.md)
-   [<span data-ttu-id="ac51b-152">Conversione di texgen</span><span class="sxs-lookup"><span data-stu-id="ac51b-152">Translating texgen</span></span>](translating-texgen.md)

 

 






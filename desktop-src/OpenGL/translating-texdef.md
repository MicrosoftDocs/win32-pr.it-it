---
title: Conversione di texdef
description: L'esempio di codice seguente è una definizione di trama di IRIS GL
ms.assetid: bb2d257d-ee74-4a65-b364-c7a97bccaa78
keywords:
- Porting di IRIS GL, trama
- porting da IRIS GL, trama
- porting in OpenGL da IRIS GL, trama
- Porting OpenGL da IRIS GL, trama
- trama
- Porting di IRIS GL, texdef
- porting da IRIS GL, texdef
- porting in OpenGL da IRIS GL, texdef
- Porting OpenGL da IRIS GL, texdef
- texdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479af06bcfd3a50daf56fb0629e4c32f24750081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856810"
---
# <a name="translating-texdef"></a><span data-ttu-id="87dc2-113">Conversione di texdef</span><span class="sxs-lookup"><span data-stu-id="87dc2-113">Translating texdef</span></span>

<span data-ttu-id="87dc2-114">L'esempio di codice seguente è una definizione di trama di IRIS GL:</span><span class="sxs-lookup"><span data-stu-id="87dc2-114">The following code example is an IRIS GL texture definition:</span></span>


```C++
float texprops[] = { TX_MINFILTER, TX_POINT, 
                         TX_MAGFILTER, TX_POINT, 
                         TX_WRAP_S, TX_REPEAT, 
                         TX_WRAP_T, TX_REPEAT, 
                         TX_NULL }; 
 
textdef2d(1, 1, 6, 6, granite_texture, 7, texprops);
```



<span data-ttu-id="87dc2-115">Nell'esempio precedente, **texdef** specifica il filtro del \_ punto TX sia come ingrandimento che come filtro di riduzione a icona e TX \_ Ripeti come meccanismo di wrapping.</span><span class="sxs-lookup"><span data-stu-id="87dc2-115">In the preceding example, **texdef** specifies the TX\_POINT filter as both the magnification and the minimizing filter, and TX\_REPEAT as the wrapping mechanism.</span></span> <span data-ttu-id="87dc2-116">Specifica anche l'immagine della trama, **ovvero \_ granito**.</span><span class="sxs-lookup"><span data-stu-id="87dc2-116">It also specifies the texture image: **granite\_texture**.</span></span>

<span data-ttu-id="87dc2-117">In OpenGL, [**glTexImage**](glteximage1d.md) specifica l'immagine e [glTexParameter](gltexparameter-functions.md) imposta la proprietà.</span><span class="sxs-lookup"><span data-stu-id="87dc2-117">In OpenGL, [**glTexImage**](glteximage1d.md) specifies the image and [glTexParameter](gltexparameter-functions.md) sets the property.</span></span> <span data-ttu-id="87dc2-118">Per tradurre le definizioni delle trame IRIS GL, sostituire la funzione **textdef** con **glTexImage** e una o più chiamate a **glTexParameter**.</span><span class="sxs-lookup"><span data-stu-id="87dc2-118">To translate IRIS GL texture definitions, replace the **textdef** function with **glTexImage** and one or more calls to **glTexParameter**.</span></span>

<span data-ttu-id="87dc2-119">Il codice di IRIS GL precedente ha un aspetto simile al seguente quando viene convertito in OpenGL:</span><span class="sxs-lookup"><span data-stu-id="87dc2-119">The preceding IRIS GL code looks like this when translated to OpenGL:</span></span>


```C++
GLfloat nearest[] = {GL_NEAREST}; 
GLfloat repeat = {GL_REPEAT}; 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MIN_FILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MAGILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_S, repeat); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_T, nearest); 
glTexImage1D( GL_TEXTURE_1D, 0, 1, 6, 0, GL_RGB, GL_UNSIGNED_SHORT, granite_texture);
```



<span data-ttu-id="87dc2-120">La tabella seguente elenca i parametri di trama di IRIS GL e i parametri OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="87dc2-120">The following table lists the IRIS GL texture parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="87dc2-121">Parametro trama IRIS GL</span><span class="sxs-lookup"><span data-stu-id="87dc2-121">IRIS GL texture parameter</span></span> | <span data-ttu-id="87dc2-122">Parametro trama OpenGL</span><span class="sxs-lookup"><span data-stu-id="87dc2-122">OpenGL texture parameter</span></span>                                  |
|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="87dc2-123">\_MINFILTER TX</span><span class="sxs-lookup"><span data-stu-id="87dc2-123">TX\_MINFILTER</span></span>             | <span data-ttu-id="87dc2-124">\_ \_ Filtro minimo trama \_ GL</span><span class="sxs-lookup"><span data-stu-id="87dc2-124">GL\_TEXTURE\_MIN\_FILTER</span></span>                                  |
| <span data-ttu-id="87dc2-125">\_MAGFILTER TX</span><span class="sxs-lookup"><span data-stu-id="87dc2-125">TX\_MAGFILTER</span></span>             | <span data-ttu-id="87dc2-126">\_ \_ filtro mag trama di contabilità \_</span><span class="sxs-lookup"><span data-stu-id="87dc2-126">GL\_TEXTURE\_MAG\_FILTER</span></span>                                  |
| <span data-ttu-id="87dc2-127">TX \_ wrap, TX \_ Wrap \_ S</span><span class="sxs-lookup"><span data-stu-id="87dc2-127">TX\_WRAP, TX\_WRAP\_S</span></span>     | <span data-ttu-id="87dc2-128">\_wrapping di trama GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="87dc2-128">GL\_TEXTURE\_WRAP\_S</span></span>                                      |
| <span data-ttu-id="87dc2-129">TX \_ wrap, TX \_ Wrap \_ T</span><span class="sxs-lookup"><span data-stu-id="87dc2-129">TX\_WRAP, TX\_WRAP\_T</span></span>     | <span data-ttu-id="87dc2-130">\_ \_ \_ \_ \_ colore bordo trama TGL \_ trama a capo</span><span class="sxs-lookup"><span data-stu-id="87dc2-130">GL\_TEXTURE\_WRAP\_TGL\_TEXTURE\_BORDER\_COLOR</span></span><br/> |



 

<span data-ttu-id="87dc2-131">La tabella seguente elenca i valori possibili dei parametri di trama di IRIS GL e i parametri OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="87dc2-131">The following table lists the possible values of the IRIS GL texture parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="87dc2-132">Parametro trama IRIS GL</span><span class="sxs-lookup"><span data-stu-id="87dc2-132">IRIS GL texture parameter</span></span> | <span data-ttu-id="87dc2-133">Parametro trama OpenGL</span><span class="sxs-lookup"><span data-stu-id="87dc2-133">OpenGL texture parameter</span></span>     |
|---------------------------|------------------------------|
| <span data-ttu-id="87dc2-134">\_punto TX</span><span class="sxs-lookup"><span data-stu-id="87dc2-134">TX\_POINT</span></span>                 | <span data-ttu-id="87dc2-135">GL \_ più vicino</span><span class="sxs-lookup"><span data-stu-id="87dc2-135">GL\_NEAREST</span></span>                  |
| <span data-ttu-id="87dc2-136">\_BIlineare TX</span><span class="sxs-lookup"><span data-stu-id="87dc2-136">TX\_BILINEAR</span></span>              | <span data-ttu-id="87dc2-137">\_linea GL</span><span class="sxs-lookup"><span data-stu-id="87dc2-137">GL\_LINEAR</span></span>                   |
| <span data-ttu-id="87dc2-138">\_punto MIPMAP \_ TX</span><span class="sxs-lookup"><span data-stu-id="87dc2-138">TX\_MIPMAP\_POINT</span></span>         | <span data-ttu-id="87dc2-139">GL \_ più vicino \_ MIPMAP \_ più vicino</span><span class="sxs-lookup"><span data-stu-id="87dc2-139">GL\_NEAREST\_MIPMAP\_NEAREST</span></span> |
| <span data-ttu-id="87dc2-140">TX \_ MIPMAP \_ bilinear</span><span class="sxs-lookup"><span data-stu-id="87dc2-140">TX\_MIPMAP\_BILINEAR</span></span>      | <span data-ttu-id="87dc2-141">\_MIPMAP lineare \_ \_ più vicino</span><span class="sxs-lookup"><span data-stu-id="87dc2-141">GL\_LINEAR\_MIPMAP\_NEAREST</span></span>  |
| <span data-ttu-id="87dc2-142">\_MIPMAP \_ lineare TX</span><span class="sxs-lookup"><span data-stu-id="87dc2-142">TX\_MIPMAP\_LINEAR</span></span>        | <span data-ttu-id="87dc2-143">GL \_ più vicino \_ MIPMAP \_ lineare</span><span class="sxs-lookup"><span data-stu-id="87dc2-143">GL\_NEAREST\_MIPMAP\_LINEAR</span></span>  |
| <span data-ttu-id="87dc2-144">\_TRIlineare TX</span><span class="sxs-lookup"><span data-stu-id="87dc2-144">TX\_TRILINEAR</span></span>             | <span data-ttu-id="87dc2-145">\_MIPMAP lineare \_ lineare \_</span><span class="sxs-lookup"><span data-stu-id="87dc2-145">GL\_LINEAR\_MIPMAP\_LINEAR</span></span>   |



 

 

 






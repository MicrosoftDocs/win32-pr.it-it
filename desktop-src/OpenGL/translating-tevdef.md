---
title: Conversione di tevdef
description: L'esempio di codice seguente è una definizione dell'ambiente di trama di IRIS GL che specifica il \_ parametro di trama-ambiente delle decalcomanie TV
ms.assetid: bb4c8231-8102-4ecb-a5d2-c41243c2682d
keywords:
- Porting di IRIS GL, trama
- porting da IRIS GL, trama
- porting in OpenGL da IRIS GL, trama
- Porting OpenGL da IRIS GL, trama
- trama
- Porting di IRIS GL, tevdef
- porting da IRIS GL, tevdef
- porting in OpenGL da IRIS GL, tevdef
- Porting OpenGL da IRIS GL, tevdef
- tevdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac2610d1467adb6faa1ea105fc8e8734bfb9c4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955786"
---
# <a name="translating-tevdef"></a><span data-ttu-id="9dc2f-113">Conversione di tevdef</span><span class="sxs-lookup"><span data-stu-id="9dc2f-113">Translating tevdef</span></span>

<span data-ttu-id="9dc2f-114">L'esempio di codice seguente è una definizione dell'ambiente di trama di IRIS GL che specifica il \_ parametro di trama-ambiente delle decalcomanie TV:</span><span class="sxs-lookup"><span data-stu-id="9dc2f-114">The following code example is an IRIS GL texture-environment definition that specifies the TV\_DECAL texture-environment parameter:</span></span>


```C++
float tevprops[] = {TV_DECAL, TV_NULL}; 
 
tevdef(1, 0, tevprops);
```



<span data-ttu-id="9dc2f-115">e lo stesso codice è stato convertito in OpenGL:</span><span class="sxs-lookup"><span data-stu-id="9dc2f-115">and the same code translated to OpenGL:</span></span>


```C++
glTexEnvfv(GL_TEXTURE_ENV, GL_TEXTURE_ENV_MODE, GL_DECAL);
```



<span data-ttu-id="9dc2f-116">La tabella seguente elenca i parametri dell'ambiente di trama di IRIS GL e i parametri OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="9dc2f-116">The following table lists the IRIS GL texture-environment parameters and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="9dc2f-117">Parametro di IRIS GL</span><span class="sxs-lookup"><span data-stu-id="9dc2f-117">IRIS GL parameter</span></span>     | <span data-ttu-id="9dc2f-118">Parametro OpenGL</span><span class="sxs-lookup"><span data-stu-id="9dc2f-118">OpenGL parameter</span></span>             |
|-----------------------|------------------------------|
| <span data-ttu-id="9dc2f-119">\_modulazione TV</span><span class="sxs-lookup"><span data-stu-id="9dc2f-119">TV\_MODULATE</span></span>          | <span data-ttu-id="9dc2f-120">\_modulazione GL</span><span class="sxs-lookup"><span data-stu-id="9dc2f-120">GL\_MODULATE</span></span>                 |
| <span data-ttu-id="9dc2f-121">\_decalcomania TV</span><span class="sxs-lookup"><span data-stu-id="9dc2f-121">TV\_DECAL</span></span>             | <span data-ttu-id="9dc2f-122">\_decalcomania GL</span><span class="sxs-lookup"><span data-stu-id="9dc2f-122">GL\_DECAL</span></span>                    |
| <span data-ttu-id="9dc2f-123">\_Blend TV</span><span class="sxs-lookup"><span data-stu-id="9dc2f-123">TV\_BLEND</span></span>             | <span data-ttu-id="9dc2f-124">\_Blend GL</span><span class="sxs-lookup"><span data-stu-id="9dc2f-124">GL\_BLEND</span></span>                    |
| <span data-ttu-id="9dc2f-125">\_colore TV</span><span class="sxs-lookup"><span data-stu-id="9dc2f-125">TV\_COLOR</span></span>             | <span data-ttu-id="9dc2f-126">\_ \_ colore ENV trama \_ GL</span><span class="sxs-lookup"><span data-stu-id="9dc2f-126">GL\_TEXTURE\_ENV\_COLOR</span></span>      |
| <span data-ttu-id="9dc2f-127">TV \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="9dc2f-127">TV\_ALPHA</span></span>             | <span data-ttu-id="9dc2f-128">Nessun equivalente OpenGL diretto.</span><span class="sxs-lookup"><span data-stu-id="9dc2f-128">No direct OpenGL equivalent.</span></span> |
| <span data-ttu-id="9dc2f-129">\_selezione componente \_ TV</span><span class="sxs-lookup"><span data-stu-id="9dc2f-129">TV\_COMPONENT\_SELECT</span></span> | <span data-ttu-id="9dc2f-130">Nessun equivalente OpenGL diretto.</span><span class="sxs-lookup"><span data-stu-id="9dc2f-130">No direct OpenGL equivalent.</span></span> |



 

<span data-ttu-id="9dc2f-131">Per ulteriori informazioni sui parametri dell'ambiente di trama, vedere [**glTexEnv**](gltexenv-functions.md).</span><span class="sxs-lookup"><span data-stu-id="9dc2f-131">For more information about texture-environment parameters, see [**glTexEnv**](gltexenv-functions.md).</span></span>

 

 





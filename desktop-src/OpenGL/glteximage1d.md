---
title: funzione glTexImage1D (GL. h)
description: La funzione glTexImage1D specifica un'immagine di trama unidimensionale.
ms.assetid: 4f537b89-2ea2-4e2e-8c57-c372bf53f12c
keywords:
- funzione glTexImage1D OpenGL
topic_type:
- apiref
api_name:
- glTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1865d19c54b9c59654f07162d2480aa5b29c47f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048233"
---
# <a name="glteximage1d-function"></a><span data-ttu-id="2ee5e-104">glTexImage1D (funzione)</span><span class="sxs-lookup"><span data-stu-id="2ee5e-104">glTexImage1D function</span></span>

<span data-ttu-id="2ee5e-105">La funzione **glTexImage1D** specifica un'immagine di trama unidimensionale.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-105">The **glTexImage1D** function specifies a one-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ee5e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ee5e-106">Syntax</span></span>


```C++
void WINAPI glTexImage1D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="2ee5e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ee5e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ee5e-108">*target*</span><span class="sxs-lookup"><span data-stu-id="2ee5e-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="2ee5e-109">Trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-109">The target texture.</span></span> <span data-ttu-id="2ee5e-110">Deve essere una \_ trama GL \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-110">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="2ee5e-111">*level*</span><span class="sxs-lookup"><span data-stu-id="2ee5e-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="2ee5e-112">Numero del livello di dettaglio.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-112">The level-of-detail number.</span></span> <span data-ttu-id="2ee5e-113">Il livello 0 è il livello dell'immagine di base.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-113">Level 0 is the base image level.</span></span> <span data-ttu-id="2ee5e-114">Il livello *n* è l'immagine di riduzione del mipmap *n*.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-114">Level *n* is the *n* Th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="2ee5e-115">*internalformat*</span><span class="sxs-lookup"><span data-stu-id="2ee5e-115">*internalformat*</span></span> 
</dt> <dd>

<span data-ttu-id="2ee5e-116">Specifica il numero di componenti di colore nella trama.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-116">Specifies the number of color components in the texture.</span></span> <span data-ttu-id="2ee5e-117">Deve essere 1, 2, 3 o 4 o una delle costanti simboliche seguenti: GL \_ Alpha, GL \_ ALPHA4, GL \_ ALPHA8, GL ALPHA12, GL ALPHA16, GL Luminance, GL LUMINANCE4, GL LUMINANCE8, GL LUMINANCE12, GL LUMINANCE16, GL \_ \_ \_ \_ \_ \_ \_ \_ Luminance \_ Alpha, GL \_ LUMINANCE4 \_ ALPHA4, GL \_ LUMINANCE6 \_ alfa2, GL LUMINANCE8 \_ \_ ALPHA8, GL \_ LUMINANCE12 ALPHA4, \_ GL \_ LUMINANCE12 \_ ALPHA12, GL LUMINANCE16 ALPHA16, GL Intensity, GL INTENSITY4, GL \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ INTENSITY8, GL INTENSITY12, GL INTENSITY16, GL RGB, GL RGB4, GL RGB5, GL RGB8, GL RGB10, GL RGB12, GL RGB16, GL RGBA, GL RGBA2, GL RGBA4, GL RGB5, GL Rgba8, GL RGB10 a1, GL RGBA12, GL RGBA16 a2, GL o GL.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-117">Must be 1, 2, 3, or 4, or one of the following symbolic constants: GL\_ALPHA, GL\_ALPHA4, GL\_ALPHA8, GL\_ALPHA12, GL\_ALPHA16, GL\_LUMINANCE, GL\_LUMINANCE4, GL\_LUMINANCE8, GL\_LUMINANCE12, GL\_LUMINANCE16, GL\_LUMINANCE\_ALPHA, GL\_LUMINANCE4\_ALPHA4, GL\_LUMINANCE6\_ALPHA2, GL\_LUMINANCE8\_ALPHA8, GL\_LUMINANCE12\_ALPHA4, GL\_LUMINANCE12\_ALPHA12, GL\_LUMINANCE16\_ALPHA16, GL\_INTENSITY, GL\_INTENSITY4, GL\_INTENSITY8, GL\_INTENSITY12, GL\_INTENSITY16, GL\_RGB, GL\_R3\_G3\_B2, GL\_RGB4, GL\_RGB5, GL\_RGB8, GL\_RGB10, GL\_RGB12, GL\_RGB16, GL\_RGBA, GL\_RGBA2, GL\_RGBA4, GL\_RGB5\_A1, GL\_RGBA8, GL\_RGB10\_A2, GL\_RGBA12, or GL\_RGBA16.</span></span>

</dd> <dt>

<span data-ttu-id="2ee5e-118">*width*</span><span class="sxs-lookup"><span data-stu-id="2ee5e-118">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="2ee5e-119">Larghezza dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-119">The width of the texture image.</span></span> <span data-ttu-id="2ee5e-120">Deve essere 2 *n* + 2 ( *bordo* ) per alcuni numeri interi *n*.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-120">Must be 2 *n* + 2( *border* ) for some integer *n*.</span></span> <span data-ttu-id="2ee5e-121">L'altezza dell'immagine della trama è 1.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-121">The height of the texture image is 1.</span></span>

</dd> <dt>

<span data-ttu-id="2ee5e-122">*bordo*</span><span class="sxs-lookup"><span data-stu-id="2ee5e-122">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="2ee5e-123">Larghezza del bordo.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-123">The width of the border.</span></span> <span data-ttu-id="2ee5e-124">Deve essere 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-124">Must be either 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="2ee5e-125">*format*</span><span class="sxs-lookup"><span data-stu-id="2ee5e-125">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="2ee5e-126">Formato dei dati pixel.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-126">The format of the pixel data.</span></span> <span data-ttu-id="2ee5e-127">Può assumere uno dei nove valori simbolici.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-127">It can assume one of nine symbolic values.</span></span>



| <span data-ttu-id="2ee5e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2ee5e-128">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="2ee5e-129">Significato</span><span class="sxs-lookup"><span data-stu-id="2ee5e-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="2ee5e-130"><dt>**\_indice colori \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-130"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="2ee5e-131">Ogni elemento è un singolo valore, ovvero un indice colori.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-131">Each element is a single value, a color index.</span></span> <span data-ttu-id="2ee5e-132">Viene convertito in un punto fisso (con un numero non specificato di 0 bit a destra del punto binario), spostato a sinistra o a destra, a seconda del valore e del segno dello spostamento di \_ indice GL \_ e aggiunto all'offset dell' \_ indice GL \_ (vedere [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="2ee5e-132">It is converted to fixed point (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="2ee5e-133">L'indice risultante viene convertito in un set di componenti colore usando il \_ mapping GL pixel i \_ \_ \_ a \_ R, GL \_ pixel \_ Map \_ i \_ a \_ G, GL \_ pixel \_ Map \_ i \_ a \_ B e GL \_ pixel \_ mappa \_ i \_ a \_ una tabella e l'intervallo viene premuto nell'intervallo \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="2ee5e-133">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="2ee5e-134"><dt>**\_rosso GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-134"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="2ee5e-135">Ogni elemento è un singolo componente rosso.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-135">Each element is a single red component.</span></span> <span data-ttu-id="2ee5e-136">Viene convertita in virgola mobile e assemblata in un elemento RGBA collegando 0,0 per verde e blu e 1,0 per alfa.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-136">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="2ee5e-137">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="2ee5e-137">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="2ee5e-138"><dt>**\_verde GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-138"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="2ee5e-139">Ogni elemento è un singolo componente verde.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-139">Each element is a single green component.</span></span> <span data-ttu-id="2ee5e-140">Viene convertita in virgola mobile e assemblata in un elemento RGBA collegando 0,0 per Red e Blue e 1,0 per Alpha.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-140">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="2ee5e-141">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="2ee5e-141">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="2ee5e-142"><dt>**\_blu GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-142"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="2ee5e-143">Ogni elemento è un singolo componente blu.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-143">Each element is a single blue component.</span></span> <span data-ttu-id="2ee5e-144">Viene convertita in virgola mobile e assemblata in un elemento RGBA collegando 0,0 per Red e Green e 1,0 per Alpha.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-144">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="2ee5e-145">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="2ee5e-145">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="2ee5e-146"><dt>**\_alfa GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-146"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="2ee5e-147">Ogni elemento è un singolo componente rosso.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-147">Each element is a single red component.</span></span> <span data-ttu-id="2ee5e-148">Viene convertita in virgola mobile e assemblata in un elemento RGBA collegando 0,0 per rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-148">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="2ee5e-149">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="2ee5e-149">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                      |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="2ee5e-150"><dt>**GL \_ RGB**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-150"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="2ee5e-151">Ogni elemento è una tripla RGB.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-151">Each element is an RGB triple.</span></span> <span data-ttu-id="2ee5e-152">Viene convertita in virgola mobile e assemblata in un elemento RGBA collegando 1,0 per Alpha.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-152">It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="2ee5e-153">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="2ee5e-153">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="2ee5e-154"><dt>**\_RGBA GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-154"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="2ee5e-155">Ogni elemento è un elemento RGBA completo.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-155">Each element is a complete RGBA element.</span></span> <span data-ttu-id="2ee5e-156">Viene convertito in virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-156">It is converted to floating point.</span></span> <span data-ttu-id="2ee5e-157">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="2ee5e-157">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="2ee5e-158"><dt>**GL \_ BGR \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-158"><dt>**GL\_BGR\_EXT**</dt></span></span> </dl>                         | <span data-ttu-id="2ee5e-159">Ogni pixel è un gruppo di tre componenti in questo ordine: blu, verde, rosso.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-159">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="2ee5e-160">GL \_ BGR \_ ext fornisce un formato corrispondente al layout di memoria delle bitmap indipendenti dal dispositivo (DIB) Windows.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-160">GL\_BGR\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="2ee5e-161">In questo modo, le applicazioni possono usare gli stessi dati con le chiamate di funzione di Windows e le chiamate di funzione pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-161">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="2ee5e-162"><dt>**GL \_ BGRA \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-162"><dt>**GL\_BGRA\_EXT**</dt></span></span> </dl>                      | <span data-ttu-id="2ee5e-163">Ogni pixel è un gruppo di quattro componenti in questo ordine: blu, verde, rosso, alfa.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-163">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="2ee5e-164">GL \_ BGRA \_ ext fornisce un formato corrispondente al layout di memoria delle bitmap indipendenti dal dispositivo (DIB) Windows.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-164">GL\_BGRA\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="2ee5e-165">In questo modo, le applicazioni possono usare gli stessi dati con le chiamate di funzione di Windows e le chiamate di funzione pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-165">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="2ee5e-166"><dt>**\_luminanza GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-166"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="2ee5e-167">Ogni elemento è un singolo valore di luminosità.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-167">Each element is a single luminance value.</span></span> <span data-ttu-id="2ee5e-168">Viene convertita in virgola mobile e quindi assemblata in un elemento RGBA replicando il valore di luminanza tre volte per rosso, verde e blu e collegando 1,0 per alfa.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-168">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="2ee5e-169">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="2ee5e-169">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="2ee5e-170"><dt>**\_alfa luminanza GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-170"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="2ee5e-171">Ogni elemento è una coppia di luminanza/alfa.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-171">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="2ee5e-172">Viene convertita in virgola mobile e quindi assemblata in un elemento RGBA replicando il valore di luminanza tre volte per rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-172">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="2ee5e-173">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="2ee5e-173">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="2ee5e-174">*type*</span><span class="sxs-lookup"><span data-stu-id="2ee5e-174">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="2ee5e-175">Tipo di dati dei dati pixel.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-175">The data type of the pixel data.</span></span> <span data-ttu-id="2ee5e-176">Sono accettati i valori simbolici seguenti: GL \_ UNsigned \_ byte, GL \_ byte, GL \_ bitmap, GL \_ unsigned \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int e GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-176">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="2ee5e-177">*pixel*</span><span class="sxs-lookup"><span data-stu-id="2ee5e-177">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="2ee5e-178">Puntatore ai dati dell'immagine in memoria.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-178">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ee5e-179">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ee5e-179">Return value</span></span>

<span data-ttu-id="2ee5e-180">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-180">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2ee5e-181">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="2ee5e-181">Error codes</span></span>

<span data-ttu-id="2ee5e-182">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="2ee5e-182">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2ee5e-183">Nome</span><span class="sxs-lookup"><span data-stu-id="2ee5e-183">Name</span></span>                                                                                                  | <span data-ttu-id="2ee5e-184">Significato</span><span class="sxs-lookup"><span data-stu-id="2ee5e-184">Meaning</span></span>                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2ee5e-185"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-185"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="2ee5e-186">la *destinazione* non è una \_ trama GL.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-186">*target* was not an GL\_TEXTURE.</span></span><br/>                                                                                                                                                                                    |
| <dl> <span data-ttu-id="2ee5e-187"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-187"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="2ee5e-188">*Format* non è una costante di *formato* accettata.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-188">*format* was not an accepted *format* constant.</span></span> <span data-ttu-id="2ee5e-189">Vengono accettate solo le costanti di formato diverse da GL \_ stencil \_ index e GL \_ Depth \_ Component.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-189">Only format constants other than GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT are accepted.</span></span> <span data-ttu-id="2ee5e-190">Vedere la descrizione del parametro *Format* per un elenco di valori possibili.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-190">See the parameter description of *format* for a list of possible values.</span></span><br/> |
| <dl> <span data-ttu-id="2ee5e-191"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-191"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="2ee5e-192">il *tipo* non è una costante di *tipo* .</span><span class="sxs-lookup"><span data-stu-id="2ee5e-192">*type* was not a *type* constant.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="2ee5e-193"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-193"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="2ee5e-194">il *tipo* è una \_ bitmap GL e *Format* non è un indice di \_ colore GL \_ .</span><span class="sxs-lookup"><span data-stu-id="2ee5e-194">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                        |
| <dl> <span data-ttu-id="2ee5e-195"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-195"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="2ee5e-196">il *livello* è minore di zero o maggiore di log2 *Max*, dove *Max* è il valore restituito della \_ dimensione della trama GL Max \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2ee5e-196">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="2ee5e-197"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-197"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="2ee5e-198">*internalformat* è diverso da 1, 2, 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-198">*internalformat* was was not 1, 2, 3, or 4.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="2ee5e-199"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="2ee5e-200">*Width* è minore di zero o maggiore di 2 + GL \_ \_ dimensione della trama massima \_ oppure non può essere rappresentata come 2 *n* + 2 (bordo) per un valore integer pari a *n*.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-200">*width* was less than zero or greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or it could not be represented as 2 *n* + 2(border) for some integer value of *n*.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="2ee5e-201"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-201"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="2ee5e-202">il *bordo* non è 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-202">*border* was not 0 or 1.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="2ee5e-203"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-203"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2ee5e-204">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2ee5e-204">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                          |



## <a name="remarks"></a><span data-ttu-id="2ee5e-205">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ee5e-205">Remarks</span></span>

<span data-ttu-id="2ee5e-206">La funzione **glTexImage1D** specifica un'immagine di trama unidimensionale.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-206">The **glTexImage1D** function specifies a one-dimensional texture image.</span></span> <span data-ttu-id="2ee5e-207">Il texturing esegue il mapping di una parte di un' *immagine di trama* specificata a ogni primitiva grafica per cui è abilitata la funzionalità di texturing.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-207">Texturing maps a portion of a specified *texture image* onto each graphical primitive for which texturing is enabled.</span></span> <span data-ttu-id="2ee5e-208">Il texturing unidimensionale viene abilitato e disabilitato usando [**glEnable**](glenable.md) e **GLDISABLE** con argument GL \_ texture \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-208">One-dimensional texturing is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_TEXTURE\_1D.</span></span>

<span data-ttu-id="2ee5e-209">Le immagini di trama sono definite con **glTexImage1D**.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-209">Texture images are defined with **glTexImage1D**.</span></span> <span data-ttu-id="2ee5e-210">Gli argomenti descrivono i parametri dell'immagine di trama, ad esempio larghezza, larghezza del bordo, numero del livello di dettaglio (vedere [**glTexParameter**](gltexparameter-functions.md)) e numero di componenti colore specificati.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-210">The arguments describe the parameters of the texture image, such as width, width of the border, level-of-detail number (see [**glTexParameter**](gltexparameter-functions.md)), and number of color components provided.</span></span> <span data-ttu-id="2ee5e-211">Gli ultimi tre argomenti descrivono il modo in cui l'immagine viene rappresentata in memoria.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-211">The last three arguments describe the way the image is represented in memory.</span></span> <span data-ttu-id="2ee5e-212">Questi argomenti sono identici ai formati pixel utilizzati per [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="2ee5e-212">These arguments are identical to the pixel formats used for [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="2ee5e-213">I dati vengono letti da *pixel* come una sequenza di byte firmati o non firmati, Shorts o Long o valori a virgola mobile a precisione singola, a seconda del *tipo*.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-213">Data is read from *pixels* as a sequence of signed or unsigned bytes, shorts or longs, or single-precision floating-point values, depending on *type*.</span></span> <span data-ttu-id="2ee5e-214">Questi valori sono raggruppati in set di uno, due, tre o quattro valori, a seconda del *formato*, per formare elementi.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-214">These values are grouped into sets of one, two, three, or four values, depending on *format*, to form elements.</span></span> <span data-ttu-id="2ee5e-215">Se *Type* è \_ una bitmap GL, i dati vengono considerati come una stringa di byte senza segno (e *Format* deve essere un \_ Indice dei colori GL \_ ).</span><span class="sxs-lookup"><span data-stu-id="2ee5e-215">If *type* is GL\_BITMAP, the data is considered as a string of unsigned bytes (and *format* must be GL\_COLOR\_INDEX).</span></span> <span data-ttu-id="2ee5e-216">Ogni byte di dati viene considerato come elementi a 8 1 bit, con l'ordinamento dei bit determinato da GL \_ depack \_ LSB \_ First (vedere [**glPixelStore**](glpixelstore-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="2ee5e-216">Each data byte is treated as eight 1-bit elements, with bit ordering determined by GL\_UNPACK\_LSB\_FIRST (see [**glPixelStore**](glpixelstore-functions.md)).</span></span>

<span data-ttu-id="2ee5e-217">Un'immagine di trama può avere fino a quattro componenti per ogni elemento di trama, a seconda dei *componenti*.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-217">A texture image can have up to four components per texture element, depending on *components*.</span></span> <span data-ttu-id="2ee5e-218">Un'immagine di trama a un componente usa solo il componente rosso del colore RGBA Estratto da *pixel*.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-218">A one-component texture image uses only the red component of the RGBA color extracted from *pixels*.</span></span> <span data-ttu-id="2ee5e-219">Un'immagine a due componenti usa i valori R e.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-219">A two-component image uses the R and A values.</span></span> <span data-ttu-id="2ee5e-220">Un'immagine A tre componenti usa i valori R, G e B.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-220">A three-component image uses the R, G, and B values.</span></span> <span data-ttu-id="2ee5e-221">Un'immagine a quattro componenti utilizza tutti i componenti di RGBA.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-221">A four-component image uses all of the RGBA components.</span></span>

<span data-ttu-id="2ee5e-222">La texturing non ha alcun effetto sulla modalità di indicizzazione del colore.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-222">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="2ee5e-223">L'immagine di trama può essere rappresentata dagli stessi formati di dati dei pixel in un comando [**glDrawPixels**](gldrawpixels.md) , ad eccezione del fatto che \_ \_ \_ \_ non è possibile usare l'indice degli stencil GL e il componente di profondità GL.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-223">The texture image can be represented by the same data formats as the pixels in a [**glDrawPixels**](gldrawpixels.md) command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="2ee5e-224">Le modalità [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) influiscono sulle immagini della trama esattamente come influiscono su **glDrawPixels**.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-224">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="2ee5e-225">Un'immagine di trama con larghezza zero indica la trama null.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-225">A texture image with zero width indicates the null texture.</span></span> <span data-ttu-id="2ee5e-226">Se la trama null è specificata per il livello di dettaglio 0, è come se la texturing fosse disabilitata.</span><span class="sxs-lookup"><span data-stu-id="2ee5e-226">If the null texture is specified for level-of-detail 0, it is as if texturing were disabled.</span></span>

<span data-ttu-id="2ee5e-227">Le funzioni seguenti consentono di recuperare informazioni correlate a **glTexImageID**:</span><span class="sxs-lookup"><span data-stu-id="2ee5e-227">The following functions retrieve information related to **glTexImageID**:</span></span>

[<span data-ttu-id="2ee5e-228">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-228">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="2ee5e-229">[**glIsEnabled**](glisenabled.md) con argomento GL \_ texture \_ 1D</span><span class="sxs-lookup"><span data-stu-id="2ee5e-229">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="2ee5e-230">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ee5e-230">Requirements</span></span>



| <span data-ttu-id="2ee5e-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ee5e-231">Requirement</span></span> | <span data-ttu-id="2ee5e-232">Valore</span><span class="sxs-lookup"><span data-stu-id="2ee5e-232">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee5e-233">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ee5e-233">Minimum supported client</span></span><br/> | <span data-ttu-id="2ee5e-234">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2ee5e-234">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2ee5e-235">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ee5e-235">Minimum supported server</span></span><br/> | <span data-ttu-id="2ee5e-236">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2ee5e-236">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2ee5e-237">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ee5e-237">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ee5e-238"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-238"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2ee5e-239">Libreria</span><span class="sxs-lookup"><span data-stu-id="2ee5e-239">Library</span></span><br/>                  | <dl> <span data-ttu-id="2ee5e-240"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-240"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2ee5e-241">DLL</span><span class="sxs-lookup"><span data-stu-id="2ee5e-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ee5e-242"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ee5e-242"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ee5e-243">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ee5e-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ee5e-244">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-244">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-245">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-245">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-246">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-246">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-247">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-247">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-248">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-248">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-249">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-249">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-250">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-250">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-251">**Remo**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-251">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-252">**glFog**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-252">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-253">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-253">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-254">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-254">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-255">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-255">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-256">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-256">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-257">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-257">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-258">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-258">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-259">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-259">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-260">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-260">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-261">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-261">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="2ee5e-262">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="2ee5e-262">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 






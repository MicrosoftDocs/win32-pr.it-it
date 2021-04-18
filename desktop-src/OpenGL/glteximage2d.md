---
title: funzione glTexImage2D (GL. h)
description: La funzione glTexImage2D specifica un'immagine di trama bidimensionale.
ms.assetid: e8b9c692-5239-47de-86eb-80c247c60e1d
keywords:
- funzione glTexImage2D OpenGL
topic_type:
- apiref
api_name:
- glTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba2d5bc6f966d9b10c0dadccb221086e64de827
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302754"
---
# <a name="glteximage2d-function"></a><span data-ttu-id="a5d8f-104">glTexImage2D (funzione)</span><span class="sxs-lookup"><span data-stu-id="a5d8f-104">glTexImage2D function</span></span>

<span data-ttu-id="a5d8f-105">La funzione **glTexImage2D** specifica un'immagine di trama bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-105">The **glTexImage2D** function specifies a two-dimensional texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5d8f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5d8f-106">Syntax</span></span>


```C++
void WINAPI glTexImage2D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLsizei height,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="a5d8f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5d8f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5d8f-108">*target*</span><span class="sxs-lookup"><span data-stu-id="a5d8f-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="a5d8f-109">Trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-109">The target texture.</span></span> <span data-ttu-id="a5d8f-110">Deve essere di \_ trama GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-110">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="a5d8f-111">*level*</span><span class="sxs-lookup"><span data-stu-id="a5d8f-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="a5d8f-112">Numero del livello di dettaglio.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-112">The level-of-detail number.</span></span> <span data-ttu-id="a5d8f-113">Il livello 0 è il livello dell'immagine di base.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-113">Level 0 is the base image level.</span></span> <span data-ttu-id="a5d8f-114">Il livello *n* è l'immagine di riduzione del mipmap *n* .</span><span class="sxs-lookup"><span data-stu-id="a5d8f-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="a5d8f-115">*internalformat*</span><span class="sxs-lookup"><span data-stu-id="a5d8f-115">*internalformat*</span></span> 
</dt> <dd>

<span data-ttu-id="a5d8f-116">Numero di componenti di colore nella trama.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-116">The number of color components in the texture.</span></span> <span data-ttu-id="a5d8f-117">Deve essere 1, 2, 3 o 4 o una delle costanti simboliche seguenti: GL \_ Alpha, GL \_ ALPHA4, GL \_ ALPHA8, GL ALPHA12, GL ALPHA16, GL Luminance, GL LUMINANCE4, GL LUMINANCE8, GL LUMINANCE12, GL LUMINANCE16, GL \_ \_ \_ \_ \_ \_ \_ \_ Luminance \_ Alpha, GL \_ LUMINANCE4 \_ ALPHA4, GL \_ LUMINANCE6 \_ alfa2, GL LUMINANCE8 \_ \_ ALPHA8, GL \_ LUMINANCE12 ALPHA4, \_ GL \_ LUMINANCE12 \_ ALPHA12, GL LUMINANCE16 ALPHA16, GL Intensity, GL INTENSITY4, GL INTENSITY8, GL INTENSITY12, GL INTENSITY16, GL \_ \_ \_ \_ \_ \_ \_ \_ R3 \_ G3 \_ B2, GL \_ RGB, GL RGB4, \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ GL RGB5, GL RGB8, GL RGB10, GL RGB12, GL RGB16, GL RGBA, GL RGBA2, GL RGBA4, GL RGB5, GL Rgba8, GL RGB10, GL RGBA12, GL RGBA16, GL e GL.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-117">Must be 1, 2, 3, or 4, or one of the following symbolic constants: GL\_ALPHA, GL\_ALPHA4, GL\_ALPHA8, GL\_ALPHA12, GL\_ALPHA16, GL\_LUMINANCE, GL\_LUMINANCE4, GL\_LUMINANCE8, GL\_LUMINANCE12, GL\_LUMINANCE16, GL\_LUMINANCE\_ALPHA, GL\_LUMINANCE4\_ALPHA4, GL\_LUMINANCE6\_ALPHA2, GL\_LUMINANCE8\_ALPHA8, GL\_LUMINANCE12\_ALPHA4, GL\_LUMINANCE12\_ALPHA12, GL\_LUMINANCE16\_ALPHA16, GL\_INTENSITY, GL\_INTENSITY4, GL\_INTENSITY8, GL\_INTENSITY12, GL\_INTENSITY16, GL\_R3\_G3\_B2, GL\_RGB, GL\_RGB4, GL\_RGB5, GL\_RGB8, GL\_RGB10, GL\_RGB12, GL\_RGB16, GL\_RGBA, GL\_RGBA2, GL\_RGBA4, GL\_RGB5\_A1, GL\_RGBA8, GL\_RGB10\_A2, GL\_RGBA12, or GL\_RGBA16.</span></span>

</dd> <dt>

<span data-ttu-id="a5d8f-118">*width*</span><span class="sxs-lookup"><span data-stu-id="a5d8f-118">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="a5d8f-119">Larghezza dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-119">The width of the texture image.</span></span> <span data-ttu-id="a5d8f-120">Deve essere 2 *n* + 2 (*bordo*) per alcuni numeri interi *n*.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-120">Must be 2 *n* + 2(*border*) for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="a5d8f-121">*height*</span><span class="sxs-lookup"><span data-stu-id="a5d8f-121">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="a5d8f-122">Altezza dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-122">The height of the texture image.</span></span> <span data-ttu-id="a5d8f-123">Deve essere 2 *<sup>m</sup>* + 2 (*bordo*) per alcuni valori integer *m*.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-123">Must be 2 *<sup>m</sup>* + 2(*border*) for some integer *m*.</span></span>

</dd> <dt>

<span data-ttu-id="a5d8f-124">*bordo*</span><span class="sxs-lookup"><span data-stu-id="a5d8f-124">*border*</span></span> 
</dt> <dd>

<span data-ttu-id="a5d8f-125">Larghezza del bordo.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-125">The width of the border.</span></span> <span data-ttu-id="a5d8f-126">Deve essere 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-126">Must be either 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="a5d8f-127">*format*</span><span class="sxs-lookup"><span data-stu-id="a5d8f-127">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="a5d8f-128">Formato dei dati pixel.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-128">The format of the pixel data.</span></span> <span data-ttu-id="a5d8f-129">Può assumere uno dei nove valori simbolici.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-129">It can assume one of nine symbolic values.</span></span>



| <span data-ttu-id="a5d8f-130">Valore</span><span class="sxs-lookup"><span data-stu-id="a5d8f-130">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="a5d8f-131">Significato</span><span class="sxs-lookup"><span data-stu-id="a5d8f-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="a5d8f-132"><dt>**\_indice colori \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-132"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="a5d8f-133">Ogni elemento è un singolo valore, ovvero un indice colori.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-133">Each element is a single value, a color index.</span></span> <span data-ttu-id="a5d8f-134">Viene convertito in un punto fisso (con un numero non specificato di 0 bit a destra del punto binario), spostato verso sinistra o verso destra a seconda del valore e del segno dello spostamento di \_ indice GL \_ e aggiunto all'offset dell' \_ indice GL \_ (vedere [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="a5d8f-134">It is converted to fixed point (with an unspecified number of 0 bits to the right of the binary point), shifted left or right depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="a5d8f-135">L'indice risultante viene convertito in un set di componenti colore usando il \_ mapping GL pixel i \_ \_ \_ a \_ R, GL \_ pixel \_ Map \_ i \_ a \_ G, GL \_ pixel \_ Map \_ i \_ a \_ B e GL \_ pixel \_ mappa \_ i \_ a \_ una tabella e l'intervallo viene premuto nell'intervallo \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="a5d8f-135">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="a5d8f-136"><dt>**\_rosso GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-136"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="a5d8f-137">Ogni elemento è un singolo componente rosso.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-137">Each element is a single red component.</span></span> <span data-ttu-id="a5d8f-138">Viene convertita in virgola mobile e assemblata in un elemento RGBA collegando 0,0 per verde e blu e 1,0 per alfa.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-138">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="a5d8f-139">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="a5d8f-139">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                               |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="a5d8f-140"><dt>**\_verde GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-140"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="a5d8f-141">Ogni elemento è un singolo componente verde.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-141">Each element is a single green component.</span></span> <span data-ttu-id="a5d8f-142">Viene convertita in virgola mobile e assemblata in un elemento RGBA collegando 0,0 per Red e Blue e 1,0 per Alpha.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-142">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="a5d8f-143">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="a5d8f-143">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                        |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="a5d8f-144"><dt>**\_blu GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-144"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="a5d8f-145">Ogni elemento è un singolo componente blu.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-145">Each element is a single blue component.</span></span> <span data-ttu-id="a5d8f-146">Viene convertita in virgola mobile e assemblata in un elemento RGBA collegando 0,0 per Red e Green e 1,0 per Alpha.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-146">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="a5d8f-147">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="a5d8f-147">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                               |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="a5d8f-148"><dt>**\_alfa GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-148"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="a5d8f-149">Ogni elemento è un singolo componente rosso.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-149">Each element is a single red component.</span></span> <span data-ttu-id="a5d8f-150">Viene convertita in virgola mobile e assemblata in un elemento RGBA collegando 0,0 per rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-150">It is converted to floating point and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="a5d8f-151">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="a5d8f-151">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                     |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="a5d8f-152"><dt>**GL \_ RGB**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-152"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="a5d8f-153">Ogni elemento è una tripla RGB.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-153">Each element is an RGB triple.</span></span> <span data-ttu-id="a5d8f-154">Viene convertita in virgola mobile e assemblata in un elemento RGBA collegando 1,0 per Alpha.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-154">It is converted to floating point and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="a5d8f-155">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="a5d8f-155">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="a5d8f-156"><dt>**\_RGBA GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-156"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="a5d8f-157">Ogni elemento è un elemento RGBA completo.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-157">Each element is a complete RGBA element.</span></span> <span data-ttu-id="a5d8f-158">Viene convertito in virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-158">It is converted to floating point.</span></span> <span data-ttu-id="a5d8f-159">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="a5d8f-159">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="a5d8f-160"><dt>**GL \_ BGR \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-160"><dt>**GL\_BGR\_EXT**</dt></span></span> </dl>                         | <span data-ttu-id="a5d8f-161">Ogni pixel è un gruppo di tre componenti in questo ordine: blu, verde, rosso.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-161">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="a5d8f-162">GL \_ BGR \_ ext fornisce un formato corrispondente al layout di memoria delle bitmap indipendenti dal dispositivo (DIB) Windows.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-162">GL\_BGR\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="a5d8f-163">In questo modo, le applicazioni possono usare gli stessi dati con le chiamate di funzione di Windows e le chiamate di funzione pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-163">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="a5d8f-164"><dt>**GL \_ BGRA \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-164"><dt>**GL\_BGRA\_EXT**</dt></span></span> </dl>                      | <span data-ttu-id="a5d8f-165">Ogni pixel è un gruppo di quattro componenti in questo ordine: blu, verde, rosso, alfa.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-165">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span> <span data-ttu-id="a5d8f-166">GL \_ BGRA \_ ext fornisce un formato corrispondente al layout di memoria delle bitmap indipendenti dal dispositivo (DIB) Windows.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-166">GL\_BGRA\_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="a5d8f-167">In questo modo, le applicazioni possono usare gli stessi dati con le chiamate di funzione di Windows e le chiamate di funzione pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-167">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="a5d8f-168"><dt>**\_luminanza GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-168"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="a5d8f-169">Ogni elemento è un singolo valore di luminosità.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-169">Each element is a single luminance value.</span></span> <span data-ttu-id="a5d8f-170">Viene convertita in virgola mobile e quindi assemblata in un elemento RGBA replicando il valore di luminanza tre volte per rosso, verde e blu e collegando 1,0 per alfa.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-170">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="a5d8f-171">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="a5d8f-171">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                         |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="a5d8f-172"><dt>**\_alfa luminanza GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-172"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="a5d8f-173">Ogni elemento è una coppia di luminanza/alfa.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-173">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="a5d8f-174">Viene convertita in virgola mobile e quindi assemblata in un elemento RGBA replicando il valore di luminanza tre volte per rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-174">It is converted to floating point, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="a5d8f-175">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="a5d8f-175">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="a5d8f-176">*type*</span><span class="sxs-lookup"><span data-stu-id="a5d8f-176">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="a5d8f-177">Tipo di dati dei dati pixel.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-177">The data type of the pixel data.</span></span> <span data-ttu-id="a5d8f-178">Sono accettati i valori simbolici seguenti: GL \_ UNsigned \_ byte, GL \_ byte, GL \_ bitmap, GL \_ unsigned \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int e GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-178">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="a5d8f-179">*pixel*</span><span class="sxs-lookup"><span data-stu-id="a5d8f-179">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="a5d8f-180">Puntatore ai dati dell'immagine in memoria.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-180">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5d8f-181">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5d8f-181">Return value</span></span>

<span data-ttu-id="a5d8f-182">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-182">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a5d8f-183">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a5d8f-183">Error codes</span></span>

<span data-ttu-id="a5d8f-184">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="a5d8f-184">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a5d8f-185">Nome</span><span class="sxs-lookup"><span data-stu-id="a5d8f-185">Name</span></span>                                                                                                  | <span data-ttu-id="a5d8f-186">Significato</span><span class="sxs-lookup"><span data-stu-id="a5d8f-186">Meaning</span></span>                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a5d8f-187"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-187"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="a5d8f-188">la *destinazione* non è un valore \_ 2D di trama GL \_ .</span><span class="sxs-lookup"><span data-stu-id="a5d8f-188">*target* was not an GL\_TEXTURE\_2D.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="a5d8f-189"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-189"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="a5d8f-190">*Format* non è una costante di *formato* accettata.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-190">*format* was not an accepted *format* constant.</span></span> <span data-ttu-id="a5d8f-191">Vengono accettate solo le costanti di formato diverse da GL \_ stencil \_ index e GL \_ Depth \_ Component.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-191">Only format constants other than GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT are accepted.</span></span> <span data-ttu-id="a5d8f-192">Vedere la descrizione del parametro *Format* per un elenco di valori possibili.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-192">See the parameter description of *format* for a list of possible values.</span></span><br/> |
| <dl> <span data-ttu-id="a5d8f-193"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-193"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="a5d8f-194">il *tipo* non è una costante di *tipo* .</span><span class="sxs-lookup"><span data-stu-id="a5d8f-194">*type* was not a *type* constant.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="a5d8f-195"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-195"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="a5d8f-196">il *tipo* è una \_ bitmap GL e *Format* non è un indice di \_ colore GL \_ .</span><span class="sxs-lookup"><span data-stu-id="a5d8f-196">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                        |
| <dl> <span data-ttu-id="a5d8f-197"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-197"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a5d8f-198">il *livello* è minore di zero o maggiore di log2 *Max*, dove *Max* è il valore restituito della \_ dimensione della trama GL Max \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a5d8f-198">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="a5d8f-199"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a5d8f-200">*internalformat* è diverso da 1, 2, 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-200">*internalformat* was was not 1, 2, 3, or 4.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="a5d8f-201"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-201"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a5d8f-202">la *larghezza* o l'altezza è minore di zero o maggiore di 2 + GL \_ dimensione massima della \_ trama \_ oppure non può essere rappresentata come 2 *n* + 2 (bordo) per un valore integer pari a *n*.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-202">*width* or height was less than zero or greater than 2 + GL\_MAX\_TEXTURE\_SIZE, or it could not be represented as 2 *n* + 2(border) for some integer value of *n*.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="a5d8f-203"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-203"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a5d8f-204">il *bordo* non è 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-204">*border* was not 0 or 1.</span></span><br/>                                                                                                                                                                                            |
| <dl> <span data-ttu-id="a5d8f-205"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-205"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a5d8f-206">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a5d8f-206">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                          |



## <a name="remarks"></a><span data-ttu-id="a5d8f-207">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5d8f-207">Remarks</span></span>

<span data-ttu-id="a5d8f-208">La funzione **glTexImage2D** specifica un'immagine di trama bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-208">The **glTexImage2D** function specifies a two-dimensional texture image.</span></span> <span data-ttu-id="a5d8f-209">Il texturing esegue il mapping di una parte di un' *immagine di trama* specificata a ogni primitiva grafica per cui è abilitata la funzionalità di texturing.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-209">Texturing maps a portion of a specified *texture image* onto each graphical primitive for which texturing is enabled.</span></span> <span data-ttu-id="a5d8f-210">Il texturing bidimensionale viene abilitato e disabilitato usando [**glEnable**](glenable.md) e **GLDISABLE** con argument GL \_ texture \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-210">Two-dimensional texturing is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_TEXTURE\_2D.</span></span>

<span data-ttu-id="a5d8f-211">Le immagini di trama sono definite con **glTexImage2D**.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-211">Texture images are defined with **glTexImage2D**.</span></span> <span data-ttu-id="a5d8f-212">Gli argomenti descrivono i parametri dell'immagine di trama, ad esempio altezza, larghezza, larghezza del bordo, numero del livello di dettaglio (vedere [**glTexParameter**](gltexparameter-functions.md)) e numero di componenti colore specificati.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-212">The arguments describe the parameters of the texture image, such as height, width, width of the border, level-of-detail number (see [**glTexParameter**](gltexparameter-functions.md)), and number of color components provided.</span></span> <span data-ttu-id="a5d8f-213">Gli ultimi tre argomenti descrivono il modo in cui l'immagine viene rappresentata in memoria.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-213">The last three arguments describe the way the image is represented in memory.</span></span> <span data-ttu-id="a5d8f-214">Questi argomenti sono identici ai formati pixel utilizzati per [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="a5d8f-214">These arguments are identical to the pixel formats used for [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="a5d8f-215">I dati vengono letti da *pixel* come una sequenza di byte firmati o non firmati, Shorts o Long o valori a virgola mobile a precisione singola, a seconda del *tipo*.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-215">Data is read from *pixels* as a sequence of signed or unsigned bytes, shorts or longs, or single-precision floating-point values, depending on *type*.</span></span> <span data-ttu-id="a5d8f-216">Questi valori sono raggruppati in set di uno, due, tre o quattro valori, a seconda del *formato*, per formare elementi.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-216">These values are grouped into sets of one, two, three, or four values, depending on *format*, to form elements.</span></span> <span data-ttu-id="a5d8f-217">Se *Type* è \_ una bitmap GL, i dati vengono considerati come una stringa di byte senza segno (e *Format* deve essere un \_ Indice dei colori GL \_ ).</span><span class="sxs-lookup"><span data-stu-id="a5d8f-217">If *type* is GL\_BITMAP, the data is considered as a string of unsigned bytes (and *format* must be GL\_COLOR\_INDEX).</span></span> <span data-ttu-id="a5d8f-218">Ogni byte di dati viene considerato come elementi a 8 1 bit, con l'ordinamento dei bit determinato da GL \_ depack \_ LSB \_ First (vedere [**glPixelStore**](glpixelstore-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="a5d8f-218">Each data byte is treated as eight 1-bit elements, with bit ordering determined by GL\_UNPACK\_LSB\_FIRST (see [**glPixelStore**](glpixelstore-functions.md)).</span></span> <span data-ttu-id="a5d8f-219">Per una descrizione dei valori accettabili per il parametro di *tipo* , vedere [**glDrawPixels**](gldrawpixels.md) .</span><span class="sxs-lookup"><span data-stu-id="a5d8f-219">Please see [**glDrawPixels**](gldrawpixels.md) for a description of the acceptable values for the *type* parameter.</span></span>

<span data-ttu-id="a5d8f-220">Un'immagine di trama può avere fino a quattro componenti per ogni elemento di trama, a seconda dei *componenti*.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-220">A texture image can have up to four components per texture element, depending on *components*.</span></span> <span data-ttu-id="a5d8f-221">Un'immagine di trama a un componente usa solo il componente rosso del colore RGBA Estratto da *pixel*.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-221">A one-component texture image uses only the red component of the RGBA color extracted from *pixels*.</span></span> <span data-ttu-id="a5d8f-222">Un'immagine a due componenti usa i valori R e.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-222">A two-component image uses the R and A values.</span></span> <span data-ttu-id="a5d8f-223">Un'immagine A tre componenti usa i valori R, G e B.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-223">A three-component image uses the R, G, and B values.</span></span> <span data-ttu-id="a5d8f-224">Un'immagine a quattro componenti utilizza tutti i componenti di RGBA.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-224">A four-component image uses all of the RGBA components.</span></span>

<span data-ttu-id="a5d8f-225">La texturing non ha alcun effetto sulla modalità di indicizzazione del colore.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-225">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="a5d8f-226">L'immagine di trama può essere rappresentata dagli stessi formati di dati dei pixel in un comando **glDrawPixels** , ad eccezione del fatto che \_ \_ \_ \_ non è possibile usare l'indice degli stencil GL e il componente di profondità GL.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-226">The texture image can be represented by the same data formats as the pixels in a **glDrawPixels** command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="a5d8f-227">Le modalità [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) influiscono sulle immagini della trama esattamente come influiscono su **glDrawPixels**.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-227">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="a5d8f-228">Un'immagine di trama con altezza o larghezza zero indica la trama null.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-228">A texture image with zero height or width indicates the null texture.</span></span> <span data-ttu-id="a5d8f-229">Se la trama null è specificata per il livello di dettaglio 0, è come se la texturing fosse disabilitata.</span><span class="sxs-lookup"><span data-stu-id="a5d8f-229">If the null texture is specified for level-of-detail 0, it is as if texturing were disabled.</span></span>

<span data-ttu-id="a5d8f-230">Le funzioni seguenti consentono di recuperare informazioni correlate a **glTexImage2D**:</span><span class="sxs-lookup"><span data-stu-id="a5d8f-230">The following functions retrieve information related to **glTexImage2D**:</span></span>

[<span data-ttu-id="a5d8f-231">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="a5d8f-231">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="a5d8f-232">[**glIsEnabled**](glisenabled.md) con argomento di \_ trama GL \_ 2D</span><span class="sxs-lookup"><span data-stu-id="a5d8f-232">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="a5d8f-233">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5d8f-233">Requirements</span></span>



| <span data-ttu-id="a5d8f-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5d8f-234">Requirement</span></span> | <span data-ttu-id="a5d8f-235">Valore</span><span class="sxs-lookup"><span data-stu-id="a5d8f-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d8f-236">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5d8f-236">Minimum supported client</span></span><br/> | <span data-ttu-id="a5d8f-237">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a5d8f-237">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a5d8f-238">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5d8f-238">Minimum supported server</span></span><br/> | <span data-ttu-id="a5d8f-239">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a5d8f-239">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a5d8f-240">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5d8f-240">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5d8f-241"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-241"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a5d8f-242">Libreria</span><span class="sxs-lookup"><span data-stu-id="a5d8f-242">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5d8f-243"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-243"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a5d8f-244">DLL</span><span class="sxs-lookup"><span data-stu-id="a5d8f-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5d8f-245"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5d8f-245"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5d8f-246">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5d8f-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5d8f-247">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a5d8f-247">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a5d8f-248">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="a5d8f-248">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="a5d8f-249">**Remo**</span><span class="sxs-lookup"><span data-stu-id="a5d8f-249">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a5d8f-250">**glFog**</span><span class="sxs-lookup"><span data-stu-id="a5d8f-250">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="a5d8f-251">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="a5d8f-251">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="a5d8f-252">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="a5d8f-252">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="a5d8f-253">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="a5d8f-253">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="a5d8f-254">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="a5d8f-254">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="a5d8f-255">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="a5d8f-255">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="a5d8f-256">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="a5d8f-256">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="a5d8f-257">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="a5d8f-257">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 






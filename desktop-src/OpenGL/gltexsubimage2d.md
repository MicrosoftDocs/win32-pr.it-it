---
title: funzione glTexSubImage2D (GL. h)
description: La funzione glTexSubImage2D specifica una parte di un'immagine di trama unidimensionale esistente. Non è possibile definire una nuova trama con glTexSubImage2D.
ms.assetid: 2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7
keywords:
- funzione glTexSubImage2D OpenGL
topic_type:
- apiref
api_name:
- glTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a0a59ae9e6724386cb2f7891a14e4bf9d4c1a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300953"
---
# <a name="gltexsubimage2d-function"></a><span data-ttu-id="ab5a5-105">glTexSubImage2D (funzione)</span><span class="sxs-lookup"><span data-stu-id="ab5a5-105">glTexSubImage2D function</span></span>

<span data-ttu-id="ab5a5-106">La funzione **glTexSubImage2D** specifica una parte di un'immagine di trama unidimensionale esistente.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-106">The **glTexSubImage2D** function specifies a portion of an existing one-dimensional texture image.</span></span> <span data-ttu-id="ab5a5-107">Non è possibile definire una nuova trama con **glTexSubImage2D**.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-107">You cannot define a new texture with **glTexSubImage2D**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab5a5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab5a5-108">Syntax</span></span>


```C++
void WINAPI glTexSubImage2D(
         GLenum  target,
         GLint   level,
         GLint   xoffset,
         GLint   yoffset,
         GLsizei width,
         GLsizei height,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="ab5a5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab5a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab5a5-110">*target*</span><span class="sxs-lookup"><span data-stu-id="ab5a5-110">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="ab5a5-111">Trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-111">The target texture.</span></span> <span data-ttu-id="ab5a5-112">Deve essere di \_ trama GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-112">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a5-113">*level*</span><span class="sxs-lookup"><span data-stu-id="ab5a5-113">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="ab5a5-114">Numero del livello di dettaglio.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-114">The level-of-detail number.</span></span> <span data-ttu-id="ab5a5-115">Il livello 0 è l'immagine di base.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-115">Level 0 is the base image.</span></span> <span data-ttu-id="ab5a5-116">Il livello *n* è l'immagine di riduzione del mipmap *n*.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-116">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a5-117">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="ab5a5-117">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="ab5a5-118">Offset di Texel nella direzione *x* all'interno della matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-118">A texel offset in the *x* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a5-119">*yoffset*</span><span class="sxs-lookup"><span data-stu-id="ab5a5-119">*yoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="ab5a5-120">Offset di Texel nella direzione *y* all'interno della matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-120">A texel offset in the *y* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a5-121">*width*</span><span class="sxs-lookup"><span data-stu-id="ab5a5-121">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="ab5a5-122">Larghezza dell'immagine secondaria della trama.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-122">The width of the texture sub-image.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a5-123">*height*</span><span class="sxs-lookup"><span data-stu-id="ab5a5-123">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="ab5a5-124">Altezza dell'immagine secondaria della trama.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-124">The height of the texture sub-image.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a5-125">*format*</span><span class="sxs-lookup"><span data-stu-id="ab5a5-125">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="ab5a5-126">Formato dei dati pixel.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-126">The format of the pixel data.</span></span> <span data-ttu-id="ab5a5-127">Può assumere uno dei seguenti valori simbolici.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-127">It can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="ab5a5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ab5a5-128">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="ab5a5-129">Significato</span><span class="sxs-lookup"><span data-stu-id="ab5a5-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <span data-ttu-id="ab5a5-130"><dt>**\_indice colori \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-130"><dt>**GL\_COLOR\_INDEX**</dt></span></span> </dl>             | <span data-ttu-id="ab5a5-131">Ogni elemento è un singolo valore, ovvero un indice colori.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-131">Each element is a single value, a color index.</span></span> <span data-ttu-id="ab5a5-132">Viene convertito in un formato a virgola fissa (con un numero non specificato di 0 bit a destra del punto binario), spostato a sinistra o a destra, a seconda del valore e del segno dello \_ spostamento di indice GL \_ e aggiunto all' \_ offset dell'indice GL \_ (vedere [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="ab5a5-132">It is converted to fixed point format (with an unspecified number of 0 bits to the right of the binary point), shifted left or right, depending on the value and sign of GL\_INDEX\_SHIFT, and added to GL\_INDEX\_OFFSET (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span> <span data-ttu-id="ab5a5-133">L'indice risultante viene convertito in un set di componenti colore usando il \_ mapping GL pixel i \_ \_ \_ a \_ R, GL \_ pixel \_ Map \_ i \_ a \_ G, GL \_ pixel \_ Map \_ i \_ a \_ B e GL \_ pixel \_ mappa \_ i \_ a \_ una tabella e l'intervallo viene premuto nell'intervallo \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="ab5a5-133">The resulting index is converted to a set of color components using the GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, and GL\_PIXEL\_MAP\_I\_TO\_A tables, and clamped to the range \[0,1\].</span></span><br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="ab5a5-134"><dt>**\_rosso GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-134"><dt>**GL\_RED**</dt></span></span> </dl>                                      | <span data-ttu-id="ab5a5-135">Ogni elemento è un singolo componente rosso.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-135">Each element is a single red component.</span></span> <span data-ttu-id="ab5a5-136">Viene convertita in formato a virgola mobile e assemblata in un elemento RGBA collegando 0,0 per verde e blu e 1,0 per alfa.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-136">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for green and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="ab5a5-137">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="ab5a5-137">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="ab5a5-138"><dt>**\_verde GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-138"><dt>**GL\_GREEN**</dt></span></span> </dl>                                | <span data-ttu-id="ab5a5-139">Ogni elemento è un singolo componente verde.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-139">Each element is a single green component.</span></span> <span data-ttu-id="ab5a5-140">Viene convertita in formato a virgola mobile e assemblata in un elemento RGBA collegando 0,0 per Red e Blue e 1,0 per Alpha.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-140">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and blue, and 1.0 for alpha.</span></span> <span data-ttu-id="ab5a5-141">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="ab5a5-141">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="ab5a5-142"><dt>**\_blu GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-142"><dt>**GL\_BLUE**</dt></span></span> </dl>                                   | <span data-ttu-id="ab5a5-143">Ogni elemento è un singolo componente blu.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-143">Each element is a single blue component.</span></span> <span data-ttu-id="ab5a5-144">Viene convertita nel formato a virgola mobile e assemblata in un elemento RGBA collegando 0,0 per il rosso e il verde e 1,0 per Alpha.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-144">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red and green, and 1.0 for alpha.</span></span> <span data-ttu-id="ab5a5-145">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="ab5a5-145">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="ab5a5-146"><dt>**\_alfa GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-146"><dt>**GL\_ALPHA**</dt></span></span> </dl>                                | <span data-ttu-id="ab5a5-147">Ogni elemento è un singolo componente alfa.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-147">Each element is a single alpha component.</span></span> <span data-ttu-id="ab5a5-148">Viene convertita in formato a virgola mobile e assemblata in un elemento RGBA collegando 0,0 per rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-148">It is converted to floating point format and assembled into an RGBA element by attaching 0.0 for red, green, and blue.</span></span> <span data-ttu-id="ab5a5-149">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="ab5a5-149">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="ab5a5-150"><dt>**GL \_ RGB**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-150"><dt>**GL\_RGB**</dt></span></span> </dl>                                      | <span data-ttu-id="ab5a5-151">Ogni elemento è una tripla RGB.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-151">Each element is an RGB triple.</span></span> <span data-ttu-id="ab5a5-152">Viene convertita nel formato a virgola mobile e assemblata in un elemento RGBA collegando 1,0 per Alpha.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-152">It is converted to floating point format and assembled into an RGBA element by attaching 1.0 for alpha.</span></span> <span data-ttu-id="ab5a5-153">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="ab5a5-153">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="ab5a5-154"><dt>**\_RGBA GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-154"><dt>**GL\_RGBA**</dt></span></span> </dl>                                   | <span data-ttu-id="ab5a5-155">Ogni elemento è un elemento RGBA completo.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-155">Each element is a complete RGBA element.</span></span> <span data-ttu-id="ab5a5-156">Viene convertito in virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-156">It is converted to floating point.</span></span> <span data-ttu-id="ab5a5-157">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="ab5a5-157">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <span data-ttu-id="ab5a5-158"><dt>**\_luminanza GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-158"><dt>**GL\_LUMINANCE**</dt></span></span> </dl>                    | <span data-ttu-id="ab5a5-159">Ogni elemento è un singolo valore di luminosità.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-159">Each element is a single luminance value.</span></span> <span data-ttu-id="ab5a5-160">Viene convertita in formato a virgola mobile e quindi assemblata in un elemento RGBA replicando il valore di luminanza tre volte per rosso, verde e blu e collegando 1,0 per alfa.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-160">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue, and attaching 1.0 for alpha.</span></span> <span data-ttu-id="ab5a5-161">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere [**glPixelTransfer**](glpixeltransfer.md)).</span><span class="sxs-lookup"><span data-stu-id="ab5a5-161">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see [**glPixelTransfer**](glpixeltransfer.md)).</span></span><br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <span data-ttu-id="ab5a5-162"><dt>**\_alfa luminanza GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-162"><dt>**GL\_LUMINANCE\_ALPHA**</dt></span></span> </dl> | <span data-ttu-id="ab5a5-163">Ogni elemento è una coppia di luminanza/alfa.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-163">Each element is a luminance/alpha pair.</span></span> <span data-ttu-id="ab5a5-164">Viene convertita in formato a virgola mobile e quindi assemblata in un elemento RGBA replicando il valore di luminanza tre volte per rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-164">It is converted to floating point format, and then assembled into an RGBA element by replicating the luminance value three times for red, green, and blue.</span></span> <span data-ttu-id="ab5a5-165">Ogni componente viene quindi moltiplicato per la scala con segno di scala GL \_ c \_ , aggiunta alla distorsione GL c della distorsione firmata \_ \_ e fissata all'intervallo \[ 0, 1 \] (vedere **glPixelTransfer**).</span><span class="sxs-lookup"><span data-stu-id="ab5a5-165">Each component is then multiplied by the signed scale factor GL\_c\_SCALE, added to the signed bias GL\_c\_BIAS, and clamped to the range \[0,1\] (see **glPixelTransfer**).</span></span><br/>                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="ab5a5-166">*type*</span><span class="sxs-lookup"><span data-stu-id="ab5a5-166">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="ab5a5-167">Tipo di dati dei dati pixel.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-167">The data type of the pixel data.</span></span> <span data-ttu-id="ab5a5-168">Sono accettati i valori simbolici seguenti: GL \_ UNsigned \_ byte, GL \_ byte, GL \_ bitmap, GL \_ unsigned \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int e GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-168">The following symbolic values are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a5-169">*pixel*</span><span class="sxs-lookup"><span data-stu-id="ab5a5-169">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="ab5a5-170">Puntatore ai dati dell'immagine in memoria.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-170">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab5a5-171">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab5a5-171">Return value</span></span>

<span data-ttu-id="ab5a5-172">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-172">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ab5a5-173">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ab5a5-173">Error codes</span></span>

<span data-ttu-id="ab5a5-174">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ab5a5-174">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ab5a5-175">Nome</span><span class="sxs-lookup"><span data-stu-id="ab5a5-175">Name</span></span>                                                                                                  | <span data-ttu-id="ab5a5-176">Significato</span><span class="sxs-lookup"><span data-stu-id="ab5a5-176">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ab5a5-177"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-177"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="ab5a5-178">la *destinazione* non è la \_ trama GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-178">*target* was not GL\_TEXTURE\_2D.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="ab5a5-179"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-179"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="ab5a5-180">*Format* non è una costante accettata.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-180">*format* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="ab5a5-181"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-181"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="ab5a5-182">il *tipo* non è una costante accettata.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-182">*type* was not an accepted constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="ab5a5-183"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-183"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="ab5a5-184">il *tipo* è una \_ bitmap GL e *Format* non è un indice di \_ colore GL \_ .</span><span class="sxs-lookup"><span data-stu-id="ab5a5-184">*type* was GL\_BITMAP and *format* was not GL\_COLOR\_INDEX.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="ab5a5-185"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-185"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="ab5a5-186">il *livello* è minore di zero o maggiore di log2 *Max*, dove *Max* è il valore restituito della \_ dimensione della trama GL Max \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ab5a5-186">*level* was less than zero or greater than log2 *max*, where *max* was the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="ab5a5-187"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-187"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="ab5a5-188">*xoffset* è minore di-*b*; la   +  *larghezza* xoffset è maggiore di *w*  -  *b* oppure *yoffset* è minore di-*b* oppure l'   +  *altezza* di yoffset è maggiore di *h*  -  *b*, dove *w* è la \_ larghezza della trama GL \_ , *h* è l' \_ altezza della trama GL \_ e *b* è la larghezza del bordo della \_ trama GL \_ dell'immagine della trama da modificare.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-188">*xoffset* was less than -*b*; or *xoffset* + *width* was greater than *w* - *b*; or *yoffset* was less than -*b*; or *yoffset* + *height* was greater than *h* - *b*, where *w* is the GL\_TEXTURE\_WIDTH, *h* is the GL\_TEXTURE\_HEIGHT, and *b* is the width of the GL\_TEXTURE\_BORDER of the texture image being modified.</span></span> <br/> <span data-ttu-id="ab5a5-189">Si noti che *w* e *h* includono due volte lo spessore del bordo.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-189">Note that *w* and *h* include twice the border width.</span></span><br/> |
| <dl> <span data-ttu-id="ab5a5-190"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-190"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="ab5a5-191">*Width* era minore di *b*, dove *b* è lo spessore del bordo della matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-191">*width* was was less than *b*, where *b* is the border width of the texture array.</span></span><br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="ab5a5-192"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-192"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="ab5a5-193">il *bordo* non è zero o 1.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-193">*border* was not zero or 1.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="ab5a5-194"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-194"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ab5a5-195">La matrice di trama non è stata definita da un'operazione **glTexImage2D** precedente.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-195">The texture array was not defined by a previous **glTexImage2D** operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="ab5a5-196"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-196"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ab5a5-197">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ab5a5-197">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                                                                                                                                                                                                        |



## <a name="remarks"></a><span data-ttu-id="ab5a5-198">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab5a5-198">Remarks</span></span>

<span data-ttu-id="ab5a5-199">Il texturing bidimensionale per una primitiva viene abilitato con [**glEnable**](glenable.md) e **glDisable** con l'argomento di \_ trama GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-199">Two-dimensional texturing for a primitive is enabled using [**glEnable**](glenable.md) and **glDisable** with the argument GL\_TEXTURE\_2D.</span></span> <span data-ttu-id="ab5a5-200">Durante la texturing, una parte di un'immagine di trama specificata viene mappata in ogni primitiva abilitata.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-200">During texturing, part of a specified texture image is mapped into each enabled primitive.</span></span> <span data-ttu-id="ab5a5-201">Usare la funzione **glTexSubImage2D** per specificare un'immagine secondaria contigua di un'immagine di trama bidimensionale esistente per la texturing.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-201">You use the **glTexSubImage2D** function to specify a contiguous sub-image of an existing two-dimensional texture image for texturing.</span></span>

<span data-ttu-id="ab5a5-202">I Texel a cui fanno riferimento i *pixel* sostituiscono un'area della matrice di trama esistente con gli indici *x* di *xoffset* e *xoffset* + (*Width* 1) inclusivi e gli indici *y* di *yoffset* e *yoffset* + (*Height* 1) inclusi.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-202">The texels referenced by *pixels* replace a region of the existing texture array with *x* indexes of *xoffset* and *xoffset* + (*width* 1) inclusive and *y* indexes of *yoffset* and *yoffset* + (*height* 1) inclusive.</span></span> <span data-ttu-id="ab5a5-203">Questa area non può includere Texel non compresi nell'intervallo della matrice di trama originariamente specificata.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-203">This region cannot include any texels outside the range of the originally specified texture array.</span></span>

<span data-ttu-id="ab5a5-204">La specifica di un'immagine secondaria con una *larghezza* pari a zero non ha alcun effetto e non genera un errore.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-204">Specifying a sub-image with a *width* of zero has no effect and does not generate an error.</span></span>

<span data-ttu-id="ab5a5-205">La texturing non ha alcun effetto sulla modalità di indicizzazione del colore.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-205">Texturing has no effect in color-index mode.</span></span>

<span data-ttu-id="ab5a5-206">In generale, le immagini di trama possono essere rappresentate dagli stessi formati di dati dei pixel in un comando [**glDrawPixels**](gldrawpixels.md) , ad eccezione del fatto che \_ \_ \_ \_ non è possibile usare l'indice degli stencil GL e il componente profondità GL.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-206">In general, texture images can be represented by the same data formats as the pixels in a [**glDrawPixels**](gldrawpixels.md) command, except that GL\_STENCIL\_INDEX and GL\_DEPTH\_COMPONENT cannot be used.</span></span> <span data-ttu-id="ab5a5-207">Le modalità [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) influiscono sulle immagini della trama esattamente come influiscono su **glDrawPixels**.</span><span class="sxs-lookup"><span data-stu-id="ab5a5-207">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) modes affect texture images in exactly the way they affect **glDrawPixels**.</span></span>

<span data-ttu-id="ab5a5-208">Le funzioni seguenti consentono di recuperare informazioni correlate a **glTexSubImage2D**:</span><span class="sxs-lookup"><span data-stu-id="ab5a5-208">The following functions retrieve information related to **glTexSubImage2D**:</span></span>

[<span data-ttu-id="ab5a5-209">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-209">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="ab5a5-210">[**glIsEnabled**](glisenabled.md) con argomento di \_ trama GL \_ 2D</span><span class="sxs-lookup"><span data-stu-id="ab5a5-210">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="ab5a5-211">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab5a5-211">Requirements</span></span>



| <span data-ttu-id="ab5a5-212">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab5a5-212">Requirement</span></span> | <span data-ttu-id="ab5a5-213">Valore</span><span class="sxs-lookup"><span data-stu-id="ab5a5-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab5a5-214">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab5a5-214">Minimum supported client</span></span><br/> | <span data-ttu-id="ab5a5-215">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ab5a5-215">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ab5a5-216">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab5a5-216">Minimum supported server</span></span><br/> | <span data-ttu-id="ab5a5-217">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ab5a5-217">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ab5a5-218">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab5a5-218">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab5a5-219"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-219"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ab5a5-220">Libreria</span><span class="sxs-lookup"><span data-stu-id="ab5a5-220">Library</span></span><br/>                  | <dl> <span data-ttu-id="ab5a5-221"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-221"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ab5a5-222">DLL</span><span class="sxs-lookup"><span data-stu-id="ab5a5-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab5a5-223"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a5-223"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab5a5-224">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab5a5-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab5a5-225">**glCopyTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-225">**glCopyTexImage1D**</span></span>](glcopyteximage1d.md)
</dt> <dt>

[<span data-ttu-id="ab5a5-226">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-226">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="ab5a5-227">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-227">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="ab5a5-228">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-228">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="ab5a5-229">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-229">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="ab5a5-230">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-230">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="ab5a5-231">**glFog**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-231">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="ab5a5-232">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-232">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="ab5a5-233">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-233">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="ab5a5-234">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-234">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="ab5a5-235">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-235">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="ab5a5-236">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-236">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="ab5a5-237">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-237">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="ab5a5-238">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-238">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="ab5a5-239">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-239">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="ab5a5-240">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-240">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="ab5a5-241">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-241">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="ab5a5-242">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="ab5a5-242">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 






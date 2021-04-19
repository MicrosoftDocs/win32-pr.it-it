---
title: funzione glPixelMapfv (GL. h)
description: La funzione glPixelMapfv imposta le mappe di trasferimento dei pixel.
ms.assetid: 13403243-1ec4-4b1d-a9da-9a6693b6f9b8
keywords:
- funzione glPixelMapfv OpenGL
topic_type:
- apiref
api_name:
- glPixelMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97124eeca8051ec23d9a4fea03a98468d320af8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302708"
---
# <a name="glpixelmapfv-function"></a><span data-ttu-id="36948-104">glPixelMapfv (funzione)</span><span class="sxs-lookup"><span data-stu-id="36948-104">glPixelMapfv function</span></span>

<span data-ttu-id="36948-105">La funzione **glPixelMapfv** imposta le mappe di trasferimento dei pixel.</span><span class="sxs-lookup"><span data-stu-id="36948-105">The **glPixelMapfv** function sets up pixel transfer maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="36948-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36948-106">Syntax</span></span>


```C++
void WINAPI glPixelMapfv(
         GLenum  map,
         GLsizei mapsize,
   const GLfloat *values
);
```



## <a name="parameters"></a><span data-ttu-id="36948-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="36948-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36948-108">*map*</span><span class="sxs-lookup"><span data-stu-id="36948-108">*map*</span></span> 
</dt> <dd>

<span data-ttu-id="36948-109">Nome di mappa simbolico.</span><span class="sxs-lookup"><span data-stu-id="36948-109">A symbolic map name.</span></span> <span data-ttu-id="36948-110">Le dieci mappe sono le seguenti.</span><span class="sxs-lookup"><span data-stu-id="36948-110">The ten maps are as follows.</span></span>



| <span data-ttu-id="36948-111">Valore</span><span class="sxs-lookup"><span data-stu-id="36948-111">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="36948-112">Significato</span><span class="sxs-lookup"><span data-stu-id="36948-112">Meaning</span></span>                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <span data-ttu-id="36948-113"><dt>**\_mappa GL \_ pixel \_ i \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="36948-113"><dt>**GL\_PIXEL\_MAP\_I\_TO\_I**</dt></span></span> </dl> | <span data-ttu-id="36948-114">Esegue il mapping degli indici colore agli indici colori.</span><span class="sxs-lookup"><span data-stu-id="36948-114">Maps color indexes to color indexes.</span></span><br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <span data-ttu-id="36948-115"><dt>**\_mapping GL \_ pixel \_ \_ a \_ s**</dt></span><span class="sxs-lookup"><span data-stu-id="36948-115"><dt>**GL\_PIXEL\_MAP\_S\_TO\_S**</dt></span></span> </dl> | <span data-ttu-id="36948-116">Esegue il mapping degli indici stencil agli indici stencil.</span><span class="sxs-lookup"><span data-stu-id="36948-116">Maps stencil indexes to stencil indexes.</span></span><br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <span data-ttu-id="36948-117"><dt>**\_mapping GL \_ pixel \_ I \_ a \_ R**</dt></span><span class="sxs-lookup"><span data-stu-id="36948-117"><dt>**GL\_PIXEL\_MAP\_I\_TO\_R**</dt></span></span> </dl> | <span data-ttu-id="36948-118">Esegue il mapping degli indici dei colori ai componenti rossi.</span><span class="sxs-lookup"><span data-stu-id="36948-118">Maps color indexes to red components.</span></span><br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <span data-ttu-id="36948-119"><dt>**\_mappa GL \_ pixel \_ I \_ a \_ G**</dt></span><span class="sxs-lookup"><span data-stu-id="36948-119"><dt>**GL\_PIXEL\_MAP\_I\_TO\_G**</dt></span></span> </dl> | <span data-ttu-id="36948-120">Esegue il mapping degli indici dei colori ai componenti verdi.</span><span class="sxs-lookup"><span data-stu-id="36948-120">Maps color indexes to green components.</span></span><br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <span data-ttu-id="36948-121"><dt>**\_mappa GL \_ pixel \_ I \_ a \_ B**</dt></span><span class="sxs-lookup"><span data-stu-id="36948-121"><dt>**GL\_PIXEL\_MAP\_I\_TO\_B**</dt></span></span> </dl> | <span data-ttu-id="36948-122">Esegue il mapping degli indici dei colori ai componenti blu.</span><span class="sxs-lookup"><span data-stu-id="36948-122">Maps color indexes to blue components.</span></span><br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <span data-ttu-id="36948-123"><dt>**\_mappa GL \_ pixel \_ I \_ a \_**</dt></span><span class="sxs-lookup"><span data-stu-id="36948-123"><dt>**GL\_PIXEL\_MAP\_I\_TO\_A**</dt></span></span> </dl> | <span data-ttu-id="36948-124">Esegue il mapping degli indici dei colori ai componenti alfa.</span><span class="sxs-lookup"><span data-stu-id="36948-124">Maps color indexes to alpha components.</span></span><br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <span data-ttu-id="36948-125"><dt>**\_mapping GL \_ pixel \_ r \_ a \_ r**</dt></span><span class="sxs-lookup"><span data-stu-id="36948-125"><dt>**GL\_PIXEL\_MAP\_R\_TO\_R**</dt></span></span> </dl> | <span data-ttu-id="36948-126">Esegue il mapping dei componenti rossi ai componenti rossi.</span><span class="sxs-lookup"><span data-stu-id="36948-126">Maps red components to red components.</span></span><br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <span data-ttu-id="36948-127"><dt>**\_mappa GL \_ pixel \_ \_ da g a \_ g**</dt></span><span class="sxs-lookup"><span data-stu-id="36948-127"><dt>**GL\_PIXEL\_MAP\_G\_TO\_G**</dt></span></span> </dl> | <span data-ttu-id="36948-128">Esegue il mapping dei componenti verdi ai componenti verdi.</span><span class="sxs-lookup"><span data-stu-id="36948-128">Maps green components to green components.</span></span><br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <span data-ttu-id="36948-129"><dt>**\_mappa GL \_ pixel \_ b \_ a \_ b**</dt></span><span class="sxs-lookup"><span data-stu-id="36948-129"><dt>**GL\_PIXEL\_MAP\_B\_TO\_B**</dt></span></span> </dl> | <span data-ttu-id="36948-130">Esegue il mapping dei componenti blu ai componenti blu.</span><span class="sxs-lookup"><span data-stu-id="36948-130">Maps blue components to blue components.</span></span><br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <span data-ttu-id="36948-131"><dt>**\_pixel GL \_ mappato \_ \_ a a \_**</dt></span><span class="sxs-lookup"><span data-stu-id="36948-131"><dt>**GL\_PIXEL\_MAP\_A\_TO\_A**</dt></span></span> </dl> | <span data-ttu-id="36948-132">Esegue il mapping dei componenti alfa ai componenti alfa.</span><span class="sxs-lookup"><span data-stu-id="36948-132">Maps alpha components to alpha components.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="36948-133">*MapSize*</span><span class="sxs-lookup"><span data-stu-id="36948-133">*mapsize*</span></span> 
</dt> <dd>

<span data-ttu-id="36948-134">Dimensione della mappa da definire.</span><span class="sxs-lookup"><span data-stu-id="36948-134">The size of the map being defined.</span></span>

</dd> <dt>

<span data-ttu-id="36948-135">*valori*</span><span class="sxs-lookup"><span data-stu-id="36948-135">*values*</span></span> 
</dt> <dd>

<span data-ttu-id="36948-136">Matrice di valori *MapSize* .</span><span class="sxs-lookup"><span data-stu-id="36948-136">An array of *mapsize* values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36948-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="36948-137">Return value</span></span>

<span data-ttu-id="36948-138">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="36948-138">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="36948-139">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="36948-139">Error codes</span></span>

<span data-ttu-id="36948-140">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="36948-140">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="36948-141">Nome</span><span class="sxs-lookup"><span data-stu-id="36948-141">Name</span></span>                                                                                                  | <span data-ttu-id="36948-142">Significato</span><span class="sxs-lookup"><span data-stu-id="36948-142">Meaning</span></span>                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="36948-143"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="36948-143"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="36948-144">il *mapping* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="36948-144">*map* was not an accepted value.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="36948-145"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="36948-145"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="36948-146">*MapSize* è un valore negativo o maggiore della tabella di mapping di GL \_ pixel \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="36948-146">*mapsize* was negative or larger than GL\_PIXEL\_MAP\_TABLE.</span></span> <br/>                                                                                                                                                   |
| <dl> <span data-ttu-id="36948-147"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="36948-147"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="36948-148">*Map* is GL \_ pixel \_ Map \_ i \_ to \_ i, GL \_ pixel \_ Map \_ S \_ to \_ s, GL \_ pixel \_ Map \_ i \_ to \_ R, GL \_ pixel \_ Map \_ i \_ to \_ G, GL \_ pixel \_ Map \_ i \_ a \_ B o GL \_ pixel \_ Map \_ i \_ to \_ a e *MapSize* non era una potenza di due.</span><span class="sxs-lookup"><span data-stu-id="36948-148">*map* was GL\_PIXEL\_MAP\_I\_TO\_I, GL\_PIXEL\_MAP\_S\_TO\_S, GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, or GL\_PIXEL\_MAP\_I\_TO\_A, and *mapsize* was not a power of two.</span></span> <br/> |
| <dl> <span data-ttu-id="36948-149"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="36948-149"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="36948-150">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="36948-150">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                                                                                     |



## <a name="remarks"></a><span data-ttu-id="36948-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="36948-151">Remarks</span></span>

<span data-ttu-id="36948-152">La funzione **glPixelMap** imposta le tabelle di conversione, *o Maps*, utilizzate [**da glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), GlCopyTexSubImage2D, glDrawPixels, [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)e [**glTexSubImage2D**](gltexsubimage2d.md). [](glcopytexsubimage2d.md) [](gldrawpixels.md)</span><span class="sxs-lookup"><span data-stu-id="36948-152">The **glPixelMap** function sets up translation tables, or *maps*, used by [**glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md), and [**glTexSubImage2D**](gltexsubimage2d.md).</span></span> <span data-ttu-id="36948-153">L'uso di queste mappe è descritto completamente nell'argomento [**glPixelTransfer**](glpixeltransfer.md) e in parte negli argomenti relativi ai comandi per immagini pixel e trama.</span><span class="sxs-lookup"><span data-stu-id="36948-153">Use of these maps is described completely in the [**glPixelTransfer**](glpixeltransfer.md) topic, and partly in the topics for the pixel and texture image commands.</span></span> <span data-ttu-id="36948-154">In questo argomento viene descritta solo la specifica delle mappe.</span><span class="sxs-lookup"><span data-stu-id="36948-154">Only the specification of the maps is described in this topic.</span></span>

<span data-ttu-id="36948-155">Il parametro *Map* è un nome di mappa simbolico che indica una delle dieci mappe da impostare.</span><span class="sxs-lookup"><span data-stu-id="36948-155">The *map* parameter is a symbolic map name, indicating one of ten maps to set.</span></span> <span data-ttu-id="36948-156">Il parametro *MapSize* specifica il numero di voci nella mappa e *values* è un puntatore a una matrice di valori della mappa *MapSize* .</span><span class="sxs-lookup"><span data-stu-id="36948-156">The *mapsize* parameter specifies the number of entries in the map, and *values* is a pointer to an array of *mapsize* map values.</span></span>

<span data-ttu-id="36948-157">Le voci in una mappa possono essere specificate come numeri a virgola mobile e precisione singola, interi brevi senza segno o interi long senza segno.</span><span class="sxs-lookup"><span data-stu-id="36948-157">The entries in a map can be specified as single-precision floating-point numbers, unsigned short integers, or unsigned long integers.</span></span> <span data-ttu-id="36948-158">Mappe che archiviano i valori dei componenti colore (tutti tranne GL \_ pixel \_ Map \_ i \_ to \_ i e GL \_ pixel \_ Map \_ s \_ to \_ s) mantengono i valori in formato a virgola mobile, con dimensioni mantissa e esponenti non specificate.</span><span class="sxs-lookup"><span data-stu-id="36948-158">Maps that store color component values (all but GL\_PIXEL\_MAP\_I\_TO\_I and GL\_PIXEL\_MAP\_S\_TO\_S) retain their values in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="36948-159">I valori a virgola mobile specificati da [**glPixelMapfv**](glpixelmap.md) vengono convertiti direttamente nel formato a virgola mobile interno di queste mappe, quindi vengono bloccati nell'intervallo compreso tra \[ 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="36948-159">Floating-point values specified by [**glPixelMapfv**](glpixelmap.md) are converted directly to the internal floating-point format of these maps, and then clamped to the range \[0,1\].</span></span> <span data-ttu-id="36948-160">I valori interi senza segno specificati da **glPixelMapusv** e **glPixelMapuiv** vengono convertiti linearmente in modo che il valore integer rappresentabile più grande sia mappato a 1,0 e zero sia mappato a 0,0.</span><span class="sxs-lookup"><span data-stu-id="36948-160">Unsigned integer values specified by **glPixelMapusv** and **glPixelMapuiv** are converted linearly such that the largest representable integer maps to 1.0, and zero maps to 0.0.</span></span>

<span data-ttu-id="36948-161">Mappe che archiviano gli indici, GL \_ pixel \_ Map \_ i \_ to \_ i e GL \_ pixel \_ Map \_ s \_ to \_ s, mantengono i valori in formato a virgola fissa, con un numero di bit non specificato a destra del punto binario.</span><span class="sxs-lookup"><span data-stu-id="36948-161">Maps that store indexes, GL\_PIXEL\_MAP\_I\_TO\_I and GL\_PIXEL\_MAP\_S\_TO\_S, retain their values in fixed-point format, with an unspecified number of bits to the right of the binary point.</span></span> <span data-ttu-id="36948-162">I valori a virgola mobile specificati da [**glPixelMapfv**](glpixelmap.md) vengono convertiti direttamente nel formato a virgola fissa interno di queste mappe.</span><span class="sxs-lookup"><span data-stu-id="36948-162">Floating-point values specified by [**glPixelMapfv**](glpixelmap.md) are converted directly to the internal fixed-point format of these maps.</span></span> <span data-ttu-id="36948-163">I valori interi senza segno specificati da **glPixelMapusv** e **glPixelMapuiv** specificano i valori integer, con tutti gli zeri a destra del punto binario.</span><span class="sxs-lookup"><span data-stu-id="36948-163">Unsigned integer values specified by **glPixelMapusv** and **glPixelMapuiv** specify integer values, with all zeros to the right of the binary point.</span></span>

<span data-ttu-id="36948-164">Nella tabella seguente vengono illustrate le dimensioni e i valori iniziali per ogni mappa.</span><span class="sxs-lookup"><span data-stu-id="36948-164">The following table shows the initial sizes and values for each of the maps.</span></span> <span data-ttu-id="36948-165">Le mappe indicizzate in base agli indici colore o stencil devono avere *MapSize* = 2 ^ *n* per alcuni *n* o i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="36948-165">Maps that are indexed by either color or stencil indexes must have *mapsize* = 2 ^ *n* for some *n* or results are undefined.</span></span> <span data-ttu-id="36948-166">Le dimensioni massime consentite per ogni mapping dipendono dall'implementazione e possono essere determinate chiamando **glGet** con la \_ tabella di mappa dei pixel max dell'argomento \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="36948-166">The maximum allowable size for each map depends on the implementation and can be determined by calling **glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE.</span></span> <span data-ttu-id="36948-167">Il valore massimo viene applicato a tutte le mappe ed è almeno pari a 32.</span><span class="sxs-lookup"><span data-stu-id="36948-167">The single maximum applies to all maps, and it is at least 32.</span></span>



| <span data-ttu-id="36948-168">Mappa</span><span class="sxs-lookup"><span data-stu-id="36948-168">Map</span></span>                      | <span data-ttu-id="36948-169">Indice di ricerca</span><span class="sxs-lookup"><span data-stu-id="36948-169">Lookup Index</span></span>  | <span data-ttu-id="36948-170">Valore di ricerca</span><span class="sxs-lookup"><span data-stu-id="36948-170">Lookup Value</span></span>  | <span data-ttu-id="36948-171">Dimensioni iniziali</span><span class="sxs-lookup"><span data-stu-id="36948-171">Initial Size</span></span> | <span data-ttu-id="36948-172">Valore iniziale</span><span class="sxs-lookup"><span data-stu-id="36948-172">Initial Value</span></span> |
|--------------------------|---------------|---------------|--------------|---------------|
| <span data-ttu-id="36948-173">\_mappa GL \_ pixel \_ i \_ \_</span><span class="sxs-lookup"><span data-stu-id="36948-173">GL\_PIXEL\_MAP\_I\_TO\_I</span></span> | <span data-ttu-id="36948-174">indice colori</span><span class="sxs-lookup"><span data-stu-id="36948-174">color index</span></span>   | <span data-ttu-id="36948-175">indice colori</span><span class="sxs-lookup"><span data-stu-id="36948-175">color index</span></span>   | <span data-ttu-id="36948-176">1</span><span class="sxs-lookup"><span data-stu-id="36948-176">1</span></span>            | <span data-ttu-id="36948-177">0,0</span><span class="sxs-lookup"><span data-stu-id="36948-177">0.0</span></span>           |
| <span data-ttu-id="36948-178">\_mapping GL \_ pixel \_ \_ a \_ s</span><span class="sxs-lookup"><span data-stu-id="36948-178">GL\_PIXEL\_MAP\_S\_TO\_S</span></span> | <span data-ttu-id="36948-179">Indice stencil</span><span class="sxs-lookup"><span data-stu-id="36948-179">stencil index</span></span> | <span data-ttu-id="36948-180">Indice stencil</span><span class="sxs-lookup"><span data-stu-id="36948-180">stencil index</span></span> | <span data-ttu-id="36948-181">1</span><span class="sxs-lookup"><span data-stu-id="36948-181">1</span></span>            | <span data-ttu-id="36948-182">0,0</span><span class="sxs-lookup"><span data-stu-id="36948-182">0.0</span></span>           |
| <span data-ttu-id="36948-183">\_mapping GL \_ pixel \_ I \_ a \_ R</span><span class="sxs-lookup"><span data-stu-id="36948-183">GL\_PIXEL\_MAP\_I\_TO\_R</span></span> | <span data-ttu-id="36948-184">indice colori</span><span class="sxs-lookup"><span data-stu-id="36948-184">color index</span></span>   | <span data-ttu-id="36948-185">R</span><span class="sxs-lookup"><span data-stu-id="36948-185">R</span></span>             | <span data-ttu-id="36948-186">1</span><span class="sxs-lookup"><span data-stu-id="36948-186">1</span></span>            | <span data-ttu-id="36948-187">0,0</span><span class="sxs-lookup"><span data-stu-id="36948-187">0.0</span></span>           |
| <span data-ttu-id="36948-188">\_mappa GL \_ pixel \_ I \_ a \_ G</span><span class="sxs-lookup"><span data-stu-id="36948-188">GL\_PIXEL\_MAP\_I\_TO\_G</span></span> | <span data-ttu-id="36948-189">indice colori</span><span class="sxs-lookup"><span data-stu-id="36948-189">color index</span></span>   | <span data-ttu-id="36948-190">G</span><span class="sxs-lookup"><span data-stu-id="36948-190">G</span></span>             | <span data-ttu-id="36948-191">1</span><span class="sxs-lookup"><span data-stu-id="36948-191">1</span></span>            | <span data-ttu-id="36948-192">0,0</span><span class="sxs-lookup"><span data-stu-id="36948-192">0.0</span></span>           |
| <span data-ttu-id="36948-193">\_mappa GL \_ pixel \_ I \_ a \_ B</span><span class="sxs-lookup"><span data-stu-id="36948-193">GL\_PIXEL\_MAP\_I\_TO\_B</span></span> | <span data-ttu-id="36948-194">indice colori</span><span class="sxs-lookup"><span data-stu-id="36948-194">color index</span></span>   | <span data-ttu-id="36948-195">B</span><span class="sxs-lookup"><span data-stu-id="36948-195">B</span></span>             | <span data-ttu-id="36948-196">1</span><span class="sxs-lookup"><span data-stu-id="36948-196">1</span></span>            | <span data-ttu-id="36948-197">0,0</span><span class="sxs-lookup"><span data-stu-id="36948-197">0.0</span></span>           |
| <span data-ttu-id="36948-198">\_mappa GL \_ pixel \_ I \_ a \_</span><span class="sxs-lookup"><span data-stu-id="36948-198">GL\_PIXEL\_MAP\_I\_TO\_A</span></span> | <span data-ttu-id="36948-199">indice colori</span><span class="sxs-lookup"><span data-stu-id="36948-199">color index</span></span>   | <span data-ttu-id="36948-200">A</span><span class="sxs-lookup"><span data-stu-id="36948-200">A</span></span>             | <span data-ttu-id="36948-201">1</span><span class="sxs-lookup"><span data-stu-id="36948-201">1</span></span>            | <span data-ttu-id="36948-202">0,0</span><span class="sxs-lookup"><span data-stu-id="36948-202">0.0</span></span>           |
| <span data-ttu-id="36948-203">\_mapping GL \_ pixel \_ r \_ a \_ r</span><span class="sxs-lookup"><span data-stu-id="36948-203">GL\_PIXEL\_MAP\_R\_TO\_R</span></span> | <span data-ttu-id="36948-204">R</span><span class="sxs-lookup"><span data-stu-id="36948-204">R</span></span>             | <span data-ttu-id="36948-205">R</span><span class="sxs-lookup"><span data-stu-id="36948-205">R</span></span>             | <span data-ttu-id="36948-206">1</span><span class="sxs-lookup"><span data-stu-id="36948-206">1</span></span>            | <span data-ttu-id="36948-207">0,0</span><span class="sxs-lookup"><span data-stu-id="36948-207">0.0</span></span>           |
| <span data-ttu-id="36948-208">\_mappa GL \_ pixel \_ \_ da g a \_ g</span><span class="sxs-lookup"><span data-stu-id="36948-208">GL\_PIXEL\_MAP\_G\_TO\_G</span></span> | <span data-ttu-id="36948-209">G</span><span class="sxs-lookup"><span data-stu-id="36948-209">G</span></span>             | <span data-ttu-id="36948-210">G</span><span class="sxs-lookup"><span data-stu-id="36948-210">G</span></span>             | <span data-ttu-id="36948-211">1</span><span class="sxs-lookup"><span data-stu-id="36948-211">1</span></span>            | <span data-ttu-id="36948-212">0,0</span><span class="sxs-lookup"><span data-stu-id="36948-212">0.0</span></span>           |
| <span data-ttu-id="36948-213">\_mappa GL \_ pixel \_ b \_ a \_ b</span><span class="sxs-lookup"><span data-stu-id="36948-213">GL\_PIXEL\_MAP\_B\_TO\_B</span></span> | <span data-ttu-id="36948-214">B</span><span class="sxs-lookup"><span data-stu-id="36948-214">B</span></span>             | <span data-ttu-id="36948-215">B</span><span class="sxs-lookup"><span data-stu-id="36948-215">B</span></span>             | <span data-ttu-id="36948-216">1</span><span class="sxs-lookup"><span data-stu-id="36948-216">1</span></span>            | <span data-ttu-id="36948-217">0,0</span><span class="sxs-lookup"><span data-stu-id="36948-217">0.0</span></span>           |
| <span data-ttu-id="36948-218">\_pixel GL \_ mappato \_ \_ a a \_</span><span class="sxs-lookup"><span data-stu-id="36948-218">GL\_PIXEL\_MAP\_A\_TO\_A</span></span> | <span data-ttu-id="36948-219">A</span><span class="sxs-lookup"><span data-stu-id="36948-219">A</span></span>             | <span data-ttu-id="36948-220">A</span><span class="sxs-lookup"><span data-stu-id="36948-220">A</span></span>             | <span data-ttu-id="36948-221">1</span><span class="sxs-lookup"><span data-stu-id="36948-221">1</span></span>            | <span data-ttu-id="36948-222">0,0</span><span class="sxs-lookup"><span data-stu-id="36948-222">0.0</span></span>           |



 

<span data-ttu-id="36948-223">Le funzioni seguenti consentono di recuperare informazioni correlate a **glPixelMap**:</span><span class="sxs-lookup"><span data-stu-id="36948-223">The following functions retrieve information related to **glPixelMap**:</span></span>

<span data-ttu-id="36948-224">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ pixel \_ Map \_ i \_ to \_ i \_ size</span><span class="sxs-lookup"><span data-stu-id="36948-224">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PIXEL\_MAP\_I\_TO\_I\_SIZE</span></span>

<span data-ttu-id="36948-225">**glGet** con argomento \_ \_ di mapping GL pixel per la \_ \_ \_ \_ dimensione s</span><span class="sxs-lookup"><span data-stu-id="36948-225">**glGet** with argument GL\_PIXEL\_MAP\_S\_TO\_S\_SIZE</span></span>

<span data-ttu-id="36948-226">**glGet** con argomento GL \_ pixel \_ Map \_ I \_ to \_ R \_ size</span><span class="sxs-lookup"><span data-stu-id="36948-226">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_R\_SIZE</span></span>

<span data-ttu-id="36948-227">**glGet** con argomento GL \_ pixel \_ mapping \_ I \_ a \_ G \_ size</span><span class="sxs-lookup"><span data-stu-id="36948-227">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_G\_SIZE</span></span>

<span data-ttu-id="36948-228">**glGet** con argomento GL \_ pixel \_ Map \_ I \_ a \_ B \_ size</span><span class="sxs-lookup"><span data-stu-id="36948-228">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_B\_SIZE</span></span>

<span data-ttu-id="36948-229">**glGet** con argomento GL \_ pixel \_ mappa \_ I \_ a \_ una \_ dimensione</span><span class="sxs-lookup"><span data-stu-id="36948-229">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_A\_SIZE</span></span>

<span data-ttu-id="36948-230">**glGet** con argomento GL \_ pixel \_ Map \_ r \_ to \_ r \_ size</span><span class="sxs-lookup"><span data-stu-id="36948-230">**glGet** with argument GL\_PIXEL\_MAP\_R\_TO\_R\_SIZE</span></span>

<span data-ttu-id="36948-231">**glGet** con argomento GL \_ pixel \_ mappa \_ g \_ a \_ g \_ size</span><span class="sxs-lookup"><span data-stu-id="36948-231">**glGet** with argument GL\_PIXEL\_MAP\_G\_TO\_G\_SIZE</span></span>

<span data-ttu-id="36948-232">**glGet** con argomento GL \_ pixel \_ mappa \_ b \_ a \_ b \_ dimensioni</span><span class="sxs-lookup"><span data-stu-id="36948-232">**glGet** with argument GL\_PIXEL\_MAP\_B\_TO\_B\_SIZE</span></span>

<span data-ttu-id="36948-233">**glGet** con argomento GL \_ pixel \_ mappa \_ a \_ \_ una \_ dimensione</span><span class="sxs-lookup"><span data-stu-id="36948-233">**glGet** with argument GL\_PIXEL\_MAP\_A\_TO\_A\_SIZE</span></span>

<span data-ttu-id="36948-234">**glGet** con argomento \_ tabella di \_ mappa pixel max \_ \_</span><span class="sxs-lookup"><span data-stu-id="36948-234">**glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE</span></span>

## <a name="requirements"></a><span data-ttu-id="36948-235">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36948-235">Requirements</span></span>



| <span data-ttu-id="36948-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="36948-236">Requirement</span></span> | <span data-ttu-id="36948-237">Valore</span><span class="sxs-lookup"><span data-stu-id="36948-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36948-238">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36948-238">Minimum supported client</span></span><br/> | <span data-ttu-id="36948-239">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="36948-239">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="36948-240">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36948-240">Minimum supported server</span></span><br/> | <span data-ttu-id="36948-241">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="36948-241">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="36948-242">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36948-242">Header</span></span><br/>                   | <dl> <span data-ttu-id="36948-243"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="36948-243"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="36948-244">Libreria</span><span class="sxs-lookup"><span data-stu-id="36948-244">Library</span></span><br/>                  | <dl> <span data-ttu-id="36948-245"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36948-245"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="36948-246">DLL</span><span class="sxs-lookup"><span data-stu-id="36948-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36948-247"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36948-247"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36948-248">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36948-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36948-249">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="36948-249">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="36948-250">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="36948-250">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="36948-251">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="36948-251">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="36948-252">**Remo**</span><span class="sxs-lookup"><span data-stu-id="36948-252">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="36948-253">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="36948-253">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="36948-254">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="36948-254">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="36948-255">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="36948-255">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="36948-256">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="36948-256">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="36948-257">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="36948-257">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 






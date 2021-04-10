---
title: funzione glPixelMapuiv (GL. h)
description: La funzione glPixelMapuiv imposta le mappe di trasferimento dei pixel.
ms.assetid: dd0f7881-fdd1-49c2-b68c-21e2f9e5ecd2
keywords:
- funzione glPixelMapuiv OpenGL
topic_type:
- apiref
api_name:
- glPixelMapuiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e9b31398060e62fa14cd35afe4f8536dd78f963
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964350"
---
# <a name="glpixelmapuiv-function"></a><span data-ttu-id="2a9bf-104">glPixelMapuiv (funzione)</span><span class="sxs-lookup"><span data-stu-id="2a9bf-104">glPixelMapuiv function</span></span>

<span data-ttu-id="2a9bf-105">La funzione **glPixelMapuiv** imposta le mappe di trasferimento dei pixel.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-105">The **glPixelMapuiv** function sets up pixel transfer maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a9bf-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a9bf-106">Syntax</span></span>


```C++
void WINAPI glPixelMapuiv(
         GLenum  map,
         GLsizei mapsize,
   const GLuint  *values
);
```



## <a name="parameters"></a><span data-ttu-id="2a9bf-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a9bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a9bf-108">*map*</span><span class="sxs-lookup"><span data-stu-id="2a9bf-108">*map*</span></span> 
</dt> <dd>

<span data-ttu-id="2a9bf-109">Nome di mappa simbolico.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-109">A symbolic map name.</span></span> <span data-ttu-id="2a9bf-110">Le dieci mappe sono le seguenti.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-110">The ten maps are as follows.</span></span>



| <span data-ttu-id="2a9bf-111">Valore</span><span class="sxs-lookup"><span data-stu-id="2a9bf-111">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="2a9bf-112">Significato</span><span class="sxs-lookup"><span data-stu-id="2a9bf-112">Meaning</span></span>                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <span data-ttu-id="2a9bf-113"><dt>**\_mappa GL \_ pixel \_ i \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bf-113"><dt>**GL\_PIXEL\_MAP\_I\_TO\_I**</dt></span></span> </dl> | <span data-ttu-id="2a9bf-114">Esegue il mapping degli indici colore agli indici colori.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-114">Maps color indexes to color indexes.</span></span><br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <span data-ttu-id="2a9bf-115"><dt>**\_mapping GL \_ pixel \_ \_ a \_ s**</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bf-115"><dt>**GL\_PIXEL\_MAP\_S\_TO\_S**</dt></span></span> </dl> | <span data-ttu-id="2a9bf-116">Esegue il mapping degli indici stencil agli indici stencil.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-116">Maps stencil indexes to stencil indexes.</span></span><br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <span data-ttu-id="2a9bf-117"><dt>**\_mapping GL \_ pixel \_ I \_ a \_ R**</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bf-117"><dt>**GL\_PIXEL\_MAP\_I\_TO\_R**</dt></span></span> </dl> | <span data-ttu-id="2a9bf-118">Esegue il mapping degli indici dei colori ai componenti rossi.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-118">Maps color indexes to red components.</span></span><br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <span data-ttu-id="2a9bf-119"><dt>**\_mappa GL \_ pixel \_ I \_ a \_ G**</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bf-119"><dt>**GL\_PIXEL\_MAP\_I\_TO\_G**</dt></span></span> </dl> | <span data-ttu-id="2a9bf-120">Esegue il mapping degli indici dei colori ai componenti verdi.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-120">Maps color indexes to green components.</span></span><br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <span data-ttu-id="2a9bf-121"><dt>**\_mappa GL \_ pixel \_ I \_ a \_ B**</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bf-121"><dt>**GL\_PIXEL\_MAP\_I\_TO\_B**</dt></span></span> </dl> | <span data-ttu-id="2a9bf-122">Esegue il mapping degli indici dei colori ai componenti blu.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-122">Maps color indexes to blue components.</span></span><br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <span data-ttu-id="2a9bf-123"><dt>**\_mappa GL \_ pixel \_ I \_ a \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bf-123"><dt>**GL\_PIXEL\_MAP\_I\_TO\_A**</dt></span></span> </dl> | <span data-ttu-id="2a9bf-124">Esegue il mapping degli indici dei colori ai componenti alfa.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-124">Maps color indexes to alpha components.</span></span><br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <span data-ttu-id="2a9bf-125"><dt>**\_mapping GL \_ pixel \_ r \_ a \_ r**</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bf-125"><dt>**GL\_PIXEL\_MAP\_R\_TO\_R**</dt></span></span> </dl> | <span data-ttu-id="2a9bf-126">Esegue il mapping dei componenti rossi ai componenti rossi.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-126">Maps red components to red components.</span></span><br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <span data-ttu-id="2a9bf-127"><dt>**\_mappa GL \_ pixel \_ \_ da g a \_ g**</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bf-127"><dt>**GL\_PIXEL\_MAP\_G\_TO\_G**</dt></span></span> </dl> | <span data-ttu-id="2a9bf-128">Esegue il mapping dei componenti verdi ai componenti verdi.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-128">Maps green components to green components.</span></span><br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <span data-ttu-id="2a9bf-129"><dt>**\_mappa GL \_ pixel \_ b \_ a \_ b**</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bf-129"><dt>**GL\_PIXEL\_MAP\_B\_TO\_B**</dt></span></span> </dl> | <span data-ttu-id="2a9bf-130">Esegue il mapping dei componenti blu ai componenti blu.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-130">Maps blue components to blue components.</span></span><br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <span data-ttu-id="2a9bf-131"><dt>**\_pixel GL \_ mappato \_ \_ a a \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bf-131"><dt>**GL\_PIXEL\_MAP\_A\_TO\_A**</dt></span></span> </dl> | <span data-ttu-id="2a9bf-132">Esegue il mapping dei componenti alfa ai componenti alfa.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-132">Maps alpha components to alpha components.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2a9bf-133">*MapSize*</span><span class="sxs-lookup"><span data-stu-id="2a9bf-133">*mapsize*</span></span> 
</dt> <dd>

<span data-ttu-id="2a9bf-134">Dimensione della mappa da definire.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-134">The size of the map being defined.</span></span>

</dd> <dt>

<span data-ttu-id="2a9bf-135">*valori*</span><span class="sxs-lookup"><span data-stu-id="2a9bf-135">*values*</span></span> 
</dt> <dd>

<span data-ttu-id="2a9bf-136">Matrice di valori *MapSize* .</span><span class="sxs-lookup"><span data-stu-id="2a9bf-136">An array of *mapsize* values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a9bf-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a9bf-137">Return value</span></span>

<span data-ttu-id="2a9bf-138">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-138">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2a9bf-139">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="2a9bf-139">Error codes</span></span>

<span data-ttu-id="2a9bf-140">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="2a9bf-140">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2a9bf-141">Nome</span><span class="sxs-lookup"><span data-stu-id="2a9bf-141">Name</span></span>                                                                                                  | <span data-ttu-id="2a9bf-142">Significato</span><span class="sxs-lookup"><span data-stu-id="2a9bf-142">Meaning</span></span>                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a9bf-143"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bf-143"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="2a9bf-144">il *mapping* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-144">*map* was not an accepted value.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="2a9bf-145"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bf-145"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="2a9bf-146">*MapSize* è un valore negativo o maggiore della tabella di mapping di GL \_ pixel \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2a9bf-146">*mapsize* was negative or larger than GL\_PIXEL\_MAP\_TABLE.</span></span> <br/>                                                                                                                                                   |
| <dl> <span data-ttu-id="2a9bf-147"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bf-147"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="2a9bf-148">*Map* is GL \_ pixel \_ Map \_ i \_ to \_ i, GL \_ pixel \_ Map \_ S \_ to \_ s, GL \_ pixel \_ Map \_ i \_ to \_ R, GL \_ pixel \_ Map \_ i \_ to \_ G, GL \_ pixel \_ Map \_ i \_ a \_ B o GL \_ pixel \_ Map \_ i \_ to \_ a e *MapSize* non era una potenza di due.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-148">*map* was GL\_PIXEL\_MAP\_I\_TO\_I, GL\_PIXEL\_MAP\_S\_TO\_S, GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, or GL\_PIXEL\_MAP\_I\_TO\_A, and *mapsize* was not a power of two.</span></span> <br/> |
| <dl> <span data-ttu-id="2a9bf-149"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bf-149"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2a9bf-150">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2a9bf-150">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                                                                                     |



## <a name="remarks"></a><span data-ttu-id="2a9bf-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a9bf-151">Remarks</span></span>

<span data-ttu-id="2a9bf-152">La funzione **glPixelMap** imposta le tabelle di conversione, *o Maps*, utilizzate [**da glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), GlCopyTexSubImage2D, glDrawPixels, [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)e [**glTexSubImage2D**](gltexsubimage2d.md). [](glcopytexsubimage2d.md) [](gldrawpixels.md)</span><span class="sxs-lookup"><span data-stu-id="2a9bf-152">The **glPixelMap** function sets up translation tables, or *maps*, used by [**glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md), and [**glTexSubImage2D**](gltexsubimage2d.md).</span></span> <span data-ttu-id="2a9bf-153">L'uso di queste mappe è descritto completamente nell'argomento [**glPixelTransfer**](glpixeltransfer.md) e in parte negli argomenti relativi ai comandi per immagini pixel e trama.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-153">Use of these maps is described completely in the [**glPixelTransfer**](glpixeltransfer.md) topic, and partly in the topics for the pixel and texture image commands.</span></span> <span data-ttu-id="2a9bf-154">In questo argomento viene descritta solo la specifica delle mappe.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-154">Only the specification of the maps is described in this topic.</span></span>

<span data-ttu-id="2a9bf-155">Il parametro *Map* è un nome di mappa simbolico che indica una delle dieci mappe da impostare.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-155">The *map* parameter is a symbolic map name, indicating one of ten maps to set.</span></span> <span data-ttu-id="2a9bf-156">Il parametro *MapSize* specifica il numero di voci nella mappa e *values* è un puntatore a una matrice di valori della mappa *MapSize* .</span><span class="sxs-lookup"><span data-stu-id="2a9bf-156">The *mapsize* parameter specifies the number of entries in the map, and *values* is a pointer to an array of *mapsize* map values.</span></span>

<span data-ttu-id="2a9bf-157">Le voci in una mappa possono essere specificate come numeri a virgola mobile e precisione singola, interi brevi senza segno o interi long senza segno.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-157">The entries in a map can be specified as single-precision floating-point numbers, unsigned short integers, or unsigned long integers.</span></span> <span data-ttu-id="2a9bf-158">Mappe che archiviano i valori dei componenti colore (tutti tranne GL \_ pixel \_ Map \_ i \_ to \_ i e GL \_ pixel \_ Map \_ s \_ to \_ s) mantengono i valori in formato a virgola mobile, con dimensioni mantissa e esponenti non specificate.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-158">Maps that store color component values (all but GL\_PIXEL\_MAP\_I\_TO\_I and GL\_PIXEL\_MAP\_S\_TO\_S) retain their values in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="2a9bf-159">I valori a virgola mobile specificati da [**glPixelMapfv**](glpixelmap.md) vengono convertiti direttamente nel formato a virgola mobile interno di queste mappe, quindi vengono bloccati nell'intervallo compreso tra \[ 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="2a9bf-159">Floating-point values specified by [**glPixelMapfv**](glpixelmap.md) are converted directly to the internal floating-point format of these maps, and then clamped to the range \[0,1\].</span></span> <span data-ttu-id="2a9bf-160">I valori interi senza segno specificati da **glPixelMapusv** e **glPixelMapuiv** vengono convertiti linearmente in modo che il valore integer rappresentabile più grande sia mappato a 1,0 e zero sia mappato a 0,0.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-160">Unsigned integer values specified by **glPixelMapusv** and **glPixelMapuiv** are converted linearly such that the largest representable integer maps to 1.0, and zero maps to 0.0.</span></span>

<span data-ttu-id="2a9bf-161">Mappe che archiviano gli indici, GL \_ pixel \_ Map \_ i \_ to \_ i e GL \_ pixel \_ Map \_ s \_ to \_ s, mantengono i valori in formato a virgola fissa, con un numero di bit non specificato a destra del punto binario.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-161">Maps that store indexes, GL\_PIXEL\_MAP\_I\_TO\_I and GL\_PIXEL\_MAP\_S\_TO\_S, retain their values in fixed-point format, with an unspecified number of bits to the right of the binary point.</span></span> <span data-ttu-id="2a9bf-162">I valori a virgola mobile specificati da [**glPixelMapfv**](glpixelmap.md) vengono convertiti direttamente nel formato a virgola fissa interno di queste mappe.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-162">Floating-point values specified by [**glPixelMapfv**](glpixelmap.md) are converted directly to the internal fixed-point format of these maps.</span></span> <span data-ttu-id="2a9bf-163">I valori interi senza segno specificati da **glPixelMapusv** e **glPixelMapuiv** specificano i valori integer, con tutti gli zeri a destra del punto binario.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-163">Unsigned integer values specified by **glPixelMapusv** and **glPixelMapuiv** specify integer values, with all zeros to the right of the binary point.</span></span>

<span data-ttu-id="2a9bf-164">Nella tabella seguente vengono illustrate le dimensioni e i valori iniziali per ogni mappa.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-164">The following table shows the initial sizes and values for each of the maps.</span></span> <span data-ttu-id="2a9bf-165">Le mappe indicizzate in base agli indici colore o stencil devono avere *MapSize* = 2 ^ *n* per alcuni *n* o i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-165">Maps that are indexed by either color or stencil indexes must have *mapsize* = 2 ^ *n* for some *n* or results are undefined.</span></span> <span data-ttu-id="2a9bf-166">Le dimensioni massime consentite per ogni mapping dipendono dall'implementazione e possono essere determinate chiamando **glGet** con la \_ tabella di mappa dei pixel max dell'argomento \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2a9bf-166">The maximum allowable size for each map depends on the implementation and can be determined by calling **glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE.</span></span> <span data-ttu-id="2a9bf-167">Il valore massimo viene applicato a tutte le mappe ed è almeno pari a 32.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-167">The single maximum applies to all maps, and it is at least 32.</span></span>



| <span data-ttu-id="2a9bf-168">Mappa</span><span class="sxs-lookup"><span data-stu-id="2a9bf-168">Map</span></span>                      | <span data-ttu-id="2a9bf-169">Indice di ricerca</span><span class="sxs-lookup"><span data-stu-id="2a9bf-169">Lookup Index</span></span>  | <span data-ttu-id="2a9bf-170">Valore di ricerca</span><span class="sxs-lookup"><span data-stu-id="2a9bf-170">Lookup Value</span></span>  | <span data-ttu-id="2a9bf-171">Dimensioni iniziali</span><span class="sxs-lookup"><span data-stu-id="2a9bf-171">Initial Size</span></span> | <span data-ttu-id="2a9bf-172">Valore iniziale</span><span class="sxs-lookup"><span data-stu-id="2a9bf-172">Initial Value</span></span> |
|--------------------------|---------------|---------------|--------------|---------------|
| <span data-ttu-id="2a9bf-173">\_mappa GL \_ pixel \_ i \_ \_</span><span class="sxs-lookup"><span data-stu-id="2a9bf-173">GL\_PIXEL\_MAP\_I\_TO\_I</span></span> | <span data-ttu-id="2a9bf-174">indice colori</span><span class="sxs-lookup"><span data-stu-id="2a9bf-174">color index</span></span>   | <span data-ttu-id="2a9bf-175">indice colori</span><span class="sxs-lookup"><span data-stu-id="2a9bf-175">color index</span></span>   | <span data-ttu-id="2a9bf-176">1</span><span class="sxs-lookup"><span data-stu-id="2a9bf-176">1</span></span>            | <span data-ttu-id="2a9bf-177">0,0</span><span class="sxs-lookup"><span data-stu-id="2a9bf-177">0.0</span></span>           |
| <span data-ttu-id="2a9bf-178">\_mapping GL \_ pixel \_ \_ a \_ s</span><span class="sxs-lookup"><span data-stu-id="2a9bf-178">GL\_PIXEL\_MAP\_S\_TO\_S</span></span> | <span data-ttu-id="2a9bf-179">Indice stencil</span><span class="sxs-lookup"><span data-stu-id="2a9bf-179">stencil index</span></span> | <span data-ttu-id="2a9bf-180">Indice stencil</span><span class="sxs-lookup"><span data-stu-id="2a9bf-180">stencil index</span></span> | <span data-ttu-id="2a9bf-181">1</span><span class="sxs-lookup"><span data-stu-id="2a9bf-181">1</span></span>            | <span data-ttu-id="2a9bf-182">0,0</span><span class="sxs-lookup"><span data-stu-id="2a9bf-182">0.0</span></span>           |
| <span data-ttu-id="2a9bf-183">\_mapping GL \_ pixel \_ I \_ a \_ R</span><span class="sxs-lookup"><span data-stu-id="2a9bf-183">GL\_PIXEL\_MAP\_I\_TO\_R</span></span> | <span data-ttu-id="2a9bf-184">indice colori</span><span class="sxs-lookup"><span data-stu-id="2a9bf-184">color index</span></span>   | <span data-ttu-id="2a9bf-185">R</span><span class="sxs-lookup"><span data-stu-id="2a9bf-185">R</span></span>             | <span data-ttu-id="2a9bf-186">1</span><span class="sxs-lookup"><span data-stu-id="2a9bf-186">1</span></span>            | <span data-ttu-id="2a9bf-187">0,0</span><span class="sxs-lookup"><span data-stu-id="2a9bf-187">0.0</span></span>           |
| <span data-ttu-id="2a9bf-188">\_mappa GL \_ pixel \_ I \_ a \_ G</span><span class="sxs-lookup"><span data-stu-id="2a9bf-188">GL\_PIXEL\_MAP\_I\_TO\_G</span></span> | <span data-ttu-id="2a9bf-189">indice colori</span><span class="sxs-lookup"><span data-stu-id="2a9bf-189">color index</span></span>   | <span data-ttu-id="2a9bf-190">G</span><span class="sxs-lookup"><span data-stu-id="2a9bf-190">G</span></span>             | <span data-ttu-id="2a9bf-191">1</span><span class="sxs-lookup"><span data-stu-id="2a9bf-191">1</span></span>            | <span data-ttu-id="2a9bf-192">0,0</span><span class="sxs-lookup"><span data-stu-id="2a9bf-192">0.0</span></span>           |
| <span data-ttu-id="2a9bf-193">\_mappa GL \_ pixel \_ I \_ a \_ B</span><span class="sxs-lookup"><span data-stu-id="2a9bf-193">GL\_PIXEL\_MAP\_I\_TO\_B</span></span> | <span data-ttu-id="2a9bf-194">indice colori</span><span class="sxs-lookup"><span data-stu-id="2a9bf-194">color index</span></span>   | <span data-ttu-id="2a9bf-195">B</span><span class="sxs-lookup"><span data-stu-id="2a9bf-195">B</span></span>             | <span data-ttu-id="2a9bf-196">1</span><span class="sxs-lookup"><span data-stu-id="2a9bf-196">1</span></span>            | <span data-ttu-id="2a9bf-197">0,0</span><span class="sxs-lookup"><span data-stu-id="2a9bf-197">0.0</span></span>           |
| <span data-ttu-id="2a9bf-198">\_mappa GL \_ pixel \_ I \_ a \_</span><span class="sxs-lookup"><span data-stu-id="2a9bf-198">GL\_PIXEL\_MAP\_I\_TO\_A</span></span> | <span data-ttu-id="2a9bf-199">indice colori</span><span class="sxs-lookup"><span data-stu-id="2a9bf-199">color index</span></span>   | <span data-ttu-id="2a9bf-200">A</span><span class="sxs-lookup"><span data-stu-id="2a9bf-200">A</span></span>             | <span data-ttu-id="2a9bf-201">1</span><span class="sxs-lookup"><span data-stu-id="2a9bf-201">1</span></span>            | <span data-ttu-id="2a9bf-202">0,0</span><span class="sxs-lookup"><span data-stu-id="2a9bf-202">0.0</span></span>           |
| <span data-ttu-id="2a9bf-203">\_mapping GL \_ pixel \_ r \_ a \_ r</span><span class="sxs-lookup"><span data-stu-id="2a9bf-203">GL\_PIXEL\_MAP\_R\_TO\_R</span></span> | <span data-ttu-id="2a9bf-204">R</span><span class="sxs-lookup"><span data-stu-id="2a9bf-204">R</span></span>             | <span data-ttu-id="2a9bf-205">R</span><span class="sxs-lookup"><span data-stu-id="2a9bf-205">R</span></span>             | <span data-ttu-id="2a9bf-206">1</span><span class="sxs-lookup"><span data-stu-id="2a9bf-206">1</span></span>            | <span data-ttu-id="2a9bf-207">0,0</span><span class="sxs-lookup"><span data-stu-id="2a9bf-207">0.0</span></span>           |
| <span data-ttu-id="2a9bf-208">\_mappa GL \_ pixel \_ \_ da g a \_ g</span><span class="sxs-lookup"><span data-stu-id="2a9bf-208">GL\_PIXEL\_MAP\_G\_TO\_G</span></span> | <span data-ttu-id="2a9bf-209">G</span><span class="sxs-lookup"><span data-stu-id="2a9bf-209">G</span></span>             | <span data-ttu-id="2a9bf-210">G</span><span class="sxs-lookup"><span data-stu-id="2a9bf-210">G</span></span>             | <span data-ttu-id="2a9bf-211">1</span><span class="sxs-lookup"><span data-stu-id="2a9bf-211">1</span></span>            | <span data-ttu-id="2a9bf-212">0,0</span><span class="sxs-lookup"><span data-stu-id="2a9bf-212">0.0</span></span>           |
| <span data-ttu-id="2a9bf-213">\_mappa GL \_ pixel \_ b \_ a \_ b</span><span class="sxs-lookup"><span data-stu-id="2a9bf-213">GL\_PIXEL\_MAP\_B\_TO\_B</span></span> | <span data-ttu-id="2a9bf-214">B</span><span class="sxs-lookup"><span data-stu-id="2a9bf-214">B</span></span>             | <span data-ttu-id="2a9bf-215">B</span><span class="sxs-lookup"><span data-stu-id="2a9bf-215">B</span></span>             | <span data-ttu-id="2a9bf-216">1</span><span class="sxs-lookup"><span data-stu-id="2a9bf-216">1</span></span>            | <span data-ttu-id="2a9bf-217">0,0</span><span class="sxs-lookup"><span data-stu-id="2a9bf-217">0.0</span></span>           |
| <span data-ttu-id="2a9bf-218">\_pixel GL \_ mappato \_ \_ a a \_</span><span class="sxs-lookup"><span data-stu-id="2a9bf-218">GL\_PIXEL\_MAP\_A\_TO\_A</span></span> | <span data-ttu-id="2a9bf-219">A</span><span class="sxs-lookup"><span data-stu-id="2a9bf-219">A</span></span>             | <span data-ttu-id="2a9bf-220">A</span><span class="sxs-lookup"><span data-stu-id="2a9bf-220">A</span></span>             | <span data-ttu-id="2a9bf-221">1</span><span class="sxs-lookup"><span data-stu-id="2a9bf-221">1</span></span>            | <span data-ttu-id="2a9bf-222">0,0</span><span class="sxs-lookup"><span data-stu-id="2a9bf-222">0.0</span></span>           |



 

<span data-ttu-id="2a9bf-223">Le funzioni seguenti consentono di recuperare informazioni correlate a **glPixelMap**:</span><span class="sxs-lookup"><span data-stu-id="2a9bf-223">The following functions retrieve information related to **glPixelMap**:</span></span>

<span data-ttu-id="2a9bf-224">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ pixel \_ Map \_ i \_ to \_ i \_ size</span><span class="sxs-lookup"><span data-stu-id="2a9bf-224">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PIXEL\_MAP\_I\_TO\_I\_SIZE</span></span>

<span data-ttu-id="2a9bf-225">**glGet** con argomento \_ \_ di mapping GL pixel per la \_ \_ \_ \_ dimensione s</span><span class="sxs-lookup"><span data-stu-id="2a9bf-225">**glGet** with argument GL\_PIXEL\_MAP\_S\_TO\_S\_SIZE</span></span>

<span data-ttu-id="2a9bf-226">**glGet** con argomento GL \_ pixel \_ Map \_ I \_ to \_ R \_ size</span><span class="sxs-lookup"><span data-stu-id="2a9bf-226">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_R\_SIZE</span></span>

<span data-ttu-id="2a9bf-227">**glGet** con argomento GL \_ pixel \_ mapping \_ I \_ a \_ G \_ size</span><span class="sxs-lookup"><span data-stu-id="2a9bf-227">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_G\_SIZE</span></span>

<span data-ttu-id="2a9bf-228">**glGet** con argomento GL \_ pixel \_ Map \_ I \_ a \_ B \_ size</span><span class="sxs-lookup"><span data-stu-id="2a9bf-228">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_B\_SIZE</span></span>

<span data-ttu-id="2a9bf-229">**glGet** con argomento GL \_ pixel \_ mappa \_ I \_ a \_ una \_ dimensione</span><span class="sxs-lookup"><span data-stu-id="2a9bf-229">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_A\_SIZE</span></span>

<span data-ttu-id="2a9bf-230">**glGet** con argomento GL \_ pixel \_ Map \_ r \_ to \_ r \_ size</span><span class="sxs-lookup"><span data-stu-id="2a9bf-230">**glGet** with argument GL\_PIXEL\_MAP\_R\_TO\_R\_SIZE</span></span>

<span data-ttu-id="2a9bf-231">**glGet** con argomento GL \_ pixel \_ mappa \_ g \_ a \_ g \_ size</span><span class="sxs-lookup"><span data-stu-id="2a9bf-231">**glGet** with argument GL\_PIXEL\_MAP\_G\_TO\_G\_SIZE</span></span>

<span data-ttu-id="2a9bf-232">**glGet** con argomento GL \_ pixel \_ mappa \_ b \_ a \_ b \_ dimensioni</span><span class="sxs-lookup"><span data-stu-id="2a9bf-232">**glGet** with argument GL\_PIXEL\_MAP\_B\_TO\_B\_SIZE</span></span>

<span data-ttu-id="2a9bf-233">**glGet** con argomento GL \_ pixel \_ mappa \_ a \_ \_ una \_ dimensione</span><span class="sxs-lookup"><span data-stu-id="2a9bf-233">**glGet** with argument GL\_PIXEL\_MAP\_A\_TO\_A\_SIZE</span></span>

<span data-ttu-id="2a9bf-234">**glGet** con argomento \_ tabella di \_ mappa pixel max \_ \_</span><span class="sxs-lookup"><span data-stu-id="2a9bf-234">**glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE</span></span>

## <a name="requirements"></a><span data-ttu-id="2a9bf-235">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a9bf-235">Requirements</span></span>



| <span data-ttu-id="2a9bf-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a9bf-236">Requirement</span></span> | <span data-ttu-id="2a9bf-237">Valore</span><span class="sxs-lookup"><span data-stu-id="2a9bf-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a9bf-238">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a9bf-238">Minimum supported client</span></span><br/> | <span data-ttu-id="2a9bf-239">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2a9bf-239">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2a9bf-240">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a9bf-240">Minimum supported server</span></span><br/> | <span data-ttu-id="2a9bf-241">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2a9bf-241">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2a9bf-242">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a9bf-242">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a9bf-243"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bf-243"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2a9bf-244">Libreria</span><span class="sxs-lookup"><span data-stu-id="2a9bf-244">Library</span></span><br/>                  | <dl> <span data-ttu-id="2a9bf-245"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bf-245"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2a9bf-246">DLL</span><span class="sxs-lookup"><span data-stu-id="2a9bf-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a9bf-247"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a9bf-247"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a9bf-248">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a9bf-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a9bf-249">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2a9bf-249">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2a9bf-250">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="2a9bf-250">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="2a9bf-251">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="2a9bf-251">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="2a9bf-252">**Remo**</span><span class="sxs-lookup"><span data-stu-id="2a9bf-252">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2a9bf-253">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="2a9bf-253">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="2a9bf-254">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="2a9bf-254">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="2a9bf-255">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="2a9bf-255">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="2a9bf-256">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="2a9bf-256">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="2a9bf-257">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="2a9bf-257">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 






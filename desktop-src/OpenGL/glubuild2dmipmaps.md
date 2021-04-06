---
title: funzione gluBuild2DMipmaps (Glu. h)
description: La funzione gluBuild2DMipmaps crea mipmap 2D.
ms.assetid: ea19a9b0-baf7-436f-afd5-609bc364b3ba
keywords:
- funzione gluBuild2DMipmaps OpenGL
topic_type:
- apiref
api_name:
- gluBuild2DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92402792e41701711e99f469ead67410d6a8c1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963921"
---
# <a name="glubuild2dmipmaps-function"></a><span data-ttu-id="cac9a-104">gluBuild2DMipmaps (funzione)</span><span class="sxs-lookup"><span data-stu-id="cac9a-104">gluBuild2DMipmaps function</span></span>

<span data-ttu-id="cac9a-105">La funzione **gluBuild2DMipmaps** crea mipmap 2D.</span><span class="sxs-lookup"><span data-stu-id="cac9a-105">The **gluBuild2DMipmaps** function creates 2-D mipmaps.</span></span>

## <a name="syntax"></a><span data-ttu-id="cac9a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cac9a-106">Syntax</span></span>


```C++
void WINAPI gluBuild2DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLInt  height,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a><span data-ttu-id="cac9a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="cac9a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cac9a-108">*target*</span><span class="sxs-lookup"><span data-stu-id="cac9a-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="cac9a-109">Trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cac9a-109">The target texture.</span></span> <span data-ttu-id="cac9a-110">Deve essere di \_ trama GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="cac9a-110">Must be GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="cac9a-111">*componenti*</span><span class="sxs-lookup"><span data-stu-id="cac9a-111">*components*</span></span> 
</dt> <dd>

<span data-ttu-id="cac9a-112">Numero di componenti di colore nella trama.</span><span class="sxs-lookup"><span data-stu-id="cac9a-112">The number of color components in the texture.</span></span> <span data-ttu-id="cac9a-113">Deve essere 1, 2, 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="cac9a-113">Must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="cac9a-114">*width*</span><span class="sxs-lookup"><span data-stu-id="cac9a-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="cac9a-115">Larghezza dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="cac9a-115">The width of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="cac9a-116">*height*</span><span class="sxs-lookup"><span data-stu-id="cac9a-116">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="cac9a-117">Altezza dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="cac9a-117">The height of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="cac9a-118">*format*</span><span class="sxs-lookup"><span data-stu-id="cac9a-118">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="cac9a-119">Formato dei dati pixel.</span><span class="sxs-lookup"><span data-stu-id="cac9a-119">The format of the pixel data.</span></span> <span data-ttu-id="cac9a-120">Deve essere uno dei seguenti: GL \_ Color \_ index, GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Luminance o GL \_ Luminance \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="cac9a-120">Must be one of the following: GL\_COLOR\_INDEX, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, or GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="cac9a-121">*type*</span><span class="sxs-lookup"><span data-stu-id="cac9a-121">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="cac9a-122">Tipo di dati per i *dati*.</span><span class="sxs-lookup"><span data-stu-id="cac9a-122">The data type for *data*.</span></span> <span data-ttu-id="cac9a-123">Deve essere uno dei seguenti: GL \_ UNsigned \_ byte, GL \_ byte, GL \_ bitmap, GL \_ unsigned \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int o GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="cac9a-123">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="cac9a-124">*data*</span><span class="sxs-lookup"><span data-stu-id="cac9a-124">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="cac9a-125">Puntatore ai dati dell'immagine in memoria.</span><span class="sxs-lookup"><span data-stu-id="cac9a-125">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cac9a-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cac9a-126">Return value</span></span>

<span data-ttu-id="cac9a-127">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="cac9a-127">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cac9a-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="cac9a-128">Remarks</span></span>

<span data-ttu-id="cac9a-129">La funzione **gluBuild2DMipmaps** Ottiene l'immagine di input e genera tutte le immagini mipmap (usando [**gluScaleImage**](gluscaleimage.md)) in modo che l'immagine di input possa essere usata come immagine di trama mipmap.</span><span class="sxs-lookup"><span data-stu-id="cac9a-129">The **gluBuild2DMipmaps** function obtains the input image and generates all mipmap images (using [**gluScaleImage**](gluscaleimage.md)) so the input image can be used as a mipmapped texture image.</span></span> <span data-ttu-id="cac9a-130">Per caricare tutte le immagini, chiamare [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="cac9a-130">To load each of the images, call [**glTexImage2D**](glteximage2d.md).</span></span> <span data-ttu-id="cac9a-131">Se le dimensioni dell'immagine di input non sono potenze di due, l'immagine viene ridimensionata in modo che sia la larghezza che l'altezza siano le potenze di due prima che vengano generati i mipmap.</span><span class="sxs-lookup"><span data-stu-id="cac9a-131">If the dimensions of the input image are not powers of two, then the image is scaled so that both the width and height are powers of two before the mipmaps are generated.</span></span>

<span data-ttu-id="cac9a-132">Un valore restituito pari a zero indica esito positivo.</span><span class="sxs-lookup"><span data-stu-id="cac9a-132">A return value of zero indicates success.</span></span> <span data-ttu-id="cac9a-133">In caso contrario, viene restituito un codice di errore GLU (vedere [**gluErrorString**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="cac9a-133">Otherwise, a GLU error code is returned (see [**gluErrorString**](gluerrorstring.md)).</span></span>

<span data-ttu-id="cac9a-134">Per una descrizione dei valori accettabili per il parametro *Format* , vedere **glTexImage2D**.</span><span class="sxs-lookup"><span data-stu-id="cac9a-134">For a description of the acceptable values for the *format* parameter, see **glTexImage2D**.</span></span> <span data-ttu-id="cac9a-135">Per una descrizione dei valori accettabili per il *tipo*, vedere [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="cac9a-135">For a description of the acceptable values for *type*, see [**glDrawPixels**](gldrawpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cac9a-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cac9a-136">Requirements</span></span>



| <span data-ttu-id="cac9a-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="cac9a-137">Requirement</span></span> | <span data-ttu-id="cac9a-138">Valore</span><span class="sxs-lookup"><span data-stu-id="cac9a-138">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cac9a-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cac9a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="cac9a-140">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cac9a-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cac9a-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cac9a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="cac9a-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cac9a-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cac9a-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cac9a-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="cac9a-144"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="cac9a-144"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="cac9a-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="cac9a-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="cac9a-146"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cac9a-146"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cac9a-147">DLL</span><span class="sxs-lookup"><span data-stu-id="cac9a-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cac9a-148"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cac9a-148"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cac9a-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cac9a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac9a-150">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="cac9a-150">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="cac9a-151">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="cac9a-151">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="cac9a-152">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="cac9a-152">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="cac9a-153">**gluScaleImage**</span><span class="sxs-lookup"><span data-stu-id="cac9a-153">**gluScaleImage**</span></span>](gluscaleimage.md)
</dt> </dl>

 

 






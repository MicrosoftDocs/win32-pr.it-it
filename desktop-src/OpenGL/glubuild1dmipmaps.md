---
title: funzione gluBuild1DMipmaps (Glu. h)
description: La funzione gluBuild1DMipmaps crea mipmap 1-D.
ms.assetid: 52ed924f-7a72-4458-b1b8-8e5d3021f60a
keywords:
- funzione gluBuild1DMipmaps OpenGL
topic_type:
- apiref
api_name:
- gluBuild1DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 089357488c7eae18e26258018473e9008fb29d24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301356"
---
# <a name="glubuild1dmipmaps-function"></a><span data-ttu-id="8becd-104">gluBuild1DMipmaps (funzione)</span><span class="sxs-lookup"><span data-stu-id="8becd-104">gluBuild1DMipmaps function</span></span>

<span data-ttu-id="8becd-105">La funzione **gluBuild1DMipmaps** crea mipmap 1-D.</span><span class="sxs-lookup"><span data-stu-id="8becd-105">The **gluBuild1DMipmaps** function creates 1-D mipmaps.</span></span>

## <a name="syntax"></a><span data-ttu-id="8becd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8becd-106">Syntax</span></span>


```C++
void WINAPI gluBuild1DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a><span data-ttu-id="8becd-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8becd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8becd-108">*target*</span><span class="sxs-lookup"><span data-stu-id="8becd-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="8becd-109">Trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8becd-109">The target texture.</span></span> <span data-ttu-id="8becd-110">Deve essere una \_ trama GL \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="8becd-110">Must be GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="8becd-111">*componenti*</span><span class="sxs-lookup"><span data-stu-id="8becd-111">*components*</span></span> 
</dt> <dd>

<span data-ttu-id="8becd-112">Numero di componenti di colore nella trama.</span><span class="sxs-lookup"><span data-stu-id="8becd-112">The number of color components in the texture.</span></span> <span data-ttu-id="8becd-113">Deve essere 1, 2, 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="8becd-113">Must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="8becd-114">*width*</span><span class="sxs-lookup"><span data-stu-id="8becd-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="8becd-115">Larghezza dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="8becd-115">The width of the texture image.</span></span>

</dd> <dt>

<span data-ttu-id="8becd-116">*format*</span><span class="sxs-lookup"><span data-stu-id="8becd-116">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="8becd-117">Formato dei dati pixel.</span><span class="sxs-lookup"><span data-stu-id="8becd-117">The format of the pixel data.</span></span> <span data-ttu-id="8becd-118">Sono validi i valori seguenti: GL \_ Color \_ index, GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Luminance o GL \_ Luminance \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="8becd-118">The following values are valid: GL\_COLOR\_INDEX, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, or GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="8becd-119">*type*</span><span class="sxs-lookup"><span data-stu-id="8becd-119">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="8becd-120">Tipo di dati per i *dati*.</span><span class="sxs-lookup"><span data-stu-id="8becd-120">The data type for *data*.</span></span> <span data-ttu-id="8becd-121">I valori seguenti sono validi: GL \_ UNsigned \_ byte, GL \_ byte, GL \_ bitmap, GL \_ unsigned \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int o GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="8becd-121">The following values are valid: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="8becd-122">*data*</span><span class="sxs-lookup"><span data-stu-id="8becd-122">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="8becd-123">Puntatore ai dati dell'immagine in memoria.</span><span class="sxs-lookup"><span data-stu-id="8becd-123">A pointer to the image data in memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8becd-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8becd-124">Return value</span></span>

<span data-ttu-id="8becd-125">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="8becd-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8becd-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="8becd-126">Remarks</span></span>

<span data-ttu-id="8becd-127">La funzione **gluBuild1DMipmaps** Ottiene l'immagine di input e genera tutte le immagini mipmap (usando [**gluScaleImage**](gluscaleimage.md)) in modo che l'immagine di input possa essere usata come immagine di trama mipmap.</span><span class="sxs-lookup"><span data-stu-id="8becd-127">The **gluBuild1DMipmaps** function obtains the input image and generates all mipmap images (using [**gluScaleImage**](gluscaleimage.md)) so that the input image can be used as a mipmapped texture image.</span></span> <span data-ttu-id="8becd-128">Viene quindi chiamata la funzione [**glTexImage1D**](glteximage1d.md) per caricare ogni immagine.</span><span class="sxs-lookup"><span data-stu-id="8becd-128">The [**glTexImage1D**](glteximage1d.md) function is then called to load each of the images.</span></span> <span data-ttu-id="8becd-129">Se la larghezza dell'immagine di input non è una potenza di due, l'immagine viene ridimensionata alla potenza più vicina di due prima che vengano generati i mipmap.</span><span class="sxs-lookup"><span data-stu-id="8becd-129">If the width of the input image is not a power of two, then the image is scaled to the nearest power of two before the mipmaps are generated.</span></span>

<span data-ttu-id="8becd-130">Un valore restituito pari a zero indica esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8becd-130">A return value of zero indicates success.</span></span> <span data-ttu-id="8becd-131">In caso contrario, viene restituito un codice di errore GLU (vedere [**gluErrorString**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="8becd-131">Otherwise, a GLU error code is returned (see [**gluErrorString**](gluerrorstring.md)).</span></span>

<span data-ttu-id="8becd-132">Per una descrizione dei valori accettabili per il parametro *Format* , vedere **glTexImage1D**.</span><span class="sxs-lookup"><span data-stu-id="8becd-132">For a description of the acceptable values for the *format* parameter, see **glTexImage1D**.</span></span> <span data-ttu-id="8becd-133">Per una descrizione dei valori accettabili per il parametro di *tipo* , vedere [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="8becd-133">For a description of the acceptable values for the *type* parameter, see [**glDrawPixels**](gldrawpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8becd-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8becd-134">Requirements</span></span>



| <span data-ttu-id="8becd-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="8becd-135">Requirement</span></span> | <span data-ttu-id="8becd-136">Valore</span><span class="sxs-lookup"><span data-stu-id="8becd-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8becd-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8becd-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8becd-138">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8becd-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8becd-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8becd-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8becd-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8becd-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8becd-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8becd-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="8becd-142"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="8becd-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="8becd-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="8becd-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="8becd-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8becd-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8becd-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8becd-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8becd-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8becd-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8becd-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8becd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8becd-148">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="8becd-148">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="8becd-149">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="8becd-149">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="8becd-150">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="8becd-150">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="8becd-151">**gluScaleImage**</span><span class="sxs-lookup"><span data-stu-id="8becd-151">**gluScaleImage**</span></span>](gluscaleimage.md)
</dt> </dl>

 

 






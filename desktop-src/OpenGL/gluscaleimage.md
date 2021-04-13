---
title: funzione gluScaleImage (Glu. h)
description: La funzione gluScaleImage ridimensiona un'immagine a una dimensione arbitraria.
ms.assetid: f47191e8-b22d-4f6a-949a-9c7782d6d338
keywords:
- funzione gluScaleImage OpenGL
topic_type:
- apiref
api_name:
- gluScaleImage
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da95f1545996a83adeb27deaceb7fab6290005e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400213"
---
# <a name="gluscaleimage-function"></a><span data-ttu-id="df48d-104">gluScaleImage (funzione)</span><span class="sxs-lookup"><span data-stu-id="df48d-104">gluScaleImage function</span></span>

<span data-ttu-id="df48d-105">La funzione **gluScaleImage** ridimensiona un'immagine a una dimensione arbitraria.</span><span class="sxs-lookup"><span data-stu-id="df48d-105">The **gluScaleImage** function scales an image to an arbitrary size.</span></span>

## <a name="syntax"></a><span data-ttu-id="df48d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df48d-106">Syntax</span></span>


```C++
int WINAPI gluScaleImage(
         GLenum format,
         GLint  widthin,
         GLint  heightin,
         GLenum typein,
   const void   *datain,
         GLint  widthout,
         GLint  heightout,
         GLenum typeout,
         void   *dataout
);
```



## <a name="parameters"></a><span data-ttu-id="df48d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="df48d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df48d-108">*format*</span><span class="sxs-lookup"><span data-stu-id="df48d-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="df48d-109">Formato dei dati pixel.</span><span class="sxs-lookup"><span data-stu-id="df48d-109">The format of the pixel data.</span></span> <span data-ttu-id="df48d-110">Sono validi i valori simbolici seguenti: GL \_ Color \_ index, GL \_ stencil \_ index, GL \_ Depth \_ Component, GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ BGR \_ ext, GL \_ BGRA \_ ext, GL \_ Luminance e GL \_ Luminance \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="df48d-110">The following symbolic values are valid: GL\_COLOR\_INDEX, GL\_STENCIL\_INDEX, GL\_DEPTH\_COMPONENT, GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_BGR\_EXT, GL\_BGRA\_EXT, GL\_LUMINANCE, and GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="df48d-111">*Larghezza*</span><span class="sxs-lookup"><span data-stu-id="df48d-111">*widthin*</span></span> 
</dt> <dd>

<span data-ttu-id="df48d-112">Larghezza dell'immagine di origine ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="df48d-112">The width of the source image that is scaled.</span></span>

</dd> <dt>

<span data-ttu-id="df48d-113">*altezza*</span><span class="sxs-lookup"><span data-stu-id="df48d-113">*heightin*</span></span> 
</dt> <dd>

<span data-ttu-id="df48d-114">Altezza dell'immagine di origine ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="df48d-114">The height of the source image that is scaled.</span></span>

</dd> <dt>

<span data-ttu-id="df48d-115">*typein*</span><span class="sxs-lookup"><span data-stu-id="df48d-115">*typein*</span></span> 
</dt> <dd>

<span data-ttu-id="df48d-116">Tipo di dati per *dataIn*.</span><span class="sxs-lookup"><span data-stu-id="df48d-116">The data type for *datain*.</span></span> <span data-ttu-id="df48d-117">Deve essere uno dei seguenti: GL \_ UNsigned \_ byte, GL \_ byte, GL \_ bitmap, GL \_ unsigned \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int o GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="df48d-117">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="df48d-118">*dataIn*</span><span class="sxs-lookup"><span data-stu-id="df48d-118">*datain*</span></span> 
</dt> <dd>

<span data-ttu-id="df48d-119">Puntatore all'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="df48d-119">A pointer to the source image.</span></span>

</dd> <dt>

<span data-ttu-id="df48d-120">*Larghezza*</span><span class="sxs-lookup"><span data-stu-id="df48d-120">*widthout*</span></span> 
</dt> <dd>

<span data-ttu-id="df48d-121">Larghezza dell'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="df48d-121">The width of the destination image.</span></span>

</dd> <dt>

<span data-ttu-id="df48d-122">*altezza*</span><span class="sxs-lookup"><span data-stu-id="df48d-122">*heightout*</span></span> 
</dt> <dd>

<span data-ttu-id="df48d-123">Altezza dell'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="df48d-123">The height of the destination image.</span></span>

</dd> <dt>

<span data-ttu-id="df48d-124">*digitare*</span><span class="sxs-lookup"><span data-stu-id="df48d-124">*typeout*</span></span> 
</dt> <dd>

<span data-ttu-id="df48d-125">Tipo di dati per i *dati*.</span><span class="sxs-lookup"><span data-stu-id="df48d-125">The data type for *dataout*.</span></span> <span data-ttu-id="df48d-126">Deve essere uno dei seguenti: GL \_ UNsigned \_ byte, GL \_ byte, GL \_ bitmap, GL \_ unsigned \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int o GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="df48d-126">Must be one of the following: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_BITMAP, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, or GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="df48d-127">*dati*</span><span class="sxs-lookup"><span data-stu-id="df48d-127">*dataout*</span></span> 
</dt> <dd>

<span data-ttu-id="df48d-128">Puntatore all'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="df48d-128">A pointer to the destination image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df48d-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df48d-129">Return value</span></span>

<span data-ttu-id="df48d-130">Se la funzione ha esito positivo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="df48d-130">If the function succeeds, the return value is zero.</span></span>

<span data-ttu-id="df48d-131">Se la funzione ha esito negativo, il valore restituito è un codice di errore GLU (vedere [**gluErrorString**](gluerrorstring.md)).</span><span class="sxs-lookup"><span data-stu-id="df48d-131">If the function fails, the return value is a GLU error code (see [**gluErrorString**](gluerrorstring.md)).</span></span>

## <a name="remarks"></a><span data-ttu-id="df48d-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="df48d-132">Remarks</span></span>

<span data-ttu-id="df48d-133">La funzione **gluScaleImage** ridimensiona un'immagine pixel usando le modalità di archivio pixel appropriate per decomprimere i dati dall'immagine di origine e comprimere i dati nell'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="df48d-133">The **gluScaleImage** function scales a pixel image using the appropriate pixel store modes to unpack data from the source image and pack data into the destination image.</span></span>

<span data-ttu-id="df48d-134">Quando si compatta un'immagine, **gluScaleImage** usa un filtro Box per campionare l'immagine di origine e creare i pixel per l'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="df48d-134">When shrinking an image, **gluScaleImage** uses a box filter to sample the source image and create pixels for the destination image.</span></span> <span data-ttu-id="df48d-135">Quando si ingrandisce un'immagine, i pixel dell'immagine di origine vengono interpolati linearmente per creare l'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="df48d-135">When magnifying an image, the pixels from the source image are linearly interpolated to create the destination image.</span></span>

<span data-ttu-id="df48d-136">Per una descrizione dei valori accettabili per il *formato*, *digitare* *e digitare i parametri,* vedere [**glReadPixels**](glreadpixels.md).</span><span class="sxs-lookup"><span data-stu-id="df48d-136">For a description of the acceptable values for the *format*, *typein*, and *typeout* parameters, see [**glReadPixels**](glreadpixels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df48d-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df48d-137">Requirements</span></span>



| <span data-ttu-id="df48d-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="df48d-138">Requirement</span></span> | <span data-ttu-id="df48d-139">Valore</span><span class="sxs-lookup"><span data-stu-id="df48d-139">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="df48d-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df48d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="df48d-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="df48d-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="df48d-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df48d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="df48d-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="df48d-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="df48d-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df48d-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="df48d-145"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="df48d-145"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="df48d-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="df48d-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="df48d-147"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df48d-147"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="df48d-148">DLL</span><span class="sxs-lookup"><span data-stu-id="df48d-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df48d-149"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df48d-149"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df48d-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df48d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df48d-151">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="df48d-151">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="df48d-152">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="df48d-152">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="df48d-153">**gluBuild1DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="df48d-153">**gluBuild1DMipmaps**</span></span>](glubuild1dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="df48d-154">**gluBuild2DMipmaps**</span><span class="sxs-lookup"><span data-stu-id="df48d-154">**gluBuild2DMipmaps**</span></span>](glubuild2dmipmaps.md)
</dt> <dt>

[<span data-ttu-id="df48d-155">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="df48d-155">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> </dl>

 

 






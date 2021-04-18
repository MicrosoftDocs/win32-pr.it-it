---
title: funzione glGetTexImage (GL. h)
description: La funzione glGetTexImage restituisce un'immagine di trama.
ms.assetid: d7235df4-2dd8-4537-aadd-284c130a3f99
keywords:
- funzione glGetTexImage OpenGL
topic_type:
- apiref
api_name:
- glGetTexImage
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da38ca1d6605fdc3cd6cf73cdd017404b71961e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302500"
---
# <a name="glgetteximage-function"></a><span data-ttu-id="00d6e-104">glGetTexImage (funzione)</span><span class="sxs-lookup"><span data-stu-id="00d6e-104">glGetTexImage function</span></span>

<span data-ttu-id="00d6e-105">La funzione **glGetTexImage** restituisce un'immagine di trama.</span><span class="sxs-lookup"><span data-stu-id="00d6e-105">The **glGetTexImage** function returns a texture image.</span></span>

## <a name="syntax"></a><span data-ttu-id="00d6e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00d6e-106">Syntax</span></span>


```C++
void WINAPI glGetTexImage(
   GLenum target,
   GLint  level,
   GLenum format,
   GLenum type,
   GLvoid *pixels
);
```



## <a name="parameters"></a><span data-ttu-id="00d6e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="00d6e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00d6e-108">*target*</span><span class="sxs-lookup"><span data-stu-id="00d6e-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="00d6e-109">Specifica la trama da ottenere.</span><span class="sxs-lookup"><span data-stu-id="00d6e-109">Specifies which texture is to be obtained.</span></span> <span data-ttu-id="00d6e-110">\_ \_ Viene accettata la trama GL 1D e GL \_ texture \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="00d6e-110">GL\_TEXTURE\_1D and GL\_TEXTURE\_2D are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="00d6e-111">*level*</span><span class="sxs-lookup"><span data-stu-id="00d6e-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="00d6e-112">Il numero del livello di dettaglio dell'immagine desiderata.</span><span class="sxs-lookup"><span data-stu-id="00d6e-112">The level-of-detail number of the desired image.</span></span> <span data-ttu-id="00d6e-113">Il livello 0 è il livello dell'immagine di base.</span><span class="sxs-lookup"><span data-stu-id="00d6e-113">Level 0 is the base image level.</span></span> <span data-ttu-id="00d6e-114">Il livello *n* è l'immagine di riduzione del mipmap *n*.</span><span class="sxs-lookup"><span data-stu-id="00d6e-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="00d6e-115">*format*</span><span class="sxs-lookup"><span data-stu-id="00d6e-115">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="00d6e-116">Formato pixel per i dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="00d6e-116">A pixel format for the returned data.</span></span> <span data-ttu-id="00d6e-117">I formati supportati sono GL \_ Red, GL \_ Green, GL \_ Blue, GL \_ Alpha, GL \_ RGB, GL \_ RGBA, GL \_ Luminance, GL \_ BGR \_ ext, GL \_ BGRA \_ ext e GL \_ Luminance \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="00d6e-117">The supported formats are GL\_RED, GL\_GREEN, GL\_BLUE, GL\_ALPHA, GL\_RGB, GL\_RGBA, GL\_LUMINANCE, GL\_BGR\_EXT, GL\_BGRA\_EXT, and GL\_LUMINANCE\_ALPHA.</span></span>

</dd> <dt>

<span data-ttu-id="00d6e-118">*type*</span><span class="sxs-lookup"><span data-stu-id="00d6e-118">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="00d6e-119">Tipo di pixel per i dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="00d6e-119">A pixel type for the returned data.</span></span> <span data-ttu-id="00d6e-120">I tipi supportati sono GL \_ UNsigned \_ byte, GL \_ byte, GL unsigned \_ \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int e GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="00d6e-120">The supported types are GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

</dd> <dt>

<span data-ttu-id="00d6e-121">*pixel*</span><span class="sxs-lookup"><span data-stu-id="00d6e-121">*pixels*</span></span> 
</dt> <dd>

<span data-ttu-id="00d6e-122">Restituisce l'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="00d6e-122">Returns the texture image.</span></span> <span data-ttu-id="00d6e-123">Deve essere un puntatore a una matrice del tipo specificato dal *tipo*.</span><span class="sxs-lookup"><span data-stu-id="00d6e-123">Should be a pointer to an array of the type specified by *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00d6e-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00d6e-124">Return value</span></span>

<span data-ttu-id="00d6e-125">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="00d6e-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="00d6e-126">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="00d6e-126">Error codes</span></span>

<span data-ttu-id="00d6e-127">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="00d6e-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="00d6e-128">Nome</span><span class="sxs-lookup"><span data-stu-id="00d6e-128">Name</span></span>                                                                                                  | <span data-ttu-id="00d6e-129">Significato</span><span class="sxs-lookup"><span data-stu-id="00d6e-129">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="00d6e-130"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="00d6e-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="00d6e-131">la *destinazione*, il *formato* o il *tipo* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="00d6e-131">*target*, *format*, or *type* was not an accepted value.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="00d6e-132"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="00d6e-132"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="00d6e-133">il *livello* è minore di zero o maggiore di *log* 2 (*Max*), dove *Max* è il valore restituito della \_ dimensione della trama GL Max \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="00d6e-133">*level* is less than zero or greater than *log* 2 (*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>      |
| <dl> <span data-ttu-id="00d6e-134"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="00d6e-134"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="00d6e-135">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md) .</span><span class="sxs-lookup"><span data-stu-id="00d6e-135">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md) .</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="00d6e-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="00d6e-136">Remarks</span></span>

<span data-ttu-id="00d6e-137">La funzione **glGetTexImage** restituisce un'immagine di trama in *pixel*.</span><span class="sxs-lookup"><span data-stu-id="00d6e-137">The **glGetTexImage** function returns a texture image into *pixels*.</span></span> <span data-ttu-id="00d6e-138">Il parametro di *destinazione* specifica se l'immagine di trama desiderata è una specificata da [**glTexImage1D**](glteximage1d.md)**(** GL \_ texture \_ 1D **)** o da [**glTexImage2D**](glteximage2d.md)**(** GL \_ trama \_ 2D **)**.</span><span class="sxs-lookup"><span data-stu-id="00d6e-138">The *target* parameter specifies whether the desired texture image is one specified by [**glTexImage1D**](glteximage1d.md)**(** GL\_TEXTURE\_1D **)** or by [**glTexImage2D**](glteximage2d.md)**(** GL\_TEXTURE\_2D **)**.</span></span> <span data-ttu-id="00d6e-139">Il parametro *Level* specifica il numero del livello di dettaglio dell'immagine desiderata.</span><span class="sxs-lookup"><span data-stu-id="00d6e-139">The *level* parameter specifies the level-of-detail number of the desired image.</span></span> <span data-ttu-id="00d6e-140">Il *formato* e i parametri di *tipo* specificano il formato e il tipo della matrice di immagini desiderata.</span><span class="sxs-lookup"><span data-stu-id="00d6e-140">The *format* and *type* parameters specify the format and type of the desired image array.</span></span> <span data-ttu-id="00d6e-141">Per una descrizione dei valori accettabili per i parametri *Format* e *Type* , vedere rispettivamente **glTexImage1D** e [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="00d6e-141">For a description of the acceptable values for the *format* and *type* parameters, respectively, see **glTexImage1D** and [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="00d6e-142">Il funzionamento di **glGetTexImage** è ottimale, considerando che l'immagine della trama a quattro componenti interna selezionata è un buffer di colore RGBA dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="00d6e-142">Operation of **glGetTexImage** is best understood by considering the selected internal four-component texture image to be an RGBA color buffer the size of the image.</span></span> <span data-ttu-id="00d6e-143">La semantica di **glGetTexImage** è quindi identica a quella di [**glReadPixels**](glreadpixels.md) chiamata con lo stesso *formato* e *tipo*, con *x* e *y* impostati su zero, *Width* impostato sulla larghezza dell'immagine della trama (incluso il bordo se ne è stato specificato uno) e *Height* impostato su uno per le immagini 1-d o sull'altezza dell'immagine della trama (incluso il bordo, se ne è stato specificato uno) per le immagini 2D.</span><span class="sxs-lookup"><span data-stu-id="00d6e-143">The semantics of **glGetTexImage** are then identical to those of [**glReadPixels**](glreadpixels.md) called with the same *format* and *type*, with *x* and *y* set to zero, *width* set to the width of the texture image (including border if one was specified), and *height* set to one for 1-D images, or to the height of the texture image (including border, if one was specified) for 2-D images.</span></span>

<span data-ttu-id="00d6e-144">Poiché l'immagine di trama interna è un'immagine RGBA, i formati di pixel GL \_ \_ index, GL \_ stencil \_ index e GL \_ Depth \_ Component non vengono accettati e il tipo di pixel \_ bitmap GL non viene accettato.</span><span class="sxs-lookup"><span data-stu-id="00d6e-144">Because the internal texture image is an RGBA image, pixel formats GL\_COLOR\_INDEX, GL\_STENCIL\_INDEX, and GL\_DEPTH\_COMPONENT are not accepted, and pixel type GL\_BITMAP is not accepted.</span></span>

<span data-ttu-id="00d6e-145">Se l'immagine di trama selezionata non contiene quattro componenti, vengono applicati i mapping seguenti.</span><span class="sxs-lookup"><span data-stu-id="00d6e-145">If the selected texture image does not contain four components, the following mappings are applied.</span></span> <span data-ttu-id="00d6e-146">Le trame a singolo componente vengono considerate come buffer RGBA con il rosso impostato sul valore del singolo componente, verde, blu e alfa impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="00d6e-146">Single-component textures are treated as RGBA buffers with red set to the single-component value, and green, blue, and alpha set to zero.</span></span>

<span data-ttu-id="00d6e-147">Le trame a due componenti vengono considerate come buffer RGBA, con rosso impostato sul valore di Component zero, Alpha impostato sul valore di Component One e verde e blu impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="00d6e-147">Two-component textures are treated as RGBA buffers, with red set to the value of component zero, alpha set to the value of component one, and green and blue set to zero.</span></span> <span data-ttu-id="00d6e-148">Infine, le trame a tre componenti vengono considerate come buffer RGBA con il rosso impostato sul componente zero, il verde impostato sul componente uno, il blu impostato sul componente due e l'alfa impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="00d6e-148">Finally, three-component textures are treated as RGBA buffers with red set to component zero, green set to component one, blue set to component two, and alpha set to zero.</span></span>

<span data-ttu-id="00d6e-149">Per determinare le dimensioni richieste dei *pixel*, usare [**glGetTexLevelParameter**](glgettexlevelparameter.md) per verificare le dimensioni dell'immagine di trama interna, quindi ridimensionare il numero necessario di pixel in base allo spazio di archiviazione necessario per ogni pixel, in base al *formato* e al *tipo*.</span><span class="sxs-lookup"><span data-stu-id="00d6e-149">To determine the required size of *pixels*, use [**glGetTexLevelParameter**](glgettexlevelparameter.md) to ascertain the dimensions of the internal texture image, and then scale the required number of pixels by the storage required for each pixel, based on *format* and *type*.</span></span> <span data-ttu-id="00d6e-150">Assicurarsi di prendere in considerazione i parametri di archiviazione in pixel, in particolare l'allineamento di GL \_ pack \_ .</span><span class="sxs-lookup"><span data-stu-id="00d6e-150">Be sure to take the pixel-storage parameters into account, especially GL\_PACK\_ALIGNMENT.</span></span>

<span data-ttu-id="00d6e-151">Se viene generato un errore, non viene apportata alcuna modifica al contenuto dei *pixel*.</span><span class="sxs-lookup"><span data-stu-id="00d6e-151">If an error is generated, no change is made to the contents of *pixels*.</span></span>

<span data-ttu-id="00d6e-152">Le funzioni seguenti consentono di recuperare informazioni correlate a **glGetTexImage**:</span><span class="sxs-lookup"><span data-stu-id="00d6e-152">The following functions retrieve information related to **glGetTexImage**:</span></span>

<span data-ttu-id="00d6e-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ allineamento GL Pack \_ e altri</span><span class="sxs-lookup"><span data-stu-id="00d6e-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PACK\_ALIGNMENT and others</span></span>

<span data-ttu-id="00d6e-154">[**glGetTexLevelParameter**](glgettexlevelparameter.md) con argomento \_ spessore trama \_ GL</span><span class="sxs-lookup"><span data-stu-id="00d6e-154">[**glGetTexLevelParameter**](glgettexlevelparameter.md) with argument GL\_TEXTURE\_WIDTH</span></span>

<span data-ttu-id="00d6e-155">**glGetTexLevelParameter** con \_ altezza trama GL \_ argomento</span><span class="sxs-lookup"><span data-stu-id="00d6e-155">**glGetTexLevelParameter** with argument GL\_TEXTURE\_HEIGHT</span></span>

<span data-ttu-id="00d6e-156">**glGetTexLevelParameter** con \_ bordo trama GL \_ argomento</span><span class="sxs-lookup"><span data-stu-id="00d6e-156">**glGetTexLevelParameter** with argument GL\_TEXTURE\_BORDER</span></span>

<span data-ttu-id="00d6e-157">**glGetTexLevelParameter** con l'argomento \_ componenti di trama GL \_</span><span class="sxs-lookup"><span data-stu-id="00d6e-157">**glGetTexLevelParameter** with argument GL\_TEXTURE\_COMPONENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="00d6e-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00d6e-158">Requirements</span></span>



| <span data-ttu-id="00d6e-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="00d6e-159">Requirement</span></span> | <span data-ttu-id="00d6e-160">Valore</span><span class="sxs-lookup"><span data-stu-id="00d6e-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00d6e-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00d6e-161">Minimum supported client</span></span><br/> | <span data-ttu-id="00d6e-162">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00d6e-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="00d6e-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00d6e-163">Minimum supported server</span></span><br/> | <span data-ttu-id="00d6e-164">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00d6e-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="00d6e-165">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00d6e-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="00d6e-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="00d6e-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="00d6e-167">Libreria</span><span class="sxs-lookup"><span data-stu-id="00d6e-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="00d6e-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00d6e-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="00d6e-169">DLL</span><span class="sxs-lookup"><span data-stu-id="00d6e-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00d6e-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00d6e-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00d6e-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00d6e-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00d6e-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="00d6e-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="00d6e-173">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="00d6e-173">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="00d6e-174">**Remo**</span><span class="sxs-lookup"><span data-stu-id="00d6e-174">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="00d6e-175">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="00d6e-175">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="00d6e-176">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="00d6e-176">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="00d6e-177">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="00d6e-177">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="00d6e-178">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="00d6e-178">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 






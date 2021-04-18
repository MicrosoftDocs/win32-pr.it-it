---
title: funzione glShadeModel (GL. h)
description: La funzione glShadeModel seleziona l'ombreggiatura piatta o smussata.
ms.assetid: 52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e
keywords:
- funzione glShadeModel OpenGL
topic_type:
- apiref
api_name:
- glShadeModel
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142ac518c91c6378f1606235e25502be8c06dd6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301460"
---
# <a name="glshademodel-function"></a><span data-ttu-id="13358-104">glShadeModel (funzione)</span><span class="sxs-lookup"><span data-stu-id="13358-104">glShadeModel function</span></span>

<span data-ttu-id="13358-105">La funzione **glShadeModel** seleziona l'ombreggiatura piatta o smussata.</span><span class="sxs-lookup"><span data-stu-id="13358-105">The **glShadeModel** function selects flat or smooth shading.</span></span>

## <a name="syntax"></a><span data-ttu-id="13358-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13358-106">Syntax</span></span>


```C++
void WINAPI glShadeModel(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="13358-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="13358-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13358-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="13358-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="13358-109">Valore simbolico che rappresenta una tecnica di ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="13358-109">A symbolic value representing a shading technique.</span></span> <span data-ttu-id="13358-110">I valori accettati sono GL \_ flat e GL \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="13358-110">Accepted values are GL\_FLAT and GL\_SMOOTH.</span></span> <span data-ttu-id="13358-111">Il valore predefinito è GL \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="13358-111">The default is GL\_SMOOTH.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13358-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13358-112">Return value</span></span>

<span data-ttu-id="13358-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="13358-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="13358-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="13358-114">Error codes</span></span>

<span data-ttu-id="13358-115">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="13358-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="13358-116">Nome</span><span class="sxs-lookup"><span data-stu-id="13358-116">Name</span></span>                                                                                                  | <span data-ttu-id="13358-117">Significato</span><span class="sxs-lookup"><span data-stu-id="13358-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="13358-118"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="13358-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="13358-119">*mode* è un valore diverso da GL \_ glat o GL \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="13358-119">*mode* was a value other than GL\_GLAT or GL\_SMOOTH.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="13358-120"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="13358-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="13358-121">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="13358-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="13358-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="13358-122">Remarks</span></span>

<span data-ttu-id="13358-123">Le primitive OpenGL possono avere ombreggiatura piatta o smussata.</span><span class="sxs-lookup"><span data-stu-id="13358-123">OpenGL primitives can have either flat or smooth shading.</span></span> <span data-ttu-id="13358-124">L'ombreggiatura uniforme, il valore predefinito, causa l'interpolazione dei colori calcolati dei vertici quando la primitiva viene rasterizzata, assegnando in genere colori diversi a ogni frammento di pixel risultante.</span><span class="sxs-lookup"><span data-stu-id="13358-124">Smooth shading, the default, causes the computed colors of vertices to be interpolated as the primitive is rasterized, typically assigning different colors to each resulting pixel fragment.</span></span> <span data-ttu-id="13358-125">Ombreggiatura piatta consente di selezionare il colore calcolato di un solo vertice e di assegnarlo a tutti i frammenti di pixel generati dalla rasterizzazione di una singola primitiva.</span><span class="sxs-lookup"><span data-stu-id="13358-125">Flat shading selects the computed color of just one vertex and assigns it to all the pixel fragments generated by rasterizing a single primitive.</span></span> <span data-ttu-id="13358-126">In entrambi i casi, il colore calcolato di un vertice è il risultato dell'illuminazione, se l'illuminazione è abilitata o è il colore corrente al momento in cui è stato specificato il vertice, se l'illuminazione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="13358-126">In either case, the computed color of a vertex is the result of lighting, if lighting is enabled, or it is the current color at the time the vertex was specified, if lighting is disabled.</span></span>

<span data-ttu-id="13358-127">L'ombreggiatura piatta e liscia non è distinguibile per i punti.</span><span class="sxs-lookup"><span data-stu-id="13358-127">Flat and smooth shading are indistinguishable for points.</span></span> <span data-ttu-id="13358-128">Conteggio dei vertici e delle primitive da uno, a partire dal momento in cui viene emesso [**glBegin**](glbegin.md) , ogni segmento di linea ombreggiato a *cui* viene assegnato il colore calcolato del vertice *i* + 1, il secondo vertice.</span><span class="sxs-lookup"><span data-stu-id="13358-128">Counting vertices and primitives from one, starting when [**glBegin**](glbegin.md) is issued, each flat-shaded line segment *i* is given the computed color of vertex *i* + 1, its second vertex.</span></span> <span data-ttu-id="13358-129">Per il conteggio analogo da uno, a ogni poligono ombreggiato viene assegnato il colore calcolato del vertice elencato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="13358-129">Counting similarly from one, each flat-shaded polygon is given the computed color of the vertex listed in the following table.</span></span> <span data-ttu-id="13358-130">Si tratta dell'ultimo vertice che consente di specificare il poligono in tutti i casi tranne i poligoni singoli, in cui il primo vertice specifica il colore con ombreggiatura piatta.</span><span class="sxs-lookup"><span data-stu-id="13358-130">This is the last vertex to specify the polygon in all cases except single polygons, where the first vertex specifies the flat-shaded color.</span></span>



| <span data-ttu-id="13358-131">Tipo primitivo del poligono i</span><span class="sxs-lookup"><span data-stu-id="13358-131">Primitive type of polygon i</span></span> | <span data-ttu-id="13358-132">Vertice</span><span class="sxs-lookup"><span data-stu-id="13358-132">Vertex</span></span>   |
|-----------------------------|----------|
| <span data-ttu-id="13358-133">Poligono singolo (*I*= 1)</span><span class="sxs-lookup"><span data-stu-id="13358-133">Single polygon (*I*=1)</span></span>      | <span data-ttu-id="13358-134">1</span><span class="sxs-lookup"><span data-stu-id="13358-134">1</span></span>        |
| <span data-ttu-id="13358-135">Striscia triangolare</span><span class="sxs-lookup"><span data-stu-id="13358-135">Triangle strip</span></span>              | <span data-ttu-id="13358-136">*i* + 2</span><span class="sxs-lookup"><span data-stu-id="13358-136">*i* + 2</span></span>  |
| <span data-ttu-id="13358-137">Ventola triangolo</span><span class="sxs-lookup"><span data-stu-id="13358-137">Triangle fan</span></span>                | <span data-ttu-id="13358-138">*i* + 2</span><span class="sxs-lookup"><span data-stu-id="13358-138">*i* + 2</span></span>  |
| <span data-ttu-id="13358-139">Triangolo indipendente</span><span class="sxs-lookup"><span data-stu-id="13358-139">Independent triangle</span></span>        | <span data-ttu-id="13358-140">3 *I*</span><span class="sxs-lookup"><span data-stu-id="13358-140">3 *I*</span></span>     |
| <span data-ttu-id="13358-141">Striping quad</span><span class="sxs-lookup"><span data-stu-id="13358-141">Quad strip</span></span>                  | <span data-ttu-id="13358-142">2 *i* + 2</span><span class="sxs-lookup"><span data-stu-id="13358-142">2 *i* + 2</span></span> |
| <span data-ttu-id="13358-143">Quad indipendente</span><span class="sxs-lookup"><span data-stu-id="13358-143">Independent quad</span></span>            | <span data-ttu-id="13358-144">4 *I*</span><span class="sxs-lookup"><span data-stu-id="13358-144">4 *I*</span></span>     |



 

<span data-ttu-id="13358-145">Le ombreggiature flat e Smooth vengono specificate da **glShadeModel** con la *modalità* impostata rispettivamente su GL \_ flat e GL \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="13358-145">Flat and smooth shading are specified by **glShadeModel** with *mode* set to GL\_FLAT and GL\_SMOOTH, respectively.</span></span>

<span data-ttu-id="13358-146">La funzione seguente recupera le informazioni correlate a **glShadeModel**:</span><span class="sxs-lookup"><span data-stu-id="13358-146">The following function retrieves information related to **glShadeModel**:</span></span>

<span data-ttu-id="13358-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ modello di ombreggiatura GL \_</span><span class="sxs-lookup"><span data-stu-id="13358-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_SHADE\_MODEL</span></span>

## <a name="requirements"></a><span data-ttu-id="13358-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13358-148">Requirements</span></span>



| <span data-ttu-id="13358-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="13358-149">Requirement</span></span> | <span data-ttu-id="13358-150">Valore</span><span class="sxs-lookup"><span data-stu-id="13358-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13358-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13358-151">Minimum supported client</span></span><br/> | <span data-ttu-id="13358-152">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="13358-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="13358-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13358-153">Minimum supported server</span></span><br/> | <span data-ttu-id="13358-154">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="13358-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="13358-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13358-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="13358-156"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="13358-156"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="13358-157">Libreria</span><span class="sxs-lookup"><span data-stu-id="13358-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="13358-158"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13358-158"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="13358-159">DLL</span><span class="sxs-lookup"><span data-stu-id="13358-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13358-160"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13358-160"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13358-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13358-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13358-162">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="13358-162">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="13358-163">**glColor**</span><span class="sxs-lookup"><span data-stu-id="13358-163">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="13358-164">**Remo**</span><span class="sxs-lookup"><span data-stu-id="13358-164">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="13358-165">**glLight**</span><span class="sxs-lookup"><span data-stu-id="13358-165">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="13358-166">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="13358-166">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 






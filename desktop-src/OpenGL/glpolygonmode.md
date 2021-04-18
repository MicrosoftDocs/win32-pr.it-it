---
title: funzione glPolygonMode (GL. h)
description: La funzione glPolygonMode seleziona una modalità di rasterizzazione poligonale.
ms.assetid: d8781bae-e78c-40fb-9f33-c742c70ebda1
keywords:
- funzione glPolygonMode OpenGL
topic_type:
- apiref
api_name:
- glPolygonMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d133243c1655432842a939b8da0f3a981fdffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302707"
---
# <a name="glpolygonmode-function"></a><span data-ttu-id="45123-104">glPolygonMode (funzione)</span><span class="sxs-lookup"><span data-stu-id="45123-104">glPolygonMode function</span></span>

<span data-ttu-id="45123-105">La funzione **glPolygonMode** seleziona una modalità di rasterizzazione poligonale.</span><span class="sxs-lookup"><span data-stu-id="45123-105">The **glPolygonMode** function selects a polygon rasterization mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="45123-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45123-106">Syntax</span></span>


```C++
void WINAPI glPolygonMode(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="45123-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="45123-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45123-108">*faccia*</span><span class="sxs-lookup"><span data-stu-id="45123-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="45123-109">Poligoni a cui si applica la *modalità* .</span><span class="sxs-lookup"><span data-stu-id="45123-109">The polygons that *mode* applies to.</span></span> <span data-ttu-id="45123-110">Deve essere di \_ primo piano per i poligoni in primo piano, GL \_ indietro per i poligoni di back-end o GL \_ front \_ e \_ back per i poligoni anteriori e di back-end.</span><span class="sxs-lookup"><span data-stu-id="45123-110">Must be GL\_FRONT for front-facing polygons, GL\_BACK for back-facing polygons, or GL\_FRONT\_AND\_BACK for front- and back-facing polygons.</span></span>

</dd> <dt>

<span data-ttu-id="45123-111">*mode*</span><span class="sxs-lookup"><span data-stu-id="45123-111">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="45123-112">Il modo in cui verranno rasterizzati i poligoni.</span><span class="sxs-lookup"><span data-stu-id="45123-112">The way polygons will be rasterized.</span></span> <span data-ttu-id="45123-113">Le modalità seguenti sono definite e possono essere specificate in *modalità*.</span><span class="sxs-lookup"><span data-stu-id="45123-113">The following modes are defined and can be specified in *mode*.</span></span> <span data-ttu-id="45123-114">Il valore predefinito è \_ riempimento GL per i poligoni di primo e indietro.</span><span class="sxs-lookup"><span data-stu-id="45123-114">The default is GL\_FILL for both front- and back-facing polygons.</span></span>



| <span data-ttu-id="45123-115">Valore</span><span class="sxs-lookup"><span data-stu-id="45123-115">Value</span></span>                                                                                                                                          | <span data-ttu-id="45123-116">Significato</span><span class="sxs-lookup"><span data-stu-id="45123-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINT"></span><span id="gl_point"></span><dl> <span data-ttu-id="45123-117"><dt>**\_punto GL**</dt></span><span class="sxs-lookup"><span data-stu-id="45123-117"><dt>**GL\_POINT**</dt></span></span> </dl> | <span data-ttu-id="45123-118">I vertici poligoni contrassegnati come inizio di un bordo limite vengono disegnati come punti.</span><span class="sxs-lookup"><span data-stu-id="45123-118">Polygon vertices that are marked as the start of a boundary edge are drawn as points.</span></span> <span data-ttu-id="45123-119">Gli attributi punto, ad \_ esempio \_ le dimensioni del punto GL e \_ il punto GL, \_ controllano la rasterizzazione dei punti.</span><span class="sxs-lookup"><span data-stu-id="45123-119">Point attributes such as GL\_POINT\_SIZE and GL\_POINT\_SMOOTH control the rasterization of the points.</span></span> <span data-ttu-id="45123-120">Gli attributi di rasterizzazione Polygon diversi dalla \_ modalità poligono GL \_ non hanno alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="45123-120">Polygon rasterization attributes other than GL\_POLYGON\_MODE have no effect.</span></span><br/>                                                                                                                                                    |
| <span id="GL_LINE"></span><span id="gl_line"></span><dl> <span data-ttu-id="45123-121"><dt>**\_linea GL**</dt></span><span class="sxs-lookup"><span data-stu-id="45123-121"><dt>**GL\_LINE**</dt></span></span> </dl>    | <span data-ttu-id="45123-122">I bordi limite del poligono vengono disegnati come segmenti di linea.</span><span class="sxs-lookup"><span data-stu-id="45123-122">Boundary edges of the polygon are drawn as line segments.</span></span> <span data-ttu-id="45123-123">Vengono trattati come segmenti di linea collegati per la riga punteggiatura; il contatore e il pattern stipple di riga non vengono reimpostati tra segmenti (vedere [**glLineStipple**](gllinestipple.md)).</span><span class="sxs-lookup"><span data-stu-id="45123-123">They are treated as connected line segments for line stippling; the line stipple counter and pattern are not reset between segments (see [**glLineStipple**](gllinestipple.md)).</span></span> <span data-ttu-id="45123-124">Gli attributi della linea, ad esempio \_ \_ la lunghezza riga GL e \_ la linea GL, \_ controllano la rasterizzazione delle linee.</span><span class="sxs-lookup"><span data-stu-id="45123-124">Line attributes such as GL\_LINE\_WIDTH and GL\_LINE\_SMOOTH control the rasterization of the lines.</span></span> <span data-ttu-id="45123-125">Gli attributi di rasterizzazione Polygon diversi dalla \_ modalità poligono GL \_ non hanno alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="45123-125">Polygon rasterization attributes other than GL\_POLYGON\_MODE have no effect.</span></span><br/> |
| <span id="GL_FILL"></span><span id="gl_fill"></span><dl> <span data-ttu-id="45123-126"><dt>**\_riempimento GL**</dt></span><span class="sxs-lookup"><span data-stu-id="45123-126"><dt>**GL\_FILL**</dt></span></span> </dl>    | <span data-ttu-id="45123-127">L'interno del poligono viene riempito.</span><span class="sxs-lookup"><span data-stu-id="45123-127">The interior of the polygon is filled.</span></span> <span data-ttu-id="45123-128">Gli attributi poligono come GL \_ Polygon \_ stipple e GL \_ Polygon \_ Smooth controllano la rasterizzazione del poligono.</span><span class="sxs-lookup"><span data-stu-id="45123-128">Polygon attributes such as GL\_POLYGON\_STIPPLE and GL\_POLYGON\_SMOOTH control the rasterization of the polygon.</span></span><br/>                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45123-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45123-129">Return value</span></span>

<span data-ttu-id="45123-130">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="45123-130">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="45123-131">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="45123-131">Error codes</span></span>

<span data-ttu-id="45123-132">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="45123-132">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="45123-133">Nome</span><span class="sxs-lookup"><span data-stu-id="45123-133">Name</span></span>                                                                                                  | <span data-ttu-id="45123-134">Significato</span><span class="sxs-lookup"><span data-stu-id="45123-134">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="45123-135"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="45123-135"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="45123-136">La *faccia* o la *modalità* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="45123-136">Either *face* or *mode* was not an accepted value.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="45123-137"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="45123-137"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="45123-138">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="45123-138">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="45123-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="45123-139">Remarks</span></span>

<span data-ttu-id="45123-140">La funzione **glPolygonMode** controlla l'interpretazione dei poligoni per la rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="45123-140">The **glPolygonMode** function controls the interpretation of polygons for rasterization.</span></span> <span data-ttu-id="45123-141">Il parametro *viso* descrive la *modalità* dei poligoni a cui si applicano i poligoni anteriori (GL \_ front), i poligoni di back-facet (GL \_ back) o entrambi (GL \_ front \_ e \_ back).</span><span class="sxs-lookup"><span data-stu-id="45123-141">The *face* parameter describes which polygons *mode* applies to: front-facing polygons (GL\_FRONT), back-facing polygons (GL\_BACK), or both (GL\_FRONT\_AND\_BACK).</span></span> <span data-ttu-id="45123-142">La modalità Polygon ha effetto solo sulla rasterizzazione finale dei poligoni.</span><span class="sxs-lookup"><span data-stu-id="45123-142">The polygon mode affects only the final rasterization of polygons.</span></span> <span data-ttu-id="45123-143">In particolare, i vertici di un poligono sono illuminati e il poligono viene troncato e possibilmente ritagliato prima dell'applicazione di queste modalità.</span><span class="sxs-lookup"><span data-stu-id="45123-143">In particular, a polygon's vertices are lit and the polygon is clipped and possibly culled before these modes are applied.</span></span>

<span data-ttu-id="45123-144">Per creare una superficie con i poligoni con riempimento e con i poligoni in primo piano, chiamare</span><span class="sxs-lookup"><span data-stu-id="45123-144">To draw a surface with filled back-facing polygons and outlined front-facing polygons, call</span></span>

<span data-ttu-id="45123-145">**glPolygonMode**(GL \_ Front, \_ linea GL);</span><span class="sxs-lookup"><span data-stu-id="45123-145">**glPolygonMode**(GL\_FRONT, GL\_LINE);</span></span>

<span data-ttu-id="45123-146">I vertici sono contrassegnati come limite o non delimitatori con un flag Edge.</span><span class="sxs-lookup"><span data-stu-id="45123-146">Vertices are marked as boundary or nonboundary with an edge flag.</span></span> <span data-ttu-id="45123-147">I flag Edge vengono generati internamente da OpenGL quando decompone i poligoni e possono essere impostati in modo esplicito tramite [**glEdgeFlag**](gledgeflag-functions.md).</span><span class="sxs-lookup"><span data-stu-id="45123-147">Edge flags are generated internally by OpenGL when it decomposes polygons, and they can be set explicitly using [**glEdgeFlag**](gledgeflag-functions.md).</span></span>

<span data-ttu-id="45123-148">La funzione seguente recupera le informazioni correlate a **glPolygonMode**:</span><span class="sxs-lookup"><span data-stu-id="45123-148">The following function retrieves information related to **glPolygonMode**:</span></span>

<span data-ttu-id="45123-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Polygon \_ mode</span><span class="sxs-lookup"><span data-stu-id="45123-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="45123-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45123-150">Requirements</span></span>



| <span data-ttu-id="45123-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="45123-151">Requirement</span></span> | <span data-ttu-id="45123-152">Valore</span><span class="sxs-lookup"><span data-stu-id="45123-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45123-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45123-153">Minimum supported client</span></span><br/> | <span data-ttu-id="45123-154">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="45123-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="45123-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45123-155">Minimum supported server</span></span><br/> | <span data-ttu-id="45123-156">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="45123-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="45123-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45123-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="45123-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="45123-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="45123-159">Libreria</span><span class="sxs-lookup"><span data-stu-id="45123-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="45123-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45123-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="45123-161">DLL</span><span class="sxs-lookup"><span data-stu-id="45123-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45123-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45123-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45123-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45123-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45123-164">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="45123-164">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="45123-165">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="45123-165">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="45123-166">**Remo**</span><span class="sxs-lookup"><span data-stu-id="45123-166">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="45123-167">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="45123-167">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="45123-168">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="45123-168">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="45123-169">**glPointSize**</span><span class="sxs-lookup"><span data-stu-id="45123-169">**glPointSize**</span></span>](glpointsize.md)
</dt> <dt>

[<span data-ttu-id="45123-170">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="45123-170">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> </dl>

 

 






---
title: funzione gluLoadSamplingMatrices (Glu. h)
description: La funzione gluLoadSamplingMatrices carica matrici di campionamento B-spline (NURBS) non uniformi e matrici di abbattimento.
ms.assetid: 7fdbc4e2-a037-4f07-bb03-e51feea42775
keywords:
- funzione gluLoadSamplingMatrices OpenGL
topic_type:
- apiref
api_name:
- gluLoadSamplingMatrices
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293b8bace0dff7d89bfcffa2af33738e0e59de7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301355"
---
# <a name="gluloadsamplingmatrices-function"></a><span data-ttu-id="2072e-104">gluLoadSamplingMatrices (funzione)</span><span class="sxs-lookup"><span data-stu-id="2072e-104">gluLoadSamplingMatrices function</span></span>

<span data-ttu-id="2072e-105">La funzione **gluLoadSamplingMatrices** carica matrici di campionamento B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniformi e matrici di abbattimento.</span><span class="sxs-lookup"><span data-stu-id="2072e-105">The **gluLoadSamplingMatrices** function loads Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) sampling and culling matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="2072e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2072e-106">Syntax</span></span>


```C++
void WINAPI gluLoadSamplingMatrices(
         GLUnurbs *nobj,
   const GLfloat  modelMatrix[16],
   const GLfloat  projMatrix[16],
   const GLint    viewport[4]
);
```



## <a name="parameters"></a><span data-ttu-id="2072e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2072e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2072e-108">*juje*</span><span class="sxs-lookup"><span data-stu-id="2072e-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="2072e-109">Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="2072e-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="2072e-110">*modelMatrix*</span><span class="sxs-lookup"><span data-stu-id="2072e-110">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="2072e-111">Matrice Modelview (come da una chiamata [**glGetFloatv**](glgetfloatv.md) ).</span><span class="sxs-lookup"><span data-stu-id="2072e-111">A modelview matrix (as from a [**glGetFloatv**](glgetfloatv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="2072e-112">*projMatrix*</span><span class="sxs-lookup"><span data-stu-id="2072e-112">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="2072e-113">Una matrice di proiezione, come da una chiamata **glGetFloatv** .</span><span class="sxs-lookup"><span data-stu-id="2072e-113">A projection matrix (as from a **glGetFloatv** call).</span></span>

</dd> <dt>

<span data-ttu-id="2072e-114">*Viewport*</span><span class="sxs-lookup"><span data-stu-id="2072e-114">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="2072e-115">Viewport (come da una chiamata [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="2072e-115">A viewport (as from a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) call).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2072e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2072e-116">Return value</span></span>

<span data-ttu-id="2072e-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2072e-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2072e-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="2072e-118">Remarks</span></span>

<span data-ttu-id="2072e-119">La funzione **gluLoadSamplingMatrices** USA *modelMatrix*, *projMatrix* e *viewport* per ricalcolare le matrici di campionamento e di eliminazione archiviate in *juje*.</span><span class="sxs-lookup"><span data-stu-id="2072e-119">The **gluLoadSamplingMatrices** function uses *modelMatrix*, *projMatrix*, and *viewport* to recompute the sampling and culling matrices stored in *nobj*.</span></span> <span data-ttu-id="2072e-120">La matrice di campionamento determina il modo in cui una curva o una superficie NURBS deve essere tassellati per soddisfare la tolleranza di campionamento, come determinato dalla \_ proprietà di tolleranza del campionamento Glu \_ .</span><span class="sxs-lookup"><span data-stu-id="2072e-120">The sampling matrix determines how finely a NURBS curve or surface must be tessellated to satisfy the sampling tolerance (as determined by the GLU\_SAMPLING\_TOLERANCE property).</span></span> <span data-ttu-id="2072e-121">La matrice di abbattimento viene usata per decidere se una curva o una superficie NURBS deve essere rilevata prima del rendering (quando la \_ proprietà di abbattimento di Glu è attivata).</span><span class="sxs-lookup"><span data-stu-id="2072e-121">The culling matrix is used in deciding if a NURBS curve or surface should be culled before rendering (when the GLU\_CULLING property is turned on).</span></span>

<span data-ttu-id="2072e-122">La funzione **gluLoadSamplingMatrices** è necessaria solo se la \_ proprietà della matrice di caricamento automatico Glu \_ \_ è spenta (vedere [**gluNurbsProperty**](glunurbsproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="2072e-122">The **gluLoadSamplingMatrices** function is necessary only if the GLU\_AUTO\_LOAD\_MATRIX property is turned off (see [**gluNurbsProperty**](glunurbsproperty.md)).</span></span> <span data-ttu-id="2072e-123">Sebbene possa essere utile lasciare attiva la proprietà della \_ matrice di caricamento automatico Glu \_ , questa \_ operazione richiede un round trip al server OpenGL per ottenere i valori correnti della matrice Modelview, della matrice di proiezione e del viewport.</span><span class="sxs-lookup"><span data-stu-id="2072e-123">Although it can be convenient to leave the GLU\_AUTO\_LOAD\_MATRIX property turned on, doing so necessitates a round trip to the OpenGL server to get the current values of the modelview matrix, projection matrix, and viewport.)</span></span>

## <a name="requirements"></a><span data-ttu-id="2072e-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2072e-124">Requirements</span></span>



| <span data-ttu-id="2072e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2072e-125">Requirement</span></span> | <span data-ttu-id="2072e-126">Valore</span><span class="sxs-lookup"><span data-stu-id="2072e-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2072e-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2072e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2072e-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2072e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2072e-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2072e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2072e-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2072e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2072e-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2072e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2072e-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="2072e-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="2072e-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="2072e-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="2072e-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2072e-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2072e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2072e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2072e-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2072e-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2072e-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2072e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2072e-138">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="2072e-138">**glGetFloatv**</span></span>](glgetfloatv.md)
</dt> <dt>

[<span data-ttu-id="2072e-139">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="2072e-139">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="2072e-140">**gluGetNurbsProperty**</span><span class="sxs-lookup"><span data-stu-id="2072e-140">**gluGetNurbsProperty**</span></span>](glugetnurbsproperty.md)
</dt> <dt>

[<span data-ttu-id="2072e-141">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="2072e-141">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 






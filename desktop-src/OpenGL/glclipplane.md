---
title: funzione glClipPlane (GL. h)
description: La funzione glClipPlane specifica un piano in base al quale viene ritagliata tutta la geometria.
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
keywords:
- funzione glClipPlane OpenGL
topic_type:
- apiref
api_name:
- glClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33380203b30b7a3a2e37ee5d58a47fec845cbc1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301928"
---
# <a name="glclipplane-function"></a><span data-ttu-id="30c4d-104">glClipPlane (funzione)</span><span class="sxs-lookup"><span data-stu-id="30c4d-104">glClipPlane function</span></span>

<span data-ttu-id="30c4d-105">La funzione **glClipPlane** specifica un piano in base al quale viene ritagliata tutta la geometria.</span><span class="sxs-lookup"><span data-stu-id="30c4d-105">The **glClipPlane** function specifies a plane against which all geometry is clipped.</span></span>

## <a name="syntax"></a><span data-ttu-id="30c4d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30c4d-106">Syntax</span></span>


```C++
void WINAPI glClipPlane(
         GLenum   plane,
   const GLdouble *equation
);
```



## <a name="parameters"></a><span data-ttu-id="30c4d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="30c4d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30c4d-108">*aereo*</span><span class="sxs-lookup"><span data-stu-id="30c4d-108">*plane*</span></span> 
</dt> <dd>

<span data-ttu-id="30c4d-109">Il piano di ritaglio in corso di posizionamento.</span><span class="sxs-lookup"><span data-stu-id="30c4d-109">The clipping plane that is being positioned.</span></span> <span data-ttu-id="30c4d-110">I nomi simbolici del formato GL \_ clip \_ plane *i*, dove *i* è un numero intero compreso tra 0 e GL \_ Max clip plane \_ \_ -1, vengono accettati.</span><span class="sxs-lookup"><span data-stu-id="30c4d-110">Symbolic names of the form GL\_CLIP\_PLANE *i*, where *i* is an integer between 0 and GL\_MAX\_CLIP\_PLANES - 1, are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="30c4d-111">*equazione*</span><span class="sxs-lookup"><span data-stu-id="30c4d-111">*equation*</span></span> 
</dt> <dd>

<span data-ttu-id="30c4d-112">Indirizzo di una matrice di quattro valori a virgola mobile e precisione doppia.</span><span class="sxs-lookup"><span data-stu-id="30c4d-112">The address of an array of four double-precision floating-point values.</span></span> <span data-ttu-id="30c4d-113">Questi valori vengono interpretati come un'equazione del piano.</span><span class="sxs-lookup"><span data-stu-id="30c4d-113">These values are interpreted as a plane equation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30c4d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30c4d-114">Return value</span></span>

<span data-ttu-id="30c4d-115">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="30c4d-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="30c4d-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="30c4d-116">Error codes</span></span>

<span data-ttu-id="30c4d-117">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="30c4d-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="30c4d-118">Nome</span><span class="sxs-lookup"><span data-stu-id="30c4d-118">Name</span></span>                                                                                                  | <span data-ttu-id="30c4d-119">Significato</span><span class="sxs-lookup"><span data-stu-id="30c4d-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="30c4d-120"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="30c4d-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="30c4d-121">il *piano* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="30c4d-121">*plane* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="30c4d-122"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="30c4d-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="30c4d-123">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="30c4d-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="30c4d-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="30c4d-124">Remarks</span></span>

<span data-ttu-id="30c4d-125">La geometria viene sempre tagliata in base ai limiti di un tronco a sei piani in *x*, *y* e *z*.</span><span class="sxs-lookup"><span data-stu-id="30c4d-125">Geometry is always clipped against the boundaries of a six-plane frustum in *x*, *y*, and *z*.</span></span> <span data-ttu-id="30c4d-126">La funzione **glClipPlane** consente di specificare piani aggiuntivi, non necessariamente perpendicolari all'asse *x*, asse *y* o asse *z*, in base al quale viene ritagliata tutta la geometria.</span><span class="sxs-lookup"><span data-stu-id="30c4d-126">The **glClipPlane** function allows the specification of additional planes, not necessarily perpendicular to the *x-* axis, *y-* axis, or *z*-axis, against which all geometry is clipped.</span></span> <span data-ttu-id="30c4d-127">È possibile specificare fino a GL max piani di \_ \_ ritaglio dei piani \_ , dove GL \_ Max \_ clip \_ Planes è almeno sei in tutte le implementazioni.</span><span class="sxs-lookup"><span data-stu-id="30c4d-127">Up to GL\_MAX\_CLIP\_PLANES planes can be specified, where GL\_MAX\_CLIP\_PLANES is at least six in all implementations.</span></span> <span data-ttu-id="30c4d-128">Poiché l'area di visualizzazione risultante è l'intersezione tra gli spazi vuoti definiti, è sempre convessa.</span><span class="sxs-lookup"><span data-stu-id="30c4d-128">Because the resulting clipping region is the intersection of the defined half-spaces, it is always convex.</span></span>

<span data-ttu-id="30c4d-129">La funzione **glClipPlane** specifica una metà dello spazio usando un'equazione del piano a quattro componenti.</span><span class="sxs-lookup"><span data-stu-id="30c4d-129">The **glClipPlane** function specifies a half-space using a four-component plane equation.</span></span> <span data-ttu-id="30c4d-130">Quando si chiama **glClipPlane**, l'*equazione* viene trasformata dall'inverso della matrice Modelview e archiviata nelle coordinate oculari risultanti.</span><span class="sxs-lookup"><span data-stu-id="30c4d-130">When you call **glClipPlane**,*equation* is transformed by the inverse of the modelview matrix and stored in the resulting eye coordinates.</span></span> <span data-ttu-id="30c4d-131">Le modifiche successive alla matrice Modelview non hanno effetto sui componenti dell'equazione del piano archiviati.</span><span class="sxs-lookup"><span data-stu-id="30c4d-131">Subsequent changes to the modelview matrix have no effect on the stored plane-equation components.</span></span> <span data-ttu-id="30c4d-132">Se il prodotto a punti delle coordinate oculari di un vertice con i componenti dell'equazione del piano archiviato è positivo o zero, il vertice si trova in rispetto al piano di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="30c4d-132">If the dot product of the eye coordinates of a vertex with the stored plane equation components is positive or zero, the vertex is in with respect to that clipping plane.</span></span> <span data-ttu-id="30c4d-133">In caso contrario, è out.</span><span class="sxs-lookup"><span data-stu-id="30c4d-133">Otherwise, it is out.</span></span>

<span data-ttu-id="30c4d-134">Usare le funzioni [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) per abilitare e disabilitare i piani di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="30c4d-134">Use the [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) functions to enable and disable clipping planes.</span></span> <span data-ttu-id="30c4d-135">Chiamare i piani di ritaglio con l'argomento GL \_ clip \_ plane *i*, dove *i* è il numero del piano.</span><span class="sxs-lookup"><span data-stu-id="30c4d-135">Call clipping planes with the argument GL\_CLIP\_PLANE *i*, where *i* is the plane number.</span></span>

<span data-ttu-id="30c4d-136">Per impostazione predefinita, tutti i piani di ritaglio sono definiti come (0, 0, 0, 0) nelle coordinate degli occhi e sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="30c4d-136">By default, all clipping planes are defined as (0,0,0,0) in eye coordinates and are disabled.</span></span>

<span data-ttu-id="30c4d-137">È sempre il caso GL \_ clip \_ plane *i* = GL \_ clip \_ PLANE0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="30c4d-137">It is always the case that GL\_CLIP\_PLANE *i* = GL\_CLIP\_PLANE0 + *i*.</span></span>

<span data-ttu-id="30c4d-138">Le funzioni seguenti consentono di recuperare informazioni correlate a **glClipPlane**:</span><span class="sxs-lookup"><span data-stu-id="30c4d-138">The following functions retrieve information related to **glClipPlane**:</span></span>

[<span data-ttu-id="30c4d-139">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="30c4d-139">**glGetClipPlane**</span></span>](glgetclipplane.md)

<span data-ttu-id="30c4d-140">[**glIsEnabled**](glisenabled.md) con argomento GL \_ clip \_ plane *i*</span><span class="sxs-lookup"><span data-stu-id="30c4d-140">[**glIsEnabled**](glisenabled.md) with argument GL\_CLIP\_PLANE *i*</span></span>

## <a name="requirements"></a><span data-ttu-id="30c4d-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30c4d-141">Requirements</span></span>



| <span data-ttu-id="30c4d-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="30c4d-142">Requirement</span></span> | <span data-ttu-id="30c4d-143">Valore</span><span class="sxs-lookup"><span data-stu-id="30c4d-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30c4d-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30c4d-144">Minimum supported client</span></span><br/> | <span data-ttu-id="30c4d-145">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="30c4d-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="30c4d-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30c4d-146">Minimum supported server</span></span><br/> | <span data-ttu-id="30c4d-147">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="30c4d-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="30c4d-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30c4d-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="30c4d-149"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="30c4d-149"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="30c4d-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="30c4d-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="30c4d-151"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30c4d-151"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="30c4d-152">DLL</span><span class="sxs-lookup"><span data-stu-id="30c4d-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30c4d-153"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30c4d-153"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30c4d-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30c4d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30c4d-155">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="30c4d-155">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="30c4d-156">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="30c4d-156">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="30c4d-157">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="30c4d-157">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="30c4d-158">**Remo**</span><span class="sxs-lookup"><span data-stu-id="30c4d-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="30c4d-159">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="30c4d-159">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="30c4d-160">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="30c4d-160">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 






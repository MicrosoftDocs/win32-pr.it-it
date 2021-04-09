---
title: funzione glBegin (GL. h)
description: Le funzioni glBegin e glEnd delimitano i vertici di una primitiva o di un gruppo di primitive like. | funzione glBegin (GL. h)
ms.assetid: 8e8e98f8-89e8-40f5-89c1-492c9e3bbd74
keywords:
- funzione glBegin OpenGL
topic_type:
- apiref
api_name:
- glBegin
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8227d30adf97bf27fecc19603a5e5e32e4f44822
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969176"
---
# <a name="glbegin-function"></a><span data-ttu-id="8ae3d-105">glBegin (funzione)</span><span class="sxs-lookup"><span data-stu-id="8ae3d-105">glBegin function</span></span>

<span data-ttu-id="8ae3d-106">Le funzioni **glBegin** e [**glEnd**](glend.md) delimitano i vertici di una primitiva o di un gruppo di primitive like.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-106">The **glBegin** and [**glend**](glend.md) functions delimit the vertices of a primitive or a group of like primitives.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ae3d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ae3d-107">Syntax</span></span>


```C++
void WINAPI glBegin(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="8ae3d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ae3d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ae3d-109">*mode*</span><span class="sxs-lookup"><span data-stu-id="8ae3d-109">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae3d-110">Primitive o primitive che verranno create dai vertici presentati tra **glBegin** e il [**glEnd**](glend.md)successivo.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-110">The primitive or primitives that will be created from vertices presented between **glBegin** and the subsequent [**glend**](glend.md).</span></span> <span data-ttu-id="8ae3d-111">Di seguito sono riportate le costanti simboliche accettate e i relativi significati:</span><span class="sxs-lookup"><span data-stu-id="8ae3d-111">The following are accepted symbolic constants and their meanings:</span></span>



| <span data-ttu-id="8ae3d-112">Valore</span><span class="sxs-lookup"><span data-stu-id="8ae3d-112">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="8ae3d-113">Significato</span><span class="sxs-lookup"><span data-stu-id="8ae3d-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINTS"></span><span id="gl_points"></span><dl> <span data-ttu-id="8ae3d-114"><dt>**\_punti GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8ae3d-114"><dt>**GL\_POINTS**</dt></span></span> </dl>                          | <span data-ttu-id="8ae3d-115">Considera ogni vertice come un singolo punto.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-115">Treats each vertex as a single point.</span></span> <span data-ttu-id="8ae3d-116">Il vertice *n* definisce il punto *n*.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-116">Vertex *n* defines point *n*.</span></span> <span data-ttu-id="8ae3d-117">Vengono disegnati *N* punti.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-117">*N* points are drawn.</span></span><br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_LINES"></span><span id="gl_lines"></span><dl> <span data-ttu-id="8ae3d-118"><dt>**\_righe GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8ae3d-118"><dt>**GL\_LINES**</dt></span></span> </dl>                             | <span data-ttu-id="8ae3d-119">Considera ogni coppia di vertici come un segmento di linea indipendente.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-119">Treats each pair of vertices as an independent line segment.</span></span> <span data-ttu-id="8ae3d-120">I vertici *2n-1* e *2n* definiscono la riga *n*.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-120">Vertices *2n - 1* and *2n* define line *n*.</span></span> <span data-ttu-id="8ae3d-121">Vengono disegnate le righe *N/2* .</span><span class="sxs-lookup"><span data-stu-id="8ae3d-121">*N/2* lines are drawn.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="GL_LINE_STRIP"></span><span id="gl_line_strip"></span><dl> <span data-ttu-id="8ae3d-122"><dt>**\_striscia linea \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8ae3d-122"><dt>**GL\_LINE\_STRIP**</dt></span></span> </dl>             | <span data-ttu-id="8ae3d-123">Disegna un gruppo connesso di segmenti di linea dal primo vertice all'ultimo.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-123">Draws a connected group of line segments from the first vertex to the last.</span></span> <span data-ttu-id="8ae3d-124">I vertici *n* e *n + 1* definiscono la riga *n*.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-124">Vertices *n* and *n+1* define line *n*.</span></span> <span data-ttu-id="8ae3d-125">Vengono disegnate *N-1* righe.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-125">*N - 1* lines are drawn.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="GL_LINE_LOOP"></span><span id="gl_line_loop"></span><dl> <span data-ttu-id="8ae3d-126"><dt>**\_ciclo linea \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8ae3d-126"><dt>**GL\_LINE\_LOOP**</dt></span></span> </dl>                | <span data-ttu-id="8ae3d-127">Disegna un gruppo connesso di segmenti di linea dal primo vertice all'ultimo, quindi di nuovo alla prima.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-127">Draws a connected group of line segments from the first vertex to the last, then back to the first.</span></span> <span data-ttu-id="8ae3d-128">I vertici *n* e *n + 1* definiscono la riga *n*.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-128">Vertices *n* and *n + 1* define line *n*.</span></span> <span data-ttu-id="8ae3d-129">L'ultima riga, tuttavia, è definita dai vertici *N* e *1*.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-129">The last line, however, is defined by vertices *N* and *1*.</span></span> <span data-ttu-id="8ae3d-130">Vengono disegnate *N* righe.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-130">*N* lines are drawn.</span></span><br/>                                                                                                                                                                 |
| <span id="GL_TRIANGLES"></span><span id="gl_triangles"></span><dl> <span data-ttu-id="8ae3d-131"><dt>**triangoli GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8ae3d-131"><dt>**GL\_TRIANGLES**</dt></span></span> </dl>                 | <span data-ttu-id="8ae3d-132">Considera ogni tripletta di vertici come un triangolo indipendente.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-132">Treats each triplet of vertices as an independent triangle.</span></span> <span data-ttu-id="8ae3d-133">I vertici *3N-2*, *3N-1* e *3N* definiscono il triangolo *n*.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-133">Vertices *3n - 2*, *3n - 1*, and *3n* define triangle *n*.</span></span> <span data-ttu-id="8ae3d-134">Vengono disegnati i triangoli *N/3* .</span><span class="sxs-lookup"><span data-stu-id="8ae3d-134">*N/3* triangles are drawn.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_TRIANGLE_STRIP"></span><span id="gl_triangle_strip"></span><dl> <span data-ttu-id="8ae3d-135"><dt>**\_striscia del triangolo GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8ae3d-135"><dt>**GL\_TRIANGLE\_STRIP**</dt></span></span> </dl> | <span data-ttu-id="8ae3d-136">Disegna un gruppo di triangoli connessi.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-136">Draws a connected group of triangles.</span></span> <span data-ttu-id="8ae3d-137">Un triangolo viene definito per ogni vertice presentato dopo i primi due vertici.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-137">One triangle is defined for each vertex presented after the first two vertices.</span></span> <span data-ttu-id="8ae3d-138">Per Odd *n*, vertici *n*, *n + 1* e *n + 2* definiscono il triangolo *n*.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-138">For odd *n*, vertices *n*, *n + 1*, and *n + 2* define triangle *n*.</span></span> <span data-ttu-id="8ae3d-139">Per even *n*, vertici *n + 1*, *n* e *n + 2* definiscono il triangolo *n*.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-139">For even *n*, vertices *n + 1*, *n*, and *n + 2* define triangle *n*.</span></span> <span data-ttu-id="8ae3d-140">Vengono disegnati *N-2* triangoli.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-140">*N - 2* triangles are drawn.</span></span><br/>                                                                                                  |
| <span id="GL_TRIANGLE_FAN"></span><span id="gl_triangle_fan"></span><dl> <span data-ttu-id="8ae3d-141"><dt>**\_ventola del triangolo GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8ae3d-141"><dt>**GL\_TRIANGLE\_FAN**</dt></span></span> </dl>       | <span data-ttu-id="8ae3d-142">Disegna un gruppo di triangoli connessi.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-142">Draws a connected group of triangles.</span></span> <span data-ttu-id="8ae3d-143">un triangolo viene definito per ogni vertice presentato dopo i primi due vertici.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-143">one triangle is defined for each vertex presented after the first two vertices.</span></span> <span data-ttu-id="8ae3d-144">I vertici *1*, *n + 1*, *n + 2* definiscono il triangolo *n*.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-144">Vertices *1*, *n + 1*, *n + 2* define triangle *n*.</span></span> <span data-ttu-id="8ae3d-145">Vengono disegnati *N-2* triangoli.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-145">*N - 2* triangles are drawn.</span></span><br/>                                                                                                                                                                                         |
| <span id="GL_QUADS"></span><span id="gl_quads"></span><dl> <span data-ttu-id="8ae3d-146"><dt>**\_Quad GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8ae3d-146"><dt>**GL\_QUADS**</dt></span></span> </dl>                             | <span data-ttu-id="8ae3d-147">Considera ogni gruppo di quattro vertici come un quadrilatero indipendente.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-147">Treats each group of four vertices as an independent quadrilateral.</span></span> <span data-ttu-id="8ae3d-148">Vertici *4N-3*, *4N-2*, *4n-1* e *4N* definiscono il quadrilatero *n*.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-148">Vertices *4n - 3*, *4n - 2*, *4n - 1*, and *4n* define quadrilateral *n*.</span></span> <span data-ttu-id="8ae3d-149">Vengono disegnati i quadrilateri *N/4* .</span><span class="sxs-lookup"><span data-stu-id="8ae3d-149">*N/4* quadrilaterals are drawn.</span></span><br/>                                                                                                                                                                                                                  |
| <span id="GL_QUAD_STRIP"></span><span id="gl_quad_strip"></span><dl> <span data-ttu-id="8ae3d-150"><dt>**\_ \_ striping GL quad**</dt></span><span class="sxs-lookup"><span data-stu-id="8ae3d-150"><dt>**GL\_QUAD\_STRIP**</dt></span></span> </dl>             | <span data-ttu-id="8ae3d-151">Disegna un gruppo di quadrilateri connesso.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-151">Draws a connected group of quadrilaterals.</span></span> <span data-ttu-id="8ae3d-152">Un quadrilatero viene definito per ogni coppia di vertici presentati dopo la prima coppia.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-152">One quadrilateral is defined for each pair of vertices presented after the first pair.</span></span> <span data-ttu-id="8ae3d-153">I vertici *2n-1*, *2n*, *2n + 2* e *2n + 1* definiscono il quadrilatero *n*.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-153">Vertices *2n - 1*, *2n*, *2n + 2*, and *2n + 1* define quadrilateral *n*.</span></span> <span data-ttu-id="8ae3d-154">Vengono disegnati i quadrilateri *N/2-1* .</span><span class="sxs-lookup"><span data-stu-id="8ae3d-154">*N/2 - 1* quadrilaterals are drawn.</span></span> <span data-ttu-id="8ae3d-155">Si noti che l'ordine in cui i vertici vengono usati per costruire un quadrilatero dai dati della striscia sono diversi da quelli usati con dati indipendenti.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-155">Note that the order in which vertices are used to construct a quadrilateral from strip data is different from that used with independent data.</span></span><br/> |
| <span id="GL_POLYGON"></span><span id="gl_polygon"></span><dl> <span data-ttu-id="8ae3d-156"><dt>**\_poligono GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8ae3d-156"><dt>**GL\_POLYGON**</dt></span></span> </dl>                       | <span data-ttu-id="8ae3d-157">Disegna un singolo poligono convesso.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-157">Draws a single, convex polygon.</span></span> <span data-ttu-id="8ae3d-158">I vertici da *1* a *N* definiscono questo poligono.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-158">Vertices *1* through *N* define this polygon.</span></span><br/>                                                                                                                                                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ae3d-159">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ae3d-159">Return value</span></span>

<span data-ttu-id="8ae3d-160">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-160">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8ae3d-161">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="8ae3d-161">Error codes</span></span>

<span data-ttu-id="8ae3d-162">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="8ae3d-162">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8ae3d-163">Nome</span><span class="sxs-lookup"><span data-stu-id="8ae3d-163">Name</span></span>                                                                                                  | <span data-ttu-id="8ae3d-164">Significato</span><span class="sxs-lookup"><span data-stu-id="8ae3d-164">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ae3d-165"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8ae3d-165"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="8ae3d-166">la *modalità* è stata impostata su un valore non accettato.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-166">*mode* was set to an unaccepted value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="8ae3d-167"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8ae3d-167"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8ae3d-168">Una funzione diversa da [glVertex](glvertex-functions.md), [glColor](glcolor-functions.md), [glIndex](glindex-functions.md), [glNormal](glnormal-functions.md), [glTexCoord](gltexcoord-functions.md), [glEvalCoord](glevalcoord-functions.md), [GlEvalPoint](glevalpoint.md), [glMaterial](glmaterial-functions.md), [glEdgeFlag](gledgeflag-functions.md), [**glCallList**](glcalllist.md)o [**glCallLists**](glcalllists.md) è stata chiamata tra **glBegin** e l'oggetto [**glEnd**](glend.md)corrispondente.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-168">A function other than [glVertex](glvertex-functions.md), [glColor](glcolor-functions.md), [glIndex](glindex-functions.md), [glNormal](glnormal-functions.md), [glTexCoord](gltexcoord-functions.md), [glEvalCoord](glevalcoord-functions.md), [glEvalPoint](glevalpoint.md), [glMaterial](glmaterial-functions.md), [glEdgeFlag](gledgeflag-functions.md), [**glCallList**](glcalllist.md), or [**glCallLists**](glcalllists.md) was called between **glBegin** and the corresponding [**glend**](glend.md).</span></span> <span data-ttu-id="8ae3d-169">La funzione **glEnd** è stata chiamata prima della chiamata del **glBegin** corrispondente oppure **glBegin** è stato chiamato all'interno di una sequenza **glBegin** / **glEnd** .</span><span class="sxs-lookup"><span data-stu-id="8ae3d-169">The function **glend** was called before the corresponding **glBegin** was called, or **glBegin** was called within a **glBegin**/**glend** sequence.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="8ae3d-170">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ae3d-170">Remarks</span></span>

<span data-ttu-id="8ae3d-171">Le funzioni **glBegin** e [**glEnd**](glend.md) delimitano i vertici che definiscono una primitiva o un gruppo di primitive like.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-171">The **glBegin** and [**glend**](glend.md) functions delimit the vertices that define a primitive or a group of like primitives.</span></span> <span data-ttu-id="8ae3d-172">La funzione **glBegin** accetta un solo argomento che specifica quale delle dieci primitive i vertici compongono.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-172">The **glBegin** function accepts a single argument that specifies which of ten primitives the vertices compose.</span></span> <span data-ttu-id="8ae3d-173">Accettando *n* come numero intero a partire da uno e *n* come numero totale di vertici specificati, le interpretazioni sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="8ae3d-173">Taking *n* as an integer count starting at one, and *N* as the total number of vertices specified, the interpretations are as follows:</span></span>

-   <span data-ttu-id="8ae3d-174">È possibile usare solo un subset di funzioni OpenGL tra **glBegin** e [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8ae3d-174">You can use only a subset of OpenGL functions between **glBegin** and [**glend**](glend.md).</span></span> <span data-ttu-id="8ae3d-175">Le funzioni che è possibile usare sono:</span><span class="sxs-lookup"><span data-stu-id="8ae3d-175">The functions you can use are:</span></span>

    [<span data-ttu-id="8ae3d-176">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-176">**glVertex**</span></span>](glvertex-functions.md)

     

    [<span data-ttu-id="8ae3d-177">**glColor**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-177">**glColor**</span></span>](glcolor-functions.md)

     

    [<span data-ttu-id="8ae3d-178">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-178">**glIndex**</span></span>](glindex-functions.md)

     

    [<span data-ttu-id="8ae3d-179">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-179">**glNormal**</span></span>](glnormal-functions.md)

     

    [<span data-ttu-id="8ae3d-180">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-180">**glTexCoord**</span></span>](gltexcoord-functions.md)

     

    [<span data-ttu-id="8ae3d-181">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-181">**glEvalCoord**</span></span>](glevalcoord-functions.md)

     

    [<span data-ttu-id="8ae3d-182">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-182">**glEvalPoint**</span></span>](glevalpoint.md)

     

    [<span data-ttu-id="8ae3d-183">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-183">**glMaterial**</span></span>](glmaterial-functions.md)

     

    [<span data-ttu-id="8ae3d-184">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-184">**glEdgeFlag**</span></span>](gledgeflag-functions.md)

    <span data-ttu-id="8ae3d-185">È anche possibile usare [**glCallList**](glcalllist.md) o [**glCallLists**](glcalllists.md) per eseguire gli elenchi di visualizzazione che includono solo le funzioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-185">You can also use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) to execute display lists that include only the preceding functions.</span></span> <span data-ttu-id="8ae3d-186">Se viene chiamata una qualsiasi altra funzione OpenGL tra **glBegin** e [**glEnd**](glend.md), viene impostato il flag di errore e la funzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-186">If any other OpenGL function is called between **glBegin** and [**glend**](glend.md), the error flag is set and the function is ignored.</span></span>

-   <span data-ttu-id="8ae3d-187">Indipendentemente dal valore scelto per la *modalità* in **glBegin**, non esiste alcun limite al numero di vertici che è possibile definire tra **glBegin** e [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8ae3d-187">Regardless of the value chosen for *mode* in **glBegin**, there is no limit to the number of vertices you can define between **glBegin** and [**glend**](glend.md).</span></span> <span data-ttu-id="8ae3d-188">Le linee, i triangoli, i quadrilateri e i poligoni specificati in un punto non completo non vengono disegnati.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-188">Lines, triangles, quadrilaterals, and polygons that are incompletely specified are not drawn.</span></span> <span data-ttu-id="8ae3d-189">Risultati di specifica incompleti quando vengono forniti un numero troppo basso di vertici per specificare anche una singola primitiva o quando viene specificato un multiplo errato di vertici.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-189">Incomplete specification results when either too few vertices are provided to specify even a single primitive or when an incorrect multiple of vertices is specified.</span></span> <span data-ttu-id="8ae3d-190">La primitiva incompleta viene ignorata; vengono disegnate le primitive complete.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-190">The incomplete primitive is ignored; the complete primitives are drawn.</span></span>
-   <span data-ttu-id="8ae3d-191">La specifica minima dei vertici per ogni primitiva è la seguente:</span><span class="sxs-lookup"><span data-stu-id="8ae3d-191">The minimum specification of vertices for each primitive is:</span></span> 

    | <span data-ttu-id="8ae3d-192">Numero minimo di vertici</span><span class="sxs-lookup"><span data-stu-id="8ae3d-192">Minimum number of vertices</span></span> | <span data-ttu-id="8ae3d-193">Tipo di primitiva</span><span class="sxs-lookup"><span data-stu-id="8ae3d-193">Type of primitive</span></span> |
    |----------------------------|-------------------|
    | <span data-ttu-id="8ae3d-194">1</span><span class="sxs-lookup"><span data-stu-id="8ae3d-194">1</span></span>                          | <span data-ttu-id="8ae3d-195">point</span><span class="sxs-lookup"><span data-stu-id="8ae3d-195">point</span></span>             |
    | <span data-ttu-id="8ae3d-196">2</span><span class="sxs-lookup"><span data-stu-id="8ae3d-196">2</span></span>                          | <span data-ttu-id="8ae3d-197">line</span><span class="sxs-lookup"><span data-stu-id="8ae3d-197">line</span></span>              |
    | <span data-ttu-id="8ae3d-198">3</span><span class="sxs-lookup"><span data-stu-id="8ae3d-198">3</span></span>                          | <span data-ttu-id="8ae3d-199">triangolo</span><span class="sxs-lookup"><span data-stu-id="8ae3d-199">triangle</span></span>          |
    | <span data-ttu-id="8ae3d-200">4</span><span class="sxs-lookup"><span data-stu-id="8ae3d-200">4</span></span>                          | <span data-ttu-id="8ae3d-201">Quadrilatero</span><span class="sxs-lookup"><span data-stu-id="8ae3d-201">quadrilateral</span></span>     |
    | <span data-ttu-id="8ae3d-202">3</span><span class="sxs-lookup"><span data-stu-id="8ae3d-202">3</span></span>                          | <span data-ttu-id="8ae3d-203">polygon</span><span class="sxs-lookup"><span data-stu-id="8ae3d-203">polygon</span></span>           |

    

     

-   <span data-ttu-id="8ae3d-204">Le modalità che richiedono un determinato multiplo di vertici sono GL \_ Lines (2), GL \_ triangoli (3), GL \_ quad (4) e GL \_ Quad \_ Strip (2).</span><span class="sxs-lookup"><span data-stu-id="8ae3d-204">Modes that require a certain multiple of vertices are GL\_LINES (2), GL\_TRIANGLES (3), GL\_QUADS (4), and GL\_QUAD\_STRIP (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ae3d-205">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ae3d-205">Requirements</span></span>



| <span data-ttu-id="8ae3d-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ae3d-206">Requirement</span></span> | <span data-ttu-id="8ae3d-207">Valore</span><span class="sxs-lookup"><span data-stu-id="8ae3d-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae3d-208">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ae3d-208">Minimum supported client</span></span><br/> | <span data-ttu-id="8ae3d-209">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8ae3d-209">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8ae3d-210">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ae3d-210">Minimum supported server</span></span><br/> | <span data-ttu-id="8ae3d-211">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8ae3d-211">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8ae3d-212">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ae3d-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ae3d-213"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ae3d-213"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8ae3d-214">Libreria</span><span class="sxs-lookup"><span data-stu-id="8ae3d-214">Library</span></span><br/>                  | <dl> <span data-ttu-id="8ae3d-215"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ae3d-215"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8ae3d-216">DLL</span><span class="sxs-lookup"><span data-stu-id="8ae3d-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ae3d-217"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ae3d-217"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ae3d-218">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ae3d-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ae3d-219">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-219">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="8ae3d-220">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-220">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="8ae3d-221">**glColor**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-221">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="8ae3d-222">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-222">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="8ae3d-223">**Remo**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-223">**glEnd**</span></span>](/windows/desktop/OpenGL/glend)
</dt> <dt>

[<span data-ttu-id="8ae3d-224">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-224">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="8ae3d-225">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-225">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="8ae3d-226">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-226">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="8ae3d-227">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-227">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="8ae3d-228">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-228">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="8ae3d-229">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-229">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="8ae3d-230">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-230">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 


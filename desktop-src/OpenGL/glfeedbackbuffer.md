---
title: funzione glFeedbackBuffer (GL. h)
description: La funzione glFeedbackBuffer controlla la modalità di feedback.
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
keywords:
- funzione glFeedbackBuffer OpenGL
topic_type:
- apiref
api_name:
- glFeedbackBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64b232db640d41ca9a1e1f75d6ab766597d6511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301920"
---
# <a name="glfeedbackbuffer-function"></a><span data-ttu-id="f38be-104">glFeedbackBuffer (funzione)</span><span class="sxs-lookup"><span data-stu-id="f38be-104">glFeedbackBuffer function</span></span>

<span data-ttu-id="f38be-105">La funzione **glFeedbackBuffer** controlla la modalità di feedback.</span><span class="sxs-lookup"><span data-stu-id="f38be-105">The **glFeedbackBuffer** function controls feedback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="f38be-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f38be-106">Syntax</span></span>


```C++
void WINAPI glFeedbackBuffer(
   GLsizei size,
   GLenum  type,
   GLfloat *buffer
);
```



## <a name="parameters"></a><span data-ttu-id="f38be-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f38be-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f38be-108">*size*</span><span class="sxs-lookup"><span data-stu-id="f38be-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="f38be-109">Numero massimo di valori che possono essere scritti nel *buffer*.</span><span class="sxs-lookup"><span data-stu-id="f38be-109">The maximum number of values that can be written into *buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="f38be-110">*type*</span><span class="sxs-lookup"><span data-stu-id="f38be-110">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="f38be-111">Costante simbolica che descrive le informazioni che verranno restituite per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="f38be-111">A symbolic constant that describes the information that will be returned for each vertex.</span></span> <span data-ttu-id="f38be-112">Sono accettate le costanti simboliche seguenti: GL \_ 2D, GL \_ 3D, GL \_ 3D \_ color, GL \_ 3D \_ Color \_ texture e GL \_ 4D \_ Color \_ texture.</span><span class="sxs-lookup"><span data-stu-id="f38be-112">The following symbolic constants are accepted: GL\_2D, GL\_3D, GL\_3D\_COLOR, GL\_3D\_COLOR\_TEXTURE, and GL\_4D\_COLOR\_TEXTURE.</span></span>

</dd> <dt>

<span data-ttu-id="f38be-113">*buffer*</span><span class="sxs-lookup"><span data-stu-id="f38be-113">*buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="f38be-114">Restituisce i dati di feedback.</span><span class="sxs-lookup"><span data-stu-id="f38be-114">Returns the feedback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f38be-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f38be-115">Return value</span></span>

<span data-ttu-id="f38be-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f38be-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f38be-117">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f38be-117">Error codes</span></span>

<span data-ttu-id="f38be-118">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="f38be-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f38be-119">Nome</span><span class="sxs-lookup"><span data-stu-id="f38be-119">Name</span></span>                                                                                                  | <span data-ttu-id="f38be-120">Significato</span><span class="sxs-lookup"><span data-stu-id="f38be-120">Meaning</span></span>                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f38be-121"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f38be-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="f38be-122">il *tipo* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="f38be-122">*type* was not an accepted value.</span></span><br/>                                                                                                                                                                           |
| <dl> <span data-ttu-id="f38be-123"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f38be-123"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="f38be-124">la *dimensione* è negativa.</span><span class="sxs-lookup"><span data-stu-id="f38be-124">*size* was negative.</span></span><br/>                                                                                                                                                                                        |
| <dl> <span data-ttu-id="f38be-125"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f38be-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f38be-126">**glFeedbackBuffer** è stato chiamato mentre la modalità di rendering è il \_ feedback GL oppure [**glRenderMode**](glrendermode.md) è stato chiamato con l'argomento GL \_ feedback prima che **glFeedbackBuffer** venisse chiamato almeno una volta.</span><span class="sxs-lookup"><span data-stu-id="f38be-126">**glFeedbackBuffer** was called while the render mode was GL\_FEEDBACK, or [**glRenderMode**](glrendermode.md) was called with argument GL\_FEEDBACK before **glFeedbackBuffer** was called at least once.</span></span><br/> |
| <dl> <span data-ttu-id="f38be-127"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f38be-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f38be-128">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f38be-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                  |



## <a name="remarks"></a><span data-ttu-id="f38be-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="f38be-129">Remarks</span></span>

<span data-ttu-id="f38be-130">La funzione **glFeedbackBuffer** controlla il feedback.</span><span class="sxs-lookup"><span data-stu-id="f38be-130">The **glFeedbackBuffer** function controls feedback.</span></span> <span data-ttu-id="f38be-131">Il feedback, ad esempio la selezione, è una modalità OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f38be-131">Feedback, like selection, is an OpenGL mode.</span></span> <span data-ttu-id="f38be-132">La modalità viene selezionata chiamando [**glRenderMode**](glrendermode.md) con feedback GL \_ .</span><span class="sxs-lookup"><span data-stu-id="f38be-132">The mode is selected by calling [**glRenderMode**](glrendermode.md) with GL\_FEEDBACK.</span></span> <span data-ttu-id="f38be-133">Quando OpenGL è in modalità di feedback, nessun pixel viene prodotto dalla rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="f38be-133">When OpenGL is in feedback mode, no pixels are produced by rasterization.</span></span> <span data-ttu-id="f38be-134">Al contrario, le informazioni sulle primitive che sarebbero state rasterizzate vengono riportate all'applicazione con OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f38be-134">Instead, information about primitives that would have been rasterized is fed back to the application using OpenGL.</span></span>

<span data-ttu-id="f38be-135">La funzione **glFeedbackBuffer** presenta tre argomenti:</span><span class="sxs-lookup"><span data-stu-id="f38be-135">The **glFeedbackBuffer** function has three arguments:</span></span>

-   <span data-ttu-id="f38be-136">*buffer* è un puntatore a una matrice di valori a virgola mobile in cui vengono inserite le informazioni sul feedback.</span><span class="sxs-lookup"><span data-stu-id="f38be-136">*buffer* is a pointer to an array of floating-point values into which feedback information is placed.</span></span>
-   <span data-ttu-id="f38be-137">*size* indica la dimensione della matrice.</span><span class="sxs-lookup"><span data-stu-id="f38be-137">*size* indicates the size of the array.</span></span>
-   <span data-ttu-id="f38be-138">il *tipo* è una costante simbolica che descrive le informazioni restituite per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="f38be-138">*type* is a symbolic constant describing the information that is fed back for each vertex.</span></span>

<span data-ttu-id="f38be-139">È necessario eseguire **glFeedbackBuffer** prima che la modalità di feedback sia abilitata (chiamando **glRenderMode** con l'argomento GL \_ feedback).</span><span class="sxs-lookup"><span data-stu-id="f38be-139">You must issue **glFeedbackBuffer** before feedback mode is enabled (by calling **glRenderMode** with argument GL\_FEEDBACK).</span></span> <span data-ttu-id="f38be-140">L'impostazione \_ del feedback GL senza stabilire il buffer di feedback o la chiamata di **GlFeedbackBuffer** mentre OpenGL è in modalità di feedback, è un errore.</span><span class="sxs-lookup"><span data-stu-id="f38be-140">Setting GL\_FEEDBACK without establishing the feedback buffer, or calling **glFeedbackBuffer** while OpenGL is in feedback mode, is an error.</span></span>

<span data-ttu-id="f38be-141">Estrarre la modalità di feedback di OpenGL chiamando [**glRenderMode**](glrendermode.md) con un valore di parametro diverso da \_ feedback GL.</span><span class="sxs-lookup"><span data-stu-id="f38be-141">Take OpenGL out of feedback mode by calling [**glRenderMode**](glrendermode.md) with a parameter value other than GL\_FEEDBACK.</span></span> <span data-ttu-id="f38be-142">Quando si esegue questa operazione mentre OpenGL è in modalità di feedback, **glRenderMode** restituisce il numero di voci inserite nella matrice di commenti.</span><span class="sxs-lookup"><span data-stu-id="f38be-142">When you do this while OpenGL is in feedback mode, **glRenderMode** returns the number of entries placed in the feedback array.</span></span> <span data-ttu-id="f38be-143">Il valore restituito non supera mai le *dimensioni*.</span><span class="sxs-lookup"><span data-stu-id="f38be-143">The returned value never exceeds *size*.</span></span> <span data-ttu-id="f38be-144">Se i dati di feedback richiedevano più spazio rispetto a quello disponibile nel *buffer*, **glRenderMode** restituisce un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="f38be-144">If the feedback data required more room than was available in *buffer*, **glRenderMode** returns a negative value.</span></span>

<span data-ttu-id="f38be-145">In modalità feedback, ogni primitiva che verrebbe rasterizzata genera un blocco di valori che vengono copiati nella matrice di commenti.</span><span class="sxs-lookup"><span data-stu-id="f38be-145">While in feedback mode, each primitive that would be rasterized generates a block of values that gets copied into the feedback array.</span></span> <span data-ttu-id="f38be-146">In caso affermativo, il numero di voci supera il limite massimo, **glFeedbackBuffer** scrive parzialmente il blocco in modo da riempire la matrice (se è presente una stanza a sinistra) e imposta un flag di overflow.</span><span class="sxs-lookup"><span data-stu-id="f38be-146">If doing so would cause the number of entries to exceed the maximum, **glFeedbackBuffer** partially writes the block so as to fill the array (if there is any room left at all), and sets an overflow flag.</span></span> <span data-ttu-id="f38be-147">Ogni blocco inizia con un codice che indica il tipo primitivo, seguito da valori che descrivono i vertici primitivi e i dati associati.</span><span class="sxs-lookup"><span data-stu-id="f38be-147">Each block begins with a code indicating the primitive type, followed by values that describe the primitive's vertices and associated data.</span></span> <span data-ttu-id="f38be-148">La funzione **glFeedbackBuffer** scrive anche le voci per le bitmap e i rettangoli pixel.</span><span class="sxs-lookup"><span data-stu-id="f38be-148">The **glFeedbackBuffer** function also writes entries for bitmaps and pixel rectangles.</span></span> <span data-ttu-id="f38be-149">Il feedback si verifica dopo che l'eliminazione del poligono e l'interpretazione [**glPolygonMode**](glpolygonmode.md) dei poligoni è stata eseguita, quindi i poligoni che vengono abbattuti non vengono restituiti nel buffer di feedback.</span><span class="sxs-lookup"><span data-stu-id="f38be-149">Feedback occurs after polygon culling and [**glPolygonMode**](glpolygonmode.md) interpretation of polygons has taken place, so polygons that are culled are not returned in the feedback buffer.</span></span> <span data-ttu-id="f38be-150">Può verificarsi anche dopo che i poligoni con più di tre bordi vengono suddivisi in triangoli, se l'implementazione di OpenGL esegue il rendering dei poligoni eseguendo questa scomposizione.</span><span class="sxs-lookup"><span data-stu-id="f38be-150">It can also occur after polygons with more than three edges are broken up into triangles, if the OpenGL implementation renders polygons by performing this decomposition.</span></span>

<span data-ttu-id="f38be-151">È possibile inserire un marcatore nel buffer di feedback con [**glPassThrough**](glpassthrough.md).</span><span class="sxs-lookup"><span data-stu-id="f38be-151">You can insert a marker into the feedback buffer with [**glPassThrough**](glpassthrough.md).</span></span>

<span data-ttu-id="f38be-152">Di seguito è riportata la grammatica per i blocchi di valori scritti nel buffer di feedback.</span><span class="sxs-lookup"><span data-stu-id="f38be-152">The following is the grammar for the blocks of values written into the feedback buffer.</span></span> <span data-ttu-id="f38be-153">Ogni primitiva è indicata con un valore di identificazione univoco seguito da un certo numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="f38be-153">Each primitive is indicated with a unique identifying value followed by some number of vertices.</span></span> <span data-ttu-id="f38be-154">Le voci poligono includono un valore integer che indica il numero di vertici seguiti.</span><span class="sxs-lookup"><span data-stu-id="f38be-154">Polygon entries include an integer value indicating how many vertices follow.</span></span> <span data-ttu-id="f38be-155">Un vertice viene alimentato come un certo numero di valori a virgola mobile, come determinato dal *tipo*.</span><span class="sxs-lookup"><span data-stu-id="f38be-155">A vertex is fed back as some number of floating-point values, as determined by *type*.</span></span> <span data-ttu-id="f38be-156">I colori vengono reinseriti come quattro valori in modalità RGBA e un valore in modalità di indice dei colori.</span><span class="sxs-lookup"><span data-stu-id="f38be-156">Colors are fed back as four values in RGBA mode and one value in color-index mode.</span></span>

<span data-ttu-id="f38be-157">textfeedback < feedbackItem feedback \| feedbackItem</span><span class="sxs-lookup"><span data-stu-id="f38be-157">feedbackList <  feedbackItem feedbackList \| feedbackItem</span></span>

<span data-ttu-id="f38be-158">feedbackItem < Point \| LineSegment \| Polygon \| bitmap \| pixelRectangle \| PassThru</span><span class="sxs-lookup"><span data-stu-id="f38be-158">feedbackItem <  point \| lineSegment \| polygon \| bitmap \| pixelRectangle \| passThru</span></span>

<span data-ttu-id="f38be-159">punto < vertice del token del \_ punto GL \_</span><span class="sxs-lookup"><span data-stu-id="f38be-159">point <  GL\_POINT\_TOKEN vertex</span></span>

<span data-ttu-id="f38be-160">lineSegment < GL riga token Vertex Vertex vertice del vertice del \_ \_ \| token di \_ \_ reimpostazione della riga \_</span><span class="sxs-lookup"><span data-stu-id="f38be-160">lineSegment <  GL\_LINE\_TOKEN vertex vertex \| GL\_LINE\_RESET\_TOKEN vertex vertex</span></span>

<span data-ttu-id="f38be-161">Polygon < \_ token poligono GL \_ n Polispec</span><span class="sxs-lookup"><span data-stu-id="f38be-161">polygon <  GL\_POLYGON\_TOKEN n polySpec</span></span>

<span data-ttu-id="f38be-162">Polispec < vertice del vertice del vertice di Polispec \|</span><span class="sxs-lookup"><span data-stu-id="f38be-162">polySpec <  polySpec vertex \| vertex vertex vertex</span></span>

<span data-ttu-id="f38be-163">bitmap < \_ vertice del \_ token bitmap GL</span><span class="sxs-lookup"><span data-stu-id="f38be-163">bitmap <  GL\_BITMAP\_TOKEN vertex</span></span>

<span data-ttu-id="f38be-164">pixelRectangle < GL creare il vertice del token di pixel per il vertice del \_ \_ \_ token pixel \| \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="f38be-164">pixelRectangle <  GL\_DRAW\_PIXEL\_TOKEN vertex \| GL\_COPY\_PIXEL\_TOKEN vertex</span></span>

<span data-ttu-id="f38be-165">passThru < GL \_ pass- \_ through del valore del \_ token</span><span class="sxs-lookup"><span data-stu-id="f38be-165">passThru <  GL\_PASS\_THROUGH\_TOKEN value</span></span>

<span data-ttu-id="f38be-166">Vertex < 2D \| 3D \| 3dColor \| 3dColorTexture \| 4dColorTexture</span><span class="sxs-lookup"><span data-stu-id="f38be-166">vertex <  2d \| 3d \| 3dColor \| 3dColorTexture \| 4dColorTexture</span></span>

<span data-ttu-id="f38be-167">valore di < 2D</span><span class="sxs-lookup"><span data-stu-id="f38be-167">2d <  value value</span></span>

<span data-ttu-id="f38be-168">valore valore < 3D</span><span class="sxs-lookup"><span data-stu-id="f38be-168">3d <  value value value</span></span>

<span data-ttu-id="f38be-169">3dColor < valore valore valore valore</span><span class="sxs-lookup"><span data-stu-id="f38be-169">3dColor <  value value value color</span></span>

<span data-ttu-id="f38be-170">3dColorTexture < valore valore valore valore Tex</span><span class="sxs-lookup"><span data-stu-id="f38be-170">3dColorTexture <  value value value color tex</span></span>

<span data-ttu-id="f38be-171">4dColorTexture < valore valore valore valore valore Tex</span><span class="sxs-lookup"><span data-stu-id="f38be-171">4dColorTexture <  value value value value color tex</span></span>

<span data-ttu-id="f38be-172">Color < \| Indice RGBA</span><span class="sxs-lookup"><span data-stu-id="f38be-172">color <  rgba \| index</span></span>

<span data-ttu-id="f38be-173">RGBA valore valore valore valore <</span><span class="sxs-lookup"><span data-stu-id="f38be-173">rgba <  value value value value</span></span>

<span data-ttu-id="f38be-174">valore < indice</span><span class="sxs-lookup"><span data-stu-id="f38be-174">index <  value</span></span>

<span data-ttu-id="f38be-175">valore valore valore valore di < Tex</span><span class="sxs-lookup"><span data-stu-id="f38be-175">tex <  value value value value</span></span>

<span data-ttu-id="f38be-176">Il parametro *value* è un numero a virgola mobile e *n* è un Integer a virgola mobile che fornisce il numero di vertici nel poligono.</span><span class="sxs-lookup"><span data-stu-id="f38be-176">The *value* parameter is a floating-point number, and *n* is a floating-point integer giving the number of vertices in the polygon.</span></span> <span data-ttu-id="f38be-177">Di seguito sono riportate le costanti a virgola mobile simboliche: \_ token del punto GL \_ , token di riga GL, token di reimpostazione della riga GL, token del poligono GL, token della \_ \_ \_ \_ \_ \_ \_ \_ bitmap GL \_ , token del \_ \_ pixel di estrazione GL \_ , token del \_ \_ pixel di copia GL \_ e \_ token di pass- \_ through \_ .</span><span class="sxs-lookup"><span data-stu-id="f38be-177">The following are symbolic floating-point constants: GL\_POINT\_TOKEN, GL\_LINE\_TOKEN, GL\_LINE\_RESET\_TOKEN, GL\_POLYGON\_TOKEN, GL\_BITMAP\_TOKEN, GL\_DRAW\_PIXEL\_TOKEN, GL\_COPY\_PIXEL\_TOKEN, and GL\_PASS\_THROUGH\_TOKEN.</span></span> <span data-ttu-id="f38be-178">\_ \_ \_ Il token di reimpostazione della riga GL viene restituito ogni volta che viene reimpostato il modello line stipple.</span><span class="sxs-lookup"><span data-stu-id="f38be-178">GL\_LINE\_RESET\_TOKEN is returned whenever the line stipple pattern is reset.</span></span> <span data-ttu-id="f38be-179">I dati restituiti come vertice dipendono dal *tipo* di feedback.</span><span class="sxs-lookup"><span data-stu-id="f38be-179">The data returned as a vertex depends on the feedback *type*.</span></span>

<span data-ttu-id="f38be-180">La tabella seguente fornisce la corrispondenza tra il *tipo* e il numero di valori per vertice. *k* è 1 nella modalità di indice colore e 4 in modalità RGBA.</span><span class="sxs-lookup"><span data-stu-id="f38be-180">The following table gives the correspondence between *type* and the number of values per vertex; *k* is 1 in color-index mode and 4 in RGBA mode.</span></span>



| <span data-ttu-id="f38be-181">Tipo</span><span class="sxs-lookup"><span data-stu-id="f38be-181">Type</span></span>                   | <span data-ttu-id="f38be-182">Coordinate</span><span class="sxs-lookup"><span data-stu-id="f38be-182">Coordinates</span></span>        | <span data-ttu-id="f38be-183">Colore</span><span class="sxs-lookup"><span data-stu-id="f38be-183">Color</span></span> | <span data-ttu-id="f38be-184">Trama</span><span class="sxs-lookup"><span data-stu-id="f38be-184">Texture</span></span> | <span data-ttu-id="f38be-185">Numero totale di valori</span><span class="sxs-lookup"><span data-stu-id="f38be-185">Total number of values</span></span> |
|------------------------|--------------------|-------|---------|------------------------|
| <span data-ttu-id="f38be-186">GL \_ 2D</span><span class="sxs-lookup"><span data-stu-id="f38be-186">GL\_2D</span></span>                 | <span data-ttu-id="f38be-187">*x*, *y*</span><span class="sxs-lookup"><span data-stu-id="f38be-187">*x*, *y*</span></span>           |       |         | <span data-ttu-id="f38be-188">2</span><span class="sxs-lookup"><span data-stu-id="f38be-188">2</span></span>                      |
| <span data-ttu-id="f38be-189">GL \_ 3D</span><span class="sxs-lookup"><span data-stu-id="f38be-189">GL\_3D</span></span>                 | <span data-ttu-id="f38be-190">*x*, *y*, *z*</span><span class="sxs-lookup"><span data-stu-id="f38be-190">*x*, *y*, *z*</span></span>      |       |         | <span data-ttu-id="f38be-191">3</span><span class="sxs-lookup"><span data-stu-id="f38be-191">3</span></span>                      |
| <span data-ttu-id="f38be-192">\_Colore GL 3D \_</span><span class="sxs-lookup"><span data-stu-id="f38be-192">GL\_3D\_COLOR</span></span>          | <span data-ttu-id="f38be-193">*x*, *y*, *z*</span><span class="sxs-lookup"><span data-stu-id="f38be-193">*x*, *y*, *z*</span></span>      | <span data-ttu-id="f38be-194">*k*</span><span class="sxs-lookup"><span data-stu-id="f38be-194">*k*</span></span>   |         | <span data-ttu-id="f38be-195">3 + *k*</span><span class="sxs-lookup"><span data-stu-id="f38be-195">3 + *k*</span></span>                |
| <span data-ttu-id="f38be-196">\_ \_ Trama colori GL \_ 3D</span><span class="sxs-lookup"><span data-stu-id="f38be-196">GL\_3D\_COLOR\_TEXTURE</span></span> | <span data-ttu-id="f38be-197">*x*, *y*, *z*,</span><span class="sxs-lookup"><span data-stu-id="f38be-197">*x*, *y*, *z*,</span></span>     | <span data-ttu-id="f38be-198">*k*</span><span class="sxs-lookup"><span data-stu-id="f38be-198">*k*</span></span>   | <span data-ttu-id="f38be-199">4</span><span class="sxs-lookup"><span data-stu-id="f38be-199">4</span></span>       | <span data-ttu-id="f38be-200">7 + *k*</span><span class="sxs-lookup"><span data-stu-id="f38be-200">7 + *k*</span></span>                |
| <span data-ttu-id="f38be-201">\_ \_ Trama colori GL \_ 4D</span><span class="sxs-lookup"><span data-stu-id="f38be-201">GL\_4D\_COLOR\_TEXTURE</span></span> | <span data-ttu-id="f38be-202">*x*, *y*, *z*, *w*</span><span class="sxs-lookup"><span data-stu-id="f38be-202">*x*, *y*, *z*, *w*</span></span> | <span data-ttu-id="f38be-203">*k*</span><span class="sxs-lookup"><span data-stu-id="f38be-203">*k*</span></span>   | <span data-ttu-id="f38be-204">4</span><span class="sxs-lookup"><span data-stu-id="f38be-204">4</span></span>       | <span data-ttu-id="f38be-205">8 + *k*</span><span class="sxs-lookup"><span data-stu-id="f38be-205">8 + *k*</span></span>                |



 

<span data-ttu-id="f38be-206">Le coordinate dei vertici dei commenti sono nelle coordinate della finestra, eccetto *w*, che è nelle coordinate di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="f38be-206">Feedback vertex coordinates are in window coordinates, except *w*, which is in clip coordinates.</span></span> <span data-ttu-id="f38be-207">Se l'illuminazione è abilitata, vengono illuminati i colori di feedback.</span><span class="sxs-lookup"><span data-stu-id="f38be-207">Feedback colors are lighted, if lighting is enabled.</span></span> <span data-ttu-id="f38be-208">Se la generazione delle coordinate di trama è abilitata, vengono generate le coordinate della trama di feedback.</span><span class="sxs-lookup"><span data-stu-id="f38be-208">Feedback texture coordinates are generated, if texture coordinate generation is enabled.</span></span> <span data-ttu-id="f38be-209">Vengono sempre trasformati dalla matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="f38be-209">They are always transformed by the texture matrix.</span></span>

<span data-ttu-id="f38be-210">La funzione **glFeedbackBuffer** , se utilizzata in un elenco di visualizzazione, non viene compilata nell'elenco di visualizzazione, bensì viene eseguita immediatamente.</span><span class="sxs-lookup"><span data-stu-id="f38be-210">The **glFeedbackBuffer** function, when used in a display list, is not compiled into the display list but rather is executed immediately.</span></span>

<span data-ttu-id="f38be-211">La funzione seguente recupera le informazioni correlate a **glFeedbackBuffer**:</span><span class="sxs-lookup"><span data-stu-id="f38be-211">The following function retrieves information related to **glFeedbackBuffer**:</span></span>

<span data-ttu-id="f38be-212">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con modalità di \_ rendering GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="f38be-212">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="f38be-213">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f38be-213">Requirements</span></span>



| <span data-ttu-id="f38be-214">Requisito</span><span class="sxs-lookup"><span data-stu-id="f38be-214">Requirement</span></span> | <span data-ttu-id="f38be-215">Valore</span><span class="sxs-lookup"><span data-stu-id="f38be-215">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f38be-216">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f38be-216">Minimum supported client</span></span><br/> | <span data-ttu-id="f38be-217">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f38be-217">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f38be-218">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f38be-218">Minimum supported server</span></span><br/> | <span data-ttu-id="f38be-219">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f38be-219">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f38be-220">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f38be-220">Header</span></span><br/>                   | <dl> <span data-ttu-id="f38be-221"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f38be-221"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f38be-222">Libreria</span><span class="sxs-lookup"><span data-stu-id="f38be-222">Library</span></span><br/>                  | <dl> <span data-ttu-id="f38be-223"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f38be-223"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f38be-224">DLL</span><span class="sxs-lookup"><span data-stu-id="f38be-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f38be-225"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f38be-225"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f38be-226">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f38be-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f38be-227">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f38be-227">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f38be-228">**Remo**</span><span class="sxs-lookup"><span data-stu-id="f38be-228">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f38be-229">**glGet**</span><span class="sxs-lookup"><span data-stu-id="f38be-229">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="f38be-230">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="f38be-230">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="f38be-231">**glPassThrough**</span><span class="sxs-lookup"><span data-stu-id="f38be-231">**glPassThrough**</span></span>](glpassthrough.md)
</dt> <dt>

[<span data-ttu-id="f38be-232">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="f38be-232">**glPolygonMode**</span></span>](glpolygonmode.md)
</dt> <dt>

[<span data-ttu-id="f38be-233">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="f38be-233">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="f38be-234">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="f38be-234">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 






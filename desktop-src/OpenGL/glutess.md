---
title: funzione gluTessCallback (Glu. h)
description: La funzione gluTessCallback definisce un callback per un oggetto a mosaico.
ms.assetid: a9709919-d34c-42c4-82b8-6a503f2b39b0
keywords:
- funzione gluTessCallback OpenGL
topic_type:
- apiref
api_name:
- gluTessCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17cdba8b9dd9a3e762a93923a3c353fbc9578377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964828"
---
# <a name="glutesscallback-function"></a><span data-ttu-id="96d39-104">gluTessCallback (funzione)</span><span class="sxs-lookup"><span data-stu-id="96d39-104">gluTessCallback function</span></span>

<span data-ttu-id="96d39-105">La funzione **gluTessCallback** definisce un callback per un oggetto a mosaico.</span><span class="sxs-lookup"><span data-stu-id="96d39-105">The **gluTessCallback** function defines a callback for a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="96d39-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96d39-106">Syntax</span></span>


```C++
void WINAPI gluTessCallback(
   GLUtesselator *tess,
   GLenum        which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="96d39-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="96d39-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96d39-108">*Tess*</span><span class="sxs-lookup"><span data-stu-id="96d39-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="96d39-109">Oggetto a mosaico creato con [**gluNewTess**](glunewtess.md).</span><span class="sxs-lookup"><span data-stu-id="96d39-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="96d39-110">*che*</span><span class="sxs-lookup"><span data-stu-id="96d39-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="96d39-111">Callback da definire.</span><span class="sxs-lookup"><span data-stu-id="96d39-111">The callback being defined.</span></span> <span data-ttu-id="96d39-112">Sono validi i valori seguenti: GLU \_ Tess \_ Begin, Glu \_ Tess \_ Begin \_ data, Glu \_ Tess \_ Edge \_ flag, Glu \_ tesse \_ Edge \_ \_ data flag, Glu \_ Tess \_ vertex, GLU \_ Tess \_ Vertex \_ data, Glu \_ Tess \_ end, Glu \_ Tess \_ End \_ data, Glu Tess, di Glu Tess, Glu Tess \_ \_ \_ \_ \_ \_ \_ Error e Glu \_ Tess, dati di \_ errore \_ .</span><span class="sxs-lookup"><span data-stu-id="96d39-112">The following values are valid: GLU\_TESS\_BEGIN, GLU\_TESS\_BEGIN\_DATA, GLU\_TESS\_EDGE\_FLAG, GLU\_TESS\_EDGE\_FLAG\_DATA, GLU\_TESS\_VERTEX, GLU\_TESS\_VERTEX\_DATA, GLU\_TESS\_END, GLU\_TESS\_END\_DATA, GLU\_TESS\_COMBINE, GLU\_TESS\_COMBINE\_DATA, GLU\_TESS\_ERROR, and GLU\_TESS\_ERROR\_DATA.</span></span>

<span data-ttu-id="96d39-113">Per ulteriori informazioni su questi callback, vedere la sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="96d39-113">For more information on these callbacks, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="96d39-114">*FN*</span><span class="sxs-lookup"><span data-stu-id="96d39-114">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="96d39-115">Funzione da chiamare.</span><span class="sxs-lookup"><span data-stu-id="96d39-115">The function to be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96d39-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96d39-116">Return value</span></span>

<span data-ttu-id="96d39-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="96d39-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96d39-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="96d39-118">Remarks</span></span>

<span data-ttu-id="96d39-119">Utilizzare **gluTessCallback** per specificare un callback che deve essere utilizzato da un oggetto a mosaico.</span><span class="sxs-lookup"><span data-stu-id="96d39-119">Use **gluTessCallback** to specify a callback to be used by a tessellation object.</span></span> <span data-ttu-id="96d39-120">Se il callback specificato è già definito, viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="96d39-120">If the specified callback is already defined, then it is replaced.</span></span> <span data-ttu-id="96d39-121">Se *FN* è **null**, il callback esistente diventa non definito.</span><span class="sxs-lookup"><span data-stu-id="96d39-121">If *fn* is **NULL**, then the existing callback becomes undefined.</span></span>

<span data-ttu-id="96d39-122">L'oggetto mosaico utilizza questi callback per descrivere il modo in cui un poligono specificato viene suddiviso in triangoli.</span><span class="sxs-lookup"><span data-stu-id="96d39-122">The tessellation object uses these callbacks to describe how a polygon that you specify is broken into triangles.</span></span>

<span data-ttu-id="96d39-123">Sono disponibili due versioni di ogni callback, una con dati Polygon che è possibile definire e una senza.</span><span class="sxs-lookup"><span data-stu-id="96d39-123">There are two versions of each callback, one with polygon data that you can define and one without.</span></span> <span data-ttu-id="96d39-124">Se vengono specificate entrambe le versioni di un particolare callback, verrà usato il callback con i dati del poligono specificati.</span><span class="sxs-lookup"><span data-stu-id="96d39-124">If both versions of a particular callback are specified, the callback with the polygon data you specify will be used.</span></span> <span data-ttu-id="96d39-125">Il parametro di *\_ dati Polygon* di [**gluTessBeginPolygon**](glutessbeginpolygon.md) è una copia del puntatore che è stato specificato al momento della chiamata di **gluTessBeginPolygon** .</span><span class="sxs-lookup"><span data-stu-id="96d39-125">The *polygon\_data* parameter of [**gluTessBeginPolygon**](glutessbeginpolygon.md) is a copy of the pointer that was specified when **gluTessBeginPolygon** was called.</span></span>

<span data-ttu-id="96d39-126">Di seguito sono riportati i callback validi:</span><span class="sxs-lookup"><span data-stu-id="96d39-126">The following are valid callbacks:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96d39-127">Callback</span><span class="sxs-lookup"><span data-stu-id="96d39-127">Callback</span></span></th>
<th><span data-ttu-id="96d39-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96d39-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="96d39-129">GLU_TESS_BEGIN</span><span class="sxs-lookup"><span data-stu-id="96d39-129">GLU_TESS_BEGIN</span></span></td>
<td><span data-ttu-id="96d39-130">Il callback GLU_TESS_BEGIN viene richiamato come <a href="glbegin.md"><strong>glBegin</strong></a> per indicare l'inizio di una primitiva (triangolo).</span><span class="sxs-lookup"><span data-stu-id="96d39-130">The GLU_TESS_BEGIN callback is invoked like <a href="glbegin.md"><strong>glBegin</strong></a> to indicate the start of a (triangle) primitive.</span></span> <span data-ttu-id="96d39-131">La funzione accetta un solo argomento di tipo <strong>GLEnum</strong>.</span><span class="sxs-lookup"><span data-stu-id="96d39-131">The function takes a single argument of type <strong>GLenum</strong>.</span></span> <span data-ttu-id="96d39-132">Se si imposta la proprietà GLU_TESS_BOUNDARY_ONLY su GL_FALSE, l'argomento viene impostato su GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP o GL_TRIANGLES.</span><span class="sxs-lookup"><span data-stu-id="96d39-132">If you set the GLU_TESS_BOUNDARY_ONLY property to GL_FALSE, the argument is set to either GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP, or GL_TRIANGLES.</span></span> <span data-ttu-id="96d39-133">Se si imposta la proprietà GLU_TESS_BOUNDARY_ONLY su GL_TRUE, l'argomento viene impostato su GL_LINE_LOOP.</span><span class="sxs-lookup"><span data-stu-id="96d39-133">If you set the GLU_TESS_BOUNDARY_ONLY property to GL_TRUE, the argument is set to GL_LINE_LOOP.</span></span> <span data-ttu-id="96d39-134">Il prototipo di funzione per questo callback è il seguente: <strong>void</strong> <strong>Begin</strong> ( <em>tipo</em><strong>GLEnum</strong> );</span><span class="sxs-lookup"><span data-stu-id="96d39-134">The function prototype for this callback is as follows: <strong>void</strong> <strong>begin</strong> (<strong>GLenum</strong> <em>type</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96d39-135">GLU_TESS_BEGIN_DATA</span><span class="sxs-lookup"><span data-stu-id="96d39-135">GLU_TESS_BEGIN_DATA</span></span></td>
<td><span data-ttu-id="96d39-136">GLU_TESS_BEGIN_DATA è uguale al callback GLU_TESS_BEGIN ad eccezione del fatto che accetta un argomento puntatore aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="96d39-136">GLU_TESS_BEGIN_DATA is the same as the GLU_TESS_BEGIN callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="96d39-137">Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="96d39-137">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="96d39-138">Il prototipo di funzione per questo callback è: <strong>void</strong> <strong>beginData</strong> (<strong>glenum</strong> <em>Type</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="96d39-138">The function prototype for this callback is: <strong>void</strong> <strong>beginData</strong> (<strong>GLenum</strong> <em>type</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96d39-139">GLU_TESS_EDGE_FLAG</span><span class="sxs-lookup"><span data-stu-id="96d39-139">GLU_TESS_EDGE_FLAG</span></span></td>
<td><span data-ttu-id="96d39-140">Il callback GLU_TESS_EDGE_FLAG è simile a <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="96d39-140">The GLU_TESS_EDGE_FLAG callback is similar to <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>.</span></span> <span data-ttu-id="96d39-141">La funzione accetta un singolo flag booleano che indica quali bordi si trovano sul limite del poligono.</span><span class="sxs-lookup"><span data-stu-id="96d39-141">The function takes a single Boolean flag that indicates which edges lie on the polygon boundary.</span></span> <span data-ttu-id="96d39-142">Se il flag è GL_TRUE, ogni vertice che segue inizia un bordo che si trova sul limite del poligono; ovvero un bordo che separa un'area interna da uno esterno.</span><span class="sxs-lookup"><span data-stu-id="96d39-142">If the flag is GL_TRUE, then each vertex that follows begins an edge that lies on the polygon boundary; that is, an edge which separates an interior region from an exterior one.</span></span> <span data-ttu-id="96d39-143">Se il flag è GL_FALSE, ogni vertice che segue inizia un bordo che si trova nell'interno del poligono.</span><span class="sxs-lookup"><span data-stu-id="96d39-143">If the flag is GL_FALSE, then each vertex that follows begins an edge that lies in the polygon interior.</span></span> <span data-ttu-id="96d39-144">Il callback GLU_TESS_EDGE_FLAG (se definito) viene richiamato prima che venga eseguito il primo callback del vertice.</span><span class="sxs-lookup"><span data-stu-id="96d39-144">The GLU_TESS_EDGE_FLAG callback (if defined) is invoked before the first vertex callback is made.</span></span> <span data-ttu-id="96d39-145">Poiché le ventole del triangolo e le strisce triangolari non supportano i flag Edge, il callback Begin non viene chiamato con GL_TRIANGLE_FAN o GL_TRIANGLE_STRIP se viene fornito un callback del flag Edge.</span><span class="sxs-lookup"><span data-stu-id="96d39-145">Because triangle fans and triangle strips do not support edge flags, the begin callback is not called with GL_TRIANGLE_FAN or GL_TRIANGLE_STRIP if an edge flag callback is provided.</span></span> <span data-ttu-id="96d39-146">Al contrario, le ventole e le strisce vengono convertite in triangoli indipendenti.</span><span class="sxs-lookup"><span data-stu-id="96d39-146">Instead, the fans and strips are converted to independent triangles.</span></span> <span data-ttu-id="96d39-147">Il prototipo di funzione per questo callback è:</span><span class="sxs-lookup"><span data-stu-id="96d39-147">The function prototype for this callback is:</span></span><br/> <span data-ttu-id="96d39-148"><strong>void</strong> <strong>edgeFlag</strong> (<strong></strong> <em>flag</em>GLboolean);</span><span class="sxs-lookup"><span data-stu-id="96d39-148"><strong>void</strong> <strong>edgeFlag</strong> (<strong>GLboolean</strong> <em>flag</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96d39-149">GLU_TESS_EDGE_FLAG_DATA</span><span class="sxs-lookup"><span data-stu-id="96d39-149">GLU_TESS_EDGE_FLAG_DATA</span></span></td>
<td><span data-ttu-id="96d39-150">Il callback GLU_TESS_EDGE_FLAG_DATA è uguale al callback GLU_TESS_EDGE_FLAG ad eccezione del fatto che accetta un argomento puntatore aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="96d39-150">The GLU_TESS_EDGE_FLAG_DATA callback is the same as the GLU_TESS_EDGE_FLAG callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="96d39-151">Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="96d39-151">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="96d39-152">Il prototipo di funzione per questo callback è: <strong>void</strong> <strong>edgeFlagData</strong> (<strong>GLboolean</strong> <em>flag</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="96d39-152">The function prototype for this callback is: <strong>void</strong> <strong>edgeFlagData</strong> (<strong>GLboolean</strong> <em>flag</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96d39-153">GLU_TESS_VERTEX</span><span class="sxs-lookup"><span data-stu-id="96d39-153">GLU_TESS_VERTEX</span></span></td>
<td><span data-ttu-id="96d39-154">Il callback GLU_TESS_VERTEX viene richiamato tra i callback Begin e end.</span><span class="sxs-lookup"><span data-stu-id="96d39-154">The GLU_TESS_VERTEX callback is invoked between the begin and end callbacks.</span></span> <span data-ttu-id="96d39-155">È simile a glVertex e definisce i vertici dei triangoli creati dal processo a mosaico.</span><span class="sxs-lookup"><span data-stu-id="96d39-155">It is similar to glVertex , and it defines the vertexes of the triangles created by the tessellation process.</span></span> <span data-ttu-id="96d39-156">La funzione accetta un puntatore come unico argomento.</span><span class="sxs-lookup"><span data-stu-id="96d39-156">The function takes a pointer as its only argument.</span></span> <span data-ttu-id="96d39-157">Questo puntatore è identico al puntatore opaco fornito quando è stato definito il vertice (vedere <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="96d39-157">This pointer is identical to the opaque pointer that you provided when you defined the vertex (see <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>).</span></span> <span data-ttu-id="96d39-158">Il prototipo di funzione per questo callback è: <strong>void</strong> <strong>vertex</strong> (<strong>void</strong> \* <em>vertex_data</em>);</span><span class="sxs-lookup"><span data-stu-id="96d39-158">The function prototype for this callback is: <strong>void</strong> <strong>vertex</strong> (<strong>void</strong> \* <em>vertex_data</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96d39-159">GLU_TESS_VERTEX_DATA</span><span class="sxs-lookup"><span data-stu-id="96d39-159">GLU_TESS_VERTEX_DATA</span></span></td>
<td><span data-ttu-id="96d39-160">Il GLU_TESS_VERTEX_DATA è uguale al callback GLU_TESS_VERTEX ad eccezione del fatto che accetta un argomento puntatore aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="96d39-160">The GLU_TESS_VERTEX_DATA is the same as the GLU_TESS_VERTEX callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="96d39-161">Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="96d39-161">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="96d39-162">Il prototipo di funzione per questo callback è: <strong>void</strong>  <strong>vertexData</strong> (void \* <em>vertex_data</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="96d39-162">The function prototype for this callback is: <strong>void</strong>  <strong>vertexData</strong> (void \* <em>vertex_data</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96d39-163">GLU_TESS_END</span><span class="sxs-lookup"><span data-stu-id="96d39-163">GLU_TESS_END</span></span></td>
<td><span data-ttu-id="96d39-164">Il callback GLU_TESS_END ha lo stesso scopo di <a href="glend.md"><strong>glEnd</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="96d39-164">The GLU_TESS_END callback serves the same purpose as <a href="glend.md"><strong>glEnd</strong></a>.</span></span> <span data-ttu-id="96d39-165">Indica la fine di una primitiva e non accetta argomenti.</span><span class="sxs-lookup"><span data-stu-id="96d39-165">It indicates the end of a primitive, and it takes no arguments.</span></span> <span data-ttu-id="96d39-166">Il prototipo di funzione per questo callback è: <strong>void</strong> <strong>end</strong> (<strong>void</strong>);</span><span class="sxs-lookup"><span data-stu-id="96d39-166">The function prototype for this callback is: <strong>void</strong> <strong>end</strong> (<strong>void</strong>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96d39-167">GLU_TESS_END_DATA</span><span class="sxs-lookup"><span data-stu-id="96d39-167">GLU_TESS_END_DATA</span></span></td>
<td><span data-ttu-id="96d39-168">Il callback GLU_TESS_END_DATA è uguale al callback GLU_TESS_END ad eccezione del fatto che accetta un argomento puntatore aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="96d39-168">The GLU_TESS_END_DATA callback is the same as the GLU_TESS_END callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="96d39-169">Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="96d39-169">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="96d39-170">Il prototipo di funzione per questo callback è: <strong>void</strong> <strong>endData</strong> (<strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="96d39-170">The function prototype for this callback is: <strong>void</strong> <strong>endData</strong> (<strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96d39-171">GLU_TESS_COMBINE</span><span class="sxs-lookup"><span data-stu-id="96d39-171">GLU_TESS_COMBINE</span></span></td>
<td><span data-ttu-id="96d39-172">Chiamare il callback GLU_TESS_COMBINE per creare un nuovo vertice quando lo schema a mosaico rileva un'intersezione o per unire le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="96d39-172">Call the GLU_TESS_COMBINE callback to create a new vertex when the tessellation detects an intersection, or to merge features.</span></span> <span data-ttu-id="96d39-173">La funzione accetta quattro argomenti: una matrice di tre elementi, ognuno di tipo Gldouble.</span><span class="sxs-lookup"><span data-stu-id="96d39-173">The function takes four arguments: An array of three elements, each of type Gldouble.</span></span><br/> <span data-ttu-id="96d39-174">Matrice di quattro puntatori.</span><span class="sxs-lookup"><span data-stu-id="96d39-174">An array of four pointers.</span></span><br/> <span data-ttu-id="96d39-175">Matrice di quattro elementi, ognuno di tipo GLfloat.</span><span class="sxs-lookup"><span data-stu-id="96d39-175">An array of four elements, each of type GLfloat.</span></span><br/> <span data-ttu-id="96d39-176">Puntatore a un puntatore.</span><span class="sxs-lookup"><span data-stu-id="96d39-176">A pointer to a pointer.</span></span><br/> <span data-ttu-id="96d39-177">Il prototipo di funzione per questo callback è:</span><span class="sxs-lookup"><span data-stu-id="96d39-177">The function prototype for this callback is:</span></span> <br/> <span data-ttu-id="96d39-178"><strong>void</strong> <strong>combine</strong>(<strong>GLdouble</strong> <em>Coordinate</em>[3], <strong>void</strong> \* <em>vertex_data</em>[4], <strong>GLfloat</strong> <em>Weight</em>[4], <strong>void</strong>  \*\* <em>OutData</em>);</span><span class="sxs-lookup"><span data-stu-id="96d39-178"><strong>void</strong> <strong>combine</strong>(<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> \* <em>vertex_data</em>[4], <strong>GLfloat</strong> <em>weight</em>[4], <strong>void</strong> \*\*<em>outData</em>);</span></span><br/> <span data-ttu-id="96d39-179">Il vertice viene definito come una combinazione lineare di un massimo di quattro vertici esistenti, archiviati in vertex_data.</span><span class="sxs-lookup"><span data-stu-id="96d39-179">The vertex is defined as a linear combination of up to four existing vertexes, stored in vertex_data.</span></span> <span data-ttu-id="96d39-180">I coefficienti della combinazione lineare vengono assegnati in base al peso; questi pesi vengono sempre sommati a 1,0.</span><span class="sxs-lookup"><span data-stu-id="96d39-180">The coefficients of the linear combination are given by weight; these weights always sum to 1.0.</span></span> <span data-ttu-id="96d39-181">Tutti i puntatori ai vertici sono validi anche quando alcuni pesi sono pari a zero.</span><span class="sxs-lookup"><span data-stu-id="96d39-181">All vertex pointers are valid even when some of the weights are zero.</span></span> <span data-ttu-id="96d39-182">Il parametro coordinate fornisce la posizione del nuovo vertice.</span><span class="sxs-lookup"><span data-stu-id="96d39-182">The coords parameter gives the location of the new vertex.</span></span><br/> <span data-ttu-id="96d39-183">Allocare un altro vertice, interpolare i parametri usando vertex_data e il peso e restituire il nuovo puntatore del vertice in OutData.</span><span class="sxs-lookup"><span data-stu-id="96d39-183">Allocate another vertex, interpolate parameters using vertex_data and weight, and return the new vertex pointer in outData.</span></span> <span data-ttu-id="96d39-184">Questo handle viene fornito durante il rendering di callback.</span><span class="sxs-lookup"><span data-stu-id="96d39-184">This handle is supplied during rendering callbacks.</span></span> <span data-ttu-id="96d39-185">Liberare la memoria qualche minuto dopo la chiamata a <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="96d39-185">Free the memory sometime after calling <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>.</span></span><br/> <span data-ttu-id="96d39-186">Se, ad esempio, il poligono si trova in un piano arbitrario in uno spazio tridimensionale e si associa un colore a ogni vertice, il callback GLU_TESS_COMBINE potrebbe essere simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="96d39-186">For example, if the polygon lies in an arbitrary plane in three-dimensional space, and you associate a color with each vertex, the GLU_TESS_COMBINE callback might look like the following:</span></span><br/>
<pre data-space="preserve"><code>void myCombine( GLdouble coords[3], VERTEX *d[4], 
                GLfloat w[4], VERTEX **dataOut ) 
{ 
    VERTEX *newVertex = new_vertex(); 
    newVertex->x = coords[0]; 
    newVertex->y = coords[1]; 
    newVertex->z = coords[2]; 
    newVertex->r = w[0]*d[0]->r + w[1]*d[1]->r + w[2]*d[2]->r + 
                   w[3]*d[3]->r; 
    newVertex->g = w[0]*d[0]->g + w[1]*d[1]->g + w[2]*d[2]->g + 
                   w[3]*d[3]->g; 
    newVertex->b = w[0]*d[0]->b + w[1]*d[1]->b + w[2]*d[2]->b + 
                   w[3]*d[3]->b; 
    newVertex->a = w[0]*d[0]->a + w[1]*d[1]->a + w[2]*d[2]->a + 
                   w[3]*d[3]->a; 
    *dataOut = newVertex; 
}</code></pre>
<span data-ttu-id="96d39-187">Quando lo schema a mosaico rileva un'intersezione, è necessario definire il callback di GLU_TESS_COMBINE o di GLU_TESS_COMBINE_DATA (vedere di seguito) e scrivere un puntatore non<strong>null</strong> in dati.</span><span class="sxs-lookup"><span data-stu-id="96d39-187">When the tessellation detects an intersection, the GLU_TESS_COMBINE or GLU_TESS_COMBINE_DATA callback (see below) must be defined, and must write a non-<strong>NULL</strong> pointer into dataOut.</span></span> <span data-ttu-id="96d39-188">In caso contrario, si verifica l'errore GLU_TESS_NEED_COMBINE_CALLBACK e non viene generato alcun output.</span><span class="sxs-lookup"><span data-stu-id="96d39-188">Otherwise the GLU_TESS_NEED_COMBINE_CALLBACK error occurs, and no output is generated.</span></span> <span data-ttu-id="96d39-189">Si tratta dell'unico errore che può verificarsi durante il mosaico e il rendering.</span><span class="sxs-lookup"><span data-stu-id="96d39-189">(This is the only error that can occur during tessellation and rendering.)</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96d39-190">GLU_TESS_COMBINE_DATA</span><span class="sxs-lookup"><span data-stu-id="96d39-190">GLU_TESS_COMBINE_DATA</span></span></td>
<td><span data-ttu-id="96d39-191">Il callback GLU_TESS_COMBINE_DATA è uguale al callback GLU_TESS_COMBINE ad eccezione del fatto che accetta un argomento puntatore aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="96d39-191">The GLU_TESS_COMBINE_DATA callback is the same as the GLU_TESS_COMBINE callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="96d39-192">Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="96d39-192">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="96d39-193">Il prototipo di funzione per questo callback è: <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>Coordinate</em>[3], <strong>void</strong> \*<em>vertex_data</em>[4], <strong>GLfloat</strong> <em>Weight</em>[4 <strong>], void</strong>  \*\* <em>OutData</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="96d39-193">The function prototype for this callback is: <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> \*<em>vertex_data</em>[4], <strong>GLfloat</strong> <em>weight</em>[4], <strong>void</strong> \*\*<em>outData</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96d39-194">GLU_TESS_ERROR</span><span class="sxs-lookup"><span data-stu-id="96d39-194">GLU_TESS_ERROR</span></span></td>
<td><span data-ttu-id="96d39-195">Il callback GLU_TESS_ERROR viene chiamato quando viene rilevato un errore.</span><span class="sxs-lookup"><span data-stu-id="96d39-195">The GLU_TESS_ERROR callback is called when an error is encountered.</span></span> <span data-ttu-id="96d39-196">Il primo argomento è di tipo <strong>GLEnum</strong>; indica l'errore specifico che si è verificato ed è impostato su uno dei seguenti elementi: GLU_TESS_MISSING_BEGIN_POLYGON</span><span class="sxs-lookup"><span data-stu-id="96d39-196">The one argument is of type <strong>GLenum</strong>; it indicates the specific error that occurred and is set to one of the following: GLU_TESS_MISSING_BEGIN_POLYGON</span></span><br/> <span data-ttu-id="96d39-197">GLU_TESS_MISSING_END_POLYGON</span><span class="sxs-lookup"><span data-stu-id="96d39-197">GLU_TESS_MISSING_END_POLYGON</span></span><br/> <span data-ttu-id="96d39-198">GLU_TESS_MISSING_BEGIN_CONTOUR</span><span class="sxs-lookup"><span data-stu-id="96d39-198">GLU_TESS_MISSING_BEGIN_CONTOUR</span></span><br/> <span data-ttu-id="96d39-199">GLU_TESS_MISSING_END_CONTOUR</span><span class="sxs-lookup"><span data-stu-id="96d39-199">GLU_TESS_MISSING_END_CONTOUR</span></span><br/> <span data-ttu-id="96d39-200">GLU_TESS_COORD_TOO_LARGE</span><span class="sxs-lookup"><span data-stu-id="96d39-200">GLU_TESS_COORD_TOO_LARGE</span></span><br/> <span data-ttu-id="96d39-201">GLU_TESS_NEED_COMBINE_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="96d39-201">GLU_TESS_NEED_COMBINE_CALLBACK</span></span><br/> <span data-ttu-id="96d39-202">Chiamare gluErrorString per recuperare le stringhe di caratteri che descrivono questi errori.</span><span class="sxs-lookup"><span data-stu-id="96d39-202">Call gluErrorString to retrieve character strings describing these errors.</span></span> <span data-ttu-id="96d39-203">Il prototipo di funzione per questo callback è il seguente:</span><span class="sxs-lookup"><span data-stu-id="96d39-203">The function prototype for this callback is as follows:</span></span><br/> <span data-ttu-id="96d39-204"><strong></strong> <strong>errore</strong> void (<strong>GLEnum</strong> <em>errno</em>);</span><span class="sxs-lookup"><span data-stu-id="96d39-204"><strong>void</strong> <strong>error</strong> (<strong>GLenum</strong> <em>errno</em>);</span></span><br/> <span data-ttu-id="96d39-205">La libreria GLU esegue il ripristino dai primi quattro errori inserendo la chiamata o le chiamate mancanti.</span><span class="sxs-lookup"><span data-stu-id="96d39-205">The GLU library recovers from the first four errors by inserting the missing call or calls.</span></span> <span data-ttu-id="96d39-206">GLU_TESS_COORD_TOO_LARGE indica che alcune coordinate del vertice hanno superato la costante predefinita GLU_TESS_MAX_COORD in un valore assoluto e che il valore è stato bloccato.</span><span class="sxs-lookup"><span data-stu-id="96d39-206">GLU_TESS_COORD_TOO_LARGE indicates that some vertex coordinate exceeded the predefined constant GLU_TESS_MAX_COORD in absolute value, and that the value has been clamped.</span></span> <span data-ttu-id="96d39-207">(I valori delle coordinate devono essere sufficientemente piccoli da poter moltiplicare due elementi senza overflow). GLU_TESS_NEED_COMBINE_CALLBACK indica che il mosaico ha rilevato un'intersezione tra due bordi nei dati di input e non è stato fornito il callback GLU_TESS_COMBINE o GLU_TESS_COMBINE_DATA.</span><span class="sxs-lookup"><span data-stu-id="96d39-207">(Coordinate values must be small enough that two can be multiplied together without overflow.) GLU_TESS_NEED_COMBINE_CALLBACK indicates that the tessellation detected an intersection between two edges in the input data, and the GLU_TESS_COMBINE or GLU_TESS_COMBINE_DATA callback was not provided.</span></span> <span data-ttu-id="96d39-208">Non verrà generato alcun output.</span><span class="sxs-lookup"><span data-stu-id="96d39-208">No output will be generated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96d39-209">GLU_TESS_ERROR_DATA</span><span class="sxs-lookup"><span data-stu-id="96d39-209">GLU_TESS_ERROR_DATA</span></span></td>
<td><span data-ttu-id="96d39-210">Il callback GLU_TESS_ERROR_DATA è uguale al callback GLU_TESS_ERROR, ad eccezione del fatto che accetta un argomento puntatore aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="96d39-210">The GLU_TESS_ERROR_DATA callback is the same as the GLU_TESS_ERROR callback, except that it takes an additional pointer argument.</span></span> <span data-ttu-id="96d39-211">Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="96d39-211">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="96d39-212">Il prototipo di funzione per questo callback è: <strong>void</strong> <strong>ErrorData</strong> (<strong>glenum</strong> <em>errno</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="96d39-212">The function prototype for this callback is: <strong>void</strong> <strong>errorData</strong> (<strong>GLenum</strong> <em>errno</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="96d39-213">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96d39-213">Requirements</span></span>



| <span data-ttu-id="96d39-214">Requisito</span><span class="sxs-lookup"><span data-stu-id="96d39-214">Requirement</span></span> | <span data-ttu-id="96d39-215">Valore</span><span class="sxs-lookup"><span data-stu-id="96d39-215">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="96d39-216">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96d39-216">Minimum supported client</span></span><br/> | <span data-ttu-id="96d39-217">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="96d39-217">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="96d39-218">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96d39-218">Minimum supported server</span></span><br/> | <span data-ttu-id="96d39-219">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="96d39-219">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="96d39-220">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96d39-220">Header</span></span><br/>                   | <dl> <span data-ttu-id="96d39-221"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="96d39-221"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="96d39-222">Libreria</span><span class="sxs-lookup"><span data-stu-id="96d39-222">Library</span></span><br/>                  | <dl> <span data-ttu-id="96d39-223"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96d39-223"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="96d39-224">DLL</span><span class="sxs-lookup"><span data-stu-id="96d39-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96d39-225"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96d39-225"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96d39-226">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96d39-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96d39-227">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="96d39-227">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="96d39-228">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="96d39-228">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="96d39-229">**Remo**</span><span class="sxs-lookup"><span data-stu-id="96d39-229">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="96d39-230">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="96d39-230">**glVertex**</span></span>](glvertex-functions.md)
</dt> <dt>

[<span data-ttu-id="96d39-231">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="96d39-231">**gluDeleteTess**</span></span>](gludeletetess.md)
</dt> <dt>

[<span data-ttu-id="96d39-232">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="96d39-232">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="96d39-233">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="96d39-233">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="96d39-234">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="96d39-234">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="96d39-235">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="96d39-235">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="96d39-236">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="96d39-236">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 






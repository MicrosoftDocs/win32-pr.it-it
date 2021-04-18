---
title: funzione glVertexPointer (GL. h)
description: La funzione glVertexPointer definisce una matrice di dati dei vertici.
ms.assetid: e5f97fdc-9448-4389-8533-3855a3213feb
keywords:
- funzione glVertexPointer OpenGL
topic_type:
- apiref
api_name:
- glVertexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422dd1a7938cc5adb183ff7e17c59a8f52eb4909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478227"
---
# <a name="glvertexpointer-function"></a><span data-ttu-id="ad1b8-104">glVertexPointer (funzione)</span><span class="sxs-lookup"><span data-stu-id="ad1b8-104">glVertexPointer function</span></span>

<span data-ttu-id="ad1b8-105">La funzione **glVertexPointer** definisce una matrice di dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-105">The **glVertexPointer** function defines an array of vertex data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad1b8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad1b8-106">Syntax</span></span>


```C++
void WINAPI glVertexPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="ad1b8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad1b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad1b8-108">*size*</span><span class="sxs-lookup"><span data-stu-id="ad1b8-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="ad1b8-109">Numero di coordinate per vertice.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-109">The number of coordinates per vertex.</span></span> <span data-ttu-id="ad1b8-110">Il valore delle *dimensioni* deve essere 2, 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-110">The value of *size* must be 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="ad1b8-111">*type*</span><span class="sxs-lookup"><span data-stu-id="ad1b8-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="ad1b8-112">Il tipo di dati di ogni coordinata nella matrice usando le costanti simboliche seguenti: GL \_ short, GL \_ int, GL \_ float e GL \_ Double.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-112">The data type of each coordinate in the array using the following symbolic constants: GL\_SHORT, GL\_INT, GL\_FLOAT, and GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="ad1b8-113">*stride*</span><span class="sxs-lookup"><span data-stu-id="ad1b8-113">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="ad1b8-114">Offset dei byte tra i vertici consecutivi.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-114">The byte offset between consecutive vertices.</span></span> <span data-ttu-id="ad1b8-115">Quando *stride* è zero, i vertici sono strettamente compressi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-115">When *stride* is zero, the vertices are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="ad1b8-116">*indicatore di misura*</span><span class="sxs-lookup"><span data-stu-id="ad1b8-116">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="ad1b8-117">Puntatore alla prima coordinata del primo vertice nella matrice.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-117">A pointer to the first coordinate of the first vertex in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad1b8-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad1b8-118">Return value</span></span>

<span data-ttu-id="ad1b8-119">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ad1b8-120">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ad1b8-120">Error codes</span></span>

<span data-ttu-id="ad1b8-121">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ad1b8-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ad1b8-122">Nome</span><span class="sxs-lookup"><span data-stu-id="ad1b8-122">Name</span></span>                                                                                              | <span data-ttu-id="ad1b8-123">Significato</span><span class="sxs-lookup"><span data-stu-id="ad1b8-123">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="ad1b8-124"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ad1b8-124"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="ad1b8-125">*size* non è 2, 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-125">*size* was not 2, 3, or 4.</span></span> <br/>        |
| <dl> <span data-ttu-id="ad1b8-126"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ad1b8-126"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="ad1b8-127">il *tipo* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-127">*type* was not an accepted value.</span></span><br/>  |
| <dl> <span data-ttu-id="ad1b8-128"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ad1b8-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="ad1b8-129">*stride* o *count* è negativo.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-129">*stride* or *count* was negative.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="ad1b8-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad1b8-130">Remarks</span></span>

<span data-ttu-id="ad1b8-131">La funzione **glVertexPointer** specifica il percorso e i dati di una matrice di coordinate del vertice da usare durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-131">The **glVertexPointer** function specifies the location and data of an array of vertex coordinates to use when rendering.</span></span> <span data-ttu-id="ad1b8-132">Il parametro *size* specifica il numero di coordinate per vertice.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-132">The *size* parameter specifies the number of coordinates per vertex.</span></span> <span data-ttu-id="ad1b8-133">Il parametro di *tipo* specifica il tipo di dati di ogni coordinata del vertice.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-133">The *type* parameter specifies the data type of each vertex coordinate.</span></span> <span data-ttu-id="ad1b8-134">Il parametro *stride* determina l'offset dei byte da un vertice a quello successivo, abilitando la compressione di vertici e attributi in una singola matrice o archiviazione in matrici separate.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-134">The *stride* parameter determines the byte offset from one vertex to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="ad1b8-135">In alcune implementazioni, l'archiviazione dei vertici e degli attributi in una singola matrice può essere più efficiente rispetto all'uso di matrici separate (vedere [**glInterleavedArrays**](glinterleavedarrays.md)).</span><span class="sxs-lookup"><span data-stu-id="ad1b8-135">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays (see [**glInterleavedArrays**](glinterleavedarrays.md)).</span></span>

<span data-ttu-id="ad1b8-136">Una matrice di vertici viene abilitata quando si specifica la \_ costante della matrice di vertici GL \_ con [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="ad1b8-136">A vertex array is enabled when you specify the GL\_VERTEX\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="ad1b8-137">Se abilitata, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md)e [**glArrayElement**](glarrayelement.md) usano la matrice di vertici.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-137">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md), and [**glArrayElement**](glarrayelement.md) use the vertex array.</span></span> <span data-ttu-id="ad1b8-138">Per impostazione predefinita, la matrice di vertici è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-138">By default, the vertex array is disabled.</span></span>

<span data-ttu-id="ad1b8-139">Non è possibile includere **glVertexPointer** negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-139">You cannot include **glVertexPointer** in display lists.</span></span>

<span data-ttu-id="ad1b8-140">Quando si specifica una matrice di vertici utilizzando **glVertexPointer**, i valori di tutti i parametri della matrice di vertici della funzione vengono salvati in uno stato lato client ed è possibile memorizzare nella cache elementi statici della matrice.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-140">When you specify a vertex array using **glVertexPointer**, the values of all the function's vertex array parameters are saved in a client-side state, and static array elements can be cached.</span></span> <span data-ttu-id="ad1b8-141">Poiché i parametri della matrice Vertex sono stati lato client, i relativi valori non vengono salvati né ripristinati da [**glPushAttrib**](glpushattrib.md) e **glPopAttrib**.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-141">Because the vertex array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span>

<span data-ttu-id="ad1b8-142">Sebbene non venga generato alcun errore se si chiama **glVertexPointer** nelle coppie [**glBegin**](glbegin.md) e [**glEnd**](glend.md) , i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-142">Although no error is generated if you call **glVertexPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="ad1b8-143">Le funzioni seguenti consentono di recuperare informazioni correlate a **glVertexPointer**:</span><span class="sxs-lookup"><span data-stu-id="ad1b8-143">The following functions retrieve information related to **glVertexPointer**:</span></span>

<span data-ttu-id="ad1b8-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con dimensione della \_ matrice di vertici dell'argomento GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="ad1b8-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_VERTEX\_ARRAY\_SIZE</span></span>

<span data-ttu-id="ad1b8-145">**glGet** con argomento della \_ matrice di vertici dell'argomento GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="ad1b8-145">**glGet** with argument GL\_VERTEX\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="ad1b8-146">**glGet** con argomento \_ numero di matrici di vertici \_ \_</span><span class="sxs-lookup"><span data-stu-id="ad1b8-146">**glGet** with argument GL\_VERTEX\_ARRAY\_COUNT</span></span>

<span data-ttu-id="ad1b8-147">**glGet** con tipo di \_ matrice di vertici GL argomento \_ \_</span><span class="sxs-lookup"><span data-stu-id="ad1b8-147">**glGet** with argument GL\_VERTEX\_ARRAY\_TYPE</span></span>

<span data-ttu-id="ad1b8-148">[**glGetPointerv**](glgetpointerv.md) con puntatore alla \_ matrice del vertice GL dell'argomento \_ \_</span><span class="sxs-lookup"><span data-stu-id="ad1b8-148">[**glGetPointerv**](glgetpointerv.md) with argument GL\_VERTEX\_ARRAY\_POINTER</span></span>

<span data-ttu-id="ad1b8-149">[**glIsEnabled**](glisenabled.md) con argomento \_ matrice di vertici GL \_</span><span class="sxs-lookup"><span data-stu-id="ad1b8-149">[**glIsEnabled**](glisenabled.md) with argument GL\_VERTEX\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="ad1b8-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad1b8-150">Requirements</span></span>



| <span data-ttu-id="ad1b8-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad1b8-151">Requirement</span></span> | <span data-ttu-id="ad1b8-152">Valore</span><span class="sxs-lookup"><span data-stu-id="ad1b8-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad1b8-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad1b8-153">Minimum supported client</span></span><br/> | <span data-ttu-id="ad1b8-154">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ad1b8-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ad1b8-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad1b8-155">Minimum supported server</span></span><br/> | <span data-ttu-id="ad1b8-156">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ad1b8-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ad1b8-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad1b8-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad1b8-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad1b8-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ad1b8-159">Libreria</span><span class="sxs-lookup"><span data-stu-id="ad1b8-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="ad1b8-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad1b8-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ad1b8-161">DLL</span><span class="sxs-lookup"><span data-stu-id="ad1b8-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad1b8-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad1b8-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad1b8-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad1b8-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad1b8-164">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-164">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="ad1b8-165">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-165">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="ad1b8-166">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-166">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="ad1b8-167">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-167">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="ad1b8-168">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-168">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="ad1b8-169">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-169">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="ad1b8-170">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-170">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="ad1b8-171">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-171">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="ad1b8-172">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-172">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="ad1b8-173">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-173">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="ad1b8-174">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-174">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> </dl>

 

 






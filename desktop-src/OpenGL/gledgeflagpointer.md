---
title: funzione glEdgeFlagPointer (GL. h)
description: La funzione glEdgeFlagPointer definisce una matrice di flag perimetrali.
ms.assetid: e0e7e442-533d-4c41-addd-a215ce0b1c56
keywords:
- funzione glEdgeFlagPointer OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4390a9838fef418763aa4bcafbf815ab0cdf3466
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742207"
---
# <a name="gledgeflagpointer-function"></a><span data-ttu-id="706a1-104">glEdgeFlagPointer (funzione)</span><span class="sxs-lookup"><span data-stu-id="706a1-104">glEdgeFlagPointer function</span></span>

<span data-ttu-id="706a1-105">La funzione **glEdgeFlagPointer** definisce una matrice di flag perimetrali.</span><span class="sxs-lookup"><span data-stu-id="706a1-105">The **glEdgeFlagPointer** function defines an array of edge flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="706a1-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="706a1-106">Syntax</span></span>


```C++
void WINAPI glEdgeFlagPointer(
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="706a1-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="706a1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="706a1-108">*stride*</span><span class="sxs-lookup"><span data-stu-id="706a1-108">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="706a1-109">Offset dei byte tra i flag Edge consecutivi.</span><span class="sxs-lookup"><span data-stu-id="706a1-109">The byte offset between consecutive edge flags.</span></span> <span data-ttu-id="706a1-110">Quando *stride* è zero, i flag perimetrali sono strettamente compressi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="706a1-110">When *stride* is zero, the edge flags are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="706a1-111">*indicatore di misura*</span><span class="sxs-lookup"><span data-stu-id="706a1-111">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="706a1-112">Puntatore al primo flag di bordo nella matrice.</span><span class="sxs-lookup"><span data-stu-id="706a1-112">A pointer to the first edge flag in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="706a1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="706a1-113">Return value</span></span>

<span data-ttu-id="706a1-114">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="706a1-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="706a1-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="706a1-115">Error codes</span></span>

<span data-ttu-id="706a1-116">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="706a1-116">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="706a1-117">Nome</span><span class="sxs-lookup"><span data-stu-id="706a1-117">Name</span></span>                                                                                             | <span data-ttu-id="706a1-118">Significato</span><span class="sxs-lookup"><span data-stu-id="706a1-118">Meaning</span></span>                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="706a1-119"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="706a1-119"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="706a1-120">*stride* o *count* è negativo.</span><span class="sxs-lookup"><span data-stu-id="706a1-120">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="706a1-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="706a1-121">Remarks</span></span>

<span data-ttu-id="706a1-122">La funzione **glEdgeFlagPointer** specifica il percorso e i dati di una matrice di flag perimetrali booleani da usare durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="706a1-122">The **glEdgeFlagPointer** function specifies the location and data of an array of Boolean edge flags to use when rendering.</span></span> <span data-ttu-id="706a1-123">Il parametro *stride* determina l'offset dei byte da un flag Edge a quello successivo, che consente di comprimere i vertici e gli attributi in una singola matrice o nello spazio di archiviazione in matrici separate.</span><span class="sxs-lookup"><span data-stu-id="706a1-123">The *stride* parameter determines the byte offset from one edge flag to the next, which enables the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="706a1-124">In alcune implementazioni, l'archiviazione dei vertici e degli attributi in una singola matrice può essere più efficiente rispetto all'utilizzo di matrici separate.</span><span class="sxs-lookup"><span data-stu-id="706a1-124">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span>

<span data-ttu-id="706a1-125">Una matrice di flag Edge viene abilitata quando si specifica la \_ \_ costante array del flag di bordo GL \_ con [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="706a1-125">An edge-flag array is enabled when you specify the GL\_EDGE\_FLAG\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="706a1-126">Se abilitata, [**glDrawArrays**](gldrawarrays.md) o [**glArrayElement**](glarrayelement.md) usa la matrice del flag Edge.</span><span class="sxs-lookup"><span data-stu-id="706a1-126">When enabled, [**glDrawArrays**](gldrawarrays.md) or [**glArrayElement**](glarrayelement.md) uses the edge-flag array.</span></span> <span data-ttu-id="706a1-127">Per impostazione predefinita, la matrice del flag Edge è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="706a1-127">By default the edge-flag array is disabled.</span></span>

<span data-ttu-id="706a1-128">Usare **glDrawArrays** per costruire una sequenza di primitive (tutti dello stesso tipo) dalle matrici di attributi Vertex e vertex specificati.</span><span class="sxs-lookup"><span data-stu-id="706a1-128">Use **glDrawArrays** to construct a sequence of primitives (all of the same type) from prespecified vertex and vertex attribute arrays.</span></span> <span data-ttu-id="706a1-129">Usare **glArrayElement** per specificare le primitive indicizzando i vertici e gli attributi dei vertici e [**glDrawElements**](gldrawelements.md) per costruire una sequenza di primitive indicizzando i vertici e gli attributi dei vertici.</span><span class="sxs-lookup"><span data-stu-id="706a1-129">Use **glArrayElement** to specify primitives by indexing vertices and vertex attributes, and [**glDrawElements**](gldrawelements.md) to construct a sequence of primitives by indexing vertices and vertex attributes.</span></span>

<span data-ttu-id="706a1-130">Non è possibile includere **glEdgeFlagPointer** negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="706a1-130">You cannot include **glEdgeFlagPointer** in display lists.</span></span>

<span data-ttu-id="706a1-131">Quando si specifica una matrice di flag Edge usando **glEdgeFlagPointer**, i valori di tutti i parametri della matrice del flag Edge della funzione vengono salvati in uno stato lato client e gli elementi della matrice statica possono essere memorizzati nella cache.</span><span class="sxs-lookup"><span data-stu-id="706a1-131">When you specify an edge-flag array using **glEdgeFlagPointer**, the values of all the function's edge-flag array parameters are saved in a client-side state and static array elements can be cached.</span></span> <span data-ttu-id="706a1-132">Poiché i parametri della matrice del flag Edge sono in uno stato lato client, [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) non salvano o ripristinano i valori.</span><span class="sxs-lookup"><span data-stu-id="706a1-132">Because the edge-flag array parameters are in a client-side state, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) do not save or restore their values.</span></span>

<span data-ttu-id="706a1-133">Sebbene la chiamata a **glEdgeFlagPointer** all'interno di una coppia [**glBegin**](glbegin.md) / [**glEnd**](glend.md) non generi un errore, i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="706a1-133">Although calling **glEdgeFlagPointer** within a [**glBegin**](glbegin.md)/[**glend**](glend.md) pair does not generate an error, the results are undefined.</span></span>

<span data-ttu-id="706a1-134">Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glEdgeFlagPointer** :</span><span class="sxs-lookup"><span data-stu-id="706a1-134">The following functions retrieve information related to the **glEdgeFlagPointer** function:</span></span>

<span data-ttu-id="706a1-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento di \_ matrice di flag Edge GL \_ \_ \_ stride</span><span class="sxs-lookup"><span data-stu-id="706a1-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_EDGE\_FLAG\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="706a1-136">**glGet** con argomento \_ numero di \_ matrici di flag Edge \_ \_</span><span class="sxs-lookup"><span data-stu-id="706a1-136">**glGet** with argument GL\_EDGE\_FLAG\_ARRAY\_COUNT</span></span>

<span data-ttu-id="706a1-137">[](glgetpointerv.md) puntatore alla matrice del \_ flag Edge GL dell'argomento glGetPointerv \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="706a1-137">[**glGetPointerv**](glgetpointerv.md) with argument GL\_EDGE\_FLAG\_ARRAY\_POINTER</span></span>

<span data-ttu-id="706a1-138">[**glIsEnabled**](glisenabled.md) con argomento \_ matrice di \_ flag \_ Edge GL</span><span class="sxs-lookup"><span data-stu-id="706a1-138">[**glIsEnabled**](glisenabled.md) with argument GL\_EDGE\_FLAG\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="706a1-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="706a1-139">Requirements</span></span>



| <span data-ttu-id="706a1-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="706a1-140">Requirement</span></span> | <span data-ttu-id="706a1-141">Valore</span><span class="sxs-lookup"><span data-stu-id="706a1-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="706a1-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="706a1-142">Minimum supported client</span></span><br/> | <span data-ttu-id="706a1-143">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="706a1-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="706a1-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="706a1-144">Minimum supported server</span></span><br/> | <span data-ttu-id="706a1-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="706a1-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="706a1-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="706a1-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="706a1-147"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="706a1-147"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="706a1-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="706a1-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="706a1-149"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="706a1-149"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="706a1-150">DLL</span><span class="sxs-lookup"><span data-stu-id="706a1-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="706a1-151"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="706a1-151"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="706a1-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="706a1-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="706a1-153">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="706a1-153">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="706a1-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="706a1-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="706a1-155">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="706a1-155">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="706a1-156">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="706a1-156">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="706a1-157">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="706a1-157">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="706a1-158">**Remo**</span><span class="sxs-lookup"><span data-stu-id="706a1-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="706a1-159">**glGet**</span><span class="sxs-lookup"><span data-stu-id="706a1-159">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="706a1-160">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="706a1-160">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="706a1-161">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="706a1-161">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="706a1-162">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="706a1-162">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="706a1-163">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="706a1-163">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="706a1-164">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="706a1-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="706a1-165">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="706a1-165">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="706a1-166">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="706a1-166">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="706a1-167">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="706a1-167">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="706a1-168">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="706a1-168">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 






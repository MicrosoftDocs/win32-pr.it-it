---
title: funzione glTexCoordPointer (GL. h)
description: La funzione glTexCoordPointer definisce una matrice di coordinate di trama.
ms.assetid: c3640a1b-ccc7-4f1a-94a5-a164f7377dbc
keywords:
- funzione glTexCoordPointer OpenGL
topic_type:
- apiref
api_name:
- glTexCoordPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: febc9c79bdbc4a1ed1c14380af47f36309f12662
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302755"
---
# <a name="gltexcoordpointer-function"></a><span data-ttu-id="fb1ec-104">glTexCoordPointer (funzione)</span><span class="sxs-lookup"><span data-stu-id="fb1ec-104">glTexCoordPointer function</span></span>

<span data-ttu-id="fb1ec-105">La funzione **glTexCoordPointer** definisce una matrice di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-105">The **glTexCoordPointer** function defines an array of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb1ec-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb1ec-106">Syntax</span></span>


```C++
void WINAPI glTexCoordPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="fb1ec-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb1ec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb1ec-108">*size*</span><span class="sxs-lookup"><span data-stu-id="fb1ec-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="fb1ec-109">Numero di coordinate per ogni elemento di matrice.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-109">The number of coordinates per array element.</span></span> <span data-ttu-id="fb1ec-110">Il valore delle *dimensioni* deve essere 1, 2, 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-110">The value of *size* must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="fb1ec-111">*type*</span><span class="sxs-lookup"><span data-stu-id="fb1ec-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="fb1ec-112">Il tipo di dati di ogni coordinata di trama nella matrice usando le costanti simboliche seguenti: **GL \_ short**, **GL \_ int**, **GL \_ float** e **GL \_ Double**.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-112">The data type of each texture coordinate in the array using the following symbolic constants: **GL\_SHORT**, **GL\_INT**, **GL\_FLOAT**, and **GL\_DOUBLE**.</span></span>

</dd> <dt>

<span data-ttu-id="fb1ec-113">*stride*</span><span class="sxs-lookup"><span data-stu-id="fb1ec-113">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="fb1ec-114">Offset dei byte tra gli elementi consecutivi della matrice.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-114">The byte offset between consecutive array elements.</span></span> <span data-ttu-id="fb1ec-115">Quando *stride* è zero, gli elementi della matrice sono strettamente compressi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-115">When *stride* is zero, the array elements are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="fb1ec-116">*indicatore di misura*</span><span class="sxs-lookup"><span data-stu-id="fb1ec-116">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="fb1ec-117">Puntatore alla prima coordinata del primo elemento nella matrice.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-117">A pointer to the first coordinate of the first element in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb1ec-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb1ec-118">Return value</span></span>

<span data-ttu-id="fb1ec-119">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fb1ec-120">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="fb1ec-120">Error codes</span></span>

<span data-ttu-id="fb1ec-121">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="fb1ec-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fb1ec-122">Nome</span><span class="sxs-lookup"><span data-stu-id="fb1ec-122">Name</span></span>                                                                                              | <span data-ttu-id="fb1ec-123">Significato</span><span class="sxs-lookup"><span data-stu-id="fb1ec-123">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="fb1ec-124"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fb1ec-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="fb1ec-125">il *tipo* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-125">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="fb1ec-126"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fb1ec-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="fb1ec-127">*size* non è 1, 2, 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-127">*size* was not 1, 2, 3, or 4.</span></span><br/>     |
| <dl> <span data-ttu-id="fb1ec-128"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fb1ec-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="fb1ec-129">*stride* è negativo.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-129">*stride* was negative.</span></span><br/>            |



## <a name="remarks"></a><span data-ttu-id="fb1ec-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb1ec-130">Remarks</span></span>

<span data-ttu-id="fb1ec-131">La funzione **glTexCoordPointer** specifica il percorso e i dati di una matrice di coordinate di trama da usare durante il rendering. Il parametro *size* specifica il numero di coordinate usate per ogni elemento della matrice. Il parametro di *tipo* specifica il tipo di dati di ogni coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-131">The **glTexCoordPointer** function specifies the location and data of an array of texture coordinates to use when rendering.The *size* parameter specifies the number of coordinates used for each element of the array.The *type* parameter specifies the data type of each texture coordinate.</span></span> <span data-ttu-id="fb1ec-132">Il parametro *stride* determina l'offset dei byte da un elemento della matrice alla successiva, abilitando la compressione di vertici e attributi in una singola matrice o archiviazione in matrici separate.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-132">The *stride* parameter determines the byte offset from one array element to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="fb1ec-133">In alcune implementazioni, l'archiviazione dei vertici e degli attributi in una singola matrice può essere più efficiente rispetto all'utilizzo di matrici separate.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-133">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span> <span data-ttu-id="fb1ec-134">Per ulteriori informazioni, vedere [**glInterleavedArrays**](glinterleavedarrays.md).</span><span class="sxs-lookup"><span data-stu-id="fb1ec-134">For more information, see [**glInterleavedArrays**](glinterleavedarrays.md).</span></span> <span data-ttu-id="fb1ec-135">Quando viene specificata una matrice di coordinate di trama, le dimensioni, il tipo, lo stride e il puntatore vengono salvati sullo stato del lato client.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-135">When a texture coordinate array is specified, size, type, stride, and pointer are saved client-side state.</span></span>

<span data-ttu-id="fb1ec-136">Una matrice di coordinate di trama viene abilitata quando si specifica la costante della **\_ \_ \_ matrice Coord della trama GL** con [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="fb1ec-136">A texture coordinate array is enabled when you specify the **GL\_TEXTURE\_COORD\_ARRAY** constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="fb1ec-137">Quando Enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md)e [**glArrayElement**](glarrayelement.md) usano la matrice di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-137">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md), and [**glArrayElement**](glarrayelement.md) use the texture coordinate array.</span></span> <span data-ttu-id="fb1ec-138">Per impostazione predefinita, la matrice di coordinate di trama è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-138">By default the texture coordinate array is disabled.</span></span>

<span data-ttu-id="fb1ec-139">Non è possibile includere **glTexCoordPointer** negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-139">You cannot include **glTexCoordPointer** in display lists.</span></span>

<span data-ttu-id="fb1ec-140">Quando si specifica una matrice di coordinate di trama usando **glTexCoordPointer**, i valori di tutti i parametri della matrice di coordinate di trama della funzione vengono salvati in uno stato lato client ed è possibile memorizzare nella cache elementi statici della matrice.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-140">When you specify a texture coordinate array using **glTexCoordPointer**, the values of all the function's texture coordinate array parameters are saved in a client-side state, and static array elements can be cached.</span></span> <span data-ttu-id="fb1ec-141">Poiché i parametri della matrice di coordinate di trama sono stati lato client, i relativi valori non vengono salvati né ripristinati da [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="fb1ec-141">Because the texture coordinate array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

<span data-ttu-id="fb1ec-142">Sebbene non venga generato alcun errore quando si chiama **glTexCoordPointer** all'interno di coppie [**glBegin**](glbegin.md) e [**glEnd**](glend.md) , i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="fb1ec-142">Although no error is generated when you call **glTexCoordPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="fb1ec-143">Le funzioni seguenti consentono di recuperare informazioni correlate a **glTexCoordPointer**:</span><span class="sxs-lookup"><span data-stu-id="fb1ec-143">The following functions retrieve information related to **glTexCoordPointer**:</span></span>

<span data-ttu-id="fb1ec-144">[**glIsEnabled**](glisenabled.md) con argomento **GL \_ texture \_ Coord \_ Array**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-144">[**glIsEnabled**](glisenabled.md) with argument **GL\_TEXTURE\_COORD\_ARRAY**</span></span>

<span data-ttu-id="fb1ec-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento **GL \_ texture \_ Coord \_ matrice \_ dimensione**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument **GL\_TEXTURE\_COORD\_ARRAY\_SIZE**</span></span>

<span data-ttu-id="fb1ec-146">**glGet** con argomento **GL \_ texture \_ Coord \_ array \_ stride**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-146">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_STRIDE**</span></span>

<span data-ttu-id="fb1ec-147">**glGet** con argomento **GL \_ texture \_ Coord \_ \_ numero di matrici**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-147">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_COUNT**</span></span>

<span data-ttu-id="fb1ec-148">**glGet** con argomento **GL \_ texture \_ Coord \_ \_ tipo matrice**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-148">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_TYPE**</span></span>

<span data-ttu-id="fb1ec-149">[**glGetPointerv**](glgetpointerv.md) con argomento **GL \_ trama \_ Coord \_ matrice \_ puntatore**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-149">[**glGetPointerv**](glgetpointerv.md) with argument **GL\_TEXTURE\_COORD\_ARRAY\_POINTER**</span></span>

## <a name="requirements"></a><span data-ttu-id="fb1ec-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb1ec-150">Requirements</span></span>



| <span data-ttu-id="fb1ec-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb1ec-151">Requirement</span></span> | <span data-ttu-id="fb1ec-152">Valore</span><span class="sxs-lookup"><span data-stu-id="fb1ec-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb1ec-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb1ec-153">Minimum supported client</span></span><br/> | <span data-ttu-id="fb1ec-154">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fb1ec-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fb1ec-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb1ec-155">Minimum supported server</span></span><br/> | <span data-ttu-id="fb1ec-156">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fb1ec-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fb1ec-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb1ec-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb1ec-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb1ec-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fb1ec-159">Libreria</span><span class="sxs-lookup"><span data-stu-id="fb1ec-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb1ec-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb1ec-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fb1ec-161">DLL</span><span class="sxs-lookup"><span data-stu-id="fb1ec-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb1ec-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb1ec-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb1ec-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb1ec-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb1ec-164">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-164">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="fb1ec-165">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-165">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="fb1ec-166">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-166">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="fb1ec-167">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-167">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="fb1ec-168">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-168">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="fb1ec-169">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-169">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="fb1ec-170">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-170">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="fb1ec-171">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-171">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="fb1ec-172">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-172">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="fb1ec-173">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-173">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="fb1ec-174">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-174">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="fb1ec-175">**glPopClientAttrib**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-175">**glPopClientAttrib**</span></span>](glpopclientattrib.md)
</dt> <dt>

[<span data-ttu-id="fb1ec-176">**glPushClientAttrib**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-176">**glPushClientAttrib**</span></span>](glpushclientattrib.md)
</dt> <dt>

[<span data-ttu-id="fb1ec-177">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="fb1ec-178">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="fb1ec-178">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 






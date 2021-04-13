---
title: funzione glIndexPointer (GL. h)
description: La funzione glIndexPointer definisce una matrice di indici dei colori.
ms.assetid: b435d950-1f87-4041-93e4-f1f8786cabdb
keywords:
- funzione glIndexPointer OpenGL
topic_type:
- apiref
api_name:
- glIndexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca6858d7d1e3f13e4155bd40307a53b22e80a56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475262"
---
# <a name="glindexpointer-function"></a><span data-ttu-id="62046-104">glIndexPointer (funzione)</span><span class="sxs-lookup"><span data-stu-id="62046-104">glIndexPointer function</span></span>

<span data-ttu-id="62046-105">La funzione **glIndexPointer** definisce una matrice di indici dei colori.</span><span class="sxs-lookup"><span data-stu-id="62046-105">The **glIndexPointer** function defines an array of color indexes.</span></span>

## <a name="syntax"></a><span data-ttu-id="62046-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62046-106">Syntax</span></span>


```C++
void WINAPI glIndexPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="62046-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="62046-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62046-108">*type*</span><span class="sxs-lookup"><span data-stu-id="62046-108">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="62046-109">Il tipo di dati di ogni indice dei colori nella matrice usando le costanti simboliche seguenti: GL \_ short, GL \_ int, GL \_ float, GL \_ Double.</span><span class="sxs-lookup"><span data-stu-id="62046-109">The data type of each color index in the array using the following symbolic constants: GL\_SHORT, GL\_INT, GL\_FLOAT, GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="62046-110">*stride*</span><span class="sxs-lookup"><span data-stu-id="62046-110">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="62046-111">Offset dei byte tra indici di colore consecutivi.</span><span class="sxs-lookup"><span data-stu-id="62046-111">The byte offset between consecutive color indexes.</span></span> <span data-ttu-id="62046-112">Quando *stride* è zero, gli indici dei colori sono strettamente compressi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="62046-112">When *stride* is zero, the color indexes are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="62046-113">*indicatore di misura*</span><span class="sxs-lookup"><span data-stu-id="62046-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="62046-114">Puntatore al primo indice dei colori nella matrice.</span><span class="sxs-lookup"><span data-stu-id="62046-114">A pointer to the first color index in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62046-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62046-115">Return value</span></span>

<span data-ttu-id="62046-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="62046-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="62046-117">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="62046-117">Error codes</span></span>

<span data-ttu-id="62046-118">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="62046-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="62046-119">Nome</span><span class="sxs-lookup"><span data-stu-id="62046-119">Name</span></span>                                                                                              | <span data-ttu-id="62046-120">Significato</span><span class="sxs-lookup"><span data-stu-id="62046-120">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="62046-121"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="62046-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="62046-122">il *tipo* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="62046-122">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="62046-123"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="62046-123"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="62046-124">*stride* o *count* è negativo.</span><span class="sxs-lookup"><span data-stu-id="62046-124">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="62046-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="62046-125">Remarks</span></span>

<span data-ttu-id="62046-126">La funzione **glIndexPointer** specifica il percorso e i dati di una matrice di indici dei colori da usare durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="62046-126">The **glIndexPointer** function specifies the location and data of an array of color indexes to use when rendering.</span></span> <span data-ttu-id="62046-127">Il parametro di *tipo* specifica il tipo di dati di ogni indice di colore e *stride* determina l'offset dei byte da un indice di colore alla successiva, abilitando la compressione di vertici e attributi in una singola matrice o archiviazione in matrici separate.</span><span class="sxs-lookup"><span data-stu-id="62046-127">The *type* parameter specifies the data type of each color index and *stride* determines the byte offset from one color index to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="62046-128">In alcune implementazioni, l'archiviazione dei vertici e degli attributi in una singola matrice può essere più efficiente rispetto all'utilizzo di matrici separate.</span><span class="sxs-lookup"><span data-stu-id="62046-128">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span> <span data-ttu-id="62046-129">Per ulteriori informazioni, vedere [**glInterleavedArrays**](glinterleavedarrays.md).</span><span class="sxs-lookup"><span data-stu-id="62046-129">For more information, see [**glInterleavedArrays**](glinterleavedarrays.md).</span></span>

<span data-ttu-id="62046-130">Una matrice di indice dei colori viene abilitata quando si specifica \_ la \_ costante della matrice di indice GL con [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="62046-130">A color-index array is enabled when you specify the GL\_INDEX\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="62046-131">Quando è abilitata, [**glDrawArrays**](gldrawarrays.md) e [**glArrayElement**](glarrayelement.md) usano la matrice di indicizzazione dei colori.</span><span class="sxs-lookup"><span data-stu-id="62046-131">When enabled, [**glDrawArrays**](gldrawarrays.md) and [**glArrayElement**](glarrayelement.md) use the color-index array.</span></span> <span data-ttu-id="62046-132">Per impostazione predefinita, la matrice di indice dei colori è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="62046-132">By default the color-index array is disabled.</span></span>

<span data-ttu-id="62046-133">Non è possibile includere **glIndexPointer** negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="62046-133">You cannot include **glIndexPointer** in display lists.</span></span>

<span data-ttu-id="62046-134">Quando si specifica una matrice di indice dei colori utilizzando **glIndexPointer**, i valori di tutti i parametri della matrice di indice dei colori della funzione vengono salvati in uno stato lato client e gli elementi della matrice statica possono essere memorizzati nella cache.</span><span class="sxs-lookup"><span data-stu-id="62046-134">When you specify a color-index array using **glIndexPointer**, the values of all the function's color-index array parameters are saved in a client-side state and static array elements can be cached.</span></span> <span data-ttu-id="62046-135">Poiché i parametri della matrice di indice dei colori sono stati lato client, i relativi valori non vengono salvati né ripristinati da [**glPushAttrib**](glpushattrib.md) e **glPopAttrib**.</span><span class="sxs-lookup"><span data-stu-id="62046-135">Because the color-index array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span>

<span data-ttu-id="62046-136">Sebbene non venga generato alcun errore quando si chiama **glIndexPointer** all'interno di coppie [**glBegin**](glbegin.md) e **glEnd** , i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="62046-136">Although no error is generated when you call **glIndexPointer** within [**glBegin**](glbegin.md) and **glEnd** pairs, the results are undefined.</span></span>

<span data-ttu-id="62046-137">Le funzioni seguenti consentono di recuperare informazioni correlate a **glIndexPointer**:</span><span class="sxs-lookup"><span data-stu-id="62046-137">The following functions retrieve information related to **glIndexPointer**:</span></span>

<span data-ttu-id="62046-138">[**glIsEnabled**](glisenabled.md) con argomento \_ Array GL index \_</span><span class="sxs-lookup"><span data-stu-id="62046-138">[**glIsEnabled**](glisenabled.md) with argument GL\_INDEX\_ARRAY</span></span>

<span data-ttu-id="62046-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ matrice di indice GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="62046-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="62046-140">**glGet** con argomento \_ numero di \_ matrici di indice GL \_</span><span class="sxs-lookup"><span data-stu-id="62046-140">**glGet** with argument GL\_INDEX\_ARRAY\_COUNT</span></span>

<span data-ttu-id="62046-141">**glGet** con tipo di \_ matrice di indice GL dell'argomento \_ \_</span><span class="sxs-lookup"><span data-stu-id="62046-141">**glGet** with argument GL\_INDEX\_ARRAY\_TYPE</span></span>

<span data-ttu-id="62046-142">**glGet** con le \_ dimensioni della \_ matrice dell'indice GL dell'argomento \_</span><span class="sxs-lookup"><span data-stu-id="62046-142">**glGet** with argument GL\_INDEX\_ARRAY\_SIZE</span></span>

<span data-ttu-id="62046-143">[**glGetPointerv**](glgetpointerv.md) con puntatore alla \_ matrice di indice GL degli argomenti \_ \_</span><span class="sxs-lookup"><span data-stu-id="62046-143">[**glGetPointerv**](glgetpointerv.md) with argument GL\_INDEX\_ARRAY\_POINTER</span></span>

## <a name="requirements"></a><span data-ttu-id="62046-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62046-144">Requirements</span></span>



| <span data-ttu-id="62046-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="62046-145">Requirement</span></span> | <span data-ttu-id="62046-146">Valore</span><span class="sxs-lookup"><span data-stu-id="62046-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62046-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62046-147">Minimum supported client</span></span><br/> | <span data-ttu-id="62046-148">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="62046-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="62046-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62046-149">Minimum supported server</span></span><br/> | <span data-ttu-id="62046-150">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="62046-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="62046-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62046-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="62046-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="62046-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="62046-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="62046-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="62046-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62046-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="62046-155">DLL</span><span class="sxs-lookup"><span data-stu-id="62046-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62046-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62046-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62046-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62046-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62046-158">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="62046-158">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="62046-159">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="62046-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="62046-160">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="62046-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="62046-161">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="62046-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="62046-162">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="62046-162">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="62046-163">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="62046-163">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="62046-164">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="62046-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="62046-165">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="62046-165">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="62046-166">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="62046-166">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="62046-167">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="62046-167">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 






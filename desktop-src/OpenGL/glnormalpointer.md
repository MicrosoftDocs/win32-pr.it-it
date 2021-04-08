---
title: funzione glNormalPointer (GL. h)
description: La funzione glNormalPointer definisce una matrice di normali.
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
keywords:
- funzione glNormalPointer OpenGL
topic_type:
- apiref
api_name:
- glNormalPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f3abbfbd989351af647557ec64f8ee3172dc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964959"
---
# <a name="glnormalpointer-function"></a><span data-ttu-id="600c3-104">glNormalPointer (funzione)</span><span class="sxs-lookup"><span data-stu-id="600c3-104">glNormalPointer function</span></span>

<span data-ttu-id="600c3-105">La funzione **glNormalPointer** definisce una matrice di normali.</span><span class="sxs-lookup"><span data-stu-id="600c3-105">The **glNormalPointer** function defines an array of normals.</span></span>

## <a name="syntax"></a><span data-ttu-id="600c3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="600c3-106">Syntax</span></span>


```C++
void WINAPI glNormalPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="600c3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="600c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="600c3-108">*type*</span><span class="sxs-lookup"><span data-stu-id="600c3-108">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="600c3-109">Il tipo di dati di ogni coordinata nella matrice usando le costanti simboliche seguenti: GL \_ byte, GL \_ short, GL \_ int, GL \_ float e GL \_ Double.</span><span class="sxs-lookup"><span data-stu-id="600c3-109">The data type of each coordinate in the array using the following symbolic constants: GL\_BYTE, GL\_SHORT, GL\_INT, GL\_FLOAT, and GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="600c3-110">*stride*</span><span class="sxs-lookup"><span data-stu-id="600c3-110">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="600c3-111">Offset dei byte tra le normali consecutive.</span><span class="sxs-lookup"><span data-stu-id="600c3-111">The byte offset between consecutive normals.</span></span> <span data-ttu-id="600c3-112">Quando *stride* è zero, le normali sono strettamente compresse nella matrice.</span><span class="sxs-lookup"><span data-stu-id="600c3-112">When *stride* is zero, the normals are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="600c3-113">*indicatore di misura*</span><span class="sxs-lookup"><span data-stu-id="600c3-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="600c3-114">Puntatore alla prima normale nella matrice.</span><span class="sxs-lookup"><span data-stu-id="600c3-114">A pointer to the first normal in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="600c3-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="600c3-115">Return value</span></span>

<span data-ttu-id="600c3-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="600c3-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="600c3-117">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="600c3-117">Error codes</span></span>

<span data-ttu-id="600c3-118">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="600c3-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="600c3-119">Nome</span><span class="sxs-lookup"><span data-stu-id="600c3-119">Name</span></span>                                                                                                  | <span data-ttu-id="600c3-120">Significato</span><span class="sxs-lookup"><span data-stu-id="600c3-120">Meaning</span></span>                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="600c3-121"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="600c3-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="600c3-122">il *tipo* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="600c3-122">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="600c3-123"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="600c3-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="600c3-124">*stride* o *count* è negativo.</span><span class="sxs-lookup"><span data-stu-id="600c3-124">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="600c3-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="600c3-125">Remarks</span></span>

<span data-ttu-id="600c3-126">La funzione **glNormalPointer** specifica il percorso e i dati di una matrice di normali da usare durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="600c3-126">The **glNormalPointer** function specifies the location and data of an array of normals to use when rendering.</span></span> <span data-ttu-id="600c3-127">Il parametro di *tipo* specifica il tipo di dati di ogni normale coordinata.</span><span class="sxs-lookup"><span data-stu-id="600c3-127">The *type* parameter specifies the data type of each normal coordinate.</span></span> <span data-ttu-id="600c3-128">Il parametro *stride* determina l'offset dei byte da un normale a quello successivo, abilitando la compressione di vertici e attributi in una singola matrice o archiviazione in matrici separate.</span><span class="sxs-lookup"><span data-stu-id="600c3-128">The *stride* parameter determines the byte offset from one normal to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="600c3-129">In alcune implementazioni, l'archiviazione dei vertici e degli attributi in una singola matrice può risultare più efficiente rispetto all'utilizzo di matrici separate; per informazioni dettagliate, vedere [**glInterleavedArrays**](glinterleavedarrays.md) .</span><span class="sxs-lookup"><span data-stu-id="600c3-129">In some implementations storing the vertices and attributes in a single array can be more efficient than using separate arrays; see [**glInterleavedArrays**](glinterleavedarrays.md) for details.</span></span>

<span data-ttu-id="600c3-130">Una matrice normale viene abilitata quando si specifica la \_ \_ costante di matrice GL Normal con [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="600c3-130">A normal array is enabled when you specify the GL\_NORMAL\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="600c3-131">Quando è abilitata, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md) e [**glArrayElement**](glarrayelement.md) usano la matrice normale.</span><span class="sxs-lookup"><span data-stu-id="600c3-131">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md) and [**glArrayElement**](glarrayelement.md) use the normal array.</span></span> <span data-ttu-id="600c3-132">Per impostazione predefinita, la matrice normale è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="600c3-132">By default the normal array is disabled.</span></span>

<span data-ttu-id="600c3-133">Non è possibile includere **glNormalPointer** negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="600c3-133">You cannot include **glNormalPointer** in display lists.</span></span>

<span data-ttu-id="600c3-134">Quando si specifica una matrice normale utilizzando **glNormalPointer**, i valori di tutti i parametri di matrice normali della funzione vengono salvati in uno stato sul lato client.</span><span class="sxs-lookup"><span data-stu-id="600c3-134">When you specify a normal array using **glNormalPointer**, the values of all the function's normal array parameters are saved in a client-side state.</span></span> <span data-ttu-id="600c3-135">Poiché i normali parametri della matrice vengono salvati in uno stato sul lato client, i relativi valori non vengono salvati né ripristinati da [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="600c3-135">Because the normal array parameters are saved in a client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

<span data-ttu-id="600c3-136">Sebbene non venga generato alcun errore quando si chiama **glNormalPointer** all'interno di coppie [**glBegin**](glbegin.md) e [**glEnd**](glend.md) , i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="600c3-136">Although no error is generated when you call **glNormalPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="600c3-137">Le funzioni seguenti sono associate a **glNormalPointer**:</span><span class="sxs-lookup"><span data-stu-id="600c3-137">The following functions are associated with **glNormalPointer**:</span></span>

<span data-ttu-id="600c3-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento con \_ lo \_ stride di matrice normale \_</span><span class="sxs-lookup"><span data-stu-id="600c3-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NORMAL\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="600c3-139">**glGet** con argomento \_ numero di \_ matrici \_ normali</span><span class="sxs-lookup"><span data-stu-id="600c3-139">**glGet** with argument GL\_NORMAL\_ARRAY\_COUNT</span></span>

<span data-ttu-id="600c3-140">**glGet** con tipo di \_ matrice Normal GL argomento \_ \_</span><span class="sxs-lookup"><span data-stu-id="600c3-140">**glGet** with argument GL\_NORMAL\_ARRAY\_TYPE</span></span>

<span data-ttu-id="600c3-141">**glGetPointerv** con puntatore alla matrice di un argomento GL \_ Normal \_ \_</span><span class="sxs-lookup"><span data-stu-id="600c3-141">**glGetPointerv** with argument GL\_NORMAL\_ARRAY\_POINTER</span></span>

<span data-ttu-id="600c3-142">[**glIsEnabled**](glisenabled.md) con matrice GL di argomenti \_ normali \_</span><span class="sxs-lookup"><span data-stu-id="600c3-142">[**glIsEnabled**](glisenabled.md) with argument GL\_NORMAL\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="600c3-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="600c3-143">Requirements</span></span>



| <span data-ttu-id="600c3-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="600c3-144">Requirement</span></span> | <span data-ttu-id="600c3-145">Valore</span><span class="sxs-lookup"><span data-stu-id="600c3-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="600c3-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="600c3-146">Minimum supported client</span></span><br/> | <span data-ttu-id="600c3-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="600c3-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="600c3-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="600c3-148">Minimum supported server</span></span><br/> | <span data-ttu-id="600c3-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="600c3-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="600c3-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="600c3-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="600c3-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="600c3-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="600c3-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="600c3-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="600c3-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="600c3-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="600c3-154">DLL</span><span class="sxs-lookup"><span data-stu-id="600c3-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="600c3-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="600c3-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="600c3-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="600c3-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="600c3-157">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="600c3-157">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="600c3-158">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="600c3-158">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="600c3-159">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="600c3-159">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="600c3-160">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="600c3-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="600c3-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="600c3-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="600c3-162">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="600c3-162">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="600c3-163">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="600c3-163">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="600c3-164">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="600c3-164">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="600c3-165">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="600c3-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="600c3-166">**glInterleavedArrays**</span><span class="sxs-lookup"><span data-stu-id="600c3-166">**glInterleavedArrays**</span></span>](glinterleavedarrays.md)
</dt> <dt>

[<span data-ttu-id="600c3-167">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="600c3-167">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="600c3-168">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="600c3-168">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> <dt>

[<span data-ttu-id="600c3-169">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="600c3-169">**glGetString**</span></span>](glgetstring.md)
</dt> </dl>

 

 






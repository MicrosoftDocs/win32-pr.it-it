---
title: funzione glInterleavedArrays (GL. h)
description: La funzione glInterleavedArrays specifica simultaneamente e Abilita diverse matrici Interleaved in una matrice di aggregazione più grande.
ms.assetid: f1133949-d755-43e3-bf29-8e4c7fb17980
keywords:
- funzione glInterleavedArrays OpenGL
topic_type:
- apiref
api_name:
- glInterleavedArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41403210e78d1a65dd700561243846d6e45bad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400354"
---
# <a name="glinterleavedarrays-function"></a><span data-ttu-id="7c200-104">glInterleavedArrays (funzione)</span><span class="sxs-lookup"><span data-stu-id="7c200-104">glInterleavedArrays function</span></span>

<span data-ttu-id="7c200-105">La funzione **glInterleavedArrays** specifica simultaneamente e Abilita diverse matrici Interleaved in una matrice di aggregazione più grande.</span><span class="sxs-lookup"><span data-stu-id="7c200-105">The **glInterleavedArrays** function simultaneously specifies and enables several interleaved arrays in a larger aggregate array.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c200-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c200-106">Syntax</span></span>


```C++
void WINAPI glInterleavedArrays(
         GLenum  format,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="7c200-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c200-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c200-108">*format*</span><span class="sxs-lookup"><span data-stu-id="7c200-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="7c200-109">Tipo di matrice da abilitare.</span><span class="sxs-lookup"><span data-stu-id="7c200-109">The type of array to enable.</span></span> <span data-ttu-id="7c200-110">Il parametro può assumere uno dei seguenti valori simbolici: GL \_ V2F, GL \_ V3F, GL \_ C4UB \_ V2F, GL \_ C4UB \_ V3F, GL \_ C3F V3F, GL N3F \_ \_ \_ V3F, GL \_ C4F \_ N3F V3F \_ , GL \_ T2F V3F, GL \_ \_ T4F \_ V4F, GL T2F C4UB V3F \_ \_ \_ , GL T2F C3F V3F \_ \_ \_ , GL T2F N3F V3F \_ \_ \_ , GL \_ T2F C4F N3F V3F \_ \_ \_ , o GL \_ T4F \_ C4F \_ \_ N3F V4F.</span><span class="sxs-lookup"><span data-stu-id="7c200-110">The parameter can assume one of the following symbolic values: GL\_V2F, GL\_V3F, GL\_C4UB\_V2F, GL\_C4UB\_V3F, GL\_C3F\_V3F, GL\_N3F\_V3F, GL\_C4F\_N3F\_V3F, GL\_T2F\_V3F, GL\_T4F\_V4F, GL\_T2F\_C4UB\_V3F, GL\_T2F\_C3F\_V3F, GL\_T2F\_N3F\_V3F, GL\_T2F\_C4F\_N3F\_V3F, or GL\_T4F\_C4F\_N3F\_V4F.</span></span>

</dd> <dt>

<span data-ttu-id="7c200-111">*stride*</span><span class="sxs-lookup"><span data-stu-id="7c200-111">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="7c200-112">Offset in byte tra ogni elemento della matrice di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="7c200-112">The offset in bytes between each aggregate array element.</span></span>

</dd> <dt>

<span data-ttu-id="7c200-113">*indicatore di misura*</span><span class="sxs-lookup"><span data-stu-id="7c200-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="7c200-114">Puntatore al primo elemento di una matrice di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="7c200-114">A pointer to the first element of an aggregate array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c200-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c200-115">Return value</span></span>

<span data-ttu-id="7c200-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7c200-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7c200-117">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="7c200-117">Error codes</span></span>

<span data-ttu-id="7c200-118">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="7c200-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7c200-119">Nome</span><span class="sxs-lookup"><span data-stu-id="7c200-119">Name</span></span>                                                                                                  | <span data-ttu-id="7c200-120">Significato</span><span class="sxs-lookup"><span data-stu-id="7c200-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c200-121"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7c200-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="7c200-122">*Format* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="7c200-122">*format* was not an accepted value.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="7c200-123"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7c200-123"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="7c200-124">*stride* è un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="7c200-124">*stride* was a negative value.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="7c200-125"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7c200-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7c200-126">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7c200-126">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7c200-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c200-127">Remarks</span></span>

<span data-ttu-id="7c200-128">Con la funzione **glInterleavedArrays** , è possibile specificare contemporaneamente e abilitare diverse matrici di colore, normali, di trama e di vertex con interfoliazione i cui elementi fanno parte di un elemento di matrice di aggregazione più grande.</span><span class="sxs-lookup"><span data-stu-id="7c200-128">With the **glInterleavedArrays** function, you can simultaneously specify and enable several interleaved color, normal, texture, and vertex arrays whose elements are part of a larger aggregate array element.</span></span> <span data-ttu-id="7c200-129">Per alcune architetture di memoria, questa operazione è più efficiente rispetto alla specifica delle matrici separatamente.</span><span class="sxs-lookup"><span data-stu-id="7c200-129">For some memory architectures, this is more efficient than specifying the arrays separately.</span></span>

<span data-ttu-id="7c200-130">Se il parametro *stride* è zero, gli elementi della matrice di aggregazione vengono archiviati consecutivamente; in caso contrario, i byte *stride* si verificano tra gli elementi della matrice</span><span class="sxs-lookup"><span data-stu-id="7c200-130">If the *stride* parameter is zero then the aggregate array elements are stored consecutively; otherwise *stride* bytes occur between aggregate array elements.</span></span>

<span data-ttu-id="7c200-131">Il parametro *Format* funge da chiave che descrive come estrarre singole matrici dalla matrice di aggregazione:</span><span class="sxs-lookup"><span data-stu-id="7c200-131">The *format* parameter serves as a key that describes how to extract individual arrays from the aggregate array:</span></span>

-   <span data-ttu-id="7c200-132">Se *Format* contiene una T, le coordinate di trama vengono estratte dalla matrice Interleaved.</span><span class="sxs-lookup"><span data-stu-id="7c200-132">If *format* contains a T, then texture coordinates are extracted from the interleaved array.</span></span>
-   <span data-ttu-id="7c200-133">Se è presente C, verranno estratti i valori dei colori.</span><span class="sxs-lookup"><span data-stu-id="7c200-133">If C is present, color values are extracted.</span></span>
-   <span data-ttu-id="7c200-134">Se N è presente, vengono estratte le coordinate normali.</span><span class="sxs-lookup"><span data-stu-id="7c200-134">If N is present, normal coordinates are extracted.</span></span>
-   <span data-ttu-id="7c200-135">Vengono sempre estratte le coordinate del vertice.</span><span class="sxs-lookup"><span data-stu-id="7c200-135">Vertex coordinates are always extracted.</span></span>
-   <span data-ttu-id="7c200-136">I numeri 2, 3 e 4 indicano il numero di valori estratti.</span><span class="sxs-lookup"><span data-stu-id="7c200-136">The digits 2, 3, and 4 denote how many values are extracted.</span></span>
-   <span data-ttu-id="7c200-137">F indica che i valori vengono estratti come valori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="7c200-137">F indicates that values are extracted as floating point values.</span></span>
-   <span data-ttu-id="7c200-138">Se 4UB segue il linguaggio C, i colori possono essere estratti anche come 4 byte senza segno.</span><span class="sxs-lookup"><span data-stu-id="7c200-138">If 4UB follows the C, colors may also be extracted as 4 unsigned bytes.</span></span> <span data-ttu-id="7c200-139">Se un colore viene estratto come 4 byte senza segno, l'elemento della matrice Vertex che segue si trova in corrispondenza del primo indirizzo a virgola mobile possibile allineato.</span><span class="sxs-lookup"><span data-stu-id="7c200-139">If a color is extracted as 4 unsigned bytes, the vertex array element that follows is located at the first possible floating-point aligned address.</span></span>

<span data-ttu-id="7c200-140">Se si chiama **glInterleavedArrays** durante la compilazione di un elenco di visualizzazione, questo non viene compilato nell'elenco ma viene eseguito immediatamente.</span><span class="sxs-lookup"><span data-stu-id="7c200-140">If you call **glInterleavedArrays** while compiling a display list, it is not compiled into the list but is executed immediately.</span></span>

<span data-ttu-id="7c200-141">Non è possibile includere chiamate a **glInterleavedArrays** in **glDisableClientState** tra le chiamate a [**glBegin**](glbegin.md) e la chiamata corrispondente a **glEnd**.</span><span class="sxs-lookup"><span data-stu-id="7c200-141">You cannot include calls to **glInterleavedArrays** in **glDisableClientState** between calls to [**glBegin**](glbegin.md) and the corresponding call to **glEnd**.</span></span>

> [!Note]  
> <span data-ttu-id="7c200-142">La funzione **glInterleavedArrays** è disponibile solo in OpenGL versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="7c200-142">The **glInterleavedArrays** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="7c200-143">La funzione **glInterleavedArrays** viene implementata sul lato client senza protocollo.</span><span class="sxs-lookup"><span data-stu-id="7c200-143">The **glInterleavedArrays** function is implemented on the client side with no protocol.</span></span> <span data-ttu-id="7c200-144">Poiché i parametri della matrice Vertex sono stati lato client, non vengono salvati né ripristinati da [**glPushAttrib**](glpushattrib.md) e **glPopAttrib**.</span><span class="sxs-lookup"><span data-stu-id="7c200-144">Because the vertex array parameters are client-side state, they are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span> <span data-ttu-id="7c200-145">In alternativa, usare [**glPushClientAttrib**](glpushclientattrib.md) e **glPopClientAttrib** .</span><span class="sxs-lookup"><span data-stu-id="7c200-145">Use [**glPushClientAttrib**](glpushclientattrib.md) and **glPopClientAttrib** instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c200-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c200-146">Requirements</span></span>



| <span data-ttu-id="7c200-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c200-147">Requirement</span></span> | <span data-ttu-id="7c200-148">Valore</span><span class="sxs-lookup"><span data-stu-id="7c200-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c200-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c200-149">Minimum supported client</span></span><br/> | <span data-ttu-id="7c200-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7c200-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7c200-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c200-151">Minimum supported server</span></span><br/> | <span data-ttu-id="7c200-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7c200-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7c200-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c200-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c200-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c200-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7c200-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="7c200-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c200-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c200-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7c200-157">DLL</span><span class="sxs-lookup"><span data-stu-id="7c200-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c200-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c200-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c200-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c200-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c200-160">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="7c200-160">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="7c200-161">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="7c200-161">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="7c200-162">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="7c200-162">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="7c200-163">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="7c200-163">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="7c200-164">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="7c200-164">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="7c200-165">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="7c200-165">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="7c200-166">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="7c200-166">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="7c200-167">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="7c200-167">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="7c200-168">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="7c200-168">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="7c200-169">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="7c200-169">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="7c200-170">**glPushClientAttrib**</span><span class="sxs-lookup"><span data-stu-id="7c200-170">**glPushClientAttrib**</span></span>](glpushclientattrib.md)
</dt> <dt>

[<span data-ttu-id="7c200-171">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="7c200-171">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="7c200-172">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="7c200-172">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 






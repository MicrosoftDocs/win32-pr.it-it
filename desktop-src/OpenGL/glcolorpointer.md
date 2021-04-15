---
title: funzione glColorPointer (GL. h)
description: La funzione glColorPointer definisce una matrice di colori.
ms.assetid: 4d9d05fb-691d-4b71-b079-c42dc7103055
keywords:
- funzione glColorPointer OpenGL
topic_type:
- apiref
api_name:
- glColorPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abced52f0d0664e998ad8380e33d43d4af36bcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475845"
---
# <a name="glcolorpointer-function"></a><span data-ttu-id="a27f3-104">glColorPointer (funzione)</span><span class="sxs-lookup"><span data-stu-id="a27f3-104">glColorPointer function</span></span>

<span data-ttu-id="a27f3-105">La funzione **glColorPointer** definisce una matrice di colori.</span><span class="sxs-lookup"><span data-stu-id="a27f3-105">The **glColorPointer** function defines an array of colors.</span></span>

## <a name="syntax"></a><span data-ttu-id="a27f3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a27f3-106">Syntax</span></span>


```C++
void WINAPI glColorPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="a27f3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a27f3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a27f3-108">*size*</span><span class="sxs-lookup"><span data-stu-id="a27f3-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="a27f3-109">Numero di componenti per colore.</span><span class="sxs-lookup"><span data-stu-id="a27f3-109">The number of components per color.</span></span> <span data-ttu-id="a27f3-110">Il valore deve essere 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="a27f3-110">The value must be either 3 or 4.</span></span>

</dd> <dt>

<span data-ttu-id="a27f3-111">*type*</span><span class="sxs-lookup"><span data-stu-id="a27f3-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="a27f3-112">Tipo di dati di ogni componente colore in una matrice di colori.</span><span class="sxs-lookup"><span data-stu-id="a27f3-112">The data type of each color component in a color array.</span></span> <span data-ttu-id="a27f3-113">I tipi di dati accettabili sono specificati con le costanti seguenti: GL \_ byte, GL \_ unsigned \_ byte, GL \_ short, GL \_ unsigned \_ short, GL \_ int, GL \_ unsigned \_ int, GL \_ float o GL \_ Double.</span><span class="sxs-lookup"><span data-stu-id="a27f3-113">Acceptable data types are specified with the following constants: GL\_BYTE, GL\_UNSIGNED\_BYTE, GL\_SHORT, GL\_UNSIGNED\_SHORT, GL\_INT, GL\_UNSIGNED\_INT, GL\_FLOAT, or GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="a27f3-114">*stride*</span><span class="sxs-lookup"><span data-stu-id="a27f3-114">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="a27f3-115">Offset dei byte tra i colori consecutivi.</span><span class="sxs-lookup"><span data-stu-id="a27f3-115">The byte offset between consecutive colors.</span></span> <span data-ttu-id="a27f3-116">Quando *stride* è zero, i colori sono strettamente compressi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="a27f3-116">When *stride* is zero, the colors are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="a27f3-117">*indicatore di misura*</span><span class="sxs-lookup"><span data-stu-id="a27f3-117">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="a27f3-118">Puntatore al primo componente del primo elemento di colore in una matrice di colori.</span><span class="sxs-lookup"><span data-stu-id="a27f3-118">A pointer to the first component of the first color element in a color array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a27f3-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a27f3-119">Return value</span></span>

<span data-ttu-id="a27f3-120">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a27f3-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a27f3-121">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a27f3-121">Error codes</span></span>

<span data-ttu-id="a27f3-122">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="a27f3-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a27f3-123">Nome</span><span class="sxs-lookup"><span data-stu-id="a27f3-123">Name</span></span>                                                                                              | <span data-ttu-id="a27f3-124">Significato</span><span class="sxs-lookup"><span data-stu-id="a27f3-124">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a27f3-125"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a27f3-125"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="a27f3-126">*size* non è 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="a27f3-126">*size* was not 3 or 4.</span></span><br/>            |
| <dl> <span data-ttu-id="a27f3-127"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a27f3-127"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="a27f3-128">il *tipo* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="a27f3-128">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="a27f3-129"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a27f3-129"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="a27f3-130">*stride* o *count* è negativo.</span><span class="sxs-lookup"><span data-stu-id="a27f3-130">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a27f3-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="a27f3-131">Remarks</span></span>

<span data-ttu-id="a27f3-132">La funzione **glColorPointer** specifica il percorso e il formato dati di una matrice di componenti colore da usare durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="a27f3-132">The **glColorPointer** function specifies the location and data format of an array of color components to use when rendering.</span></span> <span data-ttu-id="a27f3-133">Il parametro *stride* determina l'offset dei byte da un colore all'altro, abilitando la compressione degli attributi dei vertici in una singola matrice o archiviazione in matrici separate.</span><span class="sxs-lookup"><span data-stu-id="a27f3-133">The *stride* parameter determines the byte offset from one color to the next, enabling the packing of vertex attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="a27f3-134">In alcune implementazioni, l'archiviazione degli attributi dei vertici in una singola matrice può essere più efficiente rispetto all'utilizzo di matrici separate.</span><span class="sxs-lookup"><span data-stu-id="a27f3-134">In some implementations, storing vertex attributes in a single array can be more efficient than the use of separate arrays.</span></span>

<span data-ttu-id="a27f3-135">Abilitare la matrice di colori specificando la \_ costante della matrice di colori GL \_ con [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="a27f3-135">Enabled the color array by specifying the GL\_COLOR\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="a27f3-136">La chiamata a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md) usa la matrice di colori che è quindi abilitata.</span><span class="sxs-lookup"><span data-stu-id="a27f3-136">Calling [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md) uses the color array that is thus enabled.</span></span> <span data-ttu-id="a27f3-137">Per impostazione predefinita, la matrice di colori è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="a27f3-137">By default, the color array is disabled.</span></span> <span data-ttu-id="a27f3-138">Le chiamate **glColorPointer** non possono essere immesse negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="a27f3-138">The **glColorPointer** calls cannot by entered in display lists.</span></span>

<span data-ttu-id="a27f3-139">Quando si specifica una matrice di colori utilizzando **glColorPointer**, i valori di tutti i parametri della matrice di colori della funzione vengono salvati in uno stato sul lato client ed è possibile memorizzare nella cache gli elementi della matrice statica.</span><span class="sxs-lookup"><span data-stu-id="a27f3-139">When you specify a color array using **glColorPointer**, the values of all the function's color array parameters are saved in a client-side state, and you can cache static array elements.</span></span> <span data-ttu-id="a27f3-140">Poiché i parametri della matrice di colori sono in uno stato lato client, [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) non salvano o ripristinano i valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="a27f3-140">Because the color array parameters are in a client-side state, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) do not save or restore the parameters' values.</span></span>

<span data-ttu-id="a27f3-141">Sebbene l'impostazione della matrice di colori all'interno delle coppie [**glBegin**](glbegin.md) e [**glEnd**](glend.md) non generi un errore, i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="a27f3-141">Although specifying the color array within [**glBegin**](glbegin.md) and [**glend**](glend.md) pairs does not generate an error, the results are undefined.</span></span>

<span data-ttu-id="a27f3-142">Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glColorPointer** :</span><span class="sxs-lookup"><span data-stu-id="a27f3-142">The following functions retrieve information related to the **glColorPointer** function:</span></span>

<span data-ttu-id="a27f3-143">[**glIsEnabled**](glisenabled.md) con matrice di \_ colori GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="a27f3-143">[**glIsEnabled**](glisenabled.md) with argument GL\_COLOR\_ARRAY</span></span>

<span data-ttu-id="a27f3-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con le \_ dimensioni della \_ matrice di colori GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="a27f3-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_ARRAY\_SIZE</span></span>

<span data-ttu-id="a27f3-145">**glGet** con tipo di \_ matrice di colori GL argomento \_ \_</span><span class="sxs-lookup"><span data-stu-id="a27f3-145">**glGet** with argument GL\_COLOR\_ARRAY\_TYPE</span></span>

<span data-ttu-id="a27f3-146">**glGet** con argomento di \_ matrice dei colori GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="a27f3-146">**glGet** with argument GL\_COLOR\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="a27f3-147">**glGet** con argomento \_ conteggio delle \_ matrici di colori GL \_</span><span class="sxs-lookup"><span data-stu-id="a27f3-147">**glGet** with argument GL\_COLOR\_ARRAY\_COUNT</span></span>

<span data-ttu-id="a27f3-148">[**glGetPointerv**](glgetpointerv.md) con puntatore alla \_ matrice di colori GL argomento \_ \_</span><span class="sxs-lookup"><span data-stu-id="a27f3-148">[**glGetPointerv**](glgetpointerv.md) with argument GL\_COLOR\_ARRAY\_POINTER</span></span>

## <a name="requirements"></a><span data-ttu-id="a27f3-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a27f3-149">Requirements</span></span>



| <span data-ttu-id="a27f3-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="a27f3-150">Requirement</span></span> | <span data-ttu-id="a27f3-151">Valore</span><span class="sxs-lookup"><span data-stu-id="a27f3-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a27f3-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a27f3-152">Minimum supported client</span></span><br/> | <span data-ttu-id="a27f3-153">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a27f3-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a27f3-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a27f3-154">Minimum supported server</span></span><br/> | <span data-ttu-id="a27f3-155">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a27f3-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a27f3-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a27f3-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="a27f3-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a27f3-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a27f3-158">Libreria</span><span class="sxs-lookup"><span data-stu-id="a27f3-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="a27f3-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a27f3-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a27f3-160">DLL</span><span class="sxs-lookup"><span data-stu-id="a27f3-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a27f3-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a27f3-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a27f3-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a27f3-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a27f3-163">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="a27f3-163">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="a27f3-164">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a27f3-164">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a27f3-165">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="a27f3-165">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="a27f3-166">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="a27f3-166">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="a27f3-167">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="a27f3-167">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="a27f3-168">**Remo**</span><span class="sxs-lookup"><span data-stu-id="a27f3-168">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a27f3-169">**glGet**</span><span class="sxs-lookup"><span data-stu-id="a27f3-169">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="a27f3-170">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="a27f3-170">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="a27f3-171">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="a27f3-171">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="a27f3-172">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="a27f3-172">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="a27f3-173">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="a27f3-173">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="a27f3-174">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="a27f3-174">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="a27f3-175">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="a27f3-175">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="a27f3-176">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="a27f3-176">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="a27f3-177">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="a27f3-177">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="a27f3-178">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="a27f3-178">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 






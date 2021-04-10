---
title: funzione glDrawArrays (GL. h)
description: La funzione glDrawArrays specifica più primitive per il rendering.
ms.assetid: 6ebd467b-5a63-43e4-b3fd-242c704d7d13
keywords:
- funzione glDrawArrays OpenGL
topic_type:
- apiref
api_name:
- glDrawArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88b20cf3a3e3b2c96a8172f53f8126815efe16d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964352"
---
# <a name="gldrawarrays-function"></a><span data-ttu-id="2ed99-104">glDrawArrays (funzione)</span><span class="sxs-lookup"><span data-stu-id="2ed99-104">glDrawArrays function</span></span>

<span data-ttu-id="2ed99-105">La funzione **glDrawArrays** specifica più primitive per il rendering.</span><span class="sxs-lookup"><span data-stu-id="2ed99-105">The **glDrawArrays** function specifies multiple primitives to render.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ed99-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ed99-106">Syntax</span></span>


```C++
void WINAPI glDrawArrays(
   GLenum  mode,
   GLint   first,
   GLsizei count
);
```



## <a name="parameters"></a><span data-ttu-id="2ed99-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ed99-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ed99-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="2ed99-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="2ed99-109">Tipo di primitive di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="2ed99-109">The kind of primitives to render.</span></span> <span data-ttu-id="2ed99-110">Le costanti seguenti specificano tipi accettabili di primitive: \_ punti GL, \_ Strip linea GL \_ , \_ ciclo di riga GL, \_ \_ linee GL, striscia del \_ triangolo GL \_ , ventola del \_ triangolo GL \_ , \_ triangoli GL, GL \_ Quad \_ Strip, GL \_ quad e GL \_ Polygon.</span><span class="sxs-lookup"><span data-stu-id="2ed99-110">The following constants specify acceptable types of primitives: GL\_POINTS, GL\_LINE\_STRIP, GL\_LINE\_LOOP, GL\_LINES, GL\_TRIANGLE\_STRIP, GL\_TRIANGLE\_FAN, GL\_TRIANGLES, GL\_QUAD\_STRIP, GL\_QUADS, and GL\_POLYGON.</span></span>

</dd> <dt>

<span data-ttu-id="2ed99-111">*first*</span><span class="sxs-lookup"><span data-stu-id="2ed99-111">*first*</span></span> 
</dt> <dd>

<span data-ttu-id="2ed99-112">Indice iniziale nelle matrici abilitate.</span><span class="sxs-lookup"><span data-stu-id="2ed99-112">The starting index in the enabled arrays.</span></span>

</dd> <dt>

<span data-ttu-id="2ed99-113">*count*</span><span class="sxs-lookup"><span data-stu-id="2ed99-113">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="2ed99-114">Numero di indici di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="2ed99-114">The number of indexes to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ed99-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ed99-115">Return value</span></span>

<span data-ttu-id="2ed99-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2ed99-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2ed99-117">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="2ed99-117">Error codes</span></span>

<span data-ttu-id="2ed99-118">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="2ed99-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2ed99-119">Nome</span><span class="sxs-lookup"><span data-stu-id="2ed99-119">Name</span></span>                                                                                                  | <span data-ttu-id="2ed99-120">Significato</span><span class="sxs-lookup"><span data-stu-id="2ed99-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2ed99-121"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ed99-121"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="2ed99-122">*conteggio* negativo.</span><span class="sxs-lookup"><span data-stu-id="2ed99-122">*count* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="2ed99-123"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ed99-123"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="2ed99-124">la *modalità* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="2ed99-124">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="2ed99-125"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ed99-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2ed99-126">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2ed99-126">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2ed99-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ed99-127">Remarks</span></span>

<span data-ttu-id="2ed99-128">Con **glDrawArrays** è possibile specificare più primitive geometriche di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="2ed99-128">With **glDrawArrays**, you can specify multiple geometric primitives to render.</span></span> <span data-ttu-id="2ed99-129">Anziché chiamare funzioni OpenGL separate per passare ogni singolo vertice, normale o colore, è possibile specificare matrici separate di vertici, normali e colori per definire una sequenza di primitive (tutti dello stesso tipo) con una singola chiamata a **glDrawArrays**.</span><span class="sxs-lookup"><span data-stu-id="2ed99-129">Instead of calling separate OpenGL functions to pass each individual vertex, normal, or color, you can specify separate arrays of vertices, normals, and colors to define a sequence of primitives (all the same kind) with a single call to **glDrawArrays**.</span></span>

<span data-ttu-id="2ed99-130">Quando si chiama **glDrawArrays**, i *conteggi* degli elementi sequenziali di ogni matrice abilitata vengono usati per costruire una sequenza di primitive geometriche, a partire dal *primo* elemento.</span><span class="sxs-lookup"><span data-stu-id="2ed99-130">When you call **glDrawArrays**, *count* sequential elements from each enabled array are used to construct a sequence of geometric primitives, beginning with the *first* element.</span></span> <span data-ttu-id="2ed99-131">Il parametro *mode* specifica il tipo di primitiva da costruire e come usare gli elementi della matrice per costruire le primitive.</span><span class="sxs-lookup"><span data-stu-id="2ed99-131">The *mode* parameter specifies what kind of primitive to construct and how to use the array elements to construct the primitives.</span></span>

<span data-ttu-id="2ed99-132">Dopo la restituzione di **glDrawArrays** , i valori degli attributi Vertex modificati da **glDrawArrays** non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="2ed99-132">After **glDrawArrays** returns, the values of vertex attributes that are modified by **glDrawArrays** are undefined.</span></span> <span data-ttu-id="2ed99-133">Se, ad esempio, \_ \_ la matrice di colori GL è abilitata, il valore del colore corrente non è definito dopo che **glDrawArrays** restituisce.</span><span class="sxs-lookup"><span data-stu-id="2ed99-133">For example, if GL\_COLOR\_ARRAY is enabled, the value of the current color is undefined after **glDrawArrays** returns.</span></span> <span data-ttu-id="2ed99-134">Gli attributi non modificati da **glDrawArrays** rimangono definiti.</span><span class="sxs-lookup"><span data-stu-id="2ed99-134">Attributes not modified by **glDrawArrays** remain defined.</span></span> <span data-ttu-id="2ed99-135">Quando \_ \_ la matrice di vertici GL non è abilitata, non viene generata alcuna primitiva geometrica, ma gli attributi corrispondenti alle matrici abilitate vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="2ed99-135">When GL\_VERTEX\_ARRAY is not enabled, no geometric primitives are generated but the attributes corresponding to enabled arrays are modified.</span></span>

<span data-ttu-id="2ed99-136">È possibile includere **glDrawArrays** negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="2ed99-136">You can include **glDrawArrays** in display lists.</span></span> <span data-ttu-id="2ed99-137">Quando si include **glDrawArrays** in un elenco di visualizzazione, i dati di matrice necessari, determinati dai puntatori della matrice e da abilitati, vengono generati e immessi nell'elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="2ed99-137">When you include **glDrawArrays** in a display list, the necessary array data, determined by the array pointers and the enables, are generated and entered in the display list.</span></span> <span data-ttu-id="2ed99-138">I valori dei puntatori di matrice e di abilitazione vengono determinati durante la creazione degli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="2ed99-138">The values of array pointers and enables are determined during the creation of display lists.</span></span>

<span data-ttu-id="2ed99-139">È possibile leggere i dati della matrice statica in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="2ed99-139">You can read static array data at any time.</span></span> <span data-ttu-id="2ed99-140">Se gli elementi di una matrice statica vengono modificati e la matrice non viene specificata nuovamente, i risultati di qualsiasi chiamata successiva a **glDrawArrays** non saranno definiti.</span><span class="sxs-lookup"><span data-stu-id="2ed99-140">If any static array elements are modified and the array is not specified again, the results of any subsequent calls to **glDrawArrays** are undefined.</span></span>

<span data-ttu-id="2ed99-141">Sebbene non venga generato alcun errore quando si specifica una matrice più di una volta all'interno di [**glBegin**](glbegin.md) e delle coppie [**glEnd**](glend.md) , i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="2ed99-141">Although no error is generated when you specify an array more than once within [**glBegin**](glbegin.md) and [**glend**](glend.md) pairs, the results are undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ed99-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ed99-142">Requirements</span></span>



| <span data-ttu-id="2ed99-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ed99-143">Requirement</span></span> | <span data-ttu-id="2ed99-144">Valore</span><span class="sxs-lookup"><span data-stu-id="2ed99-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ed99-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ed99-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2ed99-146">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2ed99-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2ed99-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ed99-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2ed99-148">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2ed99-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2ed99-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ed99-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ed99-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ed99-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2ed99-151">Libreria</span><span class="sxs-lookup"><span data-stu-id="2ed99-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="2ed99-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ed99-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2ed99-153">DLL</span><span class="sxs-lookup"><span data-stu-id="2ed99-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ed99-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ed99-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ed99-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ed99-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ed99-156">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="2ed99-156">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="2ed99-157">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2ed99-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2ed99-158">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="2ed99-158">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="2ed99-159">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="2ed99-159">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="2ed99-160">**Remo**</span><span class="sxs-lookup"><span data-stu-id="2ed99-160">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2ed99-161">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="2ed99-161">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="2ed99-162">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="2ed99-162">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="2ed99-163">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="2ed99-163">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="2ed99-164">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="2ed99-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="2ed99-165">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="2ed99-165">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="2ed99-166">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="2ed99-166">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 






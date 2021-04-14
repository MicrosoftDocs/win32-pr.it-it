---
title: funzione glDrawElements (GL. h)
description: La funzione glDrawElements esegue il rendering di primitive da dati di matrice.
ms.assetid: fb433294-106e-48d5-ad49-4434934fe072
keywords:
- funzione glDrawElements OpenGL
topic_type:
- apiref
api_name:
- glDrawElements
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976e779235dc330467d610406156534b5e72841d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518100"
---
# <a name="gldrawelements-function"></a><span data-ttu-id="aacc6-104">glDrawElements (funzione)</span><span class="sxs-lookup"><span data-stu-id="aacc6-104">glDrawElements function</span></span>

<span data-ttu-id="aacc6-105">La funzione **glDrawElements** esegue il rendering di primitive da dati di matrice.</span><span class="sxs-lookup"><span data-stu-id="aacc6-105">The **glDrawElements** function renders primitives from array data.</span></span>

## <a name="syntax"></a><span data-ttu-id="aacc6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aacc6-106">Syntax</span></span>


```C++
void WINAPI glDrawElements(
         GLenum  mode,
         GLsizei count,
         GLenum  type,
   const GLvoid  *indices
);
```



## <a name="parameters"></a><span data-ttu-id="aacc6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="aacc6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aacc6-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="aacc6-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="aacc6-109">Tipo di primitive di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="aacc6-109">The kind of primitives to render.</span></span> <span data-ttu-id="aacc6-110">Può assumere uno dei valori simbolici seguenti: GL \_ Points, GL \_ line \_ Strip, GL \_ line \_ loop, GL \_ Lines, GL \_ triangolo \_ Strip, GL \_ Triangle \_ fan, GL \_ triangoli, GL \_ Quad \_ Strip, GL \_ Quads e GL \_ Polygon.</span><span class="sxs-lookup"><span data-stu-id="aacc6-110">It can assume one of the following symbolic values: GL\_POINTS, GL\_LINE\_STRIP, GL\_LINE\_LOOP, GL\_LINES, GL\_TRIANGLE\_STRIP, GL\_TRIANGLE\_FAN, GL\_TRIANGLES, GL\_QUAD\_STRIP, GL\_QUADS, and GL\_POLYGON.</span></span>

</dd> <dt>

<span data-ttu-id="aacc6-111">*count*</span><span class="sxs-lookup"><span data-stu-id="aacc6-111">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="aacc6-112">Numero di elementi di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="aacc6-112">The number of elements to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="aacc6-113">*type*</span><span class="sxs-lookup"><span data-stu-id="aacc6-113">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="aacc6-114">Tipo dei valori negli indici.</span><span class="sxs-lookup"><span data-stu-id="aacc6-114">The type of the values in indices.</span></span> <span data-ttu-id="aacc6-115">Deve essere uno dei byte senza segno GL, GL unsigned \_ \_ \_ \_ short o GL \_ unsigned \_ int.</span><span class="sxs-lookup"><span data-stu-id="aacc6-115">Must be one of GL\_UNSIGNED\_BYTE, GL\_UNSIGNED\_SHORT, or GL\_UNSIGNED\_INT.</span></span>

</dd> <dt>

<span data-ttu-id="aacc6-116">*indici*</span><span class="sxs-lookup"><span data-stu-id="aacc6-116">*indices*</span></span> 
</dt> <dd>

<span data-ttu-id="aacc6-117">Puntatore alla posizione in cui vengono archiviati gli indici.</span><span class="sxs-lookup"><span data-stu-id="aacc6-117">A pointer to the location where the indices are stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aacc6-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aacc6-118">Return value</span></span>

<span data-ttu-id="aacc6-119">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="aacc6-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="aacc6-120">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="aacc6-120">Error codes</span></span>

<span data-ttu-id="aacc6-121">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="aacc6-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="aacc6-122">Nome</span><span class="sxs-lookup"><span data-stu-id="aacc6-122">Name</span></span>                                                                                                  | <span data-ttu-id="aacc6-123">Significato</span><span class="sxs-lookup"><span data-stu-id="aacc6-123">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aacc6-124"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="aacc6-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="aacc6-125">la *modalità* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="aacc6-125">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="aacc6-126"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="aacc6-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="aacc6-127">*count* è un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="aacc6-127">*count* was a negative value.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="aacc6-128"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="aacc6-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="aacc6-129">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="aacc6-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="aacc6-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="aacc6-130">Remarks</span></span>

<span data-ttu-id="aacc6-131">La funzione **glDrawElements** consente di specificare più primitive geometriche con pochissime chiamate di funzione.</span><span class="sxs-lookup"><span data-stu-id="aacc6-131">The **glDrawElements** function enables you to specify multiple geometric primitives with very few function calls.</span></span> <span data-ttu-id="aacc6-132">Anziché chiamare una funzione OpenGL per passare ogni singolo vertice, normale o colore, è possibile specificare in anticipo matrici separate di vertici, normali e colori e usarle per definire una sequenza di primitive (tutti dello stesso tipo) con una singola chiamata a **glDrawElements**.</span><span class="sxs-lookup"><span data-stu-id="aacc6-132">Instead of calling an OpenGL function to pass each individual vertex, normal, or color, you can specify separate arrays of vertices, normals, and colors beforehand and use them to define a sequence of primitives (all of the same type) with a single call to **glDrawElements**.</span></span>

<span data-ttu-id="aacc6-133">Quando si chiama la funzione **glDrawElements** , viene usato il *conteggio* degli elementi sequenziali degli *indici* per costruire una sequenza di primitive geometriche.</span><span class="sxs-lookup"><span data-stu-id="aacc6-133">When you call the **glDrawElements** function, it uses *count* sequential elements from *indices* to construct a sequence of geometric primitives.</span></span> <span data-ttu-id="aacc6-134">Il parametro *mode* specifica il tipo di primitive da costruire e la modalità di utilizzo degli elementi di matrice per costruire tali primitive.</span><span class="sxs-lookup"><span data-stu-id="aacc6-134">The *mode* parameter specifies what kind of primitives are constructed, and how the array elements are used to construct these primitives.</span></span> <span data-ttu-id="aacc6-135">Se \_ \_ la matrice di vertici GL non è abilitata, non viene generata alcuna primitiva geometrica.</span><span class="sxs-lookup"><span data-stu-id="aacc6-135">If GL\_VERTEX\_ARRAY is not enabled, no geometric primitives are generated.</span></span>

<span data-ttu-id="aacc6-136">Gli attributi Vertex modificati da **glDrawElements** hanno un valore non specificato dopo la restituzione di **glDrawElements** .</span><span class="sxs-lookup"><span data-stu-id="aacc6-136">Vertex attributes that are modified by **glDrawElements** have an unspecified value after **glDrawElements** returns.</span></span> <span data-ttu-id="aacc6-137">Se, ad esempio, \_ \_ la matrice di colori GL è abilitata, il valore del colore corrente non è definito dopo l'esecuzione di **glDrawElements** .</span><span class="sxs-lookup"><span data-stu-id="aacc6-137">For example, if GL\_COLOR\_ARRAY is enabled, the value of the current color is undefined after **glDrawElements** executes.</span></span> <span data-ttu-id="aacc6-138">Gli attributi che non vengono modificati rimangono invariati.</span><span class="sxs-lookup"><span data-stu-id="aacc6-138">Attributes that aren't modified remain unchanged.</span></span>

<span data-ttu-id="aacc6-139">È possibile includere la funzione **glDrawElements** negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="aacc6-139">You can include the **glDrawElements** function in display lists.</span></span> <span data-ttu-id="aacc6-140">Quando **glDrawElements** è incluso in un elenco di visualizzazione, vengono immessi anche i dati di matrice necessari, determinati dai puntatori alla matrice e abilitati, nell'elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="aacc6-140">When **glDrawElements** is included in a display list, the necessary array data (determined by the array pointers and enables) is also entered into the display list.</span></span> <span data-ttu-id="aacc6-141">Poiché i puntatori di matrice e le abilitazioni sono variabili di stato sul lato client, i relativi valori influiscono sugli elenchi di visualizzazione quando vengono creati gli elenchi, non quando vengono eseguiti gli elenchi.</span><span class="sxs-lookup"><span data-stu-id="aacc6-141">Because the array pointers and enables are client-side state variables, their values affect display lists when the lists are created, not when the lists are executed.</span></span>

> [!Note]  
> <span data-ttu-id="aacc6-142">La funzione **glDrawElements** è disponibile solo in OpenGL versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="aacc6-142">The **glDrawElements** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aacc6-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aacc6-143">Requirements</span></span>



| <span data-ttu-id="aacc6-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="aacc6-144">Requirement</span></span> | <span data-ttu-id="aacc6-145">Valore</span><span class="sxs-lookup"><span data-stu-id="aacc6-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aacc6-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aacc6-146">Minimum supported client</span></span><br/> | <span data-ttu-id="aacc6-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aacc6-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="aacc6-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aacc6-148">Minimum supported server</span></span><br/> | <span data-ttu-id="aacc6-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aacc6-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aacc6-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aacc6-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="aacc6-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="aacc6-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="aacc6-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="aacc6-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="aacc6-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aacc6-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="aacc6-154">DLL</span><span class="sxs-lookup"><span data-stu-id="aacc6-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aacc6-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aacc6-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aacc6-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aacc6-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aacc6-157">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="aacc6-157">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="aacc6-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="aacc6-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="aacc6-159">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="aacc6-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="aacc6-160">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="aacc6-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="aacc6-161">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="aacc6-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="aacc6-162">**Remo**</span><span class="sxs-lookup"><span data-stu-id="aacc6-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="aacc6-163">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="aacc6-163">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="aacc6-164">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="aacc6-164">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="aacc6-165">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="aacc6-165">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="aacc6-166">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="aacc6-166">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="aacc6-167">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="aacc6-167">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 






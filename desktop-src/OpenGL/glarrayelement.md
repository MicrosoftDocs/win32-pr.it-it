---
title: funzione glArrayElement (GL. h)
description: La funzione glArrayElement specifica gli elementi della matrice usati per eseguire il rendering di un vertice.
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
keywords:
- funzione glArrayElement OpenGL
topic_type:
- apiref
api_name:
- glArrayElement
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a20aff9fcaa5bf922bc9447f7b7022a8cd1a9c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301804"
---
# <a name="glarrayelement-function"></a><span data-ttu-id="98518-104">glArrayElement (funzione)</span><span class="sxs-lookup"><span data-stu-id="98518-104">glArrayElement function</span></span>

<span data-ttu-id="98518-105">La funzione **glArrayElement** specifica gli elementi della matrice usati per eseguire il rendering di un vertice.</span><span class="sxs-lookup"><span data-stu-id="98518-105">The **glArrayElement** function specifies the array elements used to render a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="98518-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98518-106">Syntax</span></span>


```C++
void WINAPI glArrayElement(
   GLint index
);
```



## <a name="parameters"></a><span data-ttu-id="98518-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="98518-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98518-108">*index*</span><span class="sxs-lookup"><span data-stu-id="98518-108">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="98518-109">Indice nelle matrici abilitate.</span><span class="sxs-lookup"><span data-stu-id="98518-109">An index in the enabled arrays.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98518-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98518-110">Return value</span></span>

<span data-ttu-id="98518-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="98518-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98518-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="98518-112">Remarks</span></span>

<span data-ttu-id="98518-113">Usare la funzione **glArrayElement** all'interno delle coppie [**glBegin**](glbegin.md) e [**glEnd**](glend.md) per specificare i dati dei vertici e degli attributi per le primitive di punti, linee e poligoni.</span><span class="sxs-lookup"><span data-stu-id="98518-113">Use the **glArrayElement** function within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs to specify vertex and attribute data for point, line, and polygon primitives.</span></span> <span data-ttu-id="98518-114">La funzione **glArrayElement** specifica i dati per un singolo vertice usando i dati dei vertici e degli attributi posizionati in corrispondenza dell' *Indice* delle matrici di vertici abilitate.</span><span class="sxs-lookup"><span data-stu-id="98518-114">The **glArrayElement** function specifies the data for a single vertex using vertex and attribute data located at the *index* of the enabled vertex arrays.</span></span>

<span data-ttu-id="98518-115">È possibile utilizzare **glArrayElement** per costruire primitive indicizzando i dati dei vertici, anziché tramite la trasmissione di matrici di dati nell'ordine da primo a ultimo.</span><span class="sxs-lookup"><span data-stu-id="98518-115">You can use **glArrayElement** to construct primitives by indexing vertex data, rather than by streaming through arrays of data in first-to-last order.</span></span> <span data-ttu-id="98518-116">Poiché **glArrayElement** specifica solo un singolo vertice, è possibile specificare in modo esplicito gli attributi per le singole primitive.</span><span class="sxs-lookup"><span data-stu-id="98518-116">Because **glArrayElement** specifies a single vertex only, you can explicitly specify attributes for individual primitives.</span></span> <span data-ttu-id="98518-117">Ad esempio, è possibile impostare un singolo normale per ogni singolo triangolo.</span><span class="sxs-lookup"><span data-stu-id="98518-117">For example, you can set a single normal for each individual triangle.</span></span>

<span data-ttu-id="98518-118">Quando si includono chiamate a **glArrayElement** negli elenchi di visualizzazione, i dati di matrice necessari, determinati dai puntatori di matrice e abilitano i valori, vengono immessi anche nell'elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="98518-118">When you include calls to **glArrayElement** in display lists, the necessary array data, determined by the array pointers and enable values, is entered in the display list also.</span></span> <span data-ttu-id="98518-119">Il puntatore di matrice e i valori di abilitazione vengono determinati quando vengono creati gli elenchi di visualizzazione, non quando vengono eseguiti gli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="98518-119">Array pointer and enable values are determined when display lists are created, not when display lists are executed.</span></span>

<span data-ttu-id="98518-120">È possibile leggere e memorizzare nella cache dati di matrici statici in qualsiasi momento con **glArrayElement**.</span><span class="sxs-lookup"><span data-stu-id="98518-120">You can read and cache static array data at any time with **glArrayElement**.</span></span> <span data-ttu-id="98518-121">Quando si modificano gli elementi di una matrice statica senza specificare nuovamente la matrice, i risultati di tutte le chiamate successive a **glArrayElement** non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="98518-121">When you modify the elements of a static array without specifying the array again, the results of any subsequent calls to **glArrayElement** are undefined.</span></span>

<span data-ttu-id="98518-122">Quando si chiama **glArrayElement** senza prima chiamare **glEnableClientState**( \_ matrice di vertici GL \_ ), non viene eseguito alcun disegno, ma gli attributi corrispondenti alle matrici abilitate vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="98518-122">When you call **glArrayElement** without first calling **glEnableClientState**(GL\_VERTEX\_ARRAY), no drawing occurs, but the attributes corresponding to enabled arrays are modified.</span></span> <span data-ttu-id="98518-123">Sebbene non venga generato alcun errore quando si specifica una matrice all'interno di **glBegin** e di coppie **glEnd** , i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="98518-123">Although no error is generated when you specify an array within **glBegin** and **glEnd** pairs, the results are undefined.</span></span>

> [!Note]  
> <span data-ttu-id="98518-124">La funzione **glArrayElement** è disponibile solo in OpenGL versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="98518-124">The **glArrayElement** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="98518-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98518-125">Requirements</span></span>



| <span data-ttu-id="98518-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="98518-126">Requirement</span></span> | <span data-ttu-id="98518-127">Valore</span><span class="sxs-lookup"><span data-stu-id="98518-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98518-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98518-128">Minimum supported client</span></span><br/> | <span data-ttu-id="98518-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98518-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="98518-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98518-130">Minimum supported server</span></span><br/> | <span data-ttu-id="98518-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="98518-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="98518-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98518-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="98518-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="98518-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="98518-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="98518-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="98518-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98518-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="98518-136">DLL</span><span class="sxs-lookup"><span data-stu-id="98518-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98518-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98518-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98518-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98518-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98518-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="98518-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="98518-140">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="98518-140">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="98518-141">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="98518-141">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="98518-142">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="98518-142">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="98518-143">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="98518-143">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="98518-144">**Remo**</span><span class="sxs-lookup"><span data-stu-id="98518-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="98518-145">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="98518-145">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="98518-146">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="98518-146">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="98518-147">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="98518-147">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="98518-148">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="98518-148">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="98518-149">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="98518-149">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="98518-150">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="98518-150">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 






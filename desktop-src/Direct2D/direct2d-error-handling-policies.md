---
title: Criteri di gestione degli errori Direct2D
description: 'In questo argomento vengono descritti i criteri di gestione degli errori Direct2D. Include le sezioni seguenti:'
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D, gestione degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc930e7ee9e5b73b5f676103f45ffe25e4d4e61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963367"
---
# <a name="direct2d-error-handling-policies"></a><span data-ttu-id="9e757-105">Criteri di gestione degli errori Direct2D</span><span class="sxs-lookup"><span data-stu-id="9e757-105">Direct2D Error Handling Policies</span></span>

<span data-ttu-id="9e757-106">In questo argomento vengono descritti i criteri di gestione degli errori Direct2D.</span><span class="sxs-lookup"><span data-stu-id="9e757-106">This topic describes the Direct2D error handling policies.</span></span> <span data-ttu-id="9e757-107">Include le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e757-107">It contains the following sections.</span></span>

-   [<span data-ttu-id="9e757-108">Utilizzo di HRESULT</span><span class="sxs-lookup"><span data-stu-id="9e757-108">Use of HRESULT</span></span>](#use-of-hresult)
-   [<span data-ttu-id="9e757-109">Valore restituito delle funzioni in batch</span><span class="sxs-lookup"><span data-stu-id="9e757-109">Return Value of Batched Functions</span></span>](#return-value-of-batched-functions)
-   [<span data-ttu-id="9e757-110">Input non valido</span><span class="sxs-lookup"><span data-stu-id="9e757-110">Invalid Input</span></span>](#invalid-input)
    -   [<span data-ttu-id="9e757-111">Puntatore di output</span><span class="sxs-lookup"><span data-stu-id="9e757-111">Output Pointer</span></span>](#output-pointer)
    -   [<span data-ttu-id="9e757-112">Parametro obbligatorio</span><span class="sxs-lookup"><span data-stu-id="9e757-112">Required Parameter</span></span>](#required-parameter)
-   [<span data-ttu-id="9e757-113">RECTs di input NaN e ordinato male</span><span class="sxs-lookup"><span data-stu-id="9e757-113">NaN and Poorly Ordered Input RECTs</span></span>](#nan-and-poorly-ordered-input-rects)
    -   [<span data-ttu-id="9e757-114">NaN come input</span><span class="sxs-lookup"><span data-stu-id="9e757-114">NaN as Input</span></span>](#nan-as-input)
    -   [<span data-ttu-id="9e757-115">RETTANGOLi di input ordinati in modo non corretto</span><span class="sxs-lookup"><span data-stu-id="9e757-115">Poorly Ordered Input RECTs</span></span>](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a><span data-ttu-id="9e757-116">Utilizzo di HRESULT</span><span class="sxs-lookup"><span data-stu-id="9e757-116">Use of HRESULT</span></span>

<span data-ttu-id="9e757-117">Se una funzione non è in batch e può avere un errore di run-time, deve restituire **HRESULT** per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="9e757-117">If a function is not batched and can have a run-time failure, it should return **HRESULT** to indicate a failure.</span></span> <span data-ttu-id="9e757-118">Un errore in fase di esecuzione è un errore che non può essere evitato in fase di progettazione, ad esempio memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="9e757-118">A run-time failure is any failure that cannot be avoided at design time, such as out of memory.</span></span>

## <a name="return-value-of-batched-functions"></a><span data-ttu-id="9e757-119">Valore restituito delle funzioni in batch</span><span class="sxs-lookup"><span data-stu-id="9e757-119">Return Value of Batched Functions</span></span>

<span data-ttu-id="9e757-120">Le funzioni in batch in Direct2D sono le funzioni elaborate come una singola unità quando viene chiamato [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) .</span><span class="sxs-lookup"><span data-stu-id="9e757-120">Batched functions in Direct2D are the functions that are processed as a single unit when [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) is called.</span></span> <span data-ttu-id="9e757-121">Sono i comandi di disegno tra [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e **EndDraw** o i comandi su [**GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span><span class="sxs-lookup"><span data-stu-id="9e757-121">They are the drawing commands between [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and **EndDraw** or commands on [**GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span></span> <span data-ttu-id="9e757-122">Per queste funzioni, gli errori vengono segnalati nel momento in cui il batch viene completato.</span><span class="sxs-lookup"><span data-stu-id="9e757-122">For these functions, errors are reported at the time the batch is completed.</span></span> <span data-ttu-id="9e757-123">L'errore viene restituito dopo **EndDraw** per il disegno dei comandi e dopo la **chiusura** di **GeometrySink**.</span><span class="sxs-lookup"><span data-stu-id="9e757-123">The error is returned after **EndDraw** for drawing commands, and after **Close** for **GeometrySink**.</span></span>

<span data-ttu-id="9e757-124">RenderTargets arresta il disegno se è stato impostato uno stato di errore, ma un'applicazione può chiamare [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) per reimpostare lo stato di errore e riprendere il disegno.</span><span class="sxs-lookup"><span data-stu-id="9e757-124">RenderTargets stop drawing if an error state is set, but an application can call [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) to reset the error state and resume drawing.</span></span>

<span data-ttu-id="9e757-125">Le funzioni **Get** e **set** non restituiscono alcun valore.</span><span class="sxs-lookup"><span data-stu-id="9e757-125">**Get** and **Set** functions have no return value.</span></span> <span data-ttu-id="9e757-126">Tuttavia, se una funzione **set** ha un input non valido, il livello di debug genera un messaggio.</span><span class="sxs-lookup"><span data-stu-id="9e757-126">However, if a **Set** function has an invalid input, the debug layer generates a message.</span></span> <span data-ttu-id="9e757-127">In questo caso non viene impostato alcuno stato di errore e la funzione **set** non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="9e757-127">In this case, no error state is set and the **Set** function does nothing.</span></span>

## <a name="invalid-input"></a><span data-ttu-id="9e757-128">Input non valido</span><span class="sxs-lookup"><span data-stu-id="9e757-128">Invalid Input</span></span>

<span data-ttu-id="9e757-129">Direct2D consente di dereferenziare i puntatori di output e i parametri obbligatori che generano violazioni di accesso quando i puntatori non sono validi o sono **null**.</span><span class="sxs-lookup"><span data-stu-id="9e757-129">Direct2D dereferences output pointers and required parameters which result in access violations when the pointers are invalid or **NULL**.</span></span>

### <a name="output-pointer"></a><span data-ttu-id="9e757-130">Puntatore di output</span><span class="sxs-lookup"><span data-stu-id="9e757-130">Output Pointer</span></span>

<span data-ttu-id="9e757-131">Direct2D dereferenzia un puntatore di output e lo assegna a **null** immediatamente dopo l'immissione della funzione.</span><span class="sxs-lookup"><span data-stu-id="9e757-131">Direct2D dereferences an output pointer and assigns it to **NULL** immediately upon entering the function.</span></span> <span data-ttu-id="9e757-132">Ciò provoca una violazione di accesso se un chiamante passa **null** come puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="9e757-132">This causes an access violation if a caller passes in **NULL** as the pointer to the return value.</span></span> <span data-ttu-id="9e757-133">Questo criterio si applica anche a matrici di puntatori.</span><span class="sxs-lookup"><span data-stu-id="9e757-133">This policy also applies to arrays of pointers.</span></span> <span data-ttu-id="9e757-134">Per altri parametri di output, ad esempio uno struct, la dereferenziazione viene eseguita in un secondo momento e comporta anche una violazione di accesso.</span><span class="sxs-lookup"><span data-stu-id="9e757-134">For other output parameters, such as a struct, the dereference happens later and also results in an access violation.</span></span> <span data-ttu-id="9e757-135">Tuttavia, esistono alcuni metodi che dispongono di puntatori di output facoltativi (ovvero [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) che non provocheranno una violazione di accesso.</span><span class="sxs-lookup"><span data-stu-id="9e757-135">However, there are some methods that have optional output pointers (that is, [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) that will not cause an access violation.</span></span>

### <a name="required-parameter"></a><span data-ttu-id="9e757-136">Parametro obbligatorio</span><span class="sxs-lookup"><span data-stu-id="9e757-136">Required Parameter</span></span>

<span data-ttu-id="9e757-137">Se **null** viene passato a una funzione che richiede un valore valido, la funzione dereferenzia il puntatore errato in anticipo, causando una violazione di accesso.</span><span class="sxs-lookup"><span data-stu-id="9e757-137">If **NULL** is passed to any function requiring a valid value, the function dereferences the bad pointer early resulting in an access violation.</span></span> <span data-ttu-id="9e757-138">Per i parametri di input facoltativi, **null** è un valore valido che restituisce un valore predefinito ragionevole.</span><span class="sxs-lookup"><span data-stu-id="9e757-138">For optional input parameters, **NULL** is a valid value that results in some reasonable default.</span></span>

## <a name="nan-and-poorly-ordered-input-rects"></a><span data-ttu-id="9e757-139">RECTs di input NaN e ordinato male</span><span class="sxs-lookup"><span data-stu-id="9e757-139">NaN and Poorly Ordered Input RECTs</span></span>

<span data-ttu-id="9e757-140">In Direct2D, NaN è considerato un input valido e i RETTANGOLi di input non ordinati sono ordinati.</span><span class="sxs-lookup"><span data-stu-id="9e757-140">In Direct2D, NaN is considered a valid input and poorly ordered input RECTs are sorted.</span></span>

### <a name="nan-as-input"></a><span data-ttu-id="9e757-141">NaN come input</span><span class="sxs-lookup"><span data-stu-id="9e757-141">NaN as Input</span></span>

<span data-ttu-id="9e757-142">NaN è considerato un input valido, sebbene in genere il risultato della primitiva che contiene il valore NaN non viene disegnato.</span><span class="sxs-lookup"><span data-stu-id="9e757-142">NaN is considered a valid input, though it typically results in the primitive that contains the NaN not drawing.</span></span> <span data-ttu-id="9e757-143">L'API Direct2D non fornisce il filtro esplicito di NaN per convalidare l'input.</span><span class="sxs-lookup"><span data-stu-id="9e757-143">The Direct2D API does not provide explicit filtering of NaN to validate input.</span></span>

### <a name="poorly-ordered-input-rects"></a><span data-ttu-id="9e757-144">RETTANGOLi di input ordinati in modo non corretto</span><span class="sxs-lookup"><span data-stu-id="9e757-144">Poorly Ordered Input RECTs</span></span>

<span data-ttu-id="9e757-145">I RETTANGOLi di input poco ordinati vengono ordinati in modo che gli angoli superiore, sinistro e inferiore siano specificati correttamente.</span><span class="sxs-lookup"><span data-stu-id="9e757-145">Poorly ordered input RECTs are sorted so that the top, left and bottom, right corners are correctly specified.</span></span> <span data-ttu-id="9e757-146">Per l'output, i rettangoli vuoti hanno un aspetto simile al seguente: {Infinity, Infinity, FloatMax, FloatMax}.</span><span class="sxs-lookup"><span data-stu-id="9e757-146">For output, empty rectangles look like this: {Infinity, Infinity, FloatMax, FloatMax}.</span></span>

 

 
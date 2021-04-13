---
title: funzione glCallList (GL. h)
description: La funzione glCallList esegue un elenco di visualizzazione.
ms.assetid: 9373d32e-b11e-4a80-8713-da2c1d8d9368
keywords:
- funzione glCallList OpenGL
topic_type:
- apiref
api_name:
- glCallList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d356adc5d16ceb0ea10e3834d8dbb98abed2b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120071"
---
# <a name="glcalllist-function"></a><span data-ttu-id="3d9fe-104">glCallList (funzione)</span><span class="sxs-lookup"><span data-stu-id="3d9fe-104">glCallList function</span></span>

<span data-ttu-id="3d9fe-105">La funzione **glCallList** esegue un elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-105">The **glCallList** function executes a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d9fe-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d9fe-106">Syntax</span></span>


```C++
void WINAPI glCallList(
   GLuint list
);
```



## <a name="parameters"></a><span data-ttu-id="3d9fe-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d9fe-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d9fe-108">*list*</span><span class="sxs-lookup"><span data-stu-id="3d9fe-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="3d9fe-109">Nome intero dell'elenco di visualizzazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-109">The integer name of the display list to be executed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d9fe-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d9fe-110">Return value</span></span>

<span data-ttu-id="3d9fe-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d9fe-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d9fe-112">Remarks</span></span>

<span data-ttu-id="3d9fe-113">Quando si richiama la funzione **glCallList** , viene avviata l'esecuzione dell'elenco di visualizzazione denominato.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-113">Invoking the **glCallList** function begins execution of the named display list.</span></span> <span data-ttu-id="3d9fe-114">Le funzioni salvate nell'elenco di visualizzazione vengono eseguite in ordine, come se fossero state chiamate senza usare un elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-114">The functions saved in the display list are executed in order, just as if you called them without using a display list.</span></span> <span data-ttu-id="3d9fe-115">Se l' *elenco* non è stato definito come elenco di visualizzazione, **glCallList** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-115">If *list* has not been defined as a display list, **glCallList** is ignored.</span></span>

<span data-ttu-id="3d9fe-116">La funzione **glCallList** può essere visualizzata all'interno di un elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-116">The **glCallList** function can appear inside a display list.</span></span> <span data-ttu-id="3d9fe-117">Per evitare la possibilità di una ricorsione infinita risultante da elenchi di visualizzazione che si richiamano, viene applicato un limite al livello di annidamento degli elenchi di visualizzazione durante l'esecuzione dell'elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-117">To avoid the possibility of infinite recursion resulting from display lists calling one another, a limit is placed on the nesting level of display lists during display-list execution.</span></span> <span data-ttu-id="3d9fe-118">Questo limite è almeno 64, ma dipende dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-118">This limit is at least 64, however, it depends on the implementation.</span></span>

<span data-ttu-id="3d9fe-119">Lo stato OpenGL non viene salvato e ripristinato tramite una chiamata a **glCallList**.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-119">The OpenGL state is not saved and restored across a call to **glCallList**.</span></span> <span data-ttu-id="3d9fe-120">Pertanto, le modifiche apportate allo stato OpenGL durante l'esecuzione di un elenco di visualizzazione rimangono al termine dell'esecuzione dell'elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-120">Thus, changes made to the OpenGL state during the execution of a display list remain after execution of the display list is completed.</span></span> <span data-ttu-id="3d9fe-121">Per mantenere lo stato OpenGL tra le chiamate a **glCallList** , usare [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)e [**glPopMatrix**](glpopmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="3d9fe-121">To preserve the OpenGL state across **glCallList** calls, use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md), and [**glPopMatrix**](glpopmatrix.md).</span></span>

<span data-ttu-id="3d9fe-122">È possibile eseguire gli elenchi di visualizzazione tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md), purché nell'elenco di visualizzazione siano incluse solo le funzioni consentite in questo intervallo.</span><span class="sxs-lookup"><span data-stu-id="3d9fe-122">You can execute display lists between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md), as long as the display list includes only functions that are allowed in this interval.</span></span>

<span data-ttu-id="3d9fe-123">Le funzioni seguenti consentono di recuperare informazioni correlate a **glCallList**:</span><span class="sxs-lookup"><span data-stu-id="3d9fe-123">The following functions retrieve information related to **glCallList**:</span></span>

<span data-ttu-id="3d9fe-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con elenco di \_ \_ \_ nidificazione elenco massimo argomenti</span><span class="sxs-lookup"><span data-stu-id="3d9fe-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_LIST\_NESTING</span></span>

[<span data-ttu-id="3d9fe-125">**Pagina di**</span><span class="sxs-lookup"><span data-stu-id="3d9fe-125">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="3d9fe-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d9fe-126">Requirements</span></span>



| <span data-ttu-id="3d9fe-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d9fe-127">Requirement</span></span> | <span data-ttu-id="3d9fe-128">Valore</span><span class="sxs-lookup"><span data-stu-id="3d9fe-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d9fe-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d9fe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3d9fe-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3d9fe-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3d9fe-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d9fe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3d9fe-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3d9fe-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3d9fe-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d9fe-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d9fe-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d9fe-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3d9fe-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="3d9fe-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="3d9fe-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d9fe-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3d9fe-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3d9fe-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d9fe-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d9fe-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d9fe-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d9fe-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d9fe-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3d9fe-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3d9fe-141">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="3d9fe-141">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="3d9fe-142">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="3d9fe-142">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="3d9fe-143">**Remo**</span><span class="sxs-lookup"><span data-stu-id="3d9fe-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3d9fe-144">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="3d9fe-144">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="3d9fe-145">**glGet**</span><span class="sxs-lookup"><span data-stu-id="3d9fe-145">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="3d9fe-146">**Pagina di**</span><span class="sxs-lookup"><span data-stu-id="3d9fe-146">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="3d9fe-147">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="3d9fe-147">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="3d9fe-148">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="3d9fe-148">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="3d9fe-149">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="3d9fe-149">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="3d9fe-150">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="3d9fe-150">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="3d9fe-151">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="3d9fe-151">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 






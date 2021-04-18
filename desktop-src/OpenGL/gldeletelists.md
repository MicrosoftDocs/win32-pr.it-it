---
title: funzione glDeleteLists (GL. h)
description: La funzione glDeleteLists Elimina un gruppo contiguo di elenchi di visualizzazione.
ms.assetid: 979ab352-99db-4822-922c-a1813b9fcfce
keywords:
- funzione glDeleteLists OpenGL
topic_type:
- apiref
api_name:
- glDeleteLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11ae41273cba5bd050a62ea330cef9da0647769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301798"
---
# <a name="gldeletelists-function"></a><span data-ttu-id="f76b7-104">glDeleteLists (funzione)</span><span class="sxs-lookup"><span data-stu-id="f76b7-104">glDeleteLists function</span></span>

<span data-ttu-id="f76b7-105">La funzione **glDeleteLists** Elimina un gruppo contiguo di elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f76b7-105">The **glDeleteLists** function deletes a contiguous group of display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="f76b7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f76b7-106">Syntax</span></span>


```C++
void WINAPI glDeleteLists(
   GLuint  list,
   GLsizei range
);
```



## <a name="parameters"></a><span data-ttu-id="f76b7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f76b7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f76b7-108">*list*</span><span class="sxs-lookup"><span data-stu-id="f76b7-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="f76b7-109">Nome intero del primo elenco visualizzato da eliminare.</span><span class="sxs-lookup"><span data-stu-id="f76b7-109">The integer name of the first display list to delete.</span></span>

</dd> <dt>

<span data-ttu-id="f76b7-110">*range*</span><span class="sxs-lookup"><span data-stu-id="f76b7-110">*range*</span></span> 
</dt> <dd>

<span data-ttu-id="f76b7-111">Numero di elenchi di visualizzazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="f76b7-111">The number of display lists to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f76b7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f76b7-112">Return value</span></span>

<span data-ttu-id="f76b7-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f76b7-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f76b7-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f76b7-114">Error codes</span></span>

<span data-ttu-id="f76b7-115">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="f76b7-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f76b7-116">Nome</span><span class="sxs-lookup"><span data-stu-id="f76b7-116">Name</span></span>                                                                                                  | <span data-ttu-id="f76b7-117">Significato</span><span class="sxs-lookup"><span data-stu-id="f76b7-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f76b7-118"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f76b7-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="f76b7-119">l' *intervallo* è negativo.</span><span class="sxs-lookup"><span data-stu-id="f76b7-119">*range* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="f76b7-120"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f76b7-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f76b7-121">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f76b7-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f76b7-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="f76b7-122">Remarks</span></span>

<span data-ttu-id="f76b7-123">La funzione **glDeleteLists** causa l'eliminazione di un gruppo contiguo di elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f76b7-123">The **glDeleteLists** function causes a contiguous group of display lists to be deleted.</span></span> <span data-ttu-id="f76b7-124">Il parametro *List* è il nome del primo elenco visualizzato da eliminare e *Range* indica il numero di elenchi di visualizzazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="f76b7-124">The *list* parameter is the name of the first display list to be deleted, and *range* is the number of display lists to delete.</span></span> <span data-ttu-id="f76b7-125">Tutti gli elenchi di visualizzazione *d* con *List*  =  *d*  =  *List*  +  *Range* -1 vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="f76b7-125">All display lists *d* with *list* = *d* = *list* + *range* - 1 are deleted.</span></span>

<span data-ttu-id="f76b7-126">Tutte le posizioni di archiviazione allocate agli elenchi di visualizzazione specificati vengono liberate e i nomi sono disponibili per essere riutilizzati in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="f76b7-126">All storage locations allocated to the specified display lists are freed, and the names are available for reuse at a later time.</span></span> <span data-ttu-id="f76b7-127">I nomi compresi nell'intervallo che non dispongono di un elenco di visualizzazione associato vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="f76b7-127">Names within the range that do not have an associated display list are ignored.</span></span> <span data-ttu-id="f76b7-128">Se *Range* è zero, non viene eseguita alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="f76b7-128">If *range* is zero, nothing happens.</span></span>

## <a name="requirements"></a><span data-ttu-id="f76b7-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f76b7-129">Requirements</span></span>



| <span data-ttu-id="f76b7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f76b7-130">Requirement</span></span> | <span data-ttu-id="f76b7-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f76b7-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f76b7-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f76b7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f76b7-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f76b7-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f76b7-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f76b7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f76b7-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f76b7-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f76b7-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f76b7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f76b7-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f76b7-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f76b7-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="f76b7-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="f76b7-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f76b7-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f76b7-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f76b7-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f76b7-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f76b7-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f76b7-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f76b7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f76b7-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f76b7-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f76b7-144">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="f76b7-144">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="f76b7-145">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="f76b7-145">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="f76b7-146">**Remo**</span><span class="sxs-lookup"><span data-stu-id="f76b7-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f76b7-147">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="f76b7-147">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="f76b7-148">**Pagina di**</span><span class="sxs-lookup"><span data-stu-id="f76b7-148">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="f76b7-149">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="f76b7-149">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 






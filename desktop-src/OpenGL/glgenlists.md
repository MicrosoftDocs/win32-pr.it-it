---
title: funzione glGenLists (GL. h)
description: La funzione glGenLists genera un set contiguo di elenchi di visualizzazione vuoti.
ms.assetid: 07a97e89-1fbe-4405-b1b0-c4c47b098633
keywords:
- funzione glGenLists OpenGL
topic_type:
- apiref
api_name:
- glGenLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc556e789da9c768a7ed1aef6880ad48022a1ee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740479"
---
# <a name="glgenlists-function"></a><span data-ttu-id="c10b6-104">glGenLists (funzione)</span><span class="sxs-lookup"><span data-stu-id="c10b6-104">glGenLists function</span></span>

<span data-ttu-id="c10b6-105">La funzione **glGenLists** genera un set contiguo di elenchi di visualizzazione vuoti.</span><span class="sxs-lookup"><span data-stu-id="c10b6-105">The **glGenLists** function generates a contiguous set of empty display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="c10b6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c10b6-106">Syntax</span></span>


```C++
GLuint WINAPI glGenLists(
   GLsizei range
);
```



## <a name="parameters"></a><span data-ttu-id="c10b6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c10b6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c10b6-108">*range*</span><span class="sxs-lookup"><span data-stu-id="c10b6-108">*range*</span></span> 
</dt> <dd>

<span data-ttu-id="c10b6-109">Numero di elenchi di visualizzazione vuoti contigui da generare.</span><span class="sxs-lookup"><span data-stu-id="c10b6-109">The number of contiguous empty display lists to be generated.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="c10b6-110">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c10b6-110">Error codes</span></span>

<span data-ttu-id="c10b6-111">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="c10b6-111">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c10b6-112">Nome</span><span class="sxs-lookup"><span data-stu-id="c10b6-112">Name</span></span>                                                                                                  | <span data-ttu-id="c10b6-113">Significato</span><span class="sxs-lookup"><span data-stu-id="c10b6-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c10b6-114"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c10b6-114"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="c10b6-115">l' *intervallo* è negativo.</span><span class="sxs-lookup"><span data-stu-id="c10b6-115">*range* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="c10b6-116"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c10b6-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c10b6-117">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c10b6-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c10b6-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="c10b6-118">Remarks</span></span>

<span data-ttu-id="c10b6-119">La funzione **glGenLists** ha un argomento, *Range*.</span><span class="sxs-lookup"><span data-stu-id="c10b6-119">The **glGenLists** function has one argument, *range*.</span></span> <span data-ttu-id="c10b6-120">Restituisce un integer *n* *tale da visualizzare elenchi di visualizzazione* vuoti contigui, denominati *n*, *n* + 1,.</span><span class="sxs-lookup"><span data-stu-id="c10b6-120">It returns an integer *n* such that *range* contiguous empty display lists, named *n*, *n* + 1, .</span></span> <span data-ttu-id="c10b6-121">.</span><span class="sxs-lookup"><span data-stu-id="c10b6-121">.</span></span> <span data-ttu-id="c10b6-122">., *n* + (*intervallo* -1), vengono creati.</span><span class="sxs-lookup"><span data-stu-id="c10b6-122">., *n* + (*range* - 1), are created.</span></span> <span data-ttu-id="c10b6-123">Se *Range* è zero, se non sono disponibili gruppi di nomi contigui di *intervallo* o se viene generato un errore, non viene generato alcun elenco di visualizzazione e viene restituito zero.</span><span class="sxs-lookup"><span data-stu-id="c10b6-123">If *range* is zero, if there is no group of *range* contiguous names available, or if any error is generated, then no display lists are generated and zero is returned.</span></span>

<span data-ttu-id="c10b6-124">La funzione seguente recupera le informazioni correlate a **glGenLists**:</span><span class="sxs-lookup"><span data-stu-id="c10b6-124">The following function retrieves information related to **glGenLists**:</span></span>

[<span data-ttu-id="c10b6-125">**Pagina di**</span><span class="sxs-lookup"><span data-stu-id="c10b6-125">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="c10b6-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c10b6-126">Requirements</span></span>



| <span data-ttu-id="c10b6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c10b6-127">Requirement</span></span> | <span data-ttu-id="c10b6-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c10b6-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c10b6-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c10b6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c10b6-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c10b6-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c10b6-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c10b6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c10b6-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c10b6-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c10b6-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c10b6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c10b6-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c10b6-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c10b6-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="c10b6-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="c10b6-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c10b6-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c10b6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c10b6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c10b6-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c10b6-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c10b6-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c10b6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c10b6-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c10b6-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c10b6-141">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="c10b6-141">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="c10b6-142">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="c10b6-142">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="c10b6-143">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="c10b6-143">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="c10b6-144">**Remo**</span><span class="sxs-lookup"><span data-stu-id="c10b6-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c10b6-145">**Pagina di**</span><span class="sxs-lookup"><span data-stu-id="c10b6-145">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="c10b6-146">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="c10b6-146">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 






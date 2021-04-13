---
title: funzione glIs (GL. h)
description: La funzione gllsList verifica l'esistenza dell'elenco di visualizzazione.
ms.assetid: 86ef3684-8047-4ee4-befd-ec26bcd036c3
keywords:
- funzione di la funzione di un OpenGL
topic_type:
- apiref
api_name:
- glIsList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fdc67d0a7dad18f8850c283f0d5eb224ff9ebbd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341033"
---
# <a name="glislist-function"></a><span data-ttu-id="f2ae0-104">funzione glIs</span><span class="sxs-lookup"><span data-stu-id="f2ae0-104">glIsList function</span></span>

<span data-ttu-id="f2ae0-105">La funzione **gllsList** verifica l'esistenza dell'elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f2ae0-105">The **gllsList** function tests for display list existence.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2ae0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2ae0-106">Syntax</span></span>


```C++
GLboolean WINAPI glIsList(
   GLuint list
);
```



## <a name="parameters"></a><span data-ttu-id="f2ae0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2ae0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2ae0-108">*list*</span><span class="sxs-lookup"><span data-stu-id="f2ae0-108">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="f2ae0-109">Nome di un elenco di visualizzazione potenziale.</span><span class="sxs-lookup"><span data-stu-id="f2ae0-109">A potential display list name.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="f2ae0-110">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f2ae0-110">Error codes</span></span>

<span data-ttu-id="f2ae0-111">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="f2ae0-111">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f2ae0-112">Nome</span><span class="sxs-lookup"><span data-stu-id="f2ae0-112">Name</span></span>                                                                                                  | <span data-ttu-id="f2ae0-113">Significato</span><span class="sxs-lookup"><span data-stu-id="f2ae0-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f2ae0-114"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f2ae0-114"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f2ae0-115">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f2ae0-115">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f2ae0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2ae0-116">Remarks</span></span>

<span data-ttu-id="f2ae0-117">La funzione **gllsList** restituisce GL \_ true se *List* è il nome di un elenco di visualizzazione e restituisce GL \_ false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f2ae0-117">The **gllsList** function returns GL\_TRUE if *list* is the name of a display list and returns GL\_FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2ae0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2ae0-118">Requirements</span></span>



| <span data-ttu-id="f2ae0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2ae0-119">Requirement</span></span> | <span data-ttu-id="f2ae0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f2ae0-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ae0-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2ae0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f2ae0-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f2ae0-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f2ae0-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2ae0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f2ae0-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f2ae0-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f2ae0-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2ae0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2ae0-126"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2ae0-126"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f2ae0-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="f2ae0-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2ae0-128"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2ae0-128"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f2ae0-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f2ae0-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2ae0-130"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2ae0-130"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2ae0-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2ae0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ae0-132">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f2ae0-132">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f2ae0-133">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="f2ae0-133">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="f2ae0-134">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="f2ae0-134">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="f2ae0-135">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="f2ae0-135">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="f2ae0-136">**Remo**</span><span class="sxs-lookup"><span data-stu-id="f2ae0-136">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f2ae0-137">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="f2ae0-137">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="f2ae0-138">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="f2ae0-138">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 






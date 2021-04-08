---
title: funzione gluErrorString (Glu. h)
description: La funzione gluErrorString genera una stringa di errore da un codice di errore OpenGL o GLU. La stringa di errore è solo ANSI.
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
keywords:
- funzione gluErrorString OpenGL
topic_type:
- apiref
api_name:
- gluErrorString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cdcfad0e2a943bf3a475317f32d37921878a8f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741119"
---
# <a name="gluerrorstring-function"></a><span data-ttu-id="e6c09-105">gluErrorString (funzione)</span><span class="sxs-lookup"><span data-stu-id="e6c09-105">gluErrorString function</span></span>

<span data-ttu-id="e6c09-106">La funzione **gluErrorString** genera una stringa di errore da un codice di errore OpenGL o Glu.</span><span class="sxs-lookup"><span data-stu-id="e6c09-106">The **gluErrorString** function produces an error string from an OpenGL or GLU error code.</span></span> <span data-ttu-id="e6c09-107">La stringa di errore è solo ANSI.</span><span class="sxs-lookup"><span data-stu-id="e6c09-107">The error string is ANSI only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c09-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6c09-108">Syntax</span></span>


```C++
const GLubyte* WINAPI gluErrorString(
   GLenum errCode
);
```



## <a name="parameters"></a><span data-ttu-id="e6c09-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6c09-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6c09-110">*errCode*</span><span class="sxs-lookup"><span data-stu-id="e6c09-110">*errCode*</span></span> 
</dt> <dd>

<span data-ttu-id="e6c09-111">Codice di errore OpenGL o GLU.</span><span class="sxs-lookup"><span data-stu-id="e6c09-111">An OpenGL or GLU error code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6c09-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6c09-112">Remarks</span></span>

<span data-ttu-id="e6c09-113">La funzione **gluErrorString** genera una stringa di errore da un codice di errore OpenGL o Glu.</span><span class="sxs-lookup"><span data-stu-id="e6c09-113">The **gluErrorString** function produces an error string from an OpenGL or GLU error code.</span></span> <span data-ttu-id="e6c09-114">La stringa è in un formato ISO Latin 1.</span><span class="sxs-lookup"><span data-stu-id="e6c09-114">The string is in an ISO Latin 1 format.</span></span> <span data-ttu-id="e6c09-115">Ad esempio, **gluErrorString**(GL \_ \_ \_ insufficiente) restituisce la stringa "memoria insufficiente".</span><span class="sxs-lookup"><span data-stu-id="e6c09-115">For example, **gluErrorString**(GL\_OUT\_OF\_MEMORY) returns the string "out of memory".</span></span>

<span data-ttu-id="e6c09-116">I codici di errore standard GLU sono di tipo GLU \_ non valido \_ , il \_ valore non è valido \_ e il valore di Glu non è \_ \_ \_ sufficiente.</span><span class="sxs-lookup"><span data-stu-id="e6c09-116">The standard GLU error codes are GLU\_INVALID\_ENUM, GLU\_INVALID\_VALUE, and GLU\_OUT\_OF\_MEMORY.</span></span> <span data-ttu-id="e6c09-117">Determinate altre funzioni GLU possono restituire codici di errore specializzati tramite callback.</span><span class="sxs-lookup"><span data-stu-id="e6c09-117">Certain other GLU functions can return specialized error codes through callbacks.</span></span> <span data-ttu-id="e6c09-118">Per l'elenco dei codici di errore OpenGL, vedere [**glGetError**](glgeterror.md).</span><span class="sxs-lookup"><span data-stu-id="e6c09-118">For the list of OpenGL error codes, see [**glGetError**](glgeterror.md).</span></span>

<span data-ttu-id="e6c09-119">La funzione **gluErrorString** produce stringhe di errore solo in ANSI.</span><span class="sxs-lookup"><span data-stu-id="e6c09-119">The **gluErrorString** function produces error strings in ANSI only.</span></span> <span data-ttu-id="e6c09-120">Quando possibile, usare **gluErrorStringWIN**, che consente stringhe di errore ANSI o Unicode.</span><span class="sxs-lookup"><span data-stu-id="e6c09-120">Whenever possible, use **gluErrorStringWIN**, which allows ANSI or Unicode error strings.</span></span> <span data-ttu-id="e6c09-121">Questo consente di localizzare più facilmente il programma per l'uso con un altro linguaggio.</span><span class="sxs-lookup"><span data-stu-id="e6c09-121">This makes it easier to localize your program for use with another language.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6c09-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6c09-122">Requirements</span></span>



| <span data-ttu-id="e6c09-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6c09-123">Requirement</span></span> | <span data-ttu-id="e6c09-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e6c09-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c09-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6c09-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e6c09-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e6c09-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e6c09-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6c09-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e6c09-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e6c09-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e6c09-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6c09-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6c09-130"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6c09-130"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="e6c09-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="e6c09-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6c09-132"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6c09-132"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e6c09-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e6c09-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6c09-134"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6c09-134"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6c09-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6c09-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6c09-136">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="e6c09-136">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="e6c09-137">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="e6c09-137">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="e6c09-138">*gluQuadricCallback*</span><span class="sxs-lookup"><span data-stu-id="e6c09-138">*gluQuadricCallback*</span></span>](gluquadric.md)
</dt> <dt>

[<span data-ttu-id="e6c09-139">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="e6c09-139">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 






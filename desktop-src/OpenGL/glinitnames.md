---
title: funzione glInitNames (GL. h)
description: La funzione glInitNames Inizializza lo stack dei nomi.
ms.assetid: 26c134f5-c17c-4637-93b6-5293f316dd6c
keywords:
- funzione glInitNames OpenGL
topic_type:
- apiref
api_name:
- glInitNames
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ebdb9d19f6c88340fd53162febe694e3566408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119050"
---
# <a name="glinitnames-function"></a><span data-ttu-id="998e7-104">glInitNames (funzione)</span><span class="sxs-lookup"><span data-stu-id="998e7-104">glInitNames function</span></span>

<span data-ttu-id="998e7-105">La funzione **glInitNames** Inizializza lo stack dei nomi.</span><span class="sxs-lookup"><span data-stu-id="998e7-105">The **glInitNames** function initializes the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="998e7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="998e7-106">Syntax</span></span>


```C++
void WINAPI glInitNames(void);
```



## <a name="parameters"></a><span data-ttu-id="998e7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="998e7-107">Parameters</span></span>

<span data-ttu-id="998e7-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="998e7-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="998e7-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="998e7-109">Return value</span></span>

<span data-ttu-id="998e7-110">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="998e7-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="998e7-111">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="998e7-111">Error codes</span></span>

<span data-ttu-id="998e7-112">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="998e7-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="998e7-113">Nome</span><span class="sxs-lookup"><span data-stu-id="998e7-113">Name</span></span>                                                                                                  | <span data-ttu-id="998e7-114">Significato</span><span class="sxs-lookup"><span data-stu-id="998e7-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="998e7-115"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="998e7-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="998e7-116">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="998e7-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="998e7-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="998e7-117">Remarks</span></span>

<span data-ttu-id="998e7-118">La funzione **glInitNames** fa sì che lo stack dei nomi venga inizializzato sullo stato vuoto predefinito.</span><span class="sxs-lookup"><span data-stu-id="998e7-118">The **glInitNames** function causes the name stack to be initialized to its default empty state.</span></span> <span data-ttu-id="998e7-119">Lo stack dei nomi viene usato durante la modalità di selezione per consentire l'identificazione univoca di set di comandi di rendering.</span><span class="sxs-lookup"><span data-stu-id="998e7-119">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="998e7-120">È costituito da un set ordinato di interi senza segno.</span><span class="sxs-lookup"><span data-stu-id="998e7-120">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="998e7-121">Lo stack dei nomi è sempre vuoto mentre la modalità di rendering non è GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="998e7-121">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="998e7-122">Le chiamate a **glInitNames** mentre la modalità di rendering non è GL \_ SELECT vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="998e7-122">Calls to **glInitNames** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="998e7-123">Le funzioni seguenti consentono di recuperare informazioni correlate a **glInitNames**:</span><span class="sxs-lookup"><span data-stu-id="998e7-123">The following functions retrieve information related to **glInitNames**:</span></span>

<span data-ttu-id="998e7-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ \_ profondità dello stack nome GL \_</span><span class="sxs-lookup"><span data-stu-id="998e7-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="998e7-125">**glGet** con argomento- \_ \_ \_ profondità dello stack nome Max \_</span><span class="sxs-lookup"><span data-stu-id="998e7-125">**glGet** with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="998e7-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="998e7-126">Requirements</span></span>



| <span data-ttu-id="998e7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="998e7-127">Requirement</span></span> | <span data-ttu-id="998e7-128">Valore</span><span class="sxs-lookup"><span data-stu-id="998e7-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="998e7-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="998e7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="998e7-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="998e7-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="998e7-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="998e7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="998e7-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="998e7-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="998e7-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="998e7-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="998e7-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="998e7-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="998e7-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="998e7-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="998e7-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="998e7-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="998e7-137">DLL</span><span class="sxs-lookup"><span data-stu-id="998e7-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="998e7-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="998e7-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="998e7-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="998e7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="998e7-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="998e7-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="998e7-141">**Remo**</span><span class="sxs-lookup"><span data-stu-id="998e7-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="998e7-142">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="998e7-142">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="998e7-143">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="998e7-143">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="998e7-144">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="998e7-144">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="998e7-145">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="998e7-145">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 






---
title: funzione glPushName (GL. h)
description: Le funzioni glPushName e glPopName effettuano il push e il pop dello stack dei nomi. | funzione glPushName (GL. h)
ms.assetid: e4319018-42c0-4567-b67f-31dbdbee9b13
keywords:
- funzione glPushName OpenGL
topic_type:
- apiref
api_name:
- glPushName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff783a108f5cb1ac34141c6c57f47b16e23531a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321545"
---
# <a name="glpushname-function"></a><span data-ttu-id="cca25-105">glPushName (funzione)</span><span class="sxs-lookup"><span data-stu-id="cca25-105">glPushName function</span></span>

<span data-ttu-id="cca25-106">Le funzioni **glPushName** e [**glPopName**](glpopname.md) effettuano il push e il pop dello stack dei nomi.</span><span class="sxs-lookup"><span data-stu-id="cca25-106">The **glPushName** and [**glPopName**](glpopname.md) functions push and pop the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="cca25-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cca25-107">Syntax</span></span>


```C++
void WINAPI glPushName(
   GLuint name
);
```



## <a name="parameters"></a><span data-ttu-id="cca25-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cca25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cca25-109">*nome*</span><span class="sxs-lookup"><span data-stu-id="cca25-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="cca25-110">Nome che verrà inserito nello stack dei nomi.</span><span class="sxs-lookup"><span data-stu-id="cca25-110">A name that will be pushed onto the name stack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cca25-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cca25-111">Return value</span></span>

<span data-ttu-id="cca25-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="cca25-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cca25-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="cca25-113">Error codes</span></span>

<span data-ttu-id="cca25-114">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="cca25-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="cca25-115">Nome</span><span class="sxs-lookup"><span data-stu-id="cca25-115">Name</span></span>                                                                                                  | <span data-ttu-id="cca25-116">Significato</span><span class="sxs-lookup"><span data-stu-id="cca25-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cca25-117"><dt>**\_overflow dello stack GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cca25-117"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="cca25-118">La funzione è stata chiamata mentre lo stack della matrice corrente era pieno.</span><span class="sxs-lookup"><span data-stu-id="cca25-118">The function was called while the current matrix stack was full.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="cca25-119"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cca25-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cca25-120">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="cca25-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cca25-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="cca25-121">Remarks</span></span>

<span data-ttu-id="cca25-122">La funzione **glPushName** fa sì che il nome venga inserito nello stack dei nomi, inizialmente vuoto.</span><span class="sxs-lookup"><span data-stu-id="cca25-122">The **glPushName** function causes name to be pushed onto the name stack, which is initially empty.</span></span> <span data-ttu-id="cca25-123">La funzione [**glPopName**](glpopname.md) estrae un nome all'inizio dello stack.</span><span class="sxs-lookup"><span data-stu-id="cca25-123">The [**glPopName**](glpopname.md) function pops one name off the top of the stack.</span></span> <span data-ttu-id="cca25-124">Lo stack dei nomi viene usato durante la modalità di selezione per consentire l'identificazione univoca di set di comandi di rendering.</span><span class="sxs-lookup"><span data-stu-id="cca25-124">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="cca25-125">È costituito da un set ordinato di interi senza segno.</span><span class="sxs-lookup"><span data-stu-id="cca25-125">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="cca25-126">Lo stack dei nomi è sempre vuoto mentre la modalità di rendering non è GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="cca25-126">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="cca25-127">Le chiamate a **glPushName** o [**glPopName**](glpopname.md) mentre la modalità di rendering non è GL \_ SELECT vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="cca25-127">Calls to **glPushName** or [**glPopName**](glpopname.md) while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="cca25-128">Le funzioni seguenti recuperano informazioni relative a **glPushName** e [**glPopName**](glpopname.md):</span><span class="sxs-lookup"><span data-stu-id="cca25-128">The following functions retrieve information related to **glPushName** and [**glPopName**](glpopname.md):</span></span>

<span data-ttu-id="cca25-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ \_ profondità dello stack nome GL \_</span><span class="sxs-lookup"><span data-stu-id="cca25-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="cca25-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento- \_ \_ \_ profondità dello stack nome Max \_</span><span class="sxs-lookup"><span data-stu-id="cca25-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="cca25-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cca25-131">Requirements</span></span>



| <span data-ttu-id="cca25-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="cca25-132">Requirement</span></span> | <span data-ttu-id="cca25-133">Valore</span><span class="sxs-lookup"><span data-stu-id="cca25-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cca25-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cca25-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cca25-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cca25-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cca25-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cca25-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cca25-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cca25-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cca25-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cca25-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="cca25-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cca25-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cca25-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="cca25-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="cca25-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cca25-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cca25-142">DLL</span><span class="sxs-lookup"><span data-stu-id="cca25-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cca25-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cca25-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cca25-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cca25-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cca25-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cca25-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cca25-146">**Remo**</span><span class="sxs-lookup"><span data-stu-id="cca25-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cca25-147">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="cca25-147">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="cca25-148">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="cca25-148">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="cca25-149">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="cca25-149">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="cca25-150">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="cca25-150">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 






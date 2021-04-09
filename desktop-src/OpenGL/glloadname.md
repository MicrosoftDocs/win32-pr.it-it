---
title: funzione glLoadName (GL. h)
description: La funzione glLoadName carica un nome nello stack dei nomi.
ms.assetid: 8d7d582b-3743-401e-af71-28034e49f3c2
keywords:
- funzione glLoadName OpenGL
topic_type:
- apiref
api_name:
- glLoadName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb47a0389cda13523104ee429bca46838970e15a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121591"
---
# <a name="glloadname-function"></a><span data-ttu-id="fd589-104">glLoadName (funzione)</span><span class="sxs-lookup"><span data-stu-id="fd589-104">glLoadName function</span></span>

<span data-ttu-id="fd589-105">La funzione **glLoadName** carica un nome nello stack dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fd589-105">The **glLoadName** function loads a name onto the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd589-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd589-106">Syntax</span></span>


```C++
void WINAPI glLoadName(
   GLuint name
);
```



## <a name="parameters"></a><span data-ttu-id="fd589-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd589-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd589-108">*nome*</span><span class="sxs-lookup"><span data-stu-id="fd589-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="fd589-109">Nome che sostituisce il valore superiore nello stack dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fd589-109">A name that will replace the top value on the name stack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd589-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd589-110">Return value</span></span>

<span data-ttu-id="fd589-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="fd589-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fd589-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="fd589-112">Error codes</span></span>

<span data-ttu-id="fd589-113">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="fd589-113">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fd589-114">Nome</span><span class="sxs-lookup"><span data-stu-id="fd589-114">Name</span></span>                                                                                                  | <span data-ttu-id="fd589-115">Significato</span><span class="sxs-lookup"><span data-stu-id="fd589-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd589-116"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd589-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fd589-117">La funzione è stata chiamata mentre lo stack dei nomi era vuoto.</span><span class="sxs-lookup"><span data-stu-id="fd589-117">The function was called while the name stack was empty.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="fd589-118"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd589-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fd589-119">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fd589-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fd589-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd589-120">Remarks</span></span>

<span data-ttu-id="fd589-121">La funzione **glLoadName** fa sì che il *nome* sostituisca il valore all'inizio dello stack dei nomi, che inizialmente è vuoto.</span><span class="sxs-lookup"><span data-stu-id="fd589-121">The **glLoadName** function causes *name* to replace the value on the top of the name stack, which is initially empty.</span></span> <span data-ttu-id="fd589-122">Lo stack dei nomi viene usato durante la modalità di selezione per consentire l'identificazione univoca di set di comandi di rendering.</span><span class="sxs-lookup"><span data-stu-id="fd589-122">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="fd589-123">È costituito da un set ordinato di interi senza segno.</span><span class="sxs-lookup"><span data-stu-id="fd589-123">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="fd589-124">Lo stack dei nomi è sempre vuoto mentre la modalità di rendering non è GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="fd589-124">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="fd589-125">Le chiamate a **glLoadName** mentre la modalità di rendering non è GL \_ SELECT vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="fd589-125">Calls to **glLoadName** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="fd589-126">Le funzioni seguenti consentono di recuperare informazioni correlate a **glLoadName**:</span><span class="sxs-lookup"><span data-stu-id="fd589-126">The following functions retrieve information related to **glLoadName**:</span></span>

<span data-ttu-id="fd589-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ \_ profondità dello stack nome GL \_</span><span class="sxs-lookup"><span data-stu-id="fd589-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="fd589-128">**glGet** con argomento- \_ \_ \_ profondità dello stack nome Max \_</span><span class="sxs-lookup"><span data-stu-id="fd589-128">**glGet** with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="fd589-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd589-129">Requirements</span></span>



| <span data-ttu-id="fd589-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd589-130">Requirement</span></span> | <span data-ttu-id="fd589-131">Valore</span><span class="sxs-lookup"><span data-stu-id="fd589-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd589-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd589-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fd589-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fd589-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fd589-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd589-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fd589-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fd589-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fd589-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fd589-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd589-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd589-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fd589-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="fd589-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd589-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd589-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fd589-140">DLL</span><span class="sxs-lookup"><span data-stu-id="fd589-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd589-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd589-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd589-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd589-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd589-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fd589-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fd589-144">**Remo**</span><span class="sxs-lookup"><span data-stu-id="fd589-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fd589-145">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="fd589-145">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="fd589-146">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="fd589-146">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="fd589-147">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="fd589-147">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="fd589-148">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="fd589-148">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 






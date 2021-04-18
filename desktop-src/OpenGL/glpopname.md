---
title: funzione glPopName (GL. h)
description: Le funzioni glPushName e glPopName effettuano il push e il pop dello stack dei nomi. | funzione glPopName (GL. h)
ms.assetid: ee741188-b275-4839-a89d-4d988c547d07
keywords:
- funzione glPopName OpenGL
topic_type:
- apiref
api_name:
- glPopName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 830c4937b30cca64de3063b42ad16dd3adc87c89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321744"
---
# <a name="glpopname-function"></a><span data-ttu-id="6f921-105">glPopName (funzione)</span><span class="sxs-lookup"><span data-stu-id="6f921-105">glPopName function</span></span>

<span data-ttu-id="6f921-106">Le funzioni [**glPushName**](glpushname.md) e **glPopName** effettuano il push e il pop dello stack dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6f921-106">The [**glPushName**](glpushname.md) and **glPopName** functions push and pop the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f921-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f921-107">Syntax</span></span>


```C++
void WINAPI glPopName(void);
```



## <a name="parameters"></a><span data-ttu-id="6f921-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f921-108">Parameters</span></span>

<span data-ttu-id="6f921-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="6f921-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f921-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f921-110">Return value</span></span>

<span data-ttu-id="6f921-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6f921-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6f921-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="6f921-112">Error codes</span></span>

<span data-ttu-id="6f921-113">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="6f921-113">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6f921-114">Nome</span><span class="sxs-lookup"><span data-stu-id="6f921-114">Name</span></span>                                                                                                  | <span data-ttu-id="6f921-115">Significato</span><span class="sxs-lookup"><span data-stu-id="6f921-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6f921-116"><dt>**\_underflow dello stack GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6f921-116"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="6f921-117">La funzione è stata chiamata mentre lo stack della matrice corrente contiene una sola matrice.</span><span class="sxs-lookup"><span data-stu-id="6f921-117">The function was called while the current matrix stack contained only a single matrix.</span></span><br/>                                     |
| <dl> <span data-ttu-id="6f921-118"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6f921-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6f921-119">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6f921-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6f921-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f921-120">Remarks</span></span>

<span data-ttu-id="6f921-121">La funzione [**glPushName**](glpushname.md) fa sì che il nome venga inserito nello stack dei nomi, inizialmente vuoto.</span><span class="sxs-lookup"><span data-stu-id="6f921-121">The [**glPushName**](glpushname.md) function causes name to be pushed onto the name stack, which is initially empty.</span></span> <span data-ttu-id="6f921-122">La funzione **glPopName** estrae un nome all'inizio dello stack.</span><span class="sxs-lookup"><span data-stu-id="6f921-122">The **glPopName** function pops one name off the top of the stack.</span></span> <span data-ttu-id="6f921-123">Lo stack dei nomi viene usato durante la modalità di selezione per consentire l'identificazione univoca di set di comandi di rendering.</span><span class="sxs-lookup"><span data-stu-id="6f921-123">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="6f921-124">È costituito da un set ordinato di interi senza segno.</span><span class="sxs-lookup"><span data-stu-id="6f921-124">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="6f921-125">Lo stack dei nomi è sempre vuoto mentre la modalità di rendering non è GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="6f921-125">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="6f921-126">Le chiamate a [**glPushName**](glpushname.md) o **glPopName** mentre la modalità di rendering non è GL \_ SELECT vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="6f921-126">Calls to [**glPushName**](glpushname.md) or **glPopName** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="6f921-127">Le funzioni seguenti recuperano informazioni relative a [**glPushName**](glpushname.md) e **glPopName**:</span><span class="sxs-lookup"><span data-stu-id="6f921-127">The following functions retrieve information related to [**glPushName**](glpushname.md) and **glPopName**:</span></span>

<span data-ttu-id="6f921-128">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ \_ profondità dello stack nome GL \_</span><span class="sxs-lookup"><span data-stu-id="6f921-128">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="6f921-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento- \_ \_ \_ profondità dello stack nome Max \_</span><span class="sxs-lookup"><span data-stu-id="6f921-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="6f921-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f921-130">Requirements</span></span>



| <span data-ttu-id="6f921-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f921-131">Requirement</span></span> | <span data-ttu-id="6f921-132">Valore</span><span class="sxs-lookup"><span data-stu-id="6f921-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f921-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f921-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6f921-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f921-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6f921-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f921-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6f921-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f921-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6f921-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f921-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f921-138"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f921-138"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6f921-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="6f921-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="6f921-140"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f921-140"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6f921-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6f921-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f921-142"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f921-142"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f921-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f921-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f921-144">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6f921-144">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6f921-145">**Remo**</span><span class="sxs-lookup"><span data-stu-id="6f921-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6f921-146">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="6f921-146">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="6f921-147">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="6f921-147">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="6f921-148">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="6f921-148">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="6f921-149">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="6f921-149">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 






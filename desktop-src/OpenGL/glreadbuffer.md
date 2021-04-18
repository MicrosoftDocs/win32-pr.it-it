---
title: funzione glReadBuffer (GL. h)
description: La funzione glReadBuffer seleziona un'origine del buffer dei colori per i pixel.
ms.assetid: 734153fa-e809-4b70-867e-55e46ab95712
keywords:
- funzione glReadBuffer OpenGL
topic_type:
- apiref
api_name:
- glReadBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f0e88cdcb2b1b3257b23606f8160e0986584db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302191"
---
# <a name="glreadbuffer-function"></a><span data-ttu-id="d9fe7-104">glReadBuffer (funzione)</span><span class="sxs-lookup"><span data-stu-id="d9fe7-104">glReadBuffer function</span></span>

<span data-ttu-id="d9fe7-105">La funzione **glReadBuffer** seleziona un'origine del buffer dei colori per i pixel.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-105">The **glReadBuffer** function selects a color buffer source for pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9fe7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9fe7-106">Syntax</span></span>


```C++
void WINAPI glReadBuffer(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="d9fe7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9fe7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9fe7-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="d9fe7-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="d9fe7-109">Buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-109">A color buffer.</span></span> <span data-ttu-id="d9fe7-110">I valori accettati sono GL \_ front \_ Left, GL \_ front \_ right, GL \_ back \_ Left, GL \_ back \_ right, GL \_ Front, GL back, GL \_ \_ Left, GL \_ right e GL \_ aux *i*, dove *i* è compreso tra 0 e GL \_ aux \_ buffers 1.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-110">Accepted values are GL\_FRONT\_LEFT, GL\_FRONT\_RIGHT, GL\_BACK\_LEFT, GL\_BACK\_RIGHT, GL\_FRONT, GL\_BACK, GL\_LEFT, GL\_RIGHT, and GL\_AUX *i*, where *i* is between 0 and GL\_AUX\_BUFFERS 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9fe7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9fe7-111">Return value</span></span>

<span data-ttu-id="d9fe7-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d9fe7-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d9fe7-113">Error codes</span></span>

<span data-ttu-id="d9fe7-114">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="d9fe7-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d9fe7-115">Nome</span><span class="sxs-lookup"><span data-stu-id="d9fe7-115">Name</span></span>                                                                                                  | <span data-ttu-id="d9fe7-116">Significato</span><span class="sxs-lookup"><span data-stu-id="d9fe7-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d9fe7-117"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d9fe7-117"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d9fe7-118">la *modalità* non è uno dei dodici o più valori accettati.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-118">*mode* was not an one of the twelve (or more) accepted values.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="d9fe7-119"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d9fe7-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d9fe7-120">la *modalità* specifica un buffer che non esiste.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-120">*mode* specified a buffer that does not exist.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="d9fe7-121"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d9fe7-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d9fe7-122">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="d9fe7-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d9fe7-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9fe7-123">Remarks</span></span>

<span data-ttu-id="d9fe7-124">La funzione **glReadBuffer** specifica un buffer dei colori come origine per i comandi successivi [**glReadPixels**](glreadpixels.md) e [**glCopyPixels**](glcopypixels.md) .</span><span class="sxs-lookup"><span data-stu-id="d9fe7-124">The **glReadBuffer** function specifies a color buffer as the source for subsequent [**glReadPixels**](glreadpixels.md) and [**glCopyPixels**](glcopypixels.md) commands.</span></span> <span data-ttu-id="d9fe7-125">Il parametro *mode* accetta uno dei dodici o più valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-125">The *mode* parameter accepts one of twelve or more predefined values.</span></span> <span data-ttu-id="d9fe7-126">(GL \_ AUX0 tramite GL \_ AUX3 sono sempre definiti. In un sistema completamente configurato, GL front \_ , GL \_ Left e GL \_ front left hanno \_ tutti il nome del buffer di inizio sinistro, GL \_ front \_ right e GL \_ right denominano il buffer anteriore destro e GL \_ back \_ Left e GL \_ tornano il nome del buffer di back-left.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-126">(GL\_AUX0 through GL\_AUX3 are always defined.) In a fully configured system, GL\_FRONT, GL\_LEFT, and GL\_FRONT\_LEFT all name the front-left buffer, GL\_FRONT\_RIGHT and GL\_RIGHT name the front-right buffer, and GL\_BACK\_LEFT and GL\_BACK name the back-left buffer.</span></span>

<span data-ttu-id="d9fe7-127">Le configurazioni con doppio buffer non stereo hanno solo un buffer a sinistra e in primo piano.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-127">Nonstereo double-buffered configurations have only a front-left and a back-left buffer.</span></span> <span data-ttu-id="d9fe7-128">Le configurazioni con buffer singolo hanno un buffer anteriore sinistro e anteriore destro se stereo e solo un buffer anteriore sinistro se non stereo.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-128">Single-buffered configurations have a front-left and a front-right buffer if stereo, and only a front-left buffer if nonstereo.</span></span> <span data-ttu-id="d9fe7-129">Non è possibile specificare un buffer inesistente per **glReadBuffer**.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-129">It is an error to specify a nonexistent buffer to **glReadBuffer**.</span></span>

<span data-ttu-id="d9fe7-130">Per impostazione predefinita, la modalità è di *tipo* GL \_ front in configurazioni con buffer singolo e GL viene \_ nuovamente in configurazioni con doppio buffer.</span><span class="sxs-lookup"><span data-stu-id="d9fe7-130">By default, *mode* is GL\_FRONT in single-buffered configurations, and GL\_BACK in double-buffered configurations.</span></span>

<span data-ttu-id="d9fe7-131">La funzione seguente recupera le informazioni correlate a **glReadBuffer**:</span><span class="sxs-lookup"><span data-stu-id="d9fe7-131">The following function retrieves information related to **glReadBuffer**:</span></span>

<span data-ttu-id="d9fe7-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con buffer di \_ lettura argomento GL \_</span><span class="sxs-lookup"><span data-stu-id="d9fe7-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_READ\_BUFFER</span></span>

## <a name="requirements"></a><span data-ttu-id="d9fe7-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9fe7-133">Requirements</span></span>



| <span data-ttu-id="d9fe7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9fe7-134">Requirement</span></span> | <span data-ttu-id="d9fe7-135">Valore</span><span class="sxs-lookup"><span data-stu-id="d9fe7-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9fe7-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9fe7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d9fe7-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d9fe7-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d9fe7-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9fe7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d9fe7-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d9fe7-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d9fe7-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9fe7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9fe7-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9fe7-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d9fe7-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="d9fe7-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9fe7-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9fe7-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d9fe7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d9fe7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9fe7-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9fe7-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9fe7-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9fe7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9fe7-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d9fe7-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d9fe7-148">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="d9fe7-148">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="d9fe7-149">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="d9fe7-149">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="d9fe7-150">**Remo**</span><span class="sxs-lookup"><span data-stu-id="d9fe7-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d9fe7-151">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="d9fe7-151">**glReadPixels**</span></span>](glreadpixels.md)
</dt> </dl>

 

 






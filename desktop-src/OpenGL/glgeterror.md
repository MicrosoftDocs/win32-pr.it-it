---
title: funzione glGetError (GL. h)
description: La funzione glGetError restituisce informazioni sull'errore.
ms.assetid: 18f0368f-054f-4b84-8397-3f9ee4aa07fa
keywords:
- funzione glGetError OpenGL
topic_type:
- apiref
api_name:
- glGetError
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c0abf6ec03ca0c29ede3b7d396db375fd06ac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964775"
---
# <a name="glgeterror-function"></a><span data-ttu-id="87198-104">glGetError (funzione)</span><span class="sxs-lookup"><span data-stu-id="87198-104">glGetError function</span></span>

<span data-ttu-id="87198-105">La funzione **glGetError** restituisce informazioni sull'errore.</span><span class="sxs-lookup"><span data-stu-id="87198-105">The **glGetError** function returns error information.</span></span>

## <a name="syntax"></a><span data-ttu-id="87198-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87198-106">Syntax</span></span>


```C++
GLenum WINAPI glGetError(void);
```



## <a name="parameters"></a><span data-ttu-id="87198-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="87198-107">Parameters</span></span>

<span data-ttu-id="87198-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="87198-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87198-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87198-109">Return value</span></span>

<span data-ttu-id="87198-110">La funzione **glGetError** restituisce uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="87198-110">The **glGetError** function returns one of the following error codes.</span></span>



| <span data-ttu-id="87198-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="87198-111">Return code</span></span>                                                                                           | <span data-ttu-id="87198-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87198-112">Description</span></span>                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="87198-113"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="87198-113"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="87198-114">È stato specificato un valore non accettabile per un argomento enumerato.</span><span class="sxs-lookup"><span data-stu-id="87198-114">An unacceptable value is specified for an enumerated argument.</span></span> <span data-ttu-id="87198-115">La funzione che ha causato l'errore viene ignorata, senza alcun effetto collaterale per impostare il flag di errore.</span><span class="sxs-lookup"><span data-stu-id="87198-115">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>         |
| <dl> <span data-ttu-id="87198-116"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="87198-116"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="87198-117">Un argomento numerico non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="87198-117">A numeric argument is out of range.</span></span> <span data-ttu-id="87198-118">La funzione che ha causato l'errore viene ignorata, senza alcun effetto collaterale per impostare il flag di errore.</span><span class="sxs-lookup"><span data-stu-id="87198-118">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                                    |
| <dl> <span data-ttu-id="87198-119"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="87198-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="87198-120">L'operazione specificata non è consentita nello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="87198-120">The specified operation is not allowed in the current state.</span></span> <span data-ttu-id="87198-121">La funzione che ha causato l'errore viene ignorata, senza alcun effetto collaterale per impostare il flag di errore.</span><span class="sxs-lookup"><span data-stu-id="87198-121">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>           |
| <dl> <span data-ttu-id="87198-122"><dt>**GL \_ nessun \_ errore**</dt></span><span class="sxs-lookup"><span data-stu-id="87198-122"><dt>**GL\_NO\_ERROR**</dt></span></span> </dl>          | <span data-ttu-id="87198-123">Non è stato registrato alcun errore.</span><span class="sxs-lookup"><span data-stu-id="87198-123">No error has been recorded.</span></span> <span data-ttu-id="87198-124">Il valore di questa costante simbolica è sicuramente zero.</span><span class="sxs-lookup"><span data-stu-id="87198-124">The value of this symbolic constant is guaranteed to be zero.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="87198-125"><dt>**\_overflow dello stack GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="87198-125"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="87198-126">Questa funzione provocherebbe un overflow dello stack.</span><span class="sxs-lookup"><span data-stu-id="87198-126">This function would cause a stack overflow.</span></span> <span data-ttu-id="87198-127">La funzione che ha causato l'errore viene ignorata, senza alcun effetto collaterale per impostare il flag di errore.</span><span class="sxs-lookup"><span data-stu-id="87198-127">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                            |
| <dl> <span data-ttu-id="87198-128"><dt>**\_underflow dello stack GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="87198-128"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="87198-129">Questa funzione provocherebbe un underflow dello stack.</span><span class="sxs-lookup"><span data-stu-id="87198-129">This function would cause a stack underflow.</span></span> <span data-ttu-id="87198-130">La funzione che ha causato l'errore viene ignorata, senza alcun effetto collaterale per impostare il flag di errore.</span><span class="sxs-lookup"><span data-stu-id="87198-130">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                           |
| <dl> <span data-ttu-id="87198-131"><dt>**\_ \_ \_ memoria INsufficiente per GL**</dt></span><span class="sxs-lookup"><span data-stu-id="87198-131"><dt>**GL\_OUT\_OF\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="87198-132">Memoria insufficiente per l'esecuzione della funzione.</span><span class="sxs-lookup"><span data-stu-id="87198-132">There is not enough memory left to execute the function.</span></span> <span data-ttu-id="87198-133">Lo stato di OpenGL non è definito, ad eccezione dello stato dei flag di errore, dopo la registrazione di questo errore.</span><span class="sxs-lookup"><span data-stu-id="87198-133">The state of OpenGL is undefined, except for the state of the error flags, after this error is recorded.</span></span><br/> |



 

<span data-ttu-id="87198-134">Si noti che **glGetError** restituisce l' \_ operazione GL non valida \_ se viene chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="87198-134">Note that **glGetError** returns GL\_INVALID\_OPERATION if it is called between a call to [**glBegin**](glbegin.md) and its corresponding call to [**glEnd**](glend.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="87198-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="87198-135">Remarks</span></span>

<span data-ttu-id="87198-136">A ogni errore rilevabile viene assegnato un codice numerico e un nome simbolico.</span><span class="sxs-lookup"><span data-stu-id="87198-136">Each detectable error is assigned a numeric code and symbolic name.</span></span> <span data-ttu-id="87198-137">Quando si verifica un errore, il flag di errore viene impostato sul valore del codice di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="87198-137">When an error occurs, the error flag is set to the appropriate error code value.</span></span> <span data-ttu-id="87198-138">Non vengono registrati altri errori fino a quando non viene chiamato **glGetError** , viene restituito il codice di errore e il flag viene reimpostato su GL \_ senza \_ errori.</span><span class="sxs-lookup"><span data-stu-id="87198-138">No other errors are recorded until **glGetError** is called, the error code is returned, and the flag is reset to GL\_NO\_ERROR.</span></span> <span data-ttu-id="87198-139">Se una chiamata a **glGetError** restituisce GL \_ No \_ Error, non sono stati rilevati errori dall'ultima chiamata a **glGetError** o dall'inizializzazione di OpenGL.</span><span class="sxs-lookup"><span data-stu-id="87198-139">If a call to **glGetError** returns GL\_NO\_ERROR, there has been no detectable error since the last call to **glGetError**, or since OpenGL was initialized.</span></span>

<span data-ttu-id="87198-140">Per consentire le implementazioni distribuite, è possibile che siano presenti diversi flag di errore.</span><span class="sxs-lookup"><span data-stu-id="87198-140">To allow for distributed implementations, there may be several error flags.</span></span> <span data-ttu-id="87198-141">Se un singolo flag di errore ha registrato un errore, viene restituito il valore di tale flag e tale flag viene reimpostato su GL \_ senza \_ errori quando viene chiamato **glGetError** .</span><span class="sxs-lookup"><span data-stu-id="87198-141">If any single error flag has recorded an error, the value of that flag is returned and that flag is reset to GL\_NO\_ERROR when **glGetError** is called.</span></span> <span data-ttu-id="87198-142">Se più di un flag ha registrato un errore, **glGetError** restituisce e cancella un valore di flag di errore arbitrario.</span><span class="sxs-lookup"><span data-stu-id="87198-142">If more than one flag has recorded an error, **glGetError** returns and clears an arbitrary error flag value.</span></span> <span data-ttu-id="87198-143">Se tutti i flag di errore devono essere reimpostati, è sempre necessario chiamare **glGetError** in un ciclo fino a quando non viene restituito GL \_ nessun \_ errore.</span><span class="sxs-lookup"><span data-stu-id="87198-143">If all error flags are to be reset, you should always call **glGetError** in a loop until it returns GL\_NO\_ERROR.</span></span>

<span data-ttu-id="87198-144">Inizialmente, tutti i flag di errore sono impostati su GL \_ nessun \_ errore.</span><span class="sxs-lookup"><span data-stu-id="87198-144">Initially, all error flags are set to GL\_NO\_ERROR.</span></span>

<span data-ttu-id="87198-145">Quando viene impostato un flag di errore, i risultati di un'operazione OpenGL sono indefiniti solo se si \_ \_ \_ è verificata una memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="87198-145">When an error flag is set, results of an OpenGL operation are undefined only if GL\_OUT\_OF\_MEMORY has occurred.</span></span> <span data-ttu-id="87198-146">In tutti gli altri casi, la funzione che genera l'errore viene ignorata e non ha alcun effetto sullo stato OpenGL o sul contenuto del framebuffer.</span><span class="sxs-lookup"><span data-stu-id="87198-146">In all other cases, the function generating the error is ignored and has no effect on the OpenGL state or framebuffer contents.</span></span>

## <a name="requirements"></a><span data-ttu-id="87198-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87198-147">Requirements</span></span>



| <span data-ttu-id="87198-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="87198-148">Requirement</span></span> | <span data-ttu-id="87198-149">Valore</span><span class="sxs-lookup"><span data-stu-id="87198-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87198-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87198-150">Minimum supported client</span></span><br/> | <span data-ttu-id="87198-151">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="87198-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="87198-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87198-152">Minimum supported server</span></span><br/> | <span data-ttu-id="87198-153">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="87198-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="87198-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87198-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="87198-155"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="87198-155"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="87198-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="87198-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="87198-157"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87198-157"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="87198-158">DLL</span><span class="sxs-lookup"><span data-stu-id="87198-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87198-159"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87198-159"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87198-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87198-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87198-161">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="87198-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="87198-162">**Remo**</span><span class="sxs-lookup"><span data-stu-id="87198-162">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 






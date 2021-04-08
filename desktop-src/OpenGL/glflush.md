---
title: funzione glFlush (GL. h)
description: La funzione glFlush forza l'esecuzione delle funzioni OpenGL in tempo limitato.
ms.assetid: 7544b724-472f-4055-8f1c-64ddb58caaf3
keywords:
- funzione glFlush OpenGL
topic_type:
- apiref
api_name:
- glFlush
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8366fd5c42f68c495d544c20c3382b4e9fd37665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743874"
---
# <a name="glflush-function"></a><span data-ttu-id="5c70b-104">glFlush (funzione)</span><span class="sxs-lookup"><span data-stu-id="5c70b-104">glFlush function</span></span>

<span data-ttu-id="5c70b-105">La funzione **glFlush** forza l'esecuzione delle funzioni OpenGL in tempo limitato.</span><span class="sxs-lookup"><span data-stu-id="5c70b-105">The **glFlush** function forces execution of OpenGL functions in finite time.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c70b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c70b-106">Syntax</span></span>


```C++
void WINAPI glFlush(void);
```



## <a name="parameters"></a><span data-ttu-id="5c70b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c70b-107">Parameters</span></span>

<span data-ttu-id="5c70b-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="5c70b-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c70b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c70b-109">Return value</span></span>

<span data-ttu-id="5c70b-110">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5c70b-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5c70b-111">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="5c70b-111">Error codes</span></span>

<span data-ttu-id="5c70b-112">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5c70b-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5c70b-113">Nome</span><span class="sxs-lookup"><span data-stu-id="5c70b-113">Name</span></span>                                                                                                  | <span data-ttu-id="5c70b-114">Significato</span><span class="sxs-lookup"><span data-stu-id="5c70b-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5c70b-115"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5c70b-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5c70b-116">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5c70b-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5c70b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c70b-117">Remarks</span></span>

<span data-ttu-id="5c70b-118">Diverse implementazioni di OpenGL sono comandi del buffer in diverse posizioni, inclusi i buffer di rete e l'acceleratore grafico stesso.</span><span class="sxs-lookup"><span data-stu-id="5c70b-118">Different OpenGL implementations buffer commands in several different locations, including network buffers and the graphics accelerator itself.</span></span> <span data-ttu-id="5c70b-119">La funzione **glFlush** svuota tutti questi buffer, facendo sì che tutti i comandi rilasciati vengano eseguiti con la stessa velocità con cui vengono accettati dal motore di rendering effettivo.</span><span class="sxs-lookup"><span data-stu-id="5c70b-119">The **glFlush** function empties all these buffers, causing all issued commands to be executed as quickly as they are accepted by the actual rendering engine.</span></span> <span data-ttu-id="5c70b-120">Sebbene questa esecuzione non venga completata in un determinato periodo di tempo, viene completata in un intervallo di tempo limitato.</span><span class="sxs-lookup"><span data-stu-id="5c70b-120">Though this execution may not be completed in any particular time period, it does complete in a finite amount of time.</span></span>

<span data-ttu-id="5c70b-121">Poiché qualsiasi programma OpenGL può essere eseguito in una rete o in un acceleratore che memorizza i comandi nel buffer, assicurarsi di chiamare **glFlush** in tutti i programmi che richiedono che tutti i comandi rilasciati in precedenza siano stati completati.</span><span class="sxs-lookup"><span data-stu-id="5c70b-121">Because any OpenGL program might be executed over a network, or on an accelerator that buffers commands, be sure to call **glFlush** in any programs requiring that all of their previously issued commands have been completed.</span></span> <span data-ttu-id="5c70b-122">Ad esempio, chiamare **glFlush** prima di attendere l'input dell'utente che dipende dall'immagine generata.</span><span class="sxs-lookup"><span data-stu-id="5c70b-122">For example, call **glFlush** before waiting for user input that depends on the generated image.</span></span>

<span data-ttu-id="5c70b-123">La funzione **glFlush** può restituire in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="5c70b-123">The **glFlush** function can return at any time.</span></span> <span data-ttu-id="5c70b-124">Non attende il completamento dell'esecuzione di tutte le funzioni OpenGL rilasciate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="5c70b-124">It does not wait until the execution of all previously issued OpenGL functions is complete.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c70b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c70b-125">Requirements</span></span>



| <span data-ttu-id="5c70b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c70b-126">Requirement</span></span> | <span data-ttu-id="5c70b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5c70b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c70b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c70b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5c70b-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c70b-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5c70b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c70b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5c70b-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c70b-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5c70b-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c70b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c70b-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c70b-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5c70b-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c70b-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="5c70b-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c70b-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5c70b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5c70b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c70b-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c70b-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c70b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c70b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c70b-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5c70b-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5c70b-140">**Remo**</span><span class="sxs-lookup"><span data-stu-id="5c70b-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5c70b-141">**glFinish**</span><span class="sxs-lookup"><span data-stu-id="5c70b-141">**glFinish**</span></span>](glfinish.md)
</dt> </dl>

 

 






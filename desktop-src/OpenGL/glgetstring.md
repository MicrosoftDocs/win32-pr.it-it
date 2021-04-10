---
title: funzione glGetString (GL. h)
description: La funzione glGetString restituisce una stringa che descrive la connessione OpenGL corrente.
ms.assetid: 768e6ec2-3f00-44e6-b3cb-de0f06d6a73d
keywords:
- funzione glGetString OpenGL
topic_type:
- apiref
api_name:
- glGetString
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e263e35802af752fa262c898d036fccaa37aff87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964831"
---
# <a name="glgetstring-function"></a><span data-ttu-id="5998a-104">glGetString (funzione)</span><span class="sxs-lookup"><span data-stu-id="5998a-104">glGetString function</span></span>

<span data-ttu-id="5998a-105">La funzione **glGetString** restituisce una stringa che descrive la connessione OpenGL corrente.</span><span class="sxs-lookup"><span data-stu-id="5998a-105">The **glGetString** function returns a string describing the current OpenGL connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5998a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5998a-106">Syntax</span></span>


```C++
const GLubyte* WINAPI glGetString(
   GLenum name
);
```



## <a name="parameters"></a><span data-ttu-id="5998a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5998a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5998a-108">*nome*</span><span class="sxs-lookup"><span data-stu-id="5998a-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="5998a-109">Una delle costanti simboliche seguenti.</span><span class="sxs-lookup"><span data-stu-id="5998a-109">One of the following symbolic constants.</span></span>



| <span data-ttu-id="5998a-110">Valore</span><span class="sxs-lookup"><span data-stu-id="5998a-110">Value</span></span>                                                                                                                                                         | <span data-ttu-id="5998a-111">Significato</span><span class="sxs-lookup"><span data-stu-id="5998a-111">Meaning</span></span>                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_VENDOR"></span><span id="gl_vendor"></span><dl> <span data-ttu-id="5998a-112"><dt>**\_Fornitore GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5998a-112"><dt>**GL\_VENDOR**</dt></span></span> </dl>             | <span data-ttu-id="5998a-113">Restituisce la società responsabile di questa implementazione di OpenGL.</span><span class="sxs-lookup"><span data-stu-id="5998a-113">Returns the company responsible for this OpenGL implementation.</span></span> <span data-ttu-id="5998a-114">Questo nome non viene modificato da release a Release.</span><span class="sxs-lookup"><span data-stu-id="5998a-114">This name does not change from release to release.</span></span><br/>                                                  |
| <span id="GL_RENDERER"></span><span id="gl_renderer"></span><dl> <span data-ttu-id="5998a-115"><dt>**\_RENDERER GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5998a-115"><dt>**GL\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="5998a-116">Restituisce il nome del renderer.</span><span class="sxs-lookup"><span data-stu-id="5998a-116">Returns the name of the renderer.</span></span> <span data-ttu-id="5998a-117">Questo nome è in genere specifico di una particolare configurazione di una piattaforma hardware.</span><span class="sxs-lookup"><span data-stu-id="5998a-117">This name is typically specific to a particular configuration of a hardware platform.</span></span> <span data-ttu-id="5998a-118">Non cambia da release a Release.</span><span class="sxs-lookup"><span data-stu-id="5998a-118">It does not change from release to release.</span></span><br/> |
| <span id="GL_VERSION"></span><span id="gl_version"></span><dl> <span data-ttu-id="5998a-119"><dt>**\_versione GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5998a-119"><dt>**GL\_VERSION**</dt></span></span> </dl>          | <span data-ttu-id="5998a-120">Restituisce una versione o un numero di versione.</span><span class="sxs-lookup"><span data-stu-id="5998a-120">Returns a version or release number.</span></span><br/>                                                                                                                                |
| <span id="GL_EXTENSIONS"></span><span id="gl_extensions"></span><dl> <span data-ttu-id="5998a-121"><dt>**\_estensioni GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5998a-121"><dt>**GL\_EXTENSIONS**</dt></span></span> </dl> | <span data-ttu-id="5998a-122">Restituisce un elenco separato da spazi di estensioni supportate per OpenGL.</span><span class="sxs-lookup"><span data-stu-id="5998a-122">Returns a space-separated list of supported extensions to OpenGL.</span></span><br/>                                                                                                   |



 

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="5998a-123">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="5998a-123">Error codes</span></span>

<span data-ttu-id="5998a-124">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5998a-124">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5998a-125">Nome</span><span class="sxs-lookup"><span data-stu-id="5998a-125">Name</span></span>                                                                                                  | <span data-ttu-id="5998a-126">Significato</span><span class="sxs-lookup"><span data-stu-id="5998a-126">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5998a-127"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5998a-127"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="5998a-128">il *nome* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="5998a-128">*name* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="5998a-129"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5998a-129"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5998a-130">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5998a-130">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5998a-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="5998a-131">Remarks</span></span>

<span data-ttu-id="5998a-132">La funzione **glGetString** restituisce un puntatore a una stringa statica che descrive alcuni aspetti della connessione OpenGL corrente.</span><span class="sxs-lookup"><span data-stu-id="5998a-132">The **glGetString** function returns a pointer to a static string describing some aspect of the current OpenGL connection.</span></span>

<span data-ttu-id="5998a-133">Poiché OpenGL non include query per le caratteristiche di prestazioni di un'implementazione, si prevede che alcune applicazioni vengano scritte per riconoscere le piattaforme note e modificheranno l'utilizzo di OpenGL in base alle caratteristiche di prestazioni note di queste piattaforme.</span><span class="sxs-lookup"><span data-stu-id="5998a-133">Because OpenGL does not include queries for the performance characteristics of an implementation, it is expected that some applications will be written to recognize known platforms and will modify their OpenGL usage based on known performance characteristics of these platforms.</span></span> <span data-ttu-id="5998a-134">Il \_ Fornitore di stringhe GL e il \_ RENDERER GL insieme specificano una piattaforma in modo univoco e non cambiano da release a Release.</span><span class="sxs-lookup"><span data-stu-id="5998a-134">The strings GL\_VENDOR and GL\_RENDERER together uniquely specify a platform, and will not change from release to release.</span></span> <span data-ttu-id="5998a-135">Devono essere usati come tali dagli algoritmi di riconoscimento della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="5998a-135">They should be used as such by platform recognition algorithms.</span></span>

<span data-ttu-id="5998a-136">Il formato e il contenuto della stringa restituita da **glGetString** dipendono dall'implementazione, ad eccezione del fatto che:</span><span class="sxs-lookup"><span data-stu-id="5998a-136">The format and contents of the string that **glGetString** returns depend on the implementation, except that:</span></span>

-   <span data-ttu-id="5998a-137">I nomi di estensione non includono spazi e saranno separati da spazi nella stringa di estensioni GL \_ .</span><span class="sxs-lookup"><span data-stu-id="5998a-137">Extension names will not include space characters and will be separated by space characters in the GL\_EXTENSIONS string.</span></span>
-   <span data-ttu-id="5998a-138">La \_ stringa di versione di GL inizia con un numero di versione.</span><span class="sxs-lookup"><span data-stu-id="5998a-138">The GL\_VERSION string begins with a version number.</span></span> <span data-ttu-id="5998a-139">Il numero di versione usa uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="5998a-139">The version number uses one of these forms:</span></span>

    <span data-ttu-id="5998a-140">*\_ numero principale*. *\_ numero secondario*</span><span class="sxs-lookup"><span data-stu-id="5998a-140">*major\_number*.*minor\_number*</span></span>

    <span data-ttu-id="5998a-141">*\_ numero principale*. *\_ numero secondario*. *\_ numero di versione*</span><span class="sxs-lookup"><span data-stu-id="5998a-141">*major\_number*.*minor\_number*.*release\_number*</span></span>

-   <span data-ttu-id="5998a-142">Le informazioni specifiche del fornitore possono seguire il numero di versione.</span><span class="sxs-lookup"><span data-stu-id="5998a-142">Vendor-specific information may follow the version number.</span></span> <span data-ttu-id="5998a-143">Il formato dipende dall'implementazione, ma uno spazio separa sempre il numero di versione e le informazioni specifiche del fornitore.</span><span class="sxs-lookup"><span data-stu-id="5998a-143">Its format depends on the implementation, but a space always separates the version number and the vendor-specific information.</span></span>
-   <span data-ttu-id="5998a-144">Tutte le stringhe hanno terminazione null.</span><span class="sxs-lookup"><span data-stu-id="5998a-144">All strings are null-terminated.</span></span>

<span data-ttu-id="5998a-145">Se viene generato un errore, **glGetString** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="5998a-145">If an error is generated, **glGetString** returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="5998a-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5998a-146">Requirements</span></span>



| <span data-ttu-id="5998a-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="5998a-147">Requirement</span></span> | <span data-ttu-id="5998a-148">Valore</span><span class="sxs-lookup"><span data-stu-id="5998a-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5998a-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5998a-149">Minimum supported client</span></span><br/> | <span data-ttu-id="5998a-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5998a-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5998a-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5998a-151">Minimum supported server</span></span><br/> | <span data-ttu-id="5998a-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5998a-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5998a-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5998a-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="5998a-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5998a-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5998a-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="5998a-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="5998a-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5998a-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5998a-157">DLL</span><span class="sxs-lookup"><span data-stu-id="5998a-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5998a-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5998a-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5998a-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5998a-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5998a-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5998a-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5998a-161">**Remo**</span><span class="sxs-lookup"><span data-stu-id="5998a-161">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 






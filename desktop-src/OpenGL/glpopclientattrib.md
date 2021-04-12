---
title: funzione glPopClientAttrib (GL. h)
description: Le funzioni glPushClientAttrib e glPopClientAttrib salvano e ripristinano i gruppi di variabili di stato client nello stack dell'attributo client. | funzione glPopClientAttrib (GL. h)
ms.assetid: 030a3955-35bf-4862-9691-54b0c24514e8
keywords:
- funzione glPopClientAttrib OpenGL
topic_type:
- apiref
api_name:
- glPopClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9f09e9c7292754a736594a9bf3d57a70063744
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353351"
---
# <a name="glpopclientattrib-function"></a><span data-ttu-id="38acc-105">glPopClientAttrib (funzione)</span><span class="sxs-lookup"><span data-stu-id="38acc-105">glPopClientAttrib function</span></span>

<span data-ttu-id="38acc-106">Le funzioni [**glPushClientAttrib**](glpushclientattrib.md) e **glPopClientAttrib** salvano e ripristinano i gruppi di variabili di stato client nello stack dell'attributo client.</span><span class="sxs-lookup"><span data-stu-id="38acc-106">The [**glPushClientAttrib**](glpushclientattrib.md) and **glPopClientAttrib** functions save and restore groups of client-state variables on the client-attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="38acc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38acc-107">Syntax</span></span>


```C++
void WINAPI glPopClientAttrib(void);
```



## <a name="parameters"></a><span data-ttu-id="38acc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="38acc-108">Parameters</span></span>

<span data-ttu-id="38acc-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="38acc-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="38acc-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38acc-110">Return value</span></span>

<span data-ttu-id="38acc-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="38acc-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="38acc-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="38acc-112">Error codes</span></span>

<span data-ttu-id="38acc-113">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="38acc-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="38acc-114">Nome</span><span class="sxs-lookup"><span data-stu-id="38acc-114">Name</span></span>                                                                                               | <span data-ttu-id="38acc-115">Significato</span><span class="sxs-lookup"><span data-stu-id="38acc-115">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="38acc-116"><dt>**\_overflow dello stack GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38acc-116"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="38acc-117">La funzione è stata chiamata mentre lo stack dell'attributo client era pieno.</span><span class="sxs-lookup"><span data-stu-id="38acc-117">The function was called while the client-attribute stack was full.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="38acc-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="38acc-118">Remarks</span></span>

<span data-ttu-id="38acc-119">La funzione **glPushClientAttrib** usa il relativo parametro mask per determinare quali gruppi di variabili di stato client vengono salvati nello stack dell'attributo client.</span><span class="sxs-lookup"><span data-stu-id="38acc-119">The **glPushClientAttrib** function uses its mask parameter to determine which groups of client-state variables are saved on the client-attribute stack.</span></span> <span data-ttu-id="38acc-120">È possibile utilizzare l'operatore OR bit per bit per unire le costanti simboliche accettate per impostare bits e costruire una maschera.</span><span class="sxs-lookup"><span data-stu-id="38acc-120">You can use the bitwise OR operator to join together accepted symbolic constants to set bits and construct a mask.</span></span>

<span data-ttu-id="38acc-121">La funzione **glPopClientAttrib** Ripristina i valori delle variabili di stato client salvate per ultime con **glPushclientAttrib**.</span><span class="sxs-lookup"><span data-stu-id="38acc-121">The **glPopClientAttrib** function restores the values of the client-state variables last saved with **glPushclientAttrib**.</span></span> <span data-ttu-id="38acc-122">Le variabili di stato client non salvate in precedenza rimangono invariate.</span><span class="sxs-lookup"><span data-stu-id="38acc-122">Client-state variables not previously saved are left unchanged.</span></span> <span data-ttu-id="38acc-123">Se si esegue il push degli attributi in uno stack di attributi client completo o se gli attributi vengono estratti da uno stack vuoto, viene impostato un flag di errore e non viene apportata alcuna modifica allo stato OpenGL.</span><span class="sxs-lookup"><span data-stu-id="38acc-123">Pushing attributes onto a full client-attribute stack or popping attributes off an empty stack sets an error flag and no other change is made to the OpenGL state.</span></span> <span data-ttu-id="38acc-124">Per impostazione predefinita, lo stack dell'attributo client è vuoto.</span><span class="sxs-lookup"><span data-stu-id="38acc-124">By default the client attribute stack is empty.</span></span>

<span data-ttu-id="38acc-125">Non è possibile salvare alcuni valori dello stato del client OpenGL nello stack dell'attributo client.</span><span class="sxs-lookup"><span data-stu-id="38acc-125">Some OpenGL client-state values cannot be saved on the client-attribute stack.</span></span> <span data-ttu-id="38acc-126">Ad esempio, non è possibile salvare gli Stati SELECT o feedback nello stack dell'attributo client.</span><span class="sxs-lookup"><span data-stu-id="38acc-126">For example, you cannot save the select or feedback states on the client-attribute stack.</span></span> <span data-ttu-id="38acc-127">La profondità dello stack dell'attributo client è almeno 16.</span><span class="sxs-lookup"><span data-stu-id="38acc-127">The depth of the client-attribute stack is at least 16.</span></span>

<span data-ttu-id="38acc-128">Le funzioni **glPushclientAttrib** e **glPopClientAttrib** non vengono compilate in elenchi di visualizzazione, ma vengono eseguite immediatamente.</span><span class="sxs-lookup"><span data-stu-id="38acc-128">The **glPushclientAttrib** and **glPopClientAttrib** functions are not compiled into display lists, but are executed immediately.</span></span>

<span data-ttu-id="38acc-129">Le funzioni **glPushClientAttrib** e **glPopClientAttrib** possono solo attivare le modalità di archiviazione in pixel e push e pop per gli Stati del client.</span><span class="sxs-lookup"><span data-stu-id="38acc-129">The **glPushClientAttrib** and **glPopClientAttrib** functions can only push and pop pixel storage modes and vertex array client states.</span></span> <span data-ttu-id="38acc-130">È necessario usare [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) per eseguire il push e il pop degli stati conservati nel server.</span><span class="sxs-lookup"><span data-stu-id="38acc-130">You must use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to push and pop states that are kept on the server.</span></span>

> [!Note]  
> <span data-ttu-id="38acc-131">Le funzioni **glPushClientAttrib** e **glPopClientAttrib** sono disponibili solo in OpenGL versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="38acc-131">The **glPushClientAttrib** and **glPopClientAttrib** functions are only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="38acc-132">Le funzioni seguenti recuperano informazioni relative a **glPushClientAttrib** e **glPopClientAttrib**:</span><span class="sxs-lookup"><span data-stu-id="38acc-132">The following functions retrieve information related to **glPushClientAttrib** and **glPopClientAttrib**:</span></span>

<span data-ttu-id="38acc-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ \_ \_ profondità dello stack attrib del client GL \_</span><span class="sxs-lookup"><span data-stu-id="38acc-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="38acc-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ profondità massima \_ \_ \_ dello stack attrib \_ client</span><span class="sxs-lookup"><span data-stu-id="38acc-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="38acc-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38acc-135">Requirements</span></span>



| <span data-ttu-id="38acc-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="38acc-136">Requirement</span></span> | <span data-ttu-id="38acc-137">Valore</span><span class="sxs-lookup"><span data-stu-id="38acc-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38acc-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38acc-138">Minimum supported client</span></span><br/> | <span data-ttu-id="38acc-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="38acc-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="38acc-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38acc-140">Minimum supported server</span></span><br/> | <span data-ttu-id="38acc-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="38acc-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="38acc-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38acc-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="38acc-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="38acc-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="38acc-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="38acc-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="38acc-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38acc-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="38acc-146">DLL</span><span class="sxs-lookup"><span data-stu-id="38acc-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38acc-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38acc-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38acc-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38acc-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38acc-149">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="38acc-149">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="38acc-150">**glDisableClientState**</span><span class="sxs-lookup"><span data-stu-id="38acc-150">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="38acc-151">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="38acc-151">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="38acc-152">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="38acc-152">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="38acc-153">**glGet**</span><span class="sxs-lookup"><span data-stu-id="38acc-153">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="38acc-154">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="38acc-154">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="38acc-155">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="38acc-155">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="38acc-156">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="38acc-156">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="38acc-157">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="38acc-157">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="38acc-158">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="38acc-158">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="38acc-159">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="38acc-159">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="38acc-160">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="38acc-160">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="38acc-161">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="38acc-161">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 






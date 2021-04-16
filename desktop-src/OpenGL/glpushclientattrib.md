---
title: funzione glPushClientAttrib (GL. h)
description: Le funzioni glPushClientAttrib e glPopClientAttrib salvano e ripristinano i gruppi di variabili di stato client nello stack dell'attributo client. | funzione glPushClientAttrib (GL. h)
ms.assetid: 69f28af6-1023-4546-95ff-169525c23b07
keywords:
- funzione glPushClientAttrib OpenGL
topic_type:
- apiref
api_name:
- glPushClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 944e2e4229f0d36f0009ce337fd3806020322dbf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353781"
---
# <a name="glpushclientattrib-function"></a><span data-ttu-id="ae7fd-105">glPushClientAttrib (funzione)</span><span class="sxs-lookup"><span data-stu-id="ae7fd-105">glPushClientAttrib function</span></span>

<span data-ttu-id="ae7fd-106">Le funzioni **glPushClientAttrib** e [**glPopClientAttrib**](glpopclientattrib.md) salvano e ripristinano i gruppi di variabili di stato client nello stack dell'attributo client.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-106">The **glPushClientAttrib** and [**glPopClientAttrib**](glpopclientattrib.md) functions save and restore groups of client-state variables on the client-attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae7fd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae7fd-107">Syntax</span></span>


```C++
void WINAPI glPushClientAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="ae7fd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae7fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae7fd-109">*maschera*</span><span class="sxs-lookup"><span data-stu-id="ae7fd-109">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="ae7fd-110">Maschera che indica gli attributi da salvare.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-110">A mask that indicates which attributes to save.</span></span> <span data-ttu-id="ae7fd-111">Di seguito sono riportate le costanti di maschera simbolica e i relativi stati client OpenGL associati.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-111">The following are the symbolic mask constants and their associated OpenGL client states.</span></span>



| <span data-ttu-id="ae7fd-112">Valore</span><span class="sxs-lookup"><span data-stu-id="ae7fd-112">Value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="ae7fd-113">Significato</span><span class="sxs-lookup"><span data-stu-id="ae7fd-113">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_CLIENT_PIXEL_STORE_BIT"></span><span id="gl_client_pixel_store_bit"></span><dl> <span data-ttu-id="ae7fd-114"><dt>**\_ \_ \_ bit archivio pixel client \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ae7fd-114"><dt>**GL\_CLIENT\_PIXEL\_STORE\_BIT**</dt></span></span> </dl>                                             | <span data-ttu-id="ae7fd-115">Attributi della modalità di archiviazione pixel.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-115">Pixel storage mode attributes.</span></span><br/>         |
| <span id="GL_CLIENT_VERTEX_ARRAY_BIT"></span><span id="gl_client_vertex_array_bit"></span><dl> <span data-ttu-id="ae7fd-116"><dt>**\_ \_ \_ bit matrice Vertex client \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ae7fd-116"><dt>**GL\_CLIENT\_VERTEX\_ARRAY\_BIT**</dt></span></span> </dl>                                          | <span data-ttu-id="ae7fd-117">Attributi di matrici di vertici.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-117">Vertex array attributes.</span></span><br/>               |
| <span id="GL_CLIENT_ALL_ATTRIB_BITs"></span><span id="gl_client_all_attrib_bits"></span><span id="GL_CLIENT_ALL_ATTRIB_BITS"></span><dl> <span data-ttu-id="ae7fd-118"><dt>**\_Client GL \_ tutti \_ i \_ bit attrib**</dt></span><span class="sxs-lookup"><span data-stu-id="ae7fd-118"><dt>**GL\_CLIENT\_ALL\_ATTRIB\_BITs**</dt></span></span> </dl> | <span data-ttu-id="ae7fd-119">tutti gli attributi dello stato client impilabili.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-119">all stackable client-state attributes.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae7fd-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae7fd-120">Return value</span></span>

<span data-ttu-id="ae7fd-121">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ae7fd-122">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ae7fd-122">Error codes</span></span>

<span data-ttu-id="ae7fd-123">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ae7fd-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ae7fd-124">Nome</span><span class="sxs-lookup"><span data-stu-id="ae7fd-124">Name</span></span>                                                                                               | <span data-ttu-id="ae7fd-125">Significato</span><span class="sxs-lookup"><span data-stu-id="ae7fd-125">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ae7fd-126"><dt>**\_overflow dello stack GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ae7fd-126"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="ae7fd-127">La funzione è stata chiamata mentre lo stack dell'attributo client era pieno.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-127">The function was called while the client-attribute stack was full.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ae7fd-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae7fd-128">Remarks</span></span>

<span data-ttu-id="ae7fd-129">La funzione **glPushClientAttrib** usa il relativo parametro mask per determinare quali gruppi di variabili di stato client vengono salvati nello stack dell'attributo client.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-129">The **glPushClientAttrib** function uses its mask parameter to determine which groups of client-state variables are saved on the client-attribute stack.</span></span> <span data-ttu-id="ae7fd-130">È possibile utilizzare l'operatore OR bit per bit per unire le costanti simboliche accettate per impostare bits e costruire una maschera.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-130">You can use the bitwise OR operator to join together accepted symbolic constants to set bits and construct a mask.</span></span>

<span data-ttu-id="ae7fd-131">La funzione [**glPopClientAttrib**](glpopclientattrib.md) Ripristina i valori delle variabili di stato client salvate per ultime con **glPushclientAttrib**.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-131">The [**glPopClientAttrib**](glpopclientattrib.md) function restores the values of the client-state variables last saved with **glPushclientAttrib**.</span></span> <span data-ttu-id="ae7fd-132">Le variabili di stato client non salvate in precedenza rimangono invariate.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-132">Client-state variables not previously saved are left unchanged.</span></span> <span data-ttu-id="ae7fd-133">Se si esegue il push degli attributi in uno stack di attributi client completo o se gli attributi vengono estratti da uno stack vuoto, viene impostato un flag di errore e non viene apportata alcuna modifica allo stato OpenGL.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-133">Pushing attributes onto a full client-attribute stack or popping attributes off an empty stack sets an error flag and no other change is made to the OpenGL state.</span></span> <span data-ttu-id="ae7fd-134">Per impostazione predefinita, lo stack dell'attributo client è vuoto.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-134">By default the client attribute stack is empty.</span></span>

<span data-ttu-id="ae7fd-135">Non è possibile salvare alcuni valori dello stato del client OpenGL nello stack dell'attributo client.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-135">Some OpenGL client-state values cannot be saved on the client-attribute stack.</span></span> <span data-ttu-id="ae7fd-136">Ad esempio, non è possibile salvare gli Stati SELECT o feedback nello stack dell'attributo client.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-136">For example, you cannot save the select or feedback states on the client-attribute stack.</span></span> <span data-ttu-id="ae7fd-137">La profondità dello stack dell'attributo client è almeno 16.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-137">The depth of the client-attribute stack is at least 16.</span></span>

<span data-ttu-id="ae7fd-138">Le funzioni **glPushclientAttrib** e **glPopClientAttrib** non vengono compilate in elenchi di visualizzazione, ma vengono eseguite immediatamente.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-138">The **glPushclientAttrib** and **glPopClientAttrib** functions are not compiled into display lists, but are executed immediately.</span></span>

<span data-ttu-id="ae7fd-139">Le funzioni **glPushClientAttrib** e **glPopClientAttrib** possono solo attivare le modalità di archiviazione in pixel e push e pop per gli Stati del client.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-139">The **glPushClientAttrib** and **glPopClientAttrib** functions can only push and pop pixel storage modes and vertex array client states.</span></span> <span data-ttu-id="ae7fd-140">È necessario usare [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) per eseguire il push e il pop degli stati conservati nel server.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-140">You must use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to push and pop states that are kept on the server.</span></span>

> [!Note]  
> <span data-ttu-id="ae7fd-141">Le funzioni **glPushClientAttrib** e **glPopClientAttrib** sono disponibili solo in OpenGL versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="ae7fd-141">The **glPushClientAttrib** and **glPopClientAttrib** functions are only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="ae7fd-142">Le funzioni seguenti recuperano informazioni relative a **glPushClientAttrib** e **glPopClientAttrib**:</span><span class="sxs-lookup"><span data-stu-id="ae7fd-142">The following functions retrieve information related to **glPushClientAttrib** and **glPopClientAttrib**:</span></span>

<span data-ttu-id="ae7fd-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ \_ \_ profondità dello stack attrib del client GL \_</span><span class="sxs-lookup"><span data-stu-id="ae7fd-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="ae7fd-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ profondità massima \_ \_ \_ dello stack attrib \_ client</span><span class="sxs-lookup"><span data-stu-id="ae7fd-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="ae7fd-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae7fd-145">Requirements</span></span>



| <span data-ttu-id="ae7fd-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae7fd-146">Requirement</span></span> | <span data-ttu-id="ae7fd-147">Valore</span><span class="sxs-lookup"><span data-stu-id="ae7fd-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae7fd-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae7fd-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ae7fd-149">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ae7fd-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ae7fd-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae7fd-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ae7fd-151">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ae7fd-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ae7fd-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae7fd-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae7fd-153"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae7fd-153"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ae7fd-154">Libreria</span><span class="sxs-lookup"><span data-stu-id="ae7fd-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="ae7fd-155"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae7fd-155"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ae7fd-156">DLL</span><span class="sxs-lookup"><span data-stu-id="ae7fd-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae7fd-157"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae7fd-157"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae7fd-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae7fd-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae7fd-159">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="ae7fd-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="ae7fd-160">**glDisableClientState**</span><span class="sxs-lookup"><span data-stu-id="ae7fd-160">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="ae7fd-161">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="ae7fd-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="ae7fd-162">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="ae7fd-162">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="ae7fd-163">**glGet**</span><span class="sxs-lookup"><span data-stu-id="ae7fd-163">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="ae7fd-164">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="ae7fd-164">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="ae7fd-165">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="ae7fd-165">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="ae7fd-166">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="ae7fd-166">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="ae7fd-167">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="ae7fd-167">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="ae7fd-168">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="ae7fd-168">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="ae7fd-169">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="ae7fd-169">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="ae7fd-170">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="ae7fd-170">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="ae7fd-171">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="ae7fd-171">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 






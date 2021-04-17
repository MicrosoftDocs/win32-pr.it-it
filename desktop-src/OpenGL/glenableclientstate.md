---
title: funzione glEnableClientState (GL. h)
description: Le funzioni glEnableClientState e glDisableClientState abilitano e disabilitano rispettivamente le matrici. | funzione glEnableClientState (GL. h)
ms.assetid: 02520f81-0b0d-4774-b1e2-713cf226347f
keywords:
- funzione glEnableClientState OpenGL
topic_type:
- apiref
api_name:
- glEnableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e333a51d4c1fe0a5ff11c717790e03aa6d054a09
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353321"
---
# <a name="glenableclientstate-function"></a><span data-ttu-id="e925c-105">glEnableClientState (funzione)</span><span class="sxs-lookup"><span data-stu-id="e925c-105">glEnableClientState function</span></span>

<span data-ttu-id="e925c-106">Le funzioni **glEnableClientState** e [**glDisableClientState**](gldisableclientstate.md) abilitano e disabilitano rispettivamente le matrici.</span><span class="sxs-lookup"><span data-stu-id="e925c-106">The **glEnableClientState** and [**glDisableClientState**](gldisableclientstate.md) functions enable and disable arrays respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="e925c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e925c-107">Syntax</span></span>


```C++
void WINAPI glEnableClientState(
   GLenum array
);
```



## <a name="parameters"></a><span data-ttu-id="e925c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e925c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e925c-109">*array*</span><span class="sxs-lookup"><span data-stu-id="e925c-109">*array*</span></span> 
</dt> <dd>

<span data-ttu-id="e925c-110">Costante simbolica per la matrice che si vuole abilitare o disabilitare.</span><span class="sxs-lookup"><span data-stu-id="e925c-110">A symbolic constant for the array you want to enable or disable.</span></span> <span data-ttu-id="e925c-111">Questo parametro può assumere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e925c-111">This parameter can assume one of the following values.</span></span>



| <span data-ttu-id="e925c-112">Valore</span><span class="sxs-lookup"><span data-stu-id="e925c-112">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="e925c-113">Significato</span><span class="sxs-lookup"><span data-stu-id="e925c-113">Meaning</span></span>                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <span data-ttu-id="e925c-114"><dt>**\_matrice di colori GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e925c-114"><dt>**GL\_COLOR\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="e925c-115">Se abilitata, usare le matrici di colore con le chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="e925c-115">If enabled, use color arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="e925c-116">Vedere anche [**glColorPointer**](glcolorpointer.md).</span><span class="sxs-lookup"><span data-stu-id="e925c-116">See also [**glColorPointer**](glcolorpointer.md).</span></span><br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <span data-ttu-id="e925c-117"><dt>**\_matrice di \_ flag \_ Edge GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e925c-117"><dt>**GL\_EDGE\_FLAG\_ARRAY**</dt></span></span> </dl>             | <span data-ttu-id="e925c-118">Se abilitata, usare matrici di flag Edge con chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="e925c-118">If enabled, use edge flag arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="e925c-119">Vedere anche [**glEdgeFlagPointer**](gledgeflagpointer.md).</span><span class="sxs-lookup"><span data-stu-id="e925c-119">See also [**glEdgeFlagPointer**](gledgeflagpointer.md).</span></span><br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <span data-ttu-id="e925c-120"><dt>**\_matrice di indici GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e925c-120"><dt>**GL\_INDEX\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="e925c-121">Se abilitata, usare le matrici di indice con le chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="e925c-121">If enabled, use index arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="e925c-122">Vedere anche [**glIndexPointer**](glindexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="e925c-122">See also [**glIndexPointer**](glindexpointer.md).</span></span><br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <span data-ttu-id="e925c-123"><dt>**\_matrice normale \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e925c-123"><dt>**GL\_NORMAL\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="e925c-124">Se abilitata, usare matrici normali con chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="e925c-124">If enabled, use normal arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="e925c-125">Vedere anche [**glNormalPointer**](glnormalpointer.md).</span><span class="sxs-lookup"><span data-stu-id="e925c-125">See also [**glNormalPointer**](glnormalpointer.md).</span></span><br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <span data-ttu-id="e925c-126"><dt>**\_ \_ matrice Coord trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e925c-126"><dt>**GL\_TEXTURE\_COORD\_ARRAY**</dt></span></span> </dl> | <span data-ttu-id="e925c-127">Se abilitata, usare le matrici di coordinate di trama con chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="e925c-127">If enabled, use texture coordinate arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="e925c-128">Vedere anche [**glTexCoordPointer**](gltexcoordpointer.md).</span><span class="sxs-lookup"><span data-stu-id="e925c-128">See also [**glTexCoordPointer**](gltexcoordpointer.md).</span></span><br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <span data-ttu-id="e925c-129"><dt>**\_matrice di vertici GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e925c-129"><dt>**GL\_VERTEX\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="e925c-130">Se abilitata, usare matrici di vertici con chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="e925c-130">If enabled, use vertex arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="e925c-131">Vedere anche [**glVertexPointer**](glvertexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="e925c-131">See also [**glVertexPointer**](glvertexpointer.md).</span></span><br/>                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e925c-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e925c-132">Return value</span></span>

<span data-ttu-id="e925c-133">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="e925c-133">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e925c-134">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e925c-134">Error codes</span></span>

<span data-ttu-id="e925c-135">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="e925c-135">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e925c-136">Nome</span><span class="sxs-lookup"><span data-stu-id="e925c-136">Name</span></span>                                                                                             | <span data-ttu-id="e925c-137">Significato</span><span class="sxs-lookup"><span data-stu-id="e925c-137">Meaning</span></span>                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="e925c-138"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e925c-138"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="e925c-139">la *matrice* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="e925c-139">*array* was not an accepted value.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e925c-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="e925c-140">Remarks</span></span>

<span data-ttu-id="e925c-141">Le funzioni **glEnableClientState** e **glDisableClientState** abilitano e disabilitano varie matrici singole.</span><span class="sxs-lookup"><span data-stu-id="e925c-141">The **glEnableClientState** and **glDisableClientState** functions enable and disable various individual arrays.</span></span> <span data-ttu-id="e925c-142">Usare [**glIsEnabled**](glisenabled.md) o [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) per determinare l'impostazione corrente di tutte le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e925c-142">Use [**glIsEnabled**](glisenabled.md) or [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to determine the current setting of any capability.</span></span>

<span data-ttu-id="e925c-143">La chiamata di **glEnableClientState** e **glDisableClientState** tra le chiamate a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md) può causare un errore.</span><span class="sxs-lookup"><span data-stu-id="e925c-143">Calling **glEnableClientState** and **glDisableClientState** between calls to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md) can cause an error.</span></span> <span data-ttu-id="e925c-144">Se non viene generato alcun errore, il comportamento non è definito.</span><span class="sxs-lookup"><span data-stu-id="e925c-144">If no error is generated, the behavior is undefined.</span></span>

> [!Note]  
> <span data-ttu-id="e925c-145">Le funzioni **glEnableClientState** e **glDisableClientState** sono disponibili solo in OpenGL versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="e925c-145">The **glEnableClientState** and **glDisableClientState** functions are only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e925c-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e925c-146">Requirements</span></span>



| <span data-ttu-id="e925c-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="e925c-147">Requirement</span></span> | <span data-ttu-id="e925c-148">Valore</span><span class="sxs-lookup"><span data-stu-id="e925c-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e925c-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e925c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="e925c-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e925c-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e925c-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e925c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="e925c-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e925c-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e925c-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e925c-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="e925c-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e925c-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e925c-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="e925c-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="e925c-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e925c-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e925c-157">DLL</span><span class="sxs-lookup"><span data-stu-id="e925c-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e925c-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e925c-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e925c-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e925c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e925c-160">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="e925c-160">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="e925c-161">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e925c-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e925c-162">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="e925c-162">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="e925c-163">**glDisableClientState**</span><span class="sxs-lookup"><span data-stu-id="e925c-163">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="e925c-164">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="e925c-164">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="e925c-165">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="e925c-165">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="e925c-166">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="e925c-166">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="e925c-167">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="e925c-167">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="e925c-168">**Remo**</span><span class="sxs-lookup"><span data-stu-id="e925c-168">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e925c-169">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="e925c-169">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="e925c-170">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="e925c-170">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="e925c-171">**glInterleavedArrays**</span><span class="sxs-lookup"><span data-stu-id="e925c-171">**glInterleavedArrays**</span></span>](glinterleavedarrays.md)
</dt> <dt>

[<span data-ttu-id="e925c-172">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="e925c-172">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="e925c-173">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="e925c-173">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="e925c-174">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="e925c-174">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 






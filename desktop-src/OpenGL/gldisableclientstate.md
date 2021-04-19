---
title: funzione glDisableClientState (GL. h)
description: Le funzioni glEnableClientState e glDisableClientState abilitano e disabilitano rispettivamente le matrici. | funzione glDisableClientState (GL. h)
ms.assetid: b3316519-00ed-45f8-9c4b-2e04c483751e
keywords:
- funzione glDisableClientState OpenGL
topic_type:
- apiref
api_name:
- glDisableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 163a7c3b679c979e5c800d2aa41ba2abb00e11f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321853"
---
# <a name="gldisableclientstate-function"></a><span data-ttu-id="0db64-105">glDisableClientState (funzione)</span><span class="sxs-lookup"><span data-stu-id="0db64-105">glDisableClientState function</span></span>

<span data-ttu-id="0db64-106">Le funzioni [**glEnableClientState**](glenableclientstate.md) e **glDisableClientState** abilitano e disabilitano rispettivamente le matrici.</span><span class="sxs-lookup"><span data-stu-id="0db64-106">The [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** functions enable and disable arrays respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="0db64-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0db64-107">Syntax</span></span>


```C++
void WINAPI glDisableClientState(
   GLenum array
);
```



## <a name="parameters"></a><span data-ttu-id="0db64-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0db64-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0db64-109">*array*</span><span class="sxs-lookup"><span data-stu-id="0db64-109">*array*</span></span> 
</dt> <dd>

<span data-ttu-id="0db64-110">Costante simbolica per la matrice che si vuole abilitare o disabilitare.</span><span class="sxs-lookup"><span data-stu-id="0db64-110">A symbolic constant for the array you want to enable or disable.</span></span> <span data-ttu-id="0db64-111">Questo parametro può assumere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0db64-111">This parameter can assume one of the following values.</span></span>



| <span data-ttu-id="0db64-112">Valore</span><span class="sxs-lookup"><span data-stu-id="0db64-112">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="0db64-113">Significato</span><span class="sxs-lookup"><span data-stu-id="0db64-113">Meaning</span></span>                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <span data-ttu-id="0db64-114"><dt>**\_matrice di colori GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0db64-114"><dt>**GL\_COLOR\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="0db64-115">Se abilitata, usare le matrici di colore con le chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="0db64-115">If enabled, use color arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="0db64-116">Vedere anche [**glColorPointer**](glcolorpointer.md).</span><span class="sxs-lookup"><span data-stu-id="0db64-116">See also [**glColorPointer**](glcolorpointer.md).</span></span><br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <span data-ttu-id="0db64-117"><dt>**\_matrice di \_ flag \_ Edge GL**</dt></span><span class="sxs-lookup"><span data-stu-id="0db64-117"><dt>**GL\_EDGE\_FLAG\_ARRAY**</dt></span></span> </dl>             | <span data-ttu-id="0db64-118">Se abilitata, usare matrici di flag Edge con chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="0db64-118">If enabled, use edge flag arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="0db64-119">Vedere anche [**glEdgeFlagPointer**](gledgeflagpointer.md).</span><span class="sxs-lookup"><span data-stu-id="0db64-119">See also [**glEdgeFlagPointer**](gledgeflagpointer.md).</span></span><br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <span data-ttu-id="0db64-120"><dt>**\_matrice di indici GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0db64-120"><dt>**GL\_INDEX\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="0db64-121">Se abilitata, usare le matrici di indice con le chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="0db64-121">If enabled, use index arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="0db64-122">Vedere anche [**glIndexPointer**](glindexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="0db64-122">See also [**glIndexPointer**](glindexpointer.md).</span></span><br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <span data-ttu-id="0db64-123"><dt>**\_matrice normale \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="0db64-123"><dt>**GL\_NORMAL\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="0db64-124">Se abilitata, usare matrici normali con chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="0db64-124">If enabled, use normal arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="0db64-125">Vedere anche [**glNormalPointer**](glnormalpointer.md).</span><span class="sxs-lookup"><span data-stu-id="0db64-125">See also [**glNormalPointer**](glnormalpointer.md).</span></span><br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <span data-ttu-id="0db64-126"><dt>**\_ \_ matrice Coord trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="0db64-126"><dt>**GL\_TEXTURE\_COORD\_ARRAY**</dt></span></span> </dl> | <span data-ttu-id="0db64-127">Se abilitata, usare le matrici di coordinate di trama con chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="0db64-127">If enabled, use texture coordinate arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="0db64-128">Vedere anche [**glTexCoordPointer**](gltexcoordpointer.md).</span><span class="sxs-lookup"><span data-stu-id="0db64-128">See also [**glTexCoordPointer**](gltexcoordpointer.md).</span></span><br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <span data-ttu-id="0db64-129"><dt>**\_matrice di vertici GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0db64-129"><dt>**GL\_VERTEX\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="0db64-130">Se abilitata, usare matrici di vertici con chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="0db64-130">If enabled, use vertex arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="0db64-131">Vedere anche [**glVertexPointer**](glvertexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="0db64-131">See also [**glVertexPointer**](glvertexpointer.md).</span></span><br/>                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0db64-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0db64-132">Return value</span></span>

<span data-ttu-id="0db64-133">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="0db64-133">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0db64-134">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0db64-134">Error codes</span></span>

<span data-ttu-id="0db64-135">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="0db64-135">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0db64-136">Nome</span><span class="sxs-lookup"><span data-stu-id="0db64-136">Name</span></span>                                                                                             | <span data-ttu-id="0db64-137">Significato</span><span class="sxs-lookup"><span data-stu-id="0db64-137">Meaning</span></span>                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="0db64-138"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0db64-138"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="0db64-139">la *matrice* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="0db64-139">*array* was not an accepted value.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0db64-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="0db64-140">Remarks</span></span>

<span data-ttu-id="0db64-141">Le funzioni [**glEnableClientState**](glenableclientstate.md) e **glDisableClientState** abilitano e disabilitano varie matrici singole.</span><span class="sxs-lookup"><span data-stu-id="0db64-141">The [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** functions enable and disable various individual arrays.</span></span> <span data-ttu-id="0db64-142">Usare [**glIsEnabled**](glisenabled.md) o [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) per determinare l'impostazione corrente di tutte le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="0db64-142">Use [**glIsEnabled**](glisenabled.md) or [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to determine the current setting of any capability.</span></span>

<span data-ttu-id="0db64-143">La chiamata di [**glEnableClientState**](glenableclientstate.md) e **glDisableClientState** tra le chiamate a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md) può causare un errore.</span><span class="sxs-lookup"><span data-stu-id="0db64-143">Calling [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** between calls to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md) can cause an error.</span></span> <span data-ttu-id="0db64-144">Se non viene generato alcun errore, il comportamento non è definito.</span><span class="sxs-lookup"><span data-stu-id="0db64-144">If no error is generated, the behavior is undefined.</span></span>

> [!Note]  
> <span data-ttu-id="0db64-145">Le funzioni [**glEnableClientState**](glenableclientstate.md) e **glDisableClientState** sono disponibili solo in OpenGL versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="0db64-145">The [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** functions are only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0db64-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0db64-146">Requirements</span></span>



| <span data-ttu-id="0db64-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="0db64-147">Requirement</span></span> | <span data-ttu-id="0db64-148">Valore</span><span class="sxs-lookup"><span data-stu-id="0db64-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0db64-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0db64-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0db64-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0db64-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0db64-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0db64-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0db64-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0db64-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0db64-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0db64-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="0db64-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0db64-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0db64-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="0db64-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="0db64-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0db64-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0db64-157">DLL</span><span class="sxs-lookup"><span data-stu-id="0db64-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0db64-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0db64-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0db64-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0db64-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0db64-160">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="0db64-160">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="0db64-161">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0db64-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0db64-162">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="0db64-162">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="0db64-163">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="0db64-163">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="0db64-164">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="0db64-164">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="0db64-165">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="0db64-165">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="0db64-166">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="0db64-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="0db64-167">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="0db64-167">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="0db64-168">**Remo**</span><span class="sxs-lookup"><span data-stu-id="0db64-168">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0db64-169">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="0db64-169">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="0db64-170">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="0db64-170">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="0db64-171">**glInterleavedArrays**</span><span class="sxs-lookup"><span data-stu-id="0db64-171">**glInterleavedArrays**</span></span>](glinterleavedarrays.md)
</dt> <dt>

[<span data-ttu-id="0db64-172">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="0db64-172">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="0db64-173">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="0db64-173">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="0db64-174">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="0db64-174">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 






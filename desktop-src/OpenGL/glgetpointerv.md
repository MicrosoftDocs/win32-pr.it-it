---
title: funzione glGetPointerv (GL. h)
description: La funzione glGetPointerv restituisce l'indirizzo di una matrice di dati vertex.
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
keywords:
- funzione glGetPointerv OpenGL
topic_type:
- apiref
api_name:
- glGetPointerv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569861922514af88835fbb4e313dab3286b7c47d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302192"
---
# <a name="glgetpointerv-function"></a><span data-ttu-id="e9d41-104">glGetPointerv (funzione)</span><span class="sxs-lookup"><span data-stu-id="e9d41-104">glGetPointerv function</span></span>

<span data-ttu-id="e9d41-105">La funzione **glGetPointerv** restituisce l'indirizzo di una matrice di dati vertex.</span><span class="sxs-lookup"><span data-stu-id="e9d41-105">The **glGetPointerv** function returns the address of a vertex data array.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9d41-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9d41-106">Syntax</span></span>


```C++
void WINAPI glGetPointerv(
   GLenum pname,
   GLvoid **params
);
```



## <a name="parameters"></a><span data-ttu-id="e9d41-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9d41-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9d41-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="e9d41-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="e9d41-109">Il tipo di puntatore di matrice da restituire dalle costanti simboliche seguenti: puntatore alla matrice di colori GL, puntatore alla matrice del flag Edge GL, puntatore del buffer del feedback GL, puntatore della matrice di \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ indici GL, puntatore di matrice GL Normal, puntatore della matrice Coord della trama GL, \_ \_ \_ puntatore al \_ \_ \_ \_ \_ \_ \_ \_ \_ buffer di selezione GL \_ e puntatore alla matrice del \_ vertice GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e9d41-109">The type of array pointer to return from the following symbolic constants: GL\_COLOR\_ARRAY\_POINTER, GL\_EDGE\_FLAG\_ARRAY\_POINTER, GL\_FEEDBACK\_BUFFER\_POINTER, GL\_INDEX\_ARRAY\_POINTER, GL\_NORMAL\_ARRAY\_POINTER, GL\_TEXTURE\_COORD\_ARRAY\_POINTER, GL\_SELECTION\_BUFFER\_POINTER, and GL\_VERTEX\_ARRAY\_POINTER.</span></span>

</dd> <dt>

<span data-ttu-id="e9d41-110">*params*</span><span class="sxs-lookup"><span data-stu-id="e9d41-110">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="e9d41-111">Restituisce il valore del puntatore di matrice specificato da *pname*.</span><span class="sxs-lookup"><span data-stu-id="e9d41-111">Returns the value of the array pointer specified by *pname*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9d41-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9d41-112">Return value</span></span>

<span data-ttu-id="e9d41-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="e9d41-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e9d41-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e9d41-114">Error codes</span></span>

<span data-ttu-id="e9d41-115">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="e9d41-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e9d41-116">Nome</span><span class="sxs-lookup"><span data-stu-id="e9d41-116">Name</span></span>                                                                                             | <span data-ttu-id="e9d41-117">Significato</span><span class="sxs-lookup"><span data-stu-id="e9d41-117">Meaning</span></span>                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="e9d41-118"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e9d41-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="e9d41-119">*pname* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="e9d41-119">*pname* was not an accepted value.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e9d41-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9d41-120">Remarks</span></span>

<span data-ttu-id="e9d41-121">La funzione **glGetPointerv** restituisce informazioni sul puntatore alla matrice.</span><span class="sxs-lookup"><span data-stu-id="e9d41-121">The **glGetPointerv** function returns array pointer information.</span></span> <span data-ttu-id="e9d41-122">Il parametro *pname* è una costante simbolica che specifica il tipo di puntatore alla matrice da restituire e *params* è un puntatore a una posizione in cui inserire i dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="e9d41-122">The *pname* parameter is a symbolic constant specifying the kind of array pointer to return, and *params* is a pointer to a location to place the returned data.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9d41-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9d41-123">Requirements</span></span>



| <span data-ttu-id="e9d41-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9d41-124">Requirement</span></span> | <span data-ttu-id="e9d41-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e9d41-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d41-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9d41-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e9d41-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e9d41-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e9d41-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9d41-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e9d41-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e9d41-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e9d41-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9d41-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9d41-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9d41-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e9d41-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="e9d41-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="e9d41-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9d41-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e9d41-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e9d41-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9d41-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9d41-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9d41-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9d41-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9d41-137">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="e9d41-137">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="e9d41-138">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="e9d41-138">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="e9d41-139">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="e9d41-139">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="e9d41-140">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="e9d41-140">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="e9d41-141">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="e9d41-141">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="e9d41-142">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="e9d41-142">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="e9d41-143">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="e9d41-143">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="e9d41-144">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="e9d41-144">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="e9d41-145">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="e9d41-145">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 






---
title: funzione glTranslatef (GL. h)
description: La funzione glTranslatef moltiplica la matrice corrente in base a una matrice di traslazione.
ms.assetid: 2354ad52-e80f-49fc-82e7-ac6c146aa59d
keywords:
- funzione glTranslatef OpenGL
topic_type:
- apiref
api_name:
- glTranslatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5b52c3890b70ecb931211af1788afe2b8e6ad4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103885922"
---
# <a name="gltranslatef-function"></a><span data-ttu-id="6872c-104">glTranslatef (funzione)</span><span class="sxs-lookup"><span data-stu-id="6872c-104">glTranslatef function</span></span>

<span data-ttu-id="6872c-105">La funzione [**glTranslatef**](gltranslate.md) moltiplica la matrice corrente in base a una matrice di traslazione.</span><span class="sxs-lookup"><span data-stu-id="6872c-105">The [**glTranslatef**](gltranslate.md) function multiplies the current matrix by a translation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6872c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6872c-106">Syntax</span></span>


```C++
void WINAPI glTranslatef(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a><span data-ttu-id="6872c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6872c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6872c-108">*x*</span><span class="sxs-lookup"><span data-stu-id="6872c-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="6872c-109">Coordinata *x* di un vettore di traslazione.</span><span class="sxs-lookup"><span data-stu-id="6872c-109">The *x* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="6872c-110">*y*</span><span class="sxs-lookup"><span data-stu-id="6872c-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="6872c-111">Coordinata *y* di un vettore di traslazione.</span><span class="sxs-lookup"><span data-stu-id="6872c-111">The *y* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="6872c-112">*z*</span><span class="sxs-lookup"><span data-stu-id="6872c-112">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="6872c-113">Coordinata *z* di un vettore di traslazione.</span><span class="sxs-lookup"><span data-stu-id="6872c-113">The *z* coordinate of a translation vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6872c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6872c-114">Return value</span></span>

<span data-ttu-id="6872c-115">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6872c-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6872c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6872c-116">Remarks</span></span>

<span data-ttu-id="6872c-117">La funzione **glTranslatef** produce la traduzione specificata da (*x*, *y*, *z*).</span><span class="sxs-lookup"><span data-stu-id="6872c-117">The **glTranslatef** function produces the translation specified by (*x*, *y*, *z*).</span></span> <span data-ttu-id="6872c-118">Il vettore di traduzione viene usato per calcolare una matrice di traslazione 4x4:</span><span class="sxs-lookup"><span data-stu-id="6872c-118">The translation vector is used to compute a 4x4 translation matrix:</span></span>

![Diagramma che mostra la matrice di conversione 4x4 specificata da x, y, z.](images/trans01.png)

<span data-ttu-id="6872c-120">La matrice corrente (vedere [**glMatrixMode**](glmatrixmode.md)) viene moltiplicata per la matrice di traslazione, con il prodotto che sostituisce la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="6872c-120">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this translation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="6872c-121">Ovvero, se M è la matrice corrente e T è la matrice di traslazione, M viene sostituito con M T.</span><span class="sxs-lookup"><span data-stu-id="6872c-121">That is, if M is the current matrix and T is the translation matrix, then M is replaced with M T.</span></span>

<span data-ttu-id="6872c-122">Se la modalità matrice è la \_ proiezione GL MODELVIEW o GL \_ , verranno tradotti tutti gli oggetti disegnati dopo **glTranslatef** .</span><span class="sxs-lookup"><span data-stu-id="6872c-122">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glTranslatef** is called are translated.</span></span> <span data-ttu-id="6872c-123">Usare [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix** per salvare e ripristinare il sistema di coordinate non convertito.</span><span class="sxs-lookup"><span data-stu-id="6872c-123">Use [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** to save and restore the untranslated coordinate system.</span></span>

<span data-ttu-id="6872c-124">Le funzioni seguenti recuperano informazioni relative a [**glTranslated**](gltranslate.md) e **glTranslatef**:</span><span class="sxs-lookup"><span data-stu-id="6872c-124">The following functions retrieve information related to [**glTranslated**](gltranslate.md) and **glTranslatef**:</span></span>

<span data-ttu-id="6872c-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="6872c-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="6872c-126">**glGet** con argomento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="6872c-126">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="6872c-127">**glGet** con matrice di \_ proiezione GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="6872c-127">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="6872c-128">**glGet** con argomento della \_ matrice di trama GL \_</span><span class="sxs-lookup"><span data-stu-id="6872c-128">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="6872c-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6872c-129">Requirements</span></span>



| <span data-ttu-id="6872c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6872c-130">Requirement</span></span> | <span data-ttu-id="6872c-131">Valore</span><span class="sxs-lookup"><span data-stu-id="6872c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6872c-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6872c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6872c-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6872c-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6872c-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6872c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6872c-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6872c-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6872c-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6872c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6872c-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6872c-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6872c-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="6872c-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="6872c-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6872c-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6872c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6872c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6872c-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6872c-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6872c-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6872c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6872c-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6872c-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6872c-144">**Remo**</span><span class="sxs-lookup"><span data-stu-id="6872c-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6872c-145">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="6872c-145">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="6872c-146">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="6872c-146">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="6872c-147">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="6872c-147">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="6872c-148">**glRotate**</span><span class="sxs-lookup"><span data-stu-id="6872c-148">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="6872c-149">**glScale**</span><span class="sxs-lookup"><span data-stu-id="6872c-149">**glScale**</span></span>](glscale.md)
</dt> </dl>

 

 






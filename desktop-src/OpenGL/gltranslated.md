---
title: funzione glTranslated (GL. h)
description: La funzione glTranslated moltiplica la matrice corrente in base a una matrice di traslazione.
ms.assetid: 9f066a92-ee78-44d1-b8f8-0eacde0e1a47
keywords:
- funzione glTranslated OpenGL
topic_type:
- apiref
api_name:
- glTranslated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705c8dd0635294b066897db99c0770b5f6622c75
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320424"
---
# <a name="gltranslated-function"></a><span data-ttu-id="a3db0-104">glTranslated (funzione)</span><span class="sxs-lookup"><span data-stu-id="a3db0-104">glTranslated function</span></span>

<span data-ttu-id="a3db0-105">La funzione **glTranslated** moltiplica la matrice corrente in base a una matrice di traslazione.</span><span class="sxs-lookup"><span data-stu-id="a3db0-105">The **glTranslated** function multiplies the current matrix by a translation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3db0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3db0-106">Syntax</span></span>


```C++
void WINAPI glTranslated(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="a3db0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3db0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3db0-108">*x*</span><span class="sxs-lookup"><span data-stu-id="a3db0-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="a3db0-109">Coordinata *x* di un vettore di traslazione.</span><span class="sxs-lookup"><span data-stu-id="a3db0-109">The *x* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="a3db0-110">*y*</span><span class="sxs-lookup"><span data-stu-id="a3db0-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="a3db0-111">Coordinata *y* di un vettore di traslazione.</span><span class="sxs-lookup"><span data-stu-id="a3db0-111">The *y* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="a3db0-112">*z*</span><span class="sxs-lookup"><span data-stu-id="a3db0-112">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="a3db0-113">Coordinata *z* di un vettore di traslazione.</span><span class="sxs-lookup"><span data-stu-id="a3db0-113">The *z* coordinate of a translation vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3db0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3db0-114">Return value</span></span>

<span data-ttu-id="a3db0-115">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a3db0-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3db0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3db0-116">Remarks</span></span>

<span data-ttu-id="a3db0-117">La funzione **glTranslated** produce la traduzione specificata da (*x*, *y*, *z*).</span><span class="sxs-lookup"><span data-stu-id="a3db0-117">The **glTranslated** function produces the translation specified by (*x*, *y*, *z*).</span></span> <span data-ttu-id="a3db0-118">Il vettore di traduzione viene usato per calcolare una matrice di traslazione 4x4:</span><span class="sxs-lookup"><span data-stu-id="a3db0-118">The translation vector is used to compute a 4x4 translation matrix:</span></span>

![Diagramma che mostra la matrice di conversione 4x4 specificata da x, y, z.](images/trans01.png)

<span data-ttu-id="a3db0-120">La matrice corrente (vedere [**glMatrixMode**](glmatrixmode.md)) viene moltiplicata per la matrice di traslazione, con il prodotto che sostituisce la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="a3db0-120">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this translation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="a3db0-121">Ovvero, se M è la matrice corrente e T è la matrice di traslazione, M viene sostituito con M T.</span><span class="sxs-lookup"><span data-stu-id="a3db0-121">That is, if M is the current matrix and T is the translation matrix, then M is replaced with M T.</span></span>

<span data-ttu-id="a3db0-122">Se la modalità matrice è la \_ proiezione GL MODELVIEW o GL \_ , verranno tradotti tutti gli oggetti disegnati dopo **glTranslated** .</span><span class="sxs-lookup"><span data-stu-id="a3db0-122">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glTranslated** is called are translated.</span></span> <span data-ttu-id="a3db0-123">Usare [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix** per salvare e ripristinare il sistema di coordinate non convertito.</span><span class="sxs-lookup"><span data-stu-id="a3db0-123">Use [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** to save and restore the untranslated coordinate system.</span></span>

<span data-ttu-id="a3db0-124">Le funzioni seguenti consentono di recuperare informazioni correlate a [**glTranslated**](gltranslate.md):</span><span class="sxs-lookup"><span data-stu-id="a3db0-124">The following functions retrieve information related to [**glTranslated**](gltranslate.md):</span></span>

<span data-ttu-id="a3db0-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="a3db0-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="a3db0-126">**glGet** con argomento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="a3db0-126">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="a3db0-127">**glGet** con matrice di \_ proiezione GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="a3db0-127">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="a3db0-128">**glGet** con argomento della \_ matrice di trama GL \_</span><span class="sxs-lookup"><span data-stu-id="a3db0-128">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="a3db0-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3db0-129">Requirements</span></span>



| <span data-ttu-id="a3db0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3db0-130">Requirement</span></span> | <span data-ttu-id="a3db0-131">Valore</span><span class="sxs-lookup"><span data-stu-id="a3db0-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3db0-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3db0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a3db0-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a3db0-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a3db0-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3db0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a3db0-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a3db0-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a3db0-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3db0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3db0-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3db0-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a3db0-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="a3db0-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3db0-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3db0-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a3db0-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a3db0-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3db0-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3db0-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3db0-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3db0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3db0-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a3db0-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a3db0-144">**Remo**</span><span class="sxs-lookup"><span data-stu-id="a3db0-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a3db0-145">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="a3db0-145">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="a3db0-146">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="a3db0-146">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="a3db0-147">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="a3db0-147">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="a3db0-148">**glRotate**</span><span class="sxs-lookup"><span data-stu-id="a3db0-148">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="a3db0-149">**glScale**</span><span class="sxs-lookup"><span data-stu-id="a3db0-149">**glScale**</span></span>](glscale.md)
</dt> </dl>

 

 






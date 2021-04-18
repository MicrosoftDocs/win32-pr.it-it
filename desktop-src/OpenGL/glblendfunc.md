---
title: funzione glBlendFunc (GL. h)
description: La funzione glBlendFunc specifica l'aritmetica dei pixel.
ms.assetid: 6756774b-5eef-419a-a653-0b251aed65a0
keywords:
- funzione glBlendFunc OpenGL
topic_type:
- apiref
api_name:
- glBlendFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6300543bbf589c704da6d941bd743f693e0ed5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301801"
---
# <a name="glblendfunc-function"></a><span data-ttu-id="f05ad-104">glBlendFunc (funzione)</span><span class="sxs-lookup"><span data-stu-id="f05ad-104">glBlendFunc function</span></span>

<span data-ttu-id="f05ad-105">La funzione **glBlendFunc** specifica l'aritmetica dei pixel.</span><span class="sxs-lookup"><span data-stu-id="f05ad-105">The **glBlendFunc** function specifies pixel arithmetic.</span></span>

## <a name="syntax"></a><span data-ttu-id="f05ad-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f05ad-106">Syntax</span></span>


```C++
void WINAPI glBlendFunc(
   GLenum sfactor,
   GLenum dfactor
);
```



## <a name="parameters"></a><span data-ttu-id="f05ad-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f05ad-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f05ad-108">*sfactor*</span><span class="sxs-lookup"><span data-stu-id="f05ad-108">*sfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="f05ad-109">Specifica il modo in cui vengono calcolati i fattori di fusione del codice sorgente rosso, verde, blu e alfa.</span><span class="sxs-lookup"><span data-stu-id="f05ad-109">Specifies how the red, green, blue, and alpha source-blending factors are computed.</span></span> <span data-ttu-id="f05ad-110">Sono accettate nove costanti simboliche: GL \_ zero, GL \_ One, GL \_ DST \_ color, GL a \_ \_ meno \_ DST \_ color, GL \_ src \_ Alpha, GL \_ One \_ meno \_ src \_ Alpha, GL \_ DST Alpha, \_ GL \_ One \_ meno \_ DST \_ Alpha e GL \_ src \_ Alpha \_ satura.</span><span class="sxs-lookup"><span data-stu-id="f05ad-110">Nine symbolic constants are accepted: GL\_ZERO, GL\_ONE, GL\_DST\_COLOR, GL\_ONE\_MINUS\_DST\_COLOR, GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA, GL\_DST\_ALPHA, GL\_ONE\_MINUS\_DST\_ALPHA, and GL\_SRC\_ALPHA\_SATURATE.</span></span>

</dd> <dt>

<span data-ttu-id="f05ad-111">*dfactor*</span><span class="sxs-lookup"><span data-stu-id="f05ad-111">*dfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="f05ad-112">Specifica il modo in cui vengono calcolati i fattori di fusione di destinazione rosso, verde, blu e alfa.</span><span class="sxs-lookup"><span data-stu-id="f05ad-112">Specifies how the red, green, blue, and alpha destination-blending factors are computed.</span></span> <span data-ttu-id="f05ad-113">Sono accettate otto costanti simboliche: GL \_ zero, GL \_ One, GL \_ src \_ color, GL a \_ \_ meno \_ src \_ color, GL \_ src \_ Alpha, GL \_ One \_ meno \_ src \_ Alpha, GL \_ DST \_ Alpha e GL \_ 1 \_ meno \_ DST \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="f05ad-113">Eight symbolic constants are accepted: GL\_ZERO, GL\_ONE, GL\_SRC\_COLOR, GL\_ONE\_MINUS\_SRC\_COLOR, GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA, GL\_DST\_ALPHA, and GL\_ONE\_MINUS\_DST\_ALPHA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f05ad-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f05ad-114">Return value</span></span>

<span data-ttu-id="f05ad-115">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f05ad-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f05ad-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f05ad-116">Error codes</span></span>

<span data-ttu-id="f05ad-117">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="f05ad-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f05ad-118">Nome</span><span class="sxs-lookup"><span data-stu-id="f05ad-118">Name</span></span>                                                                                                  | <span data-ttu-id="f05ad-119">Significato</span><span class="sxs-lookup"><span data-stu-id="f05ad-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f05ad-120"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f05ad-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="f05ad-121">*Sfactor* o *dfactor* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="f05ad-121">Either *sfactor* or *dfactor* was not an accepted value.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="f05ad-122"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f05ad-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f05ad-123">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f05ad-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f05ad-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="f05ad-124">Remarks</span></span>

<span data-ttu-id="f05ad-125">In modalità RGB, i pixel possono essere disegnati usando una funzione che combina i valori RGBA in ingresso (di origine) con i valori RGBA già presenti nel framebuffer (valori di destinazione).</span><span class="sxs-lookup"><span data-stu-id="f05ad-125">In RGB mode, pixels can be drawn using a function that blends the incoming (source) RGBA values with the RGBA values that are already in the framebuffer (the destination values).</span></span> <span data-ttu-id="f05ad-126">Per impostazione predefinita, la fusione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="f05ad-126">By default, blending is disabled.</span></span> <span data-ttu-id="f05ad-127">Usare [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con l' \_ argomento di Blend GL per abilitare e disabilitare la fusione.</span><span class="sxs-lookup"><span data-stu-id="f05ad-127">Use [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the GL\_BLEND argument to enable and disable blending.</span></span>

<span data-ttu-id="f05ad-128">Se abilitata, **glBlendFunc** definisce l'operazione di fusione.</span><span class="sxs-lookup"><span data-stu-id="f05ad-128">When enabled, **glBlendFunc** defines the operation of blending.</span></span> <span data-ttu-id="f05ad-129">Il parametro *sfactor* specifica quale dei nove metodi viene usato per ridimensionare i componenti del colore di origine.</span><span class="sxs-lookup"><span data-stu-id="f05ad-129">The *sfactor* parameter specifies which of nine methods is used to scale the source color components.</span></span> <span data-ttu-id="f05ad-130">Il parametro *dfactor* specifica quale di otto metodi viene utilizzato per ridimensionare i componenti del colore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f05ad-130">The *dfactor* parameter specifies which of eight methods is used to scale the destination color components.</span></span> <span data-ttu-id="f05ad-131">Nella tabella seguente sono descritti gli undici metodi possibili.</span><span class="sxs-lookup"><span data-stu-id="f05ad-131">The eleven possible methods are described in the following table.</span></span> <span data-ttu-id="f05ad-132">Ogni metodo definisce quattro fattori di scala ognuno per rosso, verde, blu e alfa.</span><span class="sxs-lookup"><span data-stu-id="f05ad-132">Each method defines four scale factors one each for red, green, blue, and alpha.</span></span>

<span data-ttu-id="f05ad-133">Nella tabella e nelle equazioni successive, i componenti dei colori di origine e di destinazione sono detti (*R*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-133">In the table and in subsequent equations, source and destination color components are referred to as (*R*?</span></span> <span data-ttu-id="f05ad-134">, *G*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-134">, *G*?</span></span> <span data-ttu-id="f05ad-135">, *B*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-135">, *B*?</span></span> <span data-ttu-id="f05ad-136">, *A*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-136">, *A*?</span></span> <span data-ttu-id="f05ad-137">) e (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ).</span><span class="sxs-lookup"><span data-stu-id="f05ad-137">) and (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ).</span></span> <span data-ttu-id="f05ad-138">Hanno valori integer compresi tra zero e (*k*<sub>r</sub> , *k*<sub>G</sub> , *k*<sub>r</sub> , *k*<sub>a</sub> ), dove</span><span class="sxs-lookup"><span data-stu-id="f05ad-138">They are understood to have integer values between zero and (*k*<sub>R</sub> , *k*<sub>G</sub> , *k*<sub>R</sub> , *k*<sub>A</sub> ), where</span></span>

<span data-ttu-id="f05ad-139">*k*<sub>r</sub> = 2 <sup>m</sup>*r* -1</span><span class="sxs-lookup"><span data-stu-id="f05ad-139">*k*<sub>R</sub> = 2 <sup>m</sup>*R* - 1</span></span>

<span data-ttu-id="f05ad-140">*k*<sub>g</sub> = 2 <sup>m</sup>*g* -1</span><span class="sxs-lookup"><span data-stu-id="f05ad-140">*k*<sub>G</sub> = 2 <sup>m</sup>*G* - 1</span></span>

<span data-ttu-id="f05ad-141">*k*<sub>b</sub> = 2 <sup>m</sup>*b* -1</span><span class="sxs-lookup"><span data-stu-id="f05ad-141">*k*<sub>B</sub> = 2 <sup>m</sup>*B* - 1</span></span>

<span data-ttu-id="f05ad-142">*k*<sub>a</sub> = 2 <sup>m</sup>*a* -1</span><span class="sxs-lookup"><span data-stu-id="f05ad-142">*k*<sub>A</sub> = 2 <sup>m</sup>*A* - 1</span></span>

<span data-ttu-id="f05ad-143">e (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>A</sub> ) è il numero di bitplane rosso, verde, blu e alfa.</span><span class="sxs-lookup"><span data-stu-id="f05ad-143">and (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>A</sub> ) is the number of red, green, blue, and alpha bitplanes.</span></span>

<span data-ttu-id="f05ad-144">I fattori di scala di origine e di destinazione sono detti (*s*<sub>R</sub> , *s*<sub>G</sub> , *s*<sub>B</sub> , *s*<sub>A</sub> ) e (*d*<sub>R</sub> , *d*<sub>G</sub> , *d*<sub>B</sub> , *d*<sub>A</sub> ).</span><span class="sxs-lookup"><span data-stu-id="f05ad-144">Source and destination scale factors are referred to as (*s*<sub>R</sub> , *s*<sub>G</sub> , *s*<sub>B</sub> , *s*<sub>A</sub> ) and (*d*<sub>R</sub> , *d*<sub>G</sub> , *d*<sub>B</sub> , *d*<sub>A</sub> ).</span></span> <span data-ttu-id="f05ad-145">I fattori di scala descritti nella tabella, denotati (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ), rappresentano i fattori di origine o di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f05ad-145">The scale factors described in the table, denoted (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ), represent either source or destination factors.</span></span> <span data-ttu-id="f05ad-146">Tutti i fattori di scala hanno un intervallo compreso tra \[ 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="f05ad-146">All scale factors have range \[0,1\].</span></span>



| <span data-ttu-id="f05ad-147">Parametro</span><span class="sxs-lookup"><span data-stu-id="f05ad-147">Parameter</span></span>                  | <span data-ttu-id="f05ad-148">(*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )</span><span class="sxs-lookup"><span data-stu-id="f05ad-148">(*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )</span></span>                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f05ad-149">\_zero GL</span><span class="sxs-lookup"><span data-stu-id="f05ad-149">GL\_ZERO</span></span>                   | <span data-ttu-id="f05ad-150">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="f05ad-150">(0,0,0,0)</span></span>                                                                                                                                                    |
| <span data-ttu-id="f05ad-151">GL \_ uno</span><span class="sxs-lookup"><span data-stu-id="f05ad-151">GL\_ONE</span></span>                    | <span data-ttu-id="f05ad-152">(1, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="f05ad-152">(1,1,1,1)</span></span>                                                                                                                                                    |
| <span data-ttu-id="f05ad-153">\_colore GL src \_</span><span class="sxs-lookup"><span data-stu-id="f05ad-153">GL\_SRC\_COLOR</span></span>             | <span data-ttu-id="f05ad-154">(*R*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-154">(*R*?</span></span><span data-ttu-id="f05ad-155"> / *k*<sub>R</sub> , *G*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-155"> / *k*<sub>R</sub> , *G*?</span></span><span data-ttu-id="f05ad-156"> / *k*<sub>G</sub> , *B*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-156"> / *k*<sub>G</sub> , *B*?</span></span><span data-ttu-id="f05ad-157"> / *k*<sub>B</sub> , *A*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-157"> / *k*<sub>B</sub> , *A*?</span></span><span data-ttu-id="f05ad-158"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="f05ad-158"> / *k*<sub>A</sub> )</span></span>                                                         |
| <span data-ttu-id="f05ad-159">GL \_ uno \_ meno \_ il \_ colore src</span><span class="sxs-lookup"><span data-stu-id="f05ad-159">GL\_ONE\_MINUS\_SRC\_COLOR</span></span> | <span data-ttu-id="f05ad-160">(1, 1, 1, 1)-(*R*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-160">(1,1,1,1) - (*R*?</span></span><span data-ttu-id="f05ad-161"> / *k*<sub>R</sub> , *G*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-161"> / *k*<sub>R</sub> , *G*?</span></span><span data-ttu-id="f05ad-162"> / *k*<sub>G</sub> , *B*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-162"> / *k*<sub>G</sub> , *B*?</span></span><span data-ttu-id="f05ad-163"> / *k*<sub>B</sub> , *A*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-163"> / *k*<sub>B</sub> , *A*?</span></span><span data-ttu-id="f05ad-164"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="f05ad-164"> / *k*<sub>A</sub> )</span></span>                                             |
| <span data-ttu-id="f05ad-165">\_colore GL DST \_</span><span class="sxs-lookup"><span data-stu-id="f05ad-165">GL\_DST\_COLOR</span></span>             | <span data-ttu-id="f05ad-166">(*R*<sub>d</sub>  /  *k*<sub>R</sub> , *g*<sub>d</sub>  /  *k*<sub>g</sub> , *b*<sub>d</sub>  /  *k*<sub>b</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="f05ad-166">(*R*<sub>d</sub> / *k*<sub>R</sub> , *G*<sub>d</sub> / *k*<sub>G</sub> , *B*<sub>d</sub> / *k*<sub>B</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span>             |
| <span data-ttu-id="f05ad-167">GL \_ uno \_ meno \_ il \_ colore DST</span><span class="sxs-lookup"><span data-stu-id="f05ad-167">GL\_ONE\_MINUS\_DST\_COLOR</span></span> | <span data-ttu-id="f05ad-168">(1, 1, 1, 1)-(*r*<sub>d</sub>  /  *k*<sub>r</sub> , *g*<sub>d</sub>  /  *k*<sub>g</sub> , *b*<sub>d</sub>  /  *k*<sub>b</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="f05ad-168">(1,1,1,1) - (*R*<sub>d</sub> / *k*<sub>R</sub> , *G*<sub>d</sub> / *k*<sub>G</sub> , *B*<sub>d</sub> / *k*<sub>B</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span> |
| <span data-ttu-id="f05ad-169">\_alfa src \_ GL</span><span class="sxs-lookup"><span data-stu-id="f05ad-169">GL\_SRC\_ALPHA</span></span>             | <span data-ttu-id="f05ad-170">(*A*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-170">(*A*?</span></span><span data-ttu-id="f05ad-171"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-171"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="f05ad-172"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-172"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="f05ad-173"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-173"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="f05ad-174"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="f05ad-174"> / *k*<sub>A</sub> )</span></span>                                                         |
| <span data-ttu-id="f05ad-175">GL \_ 1 \_ meno \_ src \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="f05ad-175">GL\_ONE\_MINUS\_SRC\_ALPHA</span></span> | <span data-ttu-id="f05ad-176">(1, 1, 1, 1)-(*A*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-176">(1,1,1,1) - (*A*?</span></span><span data-ttu-id="f05ad-177"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-177"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="f05ad-178"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-178"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="f05ad-179"> / *k*<sub>a</sub> , *a*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-179"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="f05ad-180"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="f05ad-180"> / *k*<sub>A</sub> )</span></span>                                             |
| <span data-ttu-id="f05ad-181">\_alfa del DST GL \_</span><span class="sxs-lookup"><span data-stu-id="f05ad-181">GL\_DST\_ALPHA</span></span>             | <span data-ttu-id="f05ad-182">(*A*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="f05ad-182">(*A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span>             |
| <span data-ttu-id="f05ad-183">GL \_ 1 \_ meno \_ DST \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="f05ad-183">GL\_ONE\_MINUS\_DST\_ALPHA</span></span> | <span data-ttu-id="f05ad-184">(1, 1, 1, 1)-(*a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="f05ad-184">(1,1,1,1) - (*A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span> |
| <span data-ttu-id="f05ad-185">\_ \_ satura Alpha di GL src \_</span><span class="sxs-lookup"><span data-stu-id="f05ad-185">GL\_SRC\_ALPHA\_SATURATE</span></span>   | <span data-ttu-id="f05ad-186">(*i, i, i,* 1)</span><span class="sxs-lookup"><span data-stu-id="f05ad-186">(*i,i,i,* 1)</span></span>                                                                                                                                                 |



 

<span data-ttu-id="f05ad-187">Nella tabella,</span><span class="sxs-lookup"><span data-stu-id="f05ad-187">In the table,</span></span>

<span data-ttu-id="f05ad-188">*i* = min (*A*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-188">*i* = min (*A*?</span></span> <span data-ttu-id="f05ad-189">, *k*<sub>a</sub>   -  *a*<sub>d</sub> )/ *k*<sub>a</sub></span><span class="sxs-lookup"><span data-stu-id="f05ad-189">, *k*<sub>A</sub>  - *A*<sub>d</sub> ) / *k*<sub>A</sub></span></span>

<span data-ttu-id="f05ad-190">Per determinare i valori RGBA di Blend di un pixel durante il disegno in modalità RGBA, il sistema usa le equazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f05ad-190">To determine the blended RGBA values of a pixel when drawing in RGBA mode, the system uses the following equations:</span></span>

<span data-ttu-id="f05ad-191">*R* (*d*) = min ( *k*<sub>r</sub> , *r*? *s*<sub>r</sub>  +  *r*<sub>d</sub> *d*<sub>r</sub> )</span><span class="sxs-lookup"><span data-stu-id="f05ad-191">*R* (*d*) = min( *k*<sub>R</sub> , *R*? *s*<sub>R</sub> + *R*<sub>d</sub> *d*<sub>R</sub> )</span></span>

<span data-ttu-id="f05ad-192">*G* (*d*) = min ( *k*<sub>g</sub> , *g*? *s*<sub>g</sub>  +  *g*<sub>d</sub> <sub>g</sub> )</span><span class="sxs-lookup"><span data-stu-id="f05ad-192">*G* (*d*) = min( *k*<sub>G</sub> , *G*? *s*<sub>G</sub> + *G*<sub>d</sub> *d*<sub>G</sub>  )</span></span>

<span data-ttu-id="f05ad-193">*B* (*d*) = min ( *k*<sub>b</sub> *, b*? *s*<sub>b</sub>  +  *b*<sub>d</sub> *d*<sub>b</sub> )</span><span class="sxs-lookup"><span data-stu-id="f05ad-193">*B* (*d*) = min( *k*<sub>B</sub> *, B*? *s*<sub>B</sub> + *B*<sub>d</sub> *d*<sub>B</sub>  )</span></span>

<span data-ttu-id="f05ad-194">*A* (*d*) = min ( *k*<sub>a</sub> , *a*? *s*<sub>a</sub>  +  <sub>d</sub> *d*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="f05ad-194">*A* (*d*) = min( *k*<sub>A</sub> , *A*? *s*<sub>A</sub> + *A*<sub>d</sub> *d*<sub>A</sub>  )</span></span>

<span data-ttu-id="f05ad-195">Nonostante la precisione apparente delle equazioni precedenti, la fusione aritmetica non è esattamente specificata, perché la fusione opera con valori di colore integer imprecisi.</span><span class="sxs-lookup"><span data-stu-id="f05ad-195">Despite the apparent precision of the above equations, blending arithmetic is not exactly specified, because blending operates with imprecise integer color values.</span></span> <span data-ttu-id="f05ad-196">Tuttavia, un fattore di Blend che deve essere uguale a uno non modifica la relativa multiplicand e un fattore di fusione uguale a zero riduce il multiplicand a zero.</span><span class="sxs-lookup"><span data-stu-id="f05ad-196">However, a blend factor that should be equal to one is guaranteed not to modify its multiplicand, and a blend factor equal to zero reduces its multiplicand to zero.</span></span> <span data-ttu-id="f05ad-197">Pertanto, ad esempio, quando *sfactor* è GL \_ src \_ Alpha, *dfactor* è GL \_ One \_ meno \_ src \_ Alpha e *a*? è uguale a *k*<sub>a</sub>, le equazioni riducono alla sostituzione semplice:</span><span class="sxs-lookup"><span data-stu-id="f05ad-197">Thus, for example, when *sfactor* is GL\_SRC\_ALPHA, *dfactor* is GL\_ONE\_MINUS\_SRC\_ALPHA, and *A*? is equal to *k*<sub>A</sub>, the equations reduce to simple replacement:</span></span>

<span data-ttu-id="f05ad-198">*R*<sub>d</sub>  =  *r*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-198">*R*<sub>d</sub> = *R*?</span></span>

<span data-ttu-id="f05ad-199">*G*<sub>d</sub>  =  *g*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-199">*G*<sub>d</sub> = *G*?</span></span>

<span data-ttu-id="f05ad-200">B <sub>d</sub>  =  *b*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-200">B <sub>d</sub> = *B*?</span></span>

<span data-ttu-id="f05ad-201"><sub>D</sub>  =  *a*?</span><span class="sxs-lookup"><span data-stu-id="f05ad-201">*A*<sub>d</sub> = *A*?</span></span>

## <a name="examples"></a><span data-ttu-id="f05ad-202">Esempio</span><span class="sxs-lookup"><span data-stu-id="f05ad-202">Examples</span></span>

<span data-ttu-id="f05ad-203">La trasparenza è implementata in modo ottimale usando **glBlendFunc**(GL \_ src \_ Alpha, GL \_ One \_ meno \_ src \_ Alpha) con primitive ordinate dal più lontano al più vicino.</span><span class="sxs-lookup"><span data-stu-id="f05ad-203">Transparency is best implemented using **glBlendFunc**(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) with primitives sorted from farthest to nearest.</span></span> <span data-ttu-id="f05ad-204">Si noti che questo calcolo della trasparenza non richiede la presenza di Alpha bitplane nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="f05ad-204">Note that this transparency calculation does not require the presence of alpha bitplanes in the framebuffer.</span></span>

<span data-ttu-id="f05ad-205">È anche possibile usare **glBlendFunc**(GL \_ src \_ Alpha, GL \_ One \_ meno \_ src \_ Alpha) per il rendering di punti e righe con antialias in ordine arbitrario.</span><span class="sxs-lookup"><span data-stu-id="f05ad-205">You can also use **glBlendFunc**(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) for rendering antialiased points and lines in arbitrary order.</span></span>

<span data-ttu-id="f05ad-206">Per ottimizzare l'anti-aliasing poligono, usare **glBlendFunc**(GL \_ src \_ Alpha \_ saturate, GL \_ One) con poligoni ordinati dal più vicino al più lontano.</span><span class="sxs-lookup"><span data-stu-id="f05ad-206">To optimize polygon antialiasing, use **glBlendFunc**(GL\_SRC\_ALPHA\_SATURATE, GL\_ONE) with polygons sorted from nearest to farthest.</span></span> <span data-ttu-id="f05ad-207">(Vedere GL \_ \_Argomento smussato del poligono in [**glenble**](glenable.md) per informazioni sull'anti-aliasing del poligono. Bitplane alfa di destinazione, che deve essere presente affinché questa funzione di Blend funzioni correttamente, archiviare la copertura accumulata.</span><span class="sxs-lookup"><span data-stu-id="f05ad-207">(See the GL\_POLYGON\_SMOOTH argument in [**glEnable**](glenable.md) for information on polygon antialiasing.) Destination alpha bitplanes, which must be present for this blend function to operate correctly, store the accumulated coverage.</span></span>

<span data-ttu-id="f05ad-208">In ingresso (origine) Alfa è un'opacità del materiale, che va da 1,0 (*K*<sub>a</sub> ), che rappresenta l'opacità completa, a 0,0 (0), che rappresenta la trasparenza completa.</span><span class="sxs-lookup"><span data-stu-id="f05ad-208">Incoming (source) alpha is a material opacity, ranging from 1.0 (*K*<sub>A</sub> ), representing complete opacity, to 0.0 (0), representing complete transparency.</span></span>

<span data-ttu-id="f05ad-209">Quando si Abilita più di un buffer di colore per il disegno, ogni buffer abilitato viene mescolato separatamente e il contenuto del buffer viene utilizzato per il colore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f05ad-209">When you enable more than one color buffer for drawing, each enabled buffer is blended separately, and the contents of the buffer is used for destination color.</span></span> <span data-ttu-id="f05ad-210">Vedere [**glDrawBuffer**](gldrawbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="f05ad-210">(See [**glDrawBuffer**](gldrawbuffer.md).)</span></span>

<span data-ttu-id="f05ad-211">La fusione ha effetto solo sul rendering RGBA.</span><span class="sxs-lookup"><span data-stu-id="f05ad-211">Blending affects only RGBA rendering.</span></span> <span data-ttu-id="f05ad-212">Viene ignorato dai renderer di indice dei colori.</span><span class="sxs-lookup"><span data-stu-id="f05ad-212">It is ignored by color-index renderers.</span></span>

<span data-ttu-id="f05ad-213">Le funzioni seguenti consentono di recuperare informazioni correlate a **glBlendFunc**:</span><span class="sxs-lookup"><span data-stu-id="f05ad-213">The following functions retrieve information related to **glBlendFunc**:</span></span>

<span data-ttu-id="f05ad-214">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Blend \_ src</span><span class="sxs-lookup"><span data-stu-id="f05ad-214">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_BLEND\_SRC</span></span>

<span data-ttu-id="f05ad-215">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Blend \_ DST</span><span class="sxs-lookup"><span data-stu-id="f05ad-215">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_BLEND\_DST</span></span>

<span data-ttu-id="f05ad-216">[**glIsEnabled**](glisenabled.md) con argument GL \_ Blend</span><span class="sxs-lookup"><span data-stu-id="f05ad-216">[**glIsEnabled**](glisenabled.md) with argument GL\_BLEND</span></span>

## <a name="requirements"></a><span data-ttu-id="f05ad-217">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f05ad-217">Requirements</span></span>



| <span data-ttu-id="f05ad-218">Requisito</span><span class="sxs-lookup"><span data-stu-id="f05ad-218">Requirement</span></span> | <span data-ttu-id="f05ad-219">Valore</span><span class="sxs-lookup"><span data-stu-id="f05ad-219">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f05ad-220">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f05ad-220">Minimum supported client</span></span><br/> | <span data-ttu-id="f05ad-221">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f05ad-221">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f05ad-222">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f05ad-222">Minimum supported server</span></span><br/> | <span data-ttu-id="f05ad-223">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f05ad-223">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f05ad-224">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f05ad-224">Header</span></span><br/>                   | <dl> <span data-ttu-id="f05ad-225"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f05ad-225"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f05ad-226">Libreria</span><span class="sxs-lookup"><span data-stu-id="f05ad-226">Library</span></span><br/>                  | <dl> <span data-ttu-id="f05ad-227"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f05ad-227"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f05ad-228">DLL</span><span class="sxs-lookup"><span data-stu-id="f05ad-228">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f05ad-229"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f05ad-229"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f05ad-230">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f05ad-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f05ad-231">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="f05ad-231">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="f05ad-232">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f05ad-232">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f05ad-233">**glClear**</span><span class="sxs-lookup"><span data-stu-id="f05ad-233">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="f05ad-234">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="f05ad-234">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="f05ad-235">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="f05ad-235">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="f05ad-236">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="f05ad-236">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="f05ad-237">**glGet**</span><span class="sxs-lookup"><span data-stu-id="f05ad-237">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="f05ad-238">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="f05ad-238">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="f05ad-239">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="f05ad-239">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="f05ad-240">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="f05ad-240">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 






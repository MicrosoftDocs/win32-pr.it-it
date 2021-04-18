---
title: funzione glColor3i (GL. h)
description: Imposta il colore corrente. | funzione glColor3i (GL. h)
ms.assetid: 9c68221b-1633-435b-9ae4-abc1c52601aa
keywords:
- funzione glColor3i OpenGL
topic_type:
- apiref
api_name:
- glColor3i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6bb94421d44f7aed14c793c0f95d7b6467d7e38
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321941"
---
# <a name="glcolor3i-function"></a><span data-ttu-id="cd00b-105">glColor3i (funzione)</span><span class="sxs-lookup"><span data-stu-id="cd00b-105">glColor3i function</span></span>

<span data-ttu-id="cd00b-106">Imposta il colore corrente.</span><span class="sxs-lookup"><span data-stu-id="cd00b-106">Sets the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd00b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd00b-107">Syntax</span></span>


```C++
void WINAPI glColor3i(
   GLint red,
   GLint green,
   GLint blue
);
```



## <a name="parameters"></a><span data-ttu-id="cd00b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd00b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd00b-109">*Red*</span><span class="sxs-lookup"><span data-stu-id="cd00b-109">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="cd00b-110">Nuovo valore rosso per il colore corrente.</span><span class="sxs-lookup"><span data-stu-id="cd00b-110">The new red value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="cd00b-111">*verde*</span><span class="sxs-lookup"><span data-stu-id="cd00b-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="cd00b-112">Nuovo valore verde per il colore corrente.</span><span class="sxs-lookup"><span data-stu-id="cd00b-112">The new green value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="cd00b-113">*blu*</span><span class="sxs-lookup"><span data-stu-id="cd00b-113">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="cd00b-114">Nuovo valore blu per il colore corrente.</span><span class="sxs-lookup"><span data-stu-id="cd00b-114">The new blue value for the current color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd00b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd00b-115">Return value</span></span>

<span data-ttu-id="cd00b-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="cd00b-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd00b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd00b-117">Remarks</span></span>

<span data-ttu-id="cd00b-118">GL archivia sia un indice dei colori a valore singolo corrente sia un colore corrente RGBA a quattro valori.</span><span class="sxs-lookup"><span data-stu-id="cd00b-118">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="cd00b-119">**glcolor** imposta un nuovo colore RGBA a quattro valori.</span><span class="sxs-lookup"><span data-stu-id="cd00b-119">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="cd00b-120">**glcolor** presenta due varianti principali: **glcolor3** e **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="cd00b-120">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="cd00b-121">le varianti **glcolor3** specificano i nuovi valori rosso, verde e blu in modo esplicito e impostano in modo implicito il valore alfa corrente su 1,0 (intensità completa).</span><span class="sxs-lookup"><span data-stu-id="cd00b-121">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="cd00b-122">le varianti **glcolor4** specificano tutti e quattro i componenti colore in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="cd00b-122">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="cd00b-123">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** e **glcolor4i** accettano gli Integer a tre o quattro byte con segno, short o long come argomenti.</span><span class="sxs-lookup"><span data-stu-id="cd00b-123">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="cd00b-124">Quando v viene aggiunto al nome, i comandi color possono assumere un puntatore a una matrice di tali valori.</span><span class="sxs-lookup"><span data-stu-id="cd00b-124">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="cd00b-125">I valori dei colori correnti vengono archiviati in formato a virgola mobile, con dimensioni mantissa e esponenti non specificate.</span><span class="sxs-lookup"><span data-stu-id="cd00b-125">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="cd00b-126">I componenti dei colori integer senza segno, se specificati, vengono mappati in modo lineare ai valori a virgola mobile in modo che il valore rappresentabile più grande sia mappato a 1,0 (intensità completa) e 0 sia mappato a 0,0 (intensità zero).</span><span class="sxs-lookup"><span data-stu-id="cd00b-126">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="cd00b-127">I componenti di colore integer con segno, se specificati, vengono mappati in modo lineare ai valori a virgola mobile in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo sia mappato a-1,0.</span><span class="sxs-lookup"><span data-stu-id="cd00b-127">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="cd00b-128">Si noti che questo mapping non converte 0 esattamente in 0,0. Ai valori a virgola mobile viene eseguito il mapping diretto.</span><span class="sxs-lookup"><span data-stu-id="cd00b-128">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="cd00b-129">Nessun valore a virgola mobile né Signed Integer viene fissato all'intervallo \[ 0, 1 \] prima che venga aggiornato il colore corrente.</span><span class="sxs-lookup"><span data-stu-id="cd00b-129">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="cd00b-130">Tuttavia, i componenti dei colori vengono fissati a questo intervallo prima che vengano interpolati o scritti in un buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="cd00b-130">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd00b-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd00b-131">Requirements</span></span>



| <span data-ttu-id="cd00b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd00b-132">Requirement</span></span> | <span data-ttu-id="cd00b-133">Valore</span><span class="sxs-lookup"><span data-stu-id="cd00b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd00b-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd00b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cd00b-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd00b-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cd00b-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd00b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cd00b-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd00b-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cd00b-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd00b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd00b-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd00b-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cd00b-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="cd00b-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="cd00b-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd00b-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cd00b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="cd00b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd00b-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd00b-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd00b-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd00b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd00b-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cd00b-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cd00b-146">**Remo**</span><span class="sxs-lookup"><span data-stu-id="cd00b-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cd00b-147">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="cd00b-147">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="cd00b-148">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="cd00b-148">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 






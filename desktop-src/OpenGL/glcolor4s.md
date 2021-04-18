---
title: funzione glColor4s (GL. h)
description: Imposta il colore corrente. | funzione glColor4s (GL. h)
ms.assetid: a942e308-8507-4afe-8941-2b9c7e39bb3d
keywords:
- funzione glColor4s OpenGL
topic_type:
- apiref
api_name:
- glColor4s
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd942f8f3bd94323ec37c531047715dd50133474
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321681"
---
# <a name="glcolor4s-function"></a><span data-ttu-id="383ce-105">glColor4s (funzione)</span><span class="sxs-lookup"><span data-stu-id="383ce-105">glColor4s function</span></span>

<span data-ttu-id="383ce-106">Imposta il colore corrente.</span><span class="sxs-lookup"><span data-stu-id="383ce-106">Sets the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="383ce-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="383ce-107">Syntax</span></span>


```C++
void WINAPI glColor4s(
   GLshort red,
   GLshort green,
   GLshort blue,
   GLshort alpha
);
```



## <a name="parameters"></a><span data-ttu-id="383ce-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="383ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="383ce-109">*Red*</span><span class="sxs-lookup"><span data-stu-id="383ce-109">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="383ce-110">Nuovo valore rosso per il colore corrente.</span><span class="sxs-lookup"><span data-stu-id="383ce-110">The new red value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="383ce-111">*verde*</span><span class="sxs-lookup"><span data-stu-id="383ce-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="383ce-112">Nuovo valore verde per il colore corrente.</span><span class="sxs-lookup"><span data-stu-id="383ce-112">The new green value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="383ce-113">*blu*</span><span class="sxs-lookup"><span data-stu-id="383ce-113">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="383ce-114">Nuovo valore blu per il colore corrente.</span><span class="sxs-lookup"><span data-stu-id="383ce-114">The new blue value for the current color.</span></span>

</dd> <dt>

<span data-ttu-id="383ce-115">*Alfa*</span><span class="sxs-lookup"><span data-stu-id="383ce-115">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="383ce-116">Nuovo valore alfa per il colore corrente.</span><span class="sxs-lookup"><span data-stu-id="383ce-116">The new alpha value for the current color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="383ce-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="383ce-117">Return value</span></span>

<span data-ttu-id="383ce-118">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="383ce-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="383ce-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="383ce-119">Remarks</span></span>

<span data-ttu-id="383ce-120">GL archivia sia un indice dei colori a valore singolo corrente sia un colore corrente RGBA a quattro valori.</span><span class="sxs-lookup"><span data-stu-id="383ce-120">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="383ce-121">**glcolor** imposta un nuovo colore RGBA a quattro valori.</span><span class="sxs-lookup"><span data-stu-id="383ce-121">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="383ce-122">**glcolor** presenta due varianti principali: **glcolor3** e **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="383ce-122">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="383ce-123">le varianti **glcolor3** specificano i nuovi valori rosso, verde e blu in modo esplicito e impostano in modo implicito il valore alfa corrente su 1,0 (intensità completa).</span><span class="sxs-lookup"><span data-stu-id="383ce-123">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="383ce-124">le varianti **glcolor4** specificano tutti e quattro i componenti colore in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="383ce-124">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="383ce-125">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** e **glcolor4i** accettano gli Integer a tre o quattro byte con segno, short o long come argomenti.</span><span class="sxs-lookup"><span data-stu-id="383ce-125">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="383ce-126">Quando v viene aggiunto al nome, i comandi color possono assumere un puntatore a una matrice di tali valori.</span><span class="sxs-lookup"><span data-stu-id="383ce-126">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="383ce-127">I valori dei colori correnti vengono archiviati in formato a virgola mobile, con dimensioni mantissa e esponenti non specificate.</span><span class="sxs-lookup"><span data-stu-id="383ce-127">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="383ce-128">I componenti dei colori integer senza segno, se specificati, vengono mappati in modo lineare ai valori a virgola mobile in modo che il valore rappresentabile più grande sia mappato a 1,0 (intensità completa) e 0 sia mappato a 0,0 (intensità zero).</span><span class="sxs-lookup"><span data-stu-id="383ce-128">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="383ce-129">I componenti di colore integer con segno, se specificati, vengono mappati in modo lineare ai valori a virgola mobile in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo sia mappato a-1,0.</span><span class="sxs-lookup"><span data-stu-id="383ce-129">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="383ce-130">Si noti che questo mapping non converte 0 esattamente in 0,0. Ai valori a virgola mobile viene eseguito il mapping diretto.</span><span class="sxs-lookup"><span data-stu-id="383ce-130">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="383ce-131">Nessun valore a virgola mobile né Signed Integer viene fissato all'intervallo \[ 0, 1 \] prima che venga aggiornato il colore corrente.</span><span class="sxs-lookup"><span data-stu-id="383ce-131">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="383ce-132">Tuttavia, i componenti dei colori vengono fissati a questo intervallo prima che vengano interpolati o scritti in un buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="383ce-132">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="383ce-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="383ce-133">Requirements</span></span>



| <span data-ttu-id="383ce-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="383ce-134">Requirement</span></span> | <span data-ttu-id="383ce-135">Valore</span><span class="sxs-lookup"><span data-stu-id="383ce-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="383ce-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="383ce-136">Minimum supported client</span></span><br/> | <span data-ttu-id="383ce-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="383ce-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="383ce-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="383ce-138">Minimum supported server</span></span><br/> | <span data-ttu-id="383ce-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="383ce-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="383ce-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="383ce-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="383ce-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="383ce-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="383ce-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="383ce-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="383ce-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="383ce-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="383ce-144">DLL</span><span class="sxs-lookup"><span data-stu-id="383ce-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="383ce-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="383ce-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="383ce-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="383ce-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="383ce-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="383ce-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="383ce-148">**Remo**</span><span class="sxs-lookup"><span data-stu-id="383ce-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="383ce-149">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="383ce-149">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="383ce-150">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="383ce-150">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 






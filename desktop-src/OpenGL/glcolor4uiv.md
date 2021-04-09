---
title: funzione glColor4uiv (GL. h)
description: Imposta il colore corrente da una matrice di valori di colore già esistente. | funzione glColor4uiv (GL. h)
ms.assetid: de21116b-50f6-4a80-8fa1-e8cf6e4978e9
keywords:
- funzione glColor4uiv OpenGL
topic_type:
- apiref
api_name:
- glColor4uiv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acc9a413436b4d6b6fad4ca175aa74821ad2dbe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969048"
---
# <a name="glcolor4uiv-function"></a><span data-ttu-id="a8280-105">glColor4uiv (funzione)</span><span class="sxs-lookup"><span data-stu-id="a8280-105">glColor4uiv function</span></span>

<span data-ttu-id="a8280-106">Imposta il colore corrente da una matrice di valori di colore già esistente.</span><span class="sxs-lookup"><span data-stu-id="a8280-106">Sets the current color from an already existing array of color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8280-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8280-107">Syntax</span></span>


```C++
void WINAPI glColor4uiv(
   const GLuint *v
);
```



## <a name="parameters"></a><span data-ttu-id="a8280-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8280-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8280-109">*v*</span><span class="sxs-lookup"><span data-stu-id="a8280-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="a8280-110">Puntatore a una matrice che contiene i valori rosso, verde, blu e alfa.</span><span class="sxs-lookup"><span data-stu-id="a8280-110">A pointer to an array that contains red, green, blue, and alpha values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8280-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8280-111">Return value</span></span>

<span data-ttu-id="a8280-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a8280-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8280-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8280-113">Remarks</span></span>

<span data-ttu-id="a8280-114">GL archivia sia un indice dei colori a valore singolo corrente sia un colore corrente RGBA a quattro valori.</span><span class="sxs-lookup"><span data-stu-id="a8280-114">The GL stores both a current single-valued color index and a current four-valued RGBA color.</span></span> <span data-ttu-id="a8280-115">**glcolor** imposta un nuovo colore RGBA a quattro valori.</span><span class="sxs-lookup"><span data-stu-id="a8280-115">**glcolor** sets a new four-valued RGBA color.</span></span> <span data-ttu-id="a8280-116">**glcolor** presenta due varianti principali: **glcolor3** e **glcolor4**.</span><span class="sxs-lookup"><span data-stu-id="a8280-116">**glcolor** has two major variants: **glcolor3** and **glcolor4**.</span></span> <span data-ttu-id="a8280-117">le varianti **glcolor3** specificano i nuovi valori rosso, verde e blu in modo esplicito e impostano in modo implicito il valore alfa corrente su 1,0 (intensità completa).</span><span class="sxs-lookup"><span data-stu-id="a8280-117">**glcolor3** variants specify new red, green, and blue values explicitly and set the current alpha value to 1.0 (full intensity) implicitly.</span></span> <span data-ttu-id="a8280-118">le varianti **glcolor4** specificano tutti e quattro i componenti colore in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="a8280-118">**glcolor4** variants specify all four color components explicitly.</span></span>

<span data-ttu-id="a8280-119">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** e **glcolor4i** accettano gli Integer a tre o quattro byte con segno, short o long come argomenti.</span><span class="sxs-lookup"><span data-stu-id="a8280-119">**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i**, and **glcolor4i** take three or four signed byte, short, or long integers as arguments.</span></span> <span data-ttu-id="a8280-120">Quando v viene aggiunto al nome, i comandi color possono assumere un puntatore a una matrice di tali valori.</span><span class="sxs-lookup"><span data-stu-id="a8280-120">When v is appended to the name, the color commands can take a pointer to an array of such values.</span></span>

<span data-ttu-id="a8280-121">I valori dei colori correnti vengono archiviati in formato a virgola mobile, con dimensioni mantissa e esponenti non specificate.</span><span class="sxs-lookup"><span data-stu-id="a8280-121">Current color values are stored in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="a8280-122">I componenti dei colori integer senza segno, se specificati, vengono mappati in modo lineare ai valori a virgola mobile in modo che il valore rappresentabile più grande sia mappato a 1,0 (intensità completa) e 0 sia mappato a 0,0 (intensità zero).</span><span class="sxs-lookup"><span data-stu-id="a8280-122">Unsigned integer color components, when specified, are linearly mapped to floating-point values such that the largest representable value maps to 1.0 (full intensity), and 0 maps to 0.0 (zero intensity).</span></span> <span data-ttu-id="a8280-123">I componenti di colore integer con segno, se specificati, vengono mappati in modo lineare ai valori a virgola mobile in modo che il valore rappresentabile più positivo sia mappato a 1,0 e il valore rappresentabile più negativo sia mappato a-1,0.</span><span class="sxs-lookup"><span data-stu-id="a8280-123">Signed integer color components, when specified, are linearly mapped to floating-point values such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="a8280-124">Si noti che questo mapping non converte 0 esattamente in 0,0. Ai valori a virgola mobile viene eseguito il mapping diretto.</span><span class="sxs-lookup"><span data-stu-id="a8280-124">(Note that this mapping does not convert 0 precisely to 0.0.) Floating-point values are mapped directly.</span></span>

<span data-ttu-id="a8280-125">Nessun valore a virgola mobile né Signed Integer viene fissato all'intervallo \[ 0, 1 \] prima che venga aggiornato il colore corrente.</span><span class="sxs-lookup"><span data-stu-id="a8280-125">Neither floating-point nor signed integer values are clamped to the range \[0,1\] before the current color is updated.</span></span> <span data-ttu-id="a8280-126">Tuttavia, i componenti dei colori vengono fissati a questo intervallo prima che vengano interpolati o scritti in un buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="a8280-126">However, color components are clamped to this range before they are interpolated or written into a color buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8280-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8280-127">Requirements</span></span>



| <span data-ttu-id="a8280-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8280-128">Requirement</span></span> | <span data-ttu-id="a8280-129">Valore</span><span class="sxs-lookup"><span data-stu-id="a8280-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8280-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8280-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a8280-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a8280-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a8280-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8280-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a8280-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a8280-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a8280-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8280-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8280-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8280-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a8280-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="a8280-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="a8280-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8280-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a8280-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a8280-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8280-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8280-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8280-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8280-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8280-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a8280-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a8280-142">**Remo**</span><span class="sxs-lookup"><span data-stu-id="a8280-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a8280-143">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="a8280-143">**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="a8280-144">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="a8280-144">**glIndex**</span></span>](glindexd.md)
</dt> </dl>

 

 






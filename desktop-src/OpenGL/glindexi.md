---
title: funzione glIndexi (GL. h)
description: La funzione glIndexi imposta l'indice dei colori corrente.
ms.assetid: c57d2316-4081-40d8-af50-ae0299597803
keywords:
- funzione glIndexi OpenGL
topic_type:
- apiref
api_name:
- glIndexi
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6b40d8d0d96aac17c852fb266b23dec23d26c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301262"
---
# <a name="glindexi-function"></a><span data-ttu-id="3d3dc-104">glIndexi (funzione)</span><span class="sxs-lookup"><span data-stu-id="3d3dc-104">glIndexi function</span></span>

<span data-ttu-id="3d3dc-105">La funzione **glIndexi** imposta l'indice dei colori corrente.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-105">The **glIndexi** function sets the current color index.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d3dc-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d3dc-106">Syntax</span></span>


```C++
void WINAPI glIndexi(
   GLint c
);
```



## <a name="parameters"></a><span data-ttu-id="3d3dc-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d3dc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d3dc-108">*c*</span><span class="sxs-lookup"><span data-stu-id="3d3dc-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="3d3dc-109">Nuovo valore per l'indice dei colori corrente.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-109">The new value for the current color index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d3dc-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d3dc-110">Return value</span></span>

<span data-ttu-id="3d3dc-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d3dc-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d3dc-112">Remarks</span></span>

<span data-ttu-id="3d3dc-113">La funzione **glIndexi** aggiorna l'indice dei colori corrente (a valore singolo).</span><span class="sxs-lookup"><span data-stu-id="3d3dc-113">The **glIndexi** function updates the current (single-valued) color index.</span></span> <span data-ttu-id="3d3dc-114">Accetta un solo argomento: il nuovo valore per l'indice dei colori corrente.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-114">It takes one argument: the new value for the current color index.</span></span>

<span data-ttu-id="3d3dc-115">L'indice corrente viene archiviato come valore a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-115">The current index is stored as a floating-point value.</span></span> <span data-ttu-id="3d3dc-116">I valori integer vengono convertiti direttamente in valori a virgola mobile, senza mapping speciale.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-116">Integer values are converted directly to floating-point values, with no special mapping.</span></span>

<span data-ttu-id="3d3dc-117">I valori di indice al di fuori dell'intervallo rappresentabile del buffer dell'indice colori non vengono bloccati.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-117">Index values outside the representable range of the color-index buffer are not clamped.</span></span> <span data-ttu-id="3d3dc-118">Tuttavia, prima che un indice sia reindirizzato (se abilitato) e scritto nel framebuffer, viene convertito nel formato a virgola fissa.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-118">However, before an index is dithered (if enabled) and written to the framebuffer, it is converted to fixed-point format.</span></span> <span data-ttu-id="3d3dc-119">Eventuali bit nella parte intera del valore a virgola fissa risultante che non corrispondono a BITS nel framebuffer vengono mascherati.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-119">Any bits in the integer portion of the resulting fixed-point value that do not correspond to bits in the framebuffer are masked out.</span></span>

<span data-ttu-id="3d3dc-120">L'indice corrente può essere aggiornato in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-120">The current index can be updated at any time.</span></span> <span data-ttu-id="3d3dc-121">In particolare, è possibile chiamare **glIndexi** tra una chiamata a [**glBegin**](/windows/desktop/OpenGL/glbegin) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3d3dc-121">In particular, **glIndexi** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](glend.md).</span></span>

<span data-ttu-id="3d3dc-122">La funzione seguente recupera le informazioni correlate a **glIndexi**:</span><span class="sxs-lookup"><span data-stu-id="3d3dc-122">The following function retrieves information related to **glIndexi**:</span></span>

<span data-ttu-id="3d3dc-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ index</span><span class="sxs-lookup"><span data-stu-id="3d3dc-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_INDEX</span></span>

## <a name="requirements"></a><span data-ttu-id="3d3dc-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d3dc-124">Requirements</span></span>



| <span data-ttu-id="3d3dc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d3dc-125">Requirement</span></span> | <span data-ttu-id="3d3dc-126">Valore</span><span class="sxs-lookup"><span data-stu-id="3d3dc-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d3dc-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d3dc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3d3dc-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3d3dc-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3d3dc-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d3dc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3d3dc-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3d3dc-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3d3dc-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d3dc-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d3dc-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d3dc-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3d3dc-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="3d3dc-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="3d3dc-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d3dc-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3d3dc-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3d3dc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d3dc-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d3dc-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d3dc-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d3dc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d3dc-138">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3d3dc-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3d3dc-139">**glColor**</span><span class="sxs-lookup"><span data-stu-id="3d3dc-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="3d3dc-140">**Remo**</span><span class="sxs-lookup"><span data-stu-id="3d3dc-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3d3dc-141">**glGet**</span><span class="sxs-lookup"><span data-stu-id="3d3dc-141">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 


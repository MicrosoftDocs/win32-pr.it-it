---
title: funzione gluTessVertex (Glu. h)
description: La funzione gluTessVertex specifica un vertice in un poligono.
ms.assetid: 9c555b32-5257-4eeb-9323-ccad59591097
keywords:
- funzione gluTessVertex OpenGL
topic_type:
- apiref
api_name:
- gluTessVertex
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546bbad2be1205f62c7889fbb18f23d5b0e38b8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518856"
---
# <a name="glutessvertex-function"></a><span data-ttu-id="26117-104">gluTessVertex (funzione)</span><span class="sxs-lookup"><span data-stu-id="26117-104">gluTessVertex function</span></span>

<span data-ttu-id="26117-105">La funzione **gluTessVertex** specifica un vertice in un poligono.</span><span class="sxs-lookup"><span data-stu-id="26117-105">The **gluTessVertex** function specifies a vertex on a polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="26117-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26117-106">Syntax</span></span>


```C++
void WINAPI gluTessVertex(
   GLUtesselator *tess,
   GLdouble      coords[3],
   void          *data
);
```



## <a name="parameters"></a><span data-ttu-id="26117-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="26117-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26117-108">*Tess*</span><span class="sxs-lookup"><span data-stu-id="26117-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="26117-109">Oggetto a mosaico creato con [**gluNewTess**](glunewtess.md).</span><span class="sxs-lookup"><span data-stu-id="26117-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="26117-110">*CoOrds*</span><span class="sxs-lookup"><span data-stu-id="26117-110">*coords*</span></span> 
</dt> <dd>

<span data-ttu-id="26117-111">Posizione del vertice.</span><span class="sxs-lookup"><span data-stu-id="26117-111">The location of the vertex.</span></span>

</dd> <dt>

<span data-ttu-id="26117-112">*data*</span><span class="sxs-lookup"><span data-stu-id="26117-112">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="26117-113">Puntatore passato al programma con il callback del vertice (come specificato da [*gluTessCallback*](glutess.md)).</span><span class="sxs-lookup"><span data-stu-id="26117-113">An pointer passed back to the program with the vertex callback (as specified by [*gluTessCallback*](glutess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26117-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26117-114">Return value</span></span>

<span data-ttu-id="26117-115">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="26117-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="26117-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="26117-116">Remarks</span></span>

<span data-ttu-id="26117-117">La funzione **gluTessVertex** descrive un vertice in un poligono che l'utente sta definendo.</span><span class="sxs-lookup"><span data-stu-id="26117-117">The **gluTessVertex** function describes a vertex on a polygon that the user is defining.</span></span> <span data-ttu-id="26117-118">Le chiamate **gluTessVertex** successive descrivono un contorno chiuso.</span><span class="sxs-lookup"><span data-stu-id="26117-118">Successive **gluTessVertex** calls describe a closed contour.</span></span> <span data-ttu-id="26117-119">Per descrivere un quadrilatero, ad esempio, chiamare **gluTessVertex** quattro volte.</span><span class="sxs-lookup"><span data-stu-id="26117-119">For example, to describe a quadrilateral, call **gluTessVertex** four times.</span></span> <span data-ttu-id="26117-120">È possibile chiamare **gluTessVertex** solo tra [**gluTessBeginContour**](glutessbegincontour.md) e [**gluTessEndContour**](glutessendcontour.md).</span><span class="sxs-lookup"><span data-stu-id="26117-120">You can only call **gluTessVertex** between [**gluTessBeginContour**](glutessbegincontour.md) and [**gluTessEndContour**](glutessendcontour.md).</span></span>

<span data-ttu-id="26117-121">Il parametro *Data* in genere punta a una struttura che contiene la posizione del vertice, oltre ad altri attributi per vertice, ad esempio colore e normale.</span><span class="sxs-lookup"><span data-stu-id="26117-121">The *data* parameter normally points to a structure containing the vertex location, as well as other per-vertex attributes such as color and normal.</span></span> <span data-ttu-id="26117-122">Questo puntatore viene passato di nuovo al programma tramite il \_ callback del vertice Glu dopo la suddivisione a mosaico (vedere [*gluTessCallback*](glutess.md)).</span><span class="sxs-lookup"><span data-stu-id="26117-122">This pointer is passed back to the program through the GLU\_VERTEX callback after tessellation (see [*gluTessCallback*](glutess.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="26117-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26117-123">Requirements</span></span>



| <span data-ttu-id="26117-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="26117-124">Requirement</span></span> | <span data-ttu-id="26117-125">Valore</span><span class="sxs-lookup"><span data-stu-id="26117-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="26117-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26117-126">Minimum supported client</span></span><br/> | <span data-ttu-id="26117-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26117-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="26117-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26117-128">Minimum supported server</span></span><br/> | <span data-ttu-id="26117-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26117-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="26117-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26117-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="26117-131"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="26117-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="26117-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="26117-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="26117-133"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26117-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="26117-134">DLL</span><span class="sxs-lookup"><span data-stu-id="26117-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26117-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26117-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26117-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26117-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26117-137">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="26117-137">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="26117-138">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="26117-138">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="26117-139">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="26117-139">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="26117-140">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="26117-140">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="26117-141">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="26117-141">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="26117-142">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="26117-142">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="26117-143">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="26117-143">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> </dl>

 

 






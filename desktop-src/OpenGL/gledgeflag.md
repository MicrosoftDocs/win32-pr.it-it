---
title: funzione glEdgeFlag (GL. h)
description: Contrassegna i bordi come limite o non delimitato. | funzione glEdgeFlag (GL. h)
ms.assetid: cebaa4af-a3bc-4396-9ee0-8cc10bcaf256
keywords:
- funzione glEdgeFlag OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlag
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 599a0b539e32d0e457f92c256e2cb0b678b05b59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321309"
---
# <a name="gledgeflag-function"></a><span data-ttu-id="fa516-105">glEdgeFlag (funzione)</span><span class="sxs-lookup"><span data-stu-id="fa516-105">glEdgeFlag function</span></span>

<span data-ttu-id="fa516-106">Contrassegna i bordi come limite o non delimitato.</span><span class="sxs-lookup"><span data-stu-id="fa516-106">Flags edges as either boundary or nonboundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa516-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa516-107">Syntax</span></span>


```C++
void WINAPI glEdgeFlag(
   GLboolean flag
);
```



## <a name="parameters"></a><span data-ttu-id="fa516-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa516-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa516-109">*flag*</span><span class="sxs-lookup"><span data-stu-id="fa516-109">*flag*</span></span> 
</dt> <dd>

<span data-ttu-id="fa516-110">Specifica il valore del flag perimetrale corrente, ovvero **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="fa516-110">Specifies the current edge flag value, either **TRUE** or **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa516-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa516-111">Return value</span></span>

<span data-ttu-id="fa516-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="fa516-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa516-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa516-113">Remarks</span></span>

<span data-ttu-id="fa516-114">Ogni vertice di un poligono, un triangolo separato o un quadrilatero separato specificato tra una coppia [**glBegin**](/windows/desktop/OpenGL/glbegin) / [**glEnd**](/windows/desktop/OpenGL/glend) è contrassegnato come inizio di un limite o di un bordo non delimitatore.</span><span class="sxs-lookup"><span data-stu-id="fa516-114">Each vertex of a polygon, separate triangle, or separate quadrilateral specified between a [**glBegin**](/windows/desktop/OpenGL/glbegin)/[**glEnd**](/windows/desktop/OpenGL/glend) pair is marked as the start of either a boundary or nonboundary edge.</span></span> <span data-ttu-id="fa516-115">Se il flag del bordo corrente è **true** quando viene specificato il vertice, il vertice viene contrassegnato come inizio di un bordo limite.</span><span class="sxs-lookup"><span data-stu-id="fa516-115">If the current edge flag is **TRUE** when the vertex is specified, the vertex is marked as the start of a boundary edge.</span></span> <span data-ttu-id="fa516-116">Se il flag perimetrale corrente è **false**, il vertice è contrassegnato come inizio di un bordo non associato.</span><span class="sxs-lookup"><span data-stu-id="fa516-116">If the current edge flag is **FALSE**, the vertex is marked as the start of a nonboundary edge.</span></span> <span data-ttu-id="fa516-117">La funzione **glEdgeFlag** imposta il flag Edge su **true** se flag è diverso da zero, **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fa516-117">The **glEdgeFlag** function sets the edge flag to **TRUE** if flag is nonzero, **FALSE** otherwise.</span></span>

<span data-ttu-id="fa516-118">I vertici dei triangoli e dei quadrilateri connessi sono sempre contrassegnati come limite, indipendentemente dal valore del flag Edge.</span><span class="sxs-lookup"><span data-stu-id="fa516-118">The vertices of connected triangles and connected quadrilaterals are always marked as boundary, regardless of the value of the edge flag.</span></span>

<span data-ttu-id="fa516-119">I flag perimetrali e bordi non delimitativi sui vertici sono significativi solo se \_ la modalità del poligono GL \_ è impostata sulla \_ linea GL o sul punto GL \_ .</span><span class="sxs-lookup"><span data-stu-id="fa516-119">Boundary and nonboundary edge flags on vertices are significant only if GL\_POLYGON\_MODE is set to GL\_POINT or GL\_LINE.</span></span> <span data-ttu-id="fa516-120">Vedere [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).</span><span class="sxs-lookup"><span data-stu-id="fa516-120">See [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).</span></span>

<span data-ttu-id="fa516-121">Inizialmente, il bit del flag Edge è **true**.</span><span class="sxs-lookup"><span data-stu-id="fa516-121">Initially, the edge flag bit is **TRUE**.</span></span>

<span data-ttu-id="fa516-122">Il flag perimetrale corrente può essere aggiornato in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="fa516-122">The current edge flag can be updated at any time.</span></span> <span data-ttu-id="fa516-123">In particolare, è possibile chiamare **glEdgeFlag** tra una chiamata a [**glBegin**](/windows/desktop/OpenGL/glbegin) e la chiamata corrispondente a [**glEnd**](/windows/desktop/OpenGL/glend).</span><span class="sxs-lookup"><span data-stu-id="fa516-123">In particular, **glEdgeFlag** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](/windows/desktop/OpenGL/glend).</span></span>

<span data-ttu-id="fa516-124">Le funzioni seguenti consentono di recuperare informazioni correlate a **glEdgeFlag**:</span><span class="sxs-lookup"><span data-stu-id="fa516-124">The following functions retrieve information related to **glEdgeFlag**:</span></span>

<span data-ttu-id="fa516-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con flag di \_ bordo GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="fa516-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_EDGE\_FLAG</span></span>

## <a name="requirements"></a><span data-ttu-id="fa516-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa516-126">Requirements</span></span>



| <span data-ttu-id="fa516-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa516-127">Requirement</span></span> | <span data-ttu-id="fa516-128">Valore</span><span class="sxs-lookup"><span data-stu-id="fa516-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa516-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa516-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fa516-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fa516-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fa516-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa516-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fa516-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fa516-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fa516-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa516-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa516-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa516-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fa516-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="fa516-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa516-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa516-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fa516-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fa516-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa516-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa516-138"><dt>Opengl32.dll</dt></span></span> </dl> |



 


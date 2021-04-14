---
title: funzione glEdgeFlagv (GL. h)
description: Contrassegna i bordi come limite o non delimitato. | funzione glEdgeFlagv (GL. h)
ms.assetid: 69b5ddbd-7c0c-47f0-a358-d8bf81755c88
keywords:
- funzione glEdgeFlagv OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe031ab3981e3daa2e6b1aefd51c9eaa62c84483
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353171"
---
# <a name="gledgeflagv-function"></a><span data-ttu-id="65c58-105">glEdgeFlagv (funzione)</span><span class="sxs-lookup"><span data-stu-id="65c58-105">glEdgeFlagv function</span></span>

<span data-ttu-id="65c58-106">Contrassegna i bordi come limite o non delimitato.</span><span class="sxs-lookup"><span data-stu-id="65c58-106">Flags edges as either boundary or nonboundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="65c58-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65c58-107">Syntax</span></span>


```C++
void WINAPI glEdgeFlagv(
   const GLboolean *flag
);
```



## <a name="parameters"></a><span data-ttu-id="65c58-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="65c58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65c58-109">*flag*</span><span class="sxs-lookup"><span data-stu-id="65c58-109">*flag*</span></span> 
</dt> <dd>

<span data-ttu-id="65c58-110">Specifica un puntatore a una matrice che contiene un singolo elemento booleano, che sostituisce il valore del flag perimetrale corrente.</span><span class="sxs-lookup"><span data-stu-id="65c58-110">Specifies a pointer to an array that contains a single Boolean element, which replaces the current edge flag value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65c58-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65c58-111">Return value</span></span>

<span data-ttu-id="65c58-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="65c58-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="65c58-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="65c58-113">Remarks</span></span>

<span data-ttu-id="65c58-114">Ogni vertice di un poligono, un triangolo separato o un quadrilatero separato specificato tra una coppia [**glBegin**](/windows/desktop/OpenGL/glbegin) / [**glEnd**](/windows/desktop/OpenGL/glend) è contrassegnato come inizio di un limite o di un bordo non delimitatore.</span><span class="sxs-lookup"><span data-stu-id="65c58-114">Each vertex of a polygon, separate triangle, or separate quadrilateral specified between a [**glBegin**](/windows/desktop/OpenGL/glbegin)/[**glEnd**](/windows/desktop/OpenGL/glend) pair is marked as the start of either a boundary or nonboundary edge.</span></span> <span data-ttu-id="65c58-115">Se il flag del bordo corrente è **true** quando viene specificato il vertice, il vertice viene contrassegnato come inizio di un bordo limite.</span><span class="sxs-lookup"><span data-stu-id="65c58-115">If the current edge flag is **TRUE** when the vertex is specified, the vertex is marked as the start of a boundary edge.</span></span> <span data-ttu-id="65c58-116">Se il flag perimetrale corrente è **false**, il vertice è contrassegnato come inizio di un bordo non associato.</span><span class="sxs-lookup"><span data-stu-id="65c58-116">If the current edge flag is **FALSE**, the vertex is marked as the start of a nonboundary edge.</span></span> <span data-ttu-id="65c58-117">La funzione **glEdgeFlagv** imposta il flag Edge su **true** se flag è diverso da zero, **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="65c58-117">The **glEdgeFlagv** function sets the edge flag to **TRUE** if flag is nonzero, **FALSE** otherwise.</span></span>

<span data-ttu-id="65c58-118">I vertici dei triangoli e dei quadrilateri connessi sono sempre contrassegnati come limite, indipendentemente dal valore del flag Edge.</span><span class="sxs-lookup"><span data-stu-id="65c58-118">The vertices of connected triangles and connected quadrilaterals are always marked as boundary, regardless of the value of the edge flag.</span></span>

<span data-ttu-id="65c58-119">I flag perimetrali e bordi non delimitativi sui vertici sono significativi solo se \_ la modalità del poligono GL \_ è impostata sulla \_ linea GL o sul punto GL \_ .</span><span class="sxs-lookup"><span data-stu-id="65c58-119">Boundary and nonboundary edge flags on vertices are significant only if GL\_POLYGON\_MODE is set to GL\_POINT or GL\_LINE.</span></span> <span data-ttu-id="65c58-120">Vedere [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).</span><span class="sxs-lookup"><span data-stu-id="65c58-120">See [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).</span></span>

<span data-ttu-id="65c58-121">Inizialmente, il bit del flag Edge è **true**.</span><span class="sxs-lookup"><span data-stu-id="65c58-121">Initially, the edge flag bit is **TRUE**.</span></span>

<span data-ttu-id="65c58-122">Il flag perimetrale corrente può essere aggiornato in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="65c58-122">The current edge flag can be updated at any time.</span></span> <span data-ttu-id="65c58-123">In particolare, è possibile chiamare **glEdgeFlagv** tra una chiamata a [**glBegin**](/windows/desktop/OpenGL/glbegin) e la chiamata corrispondente a [**glEnd**](/windows/desktop/OpenGL/glend).</span><span class="sxs-lookup"><span data-stu-id="65c58-123">In particular, **glEdgeFlagv** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](/windows/desktop/OpenGL/glend).</span></span>

<span data-ttu-id="65c58-124">Le funzioni seguenti consentono di recuperare informazioni correlate a **glEdgeFlagv**:</span><span class="sxs-lookup"><span data-stu-id="65c58-124">The following functions retrieve information related to **glEdgeFlagv**:</span></span>

<span data-ttu-id="65c58-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con flag di \_ bordo GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="65c58-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_EDGE\_FLAG</span></span>

## <a name="requirements"></a><span data-ttu-id="65c58-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65c58-126">Requirements</span></span>



| <span data-ttu-id="65c58-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="65c58-127">Requirement</span></span> | <span data-ttu-id="65c58-128">Valore</span><span class="sxs-lookup"><span data-stu-id="65c58-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65c58-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65c58-129">Minimum supported client</span></span><br/> | <span data-ttu-id="65c58-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="65c58-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="65c58-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65c58-131">Minimum supported server</span></span><br/> | <span data-ttu-id="65c58-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="65c58-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65c58-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65c58-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="65c58-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="65c58-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="65c58-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="65c58-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="65c58-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65c58-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="65c58-137">DLL</span><span class="sxs-lookup"><span data-stu-id="65c58-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65c58-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65c58-138"><dt>Opengl32.dll</dt></span></span> </dl> |



 


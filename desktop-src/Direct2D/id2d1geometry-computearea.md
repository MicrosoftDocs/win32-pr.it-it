---
title: Metodi ComputeArea di ID2D1Geometry
description: Calcola l'area della geometria.
ms.assetid: 655f11bc-7435-4d23-b4b1-3d7c2110aa48
keywords:
- Metodo ComputeArea Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: f6b79e8434a2174bcb05659f6656a46cc2d43cbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333514"
---
# <a name="id2d1geometrycomputearea-methods"></a><span data-ttu-id="cb830-104">Metodi ID2D1Geometry:: ComputeArea</span><span class="sxs-lookup"><span data-stu-id="cb830-104">ID2D1Geometry::ComputeArea methods</span></span>

<span data-ttu-id="cb830-105">Calcola l'area della geometria.</span><span class="sxs-lookup"><span data-stu-id="cb830-105">Computes the area of the geometry.</span></span>

### <a name="overload-list"></a><span data-ttu-id="cb830-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="cb830-106">Overload list</span></span>



| <span data-ttu-id="cb830-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="cb830-107">Method</span></span>                                                                                                                      | <span data-ttu-id="cb830-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb830-108">Description</span></span>                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb830-109">[**ComputeArea (D2D1 \_ Matrix \_ 3X2 \_ F&, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))</span><span class="sxs-lookup"><span data-stu-id="cb830-109">[**ComputeArea(D2D1\_MATRIX\_3X2\_F&,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))</span></span>              | <span data-ttu-id="cb830-110">Calcola l'area della geometria dopo che è stata trasformata dalla matrice specificata e appiattita utilizzando la tolleranza predefinita.</span><span class="sxs-lookup"><span data-stu-id="cb830-110">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the default tolerance.</span></span><br/>    |
| <span data-ttu-id="cb830-111">[**ComputeArea (D2D1 \_ Matrix \_ 3x2 \_ F \* , float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="cb830-111">[**ComputeArea(D2D1\_MATRIX\_3X2\_F\*,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span></span>             | <span data-ttu-id="cb830-112">Calcola l'area della geometria dopo che è stata trasformata dalla matrice specificata e appiattita utilizzando la tolleranza predefinita.</span><span class="sxs-lookup"><span data-stu-id="cb830-112">Computes the area of the geometry after it has been transformed by the specified matrix and flattened by using the default tolerance.</span></span><br/> |
| <span data-ttu-id="cb830-113">[**ComputeArea (D2D1 \_ Matrix \_ 3X2 \_ F&, float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))</span><span class="sxs-lookup"><span data-stu-id="cb830-113">[**ComputeArea(D2D1\_MATRIX\_3X2\_F&,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))</span></span>  | <span data-ttu-id="cb830-114">Calcola l'area della geometria dopo che è stata trasformata dalla matrice specificata e appiattita utilizzando la tolleranza specificata.</span><span class="sxs-lookup"><span data-stu-id="cb830-114">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.</span></span><br/>  |
| <span data-ttu-id="cb830-115">[**ComputeArea (D2D1 \_ Matrix \_ 3x2 \_ F \* , float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="cb830-115">[**ComputeArea(D2D1\_MATRIX\_3X2\_F\*,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))</span></span> | <span data-ttu-id="cb830-116">Calcola l'area della geometria dopo che è stata trasformata dalla matrice specificata e appiattita utilizzando la tolleranza specificata.</span><span class="sxs-lookup"><span data-stu-id="cb830-116">Computes the area of the geometry after it has been transformed by the specified matrix and flattened using the specified tolerance.</span></span><br/>  |



## <a name="examples"></a><span data-ttu-id="cb830-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="cb830-117">Examples</span></span>

<span data-ttu-id="cb830-118">Nell'esempio di codice seguente viene usato **ComputeArea** per calcolare l'area di un cerchio specificato (**m \_ pCircleGeometry1**).</span><span class="sxs-lookup"><span data-stu-id="cb830-118">The following code example uses **ComputeArea** to compute the area of a specified circle (**m\_pCircleGeometry1**).</span></span>


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



## <a name="requirements"></a><span data-ttu-id="cb830-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb830-119">Requirements</span></span>



| <span data-ttu-id="cb830-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb830-120">Requirement</span></span> | <span data-ttu-id="cb830-121">Valore</span><span class="sxs-lookup"><span data-stu-id="cb830-121">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cb830-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="cb830-122">Library</span></span><br/> | <dl> <span data-ttu-id="cb830-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb830-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="cb830-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cb830-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="cb830-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb830-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb830-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb830-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb830-127">**ID2D1Geometry**</span><span class="sxs-lookup"><span data-stu-id="cb830-127">**ID2D1Geometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 


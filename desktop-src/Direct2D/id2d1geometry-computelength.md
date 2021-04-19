---
title: Metodi ComputeLength di ID2D1Geometry
description: Calcola la lunghezza della geometria come se ogni segmento venisse registrato in una riga.
ms.assetid: 4659d880-0aa3-485d-ac71-044d9ace6759
keywords:
- Metodo ComputeLength Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: b49b1beb0525d95967ad903b0f0fb3c464edf4d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333512"
---
# <a name="id2d1geometrycomputelength-methods"></a><span data-ttu-id="fba33-104">Metodi ID2D1Geometry:: ComputeLength</span><span class="sxs-lookup"><span data-stu-id="fba33-104">ID2D1Geometry::ComputeLength methods</span></span>

<span data-ttu-id="fba33-105">Calcola la lunghezza della geometria come se ogni segmento venisse registrato in una riga.</span><span class="sxs-lookup"><span data-stu-id="fba33-105">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span>

### <a name="overload-list"></a><span data-ttu-id="fba33-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="fba33-106">Overload list</span></span>



| <span data-ttu-id="fba33-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="fba33-107">Method</span></span>                                                                                                                          | <span data-ttu-id="fba33-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fba33-108">Description</span></span>                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fba33-109">[**ComputeLength (D2D1 \_ Matrix \_ 3X2 \_ F&, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="fba33-109">[**ComputeLength(D2D1\_MATRIX\_3X2\_F&,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span></span>              | <span data-ttu-id="fba33-110">Calcola la lunghezza della geometria come se ogni segmento venisse registrato in una riga.</span><span class="sxs-lookup"><span data-stu-id="fba33-110">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span><br/>  |
| <span data-ttu-id="fba33-111">[**ComputeLength (D2D1 \_ Matrix \_ 3x2 \_ F \* , float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="fba33-111">[**ComputeLength(D2D1\_MATRIX\_3X2\_F\*,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span></span>             | <span data-ttu-id="fba33-112">Calcola la lunghezza della geometria come se ogni segmento venisse registrato in una riga.</span><span class="sxs-lookup"><span data-stu-id="fba33-112">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span><br/>  |
| <span data-ttu-id="fba33-113">[**ComputeLength (D2D1 \_ Matrix \_ 3X2 \_ F&, float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f__float_float))</span><span class="sxs-lookup"><span data-stu-id="fba33-113">[**ComputeLength(D2D1\_MATRIX\_3X2\_F&,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f__float_float))</span></span>  | <span data-ttu-id="fba33-114">Calcola la lunghezza della geometria come se ogni segmento venisse registrato in una riga.</span><span class="sxs-lookup"><span data-stu-id="fba33-114">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span><br/>  |
| <span data-ttu-id="fba33-115">[**ComputeLength (D2D1 \_ Matrix \_ 3x2 \_ F \* , float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span><span class="sxs-lookup"><span data-stu-id="fba33-115">[**ComputeLength(D2D1\_MATRIX\_3X2\_F\*,FLOAT,FLOAT\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))</span></span> | <span data-ttu-id="fba33-116">Calcola la lunghezza della geometria come se ogni segmento venisse registrato in una riga.</span><span class="sxs-lookup"><span data-stu-id="fba33-116">Calculates the length of the geometry as though each segment were unrolled into a line.</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="fba33-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="fba33-117">Examples</span></span>

<span data-ttu-id="fba33-118">Il codice seguente illustra come usare **ComputeLength** per calcolare la lunghezza di una geometria del percorso specificata.</span><span class="sxs-lookup"><span data-stu-id="fba33-118">The following code shows how to use **ComputeLength** to compute the length of a specified path geometry.</span></span>


```C++
float length = 0;
hr = m_pPathGeometry->ComputeLength(
    NULL, //no transform
    &length
    );

if (SUCCEEDED(hr))
{
    m_Animation.SetStart(0);        //start at beginning of path
    m_Animation.SetEnd(length);     //length at end of path
    m_Animation.SetDuration(5.0f);  //seconds

    ZeroMemory(&m_DwmTimingInfo, sizeof(m_DwmTimingInfo));
    m_DwmTimingInfo.cbSize = sizeof(m_DwmTimingInfo);

    // Get the composition refresh rate. If the DWM isn't running,
    // get the refresh rate from GDI -- probably going to be 60Hz
    if (FAILED(DwmGetCompositionTimingInfo(NULL, &m_DwmTimingInfo)))
    {
        HDC hdc = GetDC(m_hwnd);
        m_DwmTimingInfo.rateCompose.uiDenominator = 1;
        m_DwmTimingInfo.rateCompose.uiNumerator = GetDeviceCaps(hdc, VREFRESH);
        ReleaseDC(m_hwnd, hdc);
    }

    ShowWindow(m_hwnd, SW_SHOWNORMAL);

    UpdateWindow(m_hwnd);
}
```



## <a name="requirements"></a><span data-ttu-id="fba33-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fba33-119">Requirements</span></span>



| <span data-ttu-id="fba33-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fba33-120">Requirement</span></span> | <span data-ttu-id="fba33-121">Valore</span><span class="sxs-lookup"><span data-stu-id="fba33-121">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fba33-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="fba33-122">Library</span></span><br/> | <dl> <span data-ttu-id="fba33-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fba33-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="fba33-124">DLL</span><span class="sxs-lookup"><span data-stu-id="fba33-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="fba33-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fba33-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fba33-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fba33-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba33-127">**ID2D1Geometry**</span><span class="sxs-lookup"><span data-stu-id="fba33-127">**ID2D1Geometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 


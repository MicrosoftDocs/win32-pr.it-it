---
title: Metodi CreateStrokeStyle di ID2D1Factory
description: Crea un ID2D1StrokeStyle che descrive l'estremità iniziale, lo schema Dash e altre funzionalità di un tratto.
ms.assetid: cc7bd68b-a6eb-4d05-b331-032ce80f375c
keywords:
- Metodo CreateStrokeStyle Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 09a578cafe6795bbf742d9dac114365d6e850586
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333382"
---
# <a name="id2d1factorycreatestrokestyle-methods"></a><span data-ttu-id="be9b9-104">Metodi ID2D1Factory:: CreateStrokeStyle</span><span class="sxs-lookup"><span data-stu-id="be9b9-104">ID2D1Factory::CreateStrokeStyle methods</span></span>

<span data-ttu-id="be9b9-105">Crea un [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) che descrive l'estremità iniziale, lo schema Dash e altre funzionalità di un tratto.</span><span class="sxs-lookup"><span data-stu-id="be9b9-105">Creates an [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) that describes start cap, dash pattern, and other features of a stroke.</span></span>

### <a name="overload-list"></a><span data-ttu-id="be9b9-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="be9b9-106">Overload list</span></span>



| <span data-ttu-id="be9b9-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="be9b9-107">Method</span></span>                                                                                                                                                                                                  | <span data-ttu-id="be9b9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be9b9-108">Description</span></span>                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be9b9-109">[**CreateStrokeStyle ( \_ \_ Proprietà stile tratto d2d1 \_&, float \* , uint, ID2D1StrokeStyle \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties__constfloat_uint32_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="be9b9-109">[**CreateStrokeStyle(D2D1\_STROKE\_STYLE\_PROPERTIES&, FLOAT\*, UINT, ID2D1StrokeStyle\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties__constfloat_uint32_id2d1strokestyle))</span></span>  | <span data-ttu-id="be9b9-110">Crea un [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) che descrive l'estremità iniziale, lo schema Dash e altre funzionalità di un tratto.</span><span class="sxs-lookup"><span data-stu-id="be9b9-110">Creates an [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) that describes start cap, dash pattern, and other features of a stroke.</span></span><br/> |
| <span data-ttu-id="be9b9-111">[**CreateStrokeStyle ( \_ \_ Proprietà stile tratto \_ d2d1 \* , float \* , uint, ID2D1StrokeStyle \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties_constfloat_uint32_id2d1strokestyle))</span><span class="sxs-lookup"><span data-stu-id="be9b9-111">[**CreateStrokeStyle(D2D1\_STROKE\_STYLE\_PROPERTIES\*, FLOAT\*, UINT, ID2D1StrokeStyle\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties_constfloat_uint32_id2d1strokestyle))</span></span> | <span data-ttu-id="be9b9-112">Crea un [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) che descrive l'estremità iniziale, lo schema Dash e altre funzionalità di un tratto.</span><span class="sxs-lookup"><span data-stu-id="be9b9-112">Creates an [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) that describes start cap, dash pattern, and other features of a stroke.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="be9b9-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="be9b9-113">Examples</span></span>

<span data-ttu-id="be9b9-114">Nell'esempio seguente viene creato un tratto che utilizza un modello di tratteggio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="be9b9-114">The following example creates a stroke that uses a custom dash pattern.</span></span>


```C++
// Dash array for dashStyle D2D1_DASH_STYLE_CUSTOM
float dashes[] = {1.0f, 2.0f, 2.0f, 3.0f, 2.0f, 2.0f};

// Stroke Style with Dash Style -- Custom
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateStrokeStyle(
        D2D1::StrokeStyleProperties(
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_ROUND,
            D2D1_LINE_JOIN_MITER,
            10.0f,
            D2D1_DASH_STYLE_CUSTOM,
            0.0f),
        dashes,
        ARRAYSIZE(dashes),
        &m_pStrokeStyleCustomOffsetZero
        );
}
```



<span data-ttu-id="be9b9-115">Nell'esempio seguente viene usato lo stile stroke durante il disegno di una linea.</span><span class="sxs-lookup"><span data-stu-id="be9b9-115">The next example uses the stroke style when drawing a line.</span></span>


```C++
m_pRenderTarget->DrawLine(
    D2D1::Point2F(0, 310),
    D2D1::Point2F(200, 310),
    m_pCornflowerBlueBrush,
    10.0f,
    m_pStrokeStyleCustomOffsetZero
    );
```



## <a name="requirements"></a><span data-ttu-id="be9b9-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be9b9-116">Requirements</span></span>



| <span data-ttu-id="be9b9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="be9b9-117">Requirement</span></span> | <span data-ttu-id="be9b9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="be9b9-118">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="be9b9-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="be9b9-119">Library</span></span><br/> | <dl> <span data-ttu-id="be9b9-120"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be9b9-120"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="be9b9-121">DLL</span><span class="sxs-lookup"><span data-stu-id="be9b9-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="be9b9-122"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be9b9-122"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be9b9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be9b9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be9b9-124">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="be9b9-124">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 


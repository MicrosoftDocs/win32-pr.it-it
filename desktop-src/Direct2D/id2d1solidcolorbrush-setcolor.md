---
title: Metodi Secolor ID2D1SolidColorBrush
description: Specifica il colore di questo pennello a tinta unita.
ms.assetid: 2900bf72-9641-419c-b0d7-334f14f8a474
keywords:
- Metodo Secolor Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 580778135e840a69342ff34ffd8e415883317517
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331189"
---
# <a name="id2d1solidcolorbrushsetcolor-methods"></a><span data-ttu-id="365e4-104">Metodi ID2D1SolidColorBrush:: Secolor</span><span class="sxs-lookup"><span data-stu-id="365e4-104">ID2D1SolidColorBrush::SetColor methods</span></span>

<span data-ttu-id="365e4-105">Specifica il colore di questo pennello a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="365e4-105">Specifies the color of this solid color brush.</span></span>

### <a name="overload-list"></a><span data-ttu-id="365e4-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="365e4-106">Overload list</span></span>



| <span data-ttu-id="365e4-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="365e4-107">Method</span></span>                                                                          | <span data-ttu-id="365e4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="365e4-108">Description</span></span>                                                |
|:--------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span data-ttu-id="365e4-109">[**Secolor (D2D1 \_ Color \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))</span><span class="sxs-lookup"><span data-stu-id="365e4-109">[**SetColor(D2D1\_COLOR\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))</span></span>  | <span data-ttu-id="365e4-110">Specifica il colore di questo pennello a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="365e4-110">Specifies the color of this solid-color brush.</span></span> <br/> |
| <span data-ttu-id="365e4-111">[**Secolor (D2D1 \_ Color \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f))</span><span class="sxs-lookup"><span data-stu-id="365e4-111">[**SetColor(D2D1\_COLOR\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f))</span></span> | <span data-ttu-id="365e4-112">Specifica il colore di questo pennello a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="365e4-112">Specifies the color of this solid color brush.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="365e4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="365e4-113">Remarks</span></span>

<span data-ttu-id="365e4-114">Per semplificare la creazione dei colori, Direct2D fornisce la classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .</span><span class="sxs-lookup"><span data-stu-id="365e4-114">To help create colors, Direct2D provides the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class.</span></span> <span data-ttu-id="365e4-115">Offre diversi metodi helper per la creazione di colori e fornisce un set o colori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="365e4-115">It offers several helper methods for creating colors and provides a set or predefined colors.</span></span>

## <a name="examples"></a><span data-ttu-id="365e4-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="365e4-116">Examples</span></span>

<span data-ttu-id="365e4-117">Il codice seguente illustra come usare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="365e4-117">The following code shows how to use this method.</span></span>


```C++
        m_pSolidColorBrush->SetColor(
            D2D1::ColorF(
                0.0f,
                intensity,
                1.0f - intensity
                ));

        hr = m_pRealization->Fill(
                m_pRT,
                m_pSolidColorBrush,
                m_useRealizations ?
                    REALIZATION_RENDER_MODE_DEFAULT :
                    REALIZATION_RENDER_MODE_FORCE_UNREALIZED
                );
```



## <a name="requirements"></a><span data-ttu-id="365e4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="365e4-118">Requirements</span></span>



| <span data-ttu-id="365e4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="365e4-119">Requirement</span></span> | <span data-ttu-id="365e4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="365e4-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="365e4-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="365e4-121">Library</span></span><br/> | <dl> <span data-ttu-id="365e4-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="365e4-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="365e4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="365e4-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="365e4-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="365e4-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="365e4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="365e4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="365e4-126">**ID2D1SolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="365e4-126">**ID2D1SolidColorBrush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)
</dt> </dl>

 


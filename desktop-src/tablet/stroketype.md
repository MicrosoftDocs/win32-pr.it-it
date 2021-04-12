---
description: Indica se un tratto deve essere analizzato come parte di un disegno o come parte della scrittura.
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: Enumerazione StrokeType (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrokeType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 3b59be130c6c7055bb7636760451dcadf5acf841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232704"
---
# <a name="stroketype-enumeration"></a><span data-ttu-id="2905f-103">Enumerazione StrokeType</span><span class="sxs-lookup"><span data-stu-id="2905f-103">StrokeType enumeration</span></span>

<span data-ttu-id="2905f-104">Indica se un tratto deve essere analizzato come parte di un disegno o come parte della scrittura.</span><span class="sxs-lookup"><span data-stu-id="2905f-104">Indicates whether a stroke should be analyzed as part of a drawing or as part of writing.</span></span>

## <a name="syntax"></a><span data-ttu-id="2905f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2905f-105">Syntax</span></span>


```C++
typedef enum StrokeType { 
  StrokeType_Unclassified  = 0,
  StrokeType_Writing       = 1,
  StrokeType_Drawing       = 2
} StrokeType;
```



## <a name="constants"></a><span data-ttu-id="2905f-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="2905f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2905f-107"><span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType non \_ Classificato**</span><span class="sxs-lookup"><span data-stu-id="2905f-107"><span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType\_Unclassified**</span></span>
</dt> <dd>

<span data-ttu-id="2905f-108">Il tratto può essere parte di un disegno o parte della scrittura.</span><span class="sxs-lookup"><span data-stu-id="2905f-108">The stroke might be either part of a drawing or part of writing.</span></span>

</dd> <dt>

<span data-ttu-id="2905f-109"><span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**\_Scrittura StrokeType**</span><span class="sxs-lookup"><span data-stu-id="2905f-109"><span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**StrokeType\_Writing**</span></span>
</dt> <dd>

<span data-ttu-id="2905f-110">Il tratto fa parte della scrittura.</span><span class="sxs-lookup"><span data-stu-id="2905f-110">The stroke is part of writing.</span></span>

</dd> <dt>

<span data-ttu-id="2905f-111"><span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**\_Disegno StrokeType**</span><span class="sxs-lookup"><span data-stu-id="2905f-111"><span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**StrokeType\_Drawing**</span></span>
</dt> <dd>

<span data-ttu-id="2905f-112">Il tratto fa parte di un disegno.</span><span class="sxs-lookup"><span data-stu-id="2905f-112">The stroke is part of a drawing.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="2905f-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="2905f-113">Examples</span></span>

<span data-ttu-id="2905f-114">Nell'esempio seguente viene illustrata una parte di un gestore eventi Stroke, implementata in modo simile all' [esempio di sink di eventi C++](c---event-sinks-sample.md).</span><span class="sxs-lookup"><span data-stu-id="2905f-114">The following example shows part of a stroke event handler, implemented in a similar fashion to the [C++ Event Sinks Sample](c---event-sinks-sample.md).</span></span> <span data-ttu-id="2905f-115">Il tratto aggiunto viene controllato per verificare se la parte superiore del riquadro è stata disegnata al di sotto di un margine `drawingMargin` .</span><span class="sxs-lookup"><span data-stu-id="2905f-115">The added stroke is checked to see if the top of its bounding box has been drawn below a margin, `drawingMargin`.</span></span> <span data-ttu-id="2905f-116">In tal caso, [](iinkanalyzer.md) l'oggetto IInkAnalyzer `m_spInkAnalyzer` è impostato per analizzare il tratto come tratto di disegno, anziché come tratto di grafia.</span><span class="sxs-lookup"><span data-stu-id="2905f-116">If so, the [**IInkAnalyzer**](iinkanalyzer.md) object, `m_spInkAnalyzer`, is set to analyze the stroke as a drawing stroke, rather than as a handwriting stroke.</span></span> <span data-ttu-id="2905f-117">`CheckHResult` è una funzione che accetta un oggetto `HRESULT` e una stringa e genera un'eccezione creata con la stringa se `HRESULT` non ha **esito positivo**.</span><span class="sxs-lookup"><span data-stu-id="2905f-117">`CheckHResult` is a function that takes an `HRESULT` and a string, and throws an exception created with the string if the `HRESULT` is not **SUCCESS**.</span></span>


```C++
IInkRectangle* bounds;
CheckHResult(pStroke->GetBoundingBox(IBBM_Default, &bounds), "IInkStrokeDisp::GetBoundingBox failed");
long top;
CheckHResult(bounds->get_Top(&top), "IInkRectangle::get_Top failed");
if (top > drawingMargin)
{
    long strokeId;
    CheckHResult(pStroke->get_ID(&strokeId), "IInkStrokeDisp::get_ID failed");
    m_pInkAnalyzer->SetStrokeType(strokeId, StrokeType_Drawing);
}
```



## <a name="requirements"></a><span data-ttu-id="2905f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2905f-118">Requirements</span></span>



| <span data-ttu-id="2905f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2905f-119">Requirement</span></span> | <span data-ttu-id="2905f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2905f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2905f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2905f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2905f-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2905f-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2905f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2905f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2905f-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2905f-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2905f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2905f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2905f-126"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2905f-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2905f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2905f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2905f-128">**Metodo IInkAnalyzer:: SetStrokeType**</span><span class="sxs-lookup"><span data-stu-id="2905f-128">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 





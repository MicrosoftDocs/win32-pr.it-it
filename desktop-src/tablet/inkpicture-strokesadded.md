---
description: Si verifica quando uno o più oggetti IInkStrokeDisp vengono aggiunti alla raccolta InkStrokes.
ms.assetid: 577ad52b-ecd3-4a49-8997-481ebdb47203
title: Evento InkPicture. StrokesAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e79d87a4315068cbb0cf9db25b6532bc4c09943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315569"
---
# <a name="inkpicturestrokesadded-event"></a><span data-ttu-id="bdb9a-103">Evento InkPicture. StrokesAdded</span><span class="sxs-lookup"><span data-stu-id="bdb9a-103">InkPicture.StrokesAdded event</span></span>

<span data-ttu-id="bdb9a-104">Si verifica quando uno o più oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) vengono aggiunti alla raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bdb9a-104">Occurs when one or more [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects are added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdb9a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bdb9a-105">Syntax</span></span>


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="bdb9a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bdb9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdb9a-107">*StrokeIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bdb9a-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdb9a-108">Matrice di interi degli identificatori per ogni oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) aggiunto quando si verifica questo evento.</span><span class="sxs-lookup"><span data-stu-id="bdb9a-108">The integer array of identifiers for every [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object added when this event occurs.</span></span>

<span data-ttu-id="bdb9a-109">Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="bdb9a-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdb9a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bdb9a-110">Return value</span></span>

<span data-ttu-id="bdb9a-111">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="bdb9a-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdb9a-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="bdb9a-112">Remarks</span></span>

<span data-ttu-id="bdb9a-113">Questo metodo di evento è definito nell'interfaccia **\_ IInkStrokesEvents** .</span><span class="sxs-lookup"><span data-stu-id="bdb9a-113">This event method is defined in the **\_IInkStrokesEvents** interface.</span></span> <span data-ttu-id="bdb9a-114">L'interfaccia **\_ IInkStrokesEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ SEStrokesAdded.</span><span class="sxs-lookup"><span data-stu-id="bdb9a-114">The **\_IInkStrokesEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_SEStrokesAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdb9a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdb9a-115">Requirements</span></span>



| <span data-ttu-id="bdb9a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdb9a-116">Requirement</span></span> | <span data-ttu-id="bdb9a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bdb9a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdb9a-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdb9a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bdb9a-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bdb9a-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="bdb9a-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdb9a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bdb9a-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bdb9a-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="bdb9a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bdb9a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdb9a-123"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bdb9a-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bdb9a-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="bdb9a-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="bdb9a-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdb9a-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="bdb9a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdb9a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdb9a-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="bdb9a-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 


---
description: "Si verifica quando il controllo InkEdit ottiene manualmente i risultati da una chiamata al Metodo InkEdit:: Recognize o automaticamente dopo l'attivazione del timeout di riconoscimento."
ms.assetid: 09618be0-fe49-494f-940f-79ff8352097e
title: Evento InkEdit. RecognitionResult (inchiostrata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d6206293b604e5540b5e6d0271e1ebe984a987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233557"
---
# <a name="inkeditrecognitionresult-event"></a><span data-ttu-id="b5071-103">Evento InkEdit. RecognitionResult</span><span class="sxs-lookup"><span data-stu-id="b5071-103">InkEdit.RecognitionResult event</span></span>

<span data-ttu-id="b5071-104">Si verifica quando il controllo [InkEdit](inkedit-control-reference.md) ottiene manualmente i risultati da una chiamata al metodo [**InkEdit:: Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) o automaticamente dopo l'attivazione del timeout di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="b5071-104">Occurs when the [InkEdit](inkedit-control-reference.md) control gets results manually from a call to the [**InkEdit::Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) method or automatically after the recognition timeout fires.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5071-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5071-105">Syntax</span></span>


```C++
void RecognitionResult(
  [in] IInkRecognitionResult *RecognitionResult
);
```



## <a name="parameters"></a><span data-ttu-id="b5071-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5071-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5071-107">*RecognitionResult* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5071-107">*RecognitionResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5071-108">Oggetto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) che contiene il risultato del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="b5071-108">An [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object that contains the result of the recognition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5071-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5071-109">Return value</span></span>

<span data-ttu-id="b5071-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b5071-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5071-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5071-111">Remarks</span></span>

<span data-ttu-id="b5071-112">Questo metodo di evento è definito nell'interfaccia **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="b5071-112">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="b5071-113">L'interfaccia **\_ IInkEditEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IeeRecognitionResult.</span><span class="sxs-lookup"><span data-stu-id="b5071-113">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeRecognitionResult.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5071-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5071-114">Requirements</span></span>



| <span data-ttu-id="b5071-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5071-115">Requirement</span></span> | <span data-ttu-id="b5071-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b5071-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5071-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5071-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b5071-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b5071-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b5071-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5071-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b5071-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b5071-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b5071-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5071-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5071-122"><dt>Inchiostrato. h (richiede anche il \_ . c)</dt></span><span class="sxs-lookup"><span data-stu-id="b5071-122"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b5071-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="b5071-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5071-124"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5071-124"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b5071-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5071-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5071-126">InkEdit</span><span class="sxs-lookup"><span data-stu-id="b5071-126">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

<span data-ttu-id="b5071-127">[**Metodo Recognize ( \[ controllo InkEdit)\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)</span><span class="sxs-lookup"><span data-stu-id="b5071-127">[**Recognize Method \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)</span></span>
</dt> </dl>

 


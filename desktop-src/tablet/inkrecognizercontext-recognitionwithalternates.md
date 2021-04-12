---
description: Si verifica quando la classe InkRecognizerContext genera risultati dopo la chiamata al metodo del metodo BackgroundRecognizeWithAlternates.
ms.assetid: 5e86a4d5-c0a7-4283-81cc-ec3a26f74880
title: Evento InkRecognizerContext. RecognitionWithAlternates (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a7d35d8281305b0cb5f84114bb2f2fa0e718c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232483"
---
# <a name="inkrecognizercontextrecognitionwithalternates-event"></a><span data-ttu-id="94d31-103">Evento InkRecognizerContext. RecognitionWithAlternates</span><span class="sxs-lookup"><span data-stu-id="94d31-103">InkRecognizerContext.RecognitionWithAlternates event</span></span>

<span data-ttu-id="94d31-104">Si verifica quando la [**classe InkRecognizerContext**](inkrecognizercontext-class.md) genera risultati dopo la chiamata al metodo del [**metodo BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) .</span><span class="sxs-lookup"><span data-stu-id="94d31-104">Occurs when the [**InkRecognizerContext Class**](inkrecognizercontext-class.md) has generated results after calling the [**BackgroundRecognizeWithAlternates Method**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="94d31-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94d31-105">Syntax</span></span>


```C++
void RecognitionWithAlternates(
  [in] IInkRecognitionResult *RecognitionResult,
  [in] VARIANT               CustomData,
  [in] InkRecognitionStatus  RecognitionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="94d31-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="94d31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94d31-107">*RecognitionResult* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94d31-107">*RecognitionResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94d31-108">Risultato del riconoscimento dall'evento.</span><span class="sxs-lookup"><span data-stu-id="94d31-108">The recognition result from the event.</span></span>

</dd> <dt>

<span data-ttu-id="94d31-109">*CustomData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94d31-109">*CustomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94d31-110">Dati personalizzati per il risultato del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="94d31-110">The custom data for the recognition result.</span></span>

<span data-ttu-id="94d31-111">Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="94d31-111">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="94d31-112">*RecognitionStatus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94d31-112">*RecognitionStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94d31-113">Stato di riconoscimento del risultato del riconoscimento più recente.</span><span class="sxs-lookup"><span data-stu-id="94d31-113">The recognition status as of the most recent recognition result.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94d31-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="94d31-114">Return value</span></span>

<span data-ttu-id="94d31-115">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="94d31-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94d31-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="94d31-116">Remarks</span></span>

<span data-ttu-id="94d31-117">Il comportamento del Application Programming Interface (API) è imprevedibile se si tenta di ottenere l'accesso all'oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) originale dal gestore dell'evento di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="94d31-117">The behavior of the application programming interface (API) is unpredictable if you try to gain access to the original [**InkRecognizerContext**](inkrecognizercontext-class.md) object from the recognition event handler.</span></span> <span data-ttu-id="94d31-118">Non tentare di eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="94d31-118">Do not attempt to do this.</span></span> <span data-ttu-id="94d31-119">In alternativa, se è necessario eseguire questa operazione, creare un flag e impostarlo nel gestore dell'evento di [**riconoscimento**](inkrecognizercontext-recognition.md) .</span><span class="sxs-lookup"><span data-stu-id="94d31-119">Instead, if you need to do this, create a flag and set it in the [**Recognition**](inkrecognizercontext-recognition.md) event handler.</span></span> <span data-ttu-id="94d31-120">È quindi possibile eseguire il polling del flag per determinare quando modificare le proprietà **InkRecognizerContext** all'esterno del gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="94d31-120">Then you can poll that flag to determine when to change the **InkRecognizerContext** properties outside of the event handler.</span></span>

<span data-ttu-id="94d31-121">Questo metodo di evento è definito nell' \_ interfaccia IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="94d31-121">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="94d31-122">L' \_ interfaccia IInkEvents implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IRERecognitionWithAlternates.</span><span class="sxs-lookup"><span data-stu-id="94d31-122">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IRERecognitionWithAlternates.</span></span>

## <a name="requirements"></a><span data-ttu-id="94d31-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94d31-123">Requirements</span></span>



| <span data-ttu-id="94d31-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="94d31-124">Requirement</span></span> | <span data-ttu-id="94d31-125">Valore</span><span class="sxs-lookup"><span data-stu-id="94d31-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94d31-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94d31-126">Minimum supported client</span></span><br/> | <span data-ttu-id="94d31-127">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="94d31-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="94d31-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94d31-128">Minimum supported server</span></span><br/> | <span data-ttu-id="94d31-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="94d31-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="94d31-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94d31-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="94d31-131"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="94d31-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="94d31-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="94d31-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="94d31-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94d31-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="94d31-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94d31-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94d31-135">**Classe InkRecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="94d31-135">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

[<span data-ttu-id="94d31-136">**Metodo BackgroundRecognizeWithAlternates**</span><span class="sxs-lookup"><span data-stu-id="94d31-136">**BackgroundRecognizeWithAlternates Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)
</dt> <dt>

[<span data-ttu-id="94d31-137">**Recognize (metodo)**</span><span class="sxs-lookup"><span data-stu-id="94d31-137">**Recognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[<span data-ttu-id="94d31-138">**Interfaccia IInkRecognitionResult**</span><span class="sxs-lookup"><span data-stu-id="94d31-138">**IInkRecognitionResult Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 


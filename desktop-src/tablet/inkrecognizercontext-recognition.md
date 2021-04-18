---
description: Si verifica quando InkRecognizerContext ha generato risultati dal metodo BackgroundRecognize.
ms.assetid: 0cc319af-cd0b-4089-928b-cae6c86f6f61
title: Evento InkRecognizerContext. Recognition (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86da1a7470169f9f978e92a87f3e32f7e63acb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316831"
---
# <a name="inkrecognizercontextrecognition-event"></a><span data-ttu-id="13819-103">Evento InkRecognizerContext. Recognition</span><span class="sxs-lookup"><span data-stu-id="13819-103">InkRecognizerContext.Recognition event</span></span>

<span data-ttu-id="13819-104">Si verifica quando [**InkRecognizerContext**](inkrecognizercontext-class.md) ha generato risultati dal metodo [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) .</span><span class="sxs-lookup"><span data-stu-id="13819-104">Occurs when the [**InkRecognizerContext**](inkrecognizercontext-class.md) has generated results from the [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="13819-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13819-105">Syntax</span></span>


```C++
void Recognition(
  [in] BSTR                 RecognizedString,
  [in] VARIANT              CustomData,
  [in] InkRecognitionStatus RecognitionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="13819-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="13819-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13819-107">*RecognizedString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13819-107">*RecognizedString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13819-108">Testo del risultato del riconoscimento con la massima confidenza.</span><span class="sxs-lookup"><span data-stu-id="13819-108">The recognition result text with the highest confidence.</span></span>

<span data-ttu-id="13819-109">Per ulteriori informazioni sul tipo di dati BSTR, vedere [utilizzando la libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="13819-109">For more information about the BSTR data type, see the [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="13819-110">*CustomData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13819-110">*CustomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13819-111">Oggetto che contiene i dati personalizzati per il risultato del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="13819-111">The object that contains the custom data for the recognition result.</span></span>

<span data-ttu-id="13819-112">Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzando la libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="13819-112">For more information about the VARIANT structure, see the [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="13819-113">*RecognitionStatus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13819-113">*RecognitionStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13819-114">Stato di riconoscimento del risultato del riconoscimento più recente.</span><span class="sxs-lookup"><span data-stu-id="13819-114">The recognition status as of the most recent recognition result.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13819-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13819-115">Return value</span></span>

<span data-ttu-id="13819-116">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="13819-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13819-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="13819-117">Remarks</span></span>

<span data-ttu-id="13819-118">Il comportamento del Application Programming Interface (API) è imprevedibile se si tenta di ottenere l'accesso all'oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) originale dal gestore dell'evento di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="13819-118">The behavior of the application programming interface (API) is unpredictable if you try to gain access to the original [**InkRecognizerContext**](inkrecognizercontext-class.md) object from the recognition event handler.</span></span> <span data-ttu-id="13819-119">Non tentare di eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="13819-119">Do not attempt to do this.</span></span> <span data-ttu-id="13819-120">In alternativa, se è necessario eseguire questa operazione, creare un flag e impostarlo nel gestore dell'evento di [riconoscimento](ink-recognition.md) .</span><span class="sxs-lookup"><span data-stu-id="13819-120">Instead, if you need to do this, create a flag and set it in the [Recognition](ink-recognition.md) event handler.</span></span> <span data-ttu-id="13819-121">È quindi possibile eseguire il polling del flag per determinare quando modificare le proprietà **InkRecognizerContext** all'esterno del gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="13819-121">Then you can poll that flag to determine when to change the **InkRecognizerContext** properties outside of the event handler.</span></span>

<span data-ttu-id="13819-122">Questo metodo di evento è definito nell' \_ interfaccia IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="13819-122">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="13819-123">L' \_ interfaccia IInkEvents implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IRERecognition.</span><span class="sxs-lookup"><span data-stu-id="13819-123">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IRERecognition.</span></span>

## <a name="requirements"></a><span data-ttu-id="13819-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13819-124">Requirements</span></span>



| <span data-ttu-id="13819-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="13819-125">Requirement</span></span> | <span data-ttu-id="13819-126">Valore</span><span class="sxs-lookup"><span data-stu-id="13819-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13819-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13819-127">Minimum supported client</span></span><br/> | <span data-ttu-id="13819-128">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="13819-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="13819-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13819-129">Minimum supported server</span></span><br/> | <span data-ttu-id="13819-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="13819-130">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="13819-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13819-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="13819-132"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="13819-132"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="13819-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="13819-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="13819-134"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13819-134"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="13819-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13819-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13819-136">**Classe InkRecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="13819-136">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

[<span data-ttu-id="13819-137">**Metodo BackgroundRecognize**</span><span class="sxs-lookup"><span data-stu-id="13819-137">**BackgroundRecognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)
</dt> <dt>

[<span data-ttu-id="13819-138">**Enumerazione InkRecognitionStatus**</span><span class="sxs-lookup"><span data-stu-id="13819-138">**InkRecognitionStatus Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionstatus)
</dt> <dt>

[<span data-ttu-id="13819-139">**Recognize (metodo)**</span><span class="sxs-lookup"><span data-stu-id="13819-139">**Recognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[<span data-ttu-id="13819-140">**Interfaccia IInkRecognitionResult**</span><span class="sxs-lookup"><span data-stu-id="13819-140">**IInkRecognitionResult Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 


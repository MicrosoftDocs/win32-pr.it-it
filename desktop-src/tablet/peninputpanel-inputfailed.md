---
description: Deprecato. L'oggetto PenInputPanel è stato sostituito dal pannello di input di testo (TIP). Si verifica quando lo stato attivo per l'input cambia prima che l'oggetto PenInputPanel fosse in grado di inserire l'input dell'utente nel controllo associato.
ms.assetid: a5928f78-29d6-40e8-8f87-17c188e51ba9
title: Evento PenInputPanel. InputFailed (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 198c2b466dc03357d9851d7c8a6b7f44c6bf6884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319158"
---
# <a name="peninputpanelinputfailed-event"></a><span data-ttu-id="1df4b-104">PenInputPanel. InputFailed, evento</span><span class="sxs-lookup"><span data-stu-id="1df4b-104">PenInputPanel.InputFailed event</span></span>

<span data-ttu-id="1df4b-105">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="1df4b-105">Deprecated.</span></span> <span data-ttu-id="1df4b-106">L'oggetto [**PenInputPanel**](peninputpanel-class.md) è stato sostituito dal [Pannello di input di testo (tip)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="1df4b-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="1df4b-107">Si verifica quando lo stato attivo per l'input cambia prima che l'oggetto [**PenInputPanel**](peninputpanel-class.md) fosse in grado di inserire l'input dell'utente nel controllo associato.</span><span class="sxs-lookup"><span data-stu-id="1df4b-107">Occurs when input focus changes before the [**PenInputPanel**](peninputpanel-class.md) object was able to insert user input into the attached control.</span></span>

## <a name="syntax"></a><span data-ttu-id="1df4b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1df4b-108">Syntax</span></span>


```C++
HRESULT InputFailed(
  [in] long  hWnd,
  [in] long  Key,
  [in] BSTR  Text,
  [in] short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="1df4b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1df4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1df4b-110">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1df4b-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1df4b-111">Handle della finestra del controllo che ha richiamato l'oggetto [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="1df4b-111">The window handle of the control that invoked the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="1df4b-112">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="1df4b-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1df4b-113">Chiave virtuale corrispondente al tasto premuto.</span><span class="sxs-lookup"><span data-stu-id="1df4b-113">The virtual key corresponding to the key pressed.</span></span>

</dd> <dt>

<span data-ttu-id="1df4b-114">*Testo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1df4b-114">*Text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1df4b-115">Stringa da inserire nel controllo rappresentato dal parametro *HWND* quando è stato generato l'evento **InputFailed** .</span><span class="sxs-lookup"><span data-stu-id="1df4b-115">The string that was to be inserted into the control represented by the *hWnd* parameter when the **InputFailed** event was raised.</span></span>

<span data-ttu-id="1df4b-116">Per ulteriori informazioni sul tipo di dati BSTR, vedere [utilizzo della libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="1df4b-116">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="1df4b-117">*ShiftKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1df4b-117">*ShiftKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1df4b-118">Stato dei modificatori della tastiera, inclusi MAIUSC, CAPS, CTRL e ALT.</span><span class="sxs-lookup"><span data-stu-id="1df4b-118">The state of the keyboard modifiers, including SHIFT, CAPS, CTRL, and ALT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1df4b-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1df4b-119">Return value</span></span>

<span data-ttu-id="1df4b-120">Se l'evento ha esito positivo, viene restituito **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1df4b-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1df4b-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1df4b-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1df4b-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="1df4b-122">Remarks</span></span>

<span data-ttu-id="1df4b-123">L'evento **InputFailed** si verifica quando lo stato attivo per l'input viene modificato prima dell'inserimento dell'input utente nel controllo associato.</span><span class="sxs-lookup"><span data-stu-id="1df4b-123">The **InputFailed** event occurs when input focus changes before user input was inserted into the attached control.</span></span> <span data-ttu-id="1df4b-124">Ad esempio, se l'utente immette input penna nel riquadro di scrittura, quindi tocca un altro controllo di modifica prima che il riconoscimento abbia avuto la possibilità di terminare, questo evento viene generato.</span><span class="sxs-lookup"><span data-stu-id="1df4b-124">For example, if the user enters ink into the writing pad, then taps on another edit control before the recognizer has had a chance to finish, this event fires.</span></span>

<span data-ttu-id="1df4b-125">Usando l'handle di finestra passato in questo evento, è possibile scegliere di inserire il testo quando si verifica questo evento.</span><span class="sxs-lookup"><span data-stu-id="1df4b-125">Using the window handle passed into this event, you can choose to insert the text yourself when this event occurs.</span></span>

> [!Note]  
> <span data-ttu-id="1df4b-126">A partire da Microsoft Windows XP Tablet PC Edition 2005, l'evento **InputFailed** non viene più applicato.</span><span class="sxs-lookup"><span data-stu-id="1df4b-126">Starting with Microsoft Windows XP Tablet PC Edition 2005, the **InputFailed** event no longer applies.</span></span> <span data-ttu-id="1df4b-127">Il testo viene sempre inserito prima della modifica dello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="1df4b-127">Text is always inserted before focus changes.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1df4b-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1df4b-128">Requirements</span></span>



| <span data-ttu-id="1df4b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1df4b-129">Requirement</span></span> | <span data-ttu-id="1df4b-130">Valore</span><span class="sxs-lookup"><span data-stu-id="1df4b-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1df4b-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1df4b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1df4b-132">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1df4b-132">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1df4b-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1df4b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1df4b-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1df4b-134">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1df4b-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1df4b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="1df4b-136"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1df4b-136"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1df4b-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="1df4b-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="1df4b-138"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1df4b-138"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1df4b-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1df4b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df4b-140">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="1df4b-140">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 





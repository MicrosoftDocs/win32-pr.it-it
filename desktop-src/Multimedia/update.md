---
title: Aggiorna comando
description: Il comando Update ridisegna il frame corrente nel contesto di dispositivo specificato (DC). I dispositivi digitali video riconoscono questo comando.
ms.assetid: 51a83262-91d5-4852-ad17-bd62c14417b1
keywords:
- Aggiorna il comando Windows Multimedia
topic_type:
- apiref
api_name:
- update
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb0fc96d404efd8e2f657985ffa5a8861d3b4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518963"
---
# <a name="update-command"></a><span data-ttu-id="22a99-105">Aggiorna comando</span><span class="sxs-lookup"><span data-stu-id="22a99-105">update command</span></span>

<span data-ttu-id="22a99-106">Il comando Update ridisegna il frame corrente nel contesto di dispositivo specificato (DC).</span><span class="sxs-lookup"><span data-stu-id="22a99-106">The update command repaints the current frame into the specified device context (DC).</span></span> <span data-ttu-id="22a99-107">I dispositivi digitali video riconoscono questo comando.</span><span class="sxs-lookup"><span data-stu-id="22a99-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="22a99-108">Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="22a99-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("update %s %s %s"), 
  lpszDeviceID, 
  lpszHDC, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="22a99-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="22a99-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22a99-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="22a99-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="22a99-111">Identificatore di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="22a99-111">Identifier of an MCI device.</span></span> <span data-ttu-id="22a99-112">Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.</span><span class="sxs-lookup"><span data-stu-id="22a99-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="22a99-113"><span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszHDC*</span><span class="sxs-lookup"><span data-stu-id="22a99-113"><span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszHDC*</span></span>
</dt> <dd>

<span data-ttu-id="22a99-114">Handle di un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="22a99-114">Handle of a DC.</span></span> <span data-ttu-id="22a99-115">Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando di **aggiornamento** e i flag utilizzati da ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="22a99-115">The following table lists device types that recognize the **update** command and the flags used by each type.</span></span>



| <span data-ttu-id="22a99-116">Valore</span><span class="sxs-lookup"><span data-stu-id="22a99-116">Value</span></span>        | <span data-ttu-id="22a99-117">Significato</span><span class="sxs-lookup"><span data-stu-id="22a99-117">Meaning</span></span>                       | <span data-ttu-id="22a99-118">Significato</span><span class="sxs-lookup"><span data-stu-id="22a99-118">Meaning</span></span>         |
|--------------|-------------------------------|-----------------|
| <span data-ttu-id="22a99-119">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="22a99-119">digitalvideo</span></span> | <span data-ttu-id="22a99-120">HDC *HDC HDC hdc*  in *Rect*</span><span class="sxs-lookup"><span data-stu-id="22a99-120">hdc *hdc* hdc *hdc* at *rect*</span></span> | <span data-ttu-id="22a99-121">Paint HDC *HDC*</span><span class="sxs-lookup"><span data-stu-id="22a99-121">paint hdc *hdc*</span></span> |



 

<span data-ttu-id="22a99-122">Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszHDC** e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="22a99-122">The following table lists the flags that can be specified in the **lpszHDC** parameter and their meanings.</span></span>



| <span data-ttu-id="22a99-123">Valore</span><span class="sxs-lookup"><span data-stu-id="22a99-123">Value</span></span>               | <span data-ttu-id="22a99-124">Significato</span><span class="sxs-lookup"><span data-stu-id="22a99-124">Meaning</span></span>                                                                                                |
|---------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22a99-125">HDC *HDC*</span><span class="sxs-lookup"><span data-stu-id="22a99-125">hdc *hdc*</span></span>           | <span data-ttu-id="22a99-126">Specifica l'handle del controller di dominio da disegnare.</span><span class="sxs-lookup"><span data-stu-id="22a99-126">Specifies the handle of the DC to paint.</span></span>                                                               |
| <span data-ttu-id="22a99-127">HDC *HDC* in *Rect*</span><span class="sxs-lookup"><span data-stu-id="22a99-127">hdc *hdc* at *rect*</span></span> | <span data-ttu-id="22a99-128">Specifica il rettangolo di ridimensionamento rispetto al rettangolo client.</span><span class="sxs-lookup"><span data-stu-id="22a99-128">Specifies the clipping rectangle relative to the client rectangle.</span></span>                                     |
| <span data-ttu-id="22a99-129">Paint HDC *HDC*</span><span class="sxs-lookup"><span data-stu-id="22a99-129">paint hdc *hdc*</span></span>     | <span data-ttu-id="22a99-130">Disegna il controller di dominio quando l'applicazione riceve un messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) destinato a un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="22a99-130">Paints the DC when the application receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message intended for a DC.</span></span> |



 

<span data-ttu-id="22a99-131">Per specificare l'handle del controller di dominio, usare la stringa "HDC" seguita da una rappresentazione ASCII dell'handle.</span><span class="sxs-lookup"><span data-stu-id="22a99-131">To specify the handle of the DC, use the string "hdc" followed by an ASCII representation of the handle.</span></span> <span data-ttu-id="22a99-132">Il rettangolo viene specificato come **X1 Y1 Y1 2**.</span><span class="sxs-lookup"><span data-stu-id="22a99-132">The rectangle is specified as **X1 Y1 X2 Y2**.</span></span> <span data-ttu-id="22a99-133">Le coordinate **X1 Y1** specificano l'angolo superiore sinistro del rettangolo e le coordinate **X2 Y2** specificano la larghezza e l'altezza.</span><span class="sxs-lookup"><span data-stu-id="22a99-133">The coordinates **X1 Y1** specify the upper left corner of the rectangle, and the coordinates **X2 Y2** specify the width and height.</span></span>

</dd> <dt>

<span data-ttu-id="22a99-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="22a99-134"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="22a99-135">Può essere "Wait", "notify" o entrambi.</span><span class="sxs-lookup"><span data-stu-id="22a99-135">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="22a99-136">Per i dispositivi digitali video è possibile specificare anche "test".</span><span class="sxs-lookup"><span data-stu-id="22a99-136">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="22a99-137">Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="22a99-137">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22a99-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22a99-138">Return Value</span></span>

<span data-ttu-id="22a99-139">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="22a99-139">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="22a99-140">Esempio</span><span class="sxs-lookup"><span data-stu-id="22a99-140">Examples</span></span>

<span data-ttu-id="22a99-141">Il comando seguente aggiorna l'intera finestra di visualizzazione usata dal dispositivo "Movie".</span><span class="sxs-lookup"><span data-stu-id="22a99-141">The following command updates the entire display window used by the "movie" device.</span></span> <span data-ttu-id="22a99-142">Il numero 203 è un handle per un controller di dominio ottenuto dalla funzione [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) .</span><span class="sxs-lookup"><span data-stu-id="22a99-142">The number 203 is a handle to a DC obtained from the [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) function.</span></span>

``` syntax
update movie hdc 203
```

## <a name="requirements"></a><span data-ttu-id="22a99-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22a99-143">Requirements</span></span>



| <span data-ttu-id="22a99-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="22a99-144">Requirement</span></span> | <span data-ttu-id="22a99-145">Valore</span><span class="sxs-lookup"><span data-stu-id="22a99-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="22a99-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22a99-146">Minimum supported client</span></span><br/> | <span data-ttu-id="22a99-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="22a99-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="22a99-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22a99-148">Minimum supported server</span></span><br/> | <span data-ttu-id="22a99-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="22a99-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="22a99-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22a99-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22a99-151">MCI</span><span class="sxs-lookup"><span data-stu-id="22a99-151">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="22a99-152">Stringhe di comando MCI</span><span class="sxs-lookup"><span data-stu-id="22a99-152">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 


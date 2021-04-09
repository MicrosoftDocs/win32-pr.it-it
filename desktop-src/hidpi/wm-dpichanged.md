---
title: Messaggio WM_DPICHANGED (WinUser. h)
description: Inviato quando viene modificato il valore dpi (punti per pollice) effettivo per una finestra.
ms.assetid: 97C458F2-89CD-45FF-ABEE-F158A3BCE0B8
keywords:
- Messaggio WM_DPICHANGED alto DPI
topic_type:
- apiref
api_name:
- WM_DPICHANGED
api_location:
- WinUser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aafbce1e784e1f205f0d32e045785125c1fb5aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741834"
---
# <a name="wm_dpichanged-message"></a><span data-ttu-id="0d8a1-104">\_Messaggio DPICHANGED WM</span><span class="sxs-lookup"><span data-stu-id="0d8a1-104">WM\_DPICHANGED message</span></span>

<span data-ttu-id="0d8a1-105">Inviato quando viene modificato il valore dpi (punti per pollice) effettivo per una finestra.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-105">Sent when the effective dots per inch (dpi) for a window has changed.</span></span> <span data-ttu-id="0d8a1-106">Il valore DPI è il fattore di scala per una finestra.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-106">The DPI is the scale factor for a window.</span></span> <span data-ttu-id="0d8a1-107">Sono presenti più eventi che possono causare la modifica del valore DPI.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-107">There are multiple events that can cause the DPI to change.</span></span> <span data-ttu-id="0d8a1-108">Nell'elenco seguente sono indicate le possibili cause della modifica in DPI.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-108">The following list indicates the possible causes for the change in DPI.</span></span>

-   <span data-ttu-id="0d8a1-109">La finestra viene spostata in un nuovo monitor con un valore DPI diverso.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-109">The window is moved to a new monitor that has a different DPI.</span></span>
-   <span data-ttu-id="0d8a1-110">Viene modificato il valore DPI del monitoraggio che ospita la finestra.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-110">The DPI of the monitor hosting the window changes.</span></span>

<span data-ttu-id="0d8a1-111">Il valore DPI corrente per una finestra è sempre uguale all'ultimo valore DPI inviato da **WM \_ DPICHANGED**.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-111">The current DPI for a window always equals the last DPI sent by **WM\_DPICHANGED**.</span></span> <span data-ttu-id="0d8a1-112">Questo è il fattore di scala che la finestra deve ridimensionare per i thread che sono consapevoli delle modifiche DPI.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-112">This is the scale factor that the window should be scaling to for threads that are aware of DPI changes.</span></span>


```C++
#define WM_DPICHANGED       0x02E0
```



## <a name="parameters"></a><span data-ttu-id="0d8a1-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d8a1-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d8a1-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d8a1-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d8a1-115">Il [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) del *wParam* contiene il valore dell'asse Y del nuovo dpi della finestra.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of the *wParam* contains the Y-axis value of the new dpi of the window.</span></span> <span data-ttu-id="0d8a1-116">Il [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) del *wParam* contiene il valore dell'asse X del nuovo valore dpi della finestra.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-116">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the *wParam* contains the X-axis value of the new DPI of the window.</span></span> <span data-ttu-id="0d8a1-117">Ad esempio, 96, 120, 144 o 192.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-117">For example, 96, 120, 144, or 192.</span></span> <span data-ttu-id="0d8a1-118">I valori dell'asse X e l'asse Y sono identici per le app di Windows.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-118">The values of the X-axis and the Y-axis are identical for Windows apps.</span></span>

</dd> <dt>

<span data-ttu-id="0d8a1-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d8a1-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d8a1-120">Puntatore a una struttura [**Rect**](/windows/desktop/api/windef/ns-windef-rect) che fornisce le dimensioni suggerite e la posizione della finestra corrente ridimensionata per il nuovo valore dpi.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-120">A pointer to a [**RECT**](/windows/desktop/api/windef/ns-windef-rect) structure that provides a suggested size and position of the current window scaled for the new DPI.</span></span> <span data-ttu-id="0d8a1-121">Si prevede che le app riposizionano e ridimensionano le finestre in base ai suggerimenti forniti da *lParam* durante la gestione di questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-121">The expectation is that apps will reposition and resize windows based on the suggestions provided by *lParam* when handling this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d8a1-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d8a1-122">Return value</span></span>

<span data-ttu-id="0d8a1-123">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-123">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d8a1-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d8a1-124">Remarks</span></span>

<span data-ttu-id="0d8a1-125">Questo messaggio è pertinente solo per le applicazioni con **\_ \_ \_ \_ riconoscimento dpi del monitor** o per la **consapevolezza dpi per thread \_ \_ \_ \_ compatibili con monitoraggio** .</span><span class="sxs-lookup"><span data-stu-id="0d8a1-125">This message is only relevant for **PROCESS\_PER\_MONITOR\_DPI\_AWARE** applications or **DPI\_AWARENESS\_PER\_MONITOR\_AWARE** threads.</span></span> <span data-ttu-id="0d8a1-126">È possibile che venga ricevuta in determinate modifiche DPI se la finestra di primo livello o il processo è in esecuzione con compatibilità **dpi** o **compatibile con DPI di sistema**, ma in tali situazioni può essere tranquillamente ignorato.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-126">It may be received on certain DPI changes if your top-level window or process is running as **DPI unaware** or **system DPI aware**, but in those situations it can be safely ignored.</span></span> <span data-ttu-id="0d8a1-127">Per ulteriori informazioni sui diversi tipi di riconoscimento, vedere [**processo \_ dpi \_ Awareness**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) e [**dpi \_ Awareness**](/windows/desktop/api/windef/ne-windef-dpi_awareness).</span><span class="sxs-lookup"><span data-stu-id="0d8a1-127">For more information about the different types of awareness, see [**PROCESS\_DPI\_AWARENESS**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) and [**DPI\_AWARENESS**](/windows/desktop/api/windef/ne-windef-dpi_awareness).</span></span> <span data-ttu-id="0d8a1-128">Le versioni precedenti di Windows richiedevano il riconoscimento DPI per essere associato al livello di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-128">Older versions of Windows required DPI awareness to be tied at the level of an application.</span></span> <span data-ttu-id="0d8a1-129">Queste app usano **la \_ \_ consapevolezza dpi del processo**.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-129">Those apps use **PROCESS\_DPI\_AWARENESS**.</span></span> <span data-ttu-id="0d8a1-130">Attualmente, la consapevolezza DPI è associata a thread e singole finestre anziché all'intera applicazione.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-130">Currently, DPI awareness is tied to threads and individual windows rather than the entire application.</span></span> <span data-ttu-id="0d8a1-131">Queste app usano **la \_ consapevolezza dpi**.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-131">These apps use **DPI\_AWARENESS**.</span></span>

<span data-ttu-id="0d8a1-132">È sufficiente usare l'asse X o il valore dell'asse Y durante il ridimensionamento dell'applicazione perché sono uguali.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-132">You only need to use either the X-axis or the Y-axis value when scaling your application since they are the same.</span></span>

<span data-ttu-id="0d8a1-133">Per gestire correttamente questo messaggio, sarà necessario ridimensionare e riposizionare la finestra in base ai suggerimenti forniti da *lParam* e usando [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="0d8a1-133">In order to handle this message correctly, you will need to resize and reposition your window based on the suggestions provided by *lParam* and using [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="0d8a1-134">Se non si esegue questa operazione, la finestra aumenterà o verrà ridotta rispetto a tutti gli altri elementi del nuovo monitor.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-134">If you do not do this, your window will grow or shrink with respect to everything else on the new monitor.</span></span> <span data-ttu-id="0d8a1-135">Se, ad esempio, un utente utilizza più monitoraggi e trascina la finestra da un monitor 96 DPI a un monitor 192 DPI, la finestra apparirà la metà delle dimensioni rispetto ad altri elementi del monitor 192 DPI.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-135">For example, if a user is using multiple monitors and drags your window from a 96 DPI monitor to a 192 DPI monitor, your window will appear to be half as large with respect to other items on the 192 DPI monitor.</span></span>

<span data-ttu-id="0d8a1-136">Il valore di base di DPI è definito **come \_ \_ \_ DPI dello schermo predefinito dell'utente** , che è impostato su 96.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-136">The base value of DPI is defined as **USER\_DEFAULT\_SCREEN\_DPI** which is set to 96.</span></span> <span data-ttu-id="0d8a1-137">Per determinare il fattore di scalabilità per un monitoraggio, impostare il valore DPI e dividere in base a **\_ \_ \_ DPI dello schermo predefinito dell'utente**.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-137">To determine the scaling factor for a monitor, take the DPI value and divide by **USER\_DEFAULT\_SCREEN\_DPI**.</span></span> <span data-ttu-id="0d8a1-138">Nella tabella seguente vengono forniti alcuni valori DPI di esempio e i fattori di scala associati.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-138">The following table provides some sample DPI values and associated scaling factors.</span></span>



| <span data-ttu-id="0d8a1-139">Valore DPI</span><span class="sxs-lookup"><span data-stu-id="0d8a1-139">DPI value</span></span> | <span data-ttu-id="0d8a1-140">Percentuale di ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="0d8a1-140">Scaling percentage</span></span> |
|-----------|--------------------|
| <span data-ttu-id="0d8a1-141">96</span><span class="sxs-lookup"><span data-stu-id="0d8a1-141">96</span></span>        | <span data-ttu-id="0d8a1-142">100%</span><span class="sxs-lookup"><span data-stu-id="0d8a1-142">100%</span></span>               |
| <span data-ttu-id="0d8a1-143">120</span><span class="sxs-lookup"><span data-stu-id="0d8a1-143">120</span></span>       | <span data-ttu-id="0d8a1-144">125%</span><span class="sxs-lookup"><span data-stu-id="0d8a1-144">125%</span></span>               |
| <span data-ttu-id="0d8a1-145">144</span><span class="sxs-lookup"><span data-stu-id="0d8a1-145">144</span></span>       | <span data-ttu-id="0d8a1-146">150%</span><span class="sxs-lookup"><span data-stu-id="0d8a1-146">150%</span></span>               |
| <span data-ttu-id="0d8a1-147">192</span><span class="sxs-lookup"><span data-stu-id="0d8a1-147">192</span></span>       | <span data-ttu-id="0d8a1-148">200%</span><span class="sxs-lookup"><span data-stu-id="0d8a1-148">200%</span></span>               |



 

<span data-ttu-id="0d8a1-149">Nell'esempio seguente viene fornito un gestore delle modifiche DPI di esempio.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-149">The following example provides a sample DPI change handler.</span></span>


```C++
    case WM_DPICHANGED:
    {
        g_dpi = HIWORD(wParam);
        UpdateDpiDependentFontsAndResources();

        RECT* const prcNewWindow = (RECT*)lParam;
        SetWindowPos(hWnd,
            NULL,
            prcNewWindow ->left,
            prcNewWindow ->top,
            prcNewWindow->right - prcNewWindow->left,
            prcNewWindow->bottom - prcNewWindow->top,
            SWP_NOZORDER | SWP_NOACTIVATE);
        break;
    }
```



<span data-ttu-id="0d8a1-150">Il codice seguente consente di ridimensionare in modo lineare un valore da 100% (96 DPI) a un valore DPI arbitrario definito da *g \_ dpi*.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-150">The following code linearly scales a value from 100% (96 DPI) to an arbitrary DPI defined by *g\_dpi*.</span></span>


```C++
    INT iBorderWidth100 = 5;
    iBorderWidth = MulDiv(iBorderWidth100, g_dpi, USER_DEFAULT_SCREEN_DPI);
```



<span data-ttu-id="0d8a1-151">Un modo alternativo per ridimensionare un valore consiste nel convertire il valore DPI in un fattore di scala e usarlo.</span><span class="sxs-lookup"><span data-stu-id="0d8a1-151">An alternative way to scale a value is to convert the DPI value into a scale factor and use that.</span></span>


```C++
    INT iBorderWidth100 = 5;
    FLOAT fscale = (float) g_dpi / USER_DEFAULT_SCREEN_DPI;
    iBorderWidth = iBorderWidth100 * fscale;
```



## <a name="requirements"></a><span data-ttu-id="0d8a1-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d8a1-152">Requirements</span></span>



| <span data-ttu-id="0d8a1-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d8a1-153">Requirement</span></span> | <span data-ttu-id="0d8a1-154">Valore</span><span class="sxs-lookup"><span data-stu-id="0d8a1-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0d8a1-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d8a1-155">Minimum supported client</span></span><br/> | <span data-ttu-id="0d8a1-156">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0d8a1-156">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0d8a1-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d8a1-157">Minimum supported server</span></span><br/> | <span data-ttu-id="0d8a1-158">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d8a1-158">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0d8a1-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d8a1-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d8a1-160"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d8a1-160"><dt>WinUser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d8a1-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d8a1-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d8a1-162">**\_riconoscimento dpi**</span><span class="sxs-lookup"><span data-stu-id="0d8a1-162">**DPI\_AWARENESS**</span></span>](/windows/desktop/api/windef/ne-windef-dpi_awareness)
</dt> <dt>

[<span data-ttu-id="0d8a1-163">**\_riconoscimento dpi \_ processo**</span><span class="sxs-lookup"><span data-stu-id="0d8a1-163">**PROCESS\_DPI\_AWARENESS**</span></span>](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)
</dt> </dl>

 


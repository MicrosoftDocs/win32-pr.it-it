---
title: Messaggio WM_GETDPISCALEDSIZE (winuser. h)
description: Questo messaggio indica al sistema operativo che la finestra verrà ridimensionata in dimensioni diverse da quelle predefinite.
ms.assetid: 038CAA21-0944-45D3-8C40-A6498F36D9E4
keywords:
- Messaggio WM_GETDPISCALEDSIZE alto DPI
topic_type:
- apiref
api_name:
- WM_GETDPISCALEDSIZE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95631e51247d7919307f36dd0af10c72621a612
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476858"
---
# <a name="wm_getdpiscaledsize-message"></a><span data-ttu-id="bc66e-104">\_Messaggio GETDPISCALEDSIZE WM</span><span class="sxs-lookup"><span data-stu-id="bc66e-104">WM\_GETDPISCALEDSIZE message</span></span>

<span data-ttu-id="bc66e-105">Questo messaggio indica al sistema operativo che la finestra verrà ridimensionata in dimensioni diverse da quelle predefinite.</span><span class="sxs-lookup"><span data-stu-id="bc66e-105">This message tells the operating system that the window will be sized to dimensions other than the default.</span></span>

<span data-ttu-id="bc66e-106">Questo messaggio viene inviato alle finestre di primo livello con un [ \_ \_ contesto](dpi-awareness-context.md) di compatibilità dpi di per monitor V2 prima dell'invio di un messaggio [**WM \_ DPICHANGED**](wm-dpichanged.md) e consente alla finestra di calcolare la dimensione desiderata per la modifica dpi in sospeso.</span><span class="sxs-lookup"><span data-stu-id="bc66e-106">This message is sent to top-level windows with a [DPI\_AWARENESS\_CONTEXT](dpi-awareness-context.md) of Per Monitor v2 before a [**WM\_DPICHANGED**](wm-dpichanged.md) message is sent, and allows the window to compute its desired size for the pending DPI change.</span></span> <span data-ttu-id="bc66e-107">Poiché il ridimensionamento DPI lineare è il comportamento predefinito, questa opzione è utile solo negli scenari in cui la finestra vuole ridimensionare in modo non lineare.</span><span class="sxs-lookup"><span data-stu-id="bc66e-107">As linear DPI scaling is the default behavior, this is only useful in scenarios where the window wants to scale non-linearly.</span></span> <span data-ttu-id="bc66e-108">Se l'applicazione risponde a questo messaggio, la dimensione risultante sarà il rettangolo candidato inviato a **WM \_ DPICHANGED**.</span><span class="sxs-lookup"><span data-stu-id="bc66e-108">If the application responds to this message, the resulting size will be the candidate rectangle send to **WM\_DPICHANGED**.</span></span>

<span data-ttu-id="bc66e-109">Utilizzare questo messaggio per modificare la dimensione del Rect fornito con [**WM \_ DPICHANGED**](wm-dpichanged.md).</span><span class="sxs-lookup"><span data-stu-id="bc66e-109">Use this message to alter the size of the rect that is provided with [**WM\_DPICHANGED**](wm-dpichanged.md).</span></span>


```C++
#define WM_GETDPISCALEDSIZE       0x02E4
```



## <a name="parameters"></a><span data-ttu-id="bc66e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc66e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc66e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bc66e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc66e-112">Il WPARAM contiene un valore DPI.</span><span class="sxs-lookup"><span data-stu-id="bc66e-112">The WPARAM contains a DPI value.</span></span> <span data-ttu-id="bc66e-113">Le dimensioni della finestra ridimensionate che l'applicazione deve impostare devono essere calcolate come se la finestra fosse in grado di passare a questo DPI.</span><span class="sxs-lookup"><span data-stu-id="bc66e-113">The scaled window size that the application would set needs to be computed as if the window were to switch to this DPI.</span></span>

</dd> <dt>

<span data-ttu-id="bc66e-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc66e-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc66e-115">LPARAM è un puntatore in/out a uno struct di dimensioni.</span><span class="sxs-lookup"><span data-stu-id="bc66e-115">The LPARAM is an in/out pointer to a SIZE struct.</span></span> <span data-ttu-id="bc66e-116">Il \_ \_ valore in in lParam è la dimensione in sospeso della finestra dopo uno spostamento avviato dall'utente o una chiamata a [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="bc66e-116">The \_In\_ value in the LPARAM is the pending size of the window after a user-initiated move or a call to [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="bc66e-117">Se è in corso il ridimensionamento della finestra, questa dimensione non corrisponde necessariamente alla dimensione corrente della finestra al momento della ricezione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="bc66e-117">If the window is being resized, this size is not necessarily the same as the window's current size at the time this message is received.</span></span>

<span data-ttu-id="bc66e-118">Il \_ \_ valore out in lParam deve essere scritto dall'applicazione per specificare le dimensioni della finestra ridimensionate desiderate corrispondenti al valore DPI fornito in wParam.</span><span class="sxs-lookup"><span data-stu-id="bc66e-118">The \_Out\_ value in the LPARAM should be written to by the application to specify the desired scaled window size corresponding to the provided DPI value in the WPARAM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc66e-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc66e-119">Return value</span></span>

<span data-ttu-id="bc66e-120">La funzione restituisce un valore BOOL.</span><span class="sxs-lookup"><span data-stu-id="bc66e-120">The function returns a BOOL.</span></span> <span data-ttu-id="bc66e-121">Restituisce TRUE indica che è stata calcolata una nuova dimensione.</span><span class="sxs-lookup"><span data-stu-id="bc66e-121">Returning TRUE indicates that a new size has been computed.</span></span> <span data-ttu-id="bc66e-122">Restituisce FALSE indica che il messaggio non verrà gestito e il ridimensionamento DPI lineare predefinito verrà applicato alla finestra.</span><span class="sxs-lookup"><span data-stu-id="bc66e-122">Returning FALSE indicates that the message will not be handled, and the default linear DPI scaling will apply to the window.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc66e-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc66e-123">Remarks</span></span>

<span data-ttu-id="bc66e-124">Questo messaggio viene inviato solo a finestre di primo livello con un contesto di compatibilità DPI di per monitor V2.</span><span class="sxs-lookup"><span data-stu-id="bc66e-124">This message is only sent to top-level windows which have a DPI awareness context of Per Monitor v2.</span></span>

<span data-ttu-id="bc66e-125">Questo evento è necessario per facilitare il ridimensionamento non lineare normale e garantisce che la posizione di Windows rimanga costante in relazione al cursore e quando si spostano avanti e indietro tra i monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="bc66e-125">This event is necessary to facilitate graceful non-linear scaling, and ensures that the windows's position remains constant in relationship to the cursor and when moving back and forth across monitors.</span></span>

<span data-ttu-id="bc66e-126">Non esiste alcuna gestione predefinita specifica del messaggio in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="bc66e-126">There is no specific default handling of this message in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="bc66e-127">Come per tutti i messaggi non gestiti in modo esplicito, [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) restituirà zero per questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="bc66e-127">As for all messages it does not explicitly handle, [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) will return zero for this message.</span></span> <span data-ttu-id="bc66e-128">Come indicato in precedenza, questo ritorno indica al sistema di usare il comportamento lineare predefinito.</span><span class="sxs-lookup"><span data-stu-id="bc66e-128">As noted above, this return tells the system to use the default linear behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc66e-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc66e-129">Requirements</span></span>



| <span data-ttu-id="bc66e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc66e-130">Requirement</span></span> | <span data-ttu-id="bc66e-131">Valore</span><span class="sxs-lookup"><span data-stu-id="bc66e-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bc66e-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc66e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bc66e-133">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc66e-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="bc66e-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc66e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bc66e-135">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="bc66e-135">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bc66e-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc66e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc66e-137"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc66e-137"><dt>Winuser.h</dt></span></span> </dl> |



 


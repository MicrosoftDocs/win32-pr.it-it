---
description: Il \_ messaggio WM CTLCOLOR viene usato nelle versioni di Windows a 16 bit per modificare la combinazione di colori delle caselle di riepilogo, le caselle di riepilogo di caselle combinate, le finestre di messaggio, i controlli pulsante, i controlli di modifica, i controlli statici e le finestre di dialogo. Nota per informazioni correlate a questo messaggio e alle versioni a 32 bit di Windows, vedere la sezione Osservazioni.
ms.assetid: e654cf48-550f-4210-9952-20470b9a397a
title: Messaggio WM_CTLCOLOR (WindowsX. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8166979c17b7d2eef50af062e5df13712e9d32ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328953"
---
# <a name="wm_ctlcolor-message"></a><span data-ttu-id="507eb-103">\_Messaggio CTLCOLOR WM</span><span class="sxs-lookup"><span data-stu-id="507eb-103">WM\_CTLCOLOR message</span></span>

<span data-ttu-id="507eb-104">Il messaggio **WM \_ CTLCOLOR** viene usato nelle versioni di Windows a 16 bit per modificare la combinazione di colori delle caselle di riepilogo, le caselle di riepilogo di caselle combinate, le finestre di messaggio, i controlli pulsante, i controlli di modifica, i controlli statici e le finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="507eb-104">The **WM\_CTLCOLOR** message is used in 16-bit versions of Windows to change the color scheme of list boxes, the list boxes of combo boxes, message boxes, button controls, edit controls, static controls, and dialog boxes.</span></span>

> [!Note]  
> <span data-ttu-id="507eb-105">Per informazioni correlate a questo messaggio e alle versioni a 32 bit di Windows, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="507eb-105">For information related to this message and 32-bit versions of Windows, see Remarks.</span></span>

 


```C++
  WM_CTLCOLOR

  WPARAM wParam;
  LPARAM lParam;
    
```



## <a name="parameters"></a><span data-ttu-id="507eb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="507eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="507eb-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="507eb-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="507eb-108">Handle per la finestra di destinazione.</span><span class="sxs-lookup"><span data-stu-id="507eb-108">A handle to destination window.</span></span>

</dd> <dt>

<span data-ttu-id="507eb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="507eb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="507eb-110">Handle per un contesto di visualizzazione (DC).</span><span class="sxs-lookup"><span data-stu-id="507eb-110">A handle to a display context (DC).</span></span>

</dd> <dt>

<span data-ttu-id="507eb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="507eb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="507eb-112">Handle per una finestra figlio (controllo).</span><span class="sxs-lookup"><span data-stu-id="507eb-112">A handle to a child window (control).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="507eb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="507eb-113">Return value</span></span>

<span data-ttu-id="507eb-114">Se un'applicazione elabora il messaggio, restituisce un handle a un pennello.</span><span class="sxs-lookup"><span data-stu-id="507eb-114">If an application processes this message, it returns a handle to a brush.</span></span> <span data-ttu-id="507eb-115">Il sistema utilizza il pennello per disegnare lo sfondo del controllo.</span><span class="sxs-lookup"><span data-stu-id="507eb-115">The system uses the brush to paint the background of the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="507eb-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="507eb-116">Remarks</span></span>

<span data-ttu-id="507eb-117">Il messaggio **WM \_ CTLCOLOR** di Windows a 16 bit è stato sostituito da notifiche più specifiche.</span><span class="sxs-lookup"><span data-stu-id="507eb-117">The **WM\_CTLCOLOR** message from 16-bit Windows has been replaced by more specific notifications.</span></span> <span data-ttu-id="507eb-118">Queste sostituzioni includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="507eb-118">These replacements include the following:</span></span>

-   [<span data-ttu-id="507eb-119">**\_CTLCOLORBTN WM**</span><span class="sxs-lookup"><span data-stu-id="507eb-119">**WM\_CTLCOLORBTN**</span></span>](../controls/wm-ctlcolorbtn.md)
-   [<span data-ttu-id="507eb-120">**\_CTLCOLOREDIT WM**</span><span class="sxs-lookup"><span data-stu-id="507eb-120">**WM\_CTLCOLOREDIT**</span></span>](../controls/wm-ctlcoloredit.md)
-   [<span data-ttu-id="507eb-121">**\_CTLCOLORDLG WM**</span><span class="sxs-lookup"><span data-stu-id="507eb-121">**WM\_CTLCOLORDLG**</span></span>](../dlgbox/wm-ctlcolordlg.md)
-   [<span data-ttu-id="507eb-122">**\_CTLCOLORLISTBOX WM**</span><span class="sxs-lookup"><span data-stu-id="507eb-122">**WM\_CTLCOLORLISTBOX**</span></span>](../controls/wm-ctlcolorlistbox.md)
-   [<span data-ttu-id="507eb-123">**\_CTLCOLORSCROLLBAR WM**</span><span class="sxs-lookup"><span data-stu-id="507eb-123">**WM\_CTLCOLORSCROLLBAR**</span></span>](../controls/wm-ctlcolorscrollbar.md)
-   [<span data-ttu-id="507eb-124">**\_CTLCOLORSTATIC WM**</span><span class="sxs-lookup"><span data-stu-id="507eb-124">**WM\_CTLCOLORSTATIC**</span></span>](../controls/wm-ctlcolorstatic.md)

## <a name="requirements"></a><span data-ttu-id="507eb-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="507eb-125">Requirements</span></span>



| <span data-ttu-id="507eb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="507eb-126">Requirement</span></span> | <span data-ttu-id="507eb-127">Valore</span><span class="sxs-lookup"><span data-stu-id="507eb-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="507eb-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="507eb-128">Header</span></span><br/> | <dl> <span data-ttu-id="507eb-129"><dt>WindowsX. h</dt></span><span class="sxs-lookup"><span data-stu-id="507eb-129"><dt>WindowsX.h</dt></span></span> </dl> |



 

 

---
title: Messaggio DM_SETDEFID (winuser. h)
description: Modifica l'identificatore del pulsante di push predefinito per una finestra di dialogo.
ms.assetid: 30720fa1-48cb-42d4-8370-87bdbaa34600
keywords:
- Finestre di dialogo DM_SETDEFID messaggio
topic_type:
- apiref
api_name:
- DM_SETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ceda9ac9e8fd399604e9c55431b8fcd74646f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518879"
---
# <a name="dm_setdefid-message"></a><span data-ttu-id="87ddd-104">\_Messaggio DM SETDEFID</span><span class="sxs-lookup"><span data-stu-id="87ddd-104">DM\_SETDEFID message</span></span>

<span data-ttu-id="87ddd-105">Modifica l'identificatore del pulsante di push predefinito per una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="87ddd-105">Changes the identifier of the default push button for a dialog box.</span></span>


```C++
#define WM_USER              0x0400
#define DM_SETDEFID         (WM_USER+1)
```



## <a name="parameters"></a><span data-ttu-id="87ddd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="87ddd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87ddd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87ddd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87ddd-108">Identificatore di un controllo pulsante di comando che diventerà il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="87ddd-108">The identifier of a push button control that will become the default.</span></span>

</dd> <dt>

<span data-ttu-id="87ddd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87ddd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="87ddd-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="87ddd-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87ddd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87ddd-111">Return value</span></span>

<span data-ttu-id="87ddd-112">Il valore restituito è sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="87ddd-112">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="87ddd-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="87ddd-113">Remarks</span></span>

<span data-ttu-id="87ddd-114">Questo messaggio viene elaborato dalla funzione [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) .</span><span class="sxs-lookup"><span data-stu-id="87ddd-114">This message is processed by the [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) function.</span></span> <span data-ttu-id="87ddd-115">Per impostare il pulsante di push predefinito, la funzione può inviare i messaggi [**di \_ tipo**](../controls/bm-setstyle.md) " [**WM \_ GETDLGCODE**](wm-getdlgcode.md) " e "BM" al controllo specificato e al pulsante di push predefinito corrente.</span><span class="sxs-lookup"><span data-stu-id="87ddd-115">To set the default push button, the function can send [**WM\_GETDLGCODE**](wm-getdlgcode.md) and [**BM\_SETSTYLE**](../controls/bm-setstyle.md) messages to the specified control and the current default push button.</span></span>

<span data-ttu-id="87ddd-116">L'uso del messaggio **DM \_ SETDEFID** può comportare la visualizzazione di più di un pulsante con lo stato predefinito del pulsante di push.</span><span class="sxs-lookup"><span data-stu-id="87ddd-116">Using the **DM\_SETDEFID** message can result in more than one button appearing to have the default push button state.</span></span> <span data-ttu-id="87ddd-117">Quando il sistema Visualizza una finestra di dialogo, disegna il primo pulsante di push nel modello di finestra di dialogo con il bordo dello stato predefinito.</span><span class="sxs-lookup"><span data-stu-id="87ddd-117">When the system brings up a dialog, it draws the first push button in the dialog template with the default state border.</span></span> <span data-ttu-id="87ddd-118">L'invio di un messaggio **DM \_ SETDEFID** per modificare il pulsante predefinito non ridurrà sempre il bordo di stato predefinito dal primo pulsante di push.</span><span class="sxs-lookup"><span data-stu-id="87ddd-118">Sending a **DM\_SETDEFID** message to change the default button will not always remove the default state border from the first push button.</span></span> <span data-ttu-id="87ddd-119">In questi casi, l'applicazione deve inviare un messaggio di [**\_ tipo BM**](../controls/bm-setstyle.md) per modificare il primo stile del bordo del pulsante di push.</span><span class="sxs-lookup"><span data-stu-id="87ddd-119">In these cases, the application should send a [**BM\_SETSTYLE**](../controls/bm-setstyle.md) message to change the first push button border style.</span></span>

## <a name="requirements"></a><span data-ttu-id="87ddd-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87ddd-120">Requirements</span></span>



| <span data-ttu-id="87ddd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="87ddd-121">Requirement</span></span> | <span data-ttu-id="87ddd-122">Valore</span><span class="sxs-lookup"><span data-stu-id="87ddd-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87ddd-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87ddd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="87ddd-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="87ddd-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="87ddd-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87ddd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="87ddd-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="87ddd-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="87ddd-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87ddd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="87ddd-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87ddd-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87ddd-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87ddd-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="87ddd-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="87ddd-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="87ddd-131">**DefDlgProc**</span><span class="sxs-lookup"><span data-stu-id="87ddd-131">**DefDlgProc**</span></span>](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="87ddd-132">**\_GETDEFID DM**</span><span class="sxs-lookup"><span data-stu-id="87ddd-132">**DM\_GETDEFID**</span></span>](dm-getdefid.md)
</dt> <dt>

[<span data-ttu-id="87ddd-133">**\_GETDLGCODE WM**</span><span class="sxs-lookup"><span data-stu-id="87ddd-133">**WM\_GETDLGCODE**</span></span>](wm-getdlgcode.md)
</dt> <dt>

<span data-ttu-id="87ddd-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="87ddd-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="87ddd-135">Finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="87ddd-135">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="87ddd-136">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="87ddd-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="87ddd-137">**distile BM \_**</span><span class="sxs-lookup"><span data-stu-id="87ddd-137">**BM\_SETSTYLE**</span></span>](../controls/bm-setstyle.md)
</dt> <dt>

[<span data-ttu-id="87ddd-138">**\_SETLIMITTEXT em**</span><span class="sxs-lookup"><span data-stu-id="87ddd-138">**EM\_SETLIMITTEXT**</span></span>](../controls/em-setlimittext.md)
</dt> </dl>

 


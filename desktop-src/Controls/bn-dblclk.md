---
title: Codice di notifica BN_DBLCLK (winuser. h)
description: Inviato quando l'utente fa doppio clic su un pulsante.
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- Controlli di Windows per il codice di notifica BN_DBLCLK
topic_type:
- apiref
api_name:
- BN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04c6bf52e213056d85d3a6d038bedb83754a27e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048129"
---
# <a name="bn_dblclk-notification-code"></a><span data-ttu-id="b26b4-104">\_Codice di notifica DBLCLK BN</span><span class="sxs-lookup"><span data-stu-id="b26b4-104">BN\_DBLCLK notification code</span></span>

<span data-ttu-id="b26b4-105">Inviato quando l'utente fa doppio clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="b26b4-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="b26b4-106">Questo codice di notifica viene inviato automaticamente per i pulsanti [**BS \_ UserButton**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)e [**BS \_ OWNERDRAW**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b26b4-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="b26b4-107">Altri tipi di pulsante inviano BN \_ DBLCLK solo se hanno lo stile di [**\_ notifica BS**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b26b4-107">Other button types send BN\_DBLCLK only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="b26b4-108">La finestra padre del pulsante riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="b26b4-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="b26b4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b26b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b26b4-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b26b4-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b26b4-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="b26b4-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="b26b4-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="b26b4-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="b26b4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b26b4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b26b4-114">Handle per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="b26b4-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b26b4-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b26b4-115">Remarks</span></span>

<span data-ttu-id="b26b4-116">BN \_ DBLCLK è uguale al codice di notifica con [ \_ doppio clic di BN](bn-doubleclicked.md) .</span><span class="sxs-lookup"><span data-stu-id="b26b4-116">BN\_DBLCLK is the same as the [BN\_DOUBLECLICKED](bn-doubleclicked.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b26b4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b26b4-117">Requirements</span></span>



| <span data-ttu-id="b26b4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b26b4-118">Requirement</span></span> | <span data-ttu-id="b26b4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b26b4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b26b4-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b26b4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b26b4-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b26b4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b26b4-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b26b4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b26b4-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b26b4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b26b4-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b26b4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b26b4-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b26b4-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b26b4-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b26b4-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b26b4-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b26b4-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b26b4-128">BN \_ selezionato</span><span class="sxs-lookup"><span data-stu-id="b26b4-128">BN\_CLICKED</span></span>](bn-clicked.md)
</dt> <dt>

[<span data-ttu-id="b26b4-129">MILIARDI di \_ DoubleClick</span><span class="sxs-lookup"><span data-stu-id="b26b4-129">BN\_DOUBLECLICKED</span></span>](bn-doubleclicked.md)
</dt> <dt>

<span data-ttu-id="b26b4-130">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="b26b4-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b26b4-131">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="b26b4-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


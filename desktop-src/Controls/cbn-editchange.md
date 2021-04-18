---
title: Codice di notifica CBN_EDITCHANGE (winuser. h)
description: Inviato dopo che l'utente ha eseguito un'azione che potrebbe aver modificato il testo nella parte del controllo di modifica di una casella combinata.
ms.assetid: 2c5de5cd-24d3-4198-906e-b520369e0f61
keywords:
- Controlli di Windows per il codice di notifica CBN_EDITCHANGE
topic_type:
- apiref
api_name:
- CBN_EDITCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a661d647d0879b93675563777d77bba2dfe8c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302645"
---
# <a name="cbn_editchange-notification-code"></a><span data-ttu-id="04fd8-104">\_Codice di notifica EDITCHANGE CBN</span><span class="sxs-lookup"><span data-stu-id="04fd8-104">CBN\_EDITCHANGE notification code</span></span>

<span data-ttu-id="04fd8-105">Inviato dopo che l'utente ha eseguito un'azione che potrebbe aver modificato il testo nella parte del controllo di modifica di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="04fd8-105">Sent after the user has taken an action that may have altered the text in the edit control portion of a combo box.</span></span> <span data-ttu-id="04fd8-106">A differenza del codice di notifica di [CBN \_ EDITUPDATE](cbn-editupdate.md) , questo codice di notifica viene inviato dopo che il sistema ha aggiornato la schermata.</span><span class="sxs-lookup"><span data-stu-id="04fd8-106">Unlike the [CBN\_EDITUPDATE](cbn-editupdate.md) notification code, this notification code is sent after the system updates the screen.</span></span> <span data-ttu-id="04fd8-107">La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="04fd8-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_EDITCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="04fd8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="04fd8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04fd8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04fd8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04fd8-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="04fd8-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="04fd8-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="04fd8-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="04fd8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04fd8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04fd8-113">Handle per la casella combinata.</span><span class="sxs-lookup"><span data-stu-id="04fd8-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04fd8-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="04fd8-114">Remarks</span></span>

<span data-ttu-id="04fd8-115">Se la casella combinata ha lo stile di [**\_ DropDownList CBS**](combo-box-styles.md) , questo codice di notifica non viene inviato.</span><span class="sxs-lookup"><span data-stu-id="04fd8-115">If the combo box has the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, this notification code is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="04fd8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04fd8-116">Requirements</span></span>



| <span data-ttu-id="04fd8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="04fd8-117">Requirement</span></span> | <span data-ttu-id="04fd8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="04fd8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04fd8-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04fd8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="04fd8-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04fd8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="04fd8-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04fd8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="04fd8-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="04fd8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="04fd8-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04fd8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="04fd8-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04fd8-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04fd8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04fd8-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="04fd8-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="04fd8-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="04fd8-127">\_EDITUPDATE CBN</span><span class="sxs-lookup"><span data-stu-id="04fd8-127">CBN\_EDITUPDATE</span></span>](cbn-editupdate.md)
</dt> <dt>

<span data-ttu-id="04fd8-128">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="04fd8-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="04fd8-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="04fd8-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="04fd8-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="04fd8-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="04fd8-131">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="04fd8-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


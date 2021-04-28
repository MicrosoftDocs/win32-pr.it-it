---
title: BN_DBLCLK di notifica (Winuser.h)
description: "BN_DBLCLK codice di notifica: inviato quando l'utente fa doppio clic su un pulsante."
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- BN_DBLCLK codice di notifica controlli Windows
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
ms.openlocfilehash: fdb403f37b8fee9ea36023a7cd2511bbaaa2af81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096849"
---
# <a name="bn_dblclk-notification-code"></a><span data-ttu-id="5707c-104">Codice di notifica \_ DBLCLK BN</span><span class="sxs-lookup"><span data-stu-id="5707c-104">BN\_DBLCLK notification code</span></span>

<span data-ttu-id="5707c-105">Inviato quando l'utente fa doppio clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="5707c-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="5707c-106">Questo codice di notifica viene inviato automaticamente per i pulsanti [**BS \_ USERBUTTON,**](button-styles.md) [**BS \_ RADIOBUTTON**](button-styles.md)e [**BS \_ OWNERDRAW.**](button-styles.md)</span><span class="sxs-lookup"><span data-stu-id="5707c-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="5707c-107">Gli altri tipi di pulsante inviano \_ BN DBLCLK solo se hanno lo [**stile BS \_ NOTIFY.**](button-styles.md)</span><span class="sxs-lookup"><span data-stu-id="5707c-107">Other button types send BN\_DBLCLK only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="5707c-108">La finestra padre del pulsante riceve questo codice di notifica tramite il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)</span><span class="sxs-lookup"><span data-stu-id="5707c-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="5707c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5707c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5707c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5707c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5707c-111">La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="5707c-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="5707c-112">HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="5707c-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="5707c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5707c-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5707c-114">Handle per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="5707c-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5707c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5707c-115">Remarks</span></span>

<span data-ttu-id="5707c-116">BN \_ DBLCLK corrisponde al codice di notifica [BN \_ DOUBLECLICKED.](bn-doubleclicked.md)</span><span class="sxs-lookup"><span data-stu-id="5707c-116">BN\_DBLCLK is the same as the [BN\_DOUBLECLICKED](bn-doubleclicked.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5707c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5707c-117">Requirements</span></span>



| <span data-ttu-id="5707c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5707c-118">Requirement</span></span> | <span data-ttu-id="5707c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5707c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5707c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5707c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5707c-121">Solo app desktop di Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="5707c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5707c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5707c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5707c-123">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5707c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5707c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5707c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5707c-125"><dt>Winuser.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="5707c-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5707c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5707c-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="5707c-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="5707c-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5707c-128">BN \_ SU CUI È STATO FATTO CLIC</span><span class="sxs-lookup"><span data-stu-id="5707c-128">BN\_CLICKED</span></span>](bn-clicked.md)
</dt> <dt>

[<span data-ttu-id="5707c-129">BN \_ DOUBLECLICKED</span><span class="sxs-lookup"><span data-stu-id="5707c-129">BN\_DOUBLECLICKED</span></span>](bn-doubleclicked.md)
</dt> <dt>

<span data-ttu-id="5707c-130">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="5707c-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5707c-131">**COMANDO \_ WM**</span><span class="sxs-lookup"><span data-stu-id="5707c-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 


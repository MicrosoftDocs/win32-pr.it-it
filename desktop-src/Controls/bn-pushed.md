---
title: Codice di notifica BN_PUSHED (winuser. h)
description: Inviato quando lo stato di push di un pulsante è impostato su push.
ms.assetid: 34000def-189c-4a37-bcef-4ca09a67df00
keywords:
- Controlli di Windows per il codice di notifica BN_PUSHED
topic_type:
- apiref
api_name:
- BN_PUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18a27599c770eb55d889a21956312512ca804cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340503"
---
# <a name="bn_pushed-notification-code"></a><span data-ttu-id="efbe9-104">\_Codice di notifica push di BN</span><span class="sxs-lookup"><span data-stu-id="efbe9-104">BN\_PUSHED notification code</span></span>

<span data-ttu-id="efbe9-105">Inviato quando lo stato di push di un pulsante è impostato su push.</span><span class="sxs-lookup"><span data-stu-id="efbe9-105">Sent when the push state of a button is set to pushed.</span></span>

> [!Note]  
> <span data-ttu-id="efbe9-106">Questo codice di notifica viene fornito solo per la compatibilità con le versioni di Windows a 16 bit precedenti alla versione 3,0.</span><span class="sxs-lookup"><span data-stu-id="efbe9-106">This notification code is provided only for compatibility with 16-bit versions of Windows earlier than version 3.0.</span></span> <span data-ttu-id="efbe9-107">Le applicazioni devono utilizzare lo stile del pulsante [**BS \_ OWNERDRAW**](button-styles.md) e la struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) per questa attività.</span><span class="sxs-lookup"><span data-stu-id="efbe9-107">Applications should use the [**BS\_OWNERDRAW**](button-styles.md) button style and the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure for this task.</span></span>

 

<span data-ttu-id="efbe9-108">La finestra padre del pulsante riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="efbe9-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_PUSHED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="efbe9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="efbe9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efbe9-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="efbe9-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="efbe9-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="efbe9-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="efbe9-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="efbe9-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="efbe9-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="efbe9-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="efbe9-114">Handle per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="efbe9-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="efbe9-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="efbe9-115">Remarks</span></span>

<span data-ttu-id="efbe9-116">Il \_ push di BN è uguale al codice di notifica [ \_ HILITE di BN](bn-hilite.md) .</span><span class="sxs-lookup"><span data-stu-id="efbe9-116">BN\_PUSHED is the same as the [BN\_HILITE](bn-hilite.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="efbe9-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efbe9-117">Requirements</span></span>



| <span data-ttu-id="efbe9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="efbe9-118">Requirement</span></span> | <span data-ttu-id="efbe9-119">Valore</span><span class="sxs-lookup"><span data-stu-id="efbe9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efbe9-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efbe9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="efbe9-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="efbe9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="efbe9-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efbe9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="efbe9-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="efbe9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="efbe9-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="efbe9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="efbe9-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="efbe9-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efbe9-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efbe9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efbe9-127">**BN non \_ push**</span><span class="sxs-lookup"><span data-stu-id="efbe9-127">**BN\_UNPUSHED**</span></span>](bn-unpushed.md)
</dt> </dl>

 


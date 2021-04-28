---
title: BN_DOUBLECLICKED di notifica (Winuser.h)
description: "BN_DOUBLECLICKED di notifica: inviato quando l'utente fa doppio clic su un pulsante."
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- BN_DOUBLECLICKED controlli Windows del codice di notifica
topic_type:
- apiref
api_name:
- BN_DOUBLECLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64a11a4dec91a7a2f1d200c4c86c6989d846604a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104189"
---
# <a name="bn_doubleclicked-notification-code"></a><span data-ttu-id="fbd5a-104">Codice di notifica BN \_ DOUBLECLICKED</span><span class="sxs-lookup"><span data-stu-id="fbd5a-104">BN\_DOUBLECLICKED notification code</span></span>

<span data-ttu-id="fbd5a-105">Inviato quando l'utente fa doppio clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="fbd5a-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="fbd5a-106">Questo codice di notifica viene inviato automaticamente per i pulsanti [**\_ BS USERBUTTON**](button-styles.md), [**BS \_ RADIOBUTTON**](button-styles.md)e [**BS \_ OWNERDRAW.**](button-styles.md)</span><span class="sxs-lookup"><span data-stu-id="fbd5a-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="fbd5a-107">Gli altri tipi di pulsante inviano BN \_ DOUBLECLICKED solo se hanno lo [**stile BS \_ NOTIFY.**](button-styles.md)</span><span class="sxs-lookup"><span data-stu-id="fbd5a-107">Other button types send BN\_DOUBLECLICKED only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="fbd5a-108">La finestra padre del pulsante riceve questo codice di notifica tramite il [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)</span><span class="sxs-lookup"><span data-stu-id="fbd5a-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DOUBLECLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="fbd5a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fbd5a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbd5a-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fbd5a-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbd5a-111">La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="fbd5a-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="fbd5a-112">HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="fbd5a-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="fbd5a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fbd5a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbd5a-114">Handle per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="fbd5a-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fbd5a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fbd5a-115">Remarks</span></span>

<span data-ttu-id="fbd5a-116">BN DOUBLECLICKED corrisponde al codice di notifica \_ [ \_ BN DBLCLK.](bn-dblclk.md)</span><span class="sxs-lookup"><span data-stu-id="fbd5a-116">BN\_DOUBLECLICKED is the same as the [BN\_DBLCLK](bn-dblclk.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbd5a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbd5a-117">Requirements</span></span>



| <span data-ttu-id="fbd5a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbd5a-118">Requirement</span></span> | <span data-ttu-id="fbd5a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fbd5a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbd5a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fbd5a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fbd5a-121">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fbd5a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fbd5a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fbd5a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fbd5a-123">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fbd5a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fbd5a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fbd5a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbd5a-125"><dt>Winuser.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="fbd5a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 


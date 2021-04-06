---
title: Codice di notifica BN_DOUBLECLICKED (winuser. h)
description: Inviato quando l'utente fa doppio clic su un pulsante.
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- Controlli di Windows per il codice di notifica BN_DOUBLECLICKED
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
ms.openlocfilehash: 018df4387b026d68e3f4e9a6c259fb19efd4a0f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873529"
---
# <a name="bn_doubleclicked-notification-code"></a><span data-ttu-id="9c1f2-104">\_Codice di notifica con DoubleClick in BN</span><span class="sxs-lookup"><span data-stu-id="9c1f2-104">BN\_DOUBLECLICKED notification code</span></span>

<span data-ttu-id="9c1f2-105">Inviato quando l'utente fa doppio clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="9c1f2-105">Sent when the user double-clicks a button.</span></span> <span data-ttu-id="9c1f2-106">Questo codice di notifica viene inviato automaticamente per i pulsanti [**BS \_ UserButton**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)e [**BS \_ OWNERDRAW**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="9c1f2-106">This notification code is sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="9c1f2-107">Altri tipi di pulsante inviano miliardi \_ di DoubleClick solo se hanno lo stile di [**\_ notifica BS**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="9c1f2-107">Other button types send BN\_DOUBLECLICKED only if they have the [**BS\_NOTIFY**](button-styles.md) style.</span></span>

<span data-ttu-id="9c1f2-108">La finestra padre del pulsante riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="9c1f2-108">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_DOUBLECLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="9c1f2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c1f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c1f2-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c1f2-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c1f2-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="9c1f2-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="9c1f2-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="9c1f2-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="9c1f2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c1f2-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c1f2-114">Handle per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="9c1f2-114">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c1f2-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c1f2-115">Remarks</span></span>

<span data-ttu-id="9c1f2-116">BN \_ doubleclickd equivale al codice di notifica [ \_ DBLCLK di BN](bn-dblclk.md) .</span><span class="sxs-lookup"><span data-stu-id="9c1f2-116">BN\_DOUBLECLICKED is the same as the [BN\_DBLCLK](bn-dblclk.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c1f2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c1f2-117">Requirements</span></span>



| <span data-ttu-id="9c1f2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c1f2-118">Requirement</span></span> | <span data-ttu-id="9c1f2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9c1f2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c1f2-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c1f2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9c1f2-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c1f2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9c1f2-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c1f2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9c1f2-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9c1f2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9c1f2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c1f2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c1f2-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c1f2-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 


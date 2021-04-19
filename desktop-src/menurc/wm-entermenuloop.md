---
title: Messaggio WM_ENTERMENULOOP (winuser. h)
description: Notifica alla routine della finestra principale di un'applicazione che è stato immesso un ciclo modale di menu.
ms.assetid: 0a018b6f-fe4b-4e90-bbb6-9b5719253dc1
keywords:
- Menu del messaggio WM_ENTERMENULOOP e altre risorse
topic_type:
- apiref
api_name:
- WM_ENTERMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a7b325719c428dc7310503320b53f3a5f96182e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301192"
---
# <a name="wm_entermenuloop-message"></a><span data-ttu-id="337d7-104">\_Messaggio ENTERMENULOOP WM</span><span class="sxs-lookup"><span data-stu-id="337d7-104">WM\_ENTERMENULOOP message</span></span>

<span data-ttu-id="337d7-105">Notifica alla routine della finestra principale di un'applicazione che è stato immesso un ciclo modale di menu.</span><span class="sxs-lookup"><span data-stu-id="337d7-105">Notifies an application's main window procedure that a menu modal loop has been entered.</span></span>


```C++
#define WM_ENTERMENULOOP                0x0211
```



## <a name="parameters"></a><span data-ttu-id="337d7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="337d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="337d7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="337d7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="337d7-108">Specifica se il menu finestra è stato immesso utilizzando la funzione [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) .</span><span class="sxs-lookup"><span data-stu-id="337d7-108">Specifies whether the window menu was entered using the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function.</span></span> <span data-ttu-id="337d7-109">Il valore di questo parametro è **true** se il menu finestra è stato immesso utilizzando **TrackPopupMenu** e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="337d7-109">This parameter has a value of **TRUE** if the window menu was entered using **TrackPopupMenu**, and **FALSE** if it was not.</span></span>

</dd> <dt>

<span data-ttu-id="337d7-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="337d7-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="337d7-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="337d7-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="337d7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="337d7-112">Return value</span></span>

<span data-ttu-id="337d7-113">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="337d7-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="337d7-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="337d7-114">Remarks</span></span>

<span data-ttu-id="337d7-115">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="337d7-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="337d7-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="337d7-116">Requirements</span></span>



| <span data-ttu-id="337d7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="337d7-117">Requirement</span></span> | <span data-ttu-id="337d7-118">Valore</span><span class="sxs-lookup"><span data-stu-id="337d7-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="337d7-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="337d7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="337d7-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="337d7-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="337d7-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="337d7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="337d7-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="337d7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="337d7-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="337d7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="337d7-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="337d7-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="337d7-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="337d7-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="337d7-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="337d7-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="337d7-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="337d7-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="337d7-128">**\_EXITMENULOOP WM**</span><span class="sxs-lookup"><span data-stu-id="337d7-128">**WM\_EXITMENULOOP**</span></span>](wm-exitmenuloop.md)
</dt> <dt>

<span data-ttu-id="337d7-129">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="337d7-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="337d7-130">Menu</span><span class="sxs-lookup"><span data-stu-id="337d7-130">Menus</span></span>](menus.md)
</dt> </dl>

 


---
title: Messaggio WM_EXITMENULOOP (winuser. h)
description: Notifica alla routine della finestra principale di un'applicazione che un ciclo modale del menu è stato terminato.
ms.assetid: b2a9d537-af7c-4c8a-932a-95e45eb8deb5
keywords:
- Menu del messaggio WM_EXITMENULOOP e altre risorse
topic_type:
- apiref
api_name:
- WM_EXITMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8440e1a255968eb3e1607b5d54375900f7b5de16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741706"
---
# <a name="wm_exitmenuloop-message"></a><span data-ttu-id="86639-104">\_Messaggio EXITMENULOOP WM</span><span class="sxs-lookup"><span data-stu-id="86639-104">WM\_EXITMENULOOP message</span></span>

<span data-ttu-id="86639-105">Notifica alla routine della finestra principale di un'applicazione che un ciclo modale del menu è stato terminato.</span><span class="sxs-lookup"><span data-stu-id="86639-105">Notifies an application's main window procedure that a menu modal loop has been exited.</span></span>


```C++
#define WM_EXITMENULOOP                 0x0212
```



## <a name="parameters"></a><span data-ttu-id="86639-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="86639-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86639-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86639-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86639-108">Specifica se il menu è un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="86639-108">Specifies whether the menu is a shortcut menu.</span></span> <span data-ttu-id="86639-109">Il valore di questo parametro è **true** se si tratta di un menu di scelta rapida; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="86639-109">This parameter has a value of **TRUE** if it is a shortcut menu, **FALSE** if it is not.</span></span>

</dd> <dt>

<span data-ttu-id="86639-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86639-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86639-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="86639-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86639-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86639-112">Return value</span></span>

<span data-ttu-id="86639-113">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="86639-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="86639-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="86639-114">Remarks</span></span>

<span data-ttu-id="86639-115">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="86639-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="86639-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86639-116">Requirements</span></span>



| <span data-ttu-id="86639-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="86639-117">Requirement</span></span> | <span data-ttu-id="86639-118">Valore</span><span class="sxs-lookup"><span data-stu-id="86639-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86639-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86639-119">Minimum supported client</span></span><br/> | <span data-ttu-id="86639-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="86639-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="86639-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86639-121">Minimum supported server</span></span><br/> | <span data-ttu-id="86639-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="86639-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="86639-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86639-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="86639-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86639-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86639-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86639-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="86639-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="86639-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="86639-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="86639-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="86639-128">**\_ENTERMENULOOP WM**</span><span class="sxs-lookup"><span data-stu-id="86639-128">**WM\_ENTERMENULOOP**</span></span>](wm-entermenuloop.md)
</dt> <dt>

<span data-ttu-id="86639-129">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="86639-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="86639-130">Menu</span><span class="sxs-lookup"><span data-stu-id="86639-130">Menus</span></span>](menus.md)
</dt> </dl>

 


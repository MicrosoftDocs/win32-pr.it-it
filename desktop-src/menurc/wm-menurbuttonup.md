---
title: Messaggio WM_MENURBUTTONUP (winuser. h)
description: Inviato quando l'utente rilascia il pulsante destro del mouse mentre il cursore si trova in una voce di menu.
ms.assetid: e061cba0-6aea-4df4-a39a-7e55f0db45c0
keywords:
- Menu del messaggio WM_MENURBUTTONUP e altre risorse
topic_type:
- apiref
api_name:
- WM_MENURBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7206fc79f6f990611c81ad0e844ae26af3764c6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341352"
---
# <a name="wm_menurbuttonup-message"></a><span data-ttu-id="c12f7-104">\_Messaggio MENURBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="c12f7-104">WM\_MENURBUTTONUP message</span></span>

<span data-ttu-id="c12f7-105">Inviato quando l'utente rilascia il pulsante destro del mouse mentre il cursore si trova in una voce di menu.</span><span class="sxs-lookup"><span data-stu-id="c12f7-105">Sent when the user releases the right mouse button while the cursor is on a menu item.</span></span>


```C++
#define WM_MENURBUTTONUP                0x0122
```



## <a name="parameters"></a><span data-ttu-id="c12f7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c12f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c12f7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c12f7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c12f7-108">Indice in base zero della voce di menu in cui è stato rilasciato il pulsante destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="c12f7-108">The zero-based index of the menu item on which the right mouse button was released.</span></span>

</dd> <dt>

<span data-ttu-id="c12f7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c12f7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c12f7-110">Handle per il menu contenente l'elemento.</span><span class="sxs-lookup"><span data-stu-id="c12f7-110">A handle to the menu containing the item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c12f7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c12f7-111">Remarks</span></span>

<span data-ttu-id="c12f7-112">Il messaggio **WM \_ MENURBUTTONUP** consente alle applicazioni di fornire un menu sensibile al contesto denominato anche menu di scelta rapida per la voce di menu specificata in questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="c12f7-112">The **WM\_MENURBUTTONUP** message allows applications to provide a context-sensitive menu also known as a shortcut menu for the menu item specified in this message.</span></span> <span data-ttu-id="c12f7-113">Per visualizzare un menu sensibile al contesto per una voce di menu, chiamare la funzione [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) con la **\_ recurse del TPM**.</span><span class="sxs-lookup"><span data-stu-id="c12f7-113">To display a context-sensitive menu for a menu item, call the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function with **TPM\_RECURSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c12f7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c12f7-114">Requirements</span></span>



| <span data-ttu-id="c12f7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c12f7-115">Requirement</span></span> | <span data-ttu-id="c12f7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c12f7-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c12f7-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c12f7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c12f7-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c12f7-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c12f7-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c12f7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c12f7-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c12f7-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c12f7-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c12f7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c12f7-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c12f7-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c12f7-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c12f7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c12f7-124">Panoramica sui menu</span><span class="sxs-lookup"><span data-stu-id="c12f7-124">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 






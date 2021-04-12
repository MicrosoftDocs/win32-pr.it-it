---
title: Messaggio WM_MENUCOMMAND (winuser. h)
description: Inviato quando l'utente effettua una selezione da un menu.
ms.assetid: 1ed702ef-8d32-4d4c-a68a-ffd199112ced
keywords:
- Menu del messaggio WM_MENUCOMMAND e altre risorse
topic_type:
- apiref
api_name:
- WM_MENUCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13288c49327b536db6ebef8a41526facd3fb2d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400934"
---
# <a name="wm_menucommand-message"></a><span data-ttu-id="38ab7-104">Messaggio dell'MENUCOMMAND di WM \_</span><span class="sxs-lookup"><span data-stu-id="38ab7-104">WM\_MENUCOMMAND message</span></span>

<span data-ttu-id="38ab7-105">Inviato quando l'utente effettua una selezione da un menu.</span><span class="sxs-lookup"><span data-stu-id="38ab7-105">Sent when the user makes a selection from a menu.</span></span>


```C++
#define WM_MENUCOMMAND                  0x0126
```



## <a name="parameters"></a><span data-ttu-id="38ab7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="38ab7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38ab7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38ab7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38ab7-108">Indice in base zero dell'elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="38ab7-108">The zero-based index of the item selected.</span></span>

</dd> <dt>

<span data-ttu-id="38ab7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38ab7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38ab7-110">Handle per il menu per l'elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="38ab7-110">A handle to the menu for the item selected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38ab7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="38ab7-111">Remarks</span></span>

<span data-ttu-id="38ab7-112">Il messaggio **WM \_ MENUCOMMAND** fornisce un handle per il menu in modo da poter accedere ai dati del menu nella struttura [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) e fornisce anche l'indice dell'elemento selezionato, che corrisponde in genere alle applicazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="38ab7-112">The **WM\_MENUCOMMAND** message gives you a handle to the menu so you can access the menu data in the [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) structure and also gives you the index of the selected item, which is typically what applications need.</span></span> <span data-ttu-id="38ab7-113">Al contrario, il messaggio del [**\_ comando WM**](wm-command.md) fornisce l'identificatore della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="38ab7-113">In contrast, the [**WM\_COMMAND**](wm-command.md) message gives you the menu item identifier.</span></span>

<span data-ttu-id="38ab7-114">Il **messaggio WM \_ MENUCOMMAND** viene inviato solo per i menu definiti con il flag **\_ NOTIFYBYPOS di MNS** impostato nel membro **dwStyle** della struttura [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) .</span><span class="sxs-lookup"><span data-stu-id="38ab7-114">The **WM\_MENUCOMMAND** message is sent only for menus that are defined with the **MNS\_NOTIFYBYPOS** flag set in the **dwStyle** member of the [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="38ab7-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38ab7-115">Requirements</span></span>



| <span data-ttu-id="38ab7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="38ab7-116">Requirement</span></span> | <span data-ttu-id="38ab7-117">Valore</span><span class="sxs-lookup"><span data-stu-id="38ab7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38ab7-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38ab7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="38ab7-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="38ab7-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="38ab7-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38ab7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="38ab7-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="38ab7-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="38ab7-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38ab7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="38ab7-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38ab7-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38ab7-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38ab7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38ab7-125">Panoramica sui menu</span><span class="sxs-lookup"><span data-stu-id="38ab7-125">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 






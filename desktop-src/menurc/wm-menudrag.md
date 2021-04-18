---
title: Messaggio WM_MENUDRAG (winuser. h)
description: Inviato al proprietario di un menu di trascinamento della selezione quando l'utente trascina una voce di menu.
ms.assetid: 99e8f490-ef1e-4964-a3a1-47030a88f10c
keywords:
- Menu del messaggio WM_MENUDRAG e altre risorse
topic_type:
- apiref
api_name:
- WM_MENUDRAG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67e83c41576a716d292187df4cb08fa803271c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302728"
---
# <a name="wm_menudrag-message"></a><span data-ttu-id="d1695-104">\_Messaggio MENUDRAG WM</span><span class="sxs-lookup"><span data-stu-id="d1695-104">WM\_MENUDRAG message</span></span>

<span data-ttu-id="d1695-105">Inviato al proprietario di un menu di trascinamento della selezione quando l'utente trascina una voce di menu.</span><span class="sxs-lookup"><span data-stu-id="d1695-105">Sent to the owner of a drag-and-drop menu when the user drags a menu item.</span></span>


```C++
#define WM_MENUDRAG                     0x0123
```



## <a name="parameters"></a><span data-ttu-id="d1695-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1695-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1695-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1695-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1695-108">Posizione dell'elemento in cui è iniziata l'operazione di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="d1695-108">The position of the item where the drag operation began.</span></span>

</dd> <dt>

<span data-ttu-id="d1695-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1695-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1695-110">Handle per il menu contenente l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d1695-110">A handle to the menu containing the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1695-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1695-111">Return value</span></span>

<span data-ttu-id="d1695-112">L'applicazione deve restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d1695-112">The application should return one of the following values.</span></span>



| <span data-ttu-id="d1695-113">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1695-113">Return code/value</span></span>                                                                                                                                   | <span data-ttu-id="d1695-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1695-114">Description</span></span>                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1695-115"><dt>**MND \_ CONTINUA**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d1695-115"><dt>**MND\_CONTINUE**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="d1695-116">Il menu deve rimanere attivo.</span><span class="sxs-lookup"><span data-stu-id="d1695-116">Menu should remain active.</span></span> <span data-ttu-id="d1695-117">Se il mouse viene rilasciato, deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="d1695-117">If the mouse is released, it should be ignored.</span></span><br/> |
| <dl> <span data-ttu-id="d1695-118"><dt>**MND \_ ENDMENU**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d1695-118"><dt>**MND\_ENDMENU**</dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="d1695-119">Il menu deve terminare.</span><span class="sxs-lookup"><span data-stu-id="d1695-119">Menu should be ended.</span></span><br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="d1695-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1695-120">Remarks</span></span>

<span data-ttu-id="d1695-121">L'applicazione può chiamare la funzione [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) in risposta a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="d1695-121">The application can call the [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) function in response to this message.</span></span>

<span data-ttu-id="d1695-122">Per creare un menu di trascinamento della selezione, chiamare [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) con **MNS \_ DragDrop**.</span><span class="sxs-lookup"><span data-stu-id="d1695-122">To create a drag-and-drop menu, call [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) with **MNS\_DRAGDROP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1695-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1695-123">Requirements</span></span>



| <span data-ttu-id="d1695-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1695-124">Requirement</span></span> | <span data-ttu-id="d1695-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d1695-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1695-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1695-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d1695-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d1695-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d1695-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1695-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d1695-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d1695-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d1695-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1695-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1695-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1695-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1695-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1695-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="d1695-133">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="d1695-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d1695-134">**SetMenuInfo**</span><span class="sxs-lookup"><span data-stu-id="d1695-134">**SetMenuInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)
</dt> <dt>

<span data-ttu-id="d1695-135">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="d1695-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d1695-136">Menu</span><span class="sxs-lookup"><span data-stu-id="d1695-136">Menus</span></span>](menus.md)
</dt> </dl>

 


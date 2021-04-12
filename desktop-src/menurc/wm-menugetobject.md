---
title: Messaggio WM_MENUGETOBJECT (winuser. h)
description: Inviato al proprietario di un menu a trascinamento quando il cursore del mouse entra in una voce di menu o viene spostato dal centro dell'elemento alla parte superiore o inferiore dell'elemento.
ms.assetid: 08348e43-3d21-4543-b624-5504575efced
keywords:
- Menu del messaggio WM_MENUGETOBJECT e altre risorse
topic_type:
- apiref
api_name:
- WM_MENUGETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e124c7f2757a0d6d1d2ac0904052b6d3c255ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519205"
---
# <a name="wm_menugetobject-message"></a><span data-ttu-id="c30b3-104">\_Messaggio MENUGETOBJECT WM</span><span class="sxs-lookup"><span data-stu-id="c30b3-104">WM\_MENUGETOBJECT message</span></span>

<span data-ttu-id="c30b3-105">Inviato al proprietario di un menu a trascinamento quando il cursore del mouse entra in una voce di menu o viene spostato dal centro dell'elemento alla parte superiore o inferiore dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="c30b3-105">Sent to the owner of a drag-and-drop menu when the mouse cursor enters a menu item or moves from the center of the item to the top or bottom of the item.</span></span>


```C++
#define WM_MENUGETOBJECT                0x0124
```



## <a name="parameters"></a><span data-ttu-id="c30b3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c30b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c30b3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c30b3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c30b3-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="c30b3-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c30b3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c30b3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c30b3-110">Puntatore a una struttura [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) .</span><span class="sxs-lookup"><span data-stu-id="c30b3-110">A pointer to a [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c30b3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c30b3-111">Return value</span></span>

<span data-ttu-id="c30b3-112">L'applicazione deve restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c30b3-112">The application should return one of the following values.</span></span>



| <span data-ttu-id="c30b3-113">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="c30b3-113">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="c30b3-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c30b3-114">Description</span></span>                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c30b3-115"><dt>**MNGO \_ NOERROR**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="c30b3-115"><dt>**MNGO\_NOERROR**</dt> <dt>0x00000001</dt></span></span> </dl>     | <span data-ttu-id="c30b3-116">Puntatore di interfaccia restituito nel membro **pvObj** di [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)</span><span class="sxs-lookup"><span data-stu-id="c30b3-116">An interface pointer was returned in the **pvObj** member of [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)</span></span><br/> |
| <dl> <span data-ttu-id="c30b3-117"><dt>**MNGO \_ Nointerface**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="c30b3-117"><dt>**MNGO\_NOINTERFACE**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="c30b3-118">L'interfaccia non è supportata.</span><span class="sxs-lookup"><span data-stu-id="c30b3-118">The interface is not supported.</span></span><br/>                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="c30b3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c30b3-119">Requirements</span></span>



| <span data-ttu-id="c30b3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c30b3-120">Requirement</span></span> | <span data-ttu-id="c30b3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c30b3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c30b3-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c30b3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c30b3-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c30b3-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c30b3-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c30b3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c30b3-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c30b3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c30b3-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c30b3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c30b3-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c30b3-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c30b3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c30b3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c30b3-129">Panoramica sui menu</span><span class="sxs-lookup"><span data-stu-id="c30b3-129">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 






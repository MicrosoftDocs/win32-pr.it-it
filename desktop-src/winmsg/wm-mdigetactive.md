---
description: Un'applicazione invia il \_ messaggio WM MDIGETACTIVE a una finestra del client di interfaccia a documenti multipli (MDI) per recuperare l'handle per la finestra figlio MDI attiva.
ms.assetid: 3ee445be-dd55-4825-8508-fa18a346ffcd
title: Messaggio WM_MDIGETACTIVE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49f4ec321f526cd4c9766555e2361ef2cfbd040
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314860"
---
# <a name="wm_mdigetactive-message"></a><span data-ttu-id="baf7f-103">\_Messaggio MDIGETACTIVE WM</span><span class="sxs-lookup"><span data-stu-id="baf7f-103">WM\_MDIGETACTIVE message</span></span>

<span data-ttu-id="baf7f-104">Un'applicazione invia il messaggio **WM \_ MDIGETACTIVE** a una finestra del client di interfaccia a documenti multipli (MDI) per recuperare l'handle per la finestra figlio MDI attiva.</span><span class="sxs-lookup"><span data-stu-id="baf7f-104">An application sends the **WM\_MDIGETACTIVE** message to a multiple-document interface (MDI) client window to retrieve the handle to the active MDI child window.</span></span>


```C++
#define WM_MDIGETACTIVE                  0x0229
```



## <a name="parameters"></a><span data-ttu-id="baf7f-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="baf7f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baf7f-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="baf7f-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="baf7f-107">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="baf7f-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="baf7f-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="baf7f-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="baf7f-109">Stato ingrandito.</span><span class="sxs-lookup"><span data-stu-id="baf7f-109">The maximized state.</span></span> <span data-ttu-id="baf7f-110">Se questo parametro non è **null**, è un puntatore a un valore che indica lo stato ingrandito della finestra figlio MDI.</span><span class="sxs-lookup"><span data-stu-id="baf7f-110">If this parameter is not **NULL**, it is a pointer to a value that indicates the maximized state of the MDI child window.</span></span> <span data-ttu-id="baf7f-111">Se il valore è **true**, la finestra è ingrandita; il valore **false** indica che non lo è.</span><span class="sxs-lookup"><span data-stu-id="baf7f-111">If the value is **TRUE**, the window is maximized; a value of **FALSE** indicates that it is not.</span></span> <span data-ttu-id="baf7f-112">Se questo parametro è **null**, il parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="baf7f-112">If this parameter is **NULL**, the parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baf7f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="baf7f-113">Return value</span></span>

<span data-ttu-id="baf7f-114">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="baf7f-114">Type: **HWND**</span></span>

<span data-ttu-id="baf7f-115">Il valore restituito è l'handle per la finestra figlio MDI attiva.</span><span class="sxs-lookup"><span data-stu-id="baf7f-115">The return value is the handle to the active MDI child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="baf7f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="baf7f-116">Requirements</span></span>



| <span data-ttu-id="baf7f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="baf7f-117">Requirement</span></span> | <span data-ttu-id="baf7f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="baf7f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baf7f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="baf7f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="baf7f-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="baf7f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="baf7f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="baf7f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="baf7f-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="baf7f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="baf7f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="baf7f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="baf7f-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="baf7f-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baf7f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="baf7f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baf7f-126">Panoramica dell'interfaccia a più documenti</span><span class="sxs-lookup"><span data-stu-id="baf7f-126">Multiple Document Interface Overview</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 





---
description: Recupera l'handle per il AppBar di Nascondi automaticamente associato a un bordo dello schermo. Se il sistema dispone di più monitoraggi, viene utilizzato il monitoraggio che contiene la barra delle applicazioni principale.
title: Messaggio ABM_GETAUTOHIDEBAR (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 545dd1d9-8cbb-4ff3-b871-4908ecac56db
api_name:
- ABM_GETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 979825a9dbc28a89e3579419542877faacbace45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128479"
---
# <a name="abm_getautohidebar-message"></a><span data-ttu-id="cc864-104">\_Messaggio GETAUTOHIDEBAR ABM</span><span class="sxs-lookup"><span data-stu-id="cc864-104">ABM\_GETAUTOHIDEBAR message</span></span>

<span data-ttu-id="cc864-105">Recupera l'handle per il AppBar di Nascondi automaticamente associato a un bordo dello schermo.</span><span class="sxs-lookup"><span data-stu-id="cc864-105">Retrieves the handle to the autohide appbar associated with an edge of the screen.</span></span> <span data-ttu-id="cc864-106">Se il sistema dispone di più monitoraggi, viene utilizzato il monitoraggio che contiene la barra delle applicazioni principale.</span><span class="sxs-lookup"><span data-stu-id="cc864-106">If the system has multiple monitors, the monitor that contains the primary taskbar is used.</span></span>

> [!Note]  
> <span data-ttu-id="cc864-107">Per eseguire una query per un AppBar di Nascondi automaticamente su un monitor specifico, usare l' [**\_ GETAUTOHIDEBAREX ABM**](abm-getautohidebarex.md).</span><span class="sxs-lookup"><span data-stu-id="cc864-107">To query for an autohide appbar on a specific monitor, use [**ABM\_GETAUTOHIDEBAREX**](abm-getautohidebarex.md).</span></span>

 


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a><span data-ttu-id="cc864-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc864-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc864-109">*pabd*</span><span class="sxs-lookup"><span data-stu-id="cc864-109">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="cc864-110">Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) che specifica il bordo dello schermo.</span><span class="sxs-lookup"><span data-stu-id="cc864-110">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that specifies the screen edge.</span></span> <span data-ttu-id="cc864-111">Quando si invia questo messaggio, è necessario specificare i membri **cbSize** e **uEdge** . tutti gli altri membri vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="cc864-111">You must specify the **cbSize** and **uEdge** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc864-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc864-112">Return value</span></span>

<span data-ttu-id="cc864-113">Restituisce l'handle per il AppBar di Nascondi automaticamente.</span><span class="sxs-lookup"><span data-stu-id="cc864-113">Returns the handle to the autohide appbar.</span></span> <span data-ttu-id="cc864-114">Il valore restituito è **null** se si verifica un errore o se non è associato alcun AppBar di Nascondi automaticamente al bordo specificato.</span><span class="sxs-lookup"><span data-stu-id="cc864-114">The return value is **NULL** if an error occurs or if no autohide appbar is associated with the given edge.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc864-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc864-115">Requirements</span></span>



| <span data-ttu-id="cc864-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc864-116">Requirement</span></span> | <span data-ttu-id="cc864-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cc864-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc864-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc864-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cc864-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cc864-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cc864-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc864-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cc864-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cc864-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc864-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc864-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc864-123"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc864-123"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc864-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc864-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc864-125">**\_SETAUTOHIDEBAR ABM**</span><span class="sxs-lookup"><span data-stu-id="cc864-125">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> <dt>

[<span data-ttu-id="cc864-126">**\_GETAUTOHIDEBAREX ABM**</span><span class="sxs-lookup"><span data-stu-id="cc864-126">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="cc864-127">**\_SETAUTOHIDEBAREX ABM**</span><span class="sxs-lookup"><span data-stu-id="cc864-127">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 





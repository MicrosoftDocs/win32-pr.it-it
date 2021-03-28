---
description: Registra o Annulla la registrazione di un AppBar di Nascondi automaticamente per un determinato bordo dello schermo. Se il sistema dispone di più monitoraggi, viene utilizzato il monitoraggio che contiene la barra delle applicazioni principale.
title: Messaggio ABM_SETAUTOHIDEBAR (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0cbd6c9c-e83f-41f8-91ed-81afaa24f524
api_name:
- ABM_SETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 53ca89008dda1233d12a7f0a9588803776ba1181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977450"
---
# <a name="abm_setautohidebar-message"></a><span data-ttu-id="a351c-104">\_Messaggio SETAUTOHIDEBAR ABM</span><span class="sxs-lookup"><span data-stu-id="a351c-104">ABM\_SETAUTOHIDEBAR message</span></span>

<span data-ttu-id="a351c-105">Registra o Annulla la registrazione di un AppBar di Nascondi automaticamente per un determinato bordo dello schermo.</span><span class="sxs-lookup"><span data-stu-id="a351c-105">Registers or unregisters an autohide appbar for a given edge of the screen.</span></span> <span data-ttu-id="a351c-106">Se il sistema dispone di più monitoraggi, viene utilizzato il monitoraggio che contiene la barra delle applicazioni principale.</span><span class="sxs-lookup"><span data-stu-id="a351c-106">If the system has multiple monitors, the monitor that contains the primary taskbar is used.</span></span>

> [!Note]  
> <span data-ttu-id="a351c-107">Per registrare o annullare la registrazione di un AppBar di Nascondi automaticamente in un monitor specifico, usare l' [**\_ SETAUTOHIDEBAREX ABM**](abm-setautohidebarex.md).</span><span class="sxs-lookup"><span data-stu-id="a351c-107">To register or unregister an autohide appbar on a specific monitor, use [**ABM\_SETAUTOHIDEBAREX**](abm-setautohidebarex.md).</span></span>

 


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="a351c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a351c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a351c-109">*pabd*</span><span class="sxs-lookup"><span data-stu-id="a351c-109">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="a351c-110">Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="a351c-110">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="a351c-111">Impostare il membro **lParam** su **true** per registrare AppBar o **false** per annullarne la registrazione.</span><span class="sxs-lookup"><span data-stu-id="a351c-111">Set the **lParam** member to **TRUE** to register the appbar or **FALSE** to unregister it.</span></span> <span data-ttu-id="a351c-112">Quando si invia questo messaggio, è necessario specificare i membri **cbSize**, **HWND**, **uEdge** e **lParam** . tutti gli altri membri vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="a351c-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **lParam** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a351c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a351c-113">Return value</span></span>

<span data-ttu-id="a351c-114">Restituisce **true** se ha esito positivo o **false** se si verifica un errore o se un AppBar di Nascondi automaticamente è già registrato per il bordo specificato.</span><span class="sxs-lookup"><span data-stu-id="a351c-114">Returns **TRUE** if successful, or **FALSE** if an error occurs or if an autohide appbar is already registered for the given edge.</span></span>

## <a name="remarks"></a><span data-ttu-id="a351c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a351c-115">Remarks</span></span>

<span data-ttu-id="a351c-116">Il sistema consente un solo AppBar di Nascondi automaticamente per ogni bordo dello schermo.</span><span class="sxs-lookup"><span data-stu-id="a351c-116">The system allows only one autohide appbar for each edge of the screen.</span></span> <span data-ttu-id="a351c-117">Questa operazione viene determinata quando viene impostato il membro **uEdge** della struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="a351c-117">This is determined when the member **uEdge** of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="a351c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a351c-118">Requirements</span></span>



| <span data-ttu-id="a351c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a351c-119">Requirement</span></span> | <span data-ttu-id="a351c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a351c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a351c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a351c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a351c-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a351c-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a351c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a351c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a351c-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a351c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a351c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a351c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a351c-126"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a351c-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a351c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a351c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a351c-128">**\_SETAUTOHIDEBAR ABM**</span><span class="sxs-lookup"><span data-stu-id="a351c-128">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="a351c-129">**\_GETAUTOHIDEBAREX ABM**</span><span class="sxs-lookup"><span data-stu-id="a351c-129">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="a351c-130">**\_SETAUTOHIDEBAREX ABM**</span><span class="sxs-lookup"><span data-stu-id="a351c-130">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 





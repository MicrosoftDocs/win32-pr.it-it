---
description: Registra o Annulla la registrazione di un AppBar di Nascondi automaticamente per un determinato bordo dello schermo. Questo messaggio estende il \_ SETAUTOHIDEBAR ABM consentendo di specificare un particolare monitoraggio, da usare in più situazioni di monitoraggio.
title: Messaggio ABM_SETAUTOHIDEBAREX (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C437727C-3FF6-4598-9D81-A39FCC2EF1C4
api_name:
- ABM_SETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba4e1474d3b57465fa68446fd7ab787c9a62570b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996465"
---
# <a name="abm_setautohidebarex-message"></a><span data-ttu-id="1ccb2-104">\_Messaggio SETAUTOHIDEBAREX ABM</span><span class="sxs-lookup"><span data-stu-id="1ccb2-104">ABM\_SETAUTOHIDEBAREX message</span></span>

<span data-ttu-id="1ccb2-105">Registra o Annulla la registrazione di un AppBar di Nascondi automaticamente per un determinato bordo dello schermo.</span><span class="sxs-lookup"><span data-stu-id="1ccb2-105">Registers or unregisters an autohide appbar for a given edge of the screen.</span></span> <span data-ttu-id="1ccb2-106">Questo messaggio estende [**il \_ SETAUTOHIDEBAR ABM**](abm-setautohidebar.md) consentendo di specificare un particolare monitoraggio, da usare in più situazioni di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="1ccb2-106">This message extends [**ABM\_SETAUTOHIDEBAR**](abm-setautohidebar.md) by enabling you to specify a particular monitor, for use in multiple monitor situations.</span></span>


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="1ccb2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ccb2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ccb2-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="1ccb2-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="1ccb2-109">Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="1ccb2-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="1ccb2-110">Impostare il membro **lParam** su **true** per registrare AppBar o **false** per annullarne la registrazione.</span><span class="sxs-lookup"><span data-stu-id="1ccb2-110">Set the **lParam** member is to **TRUE** to register the appbar or **FALSE** to unregister it.</span></span> <span data-ttu-id="1ccb2-111">Quando si invia questo messaggio, è necessario specificare i membri **cbSize**, **HWND**, **uEdge**, **RC** e **lParam** . tutti gli altri membri vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="1ccb2-111">You must specify the **cbSize**, **hWnd**, **uEdge**, **rc**, and **lParam** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ccb2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ccb2-112">Return value</span></span>

<span data-ttu-id="1ccb2-113">Restituisce **true** se ha esito positivo o **false** se si verifica un errore o se un AppBar di Nascondi automaticamente è già registrato per il bordo specificato sul monitor specificato.</span><span class="sxs-lookup"><span data-stu-id="1ccb2-113">Returns **TRUE** if successful, or **FALSE** if an error occurs or if an autohide appbar is already registered for the given edge on the given monitor.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ccb2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ccb2-114">Remarks</span></span>

<span data-ttu-id="1ccb2-115">Il sistema consente un solo AppBar di Nascondi automaticamente per ogni bordo di ogni monitor.</span><span class="sxs-lookup"><span data-stu-id="1ccb2-115">The system allows only one autohide appbar for each edge of each monitor.</span></span> <span data-ttu-id="1ccb2-116">Il monitoraggio è determinato dal membro **RC** e il bordo è determinato dal membro **UEdge** della struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="1ccb2-116">The monitor is determined by the **rc** member and the edge is determined by the **uEdge** member of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ccb2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ccb2-117">Requirements</span></span>



| <span data-ttu-id="1ccb2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ccb2-118">Requirement</span></span> | <span data-ttu-id="1ccb2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1ccb2-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ccb2-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ccb2-120">Header</span></span><br/> | <dl> <span data-ttu-id="1ccb2-121"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ccb2-121"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ccb2-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ccb2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ccb2-123">**\_GETAUTOHIDEBAR ABM**</span><span class="sxs-lookup"><span data-stu-id="1ccb2-123">**ABM\_GETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="1ccb2-124">**\_GETAUTOHIDEBAREX ABM**</span><span class="sxs-lookup"><span data-stu-id="1ccb2-124">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="1ccb2-125">**\_SETAUTOHIDEBAR ABM**</span><span class="sxs-lookup"><span data-stu-id="1ccb2-125">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> </dl>

 

 





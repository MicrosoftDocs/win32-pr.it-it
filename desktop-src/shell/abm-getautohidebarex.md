---
description: Recupera l'handle per il AppBar di Nascondi automaticamente associato a un bordo dello schermo. Questo messaggio estende il \_ GETAUTOHIDEBAR ABM consentendo di specificare un particolare monitoraggio, da usare in più situazioni di monitoraggio.
title: Messaggio ABM_GETAUTOHIDEBAREX (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 538EA230-06DF-4441-A6AA-9DD613521BE1
api_name:
- ABM_GETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ef95739a1031efb199e6acd99686e0858a9630e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982971"
---
# <a name="abm_getautohidebarex-message"></a><span data-ttu-id="12724-104">\_Messaggio GETAUTOHIDEBAREX ABM</span><span class="sxs-lookup"><span data-stu-id="12724-104">ABM\_GETAUTOHIDEBAREX message</span></span>

<span data-ttu-id="12724-105">Recupera l'handle per il AppBar di Nascondi automaticamente associato a un bordo dello schermo.</span><span class="sxs-lookup"><span data-stu-id="12724-105">Retrieves the handle to the autohide appbar associated with an edge of the screen.</span></span> <span data-ttu-id="12724-106">Questo messaggio estende [**il \_ GETAUTOHIDEBAR ABM**](abm-getautohidebar.md) consentendo di specificare un particolare monitoraggio, da usare in più situazioni di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="12724-106">This message extends [**ABM\_GETAUTOHIDEBAR**](abm-getautohidebar.md) by enabling you to specify a particular monitor, for use in multiple monitor situations.</span></span>


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a><span data-ttu-id="12724-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="12724-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12724-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="12724-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="12724-109">Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) che specifica il bordo dello schermo e il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="12724-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that specifies the screen edge and monitor.</span></span> <span data-ttu-id="12724-110">Quando si invia questo messaggio, è necessario specificare i membri **cbSize**, **uEdge** e **RC** . tutti gli altri membri vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="12724-110">You must specify the **cbSize**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12724-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12724-111">Return value</span></span>

<span data-ttu-id="12724-112">Restituisce l'handle per il AppBar di Nascondi automaticamente.</span><span class="sxs-lookup"><span data-stu-id="12724-112">Returns the handle to the autohide appbar.</span></span> <span data-ttu-id="12724-113">Il valore restituito è **null** se si verifica un errore o se non è associato alcun AppBar di Nascondi automaticamente al bordo specificato del monitor specificato.</span><span class="sxs-lookup"><span data-stu-id="12724-113">The return value is **NULL** if an error occurs or if no autohide appbar is associated with the given edge of the given monitor.</span></span>

## <a name="requirements"></a><span data-ttu-id="12724-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12724-114">Requirements</span></span>



| <span data-ttu-id="12724-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="12724-115">Requirement</span></span> | <span data-ttu-id="12724-116">Valore</span><span class="sxs-lookup"><span data-stu-id="12724-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12724-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12724-117">Header</span></span><br/> | <dl> <span data-ttu-id="12724-118"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="12724-118"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12724-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12724-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12724-120">**\_GETAUTOHIDEBAR ABM**</span><span class="sxs-lookup"><span data-stu-id="12724-120">**ABM\_GETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="12724-121">**\_SETAUTOHIDEBAR ABM**</span><span class="sxs-lookup"><span data-stu-id="12724-121">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> <dt>

[<span data-ttu-id="12724-122">**\_SETAUTOHIDEBAREX ABM**</span><span class="sxs-lookup"><span data-stu-id="12724-122">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 





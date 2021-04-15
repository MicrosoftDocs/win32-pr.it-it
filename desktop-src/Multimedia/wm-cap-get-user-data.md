---
title: Messaggio di WM_CAP_GET_USER_DATA (VFW. h)
description: Il \_ messaggio WM Cap \_ get \_ User \_ Data recupera un \_ valore di dati ptr lungo associato a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capGetUserData.
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- WM_CAP_GET_USER_DATA messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_GET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02951667600acba115f506a610b167b72b69ea99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518634"
---
# <a name="wm_cap_get_user_data-message"></a><span data-ttu-id="c6690-105">\_ \_ \_ Messaggio dati utente per ottenere WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="c6690-105">WM\_CAP\_GET\_USER\_DATA message</span></span>

<span data-ttu-id="c6690-106">Il messaggio **WM \_ Cap \_ get \_ User \_ Data** recupera un valore di dati **\_ ptr lungo** associato a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="c6690-106">The **WM\_CAP\_GET\_USER\_DATA** message retrieves a **LONG\_PTR** data value associated with a capture window.</span></span> <span data-ttu-id="c6690-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) .</span><span class="sxs-lookup"><span data-stu-id="c6690-107">You can send this message explicitly or by using the [**capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) macro.</span></span>


```C++
WM_CAP_GET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="c6690-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6690-108">Return Value</span></span>

<span data-ttu-id="c6690-109">Restituisce un valore salvato in precedenza utilizzando il messaggio di [**\_ \_ \_ \_ dati utente per l'impostazione di WM Cap**](wm-cap-set-user-data.md) .</span><span class="sxs-lookup"><span data-stu-id="c6690-109">Returns a value previously saved by using the [**WM\_CAP\_SET\_USER\_DATA**](wm-cap-set-user-data.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6690-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6690-110">Requirements</span></span>



| <span data-ttu-id="c6690-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6690-111">Requirement</span></span> | <span data-ttu-id="c6690-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c6690-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c6690-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6690-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c6690-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c6690-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c6690-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6690-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c6690-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c6690-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c6690-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6690-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6690-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6690-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6690-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6690-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6690-120">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="c6690-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="c6690-121">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="c6690-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






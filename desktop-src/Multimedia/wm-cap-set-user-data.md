---
title: Messaggio di WM_CAP_SET_USER_DATA (VFW. h)
description: Il \_ messaggio WM Cap \_ set \_ User \_ Data associa un \_ valore di dati ptr lungo a una finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capSetUserData.
ms.assetid: 067502e3-f009-4cf2-b612-4a0b64624416
keywords:
- WM_CAP_SET_USER_DATA messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542b8e49f740bfc265824947237841dede1f6065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121390"
---
# <a name="wm_cap_set_user_data-message"></a><span data-ttu-id="c870b-105">\_Messaggio di \_ \_ dati utente \_ per l'impostazione di WM Cap</span><span class="sxs-lookup"><span data-stu-id="c870b-105">WM\_CAP\_SET\_USER\_DATA message</span></span>

<span data-ttu-id="c870b-106">Il messaggio **WM \_ Cap \_ set \_ User \_ Data** associa un valore di dati **\_ ptr lungo** a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="c870b-106">The **WM\_CAP\_SET\_USER\_DATA** message associates a **LONG\_PTR** data value with a capture window.</span></span> <span data-ttu-id="c870b-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetUserData**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) .</span><span class="sxs-lookup"><span data-stu-id="c870b-107">You can send this message explicitly or by using the [**capSetUserData**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) macro.</span></span>


```C++
WM_CAP_SET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = (LPARAM)lUser; 
```



## <a name="parameters"></a><span data-ttu-id="c870b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c870b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c870b-109"><span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*</span><span class="sxs-lookup"><span data-stu-id="c870b-109"><span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*</span></span>
</dt> <dd>

<span data-ttu-id="c870b-110">Valore di dati da associare a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="c870b-110">Data value to associate with a capture window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c870b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c870b-111">Return Value</span></span>

<span data-ttu-id="c870b-112">Restituisce **true** se l'operazione è riuscita o **false** se è in corso l'acquisizione di flussi.</span><span class="sxs-lookup"><span data-stu-id="c870b-112">Returns **TRUE** if successful or **FALSE** if streaming capture is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="c870b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c870b-113">Remarks</span></span>

<span data-ttu-id="c870b-114">In genere questo messaggio viene usato per puntare a un blocco di dati associato a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="c870b-114">Typically this message is used to point to a block of data associated with a capture window.</span></span>

## <a name="requirements"></a><span data-ttu-id="c870b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c870b-115">Requirements</span></span>



| <span data-ttu-id="c870b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c870b-116">Requirement</span></span> | <span data-ttu-id="c870b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c870b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c870b-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c870b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c870b-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c870b-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c870b-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c870b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c870b-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c870b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c870b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c870b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c870b-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c870b-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c870b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c870b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c870b-125">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="c870b-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="c870b-126">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="c870b-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






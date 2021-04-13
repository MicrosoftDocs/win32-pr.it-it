---
title: Messaggio di WM_CAP_DRIVER_CONNECT (VFW. h)
description: Il \_ \_ messaggio connessione driver WM Cap \_ connette una finestra di acquisizione a un driver di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capDriverConnect.
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- WM_CAP_DRIVER_CONNECT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_CONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fdeb89968926429f7225912e3d1b3b348e287
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400530"
---
# <a name="wm_cap_driver_connect-message"></a><span data-ttu-id="9102f-105">\_Messaggio di \_ connessione driver WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="9102f-105">WM\_CAP\_DRIVER\_CONNECT message</span></span>

<span data-ttu-id="9102f-106">Il **messaggio \_ \_ \_ connessione driver WM Cap** connette una finestra di acquisizione a un driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="9102f-106">The **WM\_CAP\_DRIVER\_CONNECT** message connects a capture window to a capture driver.</span></span> <span data-ttu-id="9102f-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) .</span><span class="sxs-lookup"><span data-stu-id="9102f-107">You can send this message explicitly or by using the [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) macro.</span></span>


```C++
WM_CAP_DRIVER_CONNECT 
wParam = (WPARAM) (iIndex); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="9102f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9102f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9102f-109"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="9102f-109"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="9102f-110">Indice del driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="9102f-110">Index of the capture driver.</span></span> <span data-ttu-id="9102f-111">L'indice può variare da 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="9102f-111">The index can range from 0 through 9.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9102f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9102f-112">Return Value</span></span>

<span data-ttu-id="9102f-113">Restituisce **true** se l'operazione ha esito positivo o **false** se il driver di acquisizione specificato non può essere connesso alla finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="9102f-113">Returns **TRUE** if successful or **FALSE** if the specified capture driver cannot be connected to the capture window.</span></span>

## <a name="remarks"></a><span data-ttu-id="9102f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9102f-114">Remarks</span></span>

<span data-ttu-id="9102f-115">La connessione di un driver di acquisizione a una finestra di acquisizione disconnette automaticamente qualsiasi driver di acquisizione connesso in precedenza.</span><span class="sxs-lookup"><span data-stu-id="9102f-115">Connecting a capture driver to a capture window automatically disconnects any previously connected capture driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="9102f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9102f-116">Requirements</span></span>



| <span data-ttu-id="9102f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9102f-117">Requirement</span></span> | <span data-ttu-id="9102f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9102f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9102f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9102f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9102f-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9102f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9102f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9102f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9102f-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9102f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9102f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9102f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9102f-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9102f-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9102f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9102f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9102f-126">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="9102f-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="9102f-127">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="9102f-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






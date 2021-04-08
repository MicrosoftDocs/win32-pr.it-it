---
title: Messaggio di WM_CAP_GET_STATUS (VFW. h)
description: Il \_ \_ \_ messaggio di stato WM Cap Get recupera lo stato della finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capGetStatus.
ms.assetid: 31349599-a52c-45ba-8f08-91008773f317
keywords:
- WM_CAP_GET_STATUS messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_GET_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ef6590770e8a9ece3eb8abaffb4dbca0b1a4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047826"
---
# <a name="wm_cap_get_status-message"></a><span data-ttu-id="33a26-105">\_Messaggio di \_ stato Get Cap \_ WM</span><span class="sxs-lookup"><span data-stu-id="33a26-105">WM\_CAP\_GET\_STATUS message</span></span>

<span data-ttu-id="33a26-106">Il messaggio di **\_ \_ \_ stato WM Cap Get** recupera lo stato della finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="33a26-106">The **WM\_CAP\_GET\_STATUS** message retrieves the status of the capture window.</span></span> <span data-ttu-id="33a26-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) .</span><span class="sxs-lookup"><span data-stu-id="33a26-107">You can send this message explicitly or by using the [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) macro.</span></span>


```C++
WM_CAP_GET_STATUS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPSTATUS) (s); 
```



## <a name="parameters"></a><span data-ttu-id="33a26-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="33a26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33a26-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="33a26-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="33a26-110">Dimensione, in byte, della struttura a cui fa riferimento **s**.</span><span class="sxs-lookup"><span data-stu-id="33a26-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="33a26-111"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="33a26-111"><span id="s"></span><span id="S"></span>*s*</span></span>
</dt> <dd>

<span data-ttu-id="33a26-112">Puntatore a una struttura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) .</span><span class="sxs-lookup"><span data-stu-id="33a26-112">Pointer to a [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33a26-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33a26-113">Return Value</span></span>

<span data-ttu-id="33a26-114">Restituisce **true** se l'operazione ha esito positivo o **false** se la finestra di acquisizione non è connessa a un driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="33a26-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="33a26-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="33a26-115">Remarks</span></span>

<span data-ttu-id="33a26-116">La struttura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) contiene lo stato corrente della finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="33a26-116">The [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure contains the current state of the capture window.</span></span> <span data-ttu-id="33a26-117">Poiché questo stato è dinamico e cambia in risposta a vari messaggi, l'applicazione deve inizializzare questa struttura dopo l'invio del messaggio [**WM \_ Cap \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md) (o usando la macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ) e ogni volta che è necessario abilitare le voci di menu o determinare lo stato effettivo della finestra.</span><span class="sxs-lookup"><span data-stu-id="33a26-117">Since this state is dynamic and changes in response to various messages, the application should initialize this structure after sending the [**WM\_CAP\_DLG\_VIDEOFORMAT**](wm-cap-dlg-videoformat.md) message (or using the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro) and whenever it needs to enable menu items or determine the actual state of the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="33a26-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33a26-118">Requirements</span></span>



| <span data-ttu-id="33a26-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="33a26-119">Requirement</span></span> | <span data-ttu-id="33a26-120">Valore</span><span class="sxs-lookup"><span data-stu-id="33a26-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="33a26-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33a26-121">Minimum supported client</span></span><br/> | <span data-ttu-id="33a26-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="33a26-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="33a26-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33a26-123">Minimum supported server</span></span><br/> | <span data-ttu-id="33a26-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="33a26-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="33a26-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33a26-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="33a26-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="33a26-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33a26-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33a26-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33a26-128">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="33a26-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="33a26-129">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="33a26-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






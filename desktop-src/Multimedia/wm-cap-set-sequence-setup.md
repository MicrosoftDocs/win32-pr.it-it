---
title: Messaggio di WM_CAP_SET_SEQUENCE_SETUP (VFW. h)
description: Il \_ messaggio di configurazione della sequenza di set di WM Cap \_ \_ \_ imposta i parametri di configurazione usati con l'acquisizione di streaming. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capCaptureSetSetup.
ms.assetid: ba9adb26-6627-469b-a836-f4f277ddb7c4
keywords:
- WM_CAP_SET_SEQUENCE_SETUP messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a2129021f31694d9e601ecd97503e2a5f5c925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518952"
---
# <a name="wm_cap_set_sequence_setup-message"></a><span data-ttu-id="badfe-105">\_Messaggio di \_ \_ installazione sequenza di set Cap WM \_</span><span class="sxs-lookup"><span data-stu-id="badfe-105">WM\_CAP\_SET\_SEQUENCE\_SETUP message</span></span>

<span data-ttu-id="badfe-106">Il messaggio di configurazione della **sequenza di set di WM \_ \_ \_ \_ Cap** imposta i parametri di configurazione usati con l'acquisizione di streaming.</span><span class="sxs-lookup"><span data-stu-id="badfe-106">The **WM\_CAP\_SET\_SEQUENCE\_SETUP** message sets the configuration parameters used with streaming capture.</span></span> <span data-ttu-id="badfe-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) .</span><span class="sxs-lookup"><span data-stu-id="badfe-107">You can send this message explicitly or by using the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro.</span></span>


```C++
WM_CAP_SET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (psCapParms); 
```



## <a name="parameters"></a><span data-ttu-id="badfe-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="badfe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="badfe-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="badfe-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="badfe-110">Dimensione, in byte, della struttura a cui fa riferimento **s**.</span><span class="sxs-lookup"><span data-stu-id="badfe-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="badfe-111"><span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*psCapParms*</span><span class="sxs-lookup"><span data-stu-id="badfe-111"><span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*psCapParms*</span></span>
</dt> <dd>

<span data-ttu-id="badfe-112">Puntatore a una struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="badfe-112">Pointer to a [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="badfe-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="badfe-113">Return Value</span></span>

<span data-ttu-id="badfe-114">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="badfe-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="badfe-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="badfe-115">Remarks</span></span>

<span data-ttu-id="badfe-116">Per informazioni sui parametri usati per controllare l'acquisizione di flussi, vedere la struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="badfe-116">For information about the parameters used to control streaming capture, see the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="badfe-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="badfe-117">Requirements</span></span>



| <span data-ttu-id="badfe-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="badfe-118">Requirement</span></span> | <span data-ttu-id="badfe-119">Valore</span><span class="sxs-lookup"><span data-stu-id="badfe-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="badfe-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="badfe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="badfe-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="badfe-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="badfe-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="badfe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="badfe-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="badfe-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="badfe-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="badfe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="badfe-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="badfe-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="badfe-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="badfe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="badfe-127">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="badfe-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="badfe-128">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="badfe-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






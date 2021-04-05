---
title: Messaggio di WM_CAP_FILE_GET_CAPTURE_FILE (VFW. h)
description: Il \_ messaggio WM Cap \_ file \_ get \_ Capture \_ file restituisce il nome del file di acquisizione corrente. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capFileGetCaptureFile.
ms.assetid: 86ce2904-834d-449f-9ef8-5a158c55bbaa
keywords:
- WM_CAP_FILE_GET_CAPTURE_FILE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_FILE_GET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7008e0b217f29ad9602afbdc41cc97f9cb7ecaa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873414"
---
# <a name="wm_cap_file_get_capture_file-message"></a><span data-ttu-id="f1895-105">\_ \_ \_ \_ Messaggio file di acquisizione acquisizione file con estensione WM \_</span><span class="sxs-lookup"><span data-stu-id="f1895-105">WM\_CAP\_FILE\_GET\_CAPTURE\_FILE message</span></span>

<span data-ttu-id="f1895-106">Il messaggio **WM \_ Cap \_ file \_ get \_ Capture \_ file** restituisce il nome del file di acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="f1895-106">The **WM\_CAP\_FILE\_GET\_CAPTURE\_FILE** message returns the name of the current capture file.</span></span> <span data-ttu-id="f1895-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) .</span><span class="sxs-lookup"><span data-stu-id="f1895-107">You can send this message explicitly or by using the [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) macro.</span></span>


```C++
WM_CAP_FILE_GET_CAPTURE_FILE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="f1895-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1895-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1895-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="f1895-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="f1895-110">Dimensione, in byte, del buffer definito dall'applicazione a cui fa riferimento **szName**.</span><span class="sxs-lookup"><span data-stu-id="f1895-110">Size, in bytes, of the application-defined buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="f1895-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="f1895-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="f1895-112">Puntatore a un buffer definito dall'applicazione utilizzato per restituire il nome del file di acquisizione come stringa con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="f1895-112">Pointer to an application-defined buffer used to return the name of the capture file as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1895-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1895-113">Return Value</span></span>

<span data-ttu-id="f1895-114">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f1895-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1895-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1895-115">Remarks</span></span>

<span data-ttu-id="f1895-116">Il nome file di acquisizione predefinito è C: \\CAPTURE.AVI.</span><span class="sxs-lookup"><span data-stu-id="f1895-116">The default capture filename is C:\\CAPTURE.AVI.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1895-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1895-117">Requirements</span></span>



| <span data-ttu-id="f1895-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1895-118">Requirement</span></span> | <span data-ttu-id="f1895-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f1895-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f1895-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1895-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f1895-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f1895-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f1895-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1895-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f1895-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f1895-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f1895-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1895-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1895-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1895-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1895-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1895-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1895-127">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="f1895-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="f1895-128">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="f1895-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






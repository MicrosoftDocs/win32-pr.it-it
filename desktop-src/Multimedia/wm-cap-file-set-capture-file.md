---
title: Messaggio di WM_CAP_FILE_SET_CAPTURE_FILE (VFW. h)
description: Il file \_ \_ \_ di acquisizione del set di file di WM Cap è \_ \_ il file usato per l'acquisizione video. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capFileSetCaptureFile.
ms.assetid: d96e498b-6322-4d48-a5d7-156e95f23740
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b3f59edfc9bf01f6bd2af3b9028f8e3315e2de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963738"
---
# <a name="wm_cap_file_set_capture_file-message"></a><span data-ttu-id="0cbf5-105">\_ \_ \_ \_ Messaggio file di acquisizione del set di file di WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="0cbf5-105">WM\_CAP\_FILE\_SET\_CAPTURE\_FILE message</span></span>

<span data-ttu-id="0cbf5-106">Il file di acquisizione del set di file di **WM \_ Cap \_ \_ \_ \_** è il file usato per l'acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="0cbf5-106">The **WM\_CAP\_FILE\_SET\_CAPTURE\_FILE** message names the file used for video capture.</span></span> <span data-ttu-id="0cbf5-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) .</span><span class="sxs-lookup"><span data-stu-id="0cbf5-107">You can send this message explicitly or by using the [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) macro.</span></span>


```C++
WM_CAP_FILE_SET_CAPTURE_FILE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="0cbf5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0cbf5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cbf5-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="0cbf5-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="0cbf5-110">Puntatore alla stringa con terminazione null che contiene il nome del file di acquisizione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="0cbf5-110">Pointer to the null-terminated string that contains the name of the capture file to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cbf5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0cbf5-111">Return Value</span></span>

<span data-ttu-id="0cbf5-112">Restituisce **true** se l'operazione ha esito **positivo o negativo** se il nome del file non è valido o se è in corso l'acquisizione di un flusso o un singolo frame.</span><span class="sxs-lookup"><span data-stu-id="0cbf5-112">Returns **TRUE** if successful or **FALSE** if the filename is invalid, or if streaming or single-frame capture is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cbf5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0cbf5-113">Remarks</span></span>

<span data-ttu-id="0cbf5-114">Questo messaggio archivia il nome del file in una struttura interna.</span><span class="sxs-lookup"><span data-stu-id="0cbf5-114">This message stores the filename in an internal structure.</span></span> <span data-ttu-id="0cbf5-115">Non crea, alloca o apre il file specificato.</span><span class="sxs-lookup"><span data-stu-id="0cbf5-115">It does not create, allocate, or open the specified file.</span></span> <span data-ttu-id="0cbf5-116">Il nome file di acquisizione predefinito è C: \\CAPTURE.AVI.</span><span class="sxs-lookup"><span data-stu-id="0cbf5-116">The default capture filename is C:\\CAPTURE.AVI.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cbf5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cbf5-117">Requirements</span></span>



| <span data-ttu-id="0cbf5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cbf5-118">Requirement</span></span> | <span data-ttu-id="0cbf5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0cbf5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0cbf5-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cbf5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0cbf5-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0cbf5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0cbf5-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cbf5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0cbf5-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0cbf5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0cbf5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0cbf5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cbf5-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cbf5-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cbf5-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0cbf5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cbf5-127">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="0cbf5-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="0cbf5-128">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="0cbf5-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






---
title: Messaggio di WM_CAP_FILE_ALLOCATE (VFW. h)
description: Il \_ \_ \_ messaggio di allocazione file WM Cap crea (prealloca) un file di acquisizione di una dimensione specificata. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capFileAlloc.
ms.assetid: 31ebe824-4a30-4212-9479-a5cbd8fc1e1d
keywords:
- WM_CAP_FILE_ALLOCATE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_FILE_ALLOCATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d36cec54e5775641118679b24b0d4b3b1767693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475856"
---
# <a name="wm_cap_file_allocate-message"></a><span data-ttu-id="38c59-105">\_Messaggio di \_ allocazione file WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="38c59-105">WM\_CAP\_FILE\_ALLOCATE message</span></span>

<span data-ttu-id="38c59-106">Il messaggio di **\_ \_ \_ allocazione file WM Cap** crea (prealloca) un file di acquisizione di una dimensione specificata.</span><span class="sxs-lookup"><span data-stu-id="38c59-106">The **WM\_CAP\_FILE\_ALLOCATE** message creates (preallocates) a capture file of a specified size.</span></span> <span data-ttu-id="38c59-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) .</span><span class="sxs-lookup"><span data-stu-id="38c59-107">You can send this message explicitly or by using the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro.</span></span>


```C++
WM_CAP_FILE_ALLOCATE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (DWORD) (dwSize); 
```



## <a name="parameters"></a><span data-ttu-id="38c59-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="38c59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38c59-109"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize*</span><span class="sxs-lookup"><span data-stu-id="38c59-109"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize*</span></span>
</dt> <dd>

<span data-ttu-id="38c59-110">Dimensione, in byte, per la creazione del file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="38c59-110">Size, in bytes, to create the capture file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38c59-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38c59-111">Return Value</span></span>

<span data-ttu-id="38c59-112">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="38c59-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="38c59-113">Se si verifica un errore e viene impostata una funzione di callback di errore utilizzando il messaggio di errore di richiamata di [**WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , viene chiamata la funzione di callback dell'errore.</span><span class="sxs-lookup"><span data-stu-id="38c59-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="38c59-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="38c59-114">Remarks</span></span>

<span data-ttu-id="38c59-115">È possibile migliorare significativamente le prestazioni di acquisizione di flussi preallocando un file di acquisizione sufficientemente grande da archiviare un intero clip video e deframmentare il file di acquisizione prima di acquisire la clip.</span><span class="sxs-lookup"><span data-stu-id="38c59-115">You can improve streaming capture performance significantly by preallocating a capture file large enough to store an entire video clip and by defragmenting the capture file before capturing the clip.</span></span>

## <a name="requirements"></a><span data-ttu-id="38c59-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38c59-116">Requirements</span></span>



| <span data-ttu-id="38c59-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="38c59-117">Requirement</span></span> | <span data-ttu-id="38c59-118">Valore</span><span class="sxs-lookup"><span data-stu-id="38c59-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="38c59-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38c59-119">Minimum supported client</span></span><br/> | <span data-ttu-id="38c59-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="38c59-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="38c59-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38c59-121">Minimum supported server</span></span><br/> | <span data-ttu-id="38c59-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="38c59-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="38c59-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38c59-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="38c59-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="38c59-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38c59-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38c59-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38c59-126">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="38c59-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="38c59-127">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="38c59-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






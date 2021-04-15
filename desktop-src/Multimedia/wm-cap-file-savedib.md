---
title: Messaggio di WM_CAP_FILE_SAVEDIB (VFW. h)
description: Il \_ messaggio WM Cap \_ file \_ SAVEDIB copia il frame corrente in un file DIB. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capFileSaveDIB.
ms.assetid: bf6d343b-9236-4e68-bbda-2ed6e197a5cb
keywords:
- WM_CAP_FILE_SAVEDIB messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEDIB
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2155febfdac1b3f24133df47ce206c8e5ec33d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479060"
---
# <a name="wm_cap_file_savedib-message"></a><span data-ttu-id="d427f-105">\_ \_ Messaggio SAVEDIB file WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="d427f-105">WM\_CAP\_FILE\_SAVEDIB message</span></span>

<span data-ttu-id="d427f-106">Il messaggio **WM \_ Cap \_ file \_ SAVEDIB** copia il frame corrente in un file DIB.</span><span class="sxs-lookup"><span data-stu-id="d427f-106">The **WM\_CAP\_FILE\_SAVEDIB** message copies the current frame to a DIB file.</span></span> <span data-ttu-id="d427f-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) .</span><span class="sxs-lookup"><span data-stu-id="d427f-107">You can send this message explicitly or by using the [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) macro.</span></span>


```C++
WM_CAP_FILE_SAVEDIB 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="d427f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d427f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d427f-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="d427f-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="d427f-110">Puntatore alla stringa con terminazione null che contiene il nome del file DIB di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d427f-110">Pointer to the null-terminated string that contains the name of the destination DIB file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d427f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d427f-111">Return Value</span></span>

<span data-ttu-id="d427f-112">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d427f-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="d427f-113">Se si verifica un errore e viene impostata una funzione di callback di errore utilizzando il messaggio di errore di richiamata di [**WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , viene chiamata la funzione di callback dell'errore.</span><span class="sxs-lookup"><span data-stu-id="d427f-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="d427f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d427f-114">Remarks</span></span>

<span data-ttu-id="d427f-115">Se il driver di acquisizione fornisce frame in formato compresso, questa chiamata tenta di decomprimere il frame prima di scrivere il file.</span><span class="sxs-lookup"><span data-stu-id="d427f-115">If the capture driver supplies frames in a compressed format, this call attempts to decompress the frame before writing the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="d427f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d427f-116">Requirements</span></span>



| <span data-ttu-id="d427f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d427f-117">Requirement</span></span> | <span data-ttu-id="d427f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d427f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d427f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d427f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d427f-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d427f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d427f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d427f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d427f-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d427f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d427f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d427f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d427f-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d427f-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d427f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d427f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d427f-126">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="d427f-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d427f-127">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="d427f-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






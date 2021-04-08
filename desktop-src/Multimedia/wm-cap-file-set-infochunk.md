---
title: Messaggio di WM_CAP_FILE_SET_INFOCHUNK (VFW. h)
description: Il \_ \_ \_ set di file di WM Cap \_ imposta INFOCHUNK e cancella i blocchi di informazioni.
ms.assetid: 67d11a05-a2b4-45d2-ba66-83a198745303
keywords:
- WM_CAP_FILE_SET_INFOCHUNK messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_INFOCHUNK
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 067ba00563a5ca511f13b23615fc4542090ba397
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047890"
---
# <a name="wm_cap_file_set_infochunk-message"></a><span data-ttu-id="e8880-104">\_ \_ \_ Messaggio INFOCHUNK set di file WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="e8880-104">WM\_CAP\_FILE\_SET\_INFOCHUNK message</span></span>

<span data-ttu-id="e8880-105">Il **set di file di WM \_ Cap imposta \_ \_ \_ INFOCHUNK** e cancella i blocchi di informazioni.</span><span class="sxs-lookup"><span data-stu-id="e8880-105">The **WM\_CAP\_FILE\_SET\_INFOCHUNK** message sets and clears information chunks.</span></span> <span data-ttu-id="e8880-106">I blocchi di informazioni possono essere inseriti in un file AVI durante l'acquisizione per incorporare stringhe di testo o dati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="e8880-106">Information chunks can be inserted in an AVI file during capture to embed text strings or custom data.</span></span> <span data-ttu-id="e8880-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .</span><span class="sxs-lookup"><span data-stu-id="e8880-107">You can send this message explicitly or by using the [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) macro.</span></span>


```C++
WM_CAP_FILE_SET_INFOCHUNK 
wParam = (WPARAM)0; 
lParam = (LPARAM) (LPCAPINFOCHUNK) (lpInfoChunk); 
```



## <a name="parameters"></a><span data-ttu-id="e8880-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8880-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8880-109"><span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*</span><span class="sxs-lookup"><span data-stu-id="e8880-109"><span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*</span></span>
</dt> <dd>

<span data-ttu-id="e8880-110">Puntatore a una struttura [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) che definisce il blocco di informazioni da creare o eliminare.</span><span class="sxs-lookup"><span data-stu-id="e8880-110">Pointer to a [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) structure defining the information chunk to be created or deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8880-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8880-111">Return Value</span></span>

<span data-ttu-id="e8880-112">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e8880-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="e8880-113">Se si verifica un errore e viene impostata una funzione di callback di errore utilizzando il messaggio di errore di richiamata di [**WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , viene chiamata la funzione di callback dell'errore.</span><span class="sxs-lookup"><span data-stu-id="e8880-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8880-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8880-114">Remarks</span></span>

<span data-ttu-id="e8880-115">È possibile aggiungere più blocchi di informazioni registrate a un file AVI.</span><span class="sxs-lookup"><span data-stu-id="e8880-115">Multiple registered information chunks can be added to an AVI file.</span></span> <span data-ttu-id="e8880-116">Dopo aver impostato un blocco di informazioni, questo continua a essere aggiunto ai file di acquisizione successivi fino alla cancellazione della voce o alla cancellazione di tutte le voci del blocco di informazioni.</span><span class="sxs-lookup"><span data-stu-id="e8880-116">After an information chunk is set, it continues to be added to subsequent capture files until either the entry is cleared or all information chunk entries are cleared.</span></span> <span data-ttu-id="e8880-117">Per cancellare una singola voce, specificare il blocco Information nel membro **fccInfoID** e **null** nel membro **lpData** della struttura [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) .</span><span class="sxs-lookup"><span data-stu-id="e8880-117">To clear a single entry, specify the information chunk in the **fccInfoID** member and **NULL** in the **lpData** member of the [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) structure.</span></span> <span data-ttu-id="e8880-118">Per cancellare tutte le voci, specificare **null** in **fccInfoID**.</span><span class="sxs-lookup"><span data-stu-id="e8880-118">To clear all entries, specify **NULL** in **fccInfoID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8880-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8880-119">Requirements</span></span>



| <span data-ttu-id="e8880-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8880-120">Requirement</span></span> | <span data-ttu-id="e8880-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e8880-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e8880-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8880-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e8880-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e8880-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e8880-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8880-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e8880-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e8880-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e8880-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8880-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8880-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8880-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8880-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8880-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8880-129">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="e8880-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="e8880-130">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="e8880-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






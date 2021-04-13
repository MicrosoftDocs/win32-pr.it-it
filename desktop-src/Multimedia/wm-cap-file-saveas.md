---
title: Messaggio di WM_CAP_FILE_SAVEAS (VFW. h)
description: Il \_ \_ messaggio SaveAs del file WM Cap \_ copia il contenuto del file di acquisizione in un altro file. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capFileSaveAs.
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- WM_CAP_FILE_SAVEAS messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aca099fefab7ca0f4ef391b1b65e89938a947a01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400424"
---
# <a name="wm_cap_file_saveas-message"></a><span data-ttu-id="506e3-105">\_ \_ Messaggio SaveAs file di WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="506e3-105">WM\_CAP\_FILE\_SAVEAS message</span></span>

<span data-ttu-id="506e3-106">Il **messaggio \_ \_ \_ SaveAs del file WM Cap** copia il contenuto del file di acquisizione in un altro file.</span><span class="sxs-lookup"><span data-stu-id="506e3-106">The **WM\_CAP\_FILE\_SAVEAS** message copies the contents of the capture file to another file.</span></span> <span data-ttu-id="506e3-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) .</span><span class="sxs-lookup"><span data-stu-id="506e3-107">You can send this message explicitly or by using the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro.</span></span>


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="506e3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="506e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="506e3-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="506e3-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="506e3-110">Puntatore alla stringa con terminazione null che contiene il nome del file di destinazione utilizzato per copiare il file.</span><span class="sxs-lookup"><span data-stu-id="506e3-110">Pointer to the null-terminated string that contains the name of the destination file used to copy the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="506e3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="506e3-111">Return Value</span></span>

<span data-ttu-id="506e3-112">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="506e3-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="506e3-113">Se si verifica un errore e viene impostata una funzione di callback di errore utilizzando il messaggio di errore di richiamata di [**WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , viene chiamata la funzione di callback dell'errore.</span><span class="sxs-lookup"><span data-stu-id="506e3-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="506e3-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="506e3-114">Remarks</span></span>

<span data-ttu-id="506e3-115">Questo messaggio non modifica il nome o il contenuto del file di acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="506e3-115">This message does not change the name or contents of the current capture file.</span></span>

<span data-ttu-id="506e3-116">Se l'operazione di copia ha esito negativo a causa di un errore del disco completo, il file di destinazione viene eliminato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="506e3-116">If the copy operation is unsuccessful due to a disk full error, the destination file is automatically deleted.</span></span>

<span data-ttu-id="506e3-117">In genere, un file di acquisizione è preallocato per il segmento di acquisizione più grande previsto e solo una parte di esso potrebbe essere usato per acquisire i dati.</span><span class="sxs-lookup"><span data-stu-id="506e3-117">Typically, a capture file is preallocated for the largest capture segment anticipated and only a portion of it might be used to capture data.</span></span> <span data-ttu-id="506e3-118">Questo messaggio copia solo la parte del file che contiene i dati di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="506e3-118">This message copies only the portion of the file containing the capture data.</span></span>

## <a name="requirements"></a><span data-ttu-id="506e3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="506e3-119">Requirements</span></span>



| <span data-ttu-id="506e3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="506e3-120">Requirement</span></span> | <span data-ttu-id="506e3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="506e3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="506e3-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="506e3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="506e3-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="506e3-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="506e3-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="506e3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="506e3-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="506e3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="506e3-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="506e3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="506e3-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="506e3-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="506e3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="506e3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="506e3-129">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="506e3-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="506e3-130">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="506e3-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






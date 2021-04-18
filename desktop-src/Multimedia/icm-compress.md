---
title: Messaggio di ICM_COMPRESS (VFW. h)
description: Il messaggio MCI Compress invia una \_ notifica a un driver di compressione video per comprimere un frame di dati in un buffer definito dall'applicazione.
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- ICM_COMPRESS messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_COMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8021a4c18ab47c9b5b848dd1cb097358f2714bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302272"
---
# <a name="icm_compress-message"></a><span data-ttu-id="53500-104">\_Messaggio di compressione ICM</span><span class="sxs-lookup"><span data-stu-id="53500-104">ICM\_COMPRESS message</span></span>

<span data-ttu-id="53500-105">Il messaggio **MCI \_ Compress** invia una notifica a un driver di compressione video per comprimere un frame di dati in un buffer definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="53500-105">The **ICM\_COMPRESS** message notifies a video compression driver to compress a frame of data into an application-defined buffer.</span></span>


```C++
ICM_COMPRESS 
wParam = (DWORD) (LPVOID) &icc; 
lParam = sizeof(ICCOMPRESS); 
```



## <a name="parameters"></a><span data-ttu-id="53500-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="53500-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53500-107"><span id="icc"></span><span id="ICC"></span>*ICC*</span><span class="sxs-lookup"><span data-stu-id="53500-107"><span id="icc"></span><span id="ICC"></span>*icc*</span></span>
</dt> <dd>

<span data-ttu-id="53500-108">Puntatore a una struttura [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress) .</span><span class="sxs-lookup"><span data-stu-id="53500-108">Pointer to an [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress) structure.</span></span> <span data-ttu-id="53500-109">I membri seguenti di questa struttura specificano i parametri di compressione: **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lpckid**, **lpdwFlags**, **dwFrameSize** e **dwQuality**.</span><span class="sxs-lookup"><span data-stu-id="53500-109">The following members of this structure specify the compression parameters: **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lpckid**, **lpdwFlags**, **dwFrameSize**, and **dwQuality**.</span></span> <span data-ttu-id="53500-110">Il driver deve anche usare il membro **biSizeImage** della struttura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) associata a **lpbiOutput** di **ICCOMPRESS** per restituire le dimensioni del frame compresso.</span><span class="sxs-lookup"><span data-stu-id="53500-110">The driver should also use the **biSizeImage** member of the [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure associated with **lpbiOutput** of **ICCOMPRESS** to return the size of the compressed frame.</span></span>

</dd> <dt>

<span data-ttu-id="53500-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="53500-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="53500-112">Dimensioni, in byte, di [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress).</span><span class="sxs-lookup"><span data-stu-id="53500-112">Size, in bytes, of [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53500-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53500-113">Return Value</span></span>

<span data-ttu-id="53500-114">Restituisce ICERR \_ OK se ha esito positivo o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="53500-114">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="53500-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53500-115">Requirements</span></span>



| <span data-ttu-id="53500-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="53500-116">Requirement</span></span> | <span data-ttu-id="53500-117">Valore</span><span class="sxs-lookup"><span data-stu-id="53500-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="53500-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53500-118">Minimum supported client</span></span><br/> | <span data-ttu-id="53500-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="53500-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="53500-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53500-120">Minimum supported server</span></span><br/> | <span data-ttu-id="53500-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="53500-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="53500-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53500-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="53500-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="53500-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53500-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53500-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53500-125">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="53500-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="53500-126">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="53500-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 


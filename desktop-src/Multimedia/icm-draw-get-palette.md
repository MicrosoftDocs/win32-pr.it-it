---
title: Messaggio di ICM_DRAW_GET_PALETTE (VFW. h)
description: Il \_ messaggio della \_ \_ tavolozza di estrazione di ICM richiede a un driver di rendering di restituire una tavolozza.
ms.assetid: 02a9df7d-e0b9-4bde-9cda-c36d2a10a23c
keywords:
- ICM_DRAW_GET_PALETTE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03f3658d2a2653f940e18e9b82b7cc3d7690ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047979"
---
# <a name="icm_draw_get_palette-message"></a><span data-ttu-id="6b189-104">\_Messaggio della \_ tavolozza di estrazione di ICM \_</span><span class="sxs-lookup"><span data-stu-id="6b189-104">ICM\_DRAW\_GET\_PALETTE message</span></span>

<span data-ttu-id="6b189-105">Il messaggio della **\_ \_ \_ tavolozza di estrazione di ICM** richiede a un driver di rendering di restituire una tavolozza.</span><span class="sxs-lookup"><span data-stu-id="6b189-105">The **ICM\_DRAW\_GET\_PALETTE** message requests a rendering driver to return a palette.</span></span>


```C++
ICM_DRAW_GET_PALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="6b189-106">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b189-106">Return Value</span></span>

<span data-ttu-id="6b189-107">Il driver deve restituire uno dei seguenti: un handle della tavolozza utilizzata, **null** se non è presente un handle da restituire oppure ICERR non \_ supportato se non supporta le tavolozze.</span><span class="sxs-lookup"><span data-stu-id="6b189-107">The driver should return one of the following: a handle of the palette being used, **NULL** if it doesn't have a handle to return, or ICERR\_UNSUPPORTED if it doesn't support palettes.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b189-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b189-108">Requirements</span></span>



| <span data-ttu-id="6b189-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b189-109">Requirement</span></span> | <span data-ttu-id="6b189-110">Valore</span><span class="sxs-lookup"><span data-stu-id="6b189-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6b189-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b189-111">Minimum supported client</span></span><br/> | <span data-ttu-id="6b189-112">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b189-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6b189-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b189-113">Minimum supported server</span></span><br/> | <span data-ttu-id="6b189-114">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b189-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6b189-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b189-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b189-116"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b189-116"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b189-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b189-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b189-118">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="6b189-118">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="6b189-119">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="6b189-119">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 






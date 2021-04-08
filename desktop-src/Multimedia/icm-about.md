---
title: Messaggio di ICM_ABOUT (VFW. h)
description: Il \_ messaggio ICM about invia una notifica a un driver di compressione video per visualizzare la finestra di dialogo informazioni su o esegue una query su un driver di compressione video per determinare se è presente una finestra di dialogo informazioni su. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICAbout.
ms.assetid: 6eca69a3-0463-48e6-befb-5003b7515e7d
keywords:
- ICM_ABOUT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_ABOUT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e03e88993ba1e345a3ea32a9de7adb2d63abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047835"
---
# <a name="icm_about-message"></a><span data-ttu-id="89748-105">ICM \_ informazioni sul messaggio</span><span class="sxs-lookup"><span data-stu-id="89748-105">ICM\_ABOUT message</span></span>

<span data-ttu-id="89748-106">Il messaggio **ICM \_ About** invia una notifica a un driver di compressione video per visualizzare la finestra di dialogo informazioni su o esegue una query su un driver di compressione video per determinare se è presente una finestra di dialogo informazioni su.</span><span class="sxs-lookup"><span data-stu-id="89748-106">The **ICM\_ABOUT** message notifies a video compression driver to display its About dialog box or queries a video compression driver to determine if it has an About dialog box.</span></span> <span data-ttu-id="89748-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) .</span><span class="sxs-lookup"><span data-stu-id="89748-107">You can send this message explicitly or by using the [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macro.</span></span>


```C++
ICM_ABOUT 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="89748-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="89748-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89748-109"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="89748-109"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="89748-110">Handle per la finestra padre della finestra di dialogo visualizzata.</span><span class="sxs-lookup"><span data-stu-id="89748-110">Handle to the parent window of the displayed dialog box.</span></span> <span data-ttu-id="89748-111">È inoltre possibile determinare se un driver dispone di una finestra di dialogo informazioni su, specificando-1 in questo parametro, come nella macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) .</span><span class="sxs-lookup"><span data-stu-id="89748-111">You can also determine if a driver has an About dialog box by specifying -1 in this parameter, as in the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) macro.</span></span> <span data-ttu-id="89748-112">Il driver restituisce ICERR \_ OK se la finestra di dialogo informazioni su o ICERR non è \_ supportata in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="89748-112">The driver returns ICERR\_OK if it has an About dialog box or ICERR\_UNSUPPORTED otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89748-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89748-113">Return Value</span></span>

<span data-ttu-id="89748-114">Restituisce ICERR \_ OK se il driver supporta questo messaggio o ICERR non \_ supportato in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="89748-114">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="89748-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89748-115">Requirements</span></span>



| <span data-ttu-id="89748-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="89748-116">Requirement</span></span> | <span data-ttu-id="89748-117">Valore</span><span class="sxs-lookup"><span data-stu-id="89748-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="89748-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89748-118">Minimum supported client</span></span><br/> | <span data-ttu-id="89748-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="89748-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="89748-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89748-120">Minimum supported server</span></span><br/> | <span data-ttu-id="89748-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="89748-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="89748-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89748-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="89748-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="89748-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89748-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89748-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89748-125">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="89748-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="89748-126">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="89748-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 






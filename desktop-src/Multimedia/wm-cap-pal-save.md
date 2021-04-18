---
title: Messaggio di WM_CAP_PAL_SAVE (VFW. h)
description: Il \_ \_ \_ messaggio di salvataggio di WM Cap salva la tavolozza corrente in un file tavolozza. I file della tavolozza usano in genere l'estensione del nome file. Alla pubblicazione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capPaletteSave.
ms.assetid: b1fa3978-9147-403f-aa08-db1a803aa5ac
keywords:
- WM_CAP_PAL_SAVE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_PAL_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5ea36b2eaf50b2555fa849a176d12d0932eed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301821"
---
# <a name="wm_cap_pal_save-message"></a><span data-ttu-id="043ca-106">\_Messaggio di \_ salvataggio del PAL WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="043ca-106">WM\_CAP\_PAL\_SAVE message</span></span>

<span data-ttu-id="043ca-107">Il messaggio di **\_ \_ \_ salvataggio di WM Cap** salva la tavolozza corrente in un file tavolozza.</span><span class="sxs-lookup"><span data-stu-id="043ca-107">The **WM\_CAP\_PAL\_SAVE** message saves the current palette to a palette file.</span></span> <span data-ttu-id="043ca-108">I file della tavolozza usano in genere l'estensione del nome file. Alla pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="043ca-108">Palette files typically use the filename extension .PAL.</span></span> <span data-ttu-id="043ca-109">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) .</span><span class="sxs-lookup"><span data-stu-id="043ca-109">You can send this message explicitly or by using the [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) macro.</span></span>


```C++
WM_CAP_PAL_SAVE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="043ca-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="043ca-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="043ca-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="043ca-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="043ca-112">Puntatore a una stringa con terminazione null che contiene il nome file della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="043ca-112">Pointer to a null-terminated string containing the palette filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="043ca-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="043ca-113">Return Value</span></span>

<span data-ttu-id="043ca-114">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="043ca-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="043ca-115">Se si verifica un errore e viene impostata una funzione di callback di errore utilizzando il messaggio di errore di richiamata di [**WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , viene chiamata la funzione di callback dell'errore.</span><span class="sxs-lookup"><span data-stu-id="043ca-115">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="043ca-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="043ca-116">Requirements</span></span>



| <span data-ttu-id="043ca-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="043ca-117">Requirement</span></span> | <span data-ttu-id="043ca-118">Valore</span><span class="sxs-lookup"><span data-stu-id="043ca-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="043ca-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="043ca-119">Minimum supported client</span></span><br/> | <span data-ttu-id="043ca-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="043ca-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="043ca-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="043ca-121">Minimum supported server</span></span><br/> | <span data-ttu-id="043ca-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="043ca-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="043ca-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="043ca-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="043ca-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="043ca-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="043ca-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="043ca-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="043ca-126">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="043ca-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="043ca-127">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="043ca-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






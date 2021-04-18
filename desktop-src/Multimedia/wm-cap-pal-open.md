---
title: Messaggio di WM_CAP_PAL_OPEN (VFW. h)
description: Il \_ \_ \_ messaggio di apertura di WM Cap consente di caricare una nuova tavolozza da un file tavolozza e di passarla a un driver di acquisizione.
ms.assetid: e77b518e-ff03-4622-978f-d9ebaa49c6a4
keywords:
- WM_CAP_PAL_OPEN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_PAL_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949bab50294251543c50d72c8d8b169cfc5514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301073"
---
# <a name="wm_cap_pal_open-message"></a><span data-ttu-id="2c888-104">\_ \_ \_ Messaggio aperto WM Cap</span><span class="sxs-lookup"><span data-stu-id="2c888-104">WM\_CAP\_PAL\_OPEN message</span></span>

<span data-ttu-id="2c888-105">Il messaggio di **\_ \_ \_ apertura di WM Cap** consente di caricare una nuova tavolozza da un file tavolozza e di passarla a un driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="2c888-105">The **WM\_CAP\_PAL\_OPEN** message loads a new palette from a palette file and passes it to a capture driver.</span></span> <span data-ttu-id="2c888-106">I file della tavolozza usano in genere l'estensione del nome file. Alla pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="2c888-106">Palette files typically use the filename extension .PAL.</span></span> <span data-ttu-id="2c888-107">Un driver di acquisizione utilizza una tavolozza quando richiesto dal formato di immagine cifrato specificato.</span><span class="sxs-lookup"><span data-stu-id="2c888-107">A capture driver uses a palette when required by the specified digitized image format.</span></span> <span data-ttu-id="2c888-108">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) .</span><span class="sxs-lookup"><span data-stu-id="2c888-108">You can send this message explicitly or by using the [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) macro.</span></span>


```C++
WM_CAP_PAL_OPEN 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="2c888-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c888-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c888-110"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="2c888-110"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="2c888-111">Puntatore a una stringa con terminazione null che contiene il nome file della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="2c888-111">Pointer to a null-terminated string containing the palette filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c888-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2c888-112">Return Value</span></span>

<span data-ttu-id="2c888-113">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2c888-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="2c888-114">Se si verifica un errore e viene impostata una funzione di callback di errore utilizzando il messaggio di errore di richiamata di [**WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , viene chiamata la funzione di callback dell'errore.</span><span class="sxs-lookup"><span data-stu-id="2c888-114">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c888-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c888-115">Requirements</span></span>



| <span data-ttu-id="2c888-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c888-116">Requirement</span></span> | <span data-ttu-id="2c888-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2c888-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2c888-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c888-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2c888-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2c888-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2c888-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c888-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2c888-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2c888-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2c888-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c888-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c888-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c888-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c888-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c888-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c888-125">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="2c888-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="2c888-126">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="2c888-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






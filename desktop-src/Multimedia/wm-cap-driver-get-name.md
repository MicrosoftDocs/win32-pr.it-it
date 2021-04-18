---
title: Messaggio di WM_CAP_DRIVER_GET_NAME (VFW. h)
description: Il \_ messaggio WM Cap \_ driver \_ get \_ Name restituisce il nome del driver di acquisizione connesso alla finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capDriverGetName.
ms.assetid: 84cecaf1-e0ff-424f-8c10-8bfe5cc2e7ea
keywords:
- WM_CAP_DRIVER_GET_NAME messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_NAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256b5f7913c83ddd278f3f3a05552b3d81070c73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475857"
---
# <a name="wm_cap_driver_get_name-message"></a><span data-ttu-id="3dd2d-105">\_Messaggio di \_ \_ nome Get driver WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="3dd2d-105">WM\_CAP\_DRIVER\_GET\_NAME message</span></span>

<span data-ttu-id="3dd2d-106">Il messaggio **WM \_ Cap \_ driver \_ get \_ Name** restituisce il nome del driver di acquisizione connesso alla finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-106">The **WM\_CAP\_DRIVER\_GET\_NAME** message returns the name of the capture driver connected to the capture window.</span></span> <span data-ttu-id="3dd2d-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) .</span><span class="sxs-lookup"><span data-stu-id="3dd2d-107">You can send this message explicitly or by using the [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_NAME 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="3dd2d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3dd2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dd2d-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="3dd2d-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="3dd2d-110">Dimensione, in byte, del buffer a cui fa riferimento **szName**.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-110">Size, in bytes, of the buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="3dd2d-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="3dd2d-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="3dd2d-112">Puntatore a un buffer definito dall'applicazione usato per restituire il nome del dispositivo come stringa con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-112">Pointer to an application-defined buffer used to return the device name as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dd2d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3dd2d-113">Return Value</span></span>

<span data-ttu-id="3dd2d-114">Restituisce **true** se l'operazione ha esito positivo o **false** se la finestra di acquisizione non è connessa a un driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dd2d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3dd2d-115">Remarks</span></span>

<span data-ttu-id="3dd2d-116">Il nome è una stringa di testo recuperata dall'area delle risorse del driver.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-116">The name is a text string retrieved from the driver's resource area.</span></span> <span data-ttu-id="3dd2d-117">Le applicazioni devono allocare circa 80 byte per questa stringa.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-117">Applications should allocate approximately 80 bytes for this string.</span></span> <span data-ttu-id="3dd2d-118">Se il driver non contiene una risorsa nome, viene restituito il nome del percorso completo del driver elencato nel registro di sistema o nel file di SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="3dd2d-118">If the driver does not contain a name resource, the full path name of the driver listed in the registry or in the SYSTEM.INI file is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dd2d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3dd2d-119">Requirements</span></span>



| <span data-ttu-id="3dd2d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dd2d-120">Requirement</span></span> | <span data-ttu-id="3dd2d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3dd2d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3dd2d-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3dd2d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3dd2d-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3dd2d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3dd2d-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3dd2d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3dd2d-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3dd2d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3dd2d-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3dd2d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dd2d-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dd2d-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dd2d-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3dd2d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dd2d-129">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="3dd2d-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="3dd2d-130">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="3dd2d-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 






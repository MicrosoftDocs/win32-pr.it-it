---
title: Messaggio di MCIWNDM_SETVOLUME (VFW. h)
description: Il \_ messaggio MCIWNDM volume imposta il livello di volume di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndSetVolume.
ms.assetid: 04151588-b761-447a-9a57-808c034c3059
keywords:
- MCIWNDM_SETVOLUME messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_SETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2215f8df3ea6f7b36b224318ebac68175ff9c265
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740231"
---
# <a name="mciwndm_setvolume-message"></a><span data-ttu-id="10183-105">\_Messaggio MCIWNDM volume</span><span class="sxs-lookup"><span data-stu-id="10183-105">MCIWNDM\_SETVOLUME message</span></span>

<span data-ttu-id="10183-106">Il messaggio **MCIWNDM \_ volume** imposta il livello di volume di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="10183-106">The **MCIWNDM\_SETVOLUME** message sets the volume level of an MCI device.</span></span> <span data-ttu-id="10183-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) .</span><span class="sxs-lookup"><span data-stu-id="10183-107">You can send this message explicitly or by using the [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) macro.</span></span>


```C++
MCIWNDM_SETVOLUME 
wParam = 0; 
lParam = (LPARAM) (UINT) iVol; 
```



## <a name="parameters"></a><span data-ttu-id="10183-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="10183-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10183-109"><span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*iVol*</span><span class="sxs-lookup"><span data-stu-id="10183-109"><span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*iVol*</span></span>
</dt> <dd>

<span data-ttu-id="10183-110">Nuovo livello di volume.</span><span class="sxs-lookup"><span data-stu-id="10183-110">New volume level.</span></span> <span data-ttu-id="10183-111">Specificare 1000 per il livello di volume normale.</span><span class="sxs-lookup"><span data-stu-id="10183-111">Specify 1000 for normal volume level.</span></span> <span data-ttu-id="10183-112">Specificare un valore superiore per un volume più alto o un valore inferiore per un volume più silenzioso.</span><span class="sxs-lookup"><span data-stu-id="10183-112">Specify a higher value for a louder volume or a lower value for a quieter volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10183-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10183-113">Return Value</span></span>

<span data-ttu-id="10183-114">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="10183-114">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="10183-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10183-115">Requirements</span></span>



| <span data-ttu-id="10183-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="10183-116">Requirement</span></span> | <span data-ttu-id="10183-117">Valore</span><span class="sxs-lookup"><span data-stu-id="10183-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="10183-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10183-118">Minimum supported client</span></span><br/> | <span data-ttu-id="10183-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="10183-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="10183-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10183-120">Minimum supported server</span></span><br/> | <span data-ttu-id="10183-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="10183-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="10183-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10183-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="10183-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="10183-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10183-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10183-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10183-125">**MCIWndSetVolume**</span><span class="sxs-lookup"><span data-stu-id="10183-125">**MCIWndSetVolume**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
</dt> </dl>

 

 






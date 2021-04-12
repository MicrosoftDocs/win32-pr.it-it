---
title: Messaggio di MCIWNDM_GETVOLUME (VFW. h)
description: Il \_ messaggio MCIWNDM GetVolume recupera l'impostazione del volume corrente di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetVolume.
ms.assetid: 3f1de023-4da8-4899-accc-409701d6e921
keywords:
- MCIWNDM_GETVOLUME messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa11fb13a56dda7cb83e3d6c98b4b66083e91b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400892"
---
# <a name="mciwndm_getvolume-message"></a><span data-ttu-id="d8b0f-105">\_Messaggio GETVOLUME MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="d8b0f-105">MCIWNDM\_GETVOLUME message</span></span>

<span data-ttu-id="d8b0f-106">Il messaggio **MCIWNDM \_ GetVolume** recupera l'impostazione del volume corrente di un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="d8b0f-106">The **MCIWNDM\_GETVOLUME** message retrieves the current volume setting of an MCI device.</span></span> <span data-ttu-id="d8b0f-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) .</span><span class="sxs-lookup"><span data-stu-id="d8b0f-107">You can send this message explicitly or by using the [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) macro.</span></span>


```C++
MCIWNDM_GETVOLUME 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="d8b0f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8b0f-108">Return Value</span></span>

<span data-ttu-id="d8b0f-109">Restituisce l'impostazione corrente del volume.</span><span class="sxs-lookup"><span data-stu-id="d8b0f-109">Returns the current volume setting.</span></span> <span data-ttu-id="d8b0f-110">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="d8b0f-110">The default value is 1000.</span></span> <span data-ttu-id="d8b0f-111">I valori più alti indicano volumi più potenti. i valori inferiori indicano volumi più tranquilli.</span><span class="sxs-lookup"><span data-stu-id="d8b0f-111">Higher values indicate louder volumes, lower values indicate quieter volumes.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8b0f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8b0f-112">Requirements</span></span>



| <span data-ttu-id="d8b0f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8b0f-113">Requirement</span></span> | <span data-ttu-id="d8b0f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d8b0f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d8b0f-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8b0f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d8b0f-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d8b0f-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d8b0f-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8b0f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d8b0f-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d8b0f-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d8b0f-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8b0f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8b0f-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8b0f-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8b0f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8b0f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8b0f-122">**MCIWndGetVolume**</span><span class="sxs-lookup"><span data-stu-id="d8b0f-122">**MCIWndGetVolume**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
</dt> </dl>

 

 






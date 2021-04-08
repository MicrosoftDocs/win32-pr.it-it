---
title: Messaggio di MCIWNDM_GET_DEST (VFW. h)
description: Il \_ messaggio MCIWNDM Get \_ dest recupera le coordinate del rettangolo di destinazione usato per lo zoom o l'estensione delle immagini di un file AVI durante la riproduzione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetDest.
ms.assetid: d4d8a3eb-aad4-4435-a23b-7a9c55fc194d
keywords:
- MCIWNDM_GET_DEST messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GET_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab5f16b434caef56e6c6aa97bfd767770dc05ee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047831"
---
# <a name="mciwndm_get_dest-message"></a><span data-ttu-id="42892-105">MCIWNDM \_ Ottieni \_ messaggio dest</span><span class="sxs-lookup"><span data-stu-id="42892-105">MCIWNDM\_GET\_DEST message</span></span>

<span data-ttu-id="42892-106">Il messaggio **MCIWNDM \_ get \_ dest** recupera le coordinate del rettangolo di destinazione usato per lo zoom o l'estensione delle immagini di un file AVI durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="42892-106">The **MCIWNDM\_GET\_DEST** message retrieves the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback.</span></span> <span data-ttu-id="42892-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) .</span><span class="sxs-lookup"><span data-stu-id="42892-107">You can send this message explicitly or by using the [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) macro.</span></span>


```C++
MCIWNDM_GET_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="42892-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="42892-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42892-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="42892-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="42892-110">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) per restituire le coordinate del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="42892-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to return the coordinates of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42892-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42892-111">Return Value</span></span>

<span data-ttu-id="42892-112">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="42892-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="42892-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42892-113">Requirements</span></span>



| <span data-ttu-id="42892-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="42892-114">Requirement</span></span> | <span data-ttu-id="42892-115">Valore</span><span class="sxs-lookup"><span data-stu-id="42892-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="42892-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42892-116">Minimum supported client</span></span><br/> | <span data-ttu-id="42892-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="42892-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="42892-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42892-118">Minimum supported server</span></span><br/> | <span data-ttu-id="42892-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="42892-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="42892-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42892-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="42892-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="42892-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42892-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42892-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42892-123">**MCIWndGetDest**</span><span class="sxs-lookup"><span data-stu-id="42892-123">**MCIWndGetDest**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)
</dt> </dl>

 


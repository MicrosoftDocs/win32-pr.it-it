---
title: Messaggio di MCIWNDM_GETSTART (VFW. h)
description: Il \_ messaggio GETstart MCIWNDM Recupera il percorso dell'inizio del contenuto di un dispositivo o di un file MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetStart.
ms.assetid: 2350616c-2aac-4ff6-b074-bb785a97cdfb
keywords:
- MCIWNDM_GETSTART messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTART
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbe88df006f1f98854e42259074d82bbd87dc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475526"
---
# <a name="mciwndm_getstart-message"></a><span data-ttu-id="24eef-105">\_Messaggio GETstart MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="24eef-105">MCIWNDM\_GETSTART message</span></span>

<span data-ttu-id="24eef-106">Il **messaggio \_ getstart MCIWNDM** Recupera il percorso dell'inizio del contenuto di un dispositivo o di un file MCI.</span><span class="sxs-lookup"><span data-stu-id="24eef-106">The **MCIWNDM\_GETSTART** message retrieves the location of the beginning of the content of an MCI device or file.</span></span> <span data-ttu-id="24eef-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) .</span><span class="sxs-lookup"><span data-stu-id="24eef-107">You can send this message explicitly or by using the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) macro.</span></span>


```C++
MCIWNDM_GETSTART 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="24eef-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24eef-108">Return Value</span></span>

<span data-ttu-id="24eef-109">Restituisce la posizione nel formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="24eef-109">Returns the location in the current time format.</span></span>

## <a name="remarks"></a><span data-ttu-id="24eef-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="24eef-110">Remarks</span></span>

<span data-ttu-id="24eef-111">In genere, il valore restituito è zero; Tuttavia, alcuni dispositivi usano una posizione iniziale diversa da zero.</span><span class="sxs-lookup"><span data-stu-id="24eef-111">Typically, the return value is zero; but some devices use a nonzero starting location.</span></span> <span data-ttu-id="24eef-112">La ricerca in questa posizione consente di impostare il dispositivo sull'avvio del supporto.</span><span class="sxs-lookup"><span data-stu-id="24eef-112">Seeking to this location sets the device to the start of the media.</span></span>

## <a name="requirements"></a><span data-ttu-id="24eef-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24eef-113">Requirements</span></span>



| <span data-ttu-id="24eef-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="24eef-114">Requirement</span></span> | <span data-ttu-id="24eef-115">Valore</span><span class="sxs-lookup"><span data-stu-id="24eef-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="24eef-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24eef-116">Minimum supported client</span></span><br/> | <span data-ttu-id="24eef-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="24eef-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="24eef-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24eef-118">Minimum supported server</span></span><br/> | <span data-ttu-id="24eef-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="24eef-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="24eef-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24eef-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="24eef-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="24eef-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24eef-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24eef-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24eef-123">**MCIWndGetStart**</span><span class="sxs-lookup"><span data-stu-id="24eef-123">**MCIWndGetStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
</dt> </dl>

 

 






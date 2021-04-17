---
title: Messaggio di MCIWNDM_GET_SOURCE (VFW. h)
description: Il \_ messaggio MCIWNDM Get \_ source recupera le coordinate del rettangolo di origine usato per ritagliare le immagini di un file AVI durante la riproduzione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetSource.
ms.assetid: d5f25926-5a3d-412e-8248-fbf307583757
keywords:
- MCIWNDM_GET_SOURCE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GET_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85147182d06386efed73229fcdd6c75372244fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400807"
---
# <a name="mciwndm_get_source-message"></a><span data-ttu-id="3c212-105">MCIWNDM \_ ottenere il \_ messaggio di origine</span><span class="sxs-lookup"><span data-stu-id="3c212-105">MCIWNDM\_GET\_SOURCE message</span></span>

<span data-ttu-id="3c212-106">Il messaggio **MCIWNDM \_ get \_ source** recupera le coordinate del rettangolo di origine usato per ritagliare le immagini di un file AVI durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="3c212-106">The **MCIWNDM\_GET\_SOURCE** message retrieves the coordinates of the source rectangle used for cropping the images of an AVI file during playback.</span></span> <span data-ttu-id="3c212-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) .</span><span class="sxs-lookup"><span data-stu-id="3c212-107">You can send this message explicitly or by using the [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) macro.</span></span>


```C++
MCIWNDM_GET_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="3c212-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c212-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c212-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="3c212-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="3c212-110">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) per contenere le coordinate del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="3c212-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to contain the coordinates of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c212-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c212-111">Return Value</span></span>

<span data-ttu-id="3c212-112">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="3c212-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c212-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c212-113">Requirements</span></span>



| <span data-ttu-id="3c212-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c212-114">Requirement</span></span> | <span data-ttu-id="3c212-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3c212-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3c212-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c212-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3c212-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c212-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3c212-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c212-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3c212-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c212-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3c212-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c212-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c212-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c212-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c212-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c212-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c212-123">**MCIWndGetSource**</span><span class="sxs-lookup"><span data-stu-id="3c212-123">**MCIWndGetSource**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
</dt> </dl>

 


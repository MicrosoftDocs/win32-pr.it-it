---
title: Messaggio di MCIWNDM_PUT_SOURCE (VFW. h)
description: Il \_ messaggio di origine MCIWNDM put \_ ridefinisce le coordinate del rettangolo di origine usato per ritagliare le immagini di un file AVI durante la riproduzione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndPutSource.
ms.assetid: cff95139-0302-4db3-bf2e-559e75257e85
keywords:
- MCIWNDM_PUT_SOURCE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5407f420b8def6dda9795e87eb68943c9373b143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739815"
---
# <a name="mciwndm_put_source-message"></a><span data-ttu-id="c3c23-105">\_Messaggio di \_ origine put MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="c3c23-105">MCIWNDM\_PUT\_SOURCE message</span></span>

<span data-ttu-id="c3c23-106">Il messaggio di **\_ \_ origine MCIWNDM put** ridefinisce le coordinate del rettangolo di origine usato per ritagliare le immagini di un file AVI durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c3c23-106">The **MCIWNDM\_PUT\_SOURCE** message redefines the coordinates of the source rectangle used for cropping the images of an AVI file during playback.</span></span> <span data-ttu-id="c3c23-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) .</span><span class="sxs-lookup"><span data-stu-id="c3c23-107">You can send this message explicitly or by using the [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) macro.</span></span>


```C++
MCIWNDM_PUT_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="c3c23-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3c23-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3c23-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="c3c23-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="c3c23-110">Puntatore a una struttura [Rect](/previous-versions//ms536136(v=vs.85)) contenente le coordinate del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="c3c23-110">Pointer to a [RECT](/previous-versions//ms536136(v=vs.85)) structure containing the coordinates of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3c23-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3c23-111">Return Value</span></span>

<span data-ttu-id="c3c23-112">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="c3c23-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3c23-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3c23-113">Requirements</span></span>



| <span data-ttu-id="c3c23-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3c23-114">Requirement</span></span> | <span data-ttu-id="c3c23-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c3c23-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c3c23-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3c23-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c3c23-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c3c23-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c3c23-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3c23-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c3c23-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c3c23-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c3c23-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c3c23-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3c23-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3c23-121"><dt>Vfw.h</dt></span></span> </dl> |



 


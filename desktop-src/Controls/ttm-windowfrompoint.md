---
title: Messaggio TTM_WINDOWFROMPOINT (COMmctrl. h)
description: Consente a una routine di sottoclasse di fare in modo che una descrizione comando visualizzi un testo per una finestra diversa da quella sotto il cursore del mouse.
ms.assetid: f3bf6917-1745-4e4f-a9c1-8fe86b2b3906
keywords:
- Controlli di Windows Message TTM_WINDOWFROMPOINT
topic_type:
- apiref
api_name:
- TTM_WINDOWFROMPOINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68679f6b6c2477a8279c22f11d0d300e44c8370d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742258"
---
# <a name="ttm_windowfrompoint-message"></a><span data-ttu-id="f0555-104">\_Messaggio TTM WINDOWFROMPOINT</span><span class="sxs-lookup"><span data-stu-id="f0555-104">TTM\_WINDOWFROMPOINT message</span></span>

<span data-ttu-id="f0555-105">Consente a una routine di sottoclasse di fare in modo che una descrizione comando visualizzi un testo per una finestra diversa da quella sotto il cursore del mouse.</span><span class="sxs-lookup"><span data-stu-id="f0555-105">Allows a subclass procedure to cause a tooltip to display text for a window other than the one beneath the mouse cursor.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0555-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0555-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0555-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0555-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f0555-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f0555-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f0555-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0555-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0555-110">Puntatore a una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) che definisce il punto da controllare.</span><span class="sxs-lookup"><span data-stu-id="f0555-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that defines the point to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0555-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0555-111">Return value</span></span>

<span data-ttu-id="f0555-112">Il valore restituito è l'handle della finestra che contiene il punto oppure **null** se nessuna finestra è presente nel punto specificato.</span><span class="sxs-lookup"><span data-stu-id="f0555-112">The return value is the handle to the window that contains the point, or **NULL** if no window exists at the specified point.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0555-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0555-113">Remarks</span></span>

<span data-ttu-id="f0555-114">Questo messaggio deve essere elaborato da un'applicazione che sottoclassa una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="f0555-114">This message is intended to be processed by an application that subclasses a tooltip.</span></span> <span data-ttu-id="f0555-115">Non è destinato a essere inviato da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0555-115">It is not intended to be sent by an application.</span></span> <span data-ttu-id="f0555-116">Una descrizione comando Invia questo messaggio a se stesso prima di visualizzare il testo di una finestra.</span><span class="sxs-lookup"><span data-stu-id="f0555-116">A tooltip sends this message to itself before displaying the text for a window.</span></span> <span data-ttu-id="f0555-117">Modificando le coordinate del punto specificato da *lParam*, la procedura della sottoclasse può causare la visualizzazione del testo di una finestra diversa da quella sotto il cursore del mouse da parte della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="f0555-117">By changing the coordinates of the point specified by *lParam*, the subclass procedure can cause the tooltip to display text for a window other than the one beneath the mouse cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0555-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0555-118">Requirements</span></span>



| <span data-ttu-id="f0555-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0555-119">Requirement</span></span> | <span data-ttu-id="f0555-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f0555-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0555-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0555-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f0555-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f0555-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0555-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0555-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f0555-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f0555-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0555-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0555-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0555-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0555-126"><dt>Commctrl.h</dt></span></span> </dl> |



 


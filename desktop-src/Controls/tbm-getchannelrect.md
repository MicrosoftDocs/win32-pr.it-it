---
title: Messaggio TBM_GETCHANNELRECT (COMmctrl. h)
description: Recupera le dimensioni e la posizione del rettangolo di delimitazione per il canale di un TrackBar.
ms.assetid: 353edae3-1a26-4e85-8a32-ba8b5a976d24
keywords:
- Controlli di Windows Message TBM_GETCHANNELRECT
topic_type:
- apiref
api_name:
- TBM_GETCHANNELRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02982e9ce417b9fcf3e16d0e14d061e3ffd97a8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963934"
---
# <a name="tbm_getchannelrect-message"></a><span data-ttu-id="5c31f-104">\_Messaggio GETCHANNELRECT TBM</span><span class="sxs-lookup"><span data-stu-id="5c31f-104">TBM\_GETCHANNELRECT message</span></span>

<span data-ttu-id="5c31f-105">Recupera le dimensioni e la posizione del rettangolo di delimitazione per il canale di un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="5c31f-105">Retrieves the size and position of the bounding rectangle for a trackbar's channel.</span></span> <span data-ttu-id="5c31f-106">(Il canale è l'area in cui viene spostato il dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="5c31f-106">(The channel is the area over which the slider moves.</span></span> <span data-ttu-id="5c31f-107">Contiene l'evidenziazione quando viene selezionato un intervallo.</span><span class="sxs-lookup"><span data-stu-id="5c31f-107">It contains the highlight when a range is selected.)</span></span>

## <a name="parameters"></a><span data-ttu-id="5c31f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c31f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c31f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c31f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5c31f-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5c31f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5c31f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c31f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c31f-112">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5c31f-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="5c31f-113">Il messaggio compila questa struttura con il rettangolo di delimitazione del canale, in coordinate client della finestra del TrackBar.</span><span class="sxs-lookup"><span data-stu-id="5c31f-113">The message fills this structure with the channel's bounding rectangle, in client coordinates of the trackbar's window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c31f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c31f-114">Return value</span></span>

<span data-ttu-id="5c31f-115">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="5c31f-115">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c31f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c31f-116">Requirements</span></span>



| <span data-ttu-id="5c31f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c31f-117">Requirement</span></span> | <span data-ttu-id="5c31f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5c31f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c31f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c31f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5c31f-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c31f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5c31f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c31f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5c31f-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5c31f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5c31f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c31f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c31f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c31f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 


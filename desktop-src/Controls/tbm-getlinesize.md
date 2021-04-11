---
title: Messaggio TBM_GETLINESIZE (COMmctrl. h)
description: Recupera il numero di posizioni logiche spostate dal dispositivo di scorrimento del TrackBar in risposta all'input da tastiera dei tasti di direzione, ad esempio i tasti o. Le posizioni logiche sono gli incrementi interi nell'intervallo compreso tra minimo e massimo per le posizioni del dispositivo di scorrimento.
ms.assetid: b596060a-5bac-4b31-82f3-ee4744a9779c
keywords:
- Controlli di Windows Message TBM_GETLINESIZE
topic_type:
- apiref
api_name:
- TBM_GETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86eb103f34461e545f5a9f56148c48364d880dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964996"
---
# <a name="tbm_getlinesize-message"></a><span data-ttu-id="35b56-105">\_Messaggio GETLINESIZE TBM</span><span class="sxs-lookup"><span data-stu-id="35b56-105">TBM\_GETLINESIZE message</span></span>

<span data-ttu-id="35b56-106">Recupera il numero di posizioni logiche spostate dal dispositivo di scorrimento del TrackBar in risposta all'input da tastiera dei tasti di direzione, ad esempio i tasti o.</span><span class="sxs-lookup"><span data-stu-id="35b56-106">Retrieves the number of logical positions the trackbar's slider moves in response to keyboard input from the arrow keys, such as the or keys.</span></span> <span data-ttu-id="35b56-107">Le posizioni logiche sono gli incrementi interi nell'intervallo compreso tra minimo e massimo per le posizioni del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="35b56-107">The logical positions are the integer increments in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="35b56-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="35b56-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35b56-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35b56-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="35b56-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="35b56-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="35b56-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35b56-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="35b56-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="35b56-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35b56-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35b56-113">Return value</span></span>

<span data-ttu-id="35b56-114">Restituisce un valore a 32 bit che specifica le dimensioni della riga per il TrackBar.</span><span class="sxs-lookup"><span data-stu-id="35b56-114">Returns a 32-bit value that specifies the line size for the trackbar.</span></span>

## <a name="remarks"></a><span data-ttu-id="35b56-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="35b56-115">Remarks</span></span>

<span data-ttu-id="35b56-116">L'impostazione predefinita per le dimensioni della riga è 1.</span><span class="sxs-lookup"><span data-stu-id="35b56-116">The default setting for the line size is 1.</span></span>

<span data-ttu-id="35b56-117">TrackBar invia anche un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con i \_ \_ codici di notifica TB e TB LINEDOWN alla finestra padre quando l'utente preme i tasti di direzione.</span><span class="sxs-lookup"><span data-stu-id="35b56-117">The trackbar also sends a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the TB\_LINEUP and TB\_LINEDOWN notification codes to its parent window when the user presses the arrow keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="35b56-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35b56-118">Requirements</span></span>



| <span data-ttu-id="35b56-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="35b56-119">Requirement</span></span> | <span data-ttu-id="35b56-120">Valore</span><span class="sxs-lookup"><span data-stu-id="35b56-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35b56-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35b56-121">Minimum supported client</span></span><br/> | <span data-ttu-id="35b56-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35b56-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="35b56-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35b56-123">Minimum supported server</span></span><br/> | <span data-ttu-id="35b56-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="35b56-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="35b56-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35b56-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="35b56-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="35b56-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Messaggio TBM_GETTHUMBRECT (COMmctrl. h)
description: Recupera le dimensioni e la posizione del rettangolo di delimitazione per il dispositivo di scorrimento in un TrackBar.
ms.assetid: f53fd7af-36f8-4490-aa95-f1fa20f34efb
keywords:
- Controlli di Windows Message TBM_GETTHUMBRECT
topic_type:
- apiref
api_name:
- TBM_GETTHUMBRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce1bba8af9a65f297aa0515c1103c50daa1626d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048387"
---
# <a name="tbm_getthumbrect-message"></a><span data-ttu-id="33e62-104">\_Messaggio GETTHUMBRECT TBM</span><span class="sxs-lookup"><span data-stu-id="33e62-104">TBM\_GETTHUMBRECT message</span></span>

<span data-ttu-id="33e62-105">Recupera le dimensioni e la posizione del rettangolo di delimitazione per il dispositivo di scorrimento in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="33e62-105">Retrieves the size and position of the bounding rectangle for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="33e62-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="33e62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33e62-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33e62-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="33e62-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="33e62-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="33e62-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33e62-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33e62-110">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="33e62-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="33e62-111">Il messaggio compila questa struttura con il rettangolo delimitatore del dispositivo di scorrimento del TrackBar nelle coordinate client della finestra del TrackBar.</span><span class="sxs-lookup"><span data-stu-id="33e62-111">The message fills this structure with the bounding rectangle of the trackbar's slider in client coordinates of the trackbar's window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33e62-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33e62-112">Return value</span></span>

<span data-ttu-id="33e62-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="33e62-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="33e62-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33e62-114">Requirements</span></span>



| <span data-ttu-id="33e62-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="33e62-115">Requirement</span></span> | <span data-ttu-id="33e62-116">Valore</span><span class="sxs-lookup"><span data-stu-id="33e62-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33e62-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33e62-117">Minimum supported client</span></span><br/> | <span data-ttu-id="33e62-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33e62-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="33e62-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33e62-119">Minimum supported server</span></span><br/> | <span data-ttu-id="33e62-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="33e62-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33e62-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33e62-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="33e62-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="33e62-122"><dt>Commctrl.h</dt></span></span> </dl> |



 


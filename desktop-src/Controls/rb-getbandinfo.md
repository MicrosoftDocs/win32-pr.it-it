---
title: Messaggio RB_GETBANDINFO (COMmctrl. h)
description: Recupera le informazioni su una banda specificata in un controllo Rebar.
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- Controlli di Windows Message RB_GETBANDINFO
topic_type:
- apiref
api_name:
- RB_GETBANDINFO
- RB_GETBANDINFOA
- RB_GETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87715cf61b4eb2726eab83d500330721f41719f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120511"
---
# <a name="rb_getbandinfo-message"></a><span data-ttu-id="19a87-104">\_Messaggio GETBANDINFO RB</span><span class="sxs-lookup"><span data-stu-id="19a87-104">RB\_GETBANDINFO message</span></span>

<span data-ttu-id="19a87-105">Recupera le informazioni su una banda specificata in un controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="19a87-105">Retrieves information about a specified band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="19a87-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="19a87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19a87-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19a87-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19a87-108">Indice in base zero della banda per cui verranno recuperate le informazioni.</span><span class="sxs-lookup"><span data-stu-id="19a87-108">Zero-based index of the band for which the information will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="19a87-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19a87-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19a87-110">Puntatore a una struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) che riceverà le informazioni sulla banda richiesta.</span><span class="sxs-lookup"><span data-stu-id="19a87-110">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that will receive the requested band information.</span></span> <span data-ttu-id="19a87-111">Prima di inviare questo messaggio, è necessario impostare il membro **cbSize** della struttura sulla dimensione della struttura **REBARBANDINFO** e impostare il membro **fmask** sugli elementi che si desidera recuperare.</span><span class="sxs-lookup"><span data-stu-id="19a87-111">Before sending this message, you must set the **cbSize** member of this structure to the size of the **REBARBANDINFO** structure and set the **fMask** member to the items you want to retrieve.</span></span> <span data-ttu-id="19a87-112">Inoltre, è necessario impostare il **membro** REBARBANDINFO della struttura  sulla dimensione del buffer **lpText** quando \_ viene specificato il testo RBBIM.</span><span class="sxs-lookup"><span data-stu-id="19a87-112">Additionally, you must set the **cch** member of the **REBARBANDINFO** structure to the size of the **lpText** buffer when RBBIM\_TEXT is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19a87-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19a87-113">Return value</span></span>

<span data-ttu-id="19a87-114">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="19a87-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="19a87-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19a87-115">Requirements</span></span>



| <span data-ttu-id="19a87-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="19a87-116">Requirement</span></span> | <span data-ttu-id="19a87-117">Valore</span><span class="sxs-lookup"><span data-stu-id="19a87-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19a87-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19a87-118">Minimum supported client</span></span><br/> | <span data-ttu-id="19a87-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19a87-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19a87-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19a87-120">Minimum supported server</span></span><br/> | <span data-ttu-id="19a87-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="19a87-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19a87-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19a87-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="19a87-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="19a87-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="19a87-124">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="19a87-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="19a87-125">**RB \_ GETBANDINFOW** (Unicode) e **RB \_ GETBANDINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="19a87-125">**RB\_GETBANDINFOW** (Unicode) and **RB\_GETBANDINFOA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="19a87-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19a87-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19a87-127">**RB \_ SETBANDINFO**</span><span class="sxs-lookup"><span data-stu-id="19a87-127">**RB\_SETBANDINFO**</span></span>](rb-setbandinfo.md)
</dt> </dl>

 

 






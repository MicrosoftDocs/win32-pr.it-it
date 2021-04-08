---
title: Messaggio SB_SETICON (COMmctrl. h)
description: Imposta l'icona di una parte in una barra di stato.
ms.assetid: d8528cd1-54d2-44ba-b0d6-29111f75616a
keywords:
- Controlli di Windows Message SB_SETICON
topic_type:
- apiref
api_name:
- SB_SETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f720c414238eb89cf98bf0556ebabffefceae4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874225"
---
# <a name="sb_seticon-message"></a><span data-ttu-id="405e5-104">\_Messaggio dell'icona SB</span><span class="sxs-lookup"><span data-stu-id="405e5-104">SB\_SETICON message</span></span>

<span data-ttu-id="405e5-105">Imposta l'icona di una parte in una barra di stato.</span><span class="sxs-lookup"><span data-stu-id="405e5-105">Sets the icon for a part in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="405e5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="405e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="405e5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="405e5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="405e5-108">Indice in base zero della parte che riceverà l'icona.</span><span class="sxs-lookup"><span data-stu-id="405e5-108">Zero-based index of the part that will receive the icon.</span></span> <span data-ttu-id="405e5-109">Se questo parametro è-1, si presuppone che la barra di stato sia una barra di stato semplice.</span><span class="sxs-lookup"><span data-stu-id="405e5-109">If this parameter is -1, the status bar is assumed to be a simple status bar.</span></span>

</dd> <dt>

<span data-ttu-id="405e5-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="405e5-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="405e5-111">Handle per l'icona da impostare.</span><span class="sxs-lookup"><span data-stu-id="405e5-111">Handle to the icon to be set.</span></span> <span data-ttu-id="405e5-112">Se questo valore è **null**, l'icona viene rimossa dalla parte.</span><span class="sxs-lookup"><span data-stu-id="405e5-112">If this value is **NULL**, the icon is removed from the part.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="405e5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="405e5-113">Return value</span></span>

<span data-ttu-id="405e5-114">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="405e5-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="405e5-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="405e5-115">Remarks</span></span>

<span data-ttu-id="405e5-116">La barra di stato non eliminerà l'icona.</span><span class="sxs-lookup"><span data-stu-id="405e5-116">The status bar will not destroy the icon.</span></span> <span data-ttu-id="405e5-117">È responsabilità dell'applicazione chiamante tenere traccia ed eliminare eventuali icone.</span><span class="sxs-lookup"><span data-stu-id="405e5-117">It is the calling application's responsibility to keep track of and destroy any icons.</span></span>

## <a name="requirements"></a><span data-ttu-id="405e5-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="405e5-118">Requirements</span></span>



| <span data-ttu-id="405e5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="405e5-119">Requirement</span></span> | <span data-ttu-id="405e5-120">Valore</span><span class="sxs-lookup"><span data-stu-id="405e5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="405e5-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="405e5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="405e5-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="405e5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="405e5-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="405e5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="405e5-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="405e5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="405e5-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="405e5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="405e5-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="405e5-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






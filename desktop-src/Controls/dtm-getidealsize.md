---
title: Messaggio DTM_GETIDEALSIZE (COMmctrl. h)
description: Ottiene le dimensioni necessarie per visualizzare il controllo senza ritagliare. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro DateTime GetIdealSize.
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- Controlli di Windows Message DTM_GETIDEALSIZE
topic_type:
- apiref
api_name:
- DTM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a979883f431fea4627f52fe19c3716341e3f2328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225202"
---
# <a name="dtm_getidealsize-message"></a><span data-ttu-id="852d2-105">\_Messaggio GETIDEALSIZE DTM</span><span class="sxs-lookup"><span data-stu-id="852d2-105">DTM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="852d2-106">Ottiene le dimensioni necessarie per visualizzare il controllo senza ritagliare.</span><span class="sxs-lookup"><span data-stu-id="852d2-106">Gets the size needed to display the control without clipping.</span></span> <span data-ttu-id="852d2-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) .</span><span class="sxs-lookup"><span data-stu-id="852d2-107">Send this message explicitly or by using the [**DateTime\_GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="852d2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="852d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="852d2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="852d2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="852d2-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="852d2-110">Not used.</span></span> <span data-ttu-id="852d2-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="852d2-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="852d2-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="852d2-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="852d2-113">Puntatore a una struttura di [**dimensioni**](/previous-versions//dd145106(v=vs.85)) per la ricezione delle dimensioni ideali.</span><span class="sxs-lookup"><span data-stu-id="852d2-113">A pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure to receive the ideal size.</span></span> <span data-ttu-id="852d2-114">L'applicazione chiamante è responsabile dell'allocazione di questa struttura.</span><span class="sxs-lookup"><span data-stu-id="852d2-114">The calling application is responsible for allocating this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="852d2-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="852d2-115">Return value</span></span>

<span data-ttu-id="852d2-116">Restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="852d2-116">Returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="852d2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="852d2-117">Requirements</span></span>



| <span data-ttu-id="852d2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="852d2-118">Requirement</span></span> | <span data-ttu-id="852d2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="852d2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="852d2-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="852d2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="852d2-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="852d2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="852d2-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="852d2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="852d2-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="852d2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="852d2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="852d2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="852d2-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="852d2-125"><dt>Commctrl.h</dt></span></span> </dl> |



 


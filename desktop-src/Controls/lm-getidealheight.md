---
title: Messaggio LM_GETIDEALHEIGHT (COMmctrl. h)
description: Recupera l'altezza preferita di un collegamento per la larghezza corrente del controllo.
ms.assetid: bf6ef3c1-89bc-4c56-9384-085fd00234e1
keywords:
- Controlli di Windows Message LM_GETIDEALHEIGHT
topic_type:
- apiref
api_name:
- LM_GETIDEALHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a92f24d63cc8f58e260d79dafd0555429d65d20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873330"
---
# <a name="lm_getidealheight-message"></a><span data-ttu-id="b8f08-104">\_Messaggio GETIDEALHEIGHT LM</span><span class="sxs-lookup"><span data-stu-id="b8f08-104">LM\_GETIDEALHEIGHT message</span></span>

<span data-ttu-id="b8f08-105">Recupera l'altezza preferita di un collegamento per la larghezza corrente del controllo.</span><span class="sxs-lookup"><span data-stu-id="b8f08-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8f08-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8f08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8f08-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8f08-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b8f08-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b8f08-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b8f08-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8f08-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b8f08-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b8f08-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8f08-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8f08-111">Return value</span></span>

<span data-ttu-id="b8f08-112">Integer che rappresenta l'altezza preferita del testo del collegamento, in pixel.</span><span class="sxs-lookup"><span data-stu-id="b8f08-112">Integer representing the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8f08-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8f08-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b8f08-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="b8f08-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="b8f08-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b8f08-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b8f08-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8f08-116">Requirements</span></span>



| <span data-ttu-id="b8f08-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8f08-117">Requirement</span></span> | <span data-ttu-id="b8f08-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b8f08-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8f08-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8f08-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b8f08-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8f08-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8f08-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8f08-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b8f08-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b8f08-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8f08-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8f08-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8f08-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8f08-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






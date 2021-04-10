---
title: Messaggio TTM_GETBUBBLESIZE (COMmctrl. h)
description: Restituisce la larghezza e l'altezza di un controllo ToolTip.
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- Controlli di Windows Message TTM_GETBUBBLESIZE
topic_type:
- apiref
api_name:
- TTM_GETBUBBLESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48b48bda0f795473cb48303e88bbf3c1c35df7cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119818"
---
# <a name="ttm_getbubblesize-message"></a><span data-ttu-id="e7ea0-104">\_Messaggio TTM GETBUBBLESIZE</span><span class="sxs-lookup"><span data-stu-id="e7ea0-104">TTM\_GETBUBBLESIZE message</span></span>

<span data-ttu-id="e7ea0-105">Restituisce la larghezza e l'altezza di un controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="e7ea0-105">Returns the width and height of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7ea0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7ea0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7ea0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7ea0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e7ea0-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e7ea0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e7ea0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7ea0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7ea0-110">Puntatore alla struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="e7ea0-110">Pointer to the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7ea0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7ea0-111">Return value</span></span>

<span data-ttu-id="e7ea0-112">Restituisce la larghezza della descrizione comando nella parola bassa e l'altezza della parola alta se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e7ea0-112">Returns the width of the tooltip in the low word and the height in the high word if successful.</span></span> <span data-ttu-id="e7ea0-113">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="e7ea0-113">Otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7ea0-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7ea0-114">Remarks</span></span>

<span data-ttu-id="e7ea0-115">Se i \_ flag di traccia ttf e i \_ flag assoluti ttf sono impostati nel membro **uFlags** della struttura ToolTip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , questo messaggio può essere usato per facilitare la posizione esatta della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="e7ea0-115">If the TTF\_TRACK and TTF\_ABSOLUTE flags are set in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure, this message can be used to help position the tooltip accurately.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7ea0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7ea0-116">Requirements</span></span>



| <span data-ttu-id="e7ea0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7ea0-117">Requirement</span></span> | <span data-ttu-id="e7ea0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e7ea0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ea0-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7ea0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e7ea0-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7ea0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7ea0-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7ea0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e7ea0-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e7ea0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7ea0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7ea0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7ea0-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7ea0-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






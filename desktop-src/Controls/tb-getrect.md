---
title: Messaggio TB_GETRECT (COMmctrl. h)
description: Recupera il rettangolo di delimitazione per un pulsante della barra degli strumenti specificato.
ms.assetid: a93885eb-7eb7-4434-ad51-80fb30d3bfa1
keywords:
- Controlli di Windows Message TB_GETRECT
topic_type:
- apiref
api_name:
- TB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 889d067eb282e3d834ba4dc0cf6711c0561d86e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874598"
---
# <a name="tb_getrect-message"></a><span data-ttu-id="6b88d-104">TB- \_ messaggio GETrect</span><span class="sxs-lookup"><span data-stu-id="6b88d-104">TB\_GETRECT message</span></span>

<span data-ttu-id="6b88d-105">Recupera il rettangolo di delimitazione per un pulsante della barra degli strumenti specificato.</span><span class="sxs-lookup"><span data-stu-id="6b88d-105">Retrieves the bounding rectangle for a specified toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b88d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b88d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b88d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b88d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b88d-108">Identificatore del comando del pulsante.</span><span class="sxs-lookup"><span data-stu-id="6b88d-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="6b88d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b88d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b88d-110">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceverà le informazioni sul rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="6b88d-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the bounding rectangle information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b88d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b88d-111">Return value</span></span>

<span data-ttu-id="6b88d-112">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6b88d-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b88d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b88d-113">Remarks</span></span>

<span data-ttu-id="6b88d-114">Questo messaggio non recupera il rettangolo di delimitazione per i pulsanti il cui stato è impostato sul valore [**\_ nascosto TBSTATE**](toolbar-button-states.md) .</span><span class="sxs-lookup"><span data-stu-id="6b88d-114">This message does not retrieve the bounding rectangle for buttons whose state is set to the [**TBSTATE\_HIDDEN**](toolbar-button-states.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b88d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b88d-115">Requirements</span></span>



| <span data-ttu-id="6b88d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b88d-116">Requirement</span></span> | <span data-ttu-id="6b88d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="6b88d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b88d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b88d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6b88d-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6b88d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b88d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b88d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6b88d-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b88d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b88d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b88d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b88d-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b88d-123"><dt>Commctrl.h</dt></span></span> </dl> |



 


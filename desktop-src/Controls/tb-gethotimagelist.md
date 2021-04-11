---
title: Messaggio TB_GETHOTIMAGELIST (COMmctrl. h)
description: Recupera l'elenco di immagini utilizzato da un controllo Toolbar per visualizzare i pulsanti di scelta rapida.
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- Controlli di Windows Message TB_GETHOTIMAGELIST
topic_type:
- apiref
api_name:
- TB_GETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e19c1f3989b0d749a9c663d00b5fb7b54d67fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120003"
---
# <a name="tb_gethotimagelist-message"></a><span data-ttu-id="c398f-104">TB \_ GETHOTIMAGELIST messaggio</span><span class="sxs-lookup"><span data-stu-id="c398f-104">TB\_GETHOTIMAGELIST message</span></span>

<span data-ttu-id="c398f-105">Recupera l'elenco di immagini utilizzato da un controllo Toolbar per visualizzare i pulsanti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="c398f-105">Retrieves the image list that a toolbar control uses to display hot buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="c398f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c398f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c398f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c398f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c398f-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c398f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c398f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c398f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c398f-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c398f-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c398f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c398f-111">Return value</span></span>

<span data-ttu-id="c398f-112">Restituisce l'handle all'elenco di immagini che il controllo utilizza per visualizzare i pulsanti sensibili o **null** se non è impostato alcun elenco di immagini attive.</span><span class="sxs-lookup"><span data-stu-id="c398f-112">Returns the handle to the image list that the control uses to display hot buttons, or **NULL** if no hot image list is set.</span></span>

## <a name="remarks"></a><span data-ttu-id="c398f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c398f-113">Remarks</span></span>

<span data-ttu-id="c398f-114">Un pulsante è attivo quando il cursore è posizionato su di esso.</span><span class="sxs-lookup"><span data-stu-id="c398f-114">A button is hot when the cursor is over it.</span></span> <span data-ttu-id="c398f-115">Per gli elementi attivi, i controlli della barra degli strumenti devono avere lo stile di [**\_ elenco**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) o TBSTYLE.</span><span class="sxs-lookup"><span data-stu-id="c398f-115">Toolbar controls must have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) or [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style to have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="c398f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c398f-116">Requirements</span></span>



| <span data-ttu-id="c398f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c398f-117">Requirement</span></span> | <span data-ttu-id="c398f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c398f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c398f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c398f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c398f-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c398f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c398f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c398f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c398f-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c398f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c398f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c398f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c398f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c398f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






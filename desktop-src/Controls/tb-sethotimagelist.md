---
title: Messaggio TB_SETHOTIMAGELIST (COMmctrl. h)
description: Imposta l'elenco di immagini che il controllo toolbar utilizzerà per visualizzare i pulsanti di scelta rapida.
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- Controlli di Windows Message TB_SETHOTIMAGELIST
topic_type:
- apiref
api_name:
- TB_SETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a84c3420eaf64710ac1f8764db20d2cfc88b7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964628"
---
# <a name="tb_sethotimagelist-message"></a><span data-ttu-id="1e921-104">TB \_ SETHOTIMAGELIST messaggio</span><span class="sxs-lookup"><span data-stu-id="1e921-104">TB\_SETHOTIMAGELIST message</span></span>

<span data-ttu-id="1e921-105">Imposta l'elenco di immagini che il controllo toolbar utilizzerà per visualizzare i pulsanti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="1e921-105">Sets the image list that the toolbar control will use to display hot buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e921-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e921-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e921-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e921-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1e921-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1e921-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1e921-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e921-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e921-110">Handle per l'elenco di immagini che verrà impostato.</span><span class="sxs-lookup"><span data-stu-id="1e921-110">Handle to the image list that will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e921-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e921-111">Return value</span></span>

<span data-ttu-id="1e921-112">Restituisce l'handle per l'elenco di immagini precedentemente utilizzato per visualizzare i pulsanti di scelta rapida oppure **null** se non è stato impostato in precedenza alcun elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="1e921-112">Returns the handle to the image list previously used to display hot buttons, or **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e921-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e921-113">Remarks</span></span>

<span data-ttu-id="1e921-114">Un pulsante è attivo quando il cursore è posizionato su di esso.</span><span class="sxs-lookup"><span data-stu-id="1e921-114">A button is hot when the cursor is over it.</span></span> <span data-ttu-id="1e921-115">Per gli elementi attivi, i controlli della barra degli strumenti devono avere lo stile di [**\_ elenco**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) o TBSTYLE.</span><span class="sxs-lookup"><span data-stu-id="1e921-115">Toolbar controls must have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) or [**TBSTYLE\_LIST**](toolbar-control-and-button-styles.md) style to have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e921-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e921-116">Requirements</span></span>



| <span data-ttu-id="1e921-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e921-117">Requirement</span></span> | <span data-ttu-id="1e921-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1e921-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e921-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e921-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1e921-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1e921-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e921-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e921-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1e921-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1e921-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e921-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e921-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e921-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e921-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Messaggio TB_SETDISABLEDIMAGELIST (COMmctrl. h)
description: Imposta l'elenco di immagini che il controllo toolbar utilizzerà per visualizzare i pulsanti disabilitati.
ms.assetid: 1e76b3cf-2d06-48c8-8298-ef6caf3d85c3
keywords:
- Controlli di Windows Message TB_SETDISABLEDIMAGELIST
topic_type:
- apiref
api_name:
- TB_SETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7cc8c9ec1fdc9658413da5991fa109e7bef27a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048597"
---
# <a name="tb_setdisabledimagelist-message"></a><span data-ttu-id="12566-104">TB \_ SETDISABLEDIMAGELIST messaggio</span><span class="sxs-lookup"><span data-stu-id="12566-104">TB\_SETDISABLEDIMAGELIST message</span></span>

<span data-ttu-id="12566-105">Imposta l'elenco di immagini che il controllo toolbar utilizzerà per visualizzare i pulsanti disabilitati.</span><span class="sxs-lookup"><span data-stu-id="12566-105">Sets the image list that the toolbar control will use to display disabled buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="12566-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="12566-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12566-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="12566-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="12566-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="12566-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="12566-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12566-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12566-110">Handle per l'elenco di immagini che verrà impostato.</span><span class="sxs-lookup"><span data-stu-id="12566-110">Handle to the image list that will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12566-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12566-111">Return value</span></span>

<span data-ttu-id="12566-112">Restituisce l'handle per l'elenco di immagini precedentemente utilizzato per visualizzare i pulsanti disabilitati oppure **null** se non è stato impostato in precedenza alcun elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="12566-112">Returns the handle to the image list previously used to display disabled buttons, or **NULL** if no image list was previously set.</span></span>

## <a name="requirements"></a><span data-ttu-id="12566-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12566-113">Requirements</span></span>



| <span data-ttu-id="12566-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="12566-114">Requirement</span></span> | <span data-ttu-id="12566-115">Valore</span><span class="sxs-lookup"><span data-stu-id="12566-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12566-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12566-116">Minimum supported client</span></span><br/> | <span data-ttu-id="12566-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12566-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="12566-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12566-118">Minimum supported server</span></span><br/> | <span data-ttu-id="12566-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="12566-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12566-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12566-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="12566-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="12566-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






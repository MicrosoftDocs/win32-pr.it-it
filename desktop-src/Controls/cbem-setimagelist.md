---
title: Messaggio CBEM_SETIMAGELIST (COMmctrl. h)
description: Imposta un elenco di immagini per un controllo ComboBoxEx.
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- Controlli di Windows Message CBEM_SETIMAGELIST
topic_type:
- apiref
api_name:
- CBEM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33816abe36e2d1e1593e6365061a500d072c155b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964861"
---
# <a name="cbem_setimagelist-message"></a><span data-ttu-id="9e6eb-104">CBEM \_ messaggio di immagine</span><span class="sxs-lookup"><span data-stu-id="9e6eb-104">CBEM\_SETIMAGELIST message</span></span>

<span data-ttu-id="9e6eb-105">Imposta un elenco di immagini per un controllo ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="9e6eb-105">Sets an image list for a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e6eb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e6eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e6eb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e6eb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9e6eb-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9e6eb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9e6eb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e6eb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e6eb-110">Handle per l'elenco di immagini da impostare per il controllo.</span><span class="sxs-lookup"><span data-stu-id="9e6eb-110">A handle to the image list to be set for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e6eb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e6eb-111">Return value</span></span>

<span data-ttu-id="9e6eb-112">Restituisce l'handle per l'elenco di immagini precedentemente associato al controllo oppure restituisce **null** se non è stato impostato in precedenza alcun elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="9e6eb-112">Returns the handle to the image list previously associated with the control, or returns **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e6eb-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e6eb-113">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e6eb-114">L'altezza delle immagini nell'elenco immagini potrebbe modificare i requisiti di dimensioni del controllo ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="9e6eb-114">The height of images in your image list might change the size requirements of the ComboBoxEx control.</span></span> <span data-ttu-id="9e6eb-115">È consigliabile ridimensionare il controllo dopo l'invio di questo messaggio per assicurarsi che venga visualizzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="9e6eb-115">It is recommended that you resize the control after sending this message to ensure that it is displayed properly.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9e6eb-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e6eb-116">Requirements</span></span>



| <span data-ttu-id="9e6eb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e6eb-117">Requirement</span></span> | <span data-ttu-id="9e6eb-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9e6eb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e6eb-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e6eb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9e6eb-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9e6eb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e6eb-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e6eb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9e6eb-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9e6eb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e6eb-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e6eb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e6eb-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e6eb-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






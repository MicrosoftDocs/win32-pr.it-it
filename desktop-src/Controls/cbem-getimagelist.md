---
title: Messaggio CBEM_GETIMAGELIST (COMmctrl. h)
description: Ottiene l'handle per un elenco di immagini assegnato a un controllo ComboBoxEx.
ms.assetid: d577f920-b8f7-4d51-9507-765b7f925408
keywords:
- Controlli di Windows Message CBEM_GETIMAGELIST
topic_type:
- apiref
api_name:
- CBEM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d143b8483fb5fb97ebd65fa2a98640089f6d548
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302300"
---
# <a name="cbem_getimagelist-message"></a><span data-ttu-id="43a53-104">CBEM \_ messaggio GETimagine</span><span class="sxs-lookup"><span data-stu-id="43a53-104">CBEM\_GETIMAGELIST message</span></span>

<span data-ttu-id="43a53-105">Ottiene l'handle per un elenco di immagini assegnato a un controllo ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="43a53-105">Gets the handle to an image list assigned to a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="43a53-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="43a53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a53-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43a53-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="43a53-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="43a53-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="43a53-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43a53-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="43a53-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="43a53-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43a53-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43a53-111">Return value</span></span>

<span data-ttu-id="43a53-112">Restituisce l'handle per l'elenco di immagini assegnato al controllo, in caso di esito positivo; in caso contrario, **null** .</span><span class="sxs-lookup"><span data-stu-id="43a53-112">Returns the handle to the image list assigned to the control if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a53-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43a53-113">Requirements</span></span>



| <span data-ttu-id="43a53-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="43a53-114">Requirement</span></span> | <span data-ttu-id="43a53-115">Valore</span><span class="sxs-lookup"><span data-stu-id="43a53-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43a53-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43a53-116">Minimum supported client</span></span><br/> | <span data-ttu-id="43a53-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43a53-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43a53-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43a53-118">Minimum supported server</span></span><br/> | <span data-ttu-id="43a53-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="43a53-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43a53-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43a53-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="43a53-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="43a53-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






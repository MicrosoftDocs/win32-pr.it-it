---
title: Messaggio TB_GETDISABLEDIMAGELIST (COMmctrl. h)
description: Recupera l'elenco di immagini utilizzato da un controllo Toolbar per visualizzare i pulsanti inattivi.
ms.assetid: 8f6782d5-488b-4906-908a-e4bf8d512e0a
keywords:
- Controlli di Windows Message TB_GETDISABLEDIMAGELIST
topic_type:
- apiref
api_name:
- TB_GETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fc847927ef14312c76e26303bec5de07b788266
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964112"
---
# <a name="tb_getdisabledimagelist-message"></a><span data-ttu-id="52911-104">TB \_ GETDISABLEDIMAGELIST messaggio</span><span class="sxs-lookup"><span data-stu-id="52911-104">TB\_GETDISABLEDIMAGELIST message</span></span>

<span data-ttu-id="52911-105">Recupera l'elenco di immagini utilizzato da un controllo Toolbar per visualizzare i pulsanti inattivi.</span><span class="sxs-lookup"><span data-stu-id="52911-105">Retrieves the image list that a toolbar control uses to display inactive buttons.</span></span>

## <a name="parameters"></a><span data-ttu-id="52911-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="52911-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52911-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52911-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="52911-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="52911-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="52911-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52911-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="52911-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="52911-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52911-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52911-111">Return value</span></span>

<span data-ttu-id="52911-112">Restituisce l'handle per l'elenco di immagini inattive oppure **null** se non è impostato alcun elenco di immagini inattivo.</span><span class="sxs-lookup"><span data-stu-id="52911-112">Returns the handle to the inactive image list, or **NULL** if no inactive image list is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="52911-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52911-113">Requirements</span></span>



| <span data-ttu-id="52911-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="52911-114">Requirement</span></span> | <span data-ttu-id="52911-115">Valore</span><span class="sxs-lookup"><span data-stu-id="52911-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52911-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52911-116">Minimum supported client</span></span><br/> | <span data-ttu-id="52911-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52911-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52911-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52911-118">Minimum supported server</span></span><br/> | <span data-ttu-id="52911-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="52911-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52911-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52911-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="52911-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="52911-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






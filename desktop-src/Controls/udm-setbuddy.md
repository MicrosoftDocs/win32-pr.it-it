---
title: Messaggio UDM_SETBUDDY (COMmctrl. h)
description: Imposta la finestra buddy per un controllo di scorrimento.
ms.assetid: 66e35acc-95f6-4bc5-b654-690abf2188ba
keywords:
- Controlli di Windows Message UDM_SETBUDDY
topic_type:
- apiref
api_name:
- UDM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e8bd57727d730c67fe09a52c0bedf121eac982
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120494"
---
# <a name="udm_setbuddy-message"></a><span data-ttu-id="3a5a5-104">\_Messaggio UDM SEbuddy</span><span class="sxs-lookup"><span data-stu-id="3a5a5-104">UDM\_SETBUDDY message</span></span>

<span data-ttu-id="3a5a5-105">Imposta la finestra buddy per un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="3a5a5-105">Sets the buddy window for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a5a5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a5a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a5a5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a5a5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a5a5-108">Handle per la nuova finestra buddy.</span><span class="sxs-lookup"><span data-stu-id="3a5a5-108">Handle to the new buddy window.</span></span>

</dd> <dt>

<span data-ttu-id="3a5a5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a5a5-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3a5a5-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3a5a5-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a5a5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a5a5-111">Return value</span></span>

<span data-ttu-id="3a5a5-112">Il valore restituito è l'handle per la finestra buddy precedente.</span><span class="sxs-lookup"><span data-stu-id="3a5a5-112">The return value is the handle to the previous buddy window.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a5a5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a5a5-113">Requirements</span></span>



| <span data-ttu-id="3a5a5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a5a5-114">Requirement</span></span> | <span data-ttu-id="3a5a5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3a5a5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a5a5-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a5a5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3a5a5-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a5a5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a5a5-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a5a5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3a5a5-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3a5a5-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a5a5-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a5a5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a5a5-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a5a5-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






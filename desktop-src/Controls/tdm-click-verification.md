---
title: Messaggio TDM_CLICK_VERIFICATION (COMmctrl. h)
description: Simula un clic della casella di controllo verifica di una finestra di dialogo attività, se esistente.
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- Controlli di Windows Message TDM_CLICK_VERIFICATION
topic_type:
- apiref
api_name:
- TDM_CLICK_VERIFICATION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df61676104169e3084e7cde09439c218f2237e60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118958"
---
# <a name="tdm_click_verification-message"></a><span data-ttu-id="9fc54-104">TDM- \_ Seleziona \_ messaggio di verifica</span><span class="sxs-lookup"><span data-stu-id="9fc54-104">TDM\_CLICK\_VERIFICATION message</span></span>

<span data-ttu-id="9fc54-105">Simula un clic della casella di controllo verifica di una finestra di dialogo attività, se esistente.</span><span class="sxs-lookup"><span data-stu-id="9fc54-105">Simulates a click of the verification checkbox of a task dialog, if it exists.</span></span>

## <a name="parameters"></a><span data-ttu-id="9fc54-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9fc54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fc54-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fc54-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc54-108">**True** per impostare lo stato della casella di controllo da controllare; **False** per impostarlo come deselezionato.</span><span class="sxs-lookup"><span data-stu-id="9fc54-108">**TRUE** to set the state of the checkbox to be checked; **FALSE** to set it to be unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="9fc54-109">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fc54-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc54-110">**True** per impostare lo stato attivo della tastiera sulla casella di controllo; In caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="9fc54-110">**TRUE** to set the keyboard focus to the checkbox; **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fc54-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9fc54-111">Return value</span></span>

<span data-ttu-id="9fc54-112">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="9fc54-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc54-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fc54-113">Requirements</span></span>



| <span data-ttu-id="9fc54-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fc54-114">Requirement</span></span> | <span data-ttu-id="9fc54-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9fc54-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc54-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fc54-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9fc54-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fc54-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9fc54-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fc54-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9fc54-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9fc54-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9fc54-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9fc54-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fc54-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fc54-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






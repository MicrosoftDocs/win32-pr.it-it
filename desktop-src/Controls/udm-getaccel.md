---
title: Messaggio UDM_GETACCEL (COMmctrl. h)
description: Recupera le informazioni di accelerazione per un controllo di scorrimento.
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- Controlli di Windows Message UDM_GETACCEL
topic_type:
- apiref
api_name:
- UDM_GETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86a9740e59631b737453763a10ccb9820056d95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475736"
---
# <a name="udm_getaccel-message"></a><span data-ttu-id="6327a-104">\_Messaggio UDM GETACCEL</span><span class="sxs-lookup"><span data-stu-id="6327a-104">UDM\_GETACCEL message</span></span>

<span data-ttu-id="6327a-105">Recupera le informazioni di accelerazione per un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="6327a-105">Retrieves acceleration information for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6327a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6327a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6327a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6327a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6327a-108">Numero di elementi nella matrice specificata da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="6327a-108">Number of elements in the array specified by *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="6327a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6327a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6327a-110">Puntatore a una matrice di strutture [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) che ricevono informazioni di accelerazione.</span><span class="sxs-lookup"><span data-stu-id="6327a-110">Pointer to an array of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures that receive acceleration information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6327a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6327a-111">Return value</span></span>

<span data-ttu-id="6327a-112">Il valore restituito è il numero di acceleratori attualmente impostati per il controllo.</span><span class="sxs-lookup"><span data-stu-id="6327a-112">The return value is the number of accelerators currently set for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="6327a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6327a-113">Requirements</span></span>



| <span data-ttu-id="6327a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6327a-114">Requirement</span></span> | <span data-ttu-id="6327a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6327a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6327a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6327a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6327a-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6327a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6327a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6327a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6327a-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6327a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6327a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6327a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6327a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6327a-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6327a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6327a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6327a-123">**\_SETACCEL UDM**</span><span class="sxs-lookup"><span data-stu-id="6327a-123">**UDM\_SETACCEL**</span></span>](udm-setaccel.md)
</dt> </dl>

 

 






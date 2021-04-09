---
title: Messaggio IPM_SETRANGE (COMmctrl. h)
description: Imposta l'intervallo valido per il campo specificato nel controllo degli indirizzi IP.
ms.assetid: 03068c5d-822f-459d-8f79-e7f0430a27bf
keywords:
- Controlli di Windows Message IPM_SETRANGE
topic_type:
- apiref
api_name:
- IPM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e70df7b2b8f76f514d9a0cc6101aba2ee7cf4ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048612"
---
# <a name="ipm_setrange-message"></a><span data-ttu-id="8dfb1-104">\_Messaggio SEtrange IPM</span><span class="sxs-lookup"><span data-stu-id="8dfb1-104">IPM\_SETRANGE message</span></span>

<span data-ttu-id="8dfb1-105">Imposta l'intervallo valido per il campo specificato nel controllo degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-105">Sets the valid range for the specified field in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8dfb1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8dfb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dfb1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8dfb1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8dfb1-108">Indice di campo in base zero a cui verrà applicato l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-108">A zero-based field index to which the range will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="8dfb1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8dfb1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8dfb1-110">Valore di **parola** che contiene il limite inferiore dell'intervallo nel byte di ordine inferiore e il limite superiore nel byte di ordine superiore.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-110">A **WORD** value that contains the lower limit of the range in the low-order byte and the upper limit in the high-order byte.</span></span> <span data-ttu-id="8dfb1-111">Entrambi questi valori sono inclusivi.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-111">Both of these values are inclusive.</span></span> <span data-ttu-id="8dfb1-112">La macro [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) può essere usata anche per creare l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-112">The [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) macro can also be used to create the range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dfb1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8dfb1-113">Return value</span></span>

<span data-ttu-id="8dfb1-114">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dfb1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="8dfb1-115">Remarks</span></span>

<span data-ttu-id="8dfb1-116">Se l'utente immette un valore nel campo esterno a questo intervallo, il controllo invierà la notifica [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) con il valore immesso.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-116">If the user enters a value in the field that is outside of this range, the control will send the [IPN\_FIELDCHANGED](ipn-fieldchanged.md) notification with the entered value.</span></span> <span data-ttu-id="8dfb1-117">Se il valore non è ancora compreso nell'intervallo dopo l'invio della notifica, il controllo tenterà di modificare il valore immesso nel limite di intervallo più vicino.</span><span class="sxs-lookup"><span data-stu-id="8dfb1-117">If the value is still outside of the range after sending the notification, the control will attempt to change the entered value to the closest range limit.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dfb1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8dfb1-118">Requirements</span></span>



| <span data-ttu-id="8dfb1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dfb1-119">Requirement</span></span> | <span data-ttu-id="8dfb1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8dfb1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8dfb1-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8dfb1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8dfb1-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8dfb1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8dfb1-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8dfb1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8dfb1-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8dfb1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8dfb1-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8dfb1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dfb1-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dfb1-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






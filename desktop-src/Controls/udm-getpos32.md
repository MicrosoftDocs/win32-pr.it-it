---
title: Messaggio UDM_GETPOS32 (COMmctrl. h)
description: Restituisce la posizione a 32 bit di un controllo di scorrimento.
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- Controlli di Windows Message UDM_GETPOS32
topic_type:
- apiref
api_name:
- UDM_GETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f316b6833c67cd01d4e01910399a8730691f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475725"
---
# <a name="udm_getpos32-message"></a><span data-ttu-id="8e43a-104">\_Messaggio UDM GETPOS32</span><span class="sxs-lookup"><span data-stu-id="8e43a-104">UDM\_GETPOS32 message</span></span>

<span data-ttu-id="8e43a-105">Restituisce la posizione a 32 bit di un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="8e43a-105">Returns the 32-bit position of an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8e43a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e43a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e43a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e43a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e43a-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8e43a-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8e43a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e43a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e43a-110">Puntatore a un valore **bool** impostato su zero se il valore viene recuperato correttamente o diverso da zero se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="8e43a-110">Pointer to a **BOOL** value that is set to zero if the value is successfully retrieved or nonzero if an error occurs.</span></span> <span data-ttu-id="8e43a-111">Se questo parametro è impostato su **null**, gli errori non vengono segnalati.</span><span class="sxs-lookup"><span data-stu-id="8e43a-111">If this parameter is set to **NULL**, errors are not reported.</span></span>

<span data-ttu-id="8e43a-112">Se si usa **UDM \_ GETPOS32** in una situazione tra processi, questo parametro deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="8e43a-112">If **UDM\_GETPOS32** is used in a cross-process situation, this parameter must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e43a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e43a-113">Return value</span></span>

<span data-ttu-id="8e43a-114">Restituisce la posizione di un controllo di scorrimento con precisione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8e43a-114">Returns the position of an up-down control with 32-bit precision.</span></span> <span data-ttu-id="8e43a-115">Le applicazioni devono controllare il valore *lParam* per determinare se il valore restituito è valido.</span><span class="sxs-lookup"><span data-stu-id="8e43a-115">Applications must check the *lParam* value to determine whether the return value is valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e43a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e43a-116">Remarks</span></span>

<span data-ttu-id="8e43a-117">Quando elabora questo messaggio, il controllo di scorrimento aggiorna la posizione corrente in base alla didascalia della finestra di Buddy.</span><span class="sxs-lookup"><span data-stu-id="8e43a-117">When it processes this message, the up-down control updates its current position based on the caption of the buddy window.</span></span> <span data-ttu-id="8e43a-118">Restituisce un errore se non è presente alcuna finestra di Buddy o se la didascalia specifica un valore non valido o non compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="8e43a-118">It returns an error if there is no buddy window or if the caption specifies an invalid or out-of-range value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e43a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e43a-119">Requirements</span></span>



| <span data-ttu-id="8e43a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e43a-120">Requirement</span></span> | <span data-ttu-id="8e43a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8e43a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e43a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e43a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8e43a-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e43a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e43a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e43a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8e43a-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8e43a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e43a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e43a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e43a-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e43a-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e43a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e43a-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="8e43a-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="8e43a-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8e43a-130">**\_GETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="8e43a-130">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> <dt>

[<span data-ttu-id="8e43a-131">**\_SETPOS UDM**</span><span class="sxs-lookup"><span data-stu-id="8e43a-131">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="8e43a-132">**\_SETPOS32 UDM**</span><span class="sxs-lookup"><span data-stu-id="8e43a-132">**UDM\_SETPOS32**</span></span>](udm-setpos32.md)
</dt> </dl>

 

 






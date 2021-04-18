---
title: Messaggio MCM_SETFIRSTDAYOFWEEK (COMmctrl. h)
description: Imposta il primo giorno della settimana per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal setFirstDayOfWeek.
ms.assetid: 6e0dc906-a41e-4c3a-9528-1f5428dceb8d
keywords:
- Controlli di Windows Message MCM_SETFIRSTDAYOFWEEK
topic_type:
- apiref
api_name:
- MCM_SETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32452c9043bbd7c3bbcf96f9dc32e67714eacce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302519"
---
# <a name="mcm_setfirstdayofweek-message"></a><span data-ttu-id="9fce5-105">\_Messaggio SETFIRSTDAYOFWEEK MCM</span><span class="sxs-lookup"><span data-stu-id="9fce5-105">MCM\_SETFIRSTDAYOFWEEK message</span></span>

<span data-ttu-id="9fce5-106">Imposta il primo giorno della settimana per un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="9fce5-106">Sets the first day of the week for a month calendar control.</span></span> <span data-ttu-id="9fce5-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ setFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) .</span><span class="sxs-lookup"><span data-stu-id="9fce5-107">You can send this message explicitly or by using the [**MonthCal\_SetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9fce5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9fce5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fce5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9fce5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9fce5-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9fce5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9fce5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9fce5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9fce5-112">Valore di tipo **int** che rappresenta il giorno da impostare come primo giorno della settimana, dove 0 è lunedì, 1 è martedì e così via.</span><span class="sxs-lookup"><span data-stu-id="9fce5-112">Value of type **int** representing which day is to be set as the first day of the week, where 0 is Monday, 1 is Tuesday, and so on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fce5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9fce5-113">Return value</span></span>

<span data-ttu-id="9fce5-114">Restituisce un valore **DWORD** che contiene due valori.</span><span class="sxs-lookup"><span data-stu-id="9fce5-114">Returns a **DWORD** value that contains two values.</span></span> <span data-ttu-id="9fce5-115">La parola alta è un valore **bool** che è diverso da zero se il primo giorno della settimana precedente non era uguale a IFIRSTDAYOFWEEK delle impostazioni locali \_ , altrimenti zero.</span><span class="sxs-lookup"><span data-stu-id="9fce5-115">The high word is a **BOOL** value that is nonzero if the previous first day of the week did not equal LOCALE\_IFIRSTDAYOFWEEK, or zero otherwise.</span></span> <span data-ttu-id="9fce5-116">La parola Low è un valore INT che rappresenta il primo giorno della settimana precedente.</span><span class="sxs-lookup"><span data-stu-id="9fce5-116">The low word is an INT value that represents the previous first day of the week.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fce5-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fce5-117">Remarks</span></span>

<span data-ttu-id="9fce5-118">Se il primo giorno della settimana è impostato su un valore diverso da quello predefinito (impostazioni locali \_ IFIRSTDAYOFWEEK), il controllo non aggiornerà automaticamente le modifiche del primo giorno della settimana in base alle modifiche delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="9fce5-118">If the first day of the week is set to anything other than the default (LOCALE\_IFIRSTDAYOFWEEK), the control will not automatically update first-day-of-the-week changes based on locale changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fce5-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fce5-119">Requirements</span></span>



| <span data-ttu-id="9fce5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fce5-120">Requirement</span></span> | <span data-ttu-id="9fce5-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9fce5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fce5-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fce5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9fce5-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fce5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9fce5-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fce5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9fce5-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9fce5-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9fce5-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9fce5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fce5-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fce5-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






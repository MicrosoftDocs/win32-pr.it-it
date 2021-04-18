---
title: Messaggio MCM_GETFIRSTDAYOFWEEK (COMmctrl. h)
description: Recupera il primo giorno della settimana per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetFirstDayOfWeek.
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- Controlli di Windows Message MCM_GETFIRSTDAYOFWEEK
topic_type:
- apiref
api_name:
- MCM_GETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b625e470e13c111b0274bfef422963e48c9cc7c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301940"
---
# <a name="mcm_getfirstdayofweek-message"></a><span data-ttu-id="eeea5-105">\_Messaggio GETFIRSTDAYOFWEEK MCM</span><span class="sxs-lookup"><span data-stu-id="eeea5-105">MCM\_GETFIRSTDAYOFWEEK message</span></span>

<span data-ttu-id="eeea5-106">Recupera il primo giorno della settimana per un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="eeea5-106">Retrieves the first day of the week for a month calendar control.</span></span> <span data-ttu-id="eeea5-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) .</span><span class="sxs-lookup"><span data-stu-id="eeea5-107">You can send this message explicitly or by using the [**MonthCal\_GetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="eeea5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="eeea5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeea5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eeea5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eeea5-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="eeea5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eeea5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eeea5-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="eeea5-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="eeea5-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeea5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eeea5-113">Return value</span></span>

<span data-ttu-id="eeea5-114">Restituisce un valore **DWORD** che contiene due valori.</span><span class="sxs-lookup"><span data-stu-id="eeea5-114">Returns a **DWORD** value that contains two values.</span></span> <span data-ttu-id="eeea5-115">La parola alta è un valore **bool** che è diverso da zero se il primo giorno della settimana è impostato su un valore diverso dalle impostazioni locali \_ IFIRSTDAYOFWEEK o zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="eeea5-115">The high word is a **BOOL** value that is nonzero if the first day of the week is set to something other than LOCALE\_IFIRSTDAYOFWEEK, or zero otherwise.</span></span> <span data-ttu-id="eeea5-116">La parola Low è un valore INT che rappresenta il primo giorno della settimana, dove 0 è lunedì, 1 è martedì e così via.</span><span class="sxs-lookup"><span data-stu-id="eeea5-116">The low word is an INT value that represents the first day of the week, where 0 is Monday, 1 is Tuesday, and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeea5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eeea5-117">Requirements</span></span>



| <span data-ttu-id="eeea5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeea5-118">Requirement</span></span> | <span data-ttu-id="eeea5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="eeea5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eeea5-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eeea5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="eeea5-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eeea5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eeea5-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eeea5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="eeea5-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eeea5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eeea5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eeea5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeea5-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeea5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






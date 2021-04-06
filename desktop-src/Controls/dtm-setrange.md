---
title: Messaggio DTM_SETRANGE (COMmctrl. h)
description: Imposta l'ora di sistema minima e massima consentita per un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime SetRange.
ms.assetid: ef0f48f2-906e-4ae0-839d-177e0fb7f14e
keywords:
- Controlli di Windows Message DTM_SETRANGE
topic_type:
- apiref
api_name:
- DTM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70578e7d468c6a0e54d1373af2d46e680afbbe5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742559"
---
# <a name="dtm_setrange-message"></a><span data-ttu-id="d023d-105">\_Messaggio SEtrange DTM</span><span class="sxs-lookup"><span data-stu-id="d023d-105">DTM\_SETRANGE message</span></span>

<span data-ttu-id="d023d-106">Imposta l'ora di sistema minima e massima consentita per un controllo di selezione data e ora (DTP).</span><span class="sxs-lookup"><span data-stu-id="d023d-106">Sets the minimum and maximum allowable system times for a date and time picker (DTP) control.</span></span> <span data-ttu-id="d023d-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) .</span><span class="sxs-lookup"><span data-stu-id="d023d-107">You can send this message explicitly or use the [**DateTime\_SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d023d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d023d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d023d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d023d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d023d-110">Valore che specifica quali valori di intervallo sono validi.</span><span class="sxs-lookup"><span data-stu-id="d023d-110">A value specifying which range values are valid.</span></span> <span data-ttu-id="d023d-111">Questo parametro può essere una combinazione dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="d023d-111">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="d023d-112">Valore</span><span class="sxs-lookup"><span data-stu-id="d023d-112">Value</span></span>                                                                                                                                          | <span data-ttu-id="d023d-113">Significato</span><span class="sxs-lookup"><span data-stu-id="d023d-113">Meaning</span></span>                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <span data-ttu-id="d023d-114"><dt>**GDTR \_ min**</dt></span><span class="sxs-lookup"><span data-stu-id="d023d-114"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="d023d-115">Il primo elemento nella matrice della struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) è valido e verrà utilizzato per impostare l'ora di sistema minima consentita.</span><span class="sxs-lookup"><span data-stu-id="d023d-115">The first element in the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure array is valid and will be used to set the minimum allowable system time.</span></span><br/>  |
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <span data-ttu-id="d023d-116"><dt>**GDTR \_ Max**</dt></span><span class="sxs-lookup"><span data-stu-id="d023d-116"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="d023d-117">Il secondo elemento della matrice della struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) è valido e verrà utilizzato per impostare l'ora di sistema massima consentita.</span><span class="sxs-lookup"><span data-stu-id="d023d-117">The second element in the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure array is valid and will be used to set the maximum allowable system time.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d023d-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d023d-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d023d-119">Puntatore a una matrice a due elementi di strutture [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="d023d-119">A pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures.</span></span> <span data-ttu-id="d023d-120">Il primo elemento della matrice **SYSTEMTIME** contiene il tempo minimo consentito.</span><span class="sxs-lookup"><span data-stu-id="d023d-120">The first element of the **SYSTEMTIME** array contains the minimum allowable time.</span></span> <span data-ttu-id="d023d-121">Il secondo elemento della matrice **SYSTEMTIME** contiene il tempo massimo consentito.</span><span class="sxs-lookup"><span data-stu-id="d023d-121">The second element of the **SYSTEMTIME** array contains the maximum allowable time.</span></span> <span data-ttu-id="d023d-122">Non è necessario inserire un elemento di matrice non specificato nel parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="d023d-122">It is not necessary to fill an array element that is not specified in the *wParam* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d023d-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d023d-123">Return value</span></span>

<span data-ttu-id="d023d-124">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d023d-124">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d023d-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="d023d-125">Remarks</span></span>

<span data-ttu-id="d023d-126">Il selettore di data e ora Visualizza solo le date e le ore che rientrano nell'intervallo specificato, impedendo all'utente di selezionare una data e un'ora non comprese nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="d023d-126">The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range.</span></span> <span data-ttu-id="d023d-127">Se il [**messaggio \_ SETSYSTEMTIME di DTM**](dtm-setsystemtime.md) specifica una data e un'ora che non rientrano nell'intervallo, l'operazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="d023d-127">If the [**DTM\_SETSYSTEMTIME**](dtm-setsystemtime.md) message specifies a date and time that falls outside the range, it will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="d023d-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d023d-128">Requirements</span></span>



| <span data-ttu-id="d023d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d023d-129">Requirement</span></span> | <span data-ttu-id="d023d-130">Valore</span><span class="sxs-lookup"><span data-stu-id="d023d-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d023d-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d023d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d023d-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d023d-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d023d-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d023d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d023d-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d023d-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d023d-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d023d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d023d-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d023d-136"><dt>Commctrl.h</dt></span></span> </dl> |



 


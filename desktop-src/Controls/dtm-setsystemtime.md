---
title: Messaggio DTM_SETSYSTEMTIME (COMmctrl. h)
description: Imposta l'ora in un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime SetSystemtime.
ms.assetid: aab023ac-22ef-485b-be2f-2aa76dfcf57f
keywords:
- Controlli di Windows Message DTM_SETSYSTEMTIME
topic_type:
- apiref
api_name:
- DTM_SETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b2a3c625ad4ff02bed138a8086ca0da984de35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964692"
---
# <a name="dtm_setsystemtime-message"></a><span data-ttu-id="b7b75-105">\_Messaggio SETSYSTEMTIME DTM</span><span class="sxs-lookup"><span data-stu-id="b7b75-105">DTM\_SETSYSTEMTIME message</span></span>

<span data-ttu-id="b7b75-106">Imposta l'ora in un controllo di selezione data e ora (DTP).</span><span class="sxs-lookup"><span data-stu-id="b7b75-106">Sets the time in a date and time picker (DTP) control.</span></span> <span data-ttu-id="b7b75-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) .</span><span class="sxs-lookup"><span data-stu-id="b7b75-107">You can send this message explicitly or use the [**DateTime\_SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b7b75-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7b75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7b75-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7b75-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7b75-110">Valore che specifica l'azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="b7b75-110">A value specifying the action that should be performed.</span></span> <span data-ttu-id="b7b75-111">Questo valore deve essere impostato su uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="b7b75-111">This value must be set to one of the following:</span></span>



| <span data-ttu-id="b7b75-112">Valore</span><span class="sxs-lookup"><span data-stu-id="b7b75-112">Value</span></span>                                                                                                                                             | <span data-ttu-id="b7b75-113">Significato</span><span class="sxs-lookup"><span data-stu-id="b7b75-113">Meaning</span></span>                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDT_VALID"></span><span id="gdt_valid"></span><dl> <span data-ttu-id="b7b75-114"><dt>**GDT \_ valido**</dt></span><span class="sxs-lookup"><span data-stu-id="b7b75-114"><dt>**GDT\_VALID**</dt></span></span> </dl> | <span data-ttu-id="b7b75-115">Impostare il controllo DTP in base ai dati all'interno della struttura a cui fa riferimento *lParam* .</span><span class="sxs-lookup"><span data-stu-id="b7b75-115">Set the DTP control according to the data within the structure that *lParam* points to.</span></span> <br/>                                                                                                                                                                 |
| <span id="GDT_NONE"></span><span id="gdt_none"></span><dl> <span data-ttu-id="b7b75-116"><dt>**GDT \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="b7b75-116"><dt>**GDT\_NONE**</dt></span></span> </dl>    | <span data-ttu-id="b7b75-117">Impostare il controllo DTP su "No date" e deselezionare la relativa casella di controllo.</span><span class="sxs-lookup"><span data-stu-id="b7b75-117">Set the DTP control to "no date" and clear its check box.</span></span> <span data-ttu-id="b7b75-118">Quando si specifica questo flag, *lParam* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b7b75-118">When this flag is specified, *lParam* is ignored.</span></span> <span data-ttu-id="b7b75-119">Questo flag si applica solo ai controlli DTP impostati sullo stile [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b7b75-119">This flag applies only to DTP controls that are set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="b7b75-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7b75-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7b75-121">Puntatore a una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) contenente l'ora di sistema utilizzata per impostare il controllo DTP.</span><span class="sxs-lookup"><span data-stu-id="b7b75-121">A pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure containing the system time used to set the DTP control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7b75-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7b75-122">Return value</span></span>

<span data-ttu-id="b7b75-123">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b7b75-123">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7b75-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7b75-124">Requirements</span></span>



| <span data-ttu-id="b7b75-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7b75-125">Requirement</span></span> | <span data-ttu-id="b7b75-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b7b75-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b75-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7b75-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b7b75-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7b75-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7b75-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7b75-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b7b75-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b7b75-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7b75-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7b75-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7b75-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7b75-132"><dt>Commctrl.h</dt></span></span> </dl> |



 


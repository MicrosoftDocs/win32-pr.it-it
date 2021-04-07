---
title: Messaggio DTM_SETFORMAT (COMmctrl. h)
description: Imposta la visualizzazione di un controllo di selezione data e ora (DTP) in base a una stringa di formato specificata. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro DateTime Seformatt.
ms.assetid: a89fa3ad-9894-4c52-ab56-fb62208e39b3
keywords:
- Controlli di Windows Message DTM_SETFORMAT
topic_type:
- apiref
api_name:
- DTM_SETFORMAT
- DTM_SETFORMATA
- DTM_SETFORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17669ed2e1ed23e3b090b77701bbe05d23a5ccb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048565"
---
# <a name="dtm_setformat-message"></a><span data-ttu-id="57abd-105">DTM- \_ Formatta messaggio</span><span class="sxs-lookup"><span data-stu-id="57abd-105">DTM\_SETFORMAT message</span></span>

<span data-ttu-id="57abd-106">Imposta la visualizzazione di un controllo di selezione data e ora (DTP) in base a una stringa di formato specificata.</span><span class="sxs-lookup"><span data-stu-id="57abd-106">Sets the display of a date and time picker (DTP) control based on a given format string.</span></span> <span data-ttu-id="57abd-107">È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**DateTime \_ seformatt**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) .</span><span class="sxs-lookup"><span data-stu-id="57abd-107">You can send this message explicitly or use the [**DateTime\_SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="57abd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="57abd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57abd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57abd-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="57abd-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="57abd-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="57abd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57abd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57abd-112">Puntatore a una [stringa di formato](date-and-time-picker-controls.md) con terminazione zero che definisce la visualizzazione desiderata.</span><span class="sxs-lookup"><span data-stu-id="57abd-112">A pointer to a zero-terminated [format string](date-and-time-picker-controls.md) that defines the desired display.</span></span> <span data-ttu-id="57abd-113">Se si imposta questo parametro su **null** , il controllo verrà reimpostato sulla stringa di formato predefinita per lo stile corrente.</span><span class="sxs-lookup"><span data-stu-id="57abd-113">Setting this parameter to **NULL** will reset the control to the default format string for the current style.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57abd-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57abd-114">Return value</span></span>

<span data-ttu-id="57abd-115">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="57abd-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="57abd-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="57abd-116">Remarks</span></span>

<span data-ttu-id="57abd-117">È accettabile includere caratteri aggiuntivi nella stringa di formato per produrre una visualizzazione più dettagliata.</span><span class="sxs-lookup"><span data-stu-id="57abd-117">It is acceptable to include extra characters within the format string to produce a more rich display.</span></span> <span data-ttu-id="57abd-118">Tutti i caratteri non formattati, tuttavia, devono essere racchiusi tra virgolette singole.</span><span class="sxs-lookup"><span data-stu-id="57abd-118">However, any nonformat characters must be enclosed within single quotes.</span></span> <span data-ttu-id="57abd-119">Ad esempio, la stringa di formato "' oggi è:' HH ':'':' ddddMMMdd ',' yyy" produrrebbe output come "Today is: 04:22:31 Tuesday Mar 23, 1996".</span><span class="sxs-lookup"><span data-stu-id="57abd-119">For example, the format string "'Today is: 'hh':'m':'s ddddMMMdd', 'yyy" would produce output like "Today is: 04:22:31 Tuesday Mar 23, 1996".</span></span>

> [!Note]  
> <span data-ttu-id="57abd-120">Un controllo DTP tiene traccia delle modifiche alle impostazioni locali quando usa la stringa di formato predefinita.</span><span class="sxs-lookup"><span data-stu-id="57abd-120">A DTP control tracks locale changes when it is using the default format string.</span></span> <span data-ttu-id="57abd-121">Se si imposta una stringa di formato personalizzata, non verrà aggiornata in risposta alle modifiche delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="57abd-121">If you set a custom format string, it will not be updated in response to locale changes.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="57abd-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57abd-122">Requirements</span></span>



| <span data-ttu-id="57abd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="57abd-123">Requirement</span></span> | <span data-ttu-id="57abd-124">Valore</span><span class="sxs-lookup"><span data-stu-id="57abd-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57abd-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57abd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="57abd-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="57abd-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57abd-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57abd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="57abd-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="57abd-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57abd-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57abd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="57abd-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="57abd-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="57abd-131">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="57abd-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="57abd-132">**DTM \_ SETFORMATW** (Unicode) e **MDT \_ formattera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="57abd-132">**DTM\_SETFORMATW** (Unicode) and **DTM\_SETFORMATA** (ANSI)</span></span><br/>               |



 

 






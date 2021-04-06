---
title: Codice di notifica DTN_FORMATQUERY (COMmctrl. h)
description: Inviato da un controllo di selezione data e ora (DTP) per recuperare la dimensione massima consentita della stringa che verrà visualizzata in un campo di callback. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0f00086a-0ab8-4f6f-9c3e-6e77008aa088
keywords:
- Controlli di Windows per il codice di notifica DTN_FORMATQUERY
topic_type:
- apiref
api_name:
- DTN_FORMATQUERY
- DTN_FORMATQUERYA
- DTN_FORMATQUERYW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e9653f369f13e0ef4a775265d763e854db4de7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963808"
---
# <a name="dtn_formatquery-notification-code"></a><span data-ttu-id="06c96-105">\_Codice di notifica FORMATQUERY di DTN</span><span class="sxs-lookup"><span data-stu-id="06c96-105">DTN\_FORMATQUERY notification code</span></span>

<span data-ttu-id="06c96-106">Inviato da un controllo di selezione data e ora (DTP) per recuperare la dimensione massima consentita della stringa che verrà visualizzata in un campo di callback.</span><span class="sxs-lookup"><span data-stu-id="06c96-106">Sent by a date and time picker (DTP) control to retrieve the maximum allowable size of the string that will be displayed in a callback field.</span></span> <span data-ttu-id="06c96-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="06c96-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_FORMATQUERY

    lpDTFormatQuery = (LPNMDATETIMEFORMATQUERY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="06c96-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="06c96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06c96-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06c96-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06c96-110">Puntatore a una struttura [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) contenente informazioni sul campo di callback.</span><span class="sxs-lookup"><span data-stu-id="06c96-110">A pointer to an [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) structure containing information about the callback field.</span></span> <span data-ttu-id="06c96-111">La struttura contiene una sottostringa che definisce un campo di callback e riceve la dimensione massima consentita della stringa che verrà visualizzata nel campo callback.</span><span class="sxs-lookup"><span data-stu-id="06c96-111">The structure contains a substring that defines a callback field and receives the maximum allowable size of the string that will be displayed in the callback field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06c96-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06c96-112">Return value</span></span>

<span data-ttu-id="06c96-113">Il proprietario del controllo deve calcolare la larghezza massima possibile del testo che verrà visualizzato nel campo callback, impostare il membro **szMax** della struttura [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) e restituire zero.</span><span class="sxs-lookup"><span data-stu-id="06c96-113">The owner of the control must calculate the maximum possible width of the text that will be displayed in the callback field, set the **szMax** member of the [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) structure, and return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="06c96-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="06c96-114">Remarks</span></span>

<span data-ttu-id="06c96-115">La gestione di questo codice di notifica prepara il controllo per la regolazione della dimensione massima della stringa che verrà visualizzata in un particolare campo di callback.</span><span class="sxs-lookup"><span data-stu-id="06c96-115">Handling this notification code prepares the control to adjust for the maximum size of the string that will be displayed in a particular callback field.</span></span> <span data-ttu-id="06c96-116">Ciò consente al controllo di visualizzare correttamente l'output in qualsiasi momento, riducendo lo sfarfallio all'interno della visualizzazione del controllo.</span><span class="sxs-lookup"><span data-stu-id="06c96-116">This enables the control to properly display output at all times, reducing flicker within the control's display.</span></span> <span data-ttu-id="06c96-117">Per ulteriori informazioni sui campi di callback, vedere [campi callback](date-and-time-picker-controls.md).</span><span class="sxs-lookup"><span data-stu-id="06c96-117">(For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="06c96-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06c96-118">Requirements</span></span>



| <span data-ttu-id="06c96-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="06c96-119">Requirement</span></span> | <span data-ttu-id="06c96-120">Valore</span><span class="sxs-lookup"><span data-stu-id="06c96-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06c96-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06c96-121">Minimum supported client</span></span><br/> | <span data-ttu-id="06c96-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06c96-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06c96-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06c96-123">Minimum supported server</span></span><br/> | <span data-ttu-id="06c96-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="06c96-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06c96-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06c96-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="06c96-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c96-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="06c96-127">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="06c96-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="06c96-128">**DTN \_ FORMATQUERYW** (Unicode) e **DTN \_ FORMATQUERYA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="06c96-128">**DTN\_FORMATQUERYW** (Unicode) and **DTN\_FORMATQUERYA** (ANSI)</span></span><br/>           |



 

 






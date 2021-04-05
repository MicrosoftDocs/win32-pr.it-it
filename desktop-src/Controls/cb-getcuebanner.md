---
title: Messaggio CB_GETCUEBANNER (winuser. h)
description: Ottiene il testo del banner cue visualizzato nel controllo di modifica di una casella combinata. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro ComboBox GetCueBannerText.
ms.assetid: 38959228-9f07-4636-a1ea-681efe77b9ec
keywords:
- Controlli di Windows Message CB_GETCUEBANNER
topic_type:
- apiref
api_name:
- CB_GETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866f51df0083c4cd72c3f34bb3ce045e0f577a24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874050"
---
# <a name="cb_getcuebanner-message"></a><span data-ttu-id="fcf44-105">\_Messaggio GETCUEBANNER CB</span><span class="sxs-lookup"><span data-stu-id="fcf44-105">CB\_GETCUEBANNER message</span></span>

<span data-ttu-id="fcf44-106">Ottiene il testo del banner cue visualizzato nel controllo di modifica di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="fcf44-106">Gets the cue banner text displayed in the edit control of a combo box.</span></span> <span data-ttu-id="fcf44-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**ComboBox \_ GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) .</span><span class="sxs-lookup"><span data-stu-id="fcf44-107">Send this message explicitly or by using the [**ComboBox\_GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fcf44-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fcf44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcf44-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcf44-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcf44-110">Puntatore a un buffer di stringa Unicode che riceve il testo del banner cue.</span><span class="sxs-lookup"><span data-stu-id="fcf44-110">A pointer to a Unicode string buffer that receives the cue banner text.</span></span> <span data-ttu-id="fcf44-111">L'applicazione chiamante è responsabile dell'allocazione della memoria per il buffer.</span><span class="sxs-lookup"><span data-stu-id="fcf44-111">The calling application is responsible for allocating the memory for the buffer.</span></span> <span data-ttu-id="fcf44-112">La dimensione del buffer deve essere uguale alla lunghezza della stringa del banner cue in **WCHAR**, più 1 per il **valore null** di terminazione **WCHAR**.</span><span class="sxs-lookup"><span data-stu-id="fcf44-112">The buffer size must be equal to the length of the cue banner string in **WCHARs**, plus 1 for the terminating **NULL** **WCHAR**.</span></span>

</dd> <dt>

<span data-ttu-id="fcf44-113">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcf44-113">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcf44-114">Dimensioni del buffer a cui punta *lpcwText* in **WCHAR**.</span><span class="sxs-lookup"><span data-stu-id="fcf44-114">The size of the buffer pointed to by *lpcwText* in **WCHARs**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcf44-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fcf44-115">Return value</span></span>

<span data-ttu-id="fcf44-116">Restituisce 1 se l'operazione ha esito positivo o un valore di errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fcf44-116">Returns 1 if successful, or an error value otherwise.</span></span>

<span data-ttu-id="fcf44-117">Se non è presente un testo del banner cue da ottenere, il valore restituito è 0.</span><span class="sxs-lookup"><span data-stu-id="fcf44-117">If there is no cue banner text to get, the return value is 0.</span></span> <span data-ttu-id="fcf44-118">Se l'applicazione chiamante non riesce ad allocare un buffer o impostare *lParam* prima di inviare questo messaggio, può verificarsi un comportamento non definito e il valore restituito potrebbe non essere affidabile.</span><span class="sxs-lookup"><span data-stu-id="fcf44-118">If the calling application fails to allocate a buffer, or set *lParam* before sending this message, undefined behavior may result and the return value may not be reliable.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcf44-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fcf44-119">Requirements</span></span>



| <span data-ttu-id="fcf44-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcf44-120">Requirement</span></span> | <span data-ttu-id="fcf44-121">Valore</span><span class="sxs-lookup"><span data-stu-id="fcf44-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcf44-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcf44-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fcf44-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fcf44-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fcf44-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcf44-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fcf44-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fcf44-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fcf44-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fcf44-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcf44-127"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcf44-127"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcf44-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fcf44-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcf44-129">Funzionalità della casella combinata</span><span class="sxs-lookup"><span data-stu-id="fcf44-129">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 






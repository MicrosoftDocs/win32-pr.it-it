---
title: Messaggio EM_SETCUEBANNER (COMmctrl. h)
description: Imposta la cue testuale, o tip, visualizzata dal controllo di modifica per richiedere informazioni all'utente.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- Controlli di Windows Message EM_SETCUEBANNER
topic_type:
- apiref
api_name:
- EM_SETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d740bf0a3a055f45c6d104d44349f078d3bf9ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478575"
---
# <a name="em_setcuebanner-message"></a><span data-ttu-id="1d15a-104">\_Messaggio SETCUEBANNER em</span><span class="sxs-lookup"><span data-stu-id="1d15a-104">EM\_SETCUEBANNER message</span></span>

<span data-ttu-id="1d15a-105">Imposta la cue testuale, o tip, visualizzata dal controllo di modifica per richiedere informazioni all'utente.</span><span class="sxs-lookup"><span data-stu-id="1d15a-105">Sets the textual cue, or tip, that is displayed by the edit control to prompt the user for information.</span></span>

## <a name="parameters"></a><span data-ttu-id="1d15a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d15a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d15a-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d15a-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d15a-108">**True** se il banner cue dovrebbe essere visualizzato anche quando il controllo di modifica ha lo stato attivo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="1d15a-108">**TRUE** if the cue banner should show even when the edit control has focus; otherwise, **FALSE**.</span></span> <span data-ttu-id="1d15a-109">**False** è il comportamento predefinito. il banner di cue scompare quando l'utente fa clic nel controllo.</span><span class="sxs-lookup"><span data-stu-id="1d15a-109">**FALSE** is the default behavior the cue banner disappears when the user clicks in the control.</span></span>

</dd> <dt>

<span data-ttu-id="1d15a-110">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d15a-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d15a-111">Puntatore a una stringa Unicode che contiene il testo da visualizzare come cue testuale.</span><span class="sxs-lookup"><span data-stu-id="1d15a-111">A pointer to a Unicode string that contains the text to display as the textual cue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d15a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d15a-112">Return value</span></span>

<span data-ttu-id="1d15a-113">Se il messaggio ha esito positivo, restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="1d15a-113">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="1d15a-114">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="1d15a-114">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d15a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d15a-115">Remarks</span></span>

<span data-ttu-id="1d15a-116">Un controllo di modifica usato per iniziare una ricerca può visualizzare "immettere la ricerca qui" in testo grigio come cue testuale.</span><span class="sxs-lookup"><span data-stu-id="1d15a-116">An edit control that is used to begin a search may display "Enter search here" in gray text as a textual cue.</span></span> <span data-ttu-id="1d15a-117">Quando l'utente fa clic sul testo, il testo viene allontanato e l'utente può digitare.</span><span class="sxs-lookup"><span data-stu-id="1d15a-117">When the user clicks the text, the text goes away and the user can type.</span></span>

<span data-ttu-id="1d15a-118">Non è possibile impostare un banner cue su un controllo di modifica su più righe o su un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="1d15a-118">You cannot set a cue banner on a multiline edit control or on a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="1d15a-119">Per usare questa API, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="1d15a-119">To use this API, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1d15a-120">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1d15a-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1d15a-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d15a-121">Requirements</span></span>



| <span data-ttu-id="1d15a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d15a-122">Requirement</span></span> | <span data-ttu-id="1d15a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="1d15a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d15a-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d15a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1d15a-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1d15a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1d15a-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d15a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1d15a-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1d15a-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1d15a-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d15a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d15a-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d15a-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d15a-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d15a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d15a-131">**Modifica \_ SetCueBannerText**</span><span class="sxs-lookup"><span data-stu-id="1d15a-131">**Edit\_SetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
</dt> </dl>

 

 






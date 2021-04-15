---
title: Messaggio EM_SETPASSWORDCHAR (winuser. h)
description: Imposta o rimuove il carattere della password per un controllo di modifica. Quando viene impostato un carattere della password, il carattere viene visualizzato al posto dei caratteri digitati dall'utente. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 9091892c-9f37-4e06-a084-9326c5f7f31e
keywords:
- Controlli di Windows Message EM_SETPASSWORDCHAR
topic_type:
- apiref
api_name:
- EM_SETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd2c75039a6d447809cc17e5c44d70c6e612ede
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476336"
---
# <a name="em_setpasswordchar-message"></a><span data-ttu-id="a4dc1-106">\_Messaggio SETPASSWORDCHAR em</span><span class="sxs-lookup"><span data-stu-id="a4dc1-106">EM\_SETPASSWORDCHAR message</span></span>

<span data-ttu-id="a4dc1-107">Imposta o rimuove il carattere della password per un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="a4dc1-107">Sets or removes the password character for an edit control.</span></span> <span data-ttu-id="a4dc1-108">Quando viene impostato un carattere della password, il carattere viene visualizzato al posto dei caratteri digitati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a4dc1-108">When a password character is set, that character is displayed in place of the characters typed by the user.</span></span> <span data-ttu-id="a4dc1-109">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="a4dc1-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a4dc1-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a4dc1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4dc1-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a4dc1-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4dc1-112">Carattere da visualizzare al posto dei caratteri digitati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a4dc1-112">The character to be displayed in place of the characters typed by the user.</span></span> <span data-ttu-id="a4dc1-113">Se questo parametro è zero, il controllo rimuove il carattere della password corrente e Visualizza i caratteri digitati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a4dc1-113">If this parameter is zero, the control removes the current password character and displays the characters typed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="a4dc1-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4dc1-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4dc1-115">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="a4dc1-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4dc1-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a4dc1-116">Return value</span></span>

<span data-ttu-id="a4dc1-117">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="a4dc1-117">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4dc1-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4dc1-118">Remarks</span></span>

<span data-ttu-id="a4dc1-119">Quando un controllo di modifica riceve il messaggio **\_ SETPASSWORDCHAR em** , il controllo ridisegni tutti i caratteri visibili usando il carattere specificato dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="a4dc1-119">When an edit control receives the **EM\_SETPASSWORDCHAR** message, the control redraws all visible characters using the character specified by the *wParam* parameter.</span></span> <span data-ttu-id="a4dc1-120">Se *wParam* è zero, il controllo ridisegni tutti i caratteri visibili usando i caratteri digitati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a4dc1-120">If *wParam* is zero, the control redraws all visible characters using the characters typed by the user.</span></span>

<span data-ttu-id="a4dc1-121">Se viene creato un controllo di modifica con lo stile di [**\_ password es**](edit-control-styles.md) , il carattere predefinito della password viene impostato su un asterisco ( \* ).</span><span class="sxs-lookup"><span data-stu-id="a4dc1-121">If an edit control is created with the [**ES\_PASSWORD**](edit-control-styles.md) style, the default password character is set to an asterisk (\*).</span></span> <span data-ttu-id="a4dc1-122">Se un controllo di modifica viene creato senza lo stile di **\_ password es** , non è presente alcun carattere di password.</span><span class="sxs-lookup"><span data-stu-id="a4dc1-122">If an edit control is created without the **ES\_PASSWORD** style, there is no password character.</span></span> <span data-ttu-id="a4dc1-123">Lo stile di **\_ password es** viene rimosso se viene inviato un messaggio **\_ SETPASSWORDCHAR em** con il parametro *wParam* impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="a4dc1-123">The **ES\_PASSWORD** style is removed if an **EM\_SETPASSWORDCHAR** message is sent with the *wParam* parameter set to zero.</span></span>

<span data-ttu-id="a4dc1-124">**Controlli di modifica:** I controlli di modifica su più righe non supportano lo stile o i messaggi della password.</span><span class="sxs-lookup"><span data-stu-id="a4dc1-124">**Edit controls:** Multiline edit controls do not support the password style or messages.</span></span>

<span data-ttu-id="a4dc1-125">**Modifica avanzata:** Supportato in Microsoft Rich Edit 2,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a4dc1-125">**Rich Edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="a4dc1-126">I controlli di modifica a riga singola e a più righe supportano lo stile e i messaggi della password.</span><span class="sxs-lookup"><span data-stu-id="a4dc1-126">Both single-line and multiline edit controls support the password style and messages.</span></span> <span data-ttu-id="a4dc1-127">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="a4dc1-127">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4dc1-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4dc1-128">Requirements</span></span>



| <span data-ttu-id="a4dc1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4dc1-129">Requirement</span></span> | <span data-ttu-id="a4dc1-130">Valore</span><span class="sxs-lookup"><span data-stu-id="a4dc1-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4dc1-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4dc1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a4dc1-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4dc1-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a4dc1-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4dc1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a4dc1-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a4dc1-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a4dc1-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4dc1-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4dc1-136"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4dc1-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4dc1-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4dc1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4dc1-138">**\_GETPASSWORDCHAR em**</span><span class="sxs-lookup"><span data-stu-id="a4dc1-138">**EM\_GETPASSWORDCHAR**</span></span>](em-getpasswordchar.md)
</dt> </dl>

 

 






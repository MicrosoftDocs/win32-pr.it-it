---
title: Messaggio EM_GETPASSWORDCHAR (winuser. h)
description: Ottiene il carattere della password visualizzato da un controllo di modifica quando l'utente immette il testo. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 874336f6-701b-466a-afa6-0cb3e787ba4c
keywords:
- Controlli di Windows Message EM_GETPASSWORDCHAR
topic_type:
- apiref
api_name:
- EM_GETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6285f002554e22c89896711d3d1d355a95c6bb7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874362"
---
# <a name="em_getpasswordchar-message"></a><span data-ttu-id="4ddec-105">\_Messaggio GETPASSWORDCHAR em</span><span class="sxs-lookup"><span data-stu-id="4ddec-105">EM\_GETPASSWORDCHAR message</span></span>

<span data-ttu-id="4ddec-106">Ottiene il carattere della password visualizzato da un controllo di modifica quando l'utente immette il testo.</span><span class="sxs-lookup"><span data-stu-id="4ddec-106">Gets the password character that an edit control displays when the user enters text.</span></span> <span data-ttu-id="4ddec-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="4ddec-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4ddec-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ddec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ddec-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4ddec-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ddec-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4ddec-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4ddec-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ddec-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ddec-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4ddec-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ddec-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ddec-113">Return value</span></span>

<span data-ttu-id="4ddec-114">Il valore restituito specifica il carattere da visualizzare al posto di tutti i caratteri digitati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="4ddec-114">The return value specifies the character to be displayed in place of any characters typed by the user.</span></span> <span data-ttu-id="4ddec-115">Se il valore restituito è **null**, non è presente alcun carattere della password e il controllo Visualizza i caratteri digitati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="4ddec-115">If the return value is **NULL**, there is no password character, and the control displays the characters typed by the user.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ddec-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ddec-116">Remarks</span></span>

<span data-ttu-id="4ddec-117">Se viene creato un controllo di modifica con lo stile di [**\_ password es**](edit-control-styles.md) , il carattere predefinito della password viene impostato su un asterisco ( \* ).</span><span class="sxs-lookup"><span data-stu-id="4ddec-117">If an edit control is created with the [**ES\_PASSWORD**](edit-control-styles.md) style, the default password character is set to an asterisk (\*).</span></span> <span data-ttu-id="4ddec-118">Se un controllo di modifica viene creato senza lo stile di **\_ password es** , non è presente alcun carattere di password.</span><span class="sxs-lookup"><span data-stu-id="4ddec-118">If an edit control is created without the **ES\_PASSWORD** style, there is no password character.</span></span> <span data-ttu-id="4ddec-119">Per modificare il carattere della password, inviare il messaggio [**\_ SETPASSWORDCHAR em**](em-setpasswordchar.md) .</span><span class="sxs-lookup"><span data-stu-id="4ddec-119">To change the password character, send the [**EM\_SETPASSWORDCHAR**](em-setpasswordchar.md) message.</span></span>

<span data-ttu-id="4ddec-120">**Controlli di modifica:** I controlli di modifica su più righe non supportano lo stile o i messaggi della password.</span><span class="sxs-lookup"><span data-stu-id="4ddec-120">**Edit controls:** Multiline edit controls do not support the password style or messages.</span></span>

<span data-ttu-id="4ddec-121">**Modifica avanzata:** Supportato in Microsoft Rich Edit 2,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4ddec-121">**Rich edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="4ddec-122">I controlli di modifica a riga singola e a più righe supportano lo stile e i messaggi della password.</span><span class="sxs-lookup"><span data-stu-id="4ddec-122">Both single-line and multiline edit controls support the password style and messages.</span></span> <span data-ttu-id="4ddec-123">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="4ddec-123">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ddec-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ddec-124">Requirements</span></span>



| <span data-ttu-id="4ddec-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ddec-125">Requirement</span></span> | <span data-ttu-id="4ddec-126">Valore</span><span class="sxs-lookup"><span data-stu-id="4ddec-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ddec-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ddec-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4ddec-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ddec-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4ddec-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ddec-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4ddec-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4ddec-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4ddec-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ddec-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ddec-132"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ddec-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ddec-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ddec-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ddec-134">**\_SETPASSWORDCHAR em**</span><span class="sxs-lookup"><span data-stu-id="4ddec-134">**EM\_SETPASSWORDCHAR**</span></span>](em-setpasswordchar.md)
</dt> </dl>

 

 






---
title: Messaggio CBEM_HASEDITCHANGED (COMmctrl. h)
description: Determina se l'utente ha modificato il testo di un controllo di modifica ComboBoxEx.
ms.assetid: 8bf8c40a-e1ab-4748-899b-a9ed27767884
keywords:
- Controlli di Windows Message CBEM_HASEDITCHANGED
topic_type:
- apiref
api_name:
- CBEM_HASEDITCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5234b816a2ec080449ade072981b489968df8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964944"
---
# <a name="cbem_haseditchanged-message"></a><span data-ttu-id="f4135-104">\_Messaggio CBEM HASEDITCHANGED</span><span class="sxs-lookup"><span data-stu-id="f4135-104">CBEM\_HASEDITCHANGED message</span></span>

<span data-ttu-id="f4135-105">Determina se l'utente ha modificato il testo di un controllo di modifica ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="f4135-105">Determines whether the user has changed the text of a ComboBoxEx edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f4135-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4135-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4135-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4135-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f4135-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f4135-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f4135-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4135-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f4135-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f4135-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4135-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4135-111">Return value</span></span>

<span data-ttu-id="f4135-112">Restituisce **true** se il testo nella casella di modifica del controllo è stato modificato; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="f4135-112">Returns **TRUE** if the text in the control's edit box has been changed, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4135-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4135-113">Remarks</span></span>

<span data-ttu-id="f4135-114">Un controllo ComboBoxEx usa un controllo casella di modifica quando è impostato sullo stile [**a \_ discesa CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f4135-114">A ComboBoxEx control uses an edit box control when it is set to the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span> <span data-ttu-id="f4135-115">È possibile recuperare l'handle di finestra del controllo casella di modifica inviando un messaggio [**CBEM \_ GETEDITCONTROL**](cbem-geteditcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="f4135-115">You can retrieve the edit box control's window handle by sending a [**CBEM\_GETEDITCONTROL**](cbem-geteditcontrol.md) message.</span></span>

<span data-ttu-id="f4135-116">Quando l'utente inizia a modificare, si riceverà una notifica [CBEN \_ BEGINEDIT](cben-beginedit.md) .</span><span class="sxs-lookup"><span data-stu-id="f4135-116">When the user begins editing, you will receive a [CBEN\_BEGINEDIT](cben-beginedit.md) notification.</span></span> <span data-ttu-id="f4135-117">Al termine della modifica, o se lo stato attivo cambia, si riceverà una notifica [CBEN \_ ENDEDIT](cben-endedit.md) .</span><span class="sxs-lookup"><span data-stu-id="f4135-117">When editing is complete, or the focus changes, you will receive a [CBEN\_ENDEDIT](cben-endedit.md) notification.</span></span> <span data-ttu-id="f4135-118">Il **messaggio \_ HASEDITCHANGED CBEM** è utile solo per determinare se il testo è stato modificato se viene inviato prima della notifica di CBEN \_ ENDEDIT.</span><span class="sxs-lookup"><span data-stu-id="f4135-118">The **CBEM\_HASEDITCHANGED** message is only useful for determining whether the text has been changed if it is sent before the CBEN\_ENDEDIT notification.</span></span> <span data-ttu-id="f4135-119">Se il messaggio viene inviato in seguito, restituirà **false**.</span><span class="sxs-lookup"><span data-stu-id="f4135-119">If the message is sent afterward, it will return **FALSE**.</span></span> <span data-ttu-id="f4135-120">Si supponga, ad esempio, che l'utente inizi a modificare il testo nella casella di modifica, ma modifichi lo stato attivo, generando una \_ notifica CBEN ENDEDIT.</span><span class="sxs-lookup"><span data-stu-id="f4135-120">For example, suppose the user starts to edit the text in the edit box but changes focus, generating a CBEN\_ENDEDIT notification.</span></span> <span data-ttu-id="f4135-121">Se quindi si invia un messaggio **CBEM \_ HASEDITCHANGED** , viene restituito **false**, anche se il testo è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="f4135-121">If you then send a **CBEM\_HASEDITCHANGED** message, it will return **FALSE**, even though the text has been changed.</span></span>

<span data-ttu-id="f4135-122">Lo [**stile \_ semplice CBS**](combo-box-styles.md) non funziona correttamente con **CBEM \_ HASEDITCHANGED**.</span><span class="sxs-lookup"><span data-stu-id="f4135-122">The [**CBS\_SIMPLE**](combo-box-styles.md) style does not work correctly with **CBEM\_HASEDITCHANGED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4135-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4135-123">Requirements</span></span>



| <span data-ttu-id="f4135-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4135-124">Requirement</span></span> | <span data-ttu-id="f4135-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f4135-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4135-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4135-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f4135-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4135-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f4135-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4135-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f4135-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f4135-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4135-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4135-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4135-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4135-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






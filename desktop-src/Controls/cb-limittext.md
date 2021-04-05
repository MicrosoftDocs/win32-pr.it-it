---
title: Messaggio CB_LIMITTEXT (winuser. h)
description: Limita la lunghezza del testo che l'utente può digitare nel controllo di modifica di una casella combinata.
ms.assetid: 95b7d07a-594b-4096-afbb-4dab77bdc41d
keywords:
- Controlli di Windows Message CB_LIMITTEXT
topic_type:
- apiref
api_name:
- CB_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ea9ccd63bb1503e73aebdd584a53bc32bcb8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048351"
---
# <a name="cb_limittext-message"></a><span data-ttu-id="b6313-104">\_Messaggio LIMITTEXT CB</span><span class="sxs-lookup"><span data-stu-id="b6313-104">CB\_LIMITTEXT message</span></span>

<span data-ttu-id="b6313-105">Limita la lunghezza del testo che l'utente può digitare nel controllo di modifica di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="b6313-105">Limits the length of the text the user may type into the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6313-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6313-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6313-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6313-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6313-108">Numero massimo di **TCHARs** che l'utente può immettere, escluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="b6313-108">The maximum number of **TCHARs** the user can enter, not including the terminating null character.</span></span> <span data-ttu-id="b6313-109">Se questo parametro è zero, la lunghezza del testo è limitata ai caratteri 0x7FFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="b6313-109">If this parameter is zero, the text length is limited to 0x7FFFFFFE characters.</span></span>

</dd> <dt>

<span data-ttu-id="b6313-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6313-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6313-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="b6313-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6313-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6313-112">Return value</span></span>

<span data-ttu-id="b6313-113">Il valore restituito è sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="b6313-113">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6313-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6313-114">Remarks</span></span>

<span data-ttu-id="b6313-115">Se la casella combinata non ha lo stile [**CBS \_ AUTOHSCROLL**](combo-box-styles.md) , l'impostazione del limite di testo su un valore superiore a quello del controllo di modifica non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="b6313-115">If the combo box does not have the [**CBS\_AUTOHSCROLL**](combo-box-styles.md) style, setting the text limit to be larger than the size of the edit control has no effect.</span></span>

<span data-ttu-id="b6313-116">Il messaggio **CB \_ LIMITTEXT** limita solo il testo che l'utente può immettere.</span><span class="sxs-lookup"><span data-stu-id="b6313-116">The **CB\_LIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="b6313-117">Non ha alcun effetto sui testi già presenti nel controllo di modifica quando il messaggio viene inviato, né sulla lunghezza del testo copiato nel controllo di modifica quando viene selezionata una stringa nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="b6313-117">It has no effect on any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control when a string in the list box is selected.</span></span>

<span data-ttu-id="b6313-118">Il limite predefinito al testo che un utente può immettere nel controllo di modifica è 30.000 **TCHARs**.</span><span class="sxs-lookup"><span data-stu-id="b6313-118">The default limit to the text a user can enter in the edit control is 30,000 **TCHARs**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6313-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6313-119">Requirements</span></span>



| <span data-ttu-id="b6313-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6313-120">Requirement</span></span> | <span data-ttu-id="b6313-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b6313-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6313-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6313-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b6313-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6313-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b6313-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6313-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b6313-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6313-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b6313-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6313-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6313-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6313-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 






---
title: Messaggio di EM_EXLIMITTEXT (RichEdit. h)
description: Imposta un limite massimo per la quantità di testo che l'utente può digitare o incollare in un controllo Rich Edit.
ms.assetid: 66fcdbb9-99ac-4122-b89c-be4aef80fbae
keywords:
- Controlli di Windows Message EM_EXLIMITTEXT
topic_type:
- apiref
api_name:
- EM_EXLIMITTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c4ebb554e3aa3139a66ca63970356e1261a23f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477597"
---
# <a name="em_exlimittext-message"></a><span data-ttu-id="0df97-104">\_Messaggio EXLIMITTEXT em</span><span class="sxs-lookup"><span data-stu-id="0df97-104">EM\_EXLIMITTEXT message</span></span>

<span data-ttu-id="0df97-105">Imposta un limite massimo per la quantità di testo che l'utente può digitare o incollare in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="0df97-105">Sets an upper limit to the amount of text the user can type or paste into a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0df97-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0df97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0df97-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0df97-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0df97-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0df97-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0df97-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0df97-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0df97-110">Specifica la quantità massima di testo che è possibile immettere.</span><span class="sxs-lookup"><span data-stu-id="0df97-110">Specifies the maximum amount of text that can be entered.</span></span> <span data-ttu-id="0df97-111">Se questo parametro è zero, viene usato il valore massimo predefinito, ovvero i caratteri 64K.</span><span class="sxs-lookup"><span data-stu-id="0df97-111">If this parameter is zero, the default maximum is used, which is 64K characters.</span></span> <span data-ttu-id="0df97-112">Un oggetto COM viene conteggiato come un singolo carattere.</span><span class="sxs-lookup"><span data-stu-id="0df97-112">A COM object counts as a single character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0df97-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0df97-113">Return value</span></span>

<span data-ttu-id="0df97-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="0df97-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0df97-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="0df97-115">Remarks</span></span>

<span data-ttu-id="0df97-116">Il limite di testo impostato dal **messaggio \_ EXLIMITTEXT em** non limita la quantità di testo che è possibile trasmettere in un controllo Rich Edit usando il messaggio [**\_ flusso em**](em-streamin.md) con *lParam* impostato sul \_ testo SF.</span><span class="sxs-lookup"><span data-stu-id="0df97-116">The text limit set by the **EM\_EXLIMITTEXT** message does not limit the amount of text that you can stream into a rich edit control using the [**EM\_STREAMIN**](em-streamin.md) message with *lParam* set to SF\_TEXT.</span></span> <span data-ttu-id="0df97-117">Tuttavia, limita la quantità di testo che è possibile trasmettere in un controllo Rich Edit usando il messaggio **\_ flusso em** nel messaggio con *lParam* impostato sul formato SF \_ RTF.</span><span class="sxs-lookup"><span data-stu-id="0df97-117">However, it does limit the amount of text that you can stream into a rich edit control using the **EM\_STREAMIN** message with *lParam* set to SF\_RTF.</span></span>

<span data-ttu-id="0df97-118">Prima di chiamare **em \_ EXLIMITTEXT** , il limite predefinito per la quantità di testo che un utente può immettere è 32.767 caratteri.</span><span class="sxs-lookup"><span data-stu-id="0df97-118">Before **EM\_EXLIMITTEXT** is called, the default limit to the amount of text a user can enter is 32,767 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="0df97-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0df97-119">Requirements</span></span>



| <span data-ttu-id="0df97-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0df97-120">Requirement</span></span> | <span data-ttu-id="0df97-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0df97-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0df97-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0df97-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0df97-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0df97-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0df97-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0df97-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0df97-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0df97-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0df97-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0df97-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0df97-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0df97-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0df97-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0df97-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0df97-129">**flusso EMin \_**</span><span class="sxs-lookup"><span data-stu-id="0df97-129">**EM\_STREAMIN**</span></span>](em-streamin.md)
</dt> </dl>

 

 






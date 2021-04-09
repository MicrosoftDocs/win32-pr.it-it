---
title: Messaggio di EM_CANPASTE (RichEdit. h)
description: Determina se un controllo Rich Edit può incollare un formato degli Appunti specificato.
ms.assetid: 1b858ad8-1312-407b-b12a-c63668ba9f72
keywords:
- Controlli di Windows Message EM_CANPASTE
topic_type:
- apiref
api_name:
- EM_CANPASTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad400b610a033b6f67177da99876a892d294ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048525"
---
# <a name="em_canpaste-message"></a><span data-ttu-id="5bf62-104">\_Messaggio CANPASTE em</span><span class="sxs-lookup"><span data-stu-id="5bf62-104">EM\_CANPASTE message</span></span>

<span data-ttu-id="5bf62-105">Determina se un controllo Rich Edit può incollare un formato degli Appunti specificato.</span><span class="sxs-lookup"><span data-stu-id="5bf62-105">Determines whether a rich edit control can paste a specified clipboard format.</span></span>

## <a name="parameters"></a><span data-ttu-id="5bf62-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5bf62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bf62-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5bf62-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5bf62-108">Specifica i [formati degli Appunti](/windows/desktop/dataxchg/clipboard-formats) da provare.</span><span class="sxs-lookup"><span data-stu-id="5bf62-108">Specifies the [Clipboard Formats](/windows/desktop/dataxchg/clipboard-formats) to try.</span></span> <span data-ttu-id="5bf62-109">Per provare qualsiasi formato attualmente negli Appunti, impostare questo parametro su zero.</span><span class="sxs-lookup"><span data-stu-id="5bf62-109">To try any format currently on the clipboard, set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="5bf62-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5bf62-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5bf62-111">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5bf62-111">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bf62-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5bf62-112">Return value</span></span>

<span data-ttu-id="5bf62-113">Se il formato degli Appunti può essere incollato, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="5bf62-113">If the clipboard format can be pasted, the return value is a nonzero value.</span></span>

<span data-ttu-id="5bf62-114">Se il formato degli Appunti non può essere incollato, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="5bf62-114">If the clipboard format cannot be pasted, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bf62-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bf62-115">Requirements</span></span>



| <span data-ttu-id="5bf62-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bf62-116">Requirement</span></span> | <span data-ttu-id="5bf62-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5bf62-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5bf62-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bf62-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5bf62-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5bf62-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5bf62-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bf62-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5bf62-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5bf62-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5bf62-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5bf62-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bf62-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bf62-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bf62-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5bf62-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bf62-125">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="5bf62-125">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 


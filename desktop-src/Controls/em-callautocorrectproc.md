---
title: Messaggio di EM_CALLAUTOCORRECTPROC (RichEdit. h)
description: Chiama la funzione di callback di correzione automatica archiviata dal \_ messaggio SETAUTOCORRECTPROC em, purché il testo che precede il punto di inserimento sia candidato per la correzione automatica.
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- Controlli di Windows Message EM_CALLAUTOCORRECTPROC
topic_type:
- apiref
api_name:
- EM_CALLAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73109d2499fc01a1d811066dc6059593c7ed5e0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477626"
---
# <a name="em_callautocorrectproc-message"></a><span data-ttu-id="a2455-104">\_Messaggio CALLAUTOCORRECTPROC em</span><span class="sxs-lookup"><span data-stu-id="a2455-104">EM\_CALLAUTOCORRECTPROC message</span></span>

<span data-ttu-id="a2455-105">Chiama la funzione di callback di correzione automatica archiviata dal [**messaggio \_ SETAUTOCORRECTPROC em**](em-setautocorrectproc.md) , purché il testo che precede il punto di inserimento sia candidato per la correzione automatica.</span><span class="sxs-lookup"><span data-stu-id="a2455-105">Calls the autocorrect callback function that is stored by the [**EM\_SETAUTOCORRECTPROC**](em-setautocorrectproc.md) message, provided that the text preceding the insertion point is a candidate for autocorrection.</span></span>


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a><span data-ttu-id="a2455-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2455-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2455-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a2455-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2455-108">Carattere di tipo **WCHAR**.</span><span class="sxs-lookup"><span data-stu-id="a2455-108">A character of type **WCHAR**.</span></span> <span data-ttu-id="a2455-109">Se il carattere è una tabulazione (U + 0009) e il carattere che precede il punto di inserimento è t a Tab, il carattere che precede il punto di inserimento viene considerato come parte della stringa candidata di correzione automatica anziché come delimitatore di stringa. in caso contrario, *wParam* non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="a2455-109">If this character is a tab (U+0009), and the character preceding the insertion point isn t a tab, then the character preceding the insertion point is treated as part of the autocorrect candidate string instead of as a string delimiter; otherwise, *wParam* has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="a2455-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2455-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2455-111">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a2455-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2455-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2455-112">Return value</span></span>

<span data-ttu-id="a2455-113">Il valore restituito è zero se il messaggio riesce oppure un valore diverso da zero se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="a2455-113">The return value is zero if the message succeeds, or nonzero if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2455-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2455-114">Requirements</span></span>



| <span data-ttu-id="a2455-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2455-115">Requirement</span></span> | <span data-ttu-id="a2455-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a2455-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2455-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2455-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a2455-118">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a2455-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a2455-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2455-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a2455-120">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a2455-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a2455-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2455-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2455-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2455-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2455-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2455-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2455-124">*AutoCorrectProc*</span><span class="sxs-lookup"><span data-stu-id="a2455-124">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="a2455-125">**\_GETAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="a2455-125">**EM\_GETAUTOCORRECTPROC**</span></span>](em-getautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="a2455-126">**\_SETAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="a2455-126">**EM\_SETAUTOCORRECTPROC**</span></span>](em-setautocorrectproc.md)
</dt> </dl>

 

 






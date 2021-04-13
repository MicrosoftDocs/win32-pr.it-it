---
title: Messaggio di EM_GETTEXTMODE (RichEdit. h)
description: Ottiene la modalità testo corrente e il livello di annullamento di un controllo Rich Edit.
ms.assetid: 5c976a82-9c51-4700-9db4-a6b0ed7bb852
keywords:
- Controlli di Windows Message EM_GETTEXTMODE
topic_type:
- apiref
api_name:
- EM_GETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012a12aec573518c859ec7f2a0319036dcd1ef87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478113"
---
# <a name="em_gettextmode-message"></a><span data-ttu-id="259a1-104">\_Messaggio GETTEXTMODE em</span><span class="sxs-lookup"><span data-stu-id="259a1-104">EM\_GETTEXTMODE message</span></span>

<span data-ttu-id="259a1-105">Ottiene la modalità testo corrente e il livello di annullamento di un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="259a1-105">Gets the current text mode and undo level of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="259a1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="259a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="259a1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="259a1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="259a1-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="259a1-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="259a1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="259a1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="259a1-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="259a1-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="259a1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="259a1-111">Return value</span></span>

<span data-ttu-id="259a1-112">Il valore restituito è uno o più valori del tipo di enumerazione [**TextMode**](/windows/win32/api/richedit/ne-richedit-textmode) .</span><span class="sxs-lookup"><span data-stu-id="259a1-112">The return value is one or more values from the [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) enumeration type.</span></span> <span data-ttu-id="259a1-113">I valori indicano la modalità testo corrente e il livello di annullamento del controllo.</span><span class="sxs-lookup"><span data-stu-id="259a1-113">The values indicate the current text mode and undo level of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="259a1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="259a1-114">Requirements</span></span>



| <span data-ttu-id="259a1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="259a1-115">Requirement</span></span> | <span data-ttu-id="259a1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="259a1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="259a1-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="259a1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="259a1-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="259a1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="259a1-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="259a1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="259a1-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="259a1-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="259a1-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="259a1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="259a1-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="259a1-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="259a1-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="259a1-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="259a1-124">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="259a1-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="259a1-125">**\_SETTEXTMODE em**</span><span class="sxs-lookup"><span data-stu-id="259a1-125">**EM\_SETTEXTMODE**</span></span>](em-settextmode.md)
</dt> <dt>

[<span data-ttu-id="259a1-126">**TEXTMODE**</span><span class="sxs-lookup"><span data-stu-id="259a1-126">**TEXTMODE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> </dl>

 

 






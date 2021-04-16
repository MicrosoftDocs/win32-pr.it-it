---
title: Messaggio di EM_SETIMECOLOR (RichEdit. h)
description: Imposta il colore di composizione IME (Input Method Editor) per un controllo Rich Edit.
ms.assetid: ea5449c9-7d0f-4340-8e3e-1e0b77d443f6
keywords:
- Controlli di Windows Message EM_SETIMECOLOR
topic_type:
- apiref
api_name:
- EM_SETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c020bb3af2b1197afc005bd0b6efec82b609b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477321"
---
# <a name="em_setimecolor-message"></a><span data-ttu-id="8bd58-104">\_Messaggio SETIMECOLOR em</span><span class="sxs-lookup"><span data-stu-id="8bd58-104">EM\_SETIMECOLOR message</span></span>

<span data-ttu-id="8bd58-105">Imposta il colore di composizione IME (Input Method Editor) per un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="8bd58-105">Sets the Input Method Editor (IME) composition color for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="8bd58-106">Questo messaggio è supportato solo nelle versioni in lingua asiatica di Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="8bd58-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="8bd58-107">Non è supportata nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8bd58-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="8bd58-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8bd58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bd58-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8bd58-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8bd58-110">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8bd58-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8bd58-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8bd58-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8bd58-112">Puntatore a una struttura [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) contenente il colore di composizione da impostare.</span><span class="sxs-lookup"><span data-stu-id="8bd58-112">Pointer to a [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) structure that contains the composition color to be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bd58-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8bd58-113">Return value</span></span>

<span data-ttu-id="8bd58-114">Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="8bd58-114">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="8bd58-115">Se l'operazione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="8bd58-115">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bd58-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bd58-116">Requirements</span></span>



| <span data-ttu-id="8bd58-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bd58-117">Requirement</span></span> | <span data-ttu-id="8bd58-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8bd58-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8bd58-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bd58-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8bd58-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8bd58-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8bd58-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bd58-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8bd58-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8bd58-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8bd58-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8bd58-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bd58-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bd58-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bd58-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bd58-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="8bd58-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="8bd58-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8bd58-127">**\_GETIMECOLOR em**</span><span class="sxs-lookup"><span data-stu-id="8bd58-127">**EM\_GETIMECOLOR**</span></span>](em-getimecolor.md)
</dt> <dt>

[<span data-ttu-id="8bd58-128">**COMPCOLOR**</span><span class="sxs-lookup"><span data-stu-id="8bd58-128">**COMPCOLOR**</span></span>](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 






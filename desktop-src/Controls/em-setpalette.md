---
title: Messaggio di EM_SETPALETTE (RichEdit. h)
description: Modifica la tavolozza utilizzata da un controllo Rich Edit per la finestra di visualizzazione.
ms.assetid: c1dc0c24-eaf2-47a8-9bb1-59f37b206feb
keywords:
- Controlli di Windows Message EM_SETPALETTE
topic_type:
- apiref
api_name:
- EM_SETPALETTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026a0a85001818b6f69366e8dba80ef56a7a8f20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048264"
---
# <a name="em_setpalette-message"></a><span data-ttu-id="59ccf-104">\_Messaggio SEPALETTE em</span><span class="sxs-lookup"><span data-stu-id="59ccf-104">EM\_SETPALETTE message</span></span>

<span data-ttu-id="59ccf-105">Modifica la tavolozza utilizzata da un controllo Rich Edit per la finestra di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="59ccf-105">Changes the palette that a rich edit control uses for its display window.</span></span>

## <a name="parameters"></a><span data-ttu-id="59ccf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="59ccf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59ccf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59ccf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59ccf-108">Handle per la nuova tavolozza utilizzata dal controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="59ccf-108">Handle to the new palette used by the rich edit control.</span></span>

</dd> <dt>

<span data-ttu-id="59ccf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59ccf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59ccf-110">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="59ccf-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59ccf-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59ccf-111">Return value</span></span>

<span data-ttu-id="59ccf-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="59ccf-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59ccf-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="59ccf-113">Remarks</span></span>

<span data-ttu-id="59ccf-114">Il controllo Rich Edit non controlla se la nuova tavolozza è valida.</span><span class="sxs-lookup"><span data-stu-id="59ccf-114">The rich edit control does not check whether the new palette is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="59ccf-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59ccf-115">Requirements</span></span>



| <span data-ttu-id="59ccf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="59ccf-116">Requirement</span></span> | <span data-ttu-id="59ccf-117">Valore</span><span class="sxs-lookup"><span data-stu-id="59ccf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59ccf-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59ccf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="59ccf-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59ccf-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59ccf-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59ccf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="59ccf-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="59ccf-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59ccf-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59ccf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="59ccf-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="59ccf-123"><dt>Richedit.h</dt></span></span> </dl> |



 

 






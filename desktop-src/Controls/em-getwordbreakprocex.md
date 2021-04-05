---
title: Messaggio di EM_GETWORDBREAKPROCEX (RichEdit. h)
description: Recupera l'indirizzo della routine di Word breaker estesa attualmente registrata per un controllo Rich Edit.
ms.assetid: 391681b6-fba9-4fc8-8778-3b3bd45ee5d6
keywords:
- Controlli di Windows Message EM_GETWORDBREAKPROCEX
topic_type:
- apiref
api_name:
- EM_GETWORDBREAKPROCEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890ef921a33dc387b17fddaa504bd15fa61ac505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874237"
---
# <a name="em_getwordbreakprocex-message"></a><span data-ttu-id="f9a26-104">\_Messaggio GETWORDBREAKPROCEX em</span><span class="sxs-lookup"><span data-stu-id="f9a26-104">EM\_GETWORDBREAKPROCEX message</span></span>

<span data-ttu-id="f9a26-105">Recupera l'indirizzo della routine di Word breaker estesa attualmente registrata per un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="f9a26-105">Retrieves the address of the currently registered extended word-break procedure for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9a26-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9a26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9a26-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9a26-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9a26-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f9a26-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f9a26-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9a26-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9a26-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f9a26-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9a26-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9a26-111">Return value</span></span>

<span data-ttu-id="f9a26-112">Il messaggio restituisce l'indirizzo della routine corrente.</span><span class="sxs-lookup"><span data-stu-id="f9a26-112">The message returns the address of the current procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9a26-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9a26-113">Requirements</span></span>



| <span data-ttu-id="f9a26-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9a26-114">Requirement</span></span> | <span data-ttu-id="f9a26-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f9a26-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9a26-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9a26-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f9a26-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9a26-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9a26-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9a26-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f9a26-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f9a26-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9a26-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9a26-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9a26-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9a26-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 






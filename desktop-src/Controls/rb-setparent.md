---
title: Messaggio RB_SETPARENT (COMmctrl. h)
description: Imposta la finestra padre di un controllo Rebar.
ms.assetid: bb8036d4-cab8-4887-86c6-66460bdbe64b
keywords:
- Controlli di Windows Message RB_SETPARENT
topic_type:
- apiref
api_name:
- RB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6fafd054d9438b6aedd268620097847b42f3d60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874146"
---
# <a name="rb_setparent-message"></a><span data-ttu-id="04877-104">\_Messaggio padre RB</span><span class="sxs-lookup"><span data-stu-id="04877-104">RB\_SETPARENT message</span></span>

<span data-ttu-id="04877-105">Imposta la finestra padre di un controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="04877-105">Sets a rebar control's parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="04877-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="04877-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04877-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04877-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04877-108">Handle per la finestra padre da impostare.</span><span class="sxs-lookup"><span data-stu-id="04877-108">Handle to the parent window to be set.</span></span>

</dd> <dt>

<span data-ttu-id="04877-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04877-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="04877-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="04877-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04877-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04877-111">Return value</span></span>

<span data-ttu-id="04877-112">Restituisce l'handle per la finestra padre precedente oppure **null** se non è presente alcun elemento padre precedente.</span><span class="sxs-lookup"><span data-stu-id="04877-112">Returns the handle to the previous parent window, or **NULL** if there is no previous parent.</span></span>

## <a name="remarks"></a><span data-ttu-id="04877-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="04877-113">Remarks</span></span>

<span data-ttu-id="04877-114">Il controllo Rebar invia messaggi di notifica alla finestra specificata con questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="04877-114">The rebar control sends notification messages to the window you specify with this message.</span></span> <span data-ttu-id="04877-115">Questo messaggio non modifica effettivamente l'elemento padre del controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="04877-115">This message does not actually change the parent of the rebar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="04877-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04877-116">Requirements</span></span>



| <span data-ttu-id="04877-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="04877-117">Requirement</span></span> | <span data-ttu-id="04877-118">Valore</span><span class="sxs-lookup"><span data-stu-id="04877-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04877-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04877-119">Minimum supported client</span></span><br/> | <span data-ttu-id="04877-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04877-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="04877-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04877-121">Minimum supported server</span></span><br/> | <span data-ttu-id="04877-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="04877-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="04877-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04877-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="04877-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="04877-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






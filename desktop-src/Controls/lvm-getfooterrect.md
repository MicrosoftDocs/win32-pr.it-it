---
title: Messaggio LVM_GETFOOTERRECT (COMmctrl. h)
description: Recupera le coordinate del piè di pagina per un controllo visualizzazione elenco. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetFooterRect di ListView.
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- Controlli di Windows Message LVM_GETFOOTERRECT
topic_type:
- apiref
api_name:
- LVM_GETFOOTERRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31df3a1b7b29e5ad9191da9e990e04daec99e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118999"
---
# <a name="lvm_getfooterrect-message"></a><span data-ttu-id="a9ada-105">\_Messaggio GETFOOTERRECT LVM</span><span class="sxs-lookup"><span data-stu-id="a9ada-105">LVM\_GETFOOTERRECT message</span></span>

<span data-ttu-id="a9ada-106">Recupera le coordinate del piè di pagina per un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="a9ada-106">Retrieves the coordinates of the footer for a list-view control.</span></span> <span data-ttu-id="a9ada-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetFooterRect di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) .</span><span class="sxs-lookup"><span data-stu-id="a9ada-107">Send this message explicitly or by using the [**ListView\_GetFooterRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a9ada-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9ada-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9ada-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9ada-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9ada-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a9ada-110">Not used.</span></span> <span data-ttu-id="a9ada-111">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="a9ada-111">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="a9ada-112">*lParam* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a9ada-112">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9ada-113">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) per ricevere le coordinate.</span><span class="sxs-lookup"><span data-stu-id="a9ada-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="a9ada-114">Il processo chiamante è responsabile dell'allocazione di questa struttura.</span><span class="sxs-lookup"><span data-stu-id="a9ada-114">The calling process is responsible for allocating this structure.</span></span> <span data-ttu-id="a9ada-115">Le coordinate ricevute sono espresse come coordinate client.</span><span class="sxs-lookup"><span data-stu-id="a9ada-115">The coordinates received are expressed as client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9ada-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9ada-116">Return value</span></span>

<span data-ttu-id="a9ada-117">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a9ada-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9ada-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9ada-118">Requirements</span></span>



| <span data-ttu-id="a9ada-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9ada-119">Requirement</span></span> | <span data-ttu-id="a9ada-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a9ada-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ada-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9ada-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a9ada-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a9ada-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a9ada-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9ada-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a9ada-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a9ada-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a9ada-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9ada-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9ada-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9ada-126"><dt>Commctrl.h</dt></span></span> </dl> |



 


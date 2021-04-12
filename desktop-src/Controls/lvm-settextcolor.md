---
title: Messaggio LVM_SETTEXTCOLOR (COMmctrl. h)
description: Imposta il colore del testo di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetTextColor di ListView.
ms.assetid: ff90c18b-0cd7-4331-bcd8-61044e891d1f
keywords:
- Controlli di Windows Message LVM_SETTEXTCOLOR
topic_type:
- apiref
api_name:
- LVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b30c965bd523cd5638c894b47fc4785ffbdd09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119462"
---
# <a name="lvm_settextcolor-message"></a><span data-ttu-id="1ae50-105">\_Messaggio SETTEXTCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="1ae50-105">LVM\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="1ae50-106">Imposta il colore del testo di un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="1ae50-106">Sets the text color of a list-view control.</span></span> <span data-ttu-id="1ae50-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetTextColor di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) .</span><span class="sxs-lookup"><span data-stu-id="1ae50-107">You can send this message explicitly or by using the [**ListView\_SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ae50-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ae50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ae50-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ae50-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1ae50-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1ae50-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1ae50-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ae50-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ae50-112">Oggetto [**COLORREF**](/windows/desktop/gdi/colorref) che specifica il nuovo colore del testo.</span><span class="sxs-lookup"><span data-stu-id="1ae50-112">A [**COLORREF**](/windows/desktop/gdi/colorref) that specifies the new text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ae50-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ae50-113">Return value</span></span>

<span data-ttu-id="1ae50-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1ae50-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ae50-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ae50-115">Requirements</span></span>



| <span data-ttu-id="1ae50-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ae50-116">Requirement</span></span> | <span data-ttu-id="1ae50-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1ae50-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae50-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ae50-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1ae50-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ae50-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ae50-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ae50-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1ae50-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1ae50-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ae50-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ae50-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ae50-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ae50-123"><dt>Commctrl.h</dt></span></span> </dl> |



 


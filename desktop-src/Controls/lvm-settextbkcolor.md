---
title: Messaggio LVM_SETTEXTBKCOLOR (COMmctrl. h)
description: Imposta il colore di sfondo del testo in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetTextBkColor di ListView.
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- Controlli di Windows Message LVM_SETTEXTBKCOLOR
topic_type:
- apiref
api_name:
- LVM_SETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2247dfd04d90c2b9eacadcb1c38608f519540fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048196"
---
# <a name="lvm_settextbkcolor-message"></a><span data-ttu-id="43f27-105">\_Messaggio SETTEXTBKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="43f27-105">LVM\_SETTEXTBKCOLOR message</span></span>

<span data-ttu-id="43f27-106">Imposta il colore di sfondo del testo in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="43f27-106">Sets the background color of text in a list-view control.</span></span> <span data-ttu-id="43f27-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetTextBkColor di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="43f27-107">You can send this message explicitly or by using the [**ListView\_SetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="43f27-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="43f27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43f27-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43f27-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="43f27-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="43f27-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="43f27-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43f27-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43f27-112">Nuovo colore di sfondo del testo.</span><span class="sxs-lookup"><span data-stu-id="43f27-112">New text background color.</span></span> <span data-ttu-id="43f27-113">Può essere CLR \_ None per nessun colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="43f27-113">This can be CLR\_NONE for no background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43f27-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43f27-114">Return value</span></span>

<span data-ttu-id="43f27-115">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="43f27-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="43f27-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43f27-116">Requirements</span></span>



| <span data-ttu-id="43f27-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="43f27-117">Requirement</span></span> | <span data-ttu-id="43f27-118">Valore</span><span class="sxs-lookup"><span data-stu-id="43f27-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43f27-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43f27-119">Minimum supported client</span></span><br/> | <span data-ttu-id="43f27-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43f27-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43f27-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43f27-121">Minimum supported server</span></span><br/> | <span data-ttu-id="43f27-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="43f27-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43f27-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43f27-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="43f27-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="43f27-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






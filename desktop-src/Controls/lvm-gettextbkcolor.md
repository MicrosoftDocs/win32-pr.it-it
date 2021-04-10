---
title: Messaggio LVM_GETTEXTBKCOLOR (COMmctrl. h)
description: Recupera il colore di sfondo del testo di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetTextBkColor di ListView.
ms.assetid: 3d2c8be8-d7f9-4aa7-b358-f7effc6dbb25
keywords:
- Controlli di Windows Message LVM_GETTEXTBKCOLOR
topic_type:
- apiref
api_name:
- LVM_GETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bf5b6700904c5af47ef47e749dfa753c5ff8cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964737"
---
# <a name="lvm_gettextbkcolor-message"></a><span data-ttu-id="af6a5-105">\_Messaggio GETTEXTBKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="af6a5-105">LVM\_GETTEXTBKCOLOR message</span></span>

<span data-ttu-id="af6a5-106">Recupera il colore di sfondo del testo di un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="af6a5-106">Retrieves the text background color of a list-view control.</span></span> <span data-ttu-id="af6a5-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetTextBkColor di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="af6a5-107">You can send this message explicitly or by using the [**ListView\_GetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="af6a5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="af6a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af6a5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af6a5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="af6a5-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="af6a5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="af6a5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af6a5-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="af6a5-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="af6a5-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af6a5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af6a5-113">Return value</span></span>

<span data-ttu-id="af6a5-114">Restituisce il colore di sfondo del testo.</span><span class="sxs-lookup"><span data-stu-id="af6a5-114">Returns the background color of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="af6a5-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af6a5-115">Requirements</span></span>



| <span data-ttu-id="af6a5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="af6a5-116">Requirement</span></span> | <span data-ttu-id="af6a5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="af6a5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af6a5-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af6a5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="af6a5-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af6a5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af6a5-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af6a5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="af6a5-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af6a5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af6a5-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af6a5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="af6a5-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="af6a5-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






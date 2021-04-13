---
title: Messaggio LVM_GETBKCOLOR (COMmctrl. h)
description: Ottiene il colore di sfondo di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetBkColor di ListView.
ms.assetid: 077d3b2e-f6d1-4acc-b002-e9e707ad274c
keywords:
- Controlli di Windows Message LVM_GETBKCOLOR
topic_type:
- apiref
api_name:
- LVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4329adda75677d1cc0126eaa0196fadf143cd0b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475184"
---
# <a name="lvm_getbkcolor-message"></a><span data-ttu-id="7e81f-105">\_Messaggio GETBKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="7e81f-105">LVM\_GETBKCOLOR message</span></span>

<span data-ttu-id="7e81f-106">Ottiene il colore di sfondo di un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="7e81f-106">Gets the background color of a list-view control.</span></span> <span data-ttu-id="7e81f-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetBkColor di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="7e81f-107">You can send this message explicitly or by using the [**ListView\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e81f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e81f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e81f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e81f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7e81f-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7e81f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7e81f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e81f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7e81f-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7e81f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e81f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7e81f-113">Return value</span></span>

<span data-ttu-id="7e81f-114">Restituisce il colore di sfondo del controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="7e81f-114">Returns the background color of the list-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e81f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e81f-115">Requirements</span></span>



| <span data-ttu-id="7e81f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e81f-116">Requirement</span></span> | <span data-ttu-id="7e81f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7e81f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e81f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e81f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7e81f-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7e81f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e81f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e81f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7e81f-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7e81f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e81f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7e81f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e81f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e81f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






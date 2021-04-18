---
title: Messaggio LVM_GETTEXTCOLOR (COMmctrl. h)
description: Recupera il colore del testo di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetTextColor di ListView.
ms.assetid: 51685e61-dd0a-4c21-8c66-31cf72c2b3e4
keywords:
- Controlli di Windows Message LVM_GETTEXTCOLOR
topic_type:
- apiref
api_name:
- LVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7686e8f06f49dbfc14899f47ba52017daaf23c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302291"
---
# <a name="lvm_gettextcolor-message"></a><span data-ttu-id="9ce78-105">\_Messaggio GETTEXTCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="9ce78-105">LVM\_GETTEXTCOLOR message</span></span>

<span data-ttu-id="9ce78-106">Recupera il colore del testo di un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="9ce78-106">Retrieves the text color of a list-view control.</span></span> <span data-ttu-id="9ce78-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetTextColor di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextcolor) .</span><span class="sxs-lookup"><span data-stu-id="9ce78-107">You can send this message explicitly or by using the [**ListView\_GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9ce78-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ce78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ce78-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ce78-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9ce78-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9ce78-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9ce78-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ce78-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9ce78-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9ce78-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ce78-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ce78-113">Return value</span></span>

<span data-ttu-id="9ce78-114">Restituisce il colore del testo.</span><span class="sxs-lookup"><span data-stu-id="9ce78-114">Returns the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ce78-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ce78-115">Requirements</span></span>



| <span data-ttu-id="9ce78-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ce78-116">Requirement</span></span> | <span data-ttu-id="9ce78-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9ce78-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ce78-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ce78-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9ce78-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ce78-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9ce78-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ce78-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9ce78-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9ce78-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ce78-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ce78-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ce78-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ce78-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






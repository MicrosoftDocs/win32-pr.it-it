---
title: Messaggio LVM_SETBKCOLOR (COMmctrl. h)
description: Imposta il colore di sfondo di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetBkColor di ListView.
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- Controlli di Windows Message LVM_SETBKCOLOR
topic_type:
- apiref
api_name:
- LVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80977ed6c95a1353889265e52cfc05c26aaa2a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964472"
---
# <a name="lvm_setbkcolor-message"></a><span data-ttu-id="4a71a-105">\_Messaggio SETBKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="4a71a-105">LVM\_SETBKCOLOR message</span></span>

<span data-ttu-id="4a71a-106">Imposta il colore di sfondo di un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="4a71a-106">Sets the background color of a list-view control.</span></span> <span data-ttu-id="4a71a-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetBkColor di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="4a71a-107">You can send this message explicitly or by using the [**ListView\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a71a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a71a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a71a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a71a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4a71a-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4a71a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4a71a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a71a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a71a-112">Colore di sfondo da impostare o \_ valore CLR None per nessun colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="4a71a-112">Background color to set or the CLR\_NONE value for no background color.</span></span> <span data-ttu-id="4a71a-113">I controlli visualizzazione elenco con i colori di sfondo si ritraggono molto più velocemente rispetto a quelli senza colori di sfondo.</span><span class="sxs-lookup"><span data-stu-id="4a71a-113">List-view controls with background colors redraw themselves significantly faster than those without background colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a71a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a71a-114">Return value</span></span>

<span data-ttu-id="4a71a-115">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4a71a-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a71a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a71a-116">Requirements</span></span>



| <span data-ttu-id="4a71a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a71a-117">Requirement</span></span> | <span data-ttu-id="4a71a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4a71a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a71a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a71a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4a71a-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a71a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a71a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a71a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4a71a-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4a71a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a71a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a71a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a71a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a71a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






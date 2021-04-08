---
title: Messaggio LVM_GETBKIMAGE (COMmctrl. h)
description: Ottiene l'immagine di sfondo in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetBkImage di ListView.
ms.assetid: db0e8f31-746a-4a16-b689-68da696e3657
keywords:
- Controlli di Windows Message LVM_GETBKIMAGE
topic_type:
- apiref
api_name:
- LVM_GETBKIMAGE
- LVM_GETBKIMAGEA
- LVM_GETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e178bae10b9bed880213ca4a4ab2a1b4e07239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739959"
---
# <a name="lvm_getbkimage-message"></a><span data-ttu-id="7a857-105">\_Messaggio GETBKIMAGE LVM</span><span class="sxs-lookup"><span data-stu-id="7a857-105">LVM\_GETBKIMAGE message</span></span>

<span data-ttu-id="7a857-106">Ottiene l'immagine di sfondo in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="7a857-106">Gets the background image in a list-view control.</span></span> <span data-ttu-id="7a857-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetBkImage di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) .</span><span class="sxs-lookup"><span data-stu-id="7a857-107">You can send this message explicitly or by using the [**ListView\_GetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7a857-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a857-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a857-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a857-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7a857-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7a857-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7a857-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a857-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a857-112">Puntatore a una struttura [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) che riceverà le informazioni sull'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="7a857-112">A pointer to an [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure that will receive the background image information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a857-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a857-113">Return value</span></span>

<span data-ttu-id="7a857-114">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7a857-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a857-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a857-115">Requirements</span></span>



| <span data-ttu-id="7a857-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a857-116">Requirement</span></span> | <span data-ttu-id="7a857-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7a857-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a857-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a857-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7a857-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a857-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7a857-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a857-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7a857-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7a857-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7a857-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a857-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a857-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a857-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7a857-124">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="7a857-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7a857-125">**LVM \_ GETBKIMAGEW** (Unicode) e **LVM \_ GETBKIMAGEA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7a857-125">**LVM\_GETBKIMAGEW** (Unicode) and **LVM\_GETBKIMAGEA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="7a857-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a857-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a857-127">**\_SETBKIMAGE LVM**</span><span class="sxs-lookup"><span data-stu-id="7a857-127">**LVM\_SETBKIMAGE**</span></span>](lvm-setbkimage.md)
</dt> </dl>

 

 






---
title: Messaggio LVM_GETSTRINGWIDTH (COMmctrl. h)
description: Determina la larghezza di una stringa specificata usando il tipo di carattere corrente del controllo visualizzazione elenco specificato. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetStringWidth di ListView.
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- Controlli di Windows Message LVM_GETSTRINGWIDTH
topic_type:
- apiref
api_name:
- LVM_GETSTRINGWIDTH
- LVM_GETSTRINGWIDTHA
- LVM_GETSTRINGWIDTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e27512eb7a2a260976356ed2a128b48975f9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518652"
---
# <a name="lvm_getstringwidth-message"></a><span data-ttu-id="3222b-105">\_Messaggio GETSTRINGWIDTH LVM</span><span class="sxs-lookup"><span data-stu-id="3222b-105">LVM\_GETSTRINGWIDTH message</span></span>

<span data-ttu-id="3222b-106">Determina la larghezza di una stringa specificata usando il tipo di carattere corrente del controllo visualizzazione elenco specificato.</span><span class="sxs-lookup"><span data-stu-id="3222b-106">Determines the width of a specified string using the specified list-view control's current font.</span></span> <span data-ttu-id="3222b-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetStringWidth di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) .</span><span class="sxs-lookup"><span data-stu-id="3222b-107">You can send this message explicitly or by using the [**ListView\_GetStringWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3222b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3222b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3222b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3222b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3222b-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3222b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3222b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3222b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3222b-112">Puntatore a una stringa con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="3222b-112">Pointer to a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3222b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3222b-113">Return value</span></span>

<span data-ttu-id="3222b-114">Restituisce la larghezza della stringa in caso di esito positivo; in caso contrario, zero.</span><span class="sxs-lookup"><span data-stu-id="3222b-114">Returns the string width if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3222b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3222b-115">Remarks</span></span>

<span data-ttu-id="3222b-116">Il \_ messaggio LVM GETSTRINGWIDTH restituisce la larghezza esatta, in pixel, della stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="3222b-116">The LVM\_GETSTRINGWIDTH message returns the exact width, in pixels, of the specified string.</span></span> <span data-ttu-id="3222b-117">Se si usa la larghezza della stringa restituita come larghezza della colonna nel messaggio [**LVM \_ SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) , la stringa verrà troncata.</span><span class="sxs-lookup"><span data-stu-id="3222b-117">If you use the returned string width as the column width in the [**LVM\_SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) message, the string will be truncated.</span></span> <span data-ttu-id="3222b-118">Per recuperare la larghezza della colonna che può contenere la stringa senza troncarla, è necessario aggiungere la spaziatura interna alla lunghezza della stringa restituita.</span><span class="sxs-lookup"><span data-stu-id="3222b-118">To retrieve the column width that can contain the string without truncating it, you must add padding to the returned string width.</span></span>

## <a name="requirements"></a><span data-ttu-id="3222b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3222b-119">Requirements</span></span>



| <span data-ttu-id="3222b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3222b-120">Requirement</span></span> | <span data-ttu-id="3222b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3222b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3222b-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3222b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3222b-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3222b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3222b-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3222b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3222b-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3222b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3222b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3222b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3222b-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3222b-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="3222b-128">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="3222b-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3222b-129">**LVM \_ GETSTRINGWIDTHW** (Unicode) e **LVM \_ GETSTRINGWIDTHA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3222b-129">**LVM\_GETSTRINGWIDTHW** (Unicode) and **LVM\_GETSTRINGWIDTHA** (ANSI)</span></span><br/>     |



 

 






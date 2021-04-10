---
title: Messaggio EM_ENABLESEARCHWEB (CommCtrl. h)
description: Abilita o Disabilita la funzionalità "Cerca sul Web" e la voce del menu di scelta rapida.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- Controlli di Windows Message EM_ENABLESEARCHWEB
topic_type:
- apiref
api_name:
- EM_ENABLESEARCHWEB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb2638476027f0a7fe2bb1a66a3a00a330e28c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964478"
---
# <a name="em_enablesearchweb-message"></a><span data-ttu-id="0eb44-104">\_Messaggio ENABLESEARCHWEB em</span><span class="sxs-lookup"><span data-stu-id="0eb44-104">EM\_ENABLESEARCHWEB message</span></span>

<span data-ttu-id="0eb44-105">Abilita o Disabilita la funzionalità "Cerca sul Web" e la voce del menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="0eb44-105">Enables or disables the "Search the web" feature and context menu entry.</span></span>

## <a name="parameters"></a><span data-ttu-id="0eb44-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0eb44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0eb44-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0eb44-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0eb44-108">Il valore **true** indica che è abilitata la funzionalità "Cerca sul Web" e il valore **false** indica che è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0eb44-108">A value of **TRUE** indicates the "Search the web" feature is enabled, and a value of **FALSE** indicates it is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="0eb44-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0eb44-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0eb44-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="0eb44-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0eb44-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0eb44-111">Return value</span></span>

<span data-ttu-id="0eb44-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="0eb44-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0eb44-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0eb44-113">Remarks</span></span>

<span data-ttu-id="0eb44-114">Se si disattiva "Cerca sul Web" utilizzando questo messaggio, il [**messaggio \_ SEARCHWEB em**](em-searchweb.md) non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="0eb44-114">If you disable "Search the web" using this message, the [**EM\_SEARCHWEB**](em-searchweb.md) message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="0eb44-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0eb44-115">Requirements</span></span>



| <span data-ttu-id="0eb44-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0eb44-116">Requirement</span></span> | <span data-ttu-id="0eb44-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0eb44-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0eb44-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0eb44-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0eb44-119">Solo app desktop Windows 10, 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="0eb44-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0eb44-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0eb44-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0eb44-121">\[Solo app desktop Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="0eb44-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0eb44-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0eb44-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0eb44-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0eb44-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0eb44-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0eb44-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="0eb44-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="0eb44-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0eb44-126">**\_SEARCHWEB em**</span><span class="sxs-lookup"><span data-stu-id="0eb44-126">**EM\_SEARCHWEB**</span></span>](em-searchweb.md)
</dt> </dl>

 

 






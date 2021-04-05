---
title: Messaggio EM_GETTHUMB (winuser. h)
description: Ottiene la posizione della casella di scorrimento (Thumb) nella barra di scorrimento verticale di un controllo di modifica su più righe. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 04bd0102-1652-405b-8c42-50e138abaf75
keywords:
- Controlli di Windows Message EM_GETTHUMB
topic_type:
- apiref
api_name:
- EM_GETTHUMB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6689c530794e11897f1f88a7d5864058d53aa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120726"
---
# <a name="em_getthumb-message"></a><span data-ttu-id="d9f9b-105">\_Messaggio GETTHUMB em</span><span class="sxs-lookup"><span data-stu-id="d9f9b-105">EM\_GETTHUMB message</span></span>

<span data-ttu-id="d9f9b-106">Ottiene la posizione della casella di scorrimento (Thumb) nella barra di scorrimento verticale di un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="d9f9b-106">Gets the position of the scroll box (thumb) in the vertical scroll bar of a multiline edit control.</span></span> <span data-ttu-id="d9f9b-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d9f9b-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9f9b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9f9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9f9b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9f9b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9f9b-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d9f9b-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d9f9b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9f9b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9f9b-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d9f9b-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9f9b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9f9b-113">Return value</span></span>

<span data-ttu-id="d9f9b-114">Il valore restituito è la posizione della casella di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="d9f9b-114">The return value is the position of the scroll box.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9f9b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9f9b-115">Remarks</span></span>

<span data-ttu-id="d9f9b-116">**Modifica avanzata:** Supportato in Microsoft Rich Edit 2,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="d9f9b-116">**Rich Edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="d9f9b-117">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="d9f9b-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f9b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9f9b-118">Requirements</span></span>



| <span data-ttu-id="d9f9b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9f9b-119">Requirement</span></span> | <span data-ttu-id="d9f9b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d9f9b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f9b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9f9b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d9f9b-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9f9b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d9f9b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9f9b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d9f9b-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d9f9b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d9f9b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9f9b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9f9b-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9f9b-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 






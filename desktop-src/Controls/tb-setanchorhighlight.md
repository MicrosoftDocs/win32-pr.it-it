---
title: Messaggio TB_SETANCHORHIGHLIGHT (COMmctrl. h)
description: Imposta l'impostazione dell'evidenziazione di ancoraggio per una barra degli strumenti.
ms.assetid: d31652d5-e9cf-4bf3-8f90-818eb078fa87
keywords:
- Controlli di Windows Message TB_SETANCHORHIGHLIGHT
topic_type:
- apiref
api_name:
- TB_SETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 809f71e446f7768d637258152db1dd2d56346dfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300974"
---
# <a name="tb_setanchorhighlight-message"></a><span data-ttu-id="e980a-104">TB \_ SETANCHORHIGHLIGHT messaggio</span><span class="sxs-lookup"><span data-stu-id="e980a-104">TB\_SETANCHORHIGHLIGHT message</span></span>

<span data-ttu-id="e980a-105">Imposta l'impostazione dell'evidenziazione di ancoraggio per una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="e980a-105">Sets the anchor highlight setting for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="e980a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e980a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e980a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e980a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e980a-108">Valore **bool** che specifica se l'evidenziazione dell'ancoraggio è abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="e980a-108">**BOOL** value that specifies if anchor highlighting is enabled or disabled.</span></span> <span data-ttu-id="e980a-109">Se questo valore è diverso da zero, verrà abilitata l'evidenziazione dell'ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="e980a-109">If this value is nonzero, anchor highlighting will be enabled.</span></span> <span data-ttu-id="e980a-110">Se questo valore è zero, l'evidenziazione dell'ancoraggio verrà disabilitata.</span><span class="sxs-lookup"><span data-stu-id="e980a-110">If this value is zero, anchor highlighting will be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="e980a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e980a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e980a-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e980a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e980a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e980a-113">Return value</span></span>

<span data-ttu-id="e980a-114">Restituisce l'impostazione di evidenziazione dell'ancoraggio precedente.</span><span class="sxs-lookup"><span data-stu-id="e980a-114">Returns the previous anchor highlight setting.</span></span> <span data-ttu-id="e980a-115">Se questo valore è diverso da zero, è stata abilitata l'evidenziazione di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="e980a-115">If this value is nonzero, anchor highlighting was enabled.</span></span> <span data-ttu-id="e980a-116">Se questo valore è zero, l'evidenziazione dell'ancoraggio è stata disabilitata.</span><span class="sxs-lookup"><span data-stu-id="e980a-116">If this value is zero, anchor highlighting was disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="e980a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e980a-117">Remarks</span></span>

<span data-ttu-id="e980a-118">L'evidenziazione dell'ancoraggio in una barra degli strumenti indica che l'ultimo elemento evidenziato rimarrà evidenziato finché non viene evidenziato un altro elemento.</span><span class="sxs-lookup"><span data-stu-id="e980a-118">Anchor highlighting in a toolbar means that the last highlighted item will remain highlighted until another item is highlighted.</span></span> <span data-ttu-id="e980a-119">Ciò si verifica anche se il cursore esce dal controllo Toolbar.</span><span class="sxs-lookup"><span data-stu-id="e980a-119">This occurs even if the cursor leaves the toolbar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e980a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e980a-120">Requirements</span></span>



| <span data-ttu-id="e980a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e980a-121">Requirement</span></span> | <span data-ttu-id="e980a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e980a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e980a-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e980a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e980a-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e980a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e980a-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e980a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e980a-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e980a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e980a-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e980a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e980a-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e980a-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






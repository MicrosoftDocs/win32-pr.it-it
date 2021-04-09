---
title: Messaggio TB_SETEXTENDEDSTYLE (COMmctrl. h)
description: Imposta gli stili estesi per un controllo Toolbar.
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- Controlli di Windows Message TB_SETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- TB_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a540aaeff61bd81b649f0509e064a29282f598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120678"
---
# <a name="tb_setextendedstyle-message"></a><span data-ttu-id="d4f7a-104">TB \_ SETEXTENDEDSTYLE messaggio</span><span class="sxs-lookup"><span data-stu-id="d4f7a-104">TB\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="d4f7a-105">Imposta gli stili estesi per un controllo Toolbar.</span><span class="sxs-lookup"><span data-stu-id="d4f7a-105">Sets the extended styles for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d4f7a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4f7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4f7a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d4f7a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d4f7a-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d4f7a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d4f7a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4f7a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4f7a-110">Valore che specifica i nuovi stili estesi.</span><span class="sxs-lookup"><span data-stu-id="d4f7a-110">Value specifying the new extended styles.</span></span> <span data-ttu-id="d4f7a-111">Questo parametro può essere una combinazione di [stili estesi](toolbar-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="d4f7a-111">This parameter can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4f7a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4f7a-112">Return value</span></span>

<span data-ttu-id="d4f7a-113">Restituisce un **valore DWORD** che rappresenta gli stili estesi precedenti.</span><span class="sxs-lookup"><span data-stu-id="d4f7a-113">Returns a **DWORD** that represents the previous extended styles.</span></span> <span data-ttu-id="d4f7a-114">Questo valore può essere una combinazione di [stili estesi](toolbar-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="d4f7a-114">This value can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4f7a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4f7a-115">Requirements</span></span>



| <span data-ttu-id="d4f7a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4f7a-116">Requirement</span></span> | <span data-ttu-id="d4f7a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d4f7a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f7a-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4f7a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d4f7a-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d4f7a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d4f7a-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4f7a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d4f7a-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d4f7a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4f7a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4f7a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4f7a-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4f7a-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4f7a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4f7a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f7a-125">**TB \_ GETEXTENDEDSTYLE**</span><span class="sxs-lookup"><span data-stu-id="d4f7a-125">**TB\_GETEXTENDEDSTYLE**</span></span>](tb-getextendedstyle.md)
</dt> </dl>

 

 






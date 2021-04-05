---
title: Messaggio TB_GETEXTENDEDSTYLE (COMmctrl. h)
description: Recupera gli stili estesi per un controllo Toolbar.
ms.assetid: d9e31a8e-5e5a-4d2d-bc3b-65ac40e8592f
keywords:
- Controlli di Windows Message TB_GETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- TB_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80bc4f4ad45e5c1c75366e0890f3fd76ec1fa74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741210"
---
# <a name="tb_getextendedstyle-message"></a><span data-ttu-id="d4739-104">TB \_ GETEXTENDEDSTYLE messaggio</span><span class="sxs-lookup"><span data-stu-id="d4739-104">TB\_GETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="d4739-105">Recupera gli stili estesi per un controllo Toolbar.</span><span class="sxs-lookup"><span data-stu-id="d4739-105">Retrieves the extended styles for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d4739-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4739-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4739-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d4739-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d4739-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d4739-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d4739-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4739-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d4739-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d4739-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4739-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4739-111">Return value</span></span>

<span data-ttu-id="d4739-112">Restituisce un **valore DWORD** che rappresenta gli stili attualmente in uso per il controllo Toolbar.</span><span class="sxs-lookup"><span data-stu-id="d4739-112">Returns a **DWORD** that represents the styles currently in use for the toolbar control.</span></span> <span data-ttu-id="d4739-113">Questo valore può essere una combinazione di [stili estesi](toolbar-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="d4739-113">This value can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4739-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4739-114">Requirements</span></span>



| <span data-ttu-id="d4739-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4739-115">Requirement</span></span> | <span data-ttu-id="d4739-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d4739-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4739-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4739-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d4739-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d4739-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d4739-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4739-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d4739-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d4739-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4739-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4739-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4739-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4739-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4739-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4739-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4739-124">**TB \_ SETEXTENDEDSTYLE**</span><span class="sxs-lookup"><span data-stu-id="d4739-124">**TB\_SETEXTENDEDSTYLE**</span></span>](tb-setextendedstyle.md)
</dt> </dl>

 

 






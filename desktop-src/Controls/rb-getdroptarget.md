---
title: Messaggio RB_GETDROPTARGET (COMmctrl. h)
description: Recupera un puntatore all'interfaccia IDropTarget del controllo Rebar.
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- Controlli di Windows Message RB_GETDROPTARGET
topic_type:
- apiref
api_name:
- RB_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b7960cc13230a2715348bc55e5e65de6f72e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477872"
---
# <a name="rb_getdroptarget-message"></a><span data-ttu-id="ea14d-104">\_Messaggio GETDROPTARGET RB</span><span class="sxs-lookup"><span data-stu-id="ea14d-104">RB\_GETDROPTARGET message</span></span>

<span data-ttu-id="ea14d-105">Recupera un puntatore all'interfaccia [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) del controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="ea14d-105">Retrieves a rebar control's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface pointer.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea14d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea14d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea14d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea14d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea14d-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ea14d-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ea14d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea14d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea14d-110">Puntatore a un puntatore [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) che riceve il puntatore a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ea14d-110">Pointer to an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pointer that receives the interface pointer.</span></span> <span data-ttu-id="ea14d-111">È responsabilità del chiamante chiamare il [**rilascio**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su questo puntatore quando non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="ea14d-111">It is the caller's responsibility to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on this pointer when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea14d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea14d-112">Return value</span></span>

<span data-ttu-id="ea14d-113">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="ea14d-113">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea14d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea14d-114">Requirements</span></span>



| <span data-ttu-id="ea14d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea14d-115">Requirement</span></span> | <span data-ttu-id="ea14d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ea14d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea14d-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea14d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ea14d-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea14d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea14d-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea14d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ea14d-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ea14d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea14d-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea14d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea14d-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea14d-122"><dt>Commctrl.h</dt></span></span> </dl> |



 


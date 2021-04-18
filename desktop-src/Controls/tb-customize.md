---
title: Messaggio TB_CUSTOMIZE (COMmctrl. h)
description: Consente di visualizzare la finestra di dialogo Personalizza barra degli strumenti.
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- Controlli di Windows Message TB_CUSTOMIZE
topic_type:
- apiref
api_name:
- TB_CUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dada0ef195e898b7a46487a2d775e46d6af854ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302785"
---
# <a name="tb_customize-message"></a><span data-ttu-id="d27ba-104">TB \_ personalizzare il messaggio</span><span class="sxs-lookup"><span data-stu-id="d27ba-104">TB\_CUSTOMIZE message</span></span>

<span data-ttu-id="d27ba-105">Consente di visualizzare la finestra di dialogo **Personalizza barra degli strumenti** .</span><span class="sxs-lookup"><span data-stu-id="d27ba-105">Displays the **Customize Toolbar** dialog box.</span></span>

## <a name="parameters"></a><span data-ttu-id="d27ba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d27ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d27ba-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d27ba-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d27ba-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d27ba-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d27ba-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d27ba-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d27ba-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d27ba-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d27ba-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d27ba-111">Return value</span></span>

<span data-ttu-id="d27ba-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="d27ba-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d27ba-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d27ba-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d27ba-114">La barra degli strumenti deve gestire le notifiche [TBN \_ QUERYINSERT](tbn-queryinsert.md) e [TBN \_ QUERYDELETE](tbn-querydelete.md) per la visualizzazione della finestra di dialogo **Personalizza barra degli strumenti** .</span><span class="sxs-lookup"><span data-stu-id="d27ba-114">The toolbar must handle the [TBN\_QUERYINSERT](tbn-queryinsert.md) and [TBN\_QUERYDELETE](tbn-querydelete.md) notifications for the **Customize Toolbar** dialog box to appear.</span></span> <span data-ttu-id="d27ba-115">Se la barra degli strumenti non gestisce tali notifiche, **TB \_ Customize** non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="d27ba-115">If the toolbar does not handle those notifications, **TB\_CUSTOMIZE** has no effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d27ba-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d27ba-116">Requirements</span></span>



| <span data-ttu-id="d27ba-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d27ba-117">Requirement</span></span> | <span data-ttu-id="d27ba-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d27ba-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d27ba-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d27ba-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d27ba-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d27ba-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d27ba-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d27ba-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d27ba-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d27ba-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d27ba-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d27ba-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d27ba-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d27ba-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






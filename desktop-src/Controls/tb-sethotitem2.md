---
title: Messaggio TB_SETHOTITEM2 (COMmctrl. h)
description: Imposta l'elemento attivo in una barra degli strumenti.
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- Controlli di Windows Message TB_SETHOTITEM2
topic_type:
- apiref
api_name:
- TB_SETHOTITEM2
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7027920e4363b46fcc0b6d9b0d87129e01843318
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742650"
---
# <a name="tb_sethotitem2-message"></a><span data-ttu-id="a7b68-104">TB \_ SETHOTITEM2 messaggio</span><span class="sxs-lookup"><span data-stu-id="a7b68-104">TB\_SETHOTITEM2 message</span></span>

<span data-ttu-id="a7b68-105">Imposta l'elemento attivo in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="a7b68-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="a7b68-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7b68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7b68-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a7b68-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7b68-108">Indice dell'elemento che verrà reso attivo.</span><span class="sxs-lookup"><span data-stu-id="a7b68-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="a7b68-109">Se questo valore è-1, nessuno degli elementi sarà attivo.</span><span class="sxs-lookup"><span data-stu-id="a7b68-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="a7b68-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a7b68-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a7b68-111">Combinazione di flag HICF \_ xxx.</span><span class="sxs-lookup"><span data-stu-id="a7b68-111">A combination of HICF\_xxx flags.</span></span> <span data-ttu-id="a7b68-112">Vedere <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span><span class="sxs-lookup"><span data-stu-id="a7b68-112">See <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7b68-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7b68-113">Return value</span></span>

<span data-ttu-id="a7b68-114">Restituisce l'indice dell'elemento attivo precedente oppure-1 se non è presente alcun elemento attivo.</span><span class="sxs-lookup"><span data-stu-id="a7b68-114">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7b68-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7b68-115">Remarks</span></span>

<span data-ttu-id="a7b68-116">Il comportamento di questo messaggio non è definito per le barre degli strumenti che non hanno lo stile [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a7b68-116">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7b68-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7b68-117">Requirements</span></span>



| <span data-ttu-id="a7b68-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7b68-118">Requirement</span></span> | <span data-ttu-id="a7b68-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a7b68-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7b68-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7b68-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a7b68-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a7b68-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a7b68-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7b68-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a7b68-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a7b68-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a7b68-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7b68-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7b68-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7b68-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






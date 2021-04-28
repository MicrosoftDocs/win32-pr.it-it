---
title: TB_SETHOTITEM2 messaggio (Commctrl.h)
description: "TB_SETHOTITEM2 messaggio: imposta l'elemento di accesso rapido in una barra degli strumenti."
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- TB_SETHOTITEM2 messaggio Controlli Windows
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
ms.openlocfilehash: 7daf67839837adccfbec99bf03fc4dfff97738db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104139"
---
# <a name="tb_sethotitem2-message"></a><span data-ttu-id="0d4f8-104">TB \_ SETHOTITEM2 message</span><span class="sxs-lookup"><span data-stu-id="0d4f8-104">TB\_SETHOTITEM2 message</span></span>

<span data-ttu-id="0d4f8-105">Imposta l'elemento di accesso rapido in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="0d4f8-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d4f8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d4f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d4f8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d4f8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d4f8-108">Indice dell'elemento che verrà reso a caldo.</span><span class="sxs-lookup"><span data-stu-id="0d4f8-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="0d4f8-109">Se questo valore è -1, nessuno degli elementi sarà a caldo.</span><span class="sxs-lookup"><span data-stu-id="0d4f8-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="0d4f8-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d4f8-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0d4f8-111">Combinazione di flag HICF \_ xxx.</span><span class="sxs-lookup"><span data-stu-id="0d4f8-111">A combination of HICF\_xxx flags.</span></span> <span data-ttu-id="0d4f8-112">Vedere <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span><span class="sxs-lookup"><span data-stu-id="0d4f8-112">See <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d4f8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d4f8-113">Return value</span></span>

<span data-ttu-id="0d4f8-114">Restituisce l'indice dell'elemento a caldo precedente oppure -1 se non è presente alcun elemento a caldo.</span><span class="sxs-lookup"><span data-stu-id="0d4f8-114">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d4f8-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d4f8-115">Remarks</span></span>

<span data-ttu-id="0d4f8-116">Il comportamento di questo messaggio non è definito per le barre degli strumenti che non hanno lo [**stile TBSTYLE \_ FLAT.**](toolbar-control-and-button-styles.md)</span><span class="sxs-lookup"><span data-stu-id="0d4f8-116">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d4f8-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d4f8-117">Requirements</span></span>



| <span data-ttu-id="0d4f8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d4f8-118">Requirement</span></span> | <span data-ttu-id="0d4f8-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0d4f8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d4f8-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d4f8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0d4f8-121">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0d4f8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d4f8-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d4f8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0d4f8-123">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d4f8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d4f8-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d4f8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d4f8-125"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="0d4f8-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






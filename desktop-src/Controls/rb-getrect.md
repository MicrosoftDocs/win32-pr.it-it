---
title: Messaggio RB_GETRECT (COMmctrl. h)
description: Recupera il rettangolo di delimitazione per una determinata banda in un controllo Rebar.
ms.assetid: e272b090-1e4d-4cff-87f0-557ad8116e7e
keywords:
- Controlli di Windows Message RB_GETRECT
topic_type:
- apiref
api_name:
- RB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b9d5de00b638a3767df461595ff01316b23183
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225215"
---
# <a name="rb_getrect-message"></a><span data-ttu-id="f08b2-104">Messaggio di RB \_ GETrect</span><span class="sxs-lookup"><span data-stu-id="f08b2-104">RB\_GETRECT message</span></span>

<span data-ttu-id="f08b2-105">Recupera il rettangolo di delimitazione per una determinata banda in un controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="f08b2-105">Retrieves the bounding rectangle for a given band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f08b2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f08b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f08b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f08b2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f08b2-108">Indice in base zero di una banda nel controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="f08b2-108">Zero-based index of a band in the rebar control.</span></span>

</dd> <dt>

<span data-ttu-id="f08b2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f08b2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f08b2-110">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceverà i limiti della banda del controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="f08b2-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the bounds of the rebar band.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f08b2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f08b2-111">Return value</span></span>

<span data-ttu-id="f08b2-112">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f08b2-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f08b2-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f08b2-113">Requirements</span></span>



| <span data-ttu-id="f08b2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f08b2-114">Requirement</span></span> | <span data-ttu-id="f08b2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f08b2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f08b2-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f08b2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f08b2-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f08b2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f08b2-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f08b2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f08b2-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f08b2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f08b2-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f08b2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f08b2-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f08b2-121"><dt>Commctrl.h</dt></span></span> </dl> |



 


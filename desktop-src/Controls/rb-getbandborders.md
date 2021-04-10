---
title: Messaggio RB_GETBANDBORDERS (COMmctrl. h)
description: Recupera i bordi di una banda. Il risultato di questo messaggio può essere utilizzato per calcolare l'area utilizzabile di una banda.
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- Controlli di Windows Message RB_GETBANDBORDERS
topic_type:
- apiref
api_name:
- RB_GETBANDBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521dfecaf5e2573b30f606b7b4d7ecdec9bd896d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964552"
---
# <a name="rb_getbandborders-message"></a><span data-ttu-id="b34c8-105">\_Messaggio GETBANDBORDERS RB</span><span class="sxs-lookup"><span data-stu-id="b34c8-105">RB\_GETBANDBORDERS message</span></span>

<span data-ttu-id="b34c8-106">Recupera i bordi di una banda.</span><span class="sxs-lookup"><span data-stu-id="b34c8-106">Retrieves the borders of a band.</span></span> <span data-ttu-id="b34c8-107">Il risultato di questo messaggio può essere utilizzato per calcolare l'area utilizzabile di una banda.</span><span class="sxs-lookup"><span data-stu-id="b34c8-107">The result of this message can be used to calculate the usable area in a band.</span></span>

## <a name="parameters"></a><span data-ttu-id="b34c8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b34c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b34c8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b34c8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b34c8-110">Indice in base zero della banda per cui verranno recuperati i bordi.</span><span class="sxs-lookup"><span data-stu-id="b34c8-110">Zero-based index of the band for which the borders will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="b34c8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b34c8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b34c8-112">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceverà i bordi della banda.</span><span class="sxs-lookup"><span data-stu-id="b34c8-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the band borders.</span></span> <span data-ttu-id="b34c8-113">Se il controllo Rebar dispone dello [**stile \_ BANDBORDERS RBS**](rebar-control-styles.md) , ogni membro della struttura riceverà il numero di pixel, sul lato corrispondente della banda, che costituiscono il bordo.</span><span class="sxs-lookup"><span data-stu-id="b34c8-113">If the rebar control has the [**RBS\_BANDBORDERS**](rebar-control-styles.md) style, each member of this structure will receive the number of pixels, on the corresponding side of the band, that constitute the border.</span></span> <span data-ttu-id="b34c8-114">Se il controllo Rebar non dispone dello stile **\_ BANDBORDERS di RBS** , solo il membro **sinistro** di questa struttura riceve informazioni valide.</span><span class="sxs-lookup"><span data-stu-id="b34c8-114">If the rebar control does not have the **RBS\_BANDBORDERS** style, only the **left** member of this structure receives valid information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b34c8-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b34c8-115">Return value</span></span>

<span data-ttu-id="b34c8-116">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="b34c8-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b34c8-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b34c8-117">Requirements</span></span>



| <span data-ttu-id="b34c8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b34c8-118">Requirement</span></span> | <span data-ttu-id="b34c8-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b34c8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b34c8-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b34c8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b34c8-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b34c8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b34c8-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b34c8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b34c8-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b34c8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b34c8-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b34c8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b34c8-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b34c8-125"><dt>Commctrl.h</dt></span></span> </dl> |



 


---
title: Messaggio di EM_SETEDITSTYLE (RichEdit. h)
description: Imposta i flag di stile di modifica correnti per un controllo Rich Edit.
ms.assetid: e48de6b3-0fd2-4791-9863-a6dcdafa3642
keywords:
- Controlli di Windows Message EM_SETEDITSTYLE
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14c7b7e1d3990a00fb6931ed39bbd28aa6f8c2ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518670"
---
# <a name="em_seteditstyle-message"></a><span data-ttu-id="28831-104">\_Messaggio SETEDITSTYLE em</span><span class="sxs-lookup"><span data-stu-id="28831-104">EM\_SETEDITSTYLE message</span></span>

<span data-ttu-id="28831-105">Imposta i flag di stile di modifica correnti per un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="28831-105">Sets the current edit style flags for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="28831-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="28831-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28831-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="28831-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28831-108">Specifica uno o più flag di stile di modifica.</span><span class="sxs-lookup"><span data-stu-id="28831-108">Specifies one or more edit style flags.</span></span> <span data-ttu-id="28831-109">Per un elenco di valori possibili, vedere [**em \_ geteditname**](em-geteditstyle.md).</span><span class="sxs-lookup"><span data-stu-id="28831-109">For a list of possible values, see [**EM\_GETEDITSTYLE**](em-geteditstyle.md).</span></span>

</dd> <dt>

<span data-ttu-id="28831-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28831-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28831-111">Maschera costituita da uno o più valori *wParam* .</span><span class="sxs-lookup"><span data-stu-id="28831-111">A mask consisting of one or more of the *wParam* values.</span></span> <span data-ttu-id="28831-112">Verranno impostati o cancellati solo i valori specificati in questa maschera.</span><span class="sxs-lookup"><span data-stu-id="28831-112">Only the values specified in this mask will be set or cleared.</span></span> <span data-ttu-id="28831-113">In questo modo è possibile impostare o cancellare un flag singolo senza leggere gli Stati del flag corrente.</span><span class="sxs-lookup"><span data-stu-id="28831-113">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28831-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28831-114">Return value</span></span>

<span data-ttu-id="28831-115">Il valore restituito è lo stato dei flag di stile di modifica dopo che il controllo Rich Edit ha tentato di implementare le modifiche dello stile di modifica.</span><span class="sxs-lookup"><span data-stu-id="28831-115">The return value is the state of the edit style flags after the rich edit control has attempted to implement your edit style changes.</span></span> <span data-ttu-id="28831-116">I flag di stile di modifica sono un set di flag che indicano lo stile di modifica corrente.</span><span class="sxs-lookup"><span data-stu-id="28831-116">The edit style flags are a set of flags that indicate the current edit style.</span></span>

## <a name="requirements"></a><span data-ttu-id="28831-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28831-117">Requirements</span></span>



| <span data-ttu-id="28831-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="28831-118">Requirement</span></span> | <span data-ttu-id="28831-119">Valore</span><span class="sxs-lookup"><span data-stu-id="28831-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28831-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28831-120">Minimum supported client</span></span><br/> | <span data-ttu-id="28831-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28831-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="28831-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28831-122">Minimum supported server</span></span><br/> | <span data-ttu-id="28831-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="28831-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="28831-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="28831-124">Redistributable</span></span><br/>          | <span data-ttu-id="28831-125">Modifica avanzata 3,0</span><span class="sxs-lookup"><span data-stu-id="28831-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="28831-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28831-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="28831-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="28831-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28831-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28831-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28831-129">**\_geteditin em**</span><span class="sxs-lookup"><span data-stu-id="28831-129">**EM\_GETEDITSTYLE**</span></span>](em-geteditstyle.md)
</dt> </dl>

 

 






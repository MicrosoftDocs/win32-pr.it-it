---
title: Messaggio TB_GETITEMDROPDOWNRECT (COMmctrl. h)
description: Ottiene il rettangolo di delimitazione della finestra a discesa per un elemento della barra degli strumenti con stile \_ elenco a discesa BTNS.
ms.assetid: 4b59c96b-8d75-44c1-b771-c1d62502a2c2
keywords:
- Controlli di Windows Message TB_GETITEMDROPDOWNRECT
topic_type:
- apiref
api_name:
- TB_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbcef725b0ade0bfc776200fa5b191618d2ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047987"
---
# <a name="tb_getitemdropdownrect-message"></a><span data-ttu-id="594e4-104">TB \_ GETITEMDROPDOWNRECT messaggio</span><span class="sxs-lookup"><span data-stu-id="594e4-104">TB\_GETITEMDROPDOWNRECT message</span></span>

<span data-ttu-id="594e4-105">Ottiene il rettangolo di delimitazione della finestra a discesa per un elemento della barra degli strumenti con stile [**\_ elenco a discesa BTNS**](toolbar-control-and-button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="594e4-105">Gets the bounding rectangle of the dropdown window for a toolbar item with style [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="594e4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="594e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="594e4-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="594e4-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="594e4-108">Indice in base zero dell'elemento di controllo della barra degli strumenti per il quale recuperare il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="594e4-108">The zero-based index of the toolbar control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="594e4-109">*lParam* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="594e4-109">*lParam* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="594e4-110">Puntatore a una struttura <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> per ricevere le informazioni sul rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="594e4-110">A pointer to a <a href="/previous-versions//dd162897(v=vs.85)">**RECT**</a> structure to receive the bounding rectangle information.</span></span> <span data-ttu-id="594e4-111">Il mittente del messaggio è responsabile dell'allocazione della struttura.</span><span class="sxs-lookup"><span data-stu-id="594e4-111">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="594e4-112">Le coordinate restituite nella struttura **Rect** sono espresse come coordinate client.</span><span class="sxs-lookup"><span data-stu-id="594e4-112">The coordinates returned in the **RECT** structure are expressed as client coordinates.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="594e4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="594e4-113">Return value</span></span>

<span data-ttu-id="594e4-114">Restituisce sempre un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="594e4-114">Always returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="594e4-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="594e4-115">Remarks</span></span>

<span data-ttu-id="594e4-116">L'elemento deve avere lo stile a [**\_ discesa BTNS**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="594e4-116">The item must have the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="594e4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="594e4-117">Requirements</span></span>



| <span data-ttu-id="594e4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="594e4-118">Requirement</span></span> | <span data-ttu-id="594e4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="594e4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="594e4-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="594e4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="594e4-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="594e4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="594e4-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="594e4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="594e4-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="594e4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="594e4-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="594e4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="594e4-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="594e4-125"><dt>Commctrl.h</dt></span></span> </dl> |



 


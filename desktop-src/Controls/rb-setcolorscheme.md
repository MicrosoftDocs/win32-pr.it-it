---
title: Messaggio RB_SETCOLORSCHEME (COMmctrl. h)
description: Imposta le informazioni sulla combinazione di colori per il controllo Rebar.
ms.assetid: ddf8f3e4-66b7-4b53-a04e-b4dd372f71c4
keywords:
- Controlli di Windows Message RB_SETCOLORSCHEME
topic_type:
- apiref
api_name:
- RB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9c7725d3c0bc3f3a7a7a72db16e19626a3c4d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517962"
---
# <a name="rb_setcolorscheme-message"></a><span data-ttu-id="f2ebb-104">\_Messaggio SETCOLORSCHEME RB</span><span class="sxs-lookup"><span data-stu-id="f2ebb-104">RB\_SETCOLORSCHEME message</span></span>

<span data-ttu-id="f2ebb-105">Imposta le informazioni sulla combinazione di colori per il controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="f2ebb-105">Sets the color scheme information for the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2ebb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2ebb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2ebb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2ebb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f2ebb-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f2ebb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f2ebb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2ebb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2ebb-110">Puntatore a una struttura [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) che contiene le informazioni sulla combinazione di colori.</span><span class="sxs-lookup"><span data-stu-id="f2ebb-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that contains the color scheme information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2ebb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2ebb-111">Return value</span></span>

<span data-ttu-id="f2ebb-112">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="f2ebb-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2ebb-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2ebb-113">Remarks</span></span>

<span data-ttu-id="f2ebb-114">Il controllo Rebar utilizza le informazioni sulla combinazione di colori quando si disegnano gli elementi 3D nel controllo e nelle bande.</span><span class="sxs-lookup"><span data-stu-id="f2ebb-114">The rebar control uses the color scheme information when drawing the 3-D elements in the control and bands.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2ebb-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2ebb-115">Requirements</span></span>



| <span data-ttu-id="f2ebb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2ebb-116">Requirement</span></span> | <span data-ttu-id="f2ebb-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f2ebb-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ebb-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2ebb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f2ebb-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f2ebb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2ebb-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2ebb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f2ebb-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2ebb-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2ebb-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2ebb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2ebb-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2ebb-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2ebb-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2ebb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2ebb-125">**RB \_ GETCOLORSCHEME**</span><span class="sxs-lookup"><span data-stu-id="f2ebb-125">**RB\_GETCOLORSCHEME**</span></span>](rb-getcolorscheme.md)
</dt> </dl>

 

 






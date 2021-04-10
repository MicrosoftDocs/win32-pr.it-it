---
title: Messaggio di EM_GETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Restituisce lo stato corrente delle opzioni tipografiche di un controllo Rich Edit.
ms.assetid: 6ff5980e-3201-4b0f-9a03-3de78730ce33
keywords:
- Controlli di Windows Message EM_GETTYPOGRAPHYOPTIONS
topic_type:
- apiref
api_name:
- EM_GETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d692639ba6c8cea758abe694faed3a46e3f65be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120722"
---
# <a name="em_gettypographyoptions-message"></a><span data-ttu-id="1bfcb-104">\_Messaggio GETTYPOGRAPHYOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="1bfcb-104">EM\_GETTYPOGRAPHYOPTIONS message</span></span>

<span data-ttu-id="1bfcb-105">Restituisce lo stato corrente delle opzioni tipografiche di un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="1bfcb-105">Returns the current state of the typography options of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1bfcb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1bfcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bfcb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1bfcb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1bfcb-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1bfcb-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1bfcb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1bfcb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1bfcb-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1bfcb-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bfcb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1bfcb-111">Return value</span></span>

<span data-ttu-id="1bfcb-112">Restituisce le opzioni di tipografia correnti.</span><span class="sxs-lookup"><span data-stu-id="1bfcb-112">Returns the current typography options.</span></span> <span data-ttu-id="1bfcb-113">Per un elenco di opzioni, vedere [**em \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md).</span><span class="sxs-lookup"><span data-stu-id="1bfcb-113">For a list of options, see [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1bfcb-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1bfcb-114">Remarks</span></span>

<span data-ttu-id="1bfcb-115">È possibile attivare l'interruzioni di riga avanzate inviando il messaggio [**\_ SETTYPOGRAPHYOPTIONS em**](em-settypographyoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="1bfcb-115">You can turn on advanced line breaking by sending the [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md) message.</span></span> <span data-ttu-id="1bfcb-116">Le interruzioni di riga avanzate e normali possono anche essere attivate automaticamente dal controllo Rich Edit, se necessario per determinate lingue.</span><span class="sxs-lookup"><span data-stu-id="1bfcb-116">Advanced and normal line breaking may also be turned on automatically by the rich edit control if it is needed for certain languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bfcb-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1bfcb-117">Requirements</span></span>



| <span data-ttu-id="1bfcb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bfcb-118">Requirement</span></span> | <span data-ttu-id="1bfcb-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1bfcb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1bfcb-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1bfcb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1bfcb-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1bfcb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1bfcb-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1bfcb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1bfcb-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1bfcb-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1bfcb-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="1bfcb-124">Redistributable</span></span><br/>          | <span data-ttu-id="1bfcb-125">Modifica avanzata 3,0</span><span class="sxs-lookup"><span data-stu-id="1bfcb-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="1bfcb-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1bfcb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bfcb-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bfcb-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bfcb-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1bfcb-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="1bfcb-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="1bfcb-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1bfcb-130">**\_SETTYPOGRAPHYOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="1bfcb-130">**EM\_SETTYPOGRAPHYOPTIONS**</span></span>](em-settypographyoptions.md)
</dt> <dt>

<span data-ttu-id="1bfcb-131">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="1bfcb-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1bfcb-132">Informazioni sui controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="1bfcb-132">About Rich Edit Controls</span></span>](about-rich-edit-controls.md)
</dt> </dl>

 

 






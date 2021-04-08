---
title: Messaggio TVM_SETBORDER (COMmctrl. h)
description: Imposta la dimensione del bordo per gli elementi in un controllo di visualizzazione albero. È possibile inviare il messaggio in modo esplicito o usando la macro del bordo del controllo TreeView \_ .
ms.assetid: 468b46ae-2ab2-4753-a0af-7c644f75ce62
keywords:
- Controlli di Windows Message TVM_SETBORDER
topic_type:
- apiref
api_name:
- TVM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b4401959e2579caab7f2cb4b6eed1ea34481ffa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874013"
---
# <a name="tvm_setborder-message"></a><span data-ttu-id="a96c1-105">\_Messaggio di DEBORDO TVM</span><span class="sxs-lookup"><span data-stu-id="a96c1-105">TVM\_SETBORDER message</span></span>

<span data-ttu-id="a96c1-106">**Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni.**</span><span class="sxs-lookup"><span data-stu-id="a96c1-106">**Intended for internal use; not recommended for use in applications.**</span></span>

<span data-ttu-id="a96c1-107">Imposta la dimensione del bordo per gli elementi in un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="a96c1-107">Sets the size of the border for the items in a tree-view control.</span></span> <span data-ttu-id="a96c1-108">È possibile inviare il messaggio in modo esplicito o usando la macro del [**\_ bordo**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) del controllo TreeView.</span><span class="sxs-lookup"><span data-stu-id="a96c1-108">You can send the message explicitly or by using the [**TreeView\_SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a96c1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a96c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a96c1-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a96c1-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a96c1-111">Flag di azione.</span><span class="sxs-lookup"><span data-stu-id="a96c1-111">Action flags.</span></span> <span data-ttu-id="a96c1-112">Il parametro può essere costituito da uno o più dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a96c1-112">This parameter can be one or more of the following values:</span></span>



| <span data-ttu-id="a96c1-113">Valore</span><span class="sxs-lookup"><span data-stu-id="a96c1-113">Value</span></span>                                                                                                                                                         | <span data-ttu-id="a96c1-114">Significato</span><span class="sxs-lookup"><span data-stu-id="a96c1-114">Meaning</span></span>                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="TVSBF_XBORDER"></span><span id="tvsbf_xborder"></span><dl> <span data-ttu-id="a96c1-115"><dt>**\_XBORDER TVSBF**</dt></span><span class="sxs-lookup"><span data-stu-id="a96c1-115"><dt>**TVSBF\_XBORDER**</dt></span></span> </dl> | <span data-ttu-id="a96c1-116">Applica la dimensione del bordo specificata al lato sinistro degli elementi nel controllo di visualizzazione ad albero.</span><span class="sxs-lookup"><span data-stu-id="a96c1-116">Applies the specified border size to the left side of the items in the tree-view control.</span></span> <br/> |
| <span id="TVSBF_YBORDER"></span><span id="tvsbf_yborder"></span><dl> <span data-ttu-id="a96c1-117"><dt>**\_YBORDER TVSBF**</dt></span><span class="sxs-lookup"><span data-stu-id="a96c1-117"><dt>**TVSBF\_YBORDER**</dt></span></span> </dl> | <span data-ttu-id="a96c1-118">Applica le dimensioni del bordo specificate alla parte superiore degli elementi nel controllo di visualizzazione ad albero.</span><span class="sxs-lookup"><span data-stu-id="a96c1-118">Applies the specified border size to the top of the items in the tree-view control.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="a96c1-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a96c1-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a96c1-120">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un valore **short** che specifica la dimensione del bordo sinistro, in pixel.</span><span class="sxs-lookup"><span data-stu-id="a96c1-120">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **SHORT** that specifies the size of the left border, in pixels.</span></span> <span data-ttu-id="a96c1-121">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è un valore **short** che specifica la dimensione del bordo superiore, in pixel.</span><span class="sxs-lookup"><span data-stu-id="a96c1-121">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **SHORT** that specifies the size of the top border, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a96c1-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a96c1-122">Return value</span></span>

<span data-ttu-id="a96c1-123">Restituisce un valore **Long** che contiene le dimensioni del bordo precedenti, in pixel.</span><span class="sxs-lookup"><span data-stu-id="a96c1-123">Returns a **LONG** value that contains the previous border size, in pixels.</span></span> <span data-ttu-id="a96c1-124">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene le dimensioni precedenti del bordo orizzontale e il [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene le dimensioni precedenti del bordo verticale.</span><span class="sxs-lookup"><span data-stu-id="a96c1-124">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the previous size of the horizontal border, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the previous size of the vertical border.</span></span>

## <a name="remarks"></a><span data-ttu-id="a96c1-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="a96c1-125">Remarks</span></span>

<span data-ttu-id="a96c1-126">**Avviso di sicurezza:** L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.</span><span class="sxs-lookup"><span data-stu-id="a96c1-126">**Security Warning:** Using this message might compromise the security of your program.</span></span>

<span data-ttu-id="a96c1-127">Il bordo dell'elemento viene impostato solo per scopi di spaziatura.</span><span class="sxs-lookup"><span data-stu-id="a96c1-127">The item border is set just for spacing purposes.</span></span> <span data-ttu-id="a96c1-128">Un'impostazione corretta attiva un ricalcolo delle barre di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="a96c1-128">A successful setting triggers a recalculation of the scroll bars.</span></span>

<span data-ttu-id="a96c1-129">Questo messaggio potrebbe non essere supportato nelle versioni future di Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="a96c1-129">This message may not be supported in future versions of Comctl32.dll.</span></span> <span data-ttu-id="a96c1-130">Inoltre, questo messaggio non è definito in commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="a96c1-130">Also, this message is not defined in commctrl.h.</span></span> <span data-ttu-id="a96c1-131">Aggiungere le definizioni seguenti ai file di origine dell'applicazione per usare il messaggio:</span><span class="sxs-lookup"><span data-stu-id="a96c1-131">Add the following definitions to the source files of your application to use the message:</span></span>

``` syntax
#define TVM_SETBORDER (TV_FIRST + 35)
#define TVSBF_XBORDER 0x00000001
#define TVSBF_YBORDER 0x00000002 
```

## <a name="requirements"></a><span data-ttu-id="a96c1-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a96c1-132">Requirements</span></span>



| <span data-ttu-id="a96c1-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a96c1-133">Requirement</span></span> | <span data-ttu-id="a96c1-134">Valore</span><span class="sxs-lookup"><span data-stu-id="a96c1-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a96c1-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a96c1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a96c1-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a96c1-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a96c1-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a96c1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a96c1-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a96c1-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a96c1-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a96c1-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a96c1-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a96c1-140"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a96c1-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a96c1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a96c1-142">**Sebordo TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="a96c1-142">**TreeView\_SetBorder**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
</dt> </dl>

 


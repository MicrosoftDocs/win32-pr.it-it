---
title: Messaggio CBEM_SETEXTENDEDSTYLE (COMmctrl. h)
description: Imposta gli stili estesi in un controllo ComboBoxEx.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- Controlli di Windows Message CBEM_SETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- CBEM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a60518d2f6130c2c89e379125308fc2e647c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302524"
---
# <a name="cbem_setextendedstyle-message"></a><span data-ttu-id="96f8c-104">\_Messaggio CBEM SETEXTENDEDSTYLE</span><span class="sxs-lookup"><span data-stu-id="96f8c-104">CBEM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="96f8c-105">Imposta gli stili estesi in un controllo ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="96f8c-105">Sets extended styles within a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="96f8c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="96f8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96f8c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96f8c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96f8c-108">Valore **DWORD** che indica quali stili in *lParam* devono essere interessati.</span><span class="sxs-lookup"><span data-stu-id="96f8c-108">A **DWORD** value that indicates which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="96f8c-109">Solo gli stili estesi in *wParam* verranno modificati.</span><span class="sxs-lookup"><span data-stu-id="96f8c-109">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="96f8c-110">Se questo parametro è zero, saranno interessati tutti gli stili in *lParam* .</span><span class="sxs-lookup"><span data-stu-id="96f8c-110">If this parameter is zero, then all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="96f8c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96f8c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96f8c-112">Valore **DWORD** che contiene gli [stili estesi del controllo ComboBoxEx](comboboxex-control-extended-styles.md) da impostare per il controllo.</span><span class="sxs-lookup"><span data-stu-id="96f8c-112">A **DWORD** value that contains the [ComboBoxEx Control Extended Styles](comboboxex-control-extended-styles.md) to set for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96f8c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96f8c-113">Return value</span></span>

<span data-ttu-id="96f8c-114">Restituisce un valore **DWORD** che contiene gli stili estesi usati in precedenza per il controllo.</span><span class="sxs-lookup"><span data-stu-id="96f8c-114">Returns a **DWORD** value that contains the extended styles previously used for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="96f8c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="96f8c-115">Remarks</span></span>

<span data-ttu-id="96f8c-116">*wParam* consente di modificare uno o più stili estesi senza dover prima recuperare gli stili esistenti.</span><span class="sxs-lookup"><span data-stu-id="96f8c-116">*wParam* enables you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="96f8c-117">Se ad esempio si passa [**CBES \_ ex \_ NOEDITIMAGE**](comboboxex-control-extended-styles.md) per *wParam* e 0 per *lParam*, lo stile **CBES \_ ex \_ NOEDITIMAGE** verrà cancellato, ma tutti gli altri stili rimarranno invariati.</span><span class="sxs-lookup"><span data-stu-id="96f8c-117">For example, if you pass [**CBES\_EX\_NOEDITIMAGE**](comboboxex-control-extended-styles.md) for *wParam* and 0 for *lParam*, the **CBES\_EX\_NOEDITIMAGE** style will be cleared, but all other styles will remain the same.</span></span>

<span data-ttu-id="96f8c-118">Se si tenta di impostare uno stile esteso per un controllo ComboBoxEx creato con lo [**stile \_ semplice CBS**](combo-box-styles.md) , è possibile che non venga ridisegnato correttamente.</span><span class="sxs-lookup"><span data-stu-id="96f8c-118">If you try to set an extended style for a ComboBoxEx control created with the [**CBS\_SIMPLE**](combo-box-styles.md) style, it may not repaint properly.</span></span>

## <a name="requirements"></a><span data-ttu-id="96f8c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96f8c-119">Requirements</span></span>



| <span data-ttu-id="96f8c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="96f8c-120">Requirement</span></span> | <span data-ttu-id="96f8c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="96f8c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96f8c-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96f8c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="96f8c-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96f8c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="96f8c-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96f8c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="96f8c-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="96f8c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96f8c-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96f8c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="96f8c-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="96f8c-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






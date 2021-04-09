---
title: Messaggio TTM_GETTITLE (COMmctrl. h)
description: Recuperare le informazioni relative al titolo di un controllo ToolTip.
ms.assetid: d8992dd1-1610-44e8-8c0f-8ae1ac4b5898
keywords:
- Controlli di Windows Message TTM_GETTITLE
topic_type:
- apiref
api_name:
- TTM_GETTITLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0048925ed3dc267ac07b10b85e2ea1ca1449996c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964238"
---
# <a name="ttm_gettitle-message"></a><span data-ttu-id="e8755-104">\_Messaggio GETTITLE TTM</span><span class="sxs-lookup"><span data-stu-id="e8755-104">TTM\_GETTITLE message</span></span>

<span data-ttu-id="e8755-105">Recuperare le informazioni relative al titolo di un controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="e8755-105">Retrieve information concerning the title of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8755-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8755-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8755-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8755-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e8755-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e8755-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e8755-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8755-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8755-110">Puntatore a una struttura [**TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle) che contiene informazioni sul titolo di una descrizione comandi.</span><span class="sxs-lookup"><span data-stu-id="e8755-110">Pointer to a [**TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle) structure that contains information about a tooltip title.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8755-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8755-111">Return value</span></span>

<span data-ttu-id="e8755-112">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e8755-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8755-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8755-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e8755-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="e8755-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="e8755-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e8755-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8755-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8755-116">Requirements</span></span>



| <span data-ttu-id="e8755-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8755-117">Requirement</span></span> | <span data-ttu-id="e8755-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e8755-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8755-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8755-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e8755-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8755-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8755-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8755-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e8755-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8755-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8755-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8755-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8755-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8755-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Messaggio TTM_SETWINDOWTHEME (COMmctrl. h)
description: Imposta lo stile di visualizzazione di un controllo ToolTip.
ms.assetid: eeddb91e-8eb8-4480-9ab2-5efa9e3ef48a
keywords:
- Controlli di Windows Message TTM_SETWINDOWTHEME
topic_type:
- apiref
api_name:
- TTM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9c3f25b62bf0fe38a679234183cd5046f60784f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518862"
---
# <a name="ttm_setwindowtheme-message"></a><span data-ttu-id="cbad0-104">\_Messaggio TTM SETWINDOWTHEME</span><span class="sxs-lookup"><span data-stu-id="cbad0-104">TTM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="cbad0-105">Imposta lo stile di visualizzazione di un controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="cbad0-105">Sets the visual style of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cbad0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cbad0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbad0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cbad0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cbad0-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cbad0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cbad0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cbad0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cbad0-110">Puntatore a una stringa Unicode che contiene lo stile di visualizzazione della descrizione comando da impostare.</span><span class="sxs-lookup"><span data-stu-id="cbad0-110">Pointer to a Unicode string that contains the tooltip visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbad0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cbad0-111">Return value</span></span>

<span data-ttu-id="cbad0-112">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="cbad0-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbad0-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="cbad0-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cbad0-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="cbad0-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="cbad0-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cbad0-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cbad0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbad0-116">Requirements</span></span>



| <span data-ttu-id="cbad0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbad0-117">Requirement</span></span> | <span data-ttu-id="cbad0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="cbad0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cbad0-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbad0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cbad0-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cbad0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cbad0-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbad0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cbad0-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cbad0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cbad0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cbad0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbad0-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbad0-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






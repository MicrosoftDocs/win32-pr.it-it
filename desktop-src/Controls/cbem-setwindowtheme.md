---
title: Messaggio CBEM_SETWINDOWTHEME (COMmctrl. h)
description: Imposta lo stile di visualizzazione di un controllo ComboBoxEx.
ms.assetid: 064f9a24-42be-42f4-bee3-e7320fe8c366
keywords:
- Controlli di Windows Message CBEM_SETWINDOWTHEME
topic_type:
- apiref
api_name:
- CBEM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cda1e5c46bb6216c413737c44b5785ac26925f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301764"
---
# <a name="cbem_setwindowtheme-message"></a><span data-ttu-id="e6ca5-104">\_Messaggio CBEM SETWINDOWTHEME</span><span class="sxs-lookup"><span data-stu-id="e6ca5-104">CBEM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="e6ca5-105">Imposta lo stile di visualizzazione di un controllo ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="e6ca5-105">Sets the visual style of a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e6ca5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6ca5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6ca5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6ca5-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e6ca5-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e6ca5-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e6ca5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6ca5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6ca5-110">Puntatore a una stringa Unicode che contiene lo stile di visualizzazione del controllo da impostare.</span><span class="sxs-lookup"><span data-stu-id="e6ca5-110">A pointer to a Unicode string that contains the control visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6ca5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6ca5-111">Return value</span></span>

<span data-ttu-id="e6ca5-112">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e6ca5-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6ca5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6ca5-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e6ca5-114">Per usare questo messaggio, è necessario fornire un manifesto che specifichi la versione 6,0 di Comclt32.</span><span class="sxs-lookup"><span data-stu-id="e6ca5-114">To use this message, you must provide a manifest specifying Comclt32 version 6.0.</span></span> <span data-ttu-id="e6ca5-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e6ca5-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e6ca5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6ca5-116">Requirements</span></span>



| <span data-ttu-id="e6ca5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6ca5-117">Requirement</span></span> | <span data-ttu-id="e6ca5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e6ca5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ca5-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6ca5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e6ca5-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6ca5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6ca5-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6ca5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e6ca5-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e6ca5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6ca5-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6ca5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6ca5-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6ca5-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Messaggio CCM_SETWINDOWTHEME (COMmctrl. h)
description: Imposta lo stile di visualizzazione di un controllo.
ms.assetid: 0200fa11-847f-477c-92e0-790b4d1ca0ef
keywords:
- Controlli di Windows Message CCM_SETWINDOWTHEME
topic_type:
- apiref
api_name:
- CCM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea8996273a0c9d03123ce58f5fbb0dfb099be94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477632"
---
# <a name="ccm_setwindowtheme-message"></a><span data-ttu-id="cfc28-104">\_Messaggio SETWINDOWTHEME CCM</span><span class="sxs-lookup"><span data-stu-id="cfc28-104">CCM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="cfc28-105">Imposta lo stile di visualizzazione di un controllo.</span><span class="sxs-lookup"><span data-stu-id="cfc28-105">Sets the visual style of a control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfc28-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cfc28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfc28-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfc28-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cfc28-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cfc28-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cfc28-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfc28-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfc28-110">Puntatore a una stringa Unicode che contiene lo stile di visualizzazione del controllo da impostare.</span><span class="sxs-lookup"><span data-stu-id="cfc28-110">A pointer to a Unicode string that contains the control visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfc28-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cfc28-111">Return value</span></span>

<span data-ttu-id="cfc28-112">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="cfc28-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfc28-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="cfc28-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cfc28-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="cfc28-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="cfc28-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cfc28-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cfc28-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfc28-116">Requirements</span></span>



| <span data-ttu-id="cfc28-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfc28-117">Requirement</span></span> | <span data-ttu-id="cfc28-118">Valore</span><span class="sxs-lookup"><span data-stu-id="cfc28-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfc28-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfc28-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cfc28-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cfc28-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cfc28-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfc28-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cfc28-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cfc28-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cfc28-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cfc28-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfc28-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfc28-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






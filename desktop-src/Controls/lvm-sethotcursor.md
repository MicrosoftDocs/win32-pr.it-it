---
title: Messaggio LVM_SETHOTCURSOR (COMmctrl. h)
description: Imposta il valore HCURSOR usato dal controllo di visualizzazione elenco quando il puntatore è posizionato su un elemento mentre è abilitata la funzionalità di rilevamento a caldo.
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- Controlli di Windows Message LVM_SETHOTCURSOR
topic_type:
- apiref
api_name:
- LVM_SETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e743f74eda3b59f04f6f4793b47d76da3bab881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739946"
---
# <a name="lvm_sethotcursor-message"></a><span data-ttu-id="1702d-104">\_Messaggio SETHOTCURSOR LVM</span><span class="sxs-lookup"><span data-stu-id="1702d-104">LVM\_SETHOTCURSOR message</span></span>

<span data-ttu-id="1702d-105">Imposta il valore HCURSOR usato dal controllo di visualizzazione elenco quando il puntatore è posizionato su un elemento mentre è abilitata la funzionalità di rilevamento a caldo.</span><span class="sxs-lookup"><span data-stu-id="1702d-105">Sets the HCURSOR value that the list-view control uses when the pointer is over an item while hot tracking is enabled.</span></span> <span data-ttu-id="1702d-106">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetHotCursor di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) .</span><span class="sxs-lookup"><span data-stu-id="1702d-106">You can send this message explicitly or use the [**ListView\_SetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) macro.</span></span> <span data-ttu-id="1702d-107">Per verificare se è abilitata la funzionalità di rilevamento attivo, chiamare [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span><span class="sxs-lookup"><span data-stu-id="1702d-107">To check whether hot tracking is enabled, call [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span>

## <a name="parameters"></a><span data-ttu-id="1702d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1702d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1702d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1702d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1702d-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1702d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1702d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1702d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1702d-112">Handle per il cursore da impostare.</span><span class="sxs-lookup"><span data-stu-id="1702d-112">Handle to the cursor to be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1702d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1702d-113">Return value</span></span>

<span data-ttu-id="1702d-114">Restituisce un valore HCURSOR che rappresenta il cursore attivo precedente.</span><span class="sxs-lookup"><span data-stu-id="1702d-114">Returns an HCURSOR value that is the previous hot cursor.</span></span>

## <a name="remarks"></a><span data-ttu-id="1702d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="1702d-115">Remarks</span></span>

<span data-ttu-id="1702d-116">Un controllo di visualizzazione elenco Usa il rilevamento a caldo e la selezione del passaggio del mouse quando lo stile [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) è impostato.</span><span class="sxs-lookup"><span data-stu-id="1702d-116">A list-view control uses hot tracking and hover selection when the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) style is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="1702d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1702d-117">Requirements</span></span>



| <span data-ttu-id="1702d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1702d-118">Requirement</span></span> | <span data-ttu-id="1702d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1702d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1702d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1702d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1702d-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1702d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1702d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1702d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1702d-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1702d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1702d-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1702d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1702d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1702d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 


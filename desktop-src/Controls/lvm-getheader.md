---
title: Messaggio LVM_GETHEADER (COMmctrl. h)
description: Ottiene l'handle per il controllo intestazione utilizzato dal controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ListView GetHeader.
ms.assetid: 4708b493-4449-4844-bf0d-e6969bcf0246
keywords:
- Controlli di Windows Message LVM_GETHEADER
topic_type:
- apiref
api_name:
- LVM_GETHEADER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d53082092118cad373005743849498791f0e1ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047932"
---
# <a name="lvm_getheader-message"></a><span data-ttu-id="7434e-105">Messaggio di LVM \_ GETheader</span><span class="sxs-lookup"><span data-stu-id="7434e-105">LVM\_GETHEADER message</span></span>

<span data-ttu-id="7434e-106">Ottiene l'handle per il controllo intestazione utilizzato dal controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="7434e-106">Gets the handle to the header control used by the list-view control.</span></span> <span data-ttu-id="7434e-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**ListView \_ GetHeader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) .</span><span class="sxs-lookup"><span data-stu-id="7434e-107">You can send this message explicitly or use the [**ListView\_GetHeader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7434e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7434e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7434e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7434e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7434e-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7434e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7434e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7434e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7434e-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7434e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7434e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7434e-113">Return value</span></span>

<span data-ttu-id="7434e-114">Restituisce l'handle per il controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="7434e-114">Returns the handle to the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="7434e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7434e-115">Requirements</span></span>



| <span data-ttu-id="7434e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7434e-116">Requirement</span></span> | <span data-ttu-id="7434e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7434e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7434e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7434e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7434e-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7434e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7434e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7434e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7434e-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7434e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7434e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7434e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7434e-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7434e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






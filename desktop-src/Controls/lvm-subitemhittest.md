---
title: Messaggio LVM_SUBITEMHITTEST (COMmctrl. h)
description: Determina quale elemento della visualizzazione elenco o elemento secondario si trova in una posizione specificata. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SubItemHitTest di ListView.
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- Controlli di Windows Message LVM_SUBITEMHITTEST
topic_type:
- apiref
api_name:
- LVM_SUBITEMHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c811a3ed85b9eb157920f700b34d5d9c99597e67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475365"
---
# <a name="lvm_subitemhittest-message"></a><span data-ttu-id="ec9a6-105">\_Messaggio SUBITEMHITTEST LVM</span><span class="sxs-lookup"><span data-stu-id="ec9a6-105">LVM\_SUBITEMHITTEST message</span></span>

<span data-ttu-id="ec9a6-106">Determina quale elemento della visualizzazione elenco o elemento secondario si trova in una posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="ec9a6-106">Determines which list-view item or subitem is at a given position.</span></span> <span data-ttu-id="ec9a6-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SubItemHitTest di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) .</span><span class="sxs-lookup"><span data-stu-id="ec9a6-107">You can send this message explicitly or by using the [**ListView\_SubItemHitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec9a6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec9a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec9a6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec9a6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ec9a6-110">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="ec9a6-110">Must be 0.</span></span> <span data-ttu-id="ec9a6-111">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="ec9a6-111">**Windows Vista.**</span></span> <span data-ttu-id="ec9a6-112">Deve essere-1 se è necessario recuperare il membro **iGROUP** di *lParam* .</span><span class="sxs-lookup"><span data-stu-id="ec9a6-112">Should be -1 if the **iGroup** member of *lParam* is to be retrieved.</span></span></dd> <dt>

<span data-ttu-id="ec9a6-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec9a6-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec9a6-114">Puntatore a una struttura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) .</span><span class="sxs-lookup"><span data-stu-id="ec9a6-114">Pointer to an [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure.</span></span> <span data-ttu-id="ec9a6-115">La struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) all'interno di **LVHITTESTINFO** deve essere impostata sulle coordinate client da sottoporre a hit test.</span><span class="sxs-lookup"><span data-stu-id="ec9a6-115">The [**POINT**](/previous-versions//dd162805(v=vs.85)) structure within **LVHITTESTINFO** should be set to the client coordinates to be hit-tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec9a6-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec9a6-116">Return value</span></span>

<span data-ttu-id="ec9a6-117">Restituisce l'indice dell'elemento o del sottoelemento testato, se presente, oppure-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ec9a6-117">Returns the index of the item or subitem tested, if any, or -1 otherwise.</span></span> <span data-ttu-id="ec9a6-118">Se un elemento o un elemento secondario si trova in corrispondenza delle coordinate specificate, i campi della struttura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) verranno riempiti con le informazioni di hit applicabili.</span><span class="sxs-lookup"><span data-stu-id="ec9a6-118">If an item or subitem is at the given coordinates, the fields of the [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure will be filled with the applicable hit information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec9a6-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec9a6-119">Requirements</span></span>



| <span data-ttu-id="ec9a6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec9a6-120">Requirement</span></span> | <span data-ttu-id="ec9a6-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ec9a6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec9a6-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec9a6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ec9a6-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec9a6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec9a6-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec9a6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ec9a6-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ec9a6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec9a6-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec9a6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec9a6-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec9a6-127"><dt>Commctrl.h</dt></span></span> </dl> |



 


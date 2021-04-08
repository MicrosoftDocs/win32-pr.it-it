---
title: Messaggio LVM_GETTILEINFO (COMmctrl. h)
description: Recupera le informazioni su un riquadro in un controllo visualizzazione elenco.
ms.assetid: e89a3eae-0970-488c-ba95-1072aa85bbf4
keywords:
- Controlli di Windows Message LVM_GETTILEINFO
topic_type:
- apiref
api_name:
- LVM_GETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db5bfd085cd5cbaced0bf90b17e8862a6c0e159b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048643"
---
# <a name="lvm_gettileinfo-message"></a><span data-ttu-id="3ffd4-104">\_Messaggio GETTILEINFO LVM</span><span class="sxs-lookup"><span data-stu-id="3ffd4-104">LVM\_GETTILEINFO message</span></span>

<span data-ttu-id="3ffd4-105">Recupera le informazioni su un riquadro in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-105">Retrieves information about a tile in a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3ffd4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ffd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ffd4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3ffd4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3ffd4-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3ffd4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3ffd4-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3ffd4-110">Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> che riceve le informazioni recuperate.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> structure that receives the retrieved information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ffd4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ffd4-111">Return value</span></span>

<span data-ttu-id="3ffd4-112">Valore restituito non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ffd4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ffd4-113">Remarks</span></span>

<span data-ttu-id="3ffd4-114">Visualizzazione affiancata è un nuovo modo per organizzare e visualizzare gli elementi in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-114">Tile view is a new way of arranging and displaying items in a list-view control.</span></span> <span data-ttu-id="3ffd4-115">Le altre viste sono Icon, Small Icon, Details ed List.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-115">The other views are icon, small icon, details, and list.</span></span>

> [!Note]  
> <span data-ttu-id="3ffd4-116">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="3ffd4-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="3ffd4-117">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3ffd4-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3ffd4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ffd4-118">Requirements</span></span>



| <span data-ttu-id="3ffd4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ffd4-119">Requirement</span></span> | <span data-ttu-id="3ffd4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3ffd4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ffd4-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ffd4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3ffd4-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ffd4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3ffd4-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ffd4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3ffd4-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3ffd4-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3ffd4-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ffd4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ffd4-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ffd4-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






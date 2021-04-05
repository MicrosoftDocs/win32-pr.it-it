---
title: Messaggio LVM_GETINSERTMARK (COMmctrl. h)
description: Recupera la posizione del punto di inserimento.
ms.assetid: ad00df4c-4b4b-48f1-8821-7849a216df2e
keywords:
- Controlli di Windows Message LVM_GETINSERTMARK
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8cba96ae7d357e3e1f5a007fa41f6b7e9e3b64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873581"
---
# <a name="lvm_getinsertmark-message"></a><span data-ttu-id="69a16-104">\_Messaggio GETINSERTMARK LVM</span><span class="sxs-lookup"><span data-stu-id="69a16-104">LVM\_GETINSERTMARK message</span></span>

<span data-ttu-id="69a16-105">Recupera la posizione del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="69a16-105">Retrieves the position of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="69a16-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="69a16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69a16-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69a16-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="69a16-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="69a16-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="69a16-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69a16-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="69a16-110">Puntatore a una struttura <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> che riceve la posizione del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="69a16-110">Pointer to a <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that receives the position of the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69a16-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69a16-111">Return value</span></span>

<span data-ttu-id="69a16-112">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="69a16-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="69a16-113">Viene restituito **false** se la dimensione nel membro **cbSize** della struttura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) non è uguale alla dimensione effettiva della struttura.</span><span class="sxs-lookup"><span data-stu-id="69a16-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="69a16-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="69a16-114">Remarks</span></span>

<span data-ttu-id="69a16-115">Un punto di inserimento può essere visualizzato solo se il controllo elenco-visualizzazione si trova nella visualizzazione icone, nella visualizzazione icone piccola o nella visualizzazione affiancata e non è in modalità di visualizzazione gruppo.</span><span class="sxs-lookup"><span data-stu-id="69a16-115">An insertion point can appear only if the list-view control is in icon view, small icon view, or tile view, and is not in group-view mode.</span></span>

> [!Note]  
> <span data-ttu-id="69a16-116">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="69a16-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="69a16-117">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="69a16-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="69a16-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69a16-118">Requirements</span></span>



| <span data-ttu-id="69a16-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="69a16-119">Requirement</span></span> | <span data-ttu-id="69a16-120">Valore</span><span class="sxs-lookup"><span data-stu-id="69a16-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69a16-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69a16-121">Minimum supported client</span></span><br/> | <span data-ttu-id="69a16-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="69a16-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="69a16-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69a16-123">Minimum supported server</span></span><br/> | <span data-ttu-id="69a16-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="69a16-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69a16-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69a16-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="69a16-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="69a16-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






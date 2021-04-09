---
title: Messaggio LVM_INSERTMARKHITTEST (COMmctrl. h)
description: Recupera il punto di inserimento più vicino a un punto specificato.
ms.assetid: 901bb770-a36d-4d9f-a53b-d497b4df39e5
keywords:
- Controlli di Windows Message LVM_INSERTMARKHITTEST
topic_type:
- apiref
api_name:
- LVM_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bdb82e924b4a5d74d152917f52c4039e0aca81b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120970"
---
# <a name="lvm_insertmarkhittest-message"></a><span data-ttu-id="1b5e8-104">\_Messaggio INSERTMARKHITTEST LVM</span><span class="sxs-lookup"><span data-stu-id="1b5e8-104">LVM\_INSERTMARKHITTEST message</span></span>

<span data-ttu-id="1b5e8-105">Recupera il punto di inserimento più vicino a un punto specificato.</span><span class="sxs-lookup"><span data-stu-id="1b5e8-105">Retrieves the insertion point closest to a specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b5e8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1b5e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b5e8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b5e8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1b5e8-108">Puntatore a una struttura di **punti** che contiene le coordinate dell'hit test.</span><span class="sxs-lookup"><span data-stu-id="1b5e8-108">Pointer to a **POINT** structure that contains the hit test coordinates.</span></span></dd> <dt>

<span data-ttu-id="1b5e8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b5e8-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1b5e8-110">Puntatore a una struttura <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> che specifica il punto di inserimento più vicino alle coordinate definite dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="1b5e8-110">Pointer to an <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that specifies the insertion point closest to the coordinates defined by the *wParam* parameter.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b5e8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1b5e8-111">Return value</span></span>

<span data-ttu-id="1b5e8-112">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1b5e8-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="1b5e8-113">Viene restituito **false** se la dimensione nel membro **cbSize** della struttura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) non è uguale alla dimensione effettiva della struttura o quando un punto di inserimento non è applicabile nella visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="1b5e8-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure, or when an insertion point does not apply in the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b5e8-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1b5e8-114">Remarks</span></span>

<span data-ttu-id="1b5e8-115">Un punto di inserimento può essere visualizzato solo se il controllo elenco-visualizzazione si trova nella visualizzazione icone, nella visualizzazione icone piccole o nella visualizzazione affiancata e non è in modalità di visualizzazione gruppo.</span><span class="sxs-lookup"><span data-stu-id="1b5e8-115">An insertion point can only appear if the list-view control is in icon view, small icon view, or tile view and is not in group-view mode.</span></span>

<span data-ttu-id="1b5e8-116">Se i punti di inserimento non sono validi per la vista, la struttura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) contiene un valore-1 nel membro **iItem** .</span><span class="sxs-lookup"><span data-stu-id="1b5e8-116">If insertion points do not apply for the view, the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure contains a -1 in the **iItem** member.</span></span>

> [!Note]  
> <span data-ttu-id="1b5e8-117">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="1b5e8-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1b5e8-118">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1b5e8-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1b5e8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b5e8-119">Requirements</span></span>



| <span data-ttu-id="1b5e8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b5e8-120">Requirement</span></span> | <span data-ttu-id="1b5e8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1b5e8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b5e8-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b5e8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1b5e8-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b5e8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b5e8-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b5e8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1b5e8-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1b5e8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b5e8-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b5e8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b5e8-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b5e8-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Messaggio LVM_SETINSERTMARK (COMmctrl. h)
description: Imposta il punto di inserimento sulla posizione definita.
ms.assetid: 32cf5a11-918a-4dc4-bf10-88b3c26f26cc
keywords:
- Controlli di Windows Message LVM_SETINSERTMARK
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dab80b1b73b620ce94b75aecab90f6bdd69bf228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118990"
---
# <a name="lvm_setinsertmark-message"></a><span data-ttu-id="74acb-104">\_Messaggio SETINSERTMARK LVM</span><span class="sxs-lookup"><span data-stu-id="74acb-104">LVM\_SETINSERTMARK message</span></span>

<span data-ttu-id="74acb-105">Imposta il punto di inserimento sulla posizione definita.</span><span class="sxs-lookup"><span data-stu-id="74acb-105">Sets the insertion point to the defined position.</span></span>

## <a name="parameters"></a><span data-ttu-id="74acb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="74acb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74acb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74acb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="74acb-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="74acb-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="74acb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74acb-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="74acb-110">Puntatore a una struttura <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> che specifica la posizione in cui impostare il punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="74acb-110">Pointer to a <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that specifies where to set the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74acb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74acb-111">Return value</span></span>

<span data-ttu-id="74acb-112">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="74acb-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="74acb-113">Viene restituito **false** se la dimensione nel membro **cbSize** della struttura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) non è uguale alla dimensione effettiva della struttura o quando un punto di inserimento non è applicabile nella visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="74acb-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure, or when an insertion point does not apply in the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="74acb-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="74acb-114">Remarks</span></span>

<span data-ttu-id="74acb-115">Un punto di inserimento può essere visualizzato solo se il controllo elenco-visualizzazione si trova nella visualizzazione icone, nella visualizzazione icone piccole o nella visualizzazione affiancata e non è in modalità di visualizzazione gruppo.</span><span class="sxs-lookup"><span data-stu-id="74acb-115">An insertion point can only appear if the list-view control is in icon view, small icon view, or tile view, and is not in group-view mode.</span></span>

> [!Note]  
> <span data-ttu-id="74acb-116">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="74acb-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="74acb-117">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="74acb-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="74acb-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74acb-118">Requirements</span></span>



| <span data-ttu-id="74acb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="74acb-119">Requirement</span></span> | <span data-ttu-id="74acb-120">Valore</span><span class="sxs-lookup"><span data-stu-id="74acb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74acb-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74acb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="74acb-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74acb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74acb-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74acb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="74acb-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="74acb-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74acb-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74acb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="74acb-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="74acb-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Messaggio LM_HITTEST (COMmctrl. h)
description: Determina se l'utente ha fatto clic sul collegamento specificato.
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- Controlli di Windows Message LM_HITTEST
topic_type:
- apiref
api_name:
- LM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c497800369203ac8ea7484371e1038ba15d6cc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873329"
---
# <a name="lm_hittest-message"></a><span data-ttu-id="a804e-104">\_Messaggio HITTEST di LM</span><span class="sxs-lookup"><span data-stu-id="a804e-104">LM\_HITTEST message</span></span>

<span data-ttu-id="a804e-105">Determina se l'utente ha fatto clic sul collegamento specificato.</span><span class="sxs-lookup"><span data-stu-id="a804e-105">Determines whether the user clicked the specified link.</span></span>

## <a name="parameters"></a><span data-ttu-id="a804e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a804e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a804e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a804e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a804e-108">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="a804e-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="a804e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a804e-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a804e-110">Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LHITTESTINFO**</a> da compilare con informazioni sul collegamento su cui l'utente ha fatto clic, se presente.</span><span class="sxs-lookup"><span data-stu-id="a804e-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LHITTESTINFO**</a> structure to be filled with information about the link the user clicked, if any exists.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a804e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a804e-111">Return value</span></span>

<span data-ttu-id="a804e-112">Restituisce **true** se l'utente ha fatto clic su un collegamento; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="a804e-112">Returns **TRUE** if user clicked on a link, otherwise returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a804e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a804e-113">Remarks</span></span>

<span data-ttu-id="a804e-114">Se il messaggio di **\_ HITTEST** viene completato correttamente, il sistema compila [**iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) e **litey. szId**.</span><span class="sxs-lookup"><span data-stu-id="a804e-114">If the **LM\_HITTEST** message succeeds, the system fills in [**LITEM.iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) and **LITEM.szID**.</span></span> <span data-ttu-id="a804e-115">Se il messaggio di **\_ HITTEST** viene interrotto, non presupporre che le informazioni in **Lite** è valide.</span><span class="sxs-lookup"><span data-stu-id="a804e-115">If the **LM\_HITTEST** message fails, do not assume that any information in **LITEM** is valid.</span></span>

> [!Note]  
> <span data-ttu-id="a804e-116">Per usare questa API, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="a804e-116">To use this API, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="a804e-117">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a804e-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a804e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a804e-118">Requirements</span></span>



| <span data-ttu-id="a804e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a804e-119">Requirement</span></span> | <span data-ttu-id="a804e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a804e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a804e-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a804e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a804e-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a804e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a804e-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a804e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a804e-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a804e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a804e-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a804e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a804e-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a804e-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: LM_GETIDEALHEIGHT messaggio (Commctrl.h)
description: "LM_GETIDEALHEIGHT messaggio: recupera l'altezza preferita di un collegamento per la larghezza corrente del controllo."
ms.assetid: bf6ef3c1-89bc-4c56-9384-085fd00234e1
keywords:
- LM_GETIDEALHEIGHT messaggio controlli Windows
topic_type:
- apiref
api_name:
- LM_GETIDEALHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6e82f259124e6da285ed2357d48ca07d5f8c08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112399"
---
# <a name="lm_getidealheight-message"></a><span data-ttu-id="272d1-104">Messaggio \_ LM GETIDEALHEIGHT</span><span class="sxs-lookup"><span data-stu-id="272d1-104">LM\_GETIDEALHEIGHT message</span></span>

<span data-ttu-id="272d1-105">Recupera l'altezza preferita di un collegamento per la larghezza corrente del controllo.</span><span class="sxs-lookup"><span data-stu-id="272d1-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="272d1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="272d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="272d1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="272d1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="272d1-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="272d1-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="272d1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="272d1-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="272d1-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="272d1-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="272d1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="272d1-111">Return value</span></span>

<span data-ttu-id="272d1-112">Intero che rappresenta l'altezza preferita del testo del collegamento, in pixel.</span><span class="sxs-lookup"><span data-stu-id="272d1-112">Integer representing the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="272d1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="272d1-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="272d1-114">Per usare questo messaggio, è necessario fornire un manifesto che specifica Comclt32.dll versione 6.0.</span><span class="sxs-lookup"><span data-stu-id="272d1-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="272d1-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="272d1-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="272d1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="272d1-116">Requirements</span></span>



| <span data-ttu-id="272d1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="272d1-117">Requirement</span></span> | <span data-ttu-id="272d1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="272d1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="272d1-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="272d1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="272d1-120">Solo app desktop di Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="272d1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="272d1-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="272d1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="272d1-122">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="272d1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="272d1-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="272d1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="272d1-124"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="272d1-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






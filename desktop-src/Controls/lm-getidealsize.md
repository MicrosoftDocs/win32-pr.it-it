---
title: LM_GETIDEALSIZE messaggio (Commctrl.h)
description: "LM_GETIDEALSIZE messaggio: recupera l'altezza preferita di un collegamento per la larghezza corrente del controllo."
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- LM_GETIDEALSIZE di windows del messaggio
topic_type:
- apiref
api_name:
- LM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 761fb5f6e5f7a2e2e9b1b9cc862b9a8f2c0fcd1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112389"
---
# <a name="lm_getidealsize-message"></a><span data-ttu-id="b7b01-104">Messaggio \_ LM GETIDEALSIZE</span><span class="sxs-lookup"><span data-stu-id="b7b01-104">LM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="b7b01-105">Recupera l'altezza preferita di un collegamento per la larghezza corrente del controllo.</span><span class="sxs-lookup"><span data-stu-id="b7b01-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="b7b01-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7b01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7b01-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7b01-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b7b01-108">Larghezza massima del collegamento, in pixel.</span><span class="sxs-lookup"><span data-stu-id="b7b01-108">Maximum width of the link, in pixels.</span></span></dd> <dt>

<span data-ttu-id="b7b01-109">*lParam* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="b7b01-109">*lParam* \[out\]</span></span>
</dt> <dd><span data-ttu-id="b7b01-110">Quando il messaggio viene restituito, contiene un puntatore a una <a href="/previous-versions//dd145106(v=vs.85)">**struttura SIZE.**</a></span><span class="sxs-lookup"><span data-stu-id="b7b01-110">When this message returns, contains a pointer to a <a href="/previous-versions//dd145106(v=vs.85)">**SIZE**</a> structure.</span></span> <span data-ttu-id="b7b01-111">Il **membro cy** di questa struttura indica l'altezza ideale del controllo per la larghezza specificata.</span><span class="sxs-lookup"><span data-stu-id="b7b01-111">The **cy** member of this structure indicates the ideal height of the control for the given width.</span></span> <span data-ttu-id="b7b01-112">Regola il membro **cx** in base alla quantità di spazio effettivamente necessaria.</span><span class="sxs-lookup"><span data-stu-id="b7b01-112">It adjusts the **cx** member to the amount of space actually needed.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7b01-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7b01-113">Return value</span></span>

<span data-ttu-id="b7b01-114">Intero che rappresenta l'altezza preferita del testo del collegamento, in pixel.</span><span class="sxs-lookup"><span data-stu-id="b7b01-114">Integer that represents the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7b01-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7b01-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b7b01-116">Per usare questa API, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6.0.</span><span class="sxs-lookup"><span data-stu-id="b7b01-116">To use this API, you must provide a manifest that specifies Comclt32.dll version 6.0.</span></span> <span data-ttu-id="b7b01-117">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)</span><span class="sxs-lookup"><span data-stu-id="b7b01-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b7b01-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7b01-118">Requirements</span></span>



| <span data-ttu-id="b7b01-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7b01-119">Requirement</span></span> | <span data-ttu-id="b7b01-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b7b01-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b01-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7b01-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b7b01-122">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b7b01-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7b01-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7b01-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b7b01-124">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b7b01-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7b01-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7b01-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7b01-126"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="b7b01-126"><dt>Commctrl.h</dt></span></span> </dl> |



 


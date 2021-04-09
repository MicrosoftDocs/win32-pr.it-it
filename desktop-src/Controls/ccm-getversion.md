---
title: Messaggio CCM_GETVERSION (COMmctrl. h)
description: Ottiene il numero di versione di un controllo impostato dal messaggio della versione più recente di CCM \_ .
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- Controlli di Windows Message CCM_GETVERSION
topic_type:
- apiref
api_name:
- CCM_GETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd302774f8821b51a4abaf72bccc403e7302e6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120326"
---
# <a name="ccm_getversion-message"></a><span data-ttu-id="2eb27-104">\_Messaggio CCM GETversion</span><span class="sxs-lookup"><span data-stu-id="2eb27-104">CCM\_GETVERSION message</span></span>

<span data-ttu-id="2eb27-105">Ottiene il numero di versione di un controllo impostato dal messaggio della [**\_ versione**](ccm-setversion.md) più recente di CCM.</span><span class="sxs-lookup"><span data-stu-id="2eb27-105">Gets the version number for a control set by the most recent [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="2eb27-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2eb27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eb27-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2eb27-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2eb27-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2eb27-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2eb27-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2eb27-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2eb27-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2eb27-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eb27-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2eb27-111">Return value</span></span>

<span data-ttu-id="2eb27-112">Restituisce il numero di versione impostato dal messaggio della [**\_ versione CCM**](ccm-setversion.md) più recente.</span><span class="sxs-lookup"><span data-stu-id="2eb27-112">Returns the version number set by the most recent [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="2eb27-113">Se non è stato inviato alcun messaggio di questo tipo, viene restituito zero.</span><span class="sxs-lookup"><span data-stu-id="2eb27-113">If no such message has been sent, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2eb27-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2eb27-114">Remarks</span></span>

<span data-ttu-id="2eb27-115">Questo messaggio non restituisce la versione della DLL.</span><span class="sxs-lookup"><span data-stu-id="2eb27-115">This message does not return the DLL version.</span></span> <span data-ttu-id="2eb27-116">Per informazioni su come usare [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) per recuperare la versione corrente della dll, vedere [versioni della shell](common-control-versions.md) .</span><span class="sxs-lookup"><span data-stu-id="2eb27-116">See [Shell Versions](common-control-versions.md) for a discussion of how to use [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) to retrieve the current DLL version.</span></span>

> [!Note]  
> <span data-ttu-id="2eb27-117">Il numero di versione viene impostato su un controllo in base al controllo e potrebbe non essere lo stesso per tutti i controlli.</span><span class="sxs-lookup"><span data-stu-id="2eb27-117">The version number is set on a control by control basis, and may not be the same for all controls.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2eb27-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2eb27-118">Requirements</span></span>



| <span data-ttu-id="2eb27-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eb27-119">Requirement</span></span> | <span data-ttu-id="2eb27-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2eb27-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb27-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2eb27-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2eb27-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2eb27-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2eb27-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2eb27-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2eb27-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2eb27-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2eb27-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2eb27-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eb27-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2eb27-126"><dt>Commctrl.h</dt></span></span> </dl> |



 


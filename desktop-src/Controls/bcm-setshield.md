---
title: Messaggio BCM_SETSHIELD (COMmctrl. h)
description: Imposta lo stato di elevazione richieste per un pulsante o un collegamento di comando specificato per visualizzare un'icona con privilegi elevati. Inviare questo messaggio in modo esplicito o tramite il pulsante \_ SetElevationRequiredState macro.
ms.assetid: 2ce2a006-7136-415b-824b-46b282b100f4
keywords:
- Controlli di Windows Message BCM_SETSHIELD
topic_type:
- apiref
api_name:
- BCM_SETSHIELD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2149e2945f2876309459c287961b7b0a4a1f9acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119595"
---
# <a name="bcm_setshield-message"></a><span data-ttu-id="48dcc-105">\_Messaggio SESHIELD BCM</span><span class="sxs-lookup"><span data-stu-id="48dcc-105">BCM\_SETSHIELD message</span></span>

<span data-ttu-id="48dcc-106">Imposta lo stato di elevazione richieste per un pulsante o un collegamento di comando specificato per visualizzare un'icona con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="48dcc-106">Sets the elevation required state for a specified button or command link to display an elevated icon.</span></span> <span data-ttu-id="48dcc-107">Inviare questo messaggio in modo esplicito o tramite il [**pulsante \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) macro.</span><span class="sxs-lookup"><span data-stu-id="48dcc-107">Send this message explicitly or by using the [**Button\_SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="48dcc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="48dcc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48dcc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48dcc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48dcc-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="48dcc-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="48dcc-111">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48dcc-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48dcc-112">**Bool** che è **true** per creare un'icona con privilegi elevati o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="48dcc-112">A **BOOL** that is **TRUE** to draw an elevated icon, or **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48dcc-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="48dcc-113">Return value</span></span>

<span data-ttu-id="48dcc-114">Restituisce 1 se ha esito positivo o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="48dcc-114">Returns 1 if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="48dcc-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="48dcc-115">Remarks</span></span>

<span data-ttu-id="48dcc-116">Per ottenere questa funzionalità, è necessario manifestare un'applicazione per utilizzare comctl32.dll versione 6.</span><span class="sxs-lookup"><span data-stu-id="48dcc-116">An application must be manifested to use comctl32.dll version 6 to gain this functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="48dcc-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48dcc-117">Requirements</span></span>



| <span data-ttu-id="48dcc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="48dcc-118">Requirement</span></span> | <span data-ttu-id="48dcc-119">Valore</span><span class="sxs-lookup"><span data-stu-id="48dcc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48dcc-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48dcc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="48dcc-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48dcc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48dcc-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48dcc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="48dcc-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="48dcc-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="48dcc-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="48dcc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="48dcc-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="48dcc-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






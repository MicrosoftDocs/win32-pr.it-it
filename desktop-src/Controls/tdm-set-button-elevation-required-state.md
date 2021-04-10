---
title: Messaggio TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE (COMmctrl. h)
description: Specifica se un pulsante o un collegamento di comando di una determinata attività deve avere un'icona di schermatura controllo dell'account utente. ovvero se l'azione richiamata dal pulsante richiede l'elevazione dei privilegi.
ms.assetid: c4321fdb-3ea9-49bf-b53d-eb73d5b11084
keywords:
- Controlli di Windows Message TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE
topic_type:
- apiref
api_name:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5f8479e88a3b63cbd5fab6a5686913864fd9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121299"
---
# <a name="tdm_set_button_elevation_required_state-message"></a><span data-ttu-id="d26b3-104">\_Messaggio di \_ \_ \_ stato richiesta di elevazione del pulsante set TDM \_</span><span class="sxs-lookup"><span data-stu-id="d26b3-104">TDM\_SET\_BUTTON\_ELEVATION\_REQUIRED\_STATE message</span></span>

<span data-ttu-id="d26b3-105">Specifica se un pulsante o un collegamento di comando di una determinata attività deve avere un'icona di schermatura controllo dell'account utente. ovvero se l'azione richiamata dal pulsante richiede l'elevazione dei privilegi.</span><span class="sxs-lookup"><span data-stu-id="d26b3-105">Specifies whether a given task dialog button or command link should have a User Account Control (UAC) shield icon; that is, whether the action invoked by the button requires elevation.</span></span>

## <a name="parameters"></a><span data-ttu-id="d26b3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d26b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d26b3-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d26b3-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d26b3-108">ID del pulsante di push o del collegamento del comando da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="d26b3-108">The ID of the push button or command link to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="d26b3-109">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d26b3-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d26b3-110">Impostare su 0 per indicare che l'azione richiamata dal pulsante non richiede l'elevazione dei privilegi.</span><span class="sxs-lookup"><span data-stu-id="d26b3-110">Set to 0 to designate that the action invoked by the button does not require elevation.</span></span> <span data-ttu-id="d26b3-111">Impostare su un valore diverso da zero per indicare che l'azione richiede l'elevazione.</span><span class="sxs-lookup"><span data-stu-id="d26b3-111">Set to nonzero to designate that the action requires elevation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d26b3-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d26b3-112">Return value</span></span>

<span data-ttu-id="d26b3-113">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="d26b3-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="d26b3-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d26b3-114">Requirements</span></span>



| <span data-ttu-id="d26b3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d26b3-115">Requirement</span></span> | <span data-ttu-id="d26b3-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d26b3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d26b3-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d26b3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d26b3-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d26b3-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d26b3-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d26b3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d26b3-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d26b3-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d26b3-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d26b3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d26b3-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d26b3-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






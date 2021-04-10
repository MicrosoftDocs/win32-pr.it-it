---
title: Messaggio TDM_ENABLE_RADIO_BUTTON (COMmctrl. h)
description: Abilita o Disabilita un pulsante di opzione in una finestra di dialogo attività.
ms.assetid: da605ce0-b2d5-481a-a0e1-628ae5b65726
keywords:
- Controlli di Windows Message TDM_ENABLE_RADIO_BUTTON
topic_type:
- apiref
api_name:
- TDM_ENABLE_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a78445158c5edc920eb329cdfc52d44f9cb7d6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964850"
---
# <a name="tdm_enable_radio_button-message"></a><span data-ttu-id="6218f-104">TDM \_ Abilita \_ \_ messaggio pulsante di opzione</span><span class="sxs-lookup"><span data-stu-id="6218f-104">TDM\_ENABLE\_RADIO\_BUTTON message</span></span>

<span data-ttu-id="6218f-105">Abilita o Disabilita un pulsante di opzione in una finestra di dialogo attività.</span><span class="sxs-lookup"><span data-stu-id="6218f-105">Enables or disables a radio button in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="6218f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6218f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6218f-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6218f-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6218f-108">Valore **int** che specifica l'ID del pulsante di opzione da abilitare o disabilitare.</span><span class="sxs-lookup"><span data-stu-id="6218f-108">An **int** value that specifies the ID of the radio button to be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="6218f-109">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6218f-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6218f-110">Specifica lo stato del pulsante.</span><span class="sxs-lookup"><span data-stu-id="6218f-110">Specifies button state.</span></span> <span data-ttu-id="6218f-111">Impostare su 0 per disabilitare il pulsante. impostare su un valore diverso da zero per abilitare il pulsante.</span><span class="sxs-lookup"><span data-stu-id="6218f-111">Set to 0 to disable the button; set to nonzero to enable the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6218f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6218f-112">Return value</span></span>

<span data-ttu-id="6218f-113">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="6218f-113">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="6218f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6218f-114">Requirements</span></span>



| <span data-ttu-id="6218f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6218f-115">Requirement</span></span> | <span data-ttu-id="6218f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6218f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6218f-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6218f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6218f-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6218f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6218f-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6218f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6218f-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6218f-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6218f-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6218f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6218f-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6218f-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






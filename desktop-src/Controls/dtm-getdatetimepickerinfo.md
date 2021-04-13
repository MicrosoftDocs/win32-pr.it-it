---
title: Messaggio DTM_GETDATETIMEPICKERINFO (COMmctrl. h)
description: Ottiene informazioni su un controllo di selezione data e ora (DTP).
ms.assetid: 04847b68-ac45-4b28-8f62-2cd68ffe48d4
keywords:
- Controlli di Windows Message DTM_GETDATETIMEPICKERINFO
topic_type:
- apiref
api_name:
- DTM_GETDATETIMEPICKERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398a2543caa6d7104339fb8debd83fcee3ac71f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475406"
---
# <a name="dtm_getdatetimepickerinfo-message"></a><span data-ttu-id="3a99c-104">\_Messaggio GETDATETIMEPICKERINFO DTM</span><span class="sxs-lookup"><span data-stu-id="3a99c-104">DTM\_GETDATETIMEPICKERINFO message</span></span>

<span data-ttu-id="3a99c-105">Ottiene informazioni su un controllo di selezione data e ora (DTP).</span><span class="sxs-lookup"><span data-stu-id="3a99c-105">Gets information on a date and time picker (DTP) control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a99c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a99c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a99c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a99c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a99c-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3a99c-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3a99c-109">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a99c-109">*lParam* \[in\]</span></span>
</dt> <dd> <span data-ttu-id="3a99c-110">Puntatore a <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO**</a> per ricevere le informazioni.</span><span class="sxs-lookup"><span data-stu-id="3a99c-110">A pointer to <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO**</a> to receive the information.</span></span> <span data-ttu-id="3a99c-111">Il chiamante è responsabile dell'allocazione della memoria per questa struttura.</span><span class="sxs-lookup"><span data-stu-id="3a99c-111">The caller is responsible for allocating the memory for this structure.</span></span> <span data-ttu-id="3a99c-112">Impostare il membro **cbSize** della struttura su sizeof (DATETIMEPICKERINFO) prima di inviare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="3a99c-112">Set the **cbSize** member of the structure to sizeof(DATETIMEPICKERINFO) before sending this message.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a99c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a99c-113">Return value</span></span>

<span data-ttu-id="3a99c-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="3a99c-114">Return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a99c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a99c-115">Requirements</span></span>



| <span data-ttu-id="3a99c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a99c-116">Requirement</span></span> | <span data-ttu-id="3a99c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3a99c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a99c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a99c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3a99c-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a99c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a99c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a99c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3a99c-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3a99c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a99c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a99c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a99c-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a99c-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






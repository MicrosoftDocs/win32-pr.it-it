---
title: Messaggio UDM_GETRANGE (COMmctrl. h)
description: Recupera le posizioni minime e massime (intervallo) per un controllo di scorrimento.
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- Controlli di Windows Message UDM_GETRANGE
topic_type:
- apiref
api_name:
- UDM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6fd8467ad4494bea92a4c1f9a68d675ef1471f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225244"
---
# <a name="udm_getrange-message"></a><span data-ttu-id="1ee66-104">UDM \_ messaggio GETrange</span><span class="sxs-lookup"><span data-stu-id="1ee66-104">UDM\_GETRANGE message</span></span>

<span data-ttu-id="1ee66-105">Recupera le posizioni minime e massime (intervallo) per un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="1ee66-105">Retrieves the minimum and maximum positions (range) for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ee66-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ee66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ee66-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ee66-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1ee66-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1ee66-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1ee66-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ee66-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1ee66-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1ee66-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ee66-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ee66-111">Return value</span></span>

<span data-ttu-id="1ee66-112">Il valore restituito è un valore a 32 bit che contiene le posizioni minime e massime.</span><span class="sxs-lookup"><span data-stu-id="1ee66-112">The return value is a 32-bit value that contains the minimum and maximum positions.</span></span> <span data-ttu-id="1ee66-113">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è la posizione massima per il controllo e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è la posizione minima.</span><span class="sxs-lookup"><span data-stu-id="1ee66-113">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the maximum position for the control, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the minimum position.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ee66-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ee66-114">Requirements</span></span>



| <span data-ttu-id="1ee66-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ee66-115">Requirement</span></span> | <span data-ttu-id="1ee66-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1ee66-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ee66-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ee66-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1ee66-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ee66-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ee66-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ee66-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1ee66-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1ee66-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ee66-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ee66-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ee66-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ee66-122"><dt>Commctrl.h</dt></span></span> </dl> |



 


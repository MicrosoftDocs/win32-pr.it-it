---
title: Messaggio UDM_GETRANGE32 (COMmctrl. h)
description: Recupera l'intervallo di 32 bit di un controllo di scorrimento.
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- Controlli di Windows Message UDM_GETRANGE32
topic_type:
- apiref
api_name:
- UDM_GETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca418cd08dc4c81b3ff734d74f3ca9deeef7d848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476289"
---
# <a name="udm_getrange32-message"></a><span data-ttu-id="2c5df-104">\_Messaggio UDM GETRANGE32</span><span class="sxs-lookup"><span data-stu-id="2c5df-104">UDM\_GETRANGE32 message</span></span>

<span data-ttu-id="2c5df-105">Recupera l'intervallo di 32 bit di un controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="2c5df-105">Retrieves the 32-bit range of an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c5df-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c5df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c5df-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c5df-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c5df-108">Puntatore a un intero con segno che riceve il limite inferiore dell'intervallo di controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="2c5df-108">Pointer to a signed integer that receives the lower limit of the up-down control range.</span></span> <span data-ttu-id="2c5df-109">Questo parametro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="2c5df-109">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2c5df-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c5df-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c5df-111">Puntatore a un intero con segno che riceve il limite superiore dell'intervallo di controllo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="2c5df-111">Pointer to a signed integer that receives the upper limit of the up-down control range.</span></span> <span data-ttu-id="2c5df-112">Questo parametro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="2c5df-112">This parameter may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c5df-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2c5df-113">Return value</span></span>

<span data-ttu-id="2c5df-114">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="2c5df-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c5df-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c5df-115">Requirements</span></span>



| <span data-ttu-id="2c5df-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c5df-116">Requirement</span></span> | <span data-ttu-id="2c5df-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2c5df-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c5df-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c5df-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2c5df-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c5df-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c5df-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c5df-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2c5df-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2c5df-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c5df-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c5df-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c5df-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c5df-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Messaggio IPM_ISBLANK (COMmctrl. h)
description: Determina se tutti i campi nel controllo indirizzo IP sono vuoti.
ms.assetid: 6e35b848-943a-4475-890a-01fc3d8ed97d
keywords:
- Controlli di Windows Message IPM_ISBLANK
topic_type:
- apiref
api_name:
- IPM_ISBLANK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19f5a33ee3c35779a02cdfcb0fcb7066098f3160
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874117"
---
# <a name="ipm_isblank-message"></a><span data-ttu-id="64dc0-104">Messaggio di IPM \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="64dc0-104">IPM\_ISBLANK message</span></span>

<span data-ttu-id="64dc0-105">Determina se tutti i campi nel controllo indirizzo IP sono vuoti.</span><span class="sxs-lookup"><span data-stu-id="64dc0-105">Determines if all fields in the IP address control are blank.</span></span>

## <a name="parameters"></a><span data-ttu-id="64dc0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="64dc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64dc0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64dc0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="64dc0-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="64dc0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="64dc0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64dc0-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="64dc0-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="64dc0-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64dc0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64dc0-111">Return value</span></span>

<span data-ttu-id="64dc0-112">Restituisce un valore diverso da zero se tutti i campi sono vuoti oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="64dc0-112">Returns nonzero if all fields are blank, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="64dc0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64dc0-113">Requirements</span></span>



| <span data-ttu-id="64dc0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="64dc0-114">Requirement</span></span> | <span data-ttu-id="64dc0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="64dc0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64dc0-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64dc0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="64dc0-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="64dc0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="64dc0-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64dc0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="64dc0-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="64dc0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="64dc0-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64dc0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="64dc0-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="64dc0-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






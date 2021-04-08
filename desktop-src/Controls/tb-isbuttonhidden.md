---
title: Messaggio TB_ISBUTTONHIDDEN (COMmctrl. h)
description: Determina se il pulsante specificato in una barra degli strumenti è nascosto.
ms.assetid: 3372a64f-8209-4e3f-a6a9-8fe2e7e87ff2
keywords:
- Controlli di Windows Message TB_ISBUTTONHIDDEN
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIDDEN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db36f289a05fecfb2a0795965820324a9ce68057
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965000"
---
# <a name="tb_isbuttonhidden-message"></a><span data-ttu-id="988ae-104">TB \_ ISBUTTONHIDDEN messaggio</span><span class="sxs-lookup"><span data-stu-id="988ae-104">TB\_ISBUTTONHIDDEN message</span></span>

<span data-ttu-id="988ae-105">Determina se il pulsante specificato in una barra degli strumenti è nascosto.</span><span class="sxs-lookup"><span data-stu-id="988ae-105">Determines whether the specified button in a toolbar is hidden.</span></span>

## <a name="parameters"></a><span data-ttu-id="988ae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="988ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="988ae-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="988ae-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="988ae-108">Identificatore del comando del pulsante.</span><span class="sxs-lookup"><span data-stu-id="988ae-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="988ae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="988ae-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="988ae-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="988ae-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="988ae-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="988ae-111">Return value</span></span>

<span data-ttu-id="988ae-112">Restituisce un valore diverso da zero se il pulsante è nascosto oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="988ae-112">Returns nonzero if the button is hidden, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="988ae-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="988ae-113">Requirements</span></span>



| <span data-ttu-id="988ae-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="988ae-114">Requirement</span></span> | <span data-ttu-id="988ae-115">Valore</span><span class="sxs-lookup"><span data-stu-id="988ae-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="988ae-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="988ae-116">Minimum supported client</span></span><br/> | <span data-ttu-id="988ae-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="988ae-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="988ae-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="988ae-118">Minimum supported server</span></span><br/> | <span data-ttu-id="988ae-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="988ae-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="988ae-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="988ae-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="988ae-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="988ae-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






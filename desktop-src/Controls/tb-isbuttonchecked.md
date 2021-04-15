---
title: Messaggio TB_ISBUTTONCHECKED (COMmctrl. h)
description: Determina se il pulsante specificato in una barra degli strumenti è selezionato.
ms.assetid: ce576951-8db6-4854-8457-211ece018ce8
keywords:
- Controlli di Windows Message TB_ISBUTTONCHECKED
topic_type:
- apiref
api_name:
- TB_ISBUTTONCHECKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb9bc573478ea55ce8e0bda48ff16679b135fc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517590"
---
# <a name="tb_isbuttonchecked-message"></a><span data-ttu-id="afdc2-104">TB \_ ISBUTTONCHECKED messaggio</span><span class="sxs-lookup"><span data-stu-id="afdc2-104">TB\_ISBUTTONCHECKED message</span></span>

<span data-ttu-id="afdc2-105">Determina se il pulsante specificato in una barra degli strumenti è selezionato.</span><span class="sxs-lookup"><span data-stu-id="afdc2-105">Determines whether the specified button in a toolbar is checked.</span></span>

## <a name="parameters"></a><span data-ttu-id="afdc2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="afdc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afdc2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="afdc2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="afdc2-108">Identificatore del comando del pulsante.</span><span class="sxs-lookup"><span data-stu-id="afdc2-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="afdc2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="afdc2-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="afdc2-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="afdc2-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afdc2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="afdc2-111">Return value</span></span>

<span data-ttu-id="afdc2-112">Restituisce un valore diverso da zero se il pulsante è selezionato oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="afdc2-112">Returns nonzero if the button is checked, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="afdc2-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afdc2-113">Requirements</span></span>



| <span data-ttu-id="afdc2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="afdc2-114">Requirement</span></span> | <span data-ttu-id="afdc2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="afdc2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="afdc2-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afdc2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="afdc2-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="afdc2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="afdc2-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afdc2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="afdc2-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="afdc2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="afdc2-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="afdc2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="afdc2-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="afdc2-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






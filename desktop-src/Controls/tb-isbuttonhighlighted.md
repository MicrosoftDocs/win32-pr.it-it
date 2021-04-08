---
title: Messaggio TB_ISBUTTONHIGHLIGHTED (COMmctrl. h)
description: Controlla lo stato di evidenziazione di un pulsante della barra degli strumenti.
ms.assetid: d5aab670-a989-46f2-b4f8-d8a8968cbe07
keywords:
- Controlli di Windows Message TB_ISBUTTONHIGHLIGHTED
topic_type:
- apiref
api_name:
- TB_ISBUTTONHIGHLIGHTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53e25058fee8fa5dcac218a641277ac46aed4e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048120"
---
# <a name="tb_isbuttonhighlighted-message"></a><span data-ttu-id="4f477-104">TB \_ ISBUTTONHIGHLIGHTED messaggio</span><span class="sxs-lookup"><span data-stu-id="4f477-104">TB\_ISBUTTONHIGHLIGHTED message</span></span>

<span data-ttu-id="4f477-105">Controlla lo stato di evidenziazione di un pulsante della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="4f477-105">Checks the highlight state of a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="4f477-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f477-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f477-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f477-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f477-108">Identificatore del comando per un pulsante della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="4f477-108">Command identifier for a toolbar button.</span></span>

</dd> <dt>

<span data-ttu-id="4f477-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f477-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4f477-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4f477-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f477-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f477-111">Return value</span></span>

<span data-ttu-id="4f477-112">Restituisce un valore diverso da zero se il pulsante è evidenziato; in caso contrario, zero.</span><span class="sxs-lookup"><span data-stu-id="4f477-112">Returns nonzero if the button is highlighted, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f477-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f477-113">Requirements</span></span>



| <span data-ttu-id="4f477-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f477-114">Requirement</span></span> | <span data-ttu-id="4f477-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4f477-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f477-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f477-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4f477-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4f477-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4f477-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f477-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4f477-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4f477-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f477-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f477-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f477-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f477-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






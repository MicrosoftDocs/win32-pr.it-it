---
title: Messaggio TB_COMMANDTOINDEX (COMmctrl. h)
description: Recupera l'indice in base zero per il pulsante associato all'identificatore di comando specificato.
ms.assetid: vs|controls|~\controls\toolbar\messages\tb_commandtoindex.htm
keywords:
- Controlli di Windows Message TB_COMMANDTOINDEX
topic_type:
- apiref
api_name:
- TB_COMMANDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0257f55e01db59f1d23d59583f1ef78f44b1dac1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121722"
---
# <a name="tb_commandtoindex-message"></a><span data-ttu-id="6cc50-104">TB \_ COMMANDTOINDEX messaggio</span><span class="sxs-lookup"><span data-stu-id="6cc50-104">TB\_COMMANDTOINDEX message</span></span>

<span data-ttu-id="6cc50-105">Recupera l'indice in base zero per il pulsante associato all'identificatore di comando specificato.</span><span class="sxs-lookup"><span data-stu-id="6cc50-105">Retrieves the zero-based index for the button associated with the specified command identifier.</span></span>

## <a name="parameters"></a><span data-ttu-id="6cc50-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6cc50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cc50-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6cc50-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cc50-108">Identificatore di comando associato al pulsante.</span><span class="sxs-lookup"><span data-stu-id="6cc50-108">Command identifier associated with the button.</span></span>

</dd> <dt>

<span data-ttu-id="6cc50-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cc50-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6cc50-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6cc50-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cc50-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6cc50-111">Return value</span></span>

<span data-ttu-id="6cc50-112">Restituisce l'indice in base zero per il pulsante oppure-1 se l'identificatore di comando specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6cc50-112">Returns the zero-based index for the button or -1 if the specified command identifier is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cc50-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6cc50-113">Requirements</span></span>



| <span data-ttu-id="6cc50-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cc50-114">Requirement</span></span> | <span data-ttu-id="6cc50-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6cc50-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cc50-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6cc50-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6cc50-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6cc50-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cc50-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6cc50-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6cc50-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6cc50-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6cc50-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6cc50-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cc50-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cc50-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






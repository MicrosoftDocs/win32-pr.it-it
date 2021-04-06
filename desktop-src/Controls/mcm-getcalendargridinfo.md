---
title: Messaggio MCM_GETCALENDARGRIDINFO (COMmctrl. h)
description: Ottiene informazioni su una griglia di calendari.
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- Controlli di Windows Message MCM_GETCALENDARGRIDINFO
topic_type:
- apiref
api_name:
- MCM_GETCALENDARGRIDINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506f6193ab32d059bb85fa4583441bfbe027f224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743994"
---
# <a name="mcm_getcalendargridinfo-message"></a><span data-ttu-id="8dda0-104">\_Messaggio GETCALENDARGRIDINFO MCM</span><span class="sxs-lookup"><span data-stu-id="8dda0-104">MCM\_GETCALENDARGRIDINFO message</span></span>

<span data-ttu-id="8dda0-105">Ottiene informazioni su una griglia di calendari.</span><span class="sxs-lookup"><span data-stu-id="8dda0-105">Gets information about a calendar grid.</span></span>

## <a name="parameters"></a><span data-ttu-id="8dda0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8dda0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dda0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8dda0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8dda0-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8dda0-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8dda0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8dda0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8dda0-110">Puntatore a una struttura [**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) contenente informazioni sulla griglia del calendario.</span><span class="sxs-lookup"><span data-stu-id="8dda0-110">Pointer to an [**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo) structure that contains information about the calendar grid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dda0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8dda0-111">Return value</span></span>

<span data-ttu-id="8dda0-112">**True** se ha esito positivo, in caso contrario **false**.</span><span class="sxs-lookup"><span data-stu-id="8dda0-112">**TRUE** if successful, otherwise **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dda0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8dda0-113">Requirements</span></span>



| <span data-ttu-id="8dda0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dda0-114">Requirement</span></span> | <span data-ttu-id="8dda0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8dda0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8dda0-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8dda0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8dda0-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8dda0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8dda0-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8dda0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8dda0-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8dda0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8dda0-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8dda0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dda0-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dda0-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






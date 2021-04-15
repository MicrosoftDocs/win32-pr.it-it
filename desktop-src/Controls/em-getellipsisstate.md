---
title: Messaggio di EM_GETELLIPSISSTATE (RichEdit. h)
description: Recupera lo stato dei puntini di sospensione corrente.
ms.assetid: D02AE225-F5BF-401A-9877-55C68946CDBE
keywords:
- Controlli di Windows Message EM_GETELLIPSISSTATE
topic_type:
- apiref
api_name:
- EM_GETELLIPSISSTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 905bc8ecc180189f46e896aa0d9aaa3ba88b3f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476834"
---
# <a name="em_getellipsisstate-message"></a><span data-ttu-id="cd2f3-104">\_Messaggio GETELLIPSISSTATE em</span><span class="sxs-lookup"><span data-stu-id="cd2f3-104">EM\_GETELLIPSISSTATE message</span></span>

<span data-ttu-id="cd2f3-105">Recupera lo stato dei puntini di sospensione corrente.</span><span class="sxs-lookup"><span data-stu-id="cd2f3-105">Retrieves the current ellipsis state.</span></span>


```C++
#define EM_GETELLIPSISSTATE       (WM_USER + 322)
```



## <a name="parameters"></a><span data-ttu-id="cd2f3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd2f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd2f3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd2f3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd2f3-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cd2f3-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cd2f3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd2f3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd2f3-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cd2f3-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd2f3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd2f3-111">Return value</span></span>

<span data-ttu-id="cd2f3-112">Il valore restituito è TRUE se i puntini di sospensione vengono visualizzati e FALSE in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cd2f3-112">The return value is TRUE if an ellipsis is being displayed and FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd2f3-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd2f3-113">Requirements</span></span>



| <span data-ttu-id="cd2f3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd2f3-114">Requirement</span></span> | <span data-ttu-id="cd2f3-115">Valore</span><span class="sxs-lookup"><span data-stu-id="cd2f3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd2f3-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd2f3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cd2f3-117">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cd2f3-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cd2f3-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd2f3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cd2f3-119">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cd2f3-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd2f3-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd2f3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd2f3-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd2f3-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd2f3-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd2f3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd2f3-123">**\_GETELLIPSISMODE em**</span><span class="sxs-lookup"><span data-stu-id="cd2f3-123">**EM\_GETELLIPSISMODE**</span></span>](em-getellipsismode.md)
</dt> <dt>

[<span data-ttu-id="cd2f3-124">**\_SETELLIPSISMODE em**</span><span class="sxs-lookup"><span data-stu-id="cd2f3-124">**EM\_SETELLIPSISMODE**</span></span>](em-setellipsismode.md)
</dt> </dl>

 

 






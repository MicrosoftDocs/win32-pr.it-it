---
title: Messaggio DM_REPOSITION (winuser. h)
description: Riposiziona una finestra di dialogo di primo livello in modo che rientri nell'area del desktop. Un'applicazione può inviare questo messaggio a una finestra di dialogo dopo il ridimensionamento per garantire che l'intera finestra di dialogo rimanga visibile.
ms.assetid: 8386d23e-06ea-4ea7-adde-ac97fc97861d
keywords:
- Finestre di dialogo DM_REPOSITION messaggio
topic_type:
- apiref
api_name:
- DM_REPOSITION
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19425d4d77a62117f3fadfdd98f0629b81bf334c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048719"
---
# <a name="dm_reposition-message"></a><span data-ttu-id="465c5-105">\_Messaggio di riposizionamento DM</span><span class="sxs-lookup"><span data-stu-id="465c5-105">DM\_REPOSITION message</span></span>

<span data-ttu-id="465c5-106">Riposiziona una finestra di dialogo di primo livello in modo che rientri nell'area del desktop.</span><span class="sxs-lookup"><span data-stu-id="465c5-106">Repositions a top-level dialog box so that it fits within the desktop area.</span></span> <span data-ttu-id="465c5-107">Un'applicazione può inviare questo messaggio a una finestra di dialogo dopo il ridimensionamento per garantire che l'intera finestra di dialogo rimanga visibile.</span><span class="sxs-lookup"><span data-stu-id="465c5-107">An application can send this message to a dialog box after resizing it to ensure that the entire dialog box remains visible.</span></span>


```C++
#define WM_USER              0x0400
#define DM_REPOSITION       (WM_USER+2)
```



## <a name="parameters"></a><span data-ttu-id="465c5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="465c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="465c5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="465c5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="465c5-110">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="465c5-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="465c5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="465c5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="465c5-112">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="465c5-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="465c5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="465c5-113">Return value</span></span>

<span data-ttu-id="465c5-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="465c5-114">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="465c5-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="465c5-115">Remarks</span></span>

<span data-ttu-id="465c5-116">Questo messaggio non ha alcun effetto se la finestra di dialogo è una finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="465c5-116">This message has no effect if the dialog box is a child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="465c5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="465c5-117">Requirements</span></span>



| <span data-ttu-id="465c5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="465c5-118">Requirement</span></span> | <span data-ttu-id="465c5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="465c5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="465c5-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="465c5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="465c5-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="465c5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="465c5-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="465c5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="465c5-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="465c5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="465c5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="465c5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="465c5-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="465c5-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="465c5-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="465c5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="465c5-127">Cenni preliminari sulle finestre di dialogo</span><span class="sxs-lookup"><span data-stu-id="465c5-127">Dialog Boxes Overview</span></span>](dialog-boxes.md)
</dt> </dl>

 

 






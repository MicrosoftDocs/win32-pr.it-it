---
description: Recupera l'handle di menu per la finestra corrente.
ms.assetid: a2f6e917-39ff-42a3-8ff4-ce01db3ef9ea
title: Messaggio MN_GETHMENU (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64d501654af426a292156d05242b372336eee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231583"
---
# <a name="mn_gethmenu-message"></a><span data-ttu-id="f8183-103">\_Messaggio GETHMENU MN</span><span class="sxs-lookup"><span data-stu-id="f8183-103">MN\_GETHMENU message</span></span>

<span data-ttu-id="f8183-104">Recupera l'handle di menu per la finestra corrente.</span><span class="sxs-lookup"><span data-stu-id="f8183-104">Retrieves the menu handle for the current window.</span></span>


```C++
#define MN_GETHMENU                     0x01E1
```



## <a name="parameters"></a><span data-ttu-id="f8183-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8183-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8183-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8183-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8183-107">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="f8183-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f8183-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8183-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8183-109">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="f8183-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8183-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8183-110">Return value</span></span>

<span data-ttu-id="f8183-111">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="f8183-111">Type: **HMENU**</span></span>

<span data-ttu-id="f8183-112">In caso di esito positivo, il valore restituito è **HMENU** per la finestra corrente.</span><span class="sxs-lookup"><span data-stu-id="f8183-112">If successful, the return value is the **HMENU** for the current window.</span></span> <span data-ttu-id="f8183-113">Se ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="f8183-113">If it fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8183-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8183-114">Requirements</span></span>



| <span data-ttu-id="f8183-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8183-115">Requirement</span></span> | <span data-ttu-id="f8183-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f8183-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8183-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8183-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f8183-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f8183-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f8183-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8183-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f8183-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f8183-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f8183-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8183-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8183-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8183-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





---
title: Tipi di dati del registro eventi di Windows (WinEvt. h)
description: Il registro eventi di Windows definisce i tipi di dati seguenti
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a93794d8cc3a254fe182c439698324dccdfc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741386"
---
# <a name="windows-event-log-data-types"></a><span data-ttu-id="0c3fe-106">Tipi di dati del registro eventi di Windows</span><span class="sxs-lookup"><span data-stu-id="0c3fe-106">Windows Event Log Data Types</span></span>

<span data-ttu-id="0c3fe-107">Nel registro eventi di Windows sono definiti i tipi di dati seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c3fe-107">Windows Event Log defines the following data types:</span></span>


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

<span data-ttu-id="0c3fe-108">**\_handle evt**</span><span class="sxs-lookup"><span data-stu-id="0c3fe-108">**EVT\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="0c3fe-109">Handle per un oggetto registro eventi di Windows.</span><span class="sxs-lookup"><span data-stu-id="0c3fe-109">A handle to a Windows Event Log object.</span></span>

</dd> <dt>

<span data-ttu-id="0c3fe-110">**\_handle PEVT**</span><span class="sxs-lookup"><span data-stu-id="0c3fe-110">**PEVT\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="0c3fe-111">Puntatore all'handle di un oggetto registro eventi di Windows.</span><span class="sxs-lookup"><span data-stu-id="0c3fe-111">A pointer to the handle of a Windows Event Log object.</span></span>

</dd> <dt>

<span data-ttu-id="0c3fe-112">**\_ \_ \_ Handle proprietà matrice di oggetti evt \_**</span><span class="sxs-lookup"><span data-stu-id="0c3fe-112">**EVT\_OBJECT\_ARRAY\_PROPERTY\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="0c3fe-113">Handle per una matrice di oggetti del registro eventi di Windows.</span><span class="sxs-lookup"><span data-stu-id="0c3fe-113">A handle to an array of Windows Event Log objects.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c3fe-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c3fe-114">Requirements</span></span>



| <span data-ttu-id="0c3fe-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c3fe-115">Requirement</span></span> | <span data-ttu-id="0c3fe-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0c3fe-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0c3fe-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c3fe-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0c3fe-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c3fe-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0c3fe-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c3fe-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0c3fe-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c3fe-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0c3fe-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c3fe-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c3fe-122"><dt>WinEvt. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c3fe-122"><dt>WinEvt.h</dt></span></span> </dl> |



 

 






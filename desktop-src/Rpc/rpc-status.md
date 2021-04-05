---
title: RPC_STATUS (rpcdce. h)
description: Lo stato RPC del tipo \_ di dati rappresenta un tipo di codice di stato specifico della piattaforma.
ms.assetid: 0f929916-f3aa-477f-9c61-742f3fbbab29
keywords:
- RPC_STATUS
- RPC_STATUS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066022ce33676caadcf25a6814f3b4974701998e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048330"
---
# <a name="rpc_status"></a><span data-ttu-id="2f7af-105">\_stato RPC</span><span class="sxs-lookup"><span data-stu-id="2f7af-105">RPC\_STATUS</span></span>

<span data-ttu-id="2f7af-106">Lo **\_ stato RPC** del tipo di dati rappresenta un tipo di codice di stato specifico della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="2f7af-106">The data type **RPC\_STATUS** represents a platform-specific status code type.</span></span>


```C++
typedef long RPC_STATUS;
typedef unsigned short RPC_STATUS;
```



## <a name="remarks"></a><span data-ttu-id="2f7af-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f7af-107">Remarks</span></span>

<span data-ttu-id="2f7af-108">Il tipo di **\_ stato RPC** viene restituito dalla maggior parte delle funzioni RPC ed è parte della definizione del tipo di funzione [**\_ \_ INQ \_ FN dell'oggetto RPC**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) .</span><span class="sxs-lookup"><span data-stu-id="2f7af-108">The **RPC\_STATUS** type is returned by most RPC functions and is part of the [**RPC\_OBJECT\_INQ\_FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) function type definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f7af-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f7af-109">Requirements</span></span>



| <span data-ttu-id="2f7af-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f7af-110">Requirement</span></span> | <span data-ttu-id="2f7af-111">Valore</span><span class="sxs-lookup"><span data-stu-id="2f7af-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f7af-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f7af-112">Minimum supported client</span></span><br/> | <span data-ttu-id="2f7af-113">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f7af-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2f7af-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f7af-114">Minimum supported server</span></span><br/> | <span data-ttu-id="2f7af-115">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f7af-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2f7af-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f7af-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f7af-117"><dt>Rpcdce. h (include RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f7af-117"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f7af-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f7af-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f7af-119">**\_oggetto RPC \_ INQ \_ FN**</span><span class="sxs-lookup"><span data-stu-id="2f7af-119">**RPC\_OBJECT\_INQ\_FN**</span></span>](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)
</dt> </dl>

 

 






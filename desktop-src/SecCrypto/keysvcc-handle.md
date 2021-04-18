---
description: Il \_ tipo di dati dell'handle KEYSVCC definisce un handle del servizio Key. Un \_ handle di handle KEYSVCC viene usato dalle funzioni RKeyOpenKeyService e RKeyCloseKeyService.
ms.assetid: d0fd5184-5c8e-4f96-9ff1-8abd6f718d05
title: KEYSVCC_HANDLE (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1427a4ffd4637e073e517e5df54af72191992d11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316658"
---
# <a name="keysvcc_handle"></a><span data-ttu-id="d3417-104">\_handle KEYSVCC</span><span class="sxs-lookup"><span data-stu-id="d3417-104">KEYSVCC\_HANDLE</span></span>

<span data-ttu-id="d3417-105">Il tipo di dati dell' **\_ handle KEYSVCC** definisce un handle del servizio Key.</span><span class="sxs-lookup"><span data-stu-id="d3417-105">The **KEYSVCC\_HANDLE** data type defines a key service handle.</span></span> <span data-ttu-id="d3417-106">Un handle di **\_ handle KEYSVCC** viene usato dalle funzioni [**RKeyOpenKeyService**](rkeyopenkeyservice.md) e [**RKeyCloseKeyService**](rkeyclosekeyservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d3417-106">A **KEYSVCC\_HANDLE** handle is used by the [**RKeyOpenKeyService**](rkeyopenkeyservice.md) and [**RKeyCloseKeyService**](rkeyclosekeyservice.md) functions.</span></span>


```C++
typedef void* KEYSVCC_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="d3417-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3417-107">Requirements</span></span>



| <span data-ttu-id="d3417-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3417-108">Requirement</span></span> | <span data-ttu-id="d3417-109">Valore</span><span class="sxs-lookup"><span data-stu-id="d3417-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3417-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3417-110">Minimum supported client</span></span><br/> | <span data-ttu-id="d3417-111">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d3417-111">None supported</span></span><br/>                                                             |
| <span data-ttu-id="d3417-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3417-112">Minimum supported server</span></span><br/> | <span data-ttu-id="d3417-113">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3417-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3417-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3417-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3417-115"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3417-115"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3417-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3417-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3417-117">**RKeyCloseKeyService**</span><span class="sxs-lookup"><span data-stu-id="d3417-117">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="d3417-118">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="d3417-118">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 





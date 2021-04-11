---
description: Specifica i byte crittografati in una superficie video protetta.
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
title: Struttura D3DENCRYPTED_BLOCK_INFO (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DENCRYPTED_BLOCK_INFO
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21864dcc41ce86f139361af4357810137acf7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127918"
---
# <a name="d3dencrypted_block_info-structure"></a><span data-ttu-id="130a9-103">Struttura delle informazioni sul \_ blocco D3DENCRYPTED \_</span><span class="sxs-lookup"><span data-stu-id="130a9-103">D3DENCRYPTED\_BLOCK\_INFO structure</span></span>

<span data-ttu-id="130a9-104">Specifica i byte crittografati in una superficie video protetta.</span><span class="sxs-lookup"><span data-stu-id="130a9-104">Specifies which bytes are encrypted in a protected video surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="130a9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="130a9-105">Syntax</span></span>


```C++
typedef struct _D3DENCRYPTED_BLOCK_INFO {
  UINT NumEncryptedBytesAtBeginning;
  UINT NumBytesInSkipPattern;
  UINT NumBytesInEncryptPattern;
} D3DENCRYPTED_BLOCK_INFO;
```



## <a name="members"></a><span data-ttu-id="130a9-106">Members</span><span class="sxs-lookup"><span data-stu-id="130a9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="130a9-107">**NumEncryptedBytesAtBeginning**</span><span class="sxs-lookup"><span data-stu-id="130a9-107">**NumEncryptedBytesAtBeginning**</span></span>
</dt> <dd>

<span data-ttu-id="130a9-108">Numero di byte crittografati all'inizio del buffer.</span><span class="sxs-lookup"><span data-stu-id="130a9-108">The number of bytes that are encrypted at the start of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="130a9-109">**NumBytesInSkipPattern**</span><span class="sxs-lookup"><span data-stu-id="130a9-109">**NumBytesInSkipPattern**</span></span>
</dt> <dd>

<span data-ttu-id="130a9-110">Il numero di byte che vengono ignorati dopo i primi **NumEncryptedBytesAtBeginning** byte e quindi dopo ogni blocco di **NumBytesInEncryptPattern** byte.</span><span class="sxs-lookup"><span data-stu-id="130a9-110">The number of bytes that are skipped after the first **NumEncryptedBytesAtBeginning** bytes, and then after each block of **NumBytesInEncryptPattern** bytes.</span></span> <span data-ttu-id="130a9-111">I byte ignorati non sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="130a9-111">Skipped bytes are not encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="130a9-112">**NumBytesInEncryptPattern**</span><span class="sxs-lookup"><span data-stu-id="130a9-112">**NumBytesInEncryptPattern**</span></span>
</dt> <dd>

<span data-ttu-id="130a9-113">Numero di byte crittografati dopo ogni blocco di byte ignorati.</span><span class="sxs-lookup"><span data-stu-id="130a9-113">The number of bytes that are encrypted after each block of skipped bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="130a9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="130a9-114">Requirements</span></span>



| <span data-ttu-id="130a9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="130a9-115">Requirement</span></span> | <span data-ttu-id="130a9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="130a9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="130a9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="130a9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="130a9-118">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="130a9-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="130a9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="130a9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="130a9-120">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="130a9-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="130a9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="130a9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="130a9-122"><dt>D3d9types. h (include d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="130a9-122"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="130a9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="130a9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="130a9-124">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="130a9-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 





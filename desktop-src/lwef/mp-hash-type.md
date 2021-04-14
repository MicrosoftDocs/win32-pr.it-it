---
title: Enumerazione MP_HASH_TYPE (MpClient. h)
description: Tipi hash possibili.
ms.assetid: 46432C40-6DE1-4FB8-B7C1-C2712CCEB208
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MP_HASH_TYPE
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMP_HASH_TYPE
topic_type:
- apiref
api_name:
- MP_HASH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40c36e709d165845b729673df4aaea1042a7ee49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478748"
---
# <a name="mp_hash_type-enumeration"></a><span data-ttu-id="dd701-105">Enumerazione del tipo di \_ hash MP \_</span><span class="sxs-lookup"><span data-stu-id="dd701-105">MP\_HASH\_TYPE enumeration</span></span>

<span data-ttu-id="dd701-106">Tipi hash possibili.</span><span class="sxs-lookup"><span data-stu-id="dd701-106">Possible hash types.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd701-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd701-107">Syntax</span></span>


```C++
typedef enum tagMP_HASH_TYPE { 
  MP_HASH_TYPE_NONE    = 0,
  MP_HASH_TYPE_CRC32   = 2,
  MP_HASH_TYPE_MD5     = 4,
  MP_HASH_TYPE_SHA1    = 8,
  MP_HASH_TYPE_SHA256  = 16
} MP_HASH_TYPE, *PMP_HASH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="dd701-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="dd701-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dd701-109"><span id="MP_HASH_TYPE_NONE"></span><span id="mp_hash_type_none"></span>**\_tipo di hash MP \_ \_ None**</span><span class="sxs-lookup"><span data-stu-id="dd701-109"><span id="MP_HASH_TYPE_NONE"></span><span id="mp_hash_type_none"></span>**MP\_HASH\_TYPE\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="dd701-110">Nessun hash.</span><span class="sxs-lookup"><span data-stu-id="dd701-110">No hash.</span></span>

</dd> <dt>

<span data-ttu-id="dd701-111"><span id="MP_HASH_TYPE_CRC32"></span><span id="mp_hash_type_crc32"></span>**\_Tipo di hash MP \_ \_ CRC32**</span><span class="sxs-lookup"><span data-stu-id="dd701-111"><span id="MP_HASH_TYPE_CRC32"></span><span id="mp_hash_type_crc32"></span>**MP\_HASH\_TYPE\_CRC32**</span></span>
</dt> <dd>

<span data-ttu-id="dd701-112">CRC32</span><span class="sxs-lookup"><span data-stu-id="dd701-112">CRC32</span></span>

</dd> <dt>

<span data-ttu-id="dd701-113"><span id="MP_HASH_TYPE_MD5"></span><span id="mp_hash_type_md5"></span>**\_Tipo di hash MP \_ \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="dd701-113"><span id="MP_HASH_TYPE_MD5"></span><span id="mp_hash_type_md5"></span>**MP\_HASH\_TYPE\_MD5**</span></span>
</dt> <dd>

<span data-ttu-id="dd701-114">MD5</span><span class="sxs-lookup"><span data-stu-id="dd701-114">MD5</span></span>

</dd> <dt>

<span data-ttu-id="dd701-115"><span id="MP_HASH_TYPE_SHA1"></span><span id="mp_hash_type_sha1"></span>**\_Tipo di hash MP \_ \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="dd701-115"><span id="MP_HASH_TYPE_SHA1"></span><span id="mp_hash_type_sha1"></span>**MP\_HASH\_TYPE\_SHA1**</span></span>
</dt> <dd>

<span data-ttu-id="dd701-116">SHA1</span><span class="sxs-lookup"><span data-stu-id="dd701-116">SHA1</span></span>

</dd> <dt>

<span data-ttu-id="dd701-117"><span id="MP_HASH_TYPE_SHA256"></span><span id="mp_hash_type_sha256"></span>**\_Tipo di hash MP \_ \_ SHA256**</span><span class="sxs-lookup"><span data-stu-id="dd701-117"><span id="MP_HASH_TYPE_SHA256"></span><span id="mp_hash_type_sha256"></span>**MP\_HASH\_TYPE\_SHA256**</span></span>
</dt> <dd>

<span data-ttu-id="dd701-118">SHA 256</span><span class="sxs-lookup"><span data-stu-id="dd701-118">SHA 256</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd701-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd701-119">Requirements</span></span>



| <span data-ttu-id="dd701-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd701-120">Requirement</span></span> | <span data-ttu-id="dd701-121">Valore</span><span class="sxs-lookup"><span data-stu-id="dd701-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd701-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd701-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dd701-123">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dd701-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="dd701-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd701-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dd701-125">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dd701-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd701-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd701-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd701-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd701-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 






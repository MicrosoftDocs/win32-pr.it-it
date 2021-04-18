---
description: L' \_ enumerazione dell'algoritmo hash CAPICOM \_ definisce un algoritmo hash.
ms.assetid: 5373b6cc-944a-4d83-ac71-59edcb2af94e
title: Enumerazione CAPICOM_HASH_ALGORITHM (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_HASH_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 14ee06437f7b6e32c58415e5b9d77a75929250a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327645"
---
# <a name="capicom_hash_algorithm-enumeration"></a><span data-ttu-id="b1e31-103">\_Enumerazione dell'algoritmo hash \_ capicol</span><span class="sxs-lookup"><span data-stu-id="b1e31-103">CAPICOM\_HASH\_ALGORITHM enumeration</span></span>

<span data-ttu-id="b1e31-104">L'enumerazione dell' **\_ \_ algoritmo hash CAPICOM** definisce un algoritmo hash.</span><span class="sxs-lookup"><span data-stu-id="b1e31-104">The **CAPICOM\_HASH\_ALGORITHM** enumeration defines a hash algorithm.</span></span>

## <a name="members"></a><span data-ttu-id="b1e31-105">Membri</span><span class="sxs-lookup"><span data-stu-id="b1e31-105">Members</span></span>



| <span data-ttu-id="b1e31-106">Membro</span><span class="sxs-lookup"><span data-stu-id="b1e31-106">Member</span></span>                                 | <span data-ttu-id="b1e31-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1e31-107">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="b1e31-108">Valore</span><span class="sxs-lookup"><span data-stu-id="b1e31-108">Value</span></span> |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="b1e31-109">**Algoritmo hash capicot \_ \_ \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="b1e31-109">**CAPICOM\_HASH\_ALGORITHM\_SHA1**</span></span>     | <span data-ttu-id="b1e31-110">Sha ( [*Secure Hash Algorithm*](../secgloss/s-gly.md) ) che genera un digest del messaggio a 160 bit.</span><span class="sxs-lookup"><span data-stu-id="b1e31-110">[*Secure Hash Algorithm*](../secgloss/s-gly.md) (SHA) that generates a 160-bit message digest.</span></span><br/> | <span data-ttu-id="b1e31-111">0</span><span class="sxs-lookup"><span data-stu-id="b1e31-111">0</span></span>     |
| <span data-ttu-id="b1e31-112">**\_Algoritmo hash CAPICOM \_ \_ MD2**</span><span class="sxs-lookup"><span data-stu-id="b1e31-112">**CAPICOM\_HASH\_ALGORITHM\_MD2**</span></span>      | <span data-ttu-id="b1e31-113">Algoritmo di hash MD2.</span><span class="sxs-lookup"><span data-stu-id="b1e31-113">MD2 hashing algorithm.</span></span><br/>                                                                                                                                           | <span data-ttu-id="b1e31-114">1</span><span class="sxs-lookup"><span data-stu-id="b1e31-114">1</span></span>     |
| <span data-ttu-id="b1e31-115">**\_Algoritmo hash CAPICOM \_ \_ MD4**</span><span class="sxs-lookup"><span data-stu-id="b1e31-115">**CAPICOM\_HASH\_ALGORITHM\_MD4**</span></span>      | <span data-ttu-id="b1e31-116">Algoritmo di hash MD4.</span><span class="sxs-lookup"><span data-stu-id="b1e31-116">MD4 hashing algorithm.</span></span><br/>                                                                                                                                           | <span data-ttu-id="b1e31-117">2</span><span class="sxs-lookup"><span data-stu-id="b1e31-117">2</span></span>     |
| <span data-ttu-id="b1e31-118">**Algoritmo hash capicol \_ \_ \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="b1e31-118">**CAPICOM\_HASH\_ALGORITHM\_MD5**</span></span>      | <span data-ttu-id="b1e31-119">Algoritmo di hash MD5.</span><span class="sxs-lookup"><span data-stu-id="b1e31-119">MD5 hashing algorithm.</span></span><br/>                                                                                                                                           | <span data-ttu-id="b1e31-120">3</span><span class="sxs-lookup"><span data-stu-id="b1e31-120">3</span></span>     |
| <span data-ttu-id="b1e31-121">**Algoritmo hash capicol \_ \_ \_ Sha \_ 256**</span><span class="sxs-lookup"><span data-stu-id="b1e31-121">**CAPICOM\_HASH\_ALGORITHM\_SHA\_256**</span></span> | <span data-ttu-id="b1e31-122">Algoritmo hash SHA-256.</span><span class="sxs-lookup"><span data-stu-id="b1e31-122">SHA-256 hash algorithm.</span></span><br/> <span data-ttu-id="b1e31-123">**CAPICOM 2.0.0.3 e versioni precedenti:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b1e31-123">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/>                                                                 | <span data-ttu-id="b1e31-124">4</span><span class="sxs-lookup"><span data-stu-id="b1e31-124">4</span></span>     |
| <span data-ttu-id="b1e31-125">**Algoritmo hash capicol \_ \_ \_ Sha \_ 384**</span><span class="sxs-lookup"><span data-stu-id="b1e31-125">**CAPICOM\_HASH\_ALGORITHM\_SHA\_384**</span></span> | <span data-ttu-id="b1e31-126">Algoritmo hash SHA-384.</span><span class="sxs-lookup"><span data-stu-id="b1e31-126">SHA-384 hash algorithm.</span></span><br/> <span data-ttu-id="b1e31-127">**CAPICOM 2.0.0.3 e versioni precedenti:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b1e31-127">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/>                                                                 | <span data-ttu-id="b1e31-128">5</span><span class="sxs-lookup"><span data-stu-id="b1e31-128">5</span></span>     |
| <span data-ttu-id="b1e31-129">**Algoritmo hash capicol \_ \_ \_ Sha \_ 512**</span><span class="sxs-lookup"><span data-stu-id="b1e31-129">**CAPICOM\_HASH\_ALGORITHM\_SHA\_512**</span></span> | <span data-ttu-id="b1e31-130">Algoritmo hash SHA-512.</span><span class="sxs-lookup"><span data-stu-id="b1e31-130">SHA-512 hash algorithm.</span></span><br/> <span data-ttu-id="b1e31-131">**CAPICOM 2.0.0.3 e versioni precedenti:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b1e31-131">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/>                                                                 | <span data-ttu-id="b1e31-132">6</span><span class="sxs-lookup"><span data-stu-id="b1e31-132">6</span></span>     |



## <a name="remarks"></a><span data-ttu-id="b1e31-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1e31-133">Remarks</span></span>

<span data-ttu-id="b1e31-134">L'enumerazione dell' **\_ \_ algoritmo hash CAPICOM** viene utilizzata dalla proprietà [**HashedData. Algorithm**](hasheddata-algorithm.md) .</span><span class="sxs-lookup"><span data-stu-id="b1e31-134">The **CAPICOM\_HASH\_ALGORITHM** enumeration is used by the [**HashedData.Algorithm**](hasheddata-algorithm.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1e31-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1e31-135">Requirements</span></span>



| <span data-ttu-id="b1e31-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1e31-136">Requirement</span></span> | <span data-ttu-id="b1e31-137">Valore</span><span class="sxs-lookup"><span data-stu-id="b1e31-137">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b1e31-138">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b1e31-138">Redistributable</span></span><br/> | <span data-ttu-id="b1e31-139">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1e31-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="b1e31-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1e31-140">Header</span></span><br/>          | <dl> <span data-ttu-id="b1e31-141"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1e31-141"><dt>Capicom.h</dt></span></span> </dl> |



 

 

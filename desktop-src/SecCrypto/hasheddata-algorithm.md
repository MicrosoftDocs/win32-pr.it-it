---
description: Imposta o Recupera il tipo di algoritmo di hash utilizzato.
ms.assetid: 3f8e83f2-0e46-494b-ac63-658e663680ea
title: Proprietà HashedData. Algorithm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a27dc275ce900bfd6412599cb81ad14038f96405
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325600"
---
# <a name="hasheddataalgorithm-property"></a><span data-ttu-id="70478-103">Proprietà HashedData. Algorithm</span><span class="sxs-lookup"><span data-stu-id="70478-103">HashedData.Algorithm property</span></span>

<span data-ttu-id="70478-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="70478-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="70478-105">Usare invece la [**classe HashAlgorithm**](/previous-versions/windows/) nello spazio dei nomi [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="70478-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="70478-106">La proprietà **Algorithm** imposta o Recupera il tipo di algoritmo hash utilizzato.</span><span class="sxs-lookup"><span data-stu-id="70478-106">The **Algorithm** property sets or retrieves the type of hashing algorithm used.</span></span>

## <a name="syntax"></a><span data-ttu-id="70478-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70478-107">Syntax</span></span>


```VB
HashedData.Algorithm As CAPICOM_HASH_ALGORITHM
```



## <a name="property-value"></a><span data-ttu-id="70478-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="70478-108">Property value</span></span>

<span data-ttu-id="70478-109">Valore dell'enumerazione dell' [**\_ \_ algoritmo hash CAPICOM**](capicom-hash-algorithm.md) che definisce un algoritmo hash.</span><span class="sxs-lookup"><span data-stu-id="70478-109">A value of the [**CAPICOM\_HASH\_ALGORITHM**](capicom-hash-algorithm.md) enumeration that defines a hash algorithm.</span></span> <span data-ttu-id="70478-110">Il valore predefinito è l'algoritmo hash capicol \_ \_ \_ SHA1.</span><span class="sxs-lookup"><span data-stu-id="70478-110">The default value is CAPICOM\_HASH\_ALGORITHM\_SHA1.</span></span> <span data-ttu-id="70478-111">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="70478-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="70478-112">Valore</span><span class="sxs-lookup"><span data-stu-id="70478-112">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="70478-113">Significato</span><span class="sxs-lookup"><span data-stu-id="70478-113">Meaning</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_HASH_ALGORITHM_SHA1"></span><span id="capicom_hash_algorithm_sha1"></span><dl> <span data-ttu-id="70478-114"><dt>**Algoritmo hash capicot \_ \_ \_ SHA1**</dt></span><span class="sxs-lookup"><span data-stu-id="70478-114"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA1**</dt></span></span> </dl>           | <span data-ttu-id="70478-115">Algoritmo di hash SHA1.</span><span class="sxs-lookup"><span data-stu-id="70478-115">SHA1 hashing algorithm.</span></span><br/>                                                                          |
| <span id="CAPICOM_HASH_ALGORITHM_MD2"></span><span id="capicom_hash_algorithm_md2"></span><dl> <span data-ttu-id="70478-116"><dt>**\_Algoritmo hash CAPICOM \_ \_ MD2**</dt></span><span class="sxs-lookup"><span data-stu-id="70478-116"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD2**</dt></span></span> </dl>              | <span data-ttu-id="70478-117">Algoritmo di hash MD2.</span><span class="sxs-lookup"><span data-stu-id="70478-117">MD2 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD4"></span><span id="capicom_hash_algorithm_md4"></span><dl> <span data-ttu-id="70478-118"><dt>**\_Algoritmo hash CAPICOM \_ \_ MD4**</dt></span><span class="sxs-lookup"><span data-stu-id="70478-118"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD4**</dt></span></span> </dl>              | <span data-ttu-id="70478-119">Algoritmo di hash MD4.</span><span class="sxs-lookup"><span data-stu-id="70478-119">MD4 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD5"></span><span id="capicom_hash_algorithm_md5"></span><dl> <span data-ttu-id="70478-120"><dt>**Algoritmo hash capicol \_ \_ \_ MD5**</dt></span><span class="sxs-lookup"><span data-stu-id="70478-120"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD5**</dt></span></span> </dl>              | <span data-ttu-id="70478-121">Algoritmo di hash MD5.</span><span class="sxs-lookup"><span data-stu-id="70478-121">MD5 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_256"></span><span id="capicom_hash_algorithm_sha_256"></span><dl> <span data-ttu-id="70478-122"><dt>**Algoritmo hash capicol \_ \_ \_ Sha \_ 256**</dt></span><span class="sxs-lookup"><span data-stu-id="70478-122"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_256**</dt></span></span> </dl> | <span data-ttu-id="70478-123">Algoritmo hash SHA-256.</span><span class="sxs-lookup"><span data-stu-id="70478-123">SHA-256 hash algorithm.</span></span><br/> <span data-ttu-id="70478-124">**CAPICOM 2.0.0.3 e versioni precedenti:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="70478-124">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_384"></span><span id="capicom_hash_algorithm_sha_384"></span><dl> <span data-ttu-id="70478-125"><dt>**Algoritmo hash capicol \_ \_ \_ Sha \_ 384**</dt></span><span class="sxs-lookup"><span data-stu-id="70478-125"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_384**</dt></span></span> </dl> | <span data-ttu-id="70478-126">Algoritmo hash SHA-384.</span><span class="sxs-lookup"><span data-stu-id="70478-126">SHA-384 hash algorithm.</span></span><br/> <span data-ttu-id="70478-127">**CAPICOM 2.0.0.3 e versioni precedenti:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="70478-127">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_512"></span><span id="capicom_hash_algorithm_sha_512"></span><dl> <span data-ttu-id="70478-128"><dt>**Algoritmo hash capicol \_ \_ \_ Sha \_ 512**</dt></span><span class="sxs-lookup"><span data-stu-id="70478-128"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_512**</dt></span></span> </dl> | <span data-ttu-id="70478-129">Algoritmo hash SHA-512.</span><span class="sxs-lookup"><span data-stu-id="70478-129">SHA-512 hash algorithm.</span></span><br/> <span data-ttu-id="70478-130">**CAPICOM 2.0.0.3 e versioni precedenti:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="70478-130">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="70478-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70478-131">Requirements</span></span>



| <span data-ttu-id="70478-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="70478-132">Requirement</span></span> | <span data-ttu-id="70478-133">Valore</span><span class="sxs-lookup"><span data-stu-id="70478-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70478-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="70478-134">End of client support</span></span><br/> | <span data-ttu-id="70478-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70478-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="70478-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="70478-136">End of server support</span></span><br/> | <span data-ttu-id="70478-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70478-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="70478-138">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="70478-138">Redistributable</span></span><br/>       | <span data-ttu-id="70478-139">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="70478-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="70478-140">DLL</span><span class="sxs-lookup"><span data-stu-id="70478-140">DLL</span></span><br/>                   | <dl> <span data-ttu-id="70478-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70478-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70478-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70478-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70478-143">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="70478-143">**HashedData**</span></span>](hasheddata.md)
</dt> </dl>

 

 

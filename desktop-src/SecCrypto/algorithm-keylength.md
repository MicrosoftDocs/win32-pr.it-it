---
description: Imposta o recupera la lunghezza della chiave.
ms.assetid: c0176d2d-c000-4529-af45-1cc9060ca56a
title: Proprietà Algorithm. FileLength
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.KeyLength
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aa5dbaeeebe2daaf925b5d5f3aa82b36053fc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324599"
---
# <a name="algorithmkeylength-property"></a><span data-ttu-id="5367a-103">Proprietà Algorithm. FileLength</span><span class="sxs-lookup"><span data-stu-id="5367a-103">Algorithm.KeyLength property</span></span>

<span data-ttu-id="5367a-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5367a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="5367a-105">Usare invece la [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="5367a-105">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="5367a-106">La proprietà della **lunghezza** della chiave imposta o recupera la lunghezza della chiave.</span><span class="sxs-lookup"><span data-stu-id="5367a-106">The **KeyLength** property sets or retrieves the length of the key.</span></span>

<span data-ttu-id="5367a-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5367a-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5367a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5367a-108">Syntax</span></span>


```VB
Algorithm.KeyLength As CAPICOM_ENCRYPTION_KEY_LENGTH
```



## <a name="property-value"></a><span data-ttu-id="5367a-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5367a-109">Property value</span></span>

<span data-ttu-id="5367a-110">Valore dell'enumerazione di [**\_ \_ \_ lunghezza della chiave di crittografia CAPICOM**](capicom-encryption-key-length.md) che specifica la lunghezza della chiave.</span><span class="sxs-lookup"><span data-stu-id="5367a-110">A value of the [**CAPICOM\_ENCRYPTION\_KEY\_LENGTH**](capicom-encryption-key-length.md) enumeration that specifies the key length.</span></span> <span data-ttu-id="5367a-111">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="5367a-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="5367a-112">Valore</span><span class="sxs-lookup"><span data-stu-id="5367a-112">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="5367a-113">Significato</span><span class="sxs-lookup"><span data-stu-id="5367a-113">Meaning</span></span>                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM"></span><span id="capicom_encryption_key_length_maximum"></span><dl> <span data-ttu-id="5367a-114"><dt>**\_lunghezza della chiave di crittografia CAPICOM \_ \_ \_ massima**</dt></span><span class="sxs-lookup"><span data-stu-id="5367a-114"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_MAXIMUM**</dt></span></span> </dl>     | <span data-ttu-id="5367a-115">Utilizzare la lunghezza massima della chiave disponibile con l'algoritmo di crittografia indicato.</span><span class="sxs-lookup"><span data-stu-id="5367a-115">Use the maximum key length available with the indicated encryption algorithm.</span></span><br/> |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS"></span><span id="capicom_encryption_key_length_40_bits"></span><dl> <span data-ttu-id="5367a-116"><dt>**\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 40 \_ bit**</dt></span><span class="sxs-lookup"><span data-stu-id="5367a-116"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_40\_BITS**</dt></span></span> </dl>    | <span data-ttu-id="5367a-117">Usare chiavi a 40 bit.</span><span class="sxs-lookup"><span data-stu-id="5367a-117">Use 40-bit keys.</span></span><br/>                                                              |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS"></span><span id="capicom_encryption_key_length_56_bits"></span><dl> <span data-ttu-id="5367a-118"><dt>**\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 56 \_ bit**</dt></span><span class="sxs-lookup"><span data-stu-id="5367a-118"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_56\_BITS**</dt></span></span> </dl>    | <span data-ttu-id="5367a-119">Se disponibili, utilizzare chiavi a 56 bit.</span><span class="sxs-lookup"><span data-stu-id="5367a-119">Use 56-bit keys if available.</span></span><br/>                                                 |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS"></span><span id="capicom_encryption_key_length_128_bits"></span><dl> <span data-ttu-id="5367a-120"><dt>**\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 128 \_ bit**</dt></span><span class="sxs-lookup"><span data-stu-id="5367a-120"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_128\_BITS**</dt></span></span> </dl> | <span data-ttu-id="5367a-121">Se disponibili, utilizzare chiavi a 128 bit.</span><span class="sxs-lookup"><span data-stu-id="5367a-121">Use 128-bit keys if available.</span></span><br/>                                                |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_192_BITS"></span><span id="capicom_encryption_key_length_192_bits"></span><dl> <span data-ttu-id="5367a-122"><dt>**\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 192 \_ bit**</dt></span><span class="sxs-lookup"><span data-stu-id="5367a-122"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_192\_BITS**</dt></span></span> </dl> | <span data-ttu-id="5367a-123">Usare chiavi a 192 bit.</span><span class="sxs-lookup"><span data-stu-id="5367a-123">Use 192-bit keys.</span></span> <span data-ttu-id="5367a-124">Questa lunghezza della chiave è disponibile solo per AES.</span><span class="sxs-lookup"><span data-stu-id="5367a-124">This key length is available only for AES.</span></span><br/>                  |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_256_BITS"></span><span id="capicom_encryption_key_length_256_bits"></span><dl> <span data-ttu-id="5367a-125"><dt>**\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 256 \_ bit**</dt></span><span class="sxs-lookup"><span data-stu-id="5367a-125"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_256\_BITS**</dt></span></span> </dl> | <span data-ttu-id="5367a-126">Usare chiavi a 256 bit.</span><span class="sxs-lookup"><span data-stu-id="5367a-126">Use 256-bit keys.</span></span> <span data-ttu-id="5367a-127">Questa lunghezza della chiave è disponibile solo per AES.</span><span class="sxs-lookup"><span data-stu-id="5367a-127">This key length is available only for AES.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="5367a-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="5367a-128">Remarks</span></span>

<span data-ttu-id="5367a-129">Quando si utilizzano gli algoritmi di crittografia DES e 3DES, le lunghezze delle chiavi sono standard e la proprietà della **lunghezza** della chiave viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="5367a-129">When DES and 3DES encryption algorithms are used, the key lengths are standard and the **KeyLength** property is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="5367a-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5367a-130">Requirements</span></span>



| <span data-ttu-id="5367a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5367a-131">Requirement</span></span> | <span data-ttu-id="5367a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="5367a-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5367a-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="5367a-133">End of client support</span></span><br/> | <span data-ttu-id="5367a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5367a-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5367a-135">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="5367a-135">End of server support</span></span><br/> | <span data-ttu-id="5367a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5367a-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5367a-137">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="5367a-137">Redistributable</span></span><br/>       | <span data-ttu-id="5367a-138">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="5367a-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5367a-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5367a-139">DLL</span></span><br/>                   | <dl> <span data-ttu-id="5367a-140"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5367a-140"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5367a-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5367a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5367a-142">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="5367a-142">**Algorithm**</span></span>](algorithm.md)
</dt> </dl>

 

 

---
description: Imposta o recupera l'algoritmo utilizzato per la firma, l'inviluppo e la crittografia delle operazioni. Si tratta della proprietà predefinita.
ms.assetid: e1144a9c-a352-4f73-a91c-ea66f3d61608
title: Proprietà Algorithm.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 35ff147d8db7fb409787fa938a951dfc0a2320e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324598"
---
# <a name="algorithmname-property"></a><span data-ttu-id="7ac43-104">Proprietà Algorithm.Name</span><span class="sxs-lookup"><span data-stu-id="7ac43-104">Algorithm.Name property</span></span>

<span data-ttu-id="7ac43-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7ac43-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="7ac43-106">Usare invece la [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="7ac43-106">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="7ac43-107">La proprietà **Name** imposta o recupera l'algoritmo utilizzato per la firma, l'inviluppo e la crittografia delle operazioni.</span><span class="sxs-lookup"><span data-stu-id="7ac43-107">The **Name** property sets or retrieves the algorithm used for signing, enveloping, and encrypting operations.</span></span> <span data-ttu-id="7ac43-108">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="7ac43-108">This is the default property.</span></span>

<span data-ttu-id="7ac43-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="7ac43-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ac43-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ac43-110">Syntax</span></span>


```VB
Algorithm.Name As CAPICOM_ENCRYPTION_ALGORITHM
```



## <a name="property-value"></a><span data-ttu-id="7ac43-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7ac43-111">Property value</span></span>

<span data-ttu-id="7ac43-112">Valore dell'enumerazione dell' [**\_ \_ algoritmo di crittografia CAPICOM**](capicom-encryption-algorithm.md) che specifica quale algoritmo utilizzare.</span><span class="sxs-lookup"><span data-stu-id="7ac43-112">A value of the [**CAPICOM\_ENCRYPTION\_ALGORITHM**](capicom-encryption-algorithm.md) enumeration that specifies which algorithm to use.</span></span> <span data-ttu-id="7ac43-113">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="7ac43-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="7ac43-114">Valore</span><span class="sxs-lookup"><span data-stu-id="7ac43-114">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="7ac43-115">Significato</span><span class="sxs-lookup"><span data-stu-id="7ac43-115">Meaning</span></span>                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC2"></span><span id="capicom_encryption_algorithm_rc2"></span><dl> <span data-ttu-id="7ac43-116"><dt>**Algoritmo di crittografia capicol \_ \_ \_ RC2**</dt></span><span class="sxs-lookup"><span data-stu-id="7ac43-116"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC2**</dt></span></span> </dl>    | <span data-ttu-id="7ac43-117">Usare la crittografia RC2.</span><span class="sxs-lookup"><span data-stu-id="7ac43-117">Use RC2 encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_RC4"></span><span id="capicom_encryption_algorithm_rc4"></span><dl> <span data-ttu-id="7ac43-118"><dt>**\_Algoritmo di crittografia CAPICOM \_ \_ RC4**</dt></span><span class="sxs-lookup"><span data-stu-id="7ac43-118"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC4**</dt></span></span> </dl>    | <span data-ttu-id="7ac43-119">Usare la crittografia RC4.</span><span class="sxs-lookup"><span data-stu-id="7ac43-119">Use RC4 encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_DES"></span><span id="capicom_encryption_algorithm_des"></span><dl> <span data-ttu-id="7ac43-120"><dt>**\_algoritmo di crittografia CAPICOM \_ \_ des**</dt></span><span class="sxs-lookup"><span data-stu-id="7ac43-120"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_DES**</dt></span></span> </dl>    | <span data-ttu-id="7ac43-121">Usare la crittografia DES.</span><span class="sxs-lookup"><span data-stu-id="7ac43-121">Use DES encryption.</span></span><br/>        |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_3DES"></span><span id="capicom_encryption_algorithm_3des"></span><dl> <span data-ttu-id="7ac43-122"><dt>**Algoritmo di crittografia capicol \_ \_ \_ 3DES**</dt></span><span class="sxs-lookup"><span data-stu-id="7ac43-122"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_3DES**</dt></span></span> </dl> | <span data-ttu-id="7ac43-123">Usare la crittografia Triple DES.</span><span class="sxs-lookup"><span data-stu-id="7ac43-123">Use triple DES encryption.</span></span><br/> |
| <span id="CAPICOM_ENCRYPTION_ALGORITHM_AES"></span><span id="capicom_encryption_algorithm_aes"></span><dl> <span data-ttu-id="7ac43-124"><dt>**algoritmo di crittografia capicol \_ \_ \_ AES**</dt></span><span class="sxs-lookup"><span data-stu-id="7ac43-124"><dt>**CAPICOM\_ENCRYPTION\_ALGORITHM\_AES**</dt></span></span> </dl>    | <span data-ttu-id="7ac43-125">Usare l'algoritmo AES.</span><span class="sxs-lookup"><span data-stu-id="7ac43-125">Use the AES algorithm.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="7ac43-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ac43-126">Remarks</span></span>

<span data-ttu-id="7ac43-127">Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero stato dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7ac43-127">When the value of this property is reset, directly or indirectly, the whole state of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ac43-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ac43-128">Requirements</span></span>



| <span data-ttu-id="7ac43-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ac43-129">Requirement</span></span> | <span data-ttu-id="7ac43-130">Valore</span><span class="sxs-lookup"><span data-stu-id="7ac43-130">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac43-131">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="7ac43-131">End of client support</span></span><br/> | <span data-ttu-id="7ac43-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ac43-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7ac43-133">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="7ac43-133">End of server support</span></span><br/> | <span data-ttu-id="7ac43-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ac43-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7ac43-135">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="7ac43-135">Redistributable</span></span><br/>       | <span data-ttu-id="7ac43-136">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="7ac43-136">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7ac43-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7ac43-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7ac43-138"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ac43-138"><dt>Capicom.dll</dt></span></span> </dl> |



 

 

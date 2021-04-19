---
description: Definisce gli algoritmi da utilizzare per la crittografia e la decrittografia.
ms.assetid: c7aacd1c-02f6-4cf5-9305-50e2330f243c
title: Enumerazione CAPICOM_ENCRYPTION_ALGORITHM (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 19626ba560ead406005612db3ed90cabc61d98ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328138"
---
# <a name="capicom_encryption_algorithm-enumeration"></a><span data-ttu-id="96650-103">\_Enumerazione dell'algoritmo di crittografia CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="96650-103">CAPICOM\_ENCRYPTION\_ALGORITHM enumeration</span></span>

<span data-ttu-id="96650-104">Il tipo di enumerazione di **\_ \_ algoritmi di crittografia CAPICOM** definisce gli algoritmi da utilizzare per la crittografia e la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="96650-104">The **CAPICOM\_ENCRYPTION\_ALGORITHM** enumeration type defines the algorithms to be used in encryption and decryption.</span></span>

## <a name="members"></a><span data-ttu-id="96650-105">Membri</span><span class="sxs-lookup"><span data-stu-id="96650-105">Members</span></span>



| <span data-ttu-id="96650-106">Membro</span><span class="sxs-lookup"><span data-stu-id="96650-106">Member</span></span>                                   | <span data-ttu-id="96650-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96650-107">Description</span></span>                                                                                                                                                                                              | <span data-ttu-id="96650-108">Valore</span><span class="sxs-lookup"><span data-stu-id="96650-108">Value</span></span>     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="96650-109">**Algoritmo di crittografia capicol \_ \_ \_ RC2**</span><span class="sxs-lookup"><span data-stu-id="96650-109">**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC2**</span></span>  | <span data-ttu-id="96650-110">Usare la crittografia RSA RC2.</span><span class="sxs-lookup"><span data-stu-id="96650-110">Use RSA RC2 encryption.</span></span><br/>                                                                                                                                                                       | <span data-ttu-id="96650-111">0</span><span class="sxs-lookup"><span data-stu-id="96650-111">0</span></span>         |
| <span data-ttu-id="96650-112">**\_Algoritmo di crittografia CAPICOM \_ \_ RC4**</span><span class="sxs-lookup"><span data-stu-id="96650-112">**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC4**</span></span>  | <span data-ttu-id="96650-113">Usare la crittografia RSA RC4.</span><span class="sxs-lookup"><span data-stu-id="96650-113">Use RSA RC4 encryption.</span></span><br/>                                                                                                                                                                       | <span data-ttu-id="96650-114">1</span><span class="sxs-lookup"><span data-stu-id="96650-114">1</span></span>         |
| <span data-ttu-id="96650-115">**\_algoritmo di crittografia CAPICOM \_ \_ des**</span><span class="sxs-lookup"><span data-stu-id="96650-115">**CAPICOM\_ENCRYPTION\_ALGORITHM\_DES**</span></span>  | <span data-ttu-id="96650-116">Usare la crittografia DES.</span><span class="sxs-lookup"><span data-stu-id="96650-116">Use DES encryption.</span></span><br/>                                                                                                                                                                           | <span data-ttu-id="96650-117">2</span><span class="sxs-lookup"><span data-stu-id="96650-117">2</span></span>         |
| <span data-ttu-id="96650-118">**Algoritmo di crittografia capicol \_ \_ \_ 3DES**</span><span class="sxs-lookup"><span data-stu-id="96650-118">**CAPICOM\_ENCRYPTION\_ALGORITHM\_3DES**</span></span> | <span data-ttu-id="96650-119">Usare la crittografia Triple DES.</span><span class="sxs-lookup"><span data-stu-id="96650-119">Use triple DES encryption.</span></span><br/>                                                                                                                                                                    | <span data-ttu-id="96650-120">3</span><span class="sxs-lookup"><span data-stu-id="96650-120">3</span></span>         |
| <span data-ttu-id="96650-121">**algoritmo di crittografia capicol \_ \_ \_ AES**</span><span class="sxs-lookup"><span data-stu-id="96650-121">**CAPICOM\_ENCRYPTION\_ALGORITHM\_AES**</span></span>  | <span data-ttu-id="96650-122">Usare l'algoritmo [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES).</span><span class="sxs-lookup"><span data-stu-id="96650-122">Use the [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES) algorithm.</span></span> <span data-ttu-id="96650-123">Questo valore è valido solo per l'oggetto [**EncryptedData**](encrypteddata.md) .</span><span class="sxs-lookup"><span data-stu-id="96650-123">This value is valid for the [**EncryptedData**](encrypteddata.md) object only.</span></span><br/> | <span data-ttu-id="96650-124">4//v 2.0</span><span class="sxs-lookup"><span data-stu-id="96650-124">4 // v2.0</span></span> |



## <a name="remarks"></a><span data-ttu-id="96650-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="96650-125">Remarks</span></span>

<span data-ttu-id="96650-126">Il tipo di enumerazione dell' **\_ \_ algoritmo di crittografia CAPICOM** viene usato dalla proprietà [**Algorithm.Name**](algorithm-name.md) .</span><span class="sxs-lookup"><span data-stu-id="96650-126">The **CAPICOM\_ENCRYPTION\_ALGORITHM** enumeration type is used by the [**Algorithm.Name**](algorithm-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="96650-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96650-127">Requirements</span></span>



| <span data-ttu-id="96650-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="96650-128">Requirement</span></span> | <span data-ttu-id="96650-129">Valore</span><span class="sxs-lookup"><span data-stu-id="96650-129">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="96650-130">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="96650-130">Redistributable</span></span><br/> | <span data-ttu-id="96650-131">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="96650-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="96650-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96650-132">Header</span></span><br/>          | <dl> <span data-ttu-id="96650-133"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="96650-133"><dt>Capicom.h</dt></span></span> </dl> |



 

 

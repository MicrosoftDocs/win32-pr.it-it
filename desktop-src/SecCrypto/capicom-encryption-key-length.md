---
description: Definisce la lunghezza della chiave da utilizzare nella crittografia.
ms.assetid: a91e75db-f81e-4908-b795-34be7a1c242d
title: Enumerazione CAPICOM_ENCRYPTION_KEY_LENGTH (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_KEY_LENGTH
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 4f3e64df1e706ef20a83f4da5c81cda2a08ed331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333568"
---
# <a name="capicom_encryption_key_length-enumeration"></a><span data-ttu-id="355d4-103">\_Enumerazione della lunghezza della chiave di crittografia CAPICOM \_ \_</span><span class="sxs-lookup"><span data-stu-id="355d4-103">CAPICOM\_ENCRYPTION\_KEY\_LENGTH enumeration</span></span>

<span data-ttu-id="355d4-104">Il tipo di enumerazione della **lunghezza della \_ chiave di crittografia \_ \_ CAPICOM** definisce la [*lunghezza della chiave*](../secgloss/k-gly.md) da usare nella crittografia.</span><span class="sxs-lookup"><span data-stu-id="355d4-104">The **CAPICOM\_ENCRYPTION\_KEY\_LENGTH** enumeration type defines the [*key length*](../secgloss/k-gly.md) to be used in encryption.</span></span>

## <a name="members"></a><span data-ttu-id="355d4-105">Membri</span><span class="sxs-lookup"><span data-stu-id="355d4-105">Members</span></span>



| <span data-ttu-id="355d4-106">Membro</span><span class="sxs-lookup"><span data-stu-id="355d4-106">Member</span></span>                                          | <span data-ttu-id="355d4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="355d4-107">Description</span></span>                                                                               | <span data-ttu-id="355d4-108">Valore</span><span class="sxs-lookup"><span data-stu-id="355d4-108">Value</span></span>     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="355d4-109">**\_lunghezza della chiave di crittografia CAPICOM \_ \_ \_ massima**</span><span class="sxs-lookup"><span data-stu-id="355d4-109">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_MAXIMUM**</span></span>   | <span data-ttu-id="355d4-110">Usa la lunghezza massima della chiave disponibile con l'algoritmo di crittografia indicato.</span><span class="sxs-lookup"><span data-stu-id="355d4-110">Uses the maximum key length available with the indicated encryption algorithm.</span></span><br/> | <span data-ttu-id="355d4-111">0</span><span class="sxs-lookup"><span data-stu-id="355d4-111">0</span></span>         |
| <span data-ttu-id="355d4-112">**\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 40 \_ bit**</span><span class="sxs-lookup"><span data-stu-id="355d4-112">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_40\_BITS**</span></span>  | <span data-ttu-id="355d4-113">USA chiavi a 40 bit.</span><span class="sxs-lookup"><span data-stu-id="355d4-113">Uses 40-bit keys.</span></span><br/>                                                              | <span data-ttu-id="355d4-114">1</span><span class="sxs-lookup"><span data-stu-id="355d4-114">1</span></span>         |
| <span data-ttu-id="355d4-115">**\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 56 \_ bit**</span><span class="sxs-lookup"><span data-stu-id="355d4-115">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_56\_BITS**</span></span>  | <span data-ttu-id="355d4-116">USA chiavi a 56 bit se disponibili.</span><span class="sxs-lookup"><span data-stu-id="355d4-116">Uses 56-bit keys if available.</span></span><br/>                                                 | <span data-ttu-id="355d4-117">2</span><span class="sxs-lookup"><span data-stu-id="355d4-117">2</span></span>         |
| <span data-ttu-id="355d4-118">**\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 128 \_ bit**</span><span class="sxs-lookup"><span data-stu-id="355d4-118">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_128\_BITS**</span></span> | <span data-ttu-id="355d4-119">USA chiavi a 128 bit se disponibili.</span><span class="sxs-lookup"><span data-stu-id="355d4-119">Uses 128-bit keys if available.</span></span><br/>                                                | <span data-ttu-id="355d4-120">3</span><span class="sxs-lookup"><span data-stu-id="355d4-120">3</span></span>         |
| <span data-ttu-id="355d4-121">**\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 192 \_ bit**</span><span class="sxs-lookup"><span data-stu-id="355d4-121">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_192\_BITS**</span></span> | <span data-ttu-id="355d4-122">USA chiavi a 192 bit.</span><span class="sxs-lookup"><span data-stu-id="355d4-122">Uses 192-bit keys.</span></span> <span data-ttu-id="355d4-123">Questa lunghezza della chiave è disponibile solo per AES.</span><span class="sxs-lookup"><span data-stu-id="355d4-123">This key length is available only for AES.</span></span><br/>                  | <span data-ttu-id="355d4-124">4//v 2.0</span><span class="sxs-lookup"><span data-stu-id="355d4-124">4 // v2.0</span></span> |
| <span data-ttu-id="355d4-125">**\_Lunghezza della chiave di crittografia capicom \_ \_ \_ 256 \_ bit**</span><span class="sxs-lookup"><span data-stu-id="355d4-125">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_256\_BITS**</span></span> | <span data-ttu-id="355d4-126">USA chiavi a 256 bit.</span><span class="sxs-lookup"><span data-stu-id="355d4-126">Uses 256-bit keys.</span></span> <span data-ttu-id="355d4-127">Questa lunghezza della chiave è disponibile solo per AES.</span><span class="sxs-lookup"><span data-stu-id="355d4-127">This key length is available only for AES.</span></span><br/>                  | <span data-ttu-id="355d4-128">5//v 2.0</span><span class="sxs-lookup"><span data-stu-id="355d4-128">5 // v2.0</span></span> |



## <a name="remarks"></a><span data-ttu-id="355d4-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="355d4-129">Remarks</span></span>

<span data-ttu-id="355d4-130">Il tipo di enumerazione della lunghezza della chiave di crittografia CAPICOM viene usato dalla proprietà [**Algorithm.**](algorithm-keylength.md) **\_ \_ Key \_** length.</span><span class="sxs-lookup"><span data-stu-id="355d4-130">The **CAPICOM\_ENCRYPTION\_KEY\_LENGTH** enumeration type is used by the [**Algorithm.KeyLength**](algorithm-keylength.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="355d4-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="355d4-131">Requirements</span></span>



| <span data-ttu-id="355d4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="355d4-132">Requirement</span></span> | <span data-ttu-id="355d4-133">Valore</span><span class="sxs-lookup"><span data-stu-id="355d4-133">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="355d4-134">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="355d4-134">Redistributable</span></span><br/> | <span data-ttu-id="355d4-135">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="355d4-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="355d4-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="355d4-136">Header</span></span><br/>          | <dl> <span data-ttu-id="355d4-137"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="355d4-137"><dt>Capicom.h</dt></span></span> </dl> |



 

 

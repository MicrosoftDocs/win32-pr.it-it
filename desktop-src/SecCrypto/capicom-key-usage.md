---
description: L' \_ \_ enumerazione di utilizzo della chiave CAPICOM definisce i modi in cui è possibile utilizzare una chiave. Introdotta in capicol 2,0.
ms.assetid: 7143567b-5882-44a3-ae30-fb8965fb7997
title: Enumerazione CAPICOM_KEY_USAGE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_USAGE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1d44c7f3ecf35ddeb55dd96e5513261691010990
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327639"
---
# <a name="capicom_key_usage-enumeration"></a><span data-ttu-id="e01e6-104">\_Enumerazione utilizzo chiave CApicol \_</span><span class="sxs-lookup"><span data-stu-id="e01e6-104">CAPICOM\_KEY\_USAGE enumeration</span></span>

<span data-ttu-id="e01e6-105">L'enumerazione di **\_ \_ utilizzo della chiave CAPICOM** definisce i modi in cui è possibile utilizzare una chiave.</span><span class="sxs-lookup"><span data-stu-id="e01e6-105">The **CAPICOM\_KEY\_USAGE** enumeration defines the ways in which a key can be used.</span></span> <span data-ttu-id="e01e6-106">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="e01e6-106">Introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="e01e6-107">Membri</span><span class="sxs-lookup"><span data-stu-id="e01e6-107">Members</span></span>



| <span data-ttu-id="e01e6-108">Membro</span><span class="sxs-lookup"><span data-stu-id="e01e6-108">Member</span></span>                                      | <span data-ttu-id="e01e6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e01e6-109">Description</span></span>                                                                                                                      | <span data-ttu-id="e01e6-110">Valore</span><span class="sxs-lookup"><span data-stu-id="e01e6-110">Value</span></span>      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| <span data-ttu-id="e01e6-111">**\_ \_ \_ utilizzo chiave firma digitale CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="e01e6-111">**CAPICOM\_DIGITAL\_SIGNATURE\_KEY\_USAGE**</span></span> | <span data-ttu-id="e01e6-112">La chiave può essere usata per creare una firma digitale.</span><span class="sxs-lookup"><span data-stu-id="e01e6-112">The key can be used to create a digital signature.</span></span><br/>                                                                    | <span data-ttu-id="e01e6-113">0x00000080</span><span class="sxs-lookup"><span data-stu-id="e01e6-113">0x00000080</span></span> |
| <span data-ttu-id="e01e6-114">**\_utilizzo chiave di non \_ ripudio di \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="e01e6-114">**CAPICOM\_NON\_REPUDIATION\_KEY\_USAGE**</span></span>   | <span data-ttu-id="e01e6-115">La chiave può essere utilizzata per il non [*ripudio*](../secgloss/n-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e01e6-115">The key can be used for [*nonrepudiation*](../secgloss/n-gly.md).</span></span><br/> | <span data-ttu-id="e01e6-116">0x00000040</span><span class="sxs-lookup"><span data-stu-id="e01e6-116">0x00000040</span></span> |
| <span data-ttu-id="e01e6-117">**\_ \_ utilizzo chiave di crittografia chiave \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="e01e6-117">**CAPICOM\_KEY\_ENCIPHERMENT\_KEY\_USAGE**</span></span>  | <span data-ttu-id="e01e6-118">La chiave può essere usata per crittografare una chiave.</span><span class="sxs-lookup"><span data-stu-id="e01e6-118">The key can be used to encrypt a key.</span></span><br/>                                                                                 | <span data-ttu-id="e01e6-119">0x00000020</span><span class="sxs-lookup"><span data-stu-id="e01e6-119">0x00000020</span></span> |
| <span data-ttu-id="e01e6-120">**\_ \_ \_ utilizzo chiave crittografia dati CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="e01e6-120">**CAPICOM\_DATA\_ENCIPHERMENT\_KEY\_USAGE**</span></span> | <span data-ttu-id="e01e6-121">La chiave può essere usata per crittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="e01e6-121">The key can be used to encrypt data.</span></span><br/>                                                                                  | <span data-ttu-id="e01e6-122">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e01e6-122">0x00000010</span></span> |
| <span data-ttu-id="e01e6-123">**utilizzo chiave di capicot Key \_ \_ Agreement \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e01e6-123">**CAPICOM\_KEY\_AGREEMENT\_KEY\_USAGE**</span></span>     | <span data-ttu-id="e01e6-124">La chiave può essere usata per il contratto di chiave.</span><span class="sxs-lookup"><span data-stu-id="e01e6-124">The key can be used for key agreement.</span></span><br/>                                                                                | <span data-ttu-id="e01e6-125">0x00000008</span><span class="sxs-lookup"><span data-stu-id="e01e6-125">0x00000008</span></span> |
| <span data-ttu-id="e01e6-126">**\_utilizzo della chiave di \_ firma del certificato chiave \_ \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="e01e6-126">**CAPICOM\_KEY\_CERT\_SIGN\_KEY\_USAGE**</span></span>    | <span data-ttu-id="e01e6-127">La chiave può essere usata per la firma del certificato chiave.</span><span class="sxs-lookup"><span data-stu-id="e01e6-127">The key can be used for key certificate signing.</span></span> <span data-ttu-id="e01e6-128">Questo valore è equivalente all' \_ utilizzo della chiave di \_ firma CRL offline di CAPICOM \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e01e6-128">This value is equivalent to CAPICOM\_OFFLINE\_CRL\_SIGN\_KEY\_USAGE.</span></span><br/> | <span data-ttu-id="e01e6-129">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e01e6-129">0x00000004</span></span> |
| <span data-ttu-id="e01e6-130">**\_ \_ \_ utilizzo chiave di firma CRL \_ offline \_ di CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="e01e6-130">**CAPICOM\_OFFLINE\_CRL\_SIGN\_KEY\_USAGE**</span></span> | <span data-ttu-id="e01e6-131">La chiave può essere usata per la firma del certificato chiave.</span><span class="sxs-lookup"><span data-stu-id="e01e6-131">The key can be used for key certificate signing.</span></span> <span data-ttu-id="e01e6-132">Questo valore è equivalente all' \_ utilizzo della chiave di firma del certificato chiave CApicol \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e01e6-132">This value is equivalent to CAPICOM\_KEY\_CERT\_SIGN\_KEY\_USAGE.</span></span><br/>    | <span data-ttu-id="e01e6-133">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e01e6-133">0x00000002</span></span> |
| <span data-ttu-id="e01e6-134">**\_ \_ \_ utilizzo chiave del segno di capicol CRL \_**</span><span class="sxs-lookup"><span data-stu-id="e01e6-134">**CAPICOM\_CRL\_SIGN\_KEY\_USAGE**</span></span>          | <span data-ttu-id="e01e6-135">La chiave può essere usata per la firma.</span><span class="sxs-lookup"><span data-stu-id="e01e6-135">The key can be used for signing.</span></span><br/>                                                                                      | <span data-ttu-id="e01e6-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e01e6-136">0x00000002</span></span> |
| <span data-ttu-id="e01e6-137">**CAPICOM \_ \_ solo \_ \_ utilizzo chiavi**</span><span class="sxs-lookup"><span data-stu-id="e01e6-137">**CAPICOM\_ENCIPHER\_ONLY\_KEY\_USAGE**</span></span>     | <span data-ttu-id="e01e6-138">La chiave può essere utilizzata solo per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="e01e6-138">The key can only be used to encrypt.</span></span><br/>                                                                                  | <span data-ttu-id="e01e6-139">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e01e6-139">0x00000001</span></span> |
| <span data-ttu-id="e01e6-140">**CAPICOM \_ decifrare \_ solo \_ \_ utilizzo chiavi**</span><span class="sxs-lookup"><span data-stu-id="e01e6-140">**CAPICOM\_DECIPHER\_ONLY\_KEY\_USAGE**</span></span>     | <span data-ttu-id="e01e6-141">La chiave può essere usata solo per la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="e01e6-141">The key can only be used to decrypt.</span></span><br/>                                                                                  | <span data-ttu-id="e01e6-142">0x00008000</span><span class="sxs-lookup"><span data-stu-id="e01e6-142">0x00008000</span></span> |



## <a name="requirements"></a><span data-ttu-id="e01e6-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e01e6-143">Requirements</span></span>



| <span data-ttu-id="e01e6-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="e01e6-144">Requirement</span></span> | <span data-ttu-id="e01e6-145">Valore</span><span class="sxs-lookup"><span data-stu-id="e01e6-145">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e01e6-146">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="e01e6-146">Redistributable</span></span><br/> | <span data-ttu-id="e01e6-147">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="e01e6-147">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="e01e6-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e01e6-148">Header</span></span><br/>          | <dl> <span data-ttu-id="e01e6-149"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="e01e6-149"><dt>Capicom.h</dt></span></span> </dl> |



 

 

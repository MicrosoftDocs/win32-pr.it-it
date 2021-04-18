---
description: Definisce quali informazioni devono essere sottoposte a query da un certificato.
ms.assetid: b603c06b-e6d4-4d5d-92b2-3b4f5b93478a
title: Enumerazione CAPICOM_CERT_INFO_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERT_INFO_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 8e38bb8940645bbefecb3822bce8de8c2e0eb902
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327649"
---
# <a name="capicom_cert_info_type-enumeration"></a><span data-ttu-id="96539-103">\_Enumerazione del tipo di informazioni del certificato CApicol \_ \_</span><span class="sxs-lookup"><span data-stu-id="96539-103">CAPICOM\_CERT\_INFO\_TYPE enumeration</span></span>

<span data-ttu-id="96539-104">Il tipo di enumerazione **CApicol \_ CERT \_ info \_ Type** definisce quali informazioni devono essere sottoposte a query da un certificato.</span><span class="sxs-lookup"><span data-stu-id="96539-104">The **CAPICOM\_CERT\_INFO\_TYPE** enumeration type defines what information is to be queried from a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="96539-105">Membri</span><span class="sxs-lookup"><span data-stu-id="96539-105">Members</span></span>



| <span data-ttu-id="96539-106">Membro</span><span class="sxs-lookup"><span data-stu-id="96539-106">Member</span></span>                                         | <span data-ttu-id="96539-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96539-107">Description</span></span>                                                                                  | <span data-ttu-id="96539-108">Valore</span><span class="sxs-lookup"><span data-stu-id="96539-108">Value</span></span> |
|------------------------------------------------|----------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="96539-109">**\_ \_ \_ \_ nome semplice soggetto informazioni sul certificato capicot \_**</span><span class="sxs-lookup"><span data-stu-id="96539-109">**CAPICOM\_CERT\_INFO\_SUBJECT\_SIMPLE\_NAME**</span></span> | <span data-ttu-id="96539-110">Restituisce il nome visualizzato dell'oggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="96539-110">Returns the display name of the certificate subject.</span></span><br/>                              | <span data-ttu-id="96539-111">0</span><span class="sxs-lookup"><span data-stu-id="96539-111">0</span></span>     |
| <span data-ttu-id="96539-112">**\_ \_ \_ nome semplice dell'emittente informazioni \_ sul certificato capicot \_**</span><span class="sxs-lookup"><span data-stu-id="96539-112">**CAPICOM\_CERT\_INFO\_ISSUER\_SIMPLE\_NAME**</span></span>  | <span data-ttu-id="96539-113">Restituisce il nome visualizzato dell'emittente del certificato.</span><span class="sxs-lookup"><span data-stu-id="96539-113">Returns the display name of the issuer of the certificate.</span></span><br/>                        | <span data-ttu-id="96539-114">1</span><span class="sxs-lookup"><span data-stu-id="96539-114">1</span></span>     |
| <span data-ttu-id="96539-115">**\_ \_ \_ nome di \_ posta elettronica dell'oggetto \_ del certificato di capicol**</span><span class="sxs-lookup"><span data-stu-id="96539-115">**CAPICOM\_CERT\_INFO\_SUBJECT\_EMAIL\_NAME**</span></span>  | <span data-ttu-id="96539-116">Restituisce l'indirizzo di posta elettronica del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="96539-116">Returns the email address of the certificate subject.</span></span><br/>                             | <span data-ttu-id="96539-117">2</span><span class="sxs-lookup"><span data-stu-id="96539-117">2</span></span>     |
| <span data-ttu-id="96539-118">**\_ \_ \_ nome di \_ posta elettronica dell'autorità emittente informazioni sul certificato CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="96539-118">**CAPICOM\_CERT\_INFO\_ISSUER\_EMAIL\_NAME**</span></span>   | <span data-ttu-id="96539-119">Restituisce l'indirizzo di posta elettronica dell'emittente del certificato.</span><span class="sxs-lookup"><span data-stu-id="96539-119">Returns the email address of the issuer of the certificate.</span></span><br/>                       | <span data-ttu-id="96539-120">3</span><span class="sxs-lookup"><span data-stu-id="96539-120">3</span></span>     |
| <span data-ttu-id="96539-121">**nome \_ \_ \_ UPN oggetto informazioni del certificato \_ CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="96539-121">**CAPICOM\_CERT\_INFO\_SUBJECT\_UPN**</span></span>          | <span data-ttu-id="96539-122">Restituisce l'UPN dell'oggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="96539-122">Returns the UPN of the certificate subject.</span></span> <span data-ttu-id="96539-123">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="96539-123">Introduced in CAPICOM 2.0.</span></span><br/>            | <span data-ttu-id="96539-124">4</span><span class="sxs-lookup"><span data-stu-id="96539-124">4</span></span>     |
| <span data-ttu-id="96539-125">**nome UPN dell' \_ \_ \_ autorità emittente informazioni sul certificato capicot \_**</span><span class="sxs-lookup"><span data-stu-id="96539-125">**CAPICOM\_CERT\_INFO\_ISSUER\_UPN**</span></span>           | <span data-ttu-id="96539-126">Restituisce l'UPN dell'emittente del certificato.</span><span class="sxs-lookup"><span data-stu-id="96539-126">Returns the UPN of the issuer of the certificate.</span></span> <span data-ttu-id="96539-127">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="96539-127">Introduced in CAPICOM 2.0.</span></span><br/>      | <span data-ttu-id="96539-128">5</span><span class="sxs-lookup"><span data-stu-id="96539-128">5</span></span>     |
| <span data-ttu-id="96539-129">**\_ \_ \_ nome DNS dell'oggetto informazioni \_ sul certificato capicol \_**</span><span class="sxs-lookup"><span data-stu-id="96539-129">**CAPICOM\_CERT\_INFO\_SUBJECT\_DNS\_NAME**</span></span>    | <span data-ttu-id="96539-130">Restituisce il nome DNS del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="96539-130">Returns the DNS name of the certificate subject.</span></span> <span data-ttu-id="96539-131">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="96539-131">Introduced in CAPICOM 2.0.</span></span><br/>       | <span data-ttu-id="96539-132">6</span><span class="sxs-lookup"><span data-stu-id="96539-132">6</span></span>     |
| <span data-ttu-id="96539-133">**\_ \_ \_ nome DNS dell'autorità emittente informazioni sul \_ certificato \_ CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="96539-133">**CAPICOM\_CERT\_INFO\_ISSUER\_DNS\_NAME**</span></span>     | <span data-ttu-id="96539-134">Restituisce il nome DNS dell'emittente del certificato.</span><span class="sxs-lookup"><span data-stu-id="96539-134">Returns the DNS name of the issuer of the certificate.</span></span> <span data-ttu-id="96539-135">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="96539-135">Introduced in CAPICOM 2.0.</span></span><br/> | <span data-ttu-id="96539-136">7</span><span class="sxs-lookup"><span data-stu-id="96539-136">7</span></span>     |



## <a name="remarks"></a><span data-ttu-id="96539-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="96539-137">Remarks</span></span>

<span data-ttu-id="96539-138">Il tipo di enumerazione **CApicol \_ CERT \_ info \_ Type** viene utilizzato dal metodo [**Certificate. GetInfo**](certificate-getinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="96539-138">The **CAPICOM\_CERT\_INFO\_TYPE** enumeration type is used by the [**Certificate.GetInfo**](certificate-getinfo.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="96539-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96539-139">Requirements</span></span>



| <span data-ttu-id="96539-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="96539-140">Requirement</span></span> | <span data-ttu-id="96539-141">Valore</span><span class="sxs-lookup"><span data-stu-id="96539-141">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="96539-142">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="96539-142">Redistributable</span></span><br/> | <span data-ttu-id="96539-143">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="96539-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="96539-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96539-144">Header</span></span><br/>          | <dl> <span data-ttu-id="96539-145"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="96539-145"><dt>Capicom.h</dt></span></span> </dl> |



 

 





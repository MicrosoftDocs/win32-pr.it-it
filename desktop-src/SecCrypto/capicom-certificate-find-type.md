---
description: Il \_ \_ \_ tipo di enumerazione del tipo di individuazione del certificato di CAPICOM definisce il tipo di criteri di ricerca usati per trovare certificati specifici. Questo tipo di enumerazione è stato introdotto in capicol 2,0.
ms.assetid: d71436e5-d921-4b84-8028-301d8fc4aedb
title: Enumerazione CAPICOM_CERTIFICATE_FIND_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_FIND_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: c5c867b230ba2045d97619d7f55e257bd7803b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325164"
---
# <a name="capicom_certificate_find_type-enumeration"></a><span data-ttu-id="179a3-104">\_Enumerazione del tipo di ricerca del certificato CApicol \_ \_</span><span class="sxs-lookup"><span data-stu-id="179a3-104">CAPICOM\_CERTIFICATE\_FIND\_TYPE enumeration</span></span>

<span data-ttu-id="179a3-105">Il tipo di enumerazione del tipo di individuazione del certificato di CAPICOM definisce il tipo di criteri di ricerca usati per trovare certificati specifici. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="179a3-105">The **CAPICOM\_CERTIFICATE\_FIND\_TYPE** enumeration type defines the type of search criteria used to find specific certificates.</span></span> <span data-ttu-id="179a3-106">Questo tipo di enumerazione è stato introdotto in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="179a3-106">This enumeration type was introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="179a3-107">Membri</span><span class="sxs-lookup"><span data-stu-id="179a3-107">Members</span></span>



| <span data-ttu-id="179a3-108">Membro</span><span class="sxs-lookup"><span data-stu-id="179a3-108">Member</span></span>                                                | <span data-ttu-id="179a3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="179a3-109">Description</span></span>                                                                                                                                 | <span data-ttu-id="179a3-110">Valore</span><span class="sxs-lookup"><span data-stu-id="179a3-110">Value</span></span> |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="179a3-111">**Il certificato CAPICOM \_ \_ trova \_ hash SHA1 \_**</span><span class="sxs-lookup"><span data-stu-id="179a3-111">**CAPICOM\_CERTIFICATE\_FIND\_SHA1\_HASH**</span></span>            | <span data-ttu-id="179a3-112">Restituisce i certificati corrispondenti a un hash SHA1 specificato.</span><span class="sxs-lookup"><span data-stu-id="179a3-112">Returns certificates matching a specified SHA1 hash.</span></span><br/>                                                                             | <span data-ttu-id="179a3-113">0</span><span class="sxs-lookup"><span data-stu-id="179a3-113">0</span></span>     |
| <span data-ttu-id="179a3-114">**\_ \_ \_ nome oggetto trovato certificato capicot \_**</span><span class="sxs-lookup"><span data-stu-id="179a3-114">**CAPICOM\_CERTIFICATE\_FIND\_SUBJECT\_NAME**</span></span>         | <span data-ttu-id="179a3-115">Restituisce i certificati il cui nome soggetto è esattamente o parzialmente corrispondente a un nome soggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="179a3-115">Returns certificates whose subject name exactly or partially matches a specified subject name.</span></span><br/>                                   | <span data-ttu-id="179a3-116">1</span><span class="sxs-lookup"><span data-stu-id="179a3-116">1</span></span>     |
| <span data-ttu-id="179a3-117">**\_ \_ \_ nome dell'autorità emittente trovare il certificato di CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="179a3-117">**CAPICOM\_CERTIFICATE\_FIND\_ISSUER\_NAME**</span></span>          | <span data-ttu-id="179a3-118">Restituisce i certificati il cui nome dell'autorità di certificazione corrisponde esattamente o parzialmente a un nome di autorità emittente specificato.</span><span class="sxs-lookup"><span data-stu-id="179a3-118">Returns certificates whose issuer name exactly or partially matches a specified issuer name.</span></span><br/>                                     | <span data-ttu-id="179a3-119">2</span><span class="sxs-lookup"><span data-stu-id="179a3-119">2</span></span>     |
| <span data-ttu-id="179a3-120">**\_ \_ \_ nome radice trovato certificato capicol \_**</span><span class="sxs-lookup"><span data-stu-id="179a3-120">**CAPICOM\_CERTIFICATE\_FIND\_ROOT\_NAME**</span></span>            | <span data-ttu-id="179a3-121">Restituisce i certificati il cui nome soggetto radice corrisponde esattamente o parzialmente a un nome soggetto radice specificato.</span><span class="sxs-lookup"><span data-stu-id="179a3-121">Returns certificates whose root subject name exactly or partially matches a specified root subject name.</span></span><br/>                         | <span data-ttu-id="179a3-122">3</span><span class="sxs-lookup"><span data-stu-id="179a3-122">3</span></span>     |
| <span data-ttu-id="179a3-123">**\_nome del modello di \_ ricerca del certificato \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="179a3-123">**CAPICOM\_CERTIFICATE\_FIND\_TEMPLATE\_NAME**</span></span>        | <span data-ttu-id="179a3-124">Restituisce i certificati il cui nome modello corrisponde a un nome di modello specificato.</span><span class="sxs-lookup"><span data-stu-id="179a3-124">Returns certificates whose template name matches a specified template name.</span></span><br/>                                                      | <span data-ttu-id="179a3-125">4</span><span class="sxs-lookup"><span data-stu-id="179a3-125">4</span></span>     |
| <span data-ttu-id="179a3-126">**estensione per la \_ ricerca del certificato CApicol \_ \_**</span><span class="sxs-lookup"><span data-stu-id="179a3-126">**CAPICOM\_CERTIFICATE\_FIND\_EXTENSION**</span></span>             | <span data-ttu-id="179a3-127">Restituisce i certificati con un'estensione che corrisponde a un'estensione specificata.</span><span class="sxs-lookup"><span data-stu-id="179a3-127">Returns certificates that have an extension that matches a specified extension.</span></span><br/>                                                  | <span data-ttu-id="179a3-128">5</span><span class="sxs-lookup"><span data-stu-id="179a3-128">5</span></span>     |
| <span data-ttu-id="179a3-129">**il certificato CAPICOM \_ \_ trova la \_ \_ proprietà estesa**</span><span class="sxs-lookup"><span data-stu-id="179a3-129">**CAPICOM\_CERTIFICATE\_FIND\_EXTENDED\_PROPERTY**</span></span>    | <span data-ttu-id="179a3-130">Restituisce i certificati che dispongono di una proprietà estesa il cui identificatore di proprietà corrisponde a un identificatore di proprietà specificato.</span><span class="sxs-lookup"><span data-stu-id="179a3-130">Returns certificates that have an extended property whose property identifier matches a specified property identifier.</span></span><br/>           | <span data-ttu-id="179a3-131">6</span><span class="sxs-lookup"><span data-stu-id="179a3-131">6</span></span>     |
| <span data-ttu-id="179a3-132">**\_ \_ criterio di ricerca \_ dell'applicazione \_ per il certificato capicol**</span><span class="sxs-lookup"><span data-stu-id="179a3-132">**CAPICOM\_CERTIFICATE\_FIND\_APPLICATION\_POLICY**</span></span>   | <span data-ttu-id="179a3-133">Restituisce i certificati nell'archivio che dispongono di una proprietà o di un'estensione di utilizzo chiavi avanzata combinata a un identificatore di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="179a3-133">Returns certificates in the store that have either an enhanced key usage extension or property combined with a usage identifier.</span></span><br/> | <span data-ttu-id="179a3-134">7</span><span class="sxs-lookup"><span data-stu-id="179a3-134">7</span></span>     |
| <span data-ttu-id="179a3-135">**\_ \_ criterio di individuazione \_ \_ certificati di capicol**</span><span class="sxs-lookup"><span data-stu-id="179a3-135">**CAPICOM\_CERTIFICATE\_FIND\_CERTIFICATE\_POLICY**</span></span>   | <span data-ttu-id="179a3-136">Restituisce i certificati contenenti un OID di criteri specificato.</span><span class="sxs-lookup"><span data-stu-id="179a3-136">Returns certificates containing a specified policy OID.</span></span><br/>                                                                          | <span data-ttu-id="179a3-137">8</span><span class="sxs-lookup"><span data-stu-id="179a3-137">8</span></span>     |
| <span data-ttu-id="179a3-138">**tempo di ricerca certificato capicol \_ \_ \_ \_ valido**</span><span class="sxs-lookup"><span data-stu-id="179a3-138">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_VALID**</span></span>           | <span data-ttu-id="179a3-139">Restituisce i certificati il cui tempo è valido.</span><span class="sxs-lookup"><span data-stu-id="179a3-139">Returns certificates whose time is valid.</span></span><br/>                                                                                        | <span data-ttu-id="179a3-140">9</span><span class="sxs-lookup"><span data-stu-id="179a3-140">9</span></span>     |
| <span data-ttu-id="179a3-141">**tempo di individuazione del certificato capicol \_ \_ \_ \_ non \_ ancora \_ valido**</span><span class="sxs-lookup"><span data-stu-id="179a3-141">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_NOT\_YET\_VALID**</span></span> | <span data-ttu-id="179a3-142">Restituisce i certificati il cui tempo non è ancora valido.</span><span class="sxs-lookup"><span data-stu-id="179a3-142">Returns certificates whose time is not yet valid.</span></span><br/>                                                                                | <span data-ttu-id="179a3-143">10</span><span class="sxs-lookup"><span data-stu-id="179a3-143">10</span></span>    |
| <span data-ttu-id="179a3-144">**tempo di individuazione certificato capicot \_ \_ \_ \_ scaduto**</span><span class="sxs-lookup"><span data-stu-id="179a3-144">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_EXPIRED**</span></span>         | <span data-ttu-id="179a3-145">Restituisce i certificati il cui tempo è scaduto.</span><span class="sxs-lookup"><span data-stu-id="179a3-145">Returns certificates whose time has expired.</span></span><br/>                                                                                     | <span data-ttu-id="179a3-146">11</span><span class="sxs-lookup"><span data-stu-id="179a3-146">11</span></span>    |
| <span data-ttu-id="179a3-147">**\_ \_ utilizzo chiave di ricerca del certificato CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="179a3-147">**CAPICOM\_CERTIFICATE\_FIND\_KEY\_USAGE**</span></span>            | <span data-ttu-id="179a3-148">Restituisce i certificati contenenti una chiave che può essere utilizzata nel modo specificato.</span><span class="sxs-lookup"><span data-stu-id="179a3-148">Returns certificates containing a key that can be used in the specified manner.</span></span><br/>                                                  | <span data-ttu-id="179a3-149">12</span><span class="sxs-lookup"><span data-stu-id="179a3-149">12</span></span>    |



## <a name="remarks"></a><span data-ttu-id="179a3-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="179a3-150">Remarks</span></span>

<span data-ttu-id="179a3-151">Il tipo di enumerazione del **\_ tipo di \_ individuazione \_ del certificato CAPICOM** viene utilizzato dal metodo [**Certificates. Find**](certificates-find.md) .</span><span class="sxs-lookup"><span data-stu-id="179a3-151">The **CAPICOM\_CERTIFICATE\_FIND\_TYPE** enumeration type is used by the [**Certificates.Find**](certificates-find.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="179a3-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="179a3-152">Requirements</span></span>



| <span data-ttu-id="179a3-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="179a3-153">Requirement</span></span> | <span data-ttu-id="179a3-154">Valore</span><span class="sxs-lookup"><span data-stu-id="179a3-154">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="179a3-155">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="179a3-155">Redistributable</span></span><br/> | <span data-ttu-id="179a3-156">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="179a3-156">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="179a3-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="179a3-157">Header</span></span><br/>          | <dl> <span data-ttu-id="179a3-158"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="179a3-158"><dt>Capicom.h</dt></span></span> </dl> |



 

 





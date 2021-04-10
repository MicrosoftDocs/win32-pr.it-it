---
title: Struttura LSKeyPack
description: Contiene informazioni su un Key Pack di gestione licenze Servizi Desktop remoto specifico.
ms.assetid: c26d27ee-7dd3-49f0-a79c-752d23693a2a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto della struttura LSKeyPack
- Servizi Desktop remoto puntatore alla struttura LPLSKeyPack
topic_type:
- apiref
api_name:
- LSKeyPack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b1ac1f51e66a0a3c15c33f2535bc02f1fd3528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964811"
---
# <a name="lskeypack-structure"></a><span data-ttu-id="84a53-105">Struttura LSKeyPack</span><span class="sxs-lookup"><span data-stu-id="84a53-105">LSKeyPack structure</span></span>

<span data-ttu-id="84a53-106">Contiene informazioni su un Key Pack di gestione licenze Servizi Desktop remoto specifico.</span><span class="sxs-lookup"><span data-stu-id="84a53-106">Contains information about a specific Remote Desktop Services licensing key pack.</span></span>

> [!Note]  
> <span data-ttu-id="84a53-107">Questa struttura non è definita in alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="84a53-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="84a53-108">Per usare questa struttura, è necessario definirla come illustrato in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="84a53-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="84a53-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84a53-109">Syntax</span></span>


```C++
typedef struct _LSKeyPack {
  DWORD dwVersion;
  UCHAR ucKeyPackType;
  TCHAR szCompanyName[256];
  TCHAR szKeyPackId[256];
  TCHAR szProductName[256];
  TCHAR szProductId[256];
  TCHAR szProductDesc[256];
  WORD  wMajorVersion;
  WORD  wMinorVersion;
  DWORD dwPlatformType;
  UCHAR ucLicenseType;
  DWORD dwLanguageId;
  UCHAR ucChannelOfPurchase;
  TCHAR szBeginSerialNumber[256];
  DWORD dwTotalLicenseInKeyPack;
  DWORD dwProductFlags;
  DWORD dwKeyPackId;
  UCHAR ucKeyPackStatus;
  DWORD dwActivateDate;
  DWORD dwExpirationDate;
  DWORD dwNumberOfLicenses;
} LSKeyPack, *LPLSKeyPack;
```



## <a name="members"></a><span data-ttu-id="84a53-110">Members</span><span class="sxs-lookup"><span data-stu-id="84a53-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="84a53-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="84a53-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-112">Versione del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="84a53-112">Version of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-113">**ucKeyPackType**</span><span class="sxs-lookup"><span data-stu-id="84a53-113">**ucKeyPackType**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-114">Tipo di Key Pack.</span><span class="sxs-lookup"><span data-stu-id="84a53-114">Type of key pack.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-115">**szCompanyName**</span><span class="sxs-lookup"><span data-stu-id="84a53-115">**szCompanyName**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-116">Nome della società che ha emesso il Key Pack.</span><span class="sxs-lookup"><span data-stu-id="84a53-116">Name of the company that issued the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-117">**szKeyPackId**</span><span class="sxs-lookup"><span data-stu-id="84a53-117">**szKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-118">ID del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="84a53-118">ID of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-119">**szProductName**</span><span class="sxs-lookup"><span data-stu-id="84a53-119">**szProductName**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-120">Nome del prodotto a cui appartiene questo Key Pack.</span><span class="sxs-lookup"><span data-stu-id="84a53-120">Name of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-121">**szProductId**</span><span class="sxs-lookup"><span data-stu-id="84a53-121">**szProductId**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-122">ID del prodotto a cui appartiene questo Key Pack.</span><span class="sxs-lookup"><span data-stu-id="84a53-122">ID of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-123">**szProductDesc**</span><span class="sxs-lookup"><span data-stu-id="84a53-123">**szProductDesc**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-124">Descrizione del prodotto a cui appartiene questo Key Pack.</span><span class="sxs-lookup"><span data-stu-id="84a53-124">Description of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-125">**wMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="84a53-125">**wMajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-126">Versione principale del prodotto a cui appartiene questo Key Pack.</span><span class="sxs-lookup"><span data-stu-id="84a53-126">Major version of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-127">**wMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="84a53-127">**wMinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-128">Versione secondaria del prodotto a cui appartiene questo Key Pack.</span><span class="sxs-lookup"><span data-stu-id="84a53-128">Minor version of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-129">**dwPlatformType**</span><span class="sxs-lookup"><span data-stu-id="84a53-129">**dwPlatformType**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-130">Tipo di piattaforma.</span><span class="sxs-lookup"><span data-stu-id="84a53-130">Platform type.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-131">**ucLicenseType**</span><span class="sxs-lookup"><span data-stu-id="84a53-131">**ucLicenseType**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-132">Tipo di licenze nel Key Pack.</span><span class="sxs-lookup"><span data-stu-id="84a53-132">Type of licenses in the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-133">**dwLanguageId**</span><span class="sxs-lookup"><span data-stu-id="84a53-133">**dwLanguageId**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-134">ID della lingua.</span><span class="sxs-lookup"><span data-stu-id="84a53-134">Language ID.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-135">**ucChannelOfPurchase**</span><span class="sxs-lookup"><span data-stu-id="84a53-135">**ucChannelOfPurchase**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-136">Canale di acquisto.</span><span class="sxs-lookup"><span data-stu-id="84a53-136">Channel of purchase.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-137">**szBeginSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="84a53-137">**szBeginSerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-138">Numero di serie per la prima licenza.</span><span class="sxs-lookup"><span data-stu-id="84a53-138">Serial number for the first license.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-139">**dwTotalLicenseInKeyPack**</span><span class="sxs-lookup"><span data-stu-id="84a53-139">**dwTotalLicenseInKeyPack**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-140">Numero totale di licenze nel Key Pack.</span><span class="sxs-lookup"><span data-stu-id="84a53-140">Total number of licenses in the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-141">**dwProductFlags**</span><span class="sxs-lookup"><span data-stu-id="84a53-141">**dwProductFlags**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-142">Bandiere.</span><span class="sxs-lookup"><span data-stu-id="84a53-142">Flags.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-143">**dwKeyPackId**</span><span class="sxs-lookup"><span data-stu-id="84a53-143">**dwKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-144">ID del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="84a53-144">ID of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-145">**ucKeyPackStatus**</span><span class="sxs-lookup"><span data-stu-id="84a53-145">**ucKeyPackStatus**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-146">Stato del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="84a53-146">Status of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-147">**dwActivateDate**</span><span class="sxs-lookup"><span data-stu-id="84a53-147">**dwActivateDate**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-148">Data di attivazione per il Key Pack.</span><span class="sxs-lookup"><span data-stu-id="84a53-148">Activation date for the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-149">**dwExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="84a53-149">**dwExpirationDate**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-150">Data di scadenza per il Key Pack.</span><span class="sxs-lookup"><span data-stu-id="84a53-150">Expiration date for the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="84a53-151">**dwNumberOfLicenses**</span><span class="sxs-lookup"><span data-stu-id="84a53-151">**dwNumberOfLicenses**</span></span>
</dt> <dd>

<span data-ttu-id="84a53-152">Numero di licenze.</span><span class="sxs-lookup"><span data-stu-id="84a53-152">Number of licenses.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84a53-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84a53-153">Requirements</span></span>



| <span data-ttu-id="84a53-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="84a53-154">Requirement</span></span> | <span data-ttu-id="84a53-155">Valore</span><span class="sxs-lookup"><span data-stu-id="84a53-155">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="84a53-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84a53-156">Minimum supported client</span></span><br/> | <span data-ttu-id="84a53-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84a53-157">Windows Vista</span></span><br/>       |
| <span data-ttu-id="84a53-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84a53-158">Minimum supported server</span></span><br/> | <span data-ttu-id="84a53-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84a53-159">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84a53-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84a53-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84a53-161">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="84a53-161">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dt>

[<span data-ttu-id="84a53-162">**TLSKeyPackEnumNext**</span><span class="sxs-lookup"><span data-stu-id="84a53-162">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dt>

[<span data-ttu-id="84a53-163">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="84a53-163">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

 






---
title: Metodo ImportOpenPurchaseLicenseKeyPack della classe Win32_TSLicenseKeyPack
description: Importazioni, da un altro Desktop remoto server licenze, un Key Pack per licenze Open License Servizi Desktop remoto.
ms.assetid: FE1923FF-5292-4080-AB51-88B8A6B2322C
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ImportOpenPurchaseLicenseKeyPack
- Metodo ImportOpenPurchaseLicenseKeyPack Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo ImportOpenPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 944bb1ce63150caece2cbc247af24542fde2d4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302566"
---
# <a name="importopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="fcce1-106">Metodo ImportOpenPurchaseLicenseKeyPack della \_ classe TSLicenseKeyPack Win32</span><span class="sxs-lookup"><span data-stu-id="fcce1-106">ImportOpenPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="fcce1-107">Importazioni, da un altro Desktop remoto server licenze, un Key Pack per licenze Open License Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="fcce1-107">Imports, from another Remote Desktop license server, an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcce1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fcce1-108">Syntax</span></span>


```mof
uint32 ImportOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="fcce1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fcce1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcce1-110">*sLicenseNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcce1-110">*sLicenseNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcce1-111">stringa numerica a 8 caratteri fornita con il Key Pack per le licenze.</span><span class="sxs-lookup"><span data-stu-id="fcce1-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="fcce1-112">Il parametro *sLicenseNumber* non può contenere trattini.</span><span class="sxs-lookup"><span data-stu-id="fcce1-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="fcce1-113">*sAuthorizationNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcce1-113">*sAuthorizationNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcce1-114">stringa alfanumerica a 15 caratteri fornita con il codice di licenza.</span><span class="sxs-lookup"><span data-stu-id="fcce1-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="fcce1-115">Il parametro *sAuthorizationNumber* non può contenere trattini.</span><span class="sxs-lookup"><span data-stu-id="fcce1-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="fcce1-116">*ProductVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcce1-116">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcce1-117">Versione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="fcce1-117">Product version.</span></span>

<dt>

<span data-ttu-id="fcce1-118">0</span><span class="sxs-lookup"><span data-stu-id="fcce1-118">0</span></span>
</dt> <dd>

<span data-ttu-id="fcce1-119">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="fcce1-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fcce1-120">1</span><span class="sxs-lookup"><span data-stu-id="fcce1-120">1</span></span>
</dt> <dd>

<span data-ttu-id="fcce1-121">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="fcce1-121">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fcce1-122">2</span><span class="sxs-lookup"><span data-stu-id="fcce1-122">2</span></span>
</dt> <dd>

<span data-ttu-id="fcce1-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fcce1-123">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fcce1-124">*ProductType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcce1-124">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcce1-125">Tipo di prodotto.</span><span class="sxs-lookup"><span data-stu-id="fcce1-125">Product type.</span></span>

<dt>

<span data-ttu-id="fcce1-126">0</span><span class="sxs-lookup"><span data-stu-id="fcce1-126">0</span></span>
</dt> <dd>

<span data-ttu-id="fcce1-127">Il tipo di prodotto Servizi Desktop remoto License Key Pack è per dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fcce1-127">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="fcce1-128">Pertanto, ogni dispositivo che si connette al server Host sessione Desktop remoto deve disporre di una licenza.</span><span class="sxs-lookup"><span data-stu-id="fcce1-128">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="fcce1-129">1</span><span class="sxs-lookup"><span data-stu-id="fcce1-129">1</span></span>
</dt> <dd>

<span data-ttu-id="fcce1-130">Il tipo di prodotto Servizi Desktop remoto License Key Pack è per utente.</span><span class="sxs-lookup"><span data-stu-id="fcce1-130">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="fcce1-131">Pertanto, ogni utente che si connette al server Host sessione Desktop remoto deve disporre di una licenza.</span><span class="sxs-lookup"><span data-stu-id="fcce1-131">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="fcce1-132">2</span><span class="sxs-lookup"><span data-stu-id="fcce1-132">2</span></span>
</dt> <dd>

<span data-ttu-id="fcce1-133">Questo tipo di prodotto non è valido.</span><span class="sxs-lookup"><span data-stu-id="fcce1-133">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fcce1-134">*LicenseCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcce1-134">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcce1-135">Numero di licenze da importare</span><span class="sxs-lookup"><span data-stu-id="fcce1-135">The number of licenses to import</span></span>

</dd> <dt>

<span data-ttu-id="fcce1-136">*sSourceLSName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcce1-136">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcce1-137">Nome dell'origine Desktop remoto server licenze.</span><span class="sxs-lookup"><span data-stu-id="fcce1-137">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="fcce1-138">Si tratta del nome distinto completo o dell'indirizzo IP del server.</span><span class="sxs-lookup"><span data-stu-id="fcce1-138">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="fcce1-139">*sSourceLSProductId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcce1-139">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcce1-140">Identificatore del server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="fcce1-140">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="fcce1-141">È una stringa alfanumerica di 35 caratteri che non può includere trattini.</span><span class="sxs-lookup"><span data-stu-id="fcce1-141">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="fcce1-142">*KeyPackId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fcce1-142">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcce1-143">Riceve l'identificatore del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="fcce1-143">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcce1-144">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fcce1-144">Return value</span></span>

<span data-ttu-id="fcce1-145">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="fcce1-145">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fcce1-146">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="fcce1-146">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fcce1-147">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fcce1-147">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcce1-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fcce1-148">Requirements</span></span>



| <span data-ttu-id="fcce1-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcce1-149">Requirement</span></span> | <span data-ttu-id="fcce1-150">Valore</span><span class="sxs-lookup"><span data-stu-id="fcce1-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcce1-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcce1-151">Minimum supported client</span></span><br/> | <span data-ttu-id="fcce1-152">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fcce1-152">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="fcce1-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcce1-153">Minimum supported server</span></span><br/> | <span data-ttu-id="fcce1-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fcce1-154">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="fcce1-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fcce1-155">Namespace</span></span><br/>                | <span data-ttu-id="fcce1-156">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="fcce1-156">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="fcce1-157">MOF</span><span class="sxs-lookup"><span data-stu-id="fcce1-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fcce1-158"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fcce1-158"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fcce1-159">DLL</span><span class="sxs-lookup"><span data-stu-id="fcce1-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcce1-160"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcce1-160"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcce1-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fcce1-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcce1-162">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="fcce1-162">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 






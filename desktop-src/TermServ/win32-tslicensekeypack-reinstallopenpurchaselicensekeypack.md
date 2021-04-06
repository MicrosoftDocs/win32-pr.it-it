---
title: Metodo ReinstallOpenPurchaseLicenseKeyPack della classe Win32_TSLicenseKeyPack
description: Reinstalla un Key Pack per licenze Open License Servizi Desktop remoto.
ms.assetid: 3E70711E-284A-466E-A733-1219F5E0B741
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ReinstallOpenPurchaseLicenseKeyPack
- Metodo ReinstallOpenPurchaseLicenseKeyPack Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo ReinstallOpenPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1eae765b74feed98760ef30c2b89a1090c4200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743271"
---
# <a name="reinstallopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="bd443-106">Metodo ReinstallOpenPurchaseLicenseKeyPack della \_ classe TSLicenseKeyPack Win32</span><span class="sxs-lookup"><span data-stu-id="bd443-106">ReinstallOpenPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="bd443-107">Reinstalla un Key Pack per licenze Open License Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bd443-107">Reinstalls an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd443-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd443-108">Syntax</span></span>


```mof
uint32 ReinstallOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="bd443-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd443-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd443-110">*sLicenseNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd443-110">*sLicenseNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd443-111">stringa numerica a 8 caratteri fornita con il Key Pack per le licenze.</span><span class="sxs-lookup"><span data-stu-id="bd443-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="bd443-112">Il parametro *sLicenseNumber* non può contenere trattini.</span><span class="sxs-lookup"><span data-stu-id="bd443-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="bd443-113">*sAuthorizationNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd443-113">*sAuthorizationNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd443-114">stringa alfanumerica a 15 caratteri fornita con il codice di licenza.</span><span class="sxs-lookup"><span data-stu-id="bd443-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="bd443-115">Il parametro *sAuthorizationNumber* non può contenere trattini.</span><span class="sxs-lookup"><span data-stu-id="bd443-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="bd443-116">*ProductVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd443-116">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd443-117">Versione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="bd443-117">Product version.</span></span>

<dt>

<span data-ttu-id="bd443-118">0</span><span class="sxs-lookup"><span data-stu-id="bd443-118">0</span></span>
</dt> <dd>

<span data-ttu-id="bd443-119">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="bd443-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="bd443-120">1</span><span class="sxs-lookup"><span data-stu-id="bd443-120">1</span></span>
</dt> <dd>

<span data-ttu-id="bd443-121">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="bd443-121">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="bd443-122">2</span><span class="sxs-lookup"><span data-stu-id="bd443-122">2</span></span>
</dt> <dd>

<span data-ttu-id="bd443-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd443-123">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bd443-124">*ProductType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd443-124">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd443-125">Tipo di prodotto.</span><span class="sxs-lookup"><span data-stu-id="bd443-125">Product type.</span></span>

<dt>

<span data-ttu-id="bd443-126">0</span><span class="sxs-lookup"><span data-stu-id="bd443-126">0</span></span>
</dt> <dd>

<span data-ttu-id="bd443-127">Il tipo di prodotto Servizi Desktop remoto License Key Pack è per dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bd443-127">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="bd443-128">Pertanto, ogni dispositivo che si connette al server Host sessione Desktop remoto deve disporre di una licenza.</span><span class="sxs-lookup"><span data-stu-id="bd443-128">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="bd443-129">1</span><span class="sxs-lookup"><span data-stu-id="bd443-129">1</span></span>
</dt> <dd>

<span data-ttu-id="bd443-130">Il tipo di prodotto Servizi Desktop remoto License Key Pack è per utente.</span><span class="sxs-lookup"><span data-stu-id="bd443-130">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="bd443-131">Pertanto, ogni utente che si connette al server Host sessione Desktop remoto deve disporre di una licenza.</span><span class="sxs-lookup"><span data-stu-id="bd443-131">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="bd443-132">2</span><span class="sxs-lookup"><span data-stu-id="bd443-132">2</span></span>
</dt> <dd>

<span data-ttu-id="bd443-133">Questo tipo di prodotto non è valido.</span><span class="sxs-lookup"><span data-stu-id="bd443-133">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bd443-134">*LicenseCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd443-134">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd443-135">Numero di licenze da installare.</span><span class="sxs-lookup"><span data-stu-id="bd443-135">The number of licenses to install.</span></span>

</dd> <dt>

<span data-ttu-id="bd443-136">*KeyPackId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bd443-136">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd443-137">Riceve l'identificatore del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="bd443-137">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd443-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd443-138">Return value</span></span>

<span data-ttu-id="bd443-139">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="bd443-139">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bd443-140">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="bd443-140">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bd443-141">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bd443-141">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd443-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd443-142">Requirements</span></span>



| <span data-ttu-id="bd443-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd443-143">Requirement</span></span> | <span data-ttu-id="bd443-144">Valore</span><span class="sxs-lookup"><span data-stu-id="bd443-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd443-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd443-145">Minimum supported client</span></span><br/> | <span data-ttu-id="bd443-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bd443-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="bd443-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd443-147">Minimum supported server</span></span><br/> | <span data-ttu-id="bd443-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd443-148">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="bd443-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bd443-149">Namespace</span></span><br/>                | <span data-ttu-id="bd443-150">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="bd443-150">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="bd443-151">MOF</span><span class="sxs-lookup"><span data-stu-id="bd443-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd443-152"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd443-152"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd443-153">DLL</span><span class="sxs-lookup"><span data-stu-id="bd443-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd443-154"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd443-154"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd443-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd443-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd443-156">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="bd443-156">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 






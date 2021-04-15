---
title: Metodo InstallOpenLicenseKeyPack della classe Win32_TSLicenseKeyPack
description: Installa un Key Pack per licenze Open License Servizi Desktop remoto.
ms.assetid: be50e25c-cda3-408b-934b-51ce343f3271
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo InstallOpenLicenseKeyPack
- Metodo InstallOpenLicenseKeyPack Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo InstallOpenLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallOpenLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7335f25d3118c14f8cd0d27f72fd6a8d4cf1e0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475946"
---
# <a name="installopenlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="ccb1d-106">Metodo InstallOpenLicenseKeyPack della \_ classe TSLicenseKeyPack Win32</span><span class="sxs-lookup"><span data-stu-id="ccb1d-106">InstallOpenLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="ccb1d-107">Installa un Key Pack per licenze Open License Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-107">Installs an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccb1d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ccb1d-108">Syntax</span></span>


```mof
uint32 InstallOpenLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a><span data-ttu-id="ccb1d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ccb1d-109">Parameters</span></span>

<span data-ttu-id="ccb1d-110">*sLicenseNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ccb1d-110">*sLicenseNumber* \[in\]</span></span>

<span data-ttu-id="ccb1d-111">stringa numerica a 8 caratteri fornita con il Key Pack per le licenze.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="ccb1d-112">Il parametro *sLicenseNumber* non può contenere trattini.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

<span data-ttu-id="ccb1d-113">*sAuthorizationNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ccb1d-113">*sAuthorizationNumber* \[in\]</span></span>

<span data-ttu-id="ccb1d-114">stringa alfanumerica a 15 caratteri fornita con il codice di licenza.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="ccb1d-115">Il parametro *sAuthorizationNumber* non può contenere trattini.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

<span data-ttu-id="ccb1d-116">*ProductVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ccb1d-116">*ProductVersion* \[in\]</span></span>

<span data-ttu-id="ccb1d-117">Versione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-117">Product version.</span></span>

| <span data-ttu-id="ccb1d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ccb1d-118">Value</span></span> | <span data-ttu-id="ccb1d-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccb1d-119">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="ccb1d-120">0</span><span class="sxs-lookup"><span data-stu-id="ccb1d-120">0</span></span> | <span data-ttu-id="ccb1d-121">Non supportato</span><span class="sxs-lookup"><span data-stu-id="ccb1d-121">Not supported</span></span> |
| <span data-ttu-id="ccb1d-122">1</span><span class="sxs-lookup"><span data-stu-id="ccb1d-122">1</span></span> | <span data-ttu-id="ccb1d-123">Non supportato</span><span class="sxs-lookup"><span data-stu-id="ccb1d-123">Not supported</span></span> |
| <span data-ttu-id="ccb1d-124">2</span><span class="sxs-lookup"><span data-stu-id="ccb1d-124">2</span></span> | <span data-ttu-id="ccb1d-125">Windows Server 2008/Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ccb1d-125">Windows Server 2008/Windows Server 2008 R2</span></span> |
| <span data-ttu-id="ccb1d-126">4</span><span class="sxs-lookup"><span data-stu-id="ccb1d-126">4</span></span> | <span data-ttu-id="ccb1d-127">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ccb1d-127">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="ccb1d-128">5</span><span class="sxs-lookup"><span data-stu-id="ccb1d-128">5</span></span> | <span data-ttu-id="ccb1d-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ccb1d-129">Windows Server 2016</span></span> |
| <span data-ttu-id="ccb1d-130">6</span><span class="sxs-lookup"><span data-stu-id="ccb1d-130">6</span></span> | <span data-ttu-id="ccb1d-131">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="ccb1d-131">Windows Server 2019</span></span> |

<span data-ttu-id="ccb1d-132">*ProductType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ccb1d-132">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccb1d-133">Tipo di prodotto.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-133">Product type.</span></span>

| <span data-ttu-id="ccb1d-134">Valore</span><span class="sxs-lookup"><span data-stu-id="ccb1d-134">Value</span></span> | <span data-ttu-id="ccb1d-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccb1d-135">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="ccb1d-136">0</span><span class="sxs-lookup"><span data-stu-id="ccb1d-136">0</span></span> | <span data-ttu-id="ccb1d-137">Il tipo di prodotto Servizi Desktop remoto License Key Pack è per dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-137">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="ccb1d-138">Pertanto, ogni dispositivo che si connette al server Host sessione Desktop remoto deve disporre di una licenza.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-138">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="ccb1d-139">1</span><span class="sxs-lookup"><span data-stu-id="ccb1d-139">1</span></span> | <span data-ttu-id="ccb1d-140">Il tipo di prodotto Servizi Desktop remoto License Key Pack è per utente.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-140">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="ccb1d-141">Pertanto, ogni utente che si connette al server Host sessione Desktop remoto deve disporre di una licenza.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-141">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="ccb1d-142">2</span><span class="sxs-lookup"><span data-stu-id="ccb1d-142">2</span></span> | <span data-ttu-id="ccb1d-143">Questo tipo di prodotto non è valido.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-143">This product type is not valid.</span></span> |

<span data-ttu-id="ccb1d-144">*LicenseCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ccb1d-144">*LicenseCount* \[in\]</span></span>

<span data-ttu-id="ccb1d-145">Numero di licenze da installare.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-145">The number of licenses to install.</span></span>

<span data-ttu-id="ccb1d-146">*KeyPackId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ccb1d-146">*KeyPackId* \[out\]</span></span>

<span data-ttu-id="ccb1d-147">Riceve l'identificatore del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-147">Receives the key pack identifier.</span></span>

## <a name="return-value"></a><span data-ttu-id="ccb1d-148">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ccb1d-148">Return value</span></span>

<span data-ttu-id="ccb1d-149">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-149">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ccb1d-150">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-150">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ccb1d-151">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ccb1d-151">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ccb1d-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="ccb1d-152">Remarks</span></span>

<span data-ttu-id="ccb1d-153">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-153">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ccb1d-154">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ccb1d-154">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ccb1d-155">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="ccb1d-155">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ccb1d-156">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-156">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ccb1d-157">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ccb1d-157">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ccb1d-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccb1d-158">Requirements</span></span>



| <span data-ttu-id="ccb1d-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccb1d-159">Requirement</span></span> | <span data-ttu-id="ccb1d-160">Valore</span><span class="sxs-lookup"><span data-stu-id="ccb1d-160">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccb1d-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccb1d-161">Minimum supported client</span></span><br/> | <span data-ttu-id="ccb1d-162">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ccb1d-162">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ccb1d-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccb1d-163">Minimum supported server</span></span><br/> | <span data-ttu-id="ccb1d-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ccb1d-164">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ccb1d-165">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ccb1d-165">Namespace</span></span><br/>                | <span data-ttu-id="ccb1d-166">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="ccb1d-166">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="ccb1d-167">MOF</span><span class="sxs-lookup"><span data-stu-id="ccb1d-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ccb1d-168"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ccb1d-168"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ccb1d-169">DLL</span><span class="sxs-lookup"><span data-stu-id="ccb1d-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccb1d-170"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccb1d-170"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccb1d-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccb1d-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccb1d-172">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="ccb1d-172">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 


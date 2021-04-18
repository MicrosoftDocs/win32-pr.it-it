---
title: Metodo InstallAgreementLicenseKeyPack della classe Win32_TSLicenseKeyPack
description: Installa un Key Pack di licenza Servizi Desktop remoto acquistato tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del Key Pack.
ms.assetid: 70a0aac3-2709-47ba-bf6a-549393c4c115
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo InstallAgreementLicenseKeyPack
- Metodo InstallAgreementLicenseKeyPack Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo InstallAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb891469feae169c1267c12c04af6d21415c309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302459"
---
# <a name="installagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="3d2f5-106">Metodo InstallAgreementLicenseKeyPack della \_ classe TSLicenseKeyPack Win32</span><span class="sxs-lookup"><span data-stu-id="3d2f5-106">InstallAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="3d2f5-107">Installa un Key Pack di licenza Servizi Desktop remoto acquistato tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-107">Installs a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d2f5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d2f5-108">Syntax</span></span>


```mof
uint32 InstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a><span data-ttu-id="3d2f5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d2f5-109">Parameters</span></span>

<span data-ttu-id="3d2f5-110">*AgreementType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d2f5-110">*AgreementType* \[in\]</span></span>

<span data-ttu-id="3d2f5-111">Tipo di contratto.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-111">Agreement type.</span></span>

| <span data-ttu-id="3d2f5-112">Valore</span><span class="sxs-lookup"><span data-stu-id="3d2f5-112">Value</span></span> | <span data-ttu-id="3d2f5-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d2f5-113">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="3d2f5-114">0</span><span class="sxs-lookup"><span data-stu-id="3d2f5-114">0</span></span> | <span data-ttu-id="3d2f5-115">Il Key Pack per le licenze è da un contratto Select Volume License (per i clienti con 250 o più computer).</span><span class="sxs-lookup"><span data-stu-id="3d2f5-115">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="3d2f5-116">Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-116">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="3d2f5-117">1</span><span class="sxs-lookup"><span data-stu-id="3d2f5-117">1</span></span> | <span data-ttu-id="3d2f5-118">Il Key Pack per le licenze è da un contratto multilicenza Enterprise per i clienti con 250 o più computer.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-118">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="3d2f5-119">Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-119">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="3d2f5-120">2</span><span class="sxs-lookup"><span data-stu-id="3d2f5-120">2</span></span> | <span data-ttu-id="3d2f5-121">Il Key Pack per le licenze è da un contratto multilicenza campus per un Istituto di istruzione superiore.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-121">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="3d2f5-122">Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-122">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="3d2f5-123">3</span><span class="sxs-lookup"><span data-stu-id="3d2f5-123">3</span></span> | <span data-ttu-id="3d2f5-124">Il Key Pack per le licenze è di un contratto multilicenza School per le istituzioni primarie e secondarie.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-124">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="3d2f5-125">Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-125">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="3d2f5-126">4</span><span class="sxs-lookup"><span data-stu-id="3d2f5-126">4</span></span> | <span data-ttu-id="3d2f5-127">Il Key Pack per le licenze è da un contratto di licenza di Service provider per i provider di servizi di concedere in licenza il software Microsoft su base mensile.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-127">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="3d2f5-128">Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-128">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="3d2f5-129">5</span><span class="sxs-lookup"><span data-stu-id="3d2f5-129">5</span></span> | <span data-ttu-id="3d2f5-130">Il Key Pack per le licenze è da un altro contratto di licenza, ad esempio Open Value, multiyear Open License e Open Subscription License.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-130">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="3d2f5-131">Il parametro *sAgreementNumber* è il numero di contratto fornito con le informazioni sul programma.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-131">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span> |

<span data-ttu-id="3d2f5-132">*sAgreementNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d2f5-132">*sAgreementNumber* \[in\]</span></span>

<span data-ttu-id="3d2f5-133">Numero di contratto o numero di registrazione.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-133">Agreement number or enrollment number.</span></span> <span data-ttu-id="3d2f5-134">Il parametro *sAgreementNumber* è una stringa numerica di sette cifre senza trattini.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-134">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

<span data-ttu-id="3d2f5-135">*ProductVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d2f5-135">*ProductVersion* \[in\]</span></span>

<span data-ttu-id="3d2f5-136">Versione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-136">Product version.</span></span>

| <span data-ttu-id="3d2f5-137">Valore</span><span class="sxs-lookup"><span data-stu-id="3d2f5-137">Value</span></span> | <span data-ttu-id="3d2f5-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d2f5-138">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="3d2f5-139">0</span><span class="sxs-lookup"><span data-stu-id="3d2f5-139">0</span></span> | <span data-ttu-id="3d2f5-140">Non supportato</span><span class="sxs-lookup"><span data-stu-id="3d2f5-140">Not supported</span></span> |
| <span data-ttu-id="3d2f5-141">1</span><span class="sxs-lookup"><span data-stu-id="3d2f5-141">1</span></span> | <span data-ttu-id="3d2f5-142">Non supportato</span><span class="sxs-lookup"><span data-stu-id="3d2f5-142">Not supported</span></span> |
| <span data-ttu-id="3d2f5-143">2</span><span class="sxs-lookup"><span data-stu-id="3d2f5-143">2</span></span> | <span data-ttu-id="3d2f5-144">Windows Server 2008/Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3d2f5-144">Windows Server 2008/Windows Server 2008 R2</span></span> |
| <span data-ttu-id="3d2f5-145">4</span><span class="sxs-lookup"><span data-stu-id="3d2f5-145">4</span></span> | <span data-ttu-id="3d2f5-146">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3d2f5-146">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="3d2f5-147">5</span><span class="sxs-lookup"><span data-stu-id="3d2f5-147">5</span></span> | <span data-ttu-id="3d2f5-148">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3d2f5-148">Windows Server 2016</span></span> |
| <span data-ttu-id="3d2f5-149">6</span><span class="sxs-lookup"><span data-stu-id="3d2f5-149">6</span></span> | <span data-ttu-id="3d2f5-150">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="3d2f5-150">Windows Server 2019</span></span> |

<span data-ttu-id="3d2f5-151">*ProductType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d2f5-151">*ProductType* \[in\]</span></span>

<span data-ttu-id="3d2f5-152">Tipo di prodotto.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-152">Product type.</span></span>

| <span data-ttu-id="3d2f5-153">Valore</span><span class="sxs-lookup"><span data-stu-id="3d2f5-153">Value</span></span> | <span data-ttu-id="3d2f5-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d2f5-154">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="3d2f5-155">0</span><span class="sxs-lookup"><span data-stu-id="3d2f5-155">0</span></span> | <span data-ttu-id="3d2f5-156">Il tipo di prodotto Servizi Desktop remoto License Key Pack è per dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-156">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="3d2f5-157">Pertanto, ogni dispositivo che si connette al server Host sessione Desktop remoto deve disporre di una licenza.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-157">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="3d2f5-158">1</span><span class="sxs-lookup"><span data-stu-id="3d2f5-158">1</span></span> | <span data-ttu-id="3d2f5-159">Il tipo di prodotto Servizi Desktop remoto License Key Pack è per utente.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-159">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="3d2f5-160">Pertanto, ogni utente che si connette al server Host sessione Desktop remoto deve disporre di una licenza.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-160">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="3d2f5-161">2</span><span class="sxs-lookup"><span data-stu-id="3d2f5-161">2</span></span> | <span data-ttu-id="3d2f5-162">Questo tipo di prodotto non è valido.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-162">This product type is not valid.</span></span> |

<span data-ttu-id="3d2f5-163">*LicenseCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d2f5-163">*LicenseCount* \[in\]</span></span>

<span data-ttu-id="3d2f5-164">Numero di licenze da installare.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-164">Number of licenses to install.</span></span>

<span data-ttu-id="3d2f5-165">*KeyPackId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3d2f5-165">*KeyPackId* \[out\]</span></span>

<span data-ttu-id="3d2f5-166">Riceve l'identificatore del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-166">Receives the key pack identifier.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d2f5-167">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d2f5-167">Return value</span></span>

<span data-ttu-id="3d2f5-168">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-168">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3d2f5-169">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-169">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3d2f5-170">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3d2f5-170">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3d2f5-171">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d2f5-171">Remarks</span></span>

<span data-ttu-id="3d2f5-172">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-172">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3d2f5-173">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="3d2f5-173">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3d2f5-174">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="3d2f5-174">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3d2f5-175">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="3d2f5-175">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3d2f5-176">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3d2f5-176">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d2f5-177">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d2f5-177">Requirements</span></span>

| <span data-ttu-id="3d2f5-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d2f5-178">Requirement</span></span> | <span data-ttu-id="3d2f5-179">Valore</span><span class="sxs-lookup"><span data-stu-id="3d2f5-179">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d2f5-180">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d2f5-180">Minimum supported client</span></span><br/> | <span data-ttu-id="3d2f5-181">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3d2f5-181">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="3d2f5-182">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d2f5-182">Minimum supported server</span></span><br/> | <span data-ttu-id="3d2f5-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d2f5-183">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="3d2f5-184">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3d2f5-184">Namespace</span></span><br/>                | <span data-ttu-id="3d2f5-185">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="3d2f5-185">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="3d2f5-186">MOF</span><span class="sxs-lookup"><span data-stu-id="3d2f5-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d2f5-187"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d2f5-187"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d2f5-188">DLL</span><span class="sxs-lookup"><span data-stu-id="3d2f5-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d2f5-189"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d2f5-189"><dt>TlsWmiProv.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="3d2f5-190">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d2f5-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d2f5-191">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="3d2f5-191">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 


---
title: Metodo ReinstallAgreementLicenseKeyPack della classe Win32_TSLicenseKeyPack
description: Reinstalla un Key Pack di Servizi Desktop remoto License acquistato tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del Key Pack.
ms.assetid: BC3C966B-E6CE-45E2-BC1D-2439B75D4C3C
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ReinstallAgreementLicenseKeyPack
- Metodo ReinstallAgreementLicenseKeyPack Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo ReinstallAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821ff6dc538a670e03757253b616ff16489dc108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517866"
---
# <a name="reinstallagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="09e08-106">Metodo ReinstallAgreementLicenseKeyPack della \_ classe TSLicenseKeyPack Win32</span><span class="sxs-lookup"><span data-stu-id="09e08-106">ReinstallAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="09e08-107">Reinstalla un Key Pack di Servizi Desktop remoto License acquistato tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="09e08-107">Reinstalls a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="09e08-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09e08-108">Syntax</span></span>


```mof
uint32 ReinstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="09e08-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="09e08-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09e08-110">*AgreementType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09e08-110">*AgreementType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09e08-111">Tipo di contratto.</span><span class="sxs-lookup"><span data-stu-id="09e08-111">Agreement type.</span></span>

<dt>

<span data-ttu-id="09e08-112">0</span><span class="sxs-lookup"><span data-stu-id="09e08-112">0</span></span>
</dt> <dd>

<span data-ttu-id="09e08-113">Il Key Pack per le licenze è da un contratto Select Volume License (per i clienti con 250 o più computer).</span><span class="sxs-lookup"><span data-stu-id="09e08-113">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="09e08-114">Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.</span><span class="sxs-lookup"><span data-stu-id="09e08-114">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="09e08-115">1</span><span class="sxs-lookup"><span data-stu-id="09e08-115">1</span></span>
</dt> <dd>

<span data-ttu-id="09e08-116">Il Key Pack per le licenze è da un contratto multilicenza Enterprise per i clienti con 250 o più computer.</span><span class="sxs-lookup"><span data-stu-id="09e08-116">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="09e08-117">Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.</span><span class="sxs-lookup"><span data-stu-id="09e08-117">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="09e08-118">2</span><span class="sxs-lookup"><span data-stu-id="09e08-118">2</span></span>
</dt> <dd>

<span data-ttu-id="09e08-119">Il Key Pack per le licenze è da un contratto multilicenza campus per un Istituto di istruzione superiore.</span><span class="sxs-lookup"><span data-stu-id="09e08-119">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="09e08-120">Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.</span><span class="sxs-lookup"><span data-stu-id="09e08-120">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="09e08-121">3</span><span class="sxs-lookup"><span data-stu-id="09e08-121">3</span></span>
</dt> <dd>

<span data-ttu-id="09e08-122">Il Key Pack per le licenze è di un contratto multilicenza School per le istituzioni primarie e secondarie.</span><span class="sxs-lookup"><span data-stu-id="09e08-122">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="09e08-123">Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.</span><span class="sxs-lookup"><span data-stu-id="09e08-123">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="09e08-124">4</span><span class="sxs-lookup"><span data-stu-id="09e08-124">4</span></span>
</dt> <dd>

<span data-ttu-id="09e08-125">Il Key Pack per le licenze è da un contratto di licenza di Service provider per i provider di servizi di concedere in licenza il software Microsoft su base mensile.</span><span class="sxs-lookup"><span data-stu-id="09e08-125">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="09e08-126">Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.</span><span class="sxs-lookup"><span data-stu-id="09e08-126">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="09e08-127">5</span><span class="sxs-lookup"><span data-stu-id="09e08-127">5</span></span>
</dt> <dd>

<span data-ttu-id="09e08-128">Il Key Pack per le licenze è da un altro contratto di licenza, ad esempio Open Value, multiyear Open License e Open Subscription License.</span><span class="sxs-lookup"><span data-stu-id="09e08-128">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="09e08-129">Il parametro *sAgreementNumber* è il numero di contratto fornito con le informazioni sul programma.</span><span class="sxs-lookup"><span data-stu-id="09e08-129">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="09e08-130">*sAgreementNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09e08-130">*sAgreementNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09e08-131">Numero di contratto o numero di registrazione.</span><span class="sxs-lookup"><span data-stu-id="09e08-131">Agreement number or enrollment number.</span></span> <span data-ttu-id="09e08-132">Il parametro *sAgreementNumber* è una stringa numerica di sette cifre senza trattini.</span><span class="sxs-lookup"><span data-stu-id="09e08-132">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="09e08-133">*ProductVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09e08-133">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09e08-134">Versione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="09e08-134">Product version.</span></span>

<dt>

<span data-ttu-id="09e08-135">0</span><span class="sxs-lookup"><span data-stu-id="09e08-135">0</span></span>
</dt> <dd>

<span data-ttu-id="09e08-136">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="09e08-136">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="09e08-137">1</span><span class="sxs-lookup"><span data-stu-id="09e08-137">1</span></span>
</dt> <dd>

<span data-ttu-id="09e08-138">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="09e08-138">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="09e08-139">2</span><span class="sxs-lookup"><span data-stu-id="09e08-139">2</span></span>
</dt> <dd>

<span data-ttu-id="09e08-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09e08-140">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="09e08-141">*ProductType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09e08-141">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09e08-142">Tipo di prodotto.</span><span class="sxs-lookup"><span data-stu-id="09e08-142">Product type.</span></span>

<dt>

<span data-ttu-id="09e08-143">0</span><span class="sxs-lookup"><span data-stu-id="09e08-143">0</span></span>
</dt> <dd>

<span data-ttu-id="09e08-144">Il tipo di prodotto Servizi Desktop remoto License Key Pack è per dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09e08-144">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="09e08-145">Pertanto, ogni dispositivo che si connette al server Host sessione Desktop remoto deve disporre di una licenza.</span><span class="sxs-lookup"><span data-stu-id="09e08-145">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="09e08-146">1</span><span class="sxs-lookup"><span data-stu-id="09e08-146">1</span></span>
</dt> <dd>

<span data-ttu-id="09e08-147">Il tipo di prodotto Servizi Desktop remoto License Key Pack è per utente.</span><span class="sxs-lookup"><span data-stu-id="09e08-147">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="09e08-148">Pertanto, ogni utente che si connette al server Host sessione Desktop remoto deve disporre di una licenza.</span><span class="sxs-lookup"><span data-stu-id="09e08-148">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="09e08-149">2</span><span class="sxs-lookup"><span data-stu-id="09e08-149">2</span></span>
</dt> <dd>

<span data-ttu-id="09e08-150">Questo tipo di prodotto non è valido.</span><span class="sxs-lookup"><span data-stu-id="09e08-150">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="09e08-151">*LicenseCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09e08-151">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09e08-152">Numero di licenze da installare.</span><span class="sxs-lookup"><span data-stu-id="09e08-152">Number of licenses to install.</span></span>

</dd> <dt>

<span data-ttu-id="09e08-153">*KeyPackId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="09e08-153">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09e08-154">Riceve l'identificatore del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="09e08-154">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09e08-155">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09e08-155">Return value</span></span>

<span data-ttu-id="09e08-156">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="09e08-156">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="09e08-157">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="09e08-157">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="09e08-158">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="09e08-158">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="09e08-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09e08-159">Requirements</span></span>



| <span data-ttu-id="09e08-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="09e08-160">Requirement</span></span> | <span data-ttu-id="09e08-161">Valore</span><span class="sxs-lookup"><span data-stu-id="09e08-161">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="09e08-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09e08-162">Minimum supported client</span></span><br/> | <span data-ttu-id="09e08-163">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="09e08-163">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="09e08-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09e08-164">Minimum supported server</span></span><br/> | <span data-ttu-id="09e08-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09e08-165">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="09e08-166">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="09e08-166">Namespace</span></span><br/>                | <span data-ttu-id="09e08-167">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="09e08-167">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="09e08-168">MOF</span><span class="sxs-lookup"><span data-stu-id="09e08-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09e08-169"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09e08-169"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="09e08-170">DLL</span><span class="sxs-lookup"><span data-stu-id="09e08-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09e08-171"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09e08-171"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09e08-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09e08-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09e08-173">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="09e08-173">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 






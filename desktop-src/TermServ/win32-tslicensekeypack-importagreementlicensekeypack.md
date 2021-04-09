---
title: Metodo ImportAgreementLicenseKeyPack della classe Win32_TSLicenseKeyPack
description: Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License acquistato tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del Key Pack.
ms.assetid: 3C29E691-3734-4D39-A89F-F381F285DC9E
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ImportAgreementLicenseKeyPack
- Metodo ImportAgreementLicenseKeyPack Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo ImportAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff61d022f9cf195eb357817f7733f4ec49e2986f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121367"
---
# <a name="importagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="c7f69-106">Metodo ImportAgreementLicenseKeyPack della \_ classe TSLicenseKeyPack Win32</span><span class="sxs-lookup"><span data-stu-id="c7f69-106">ImportAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="c7f69-107">Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License acquistato tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="c7f69-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7f69-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7f69-108">Syntax</span></span>


```mof
uint32 ImportAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="c7f69-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7f69-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7f69-110">*AgreementType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7f69-110">*AgreementType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-111">Tipo di contratto.</span><span class="sxs-lookup"><span data-stu-id="c7f69-111">Agreement type.</span></span>

<dt>

<span data-ttu-id="c7f69-112">0</span><span class="sxs-lookup"><span data-stu-id="c7f69-112">0</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-113">Il Key Pack per le licenze è da un contratto Select Volume License (per i clienti con 250 o più computer).</span><span class="sxs-lookup"><span data-stu-id="c7f69-113">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="c7f69-114">Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.</span><span class="sxs-lookup"><span data-stu-id="c7f69-114">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="c7f69-115">1</span><span class="sxs-lookup"><span data-stu-id="c7f69-115">1</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-116">Il Key Pack per le licenze è da un contratto multilicenza Enterprise per i clienti con 250 o più computer.</span><span class="sxs-lookup"><span data-stu-id="c7f69-116">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="c7f69-117">Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.</span><span class="sxs-lookup"><span data-stu-id="c7f69-117">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="c7f69-118">2</span><span class="sxs-lookup"><span data-stu-id="c7f69-118">2</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-119">Il Key Pack per le licenze è da un contratto multilicenza campus per un Istituto di istruzione superiore.</span><span class="sxs-lookup"><span data-stu-id="c7f69-119">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="c7f69-120">Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.</span><span class="sxs-lookup"><span data-stu-id="c7f69-120">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="c7f69-121">3</span><span class="sxs-lookup"><span data-stu-id="c7f69-121">3</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-122">Il Key Pack per le licenze è di un contratto multilicenza School per le istituzioni primarie e secondarie.</span><span class="sxs-lookup"><span data-stu-id="c7f69-122">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="c7f69-123">Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.</span><span class="sxs-lookup"><span data-stu-id="c7f69-123">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="c7f69-124">4</span><span class="sxs-lookup"><span data-stu-id="c7f69-124">4</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-125">Il Key Pack per le licenze è da un contratto di licenza di Service provider per i provider di servizi di concedere in licenza il software Microsoft su base mensile.</span><span class="sxs-lookup"><span data-stu-id="c7f69-125">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="c7f69-126">Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.</span><span class="sxs-lookup"><span data-stu-id="c7f69-126">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="c7f69-127">5</span><span class="sxs-lookup"><span data-stu-id="c7f69-127">5</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-128">Il Key Pack per le licenze è da un altro contratto di licenza, ad esempio Open Value, multiyear Open License e Open Subscription License.</span><span class="sxs-lookup"><span data-stu-id="c7f69-128">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="c7f69-129">Il parametro *sAgreementNumber* è il numero di contratto fornito con le informazioni sul programma.</span><span class="sxs-lookup"><span data-stu-id="c7f69-129">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c7f69-130">*sAgreementNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7f69-130">*sAgreementNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-131">Numero di contratto o numero di registrazione.</span><span class="sxs-lookup"><span data-stu-id="c7f69-131">Agreement number or enrollment number.</span></span> <span data-ttu-id="c7f69-132">Il parametro *sAgreementNumber* è una stringa numerica di sette cifre senza trattini.</span><span class="sxs-lookup"><span data-stu-id="c7f69-132">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="c7f69-133">*ProductVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7f69-133">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-134">Versione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="c7f69-134">Product version.</span></span>

<dt>

<span data-ttu-id="c7f69-135">0</span><span class="sxs-lookup"><span data-stu-id="c7f69-135">0</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-136">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="c7f69-136">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c7f69-137">1</span><span class="sxs-lookup"><span data-stu-id="c7f69-137">1</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-138">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="c7f69-138">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c7f69-139">2</span><span class="sxs-lookup"><span data-stu-id="c7f69-139">2</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7f69-140">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c7f69-141">*ProductType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7f69-141">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-142">Tipo di prodotto.</span><span class="sxs-lookup"><span data-stu-id="c7f69-142">Product type.</span></span>

<dt>

<span data-ttu-id="c7f69-143">0</span><span class="sxs-lookup"><span data-stu-id="c7f69-143">0</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-144">Il tipo di prodotto Servizi Desktop remoto License Key Pack è per dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c7f69-144">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="c7f69-145">Pertanto, ogni dispositivo che si connette al server Host sessione Desktop remoto deve disporre di una licenza.</span><span class="sxs-lookup"><span data-stu-id="c7f69-145">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="c7f69-146">1</span><span class="sxs-lookup"><span data-stu-id="c7f69-146">1</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-147">Il tipo di prodotto Servizi Desktop remoto License Key Pack è per utente.</span><span class="sxs-lookup"><span data-stu-id="c7f69-147">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="c7f69-148">Pertanto, ogni utente che si connette al server Host sessione Desktop remoto deve disporre di una licenza.</span><span class="sxs-lookup"><span data-stu-id="c7f69-148">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="c7f69-149">2</span><span class="sxs-lookup"><span data-stu-id="c7f69-149">2</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-150">Questo tipo di prodotto non è valido.</span><span class="sxs-lookup"><span data-stu-id="c7f69-150">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c7f69-151">*LicenseCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7f69-151">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-152">Numero di licenze da importare.</span><span class="sxs-lookup"><span data-stu-id="c7f69-152">Number of licenses to import.</span></span>

</dd> <dt>

<span data-ttu-id="c7f69-153">*sSourceLSName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7f69-153">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-154">Nome dell'origine Desktop remoto server licenze.</span><span class="sxs-lookup"><span data-stu-id="c7f69-154">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="c7f69-155">Si tratta del nome distinto completo o dell'indirizzo IP del server.</span><span class="sxs-lookup"><span data-stu-id="c7f69-155">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="c7f69-156">*sSourceLSProductId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7f69-156">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-157">Identificatore del server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c7f69-157">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="c7f69-158">È una stringa alfanumerica di 35 caratteri che non può includere trattini.</span><span class="sxs-lookup"><span data-stu-id="c7f69-158">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="c7f69-159">*KeyPackId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c7f69-159">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7f69-160">Riceve l'identificatore del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="c7f69-160">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7f69-161">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7f69-161">Return value</span></span>

<span data-ttu-id="c7f69-162">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="c7f69-162">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c7f69-163">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="c7f69-163">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c7f69-164">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c7f69-164">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7f69-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7f69-165">Requirements</span></span>



| <span data-ttu-id="c7f69-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7f69-166">Requirement</span></span> | <span data-ttu-id="c7f69-167">Valore</span><span class="sxs-lookup"><span data-stu-id="c7f69-167">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7f69-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7f69-168">Minimum supported client</span></span><br/> | <span data-ttu-id="c7f69-169">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c7f69-169">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c7f69-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7f69-170">Minimum supported server</span></span><br/> | <span data-ttu-id="c7f69-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7f69-171">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c7f69-172">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c7f69-172">Namespace</span></span><br/>                | <span data-ttu-id="c7f69-173">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c7f69-173">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="c7f69-174">MOF</span><span class="sxs-lookup"><span data-stu-id="c7f69-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7f69-175"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7f69-175"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7f69-176">DLL</span><span class="sxs-lookup"><span data-stu-id="c7f69-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7f69-177"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7f69-177"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7f69-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7f69-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7f69-179">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="c7f69-179">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 






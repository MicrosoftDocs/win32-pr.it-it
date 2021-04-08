---
title: Metodo ImportRetailPurchaseLicenseKeyPack della classe Win32_TSLicenseKeyPack
description: Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License acquistato tramite un canale di vendita al dettaglio.
ms.assetid: B45C3263-216E-4284-89A1-BE2ADE3A8E84
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ImportRetailPurchaseLicenseKeyPack
- Metodo ImportRetailPurchaseLicenseKeyPack Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo ImportRetailPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2699d1f96827f9ace0f111a4c95adb64d5f8467e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741767"
---
# <a name="importretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="1f131-106">Metodo ImportRetailPurchaseLicenseKeyPack della \_ classe TSLicenseKeyPack Win32</span><span class="sxs-lookup"><span data-stu-id="1f131-106">ImportRetailPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="1f131-107">Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License acquistato tramite un canale di vendita al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="1f131-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f131-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f131-108">Syntax</span></span>


```mof
uint32 ImportRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="1f131-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f131-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f131-110">*sLicenseCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f131-110">*sLicenseCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f131-111">Contiene il codice di licenza di 25 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1f131-111">Contains the 25-character license code.</span></span> <span data-ttu-id="1f131-112">Come input deve essere specificata solo la stringa di caratteri alfanumerici di 25 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1f131-112">Only the 25-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="1f131-113">Nessun trattino da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="1f131-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="1f131-114">*sSourceLSName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f131-114">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f131-115">Nome dell'origine Desktop remoto server licenze.</span><span class="sxs-lookup"><span data-stu-id="1f131-115">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="1f131-116">Si tratta del nome distinto completo o dell'indirizzo IP del server.</span><span class="sxs-lookup"><span data-stu-id="1f131-116">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="1f131-117">*sSourceLSProductId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f131-117">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f131-118">Identificatore del server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="1f131-118">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="1f131-119">È una stringa alfanumerica di 35 caratteri che non può includere trattini.</span><span class="sxs-lookup"><span data-stu-id="1f131-119">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="1f131-120">*KeyPackId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1f131-120">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f131-121">Riceve l'identificatore del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="1f131-121">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f131-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1f131-122">Return value</span></span>

<span data-ttu-id="1f131-123">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="1f131-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1f131-124">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="1f131-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1f131-125">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1f131-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f131-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f131-126">Requirements</span></span>



| <span data-ttu-id="1f131-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f131-127">Requirement</span></span> | <span data-ttu-id="1f131-128">Valore</span><span class="sxs-lookup"><span data-stu-id="1f131-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f131-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f131-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1f131-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1f131-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="1f131-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f131-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1f131-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f131-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="1f131-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1f131-133">Namespace</span></span><br/>                | <span data-ttu-id="1f131-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="1f131-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="1f131-135">MOF</span><span class="sxs-lookup"><span data-stu-id="1f131-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f131-136"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f131-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f131-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1f131-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f131-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f131-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f131-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f131-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f131-140">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="1f131-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 






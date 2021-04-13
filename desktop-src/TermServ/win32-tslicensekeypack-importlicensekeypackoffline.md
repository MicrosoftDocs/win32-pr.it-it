---
title: Metodo ImportLicenseKeyPackOffline della classe Win32_TSLicenseKeyPack
description: Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License che usa un identificatore di licenza ricevuto tramite Internet o il telefono.
ms.assetid: 69D65917-8B82-4C24-AFFA-BBE529D3883C
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ImportLicenseKeyPackOffline
- Metodo ImportLicenseKeyPackOffline Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo ImportLicenseKeyPackOffline
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de474cce6eb91cdc605588f7f4a63d97f985769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517871"
---
# <a name="importlicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="21e05-106">Metodo ImportLicenseKeyPackOffline della \_ classe TSLicenseKeyPack Win32</span><span class="sxs-lookup"><span data-stu-id="21e05-106">ImportLicenseKeyPackOffline method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="21e05-107">Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License che usa un identificatore di licenza ricevuto tramite Internet o il telefono.</span><span class="sxs-lookup"><span data-stu-id="21e05-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that uses a license identifier that was received over the Internet or the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="21e05-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21e05-108">Syntax</span></span>


```mof
uint32 ImportLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="21e05-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="21e05-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21e05-110">*sLicenseKeyPackId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21e05-110">*sLicenseKeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e05-111">Contiene il codice di licenza a 35 caratteri.</span><span class="sxs-lookup"><span data-stu-id="21e05-111">Contains the 35-character license code.</span></span> <span data-ttu-id="21e05-112">Come input è necessario assegnare solo la stringa di caratteri alfanumerici a 35 caratteri.</span><span class="sxs-lookup"><span data-stu-id="21e05-112">Only the 35-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="21e05-113">Nessun trattino da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="21e05-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="21e05-114">*sSourceLSName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21e05-114">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e05-115">Nome dell'origine Desktop remoto server licenze.</span><span class="sxs-lookup"><span data-stu-id="21e05-115">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="21e05-116">Si tratta del nome distinto completo o dell'indirizzo IP del server.</span><span class="sxs-lookup"><span data-stu-id="21e05-116">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="21e05-117">*sSourceLSProductId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21e05-117">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e05-118">Identificatore del server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="21e05-118">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="21e05-119">È una stringa alfanumerica di 35 caratteri che non può includere trattini.</span><span class="sxs-lookup"><span data-stu-id="21e05-119">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="21e05-120">*KeyPackId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="21e05-120">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21e05-121">Riceve l'identificatore del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="21e05-121">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21e05-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21e05-122">Return value</span></span>

<span data-ttu-id="21e05-123">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="21e05-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="21e05-124">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="21e05-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="21e05-125">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="21e05-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="21e05-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21e05-126">Requirements</span></span>



| <span data-ttu-id="21e05-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="21e05-127">Requirement</span></span> | <span data-ttu-id="21e05-128">Valore</span><span class="sxs-lookup"><span data-stu-id="21e05-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="21e05-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21e05-129">Minimum supported client</span></span><br/> | <span data-ttu-id="21e05-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="21e05-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="21e05-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21e05-131">Minimum supported server</span></span><br/> | <span data-ttu-id="21e05-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21e05-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="21e05-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="21e05-133">Namespace</span></span><br/>                | <span data-ttu-id="21e05-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="21e05-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="21e05-135">MOF</span><span class="sxs-lookup"><span data-stu-id="21e05-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21e05-136"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21e05-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="21e05-137">DLL</span><span class="sxs-lookup"><span data-stu-id="21e05-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21e05-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21e05-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21e05-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21e05-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21e05-140">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="21e05-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 






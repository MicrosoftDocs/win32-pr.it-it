---
title: Metodo ReinstallRetailPurchaseLicenseKeyPack della classe Win32_TSLicenseKeyPack
description: Reinstalla un Key Pack di Servizi Desktop remoto License acquistato tramite un canale di vendita al dettaglio.
ms.assetid: 19528726-8DEB-4D03-BFA6-647C8A612FA2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ReinstallRetailPurchaseLicenseKeyPack
- Metodo ReinstallRetailPurchaseLicenseKeyPack Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo ReinstallRetailPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4caa8635eaf28ad823add500883832a7fe885b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047955"
---
# <a name="reinstallretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="15d6e-106">Metodo ReinstallRetailPurchaseLicenseKeyPack della \_ classe TSLicenseKeyPack Win32</span><span class="sxs-lookup"><span data-stu-id="15d6e-106">ReinstallRetailPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="15d6e-107">Reinstalla un Key Pack di Servizi Desktop remoto License acquistato tramite un canale di vendita al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="15d6e-107">Reinstalls a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="15d6e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15d6e-108">Syntax</span></span>


```mof
uint32 ReinstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="15d6e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="15d6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15d6e-110">*sLicenseCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15d6e-110">*sLicenseCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15d6e-111">Contiene il codice di licenza di 25 caratteri.</span><span class="sxs-lookup"><span data-stu-id="15d6e-111">Contains the 25-character license code.</span></span> <span data-ttu-id="15d6e-112">Come input deve essere specificata solo la stringa di caratteri alfanumerici di 25 caratteri.</span><span class="sxs-lookup"><span data-stu-id="15d6e-112">Only the 25-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="15d6e-113">Nessun trattino da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="15d6e-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="15d6e-114">*KeyPackId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="15d6e-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15d6e-115">Riceve l'identificatore del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="15d6e-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15d6e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15d6e-116">Return value</span></span>

<span data-ttu-id="15d6e-117">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="15d6e-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="15d6e-118">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="15d6e-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="15d6e-119">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="15d6e-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15d6e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15d6e-120">Requirements</span></span>



| <span data-ttu-id="15d6e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="15d6e-121">Requirement</span></span> | <span data-ttu-id="15d6e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="15d6e-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="15d6e-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15d6e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="15d6e-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="15d6e-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="15d6e-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15d6e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="15d6e-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15d6e-126">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="15d6e-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="15d6e-127">Namespace</span></span><br/>                | <span data-ttu-id="15d6e-128">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="15d6e-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="15d6e-129">MOF</span><span class="sxs-lookup"><span data-stu-id="15d6e-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15d6e-130"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15d6e-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="15d6e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="15d6e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15d6e-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15d6e-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15d6e-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15d6e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15d6e-134">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="15d6e-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 






---
title: Metodo ReinstallLicenseKeyPackOffline della classe Win32_TSLicenseKeyPack
description: Reinstalla un Key Pack di Servizi Desktop remoto License che utilizza l'identificatore di licenza ricevuto tramite Internet o il telefono.
ms.assetid: CFDB4C3B-C7C1-4670-BC87-92727057A500
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ReinstallLicenseKeyPackOffline
- Metodo ReinstallLicenseKeyPackOffline Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo ReinstallLicenseKeyPackOffline
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e805521ea750c018ab2e7965e7fbfba05a92d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873409"
---
# <a name="reinstalllicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="58ca0-106">Metodo ReinstallLicenseKeyPackOffline della \_ classe TSLicenseKeyPack Win32</span><span class="sxs-lookup"><span data-stu-id="58ca0-106">ReinstallLicenseKeyPackOffline method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="58ca0-107">Reinstalla un Key Pack di Servizi Desktop remoto License che utilizza l'identificatore di licenza ricevuto tramite Internet o il telefono.</span><span class="sxs-lookup"><span data-stu-id="58ca0-107">Reinstalls a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="58ca0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58ca0-108">Syntax</span></span>


```mof
uint32 ReinstallLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="58ca0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="58ca0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58ca0-110">*sLicenseKeyPackId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58ca0-110">*sLicenseKeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ca0-111">Contiene il codice di licenza a 35 caratteri.</span><span class="sxs-lookup"><span data-stu-id="58ca0-111">Contains the 35-character license code.</span></span> <span data-ttu-id="58ca0-112">Come input è necessario assegnare solo la stringa di caratteri alfanumerici a 35 caratteri.</span><span class="sxs-lookup"><span data-stu-id="58ca0-112">Only the 35-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="58ca0-113">Nessun trattino da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="58ca0-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="58ca0-114">*KeyPackId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="58ca0-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58ca0-115">Riceve l'identificatore del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="58ca0-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58ca0-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58ca0-116">Return value</span></span>

<span data-ttu-id="58ca0-117">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="58ca0-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="58ca0-118">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="58ca0-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="58ca0-119">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="58ca0-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="58ca0-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58ca0-120">Requirements</span></span>



| <span data-ttu-id="58ca0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="58ca0-121">Requirement</span></span> | <span data-ttu-id="58ca0-122">Valore</span><span class="sxs-lookup"><span data-stu-id="58ca0-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="58ca0-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58ca0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="58ca0-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="58ca0-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="58ca0-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58ca0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="58ca0-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58ca0-126">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="58ca0-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="58ca0-127">Namespace</span></span><br/>                | <span data-ttu-id="58ca0-128">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="58ca0-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="58ca0-129">MOF</span><span class="sxs-lookup"><span data-stu-id="58ca0-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58ca0-130"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58ca0-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="58ca0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="58ca0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58ca0-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58ca0-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58ca0-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58ca0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ca0-134">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="58ca0-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 






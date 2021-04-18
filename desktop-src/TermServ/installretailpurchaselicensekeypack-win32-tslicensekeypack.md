---
title: Metodo InstallRetailPurchaseLicenseKeyPack della classe Win32_TSLicenseKeyPack
description: Installa un Key Pack di licenza Servizi Desktop remoto acquistato tramite un canale di vendita al dettaglio.
ms.assetid: cd33c785-7aa1-4e30-8155-4176b6f4c037
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo InstallRetailPurchaseLicenseKeyPack
- Metodo InstallRetailPurchaseLicenseKeyPack Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo InstallRetailPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7523e2106a68284d6b9b376d47608114f940c194
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301211"
---
# <a name="installretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="e2019-106">Metodo InstallRetailPurchaseLicenseKeyPack della \_ classe TSLicenseKeyPack Win32</span><span class="sxs-lookup"><span data-stu-id="e2019-106">InstallRetailPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="e2019-107">Installa un Key Pack di licenza Servizi Desktop remoto acquistato tramite un canale di vendita al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="e2019-107">Installs a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2019-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2019-108">Syntax</span></span>


```mof
uint32 InstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="e2019-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2019-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2019-110">*sLicenseCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2019-110">*sLicenseCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2019-111">Contiene il codice di licenza di 25 caratteri.</span><span class="sxs-lookup"><span data-stu-id="e2019-111">Contains the 25-character license code.</span></span> <span data-ttu-id="e2019-112">Come input deve essere specificata solo la stringa di caratteri alfanumerici di 25 caratteri.</span><span class="sxs-lookup"><span data-stu-id="e2019-112">Only the 25-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="e2019-113">Nessun trattino da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e2019-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="e2019-114">*KeyPackId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e2019-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2019-115">Riceve l'identificatore del Key Pack.</span><span class="sxs-lookup"><span data-stu-id="e2019-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2019-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2019-116">Return value</span></span>

<span data-ttu-id="e2019-117">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="e2019-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e2019-118">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="e2019-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e2019-119">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e2019-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e2019-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2019-120">Remarks</span></span>

<span data-ttu-id="e2019-121">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="e2019-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e2019-122">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e2019-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e2019-123">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="e2019-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e2019-124">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="e2019-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e2019-125">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e2019-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2019-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2019-126">Requirements</span></span>



| <span data-ttu-id="e2019-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2019-127">Requirement</span></span> | <span data-ttu-id="e2019-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e2019-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2019-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2019-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e2019-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e2019-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e2019-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2019-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e2019-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2019-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e2019-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e2019-133">Namespace</span></span><br/>                | <span data-ttu-id="e2019-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e2019-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e2019-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e2019-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2019-136"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2019-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2019-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e2019-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2019-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2019-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2019-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2019-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2019-140">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="e2019-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 


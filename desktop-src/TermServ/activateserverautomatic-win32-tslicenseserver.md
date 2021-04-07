---
title: Metodo ActivateServerAutomatic della classe Win32_TSLicenseServer
description: Attiva automaticamente il server licenze Desktop remoto tramite Internet.
ms.assetid: a33ba72f-3403-4bd2-94a9-0c5ef1cbb03e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ActivateServerAutomatic
- Metodo ActivateServerAutomatic Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo ActivateServerAutomatic
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68879dbc40cc4161edcfef631bf9bb4b72558df8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963976"
---
# <a name="activateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="4788d-106">Metodo ActivateServerAutomatic della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="4788d-106">ActivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="4788d-107">Attiva automaticamente il server licenze Desktop remoto tramite Internet.</span><span class="sxs-lookup"><span data-stu-id="4788d-107">Activates the Remote Desktop license server automatically over the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="4788d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4788d-108">Syntax</span></span>


```mof
uint32 ActivateServerAutomatic(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="4788d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4788d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4788d-110">*ActivationStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4788d-110">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4788d-111">Lo stato di attivazione restituito può essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="4788d-111">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="4788d-112">0</span><span class="sxs-lookup"><span data-stu-id="4788d-112">0</span></span>
</dt> <dd>

<span data-ttu-id="4788d-113">Il server licenze Desktop remoto viene attivato.</span><span class="sxs-lookup"><span data-stu-id="4788d-113">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="4788d-114">1</span><span class="sxs-lookup"><span data-stu-id="4788d-114">1</span></span>
</dt> <dd>

<span data-ttu-id="4788d-115">Il server licenze Desktop remoto non è attivato.</span><span class="sxs-lookup"><span data-stu-id="4788d-115">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="4788d-116">2</span><span class="sxs-lookup"><span data-stu-id="4788d-116">2</span></span>
</dt> <dd>

<span data-ttu-id="4788d-117">Si è verificato un errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="4788d-117">An unknown error occurred.</span></span> <span data-ttu-id="4788d-118">Non è noto se il server licenze Desktop remoto è attivato.</span><span class="sxs-lookup"><span data-stu-id="4788d-118">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4788d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4788d-119">Return value</span></span>

<span data-ttu-id="4788d-120">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="4788d-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4788d-121">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="4788d-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4788d-122">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4788d-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4788d-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="4788d-123">Remarks</span></span>

<span data-ttu-id="4788d-124">Questo metodo ha esito negativo a meno che non siano impostate le proprietà **FirstName**, **LastName**, **Company** e **CountryRegion** .</span><span class="sxs-lookup"><span data-stu-id="4788d-124">This method fails unless the **FirstName**, **LastName**, **Company**, and **CountryRegion** properties are set.</span></span>

<span data-ttu-id="4788d-125">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="4788d-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4788d-126">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4788d-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4788d-127">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="4788d-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4788d-128">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="4788d-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4788d-129">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4788d-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4788d-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4788d-130">Requirements</span></span>



| <span data-ttu-id="4788d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4788d-131">Requirement</span></span> | <span data-ttu-id="4788d-132">Valore</span><span class="sxs-lookup"><span data-stu-id="4788d-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4788d-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4788d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4788d-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4788d-134">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="4788d-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4788d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4788d-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4788d-136">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="4788d-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4788d-137">Namespace</span></span><br/>                | <span data-ttu-id="4788d-138">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="4788d-138">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="4788d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="4788d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4788d-140"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4788d-140"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4788d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4788d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4788d-142"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4788d-142"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4788d-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4788d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4788d-144">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="4788d-144">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


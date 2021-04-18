---
title: Metodo ActivateServer della classe Win32_TSLicenseServer
description: Attiva il server licenze Desktop remoto usando un identificatore del server licenze Desktop remoto ottenuto tramite telefono o Internet.
ms.assetid: 628e87f0-600e-404d-a0b4-35f1570b4fc0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ActivateServer
- Metodo ActivateServer Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo ActivateServer
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19db0df0ca9b0bf41fe692ba07fe605dc1e8d5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302479"
---
# <a name="activateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="bf8e3-106">Metodo ActivateServer della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="bf8e3-106">ActivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="bf8e3-107">Attiva il server licenze Desktop remoto usando un identificatore del server licenze Desktop remoto ottenuto tramite telefono o Internet.</span><span class="sxs-lookup"><span data-stu-id="bf8e3-107">Activates the Remote Desktop license server by using a Remote Desktop license server identifier that is obtained over the phone or the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf8e3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf8e3-108">Syntax</span></span>


```mof
uint32 ActivateServer(
  [in]  string sLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="bf8e3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf8e3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf8e3-110">*sLicenseServerId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf8e3-110">*sLicenseServerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf8e3-111">Desktop remoto ID del server licenze ottenuto sul telefono o su Internet.</span><span class="sxs-lookup"><span data-stu-id="bf8e3-111">Remote Desktop license server ID that was obtained over the phone or the Internet.</span></span> <span data-ttu-id="bf8e3-112">Il parametro *sLicenseServerId* è una stringa alfanumerica di 35 caratteri che non può includere trattini.</span><span class="sxs-lookup"><span data-stu-id="bf8e3-112">The *sLicenseServerId* parameter is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="bf8e3-113">*ActivationStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bf8e3-113">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf8e3-114">Lo stato di attivazione restituito può essere uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="bf8e3-114">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="bf8e3-115">0</span><span class="sxs-lookup"><span data-stu-id="bf8e3-115">0</span></span>
</dt> <dd>

<span data-ttu-id="bf8e3-116">Il server licenze Desktop remoto viene attivato.</span><span class="sxs-lookup"><span data-stu-id="bf8e3-116">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="bf8e3-117">1</span><span class="sxs-lookup"><span data-stu-id="bf8e3-117">1</span></span>
</dt> <dd>

<span data-ttu-id="bf8e3-118">Il server licenze Desktop remoto non è attivato.</span><span class="sxs-lookup"><span data-stu-id="bf8e3-118">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="bf8e3-119">2</span><span class="sxs-lookup"><span data-stu-id="bf8e3-119">2</span></span>
</dt> <dd>

<span data-ttu-id="bf8e3-120">Si è verificato un errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="bf8e3-120">An unknown error occurred.</span></span> <span data-ttu-id="bf8e3-121">Non è noto se il server licenze Desktop remoto è attivato.</span><span class="sxs-lookup"><span data-stu-id="bf8e3-121">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf8e3-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf8e3-122">Return value</span></span>

<span data-ttu-id="bf8e3-123">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="bf8e3-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bf8e3-124">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="bf8e3-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bf8e3-125">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bf8e3-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bf8e3-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf8e3-126">Remarks</span></span>

<span data-ttu-id="bf8e3-127">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="bf8e3-127">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="bf8e3-128">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bf8e3-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bf8e3-129">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="bf8e3-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bf8e3-130">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="bf8e3-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bf8e3-131">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bf8e3-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf8e3-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf8e3-132">Requirements</span></span>



| <span data-ttu-id="bf8e3-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf8e3-133">Requirement</span></span> | <span data-ttu-id="bf8e3-134">Valore</span><span class="sxs-lookup"><span data-stu-id="bf8e3-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf8e3-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf8e3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bf8e3-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bf8e3-136">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="bf8e3-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf8e3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bf8e3-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf8e3-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="bf8e3-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bf8e3-139">Namespace</span></span><br/>                | <span data-ttu-id="bf8e3-140">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="bf8e3-140">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="bf8e3-141">MOF</span><span class="sxs-lookup"><span data-stu-id="bf8e3-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf8e3-142"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf8e3-142"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf8e3-143">DLL</span><span class="sxs-lookup"><span data-stu-id="bf8e3-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf8e3-144"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf8e3-144"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf8e3-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf8e3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf8e3-146">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="bf8e3-146">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


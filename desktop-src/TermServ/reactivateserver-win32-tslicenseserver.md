---
title: Metodo ReactivateServer della classe Win32_TSLicenseServer
description: Riattiva il server licenze Desktop remoto usando un nuovo identificatore ottenuto sul telefono o su Internet.
ms.assetid: dd9ff938-a683-4f60-b7cc-7580892953b6
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ReactivateServer
- Metodo ReactivateServer Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo ReactivateServer
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50e84eb0bed0b52ad463fce50ce334d6c8eb8d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476709"
---
# <a name="reactivateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="4d8bb-106">Metodo ReactivateServer della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="4d8bb-106">ReactivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="4d8bb-107">Riattiva il server licenze Desktop remoto usando un nuovo identificatore ottenuto sul telefono o su Internet.</span><span class="sxs-lookup"><span data-stu-id="4d8bb-107">Reactivates the Remote Desktop license server by using a new identifier that was obtained over the phone or the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d8bb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d8bb-108">Syntax</span></span>


```mof
uint32 ReactivateServer(
  [in]  string sNewLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="4d8bb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d8bb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d8bb-110">*sNewLicenseServerId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d8bb-110">*sNewLicenseServerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d8bb-111">Desktop remoto ID del server licenze ottenuto sul telefono o su Internet.</span><span class="sxs-lookup"><span data-stu-id="4d8bb-111">Remote Desktop license server ID that was obtained over the phone or the Internet.</span></span>

</dd> <dt>

<span data-ttu-id="4d8bb-112">*ActivationStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4d8bb-112">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d8bb-113">Lo stato di attivazione restituito può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4d8bb-113">The activation status returned can be one of the following values.</span></span>

<dt>

<span data-ttu-id="4d8bb-114">0</span><span class="sxs-lookup"><span data-stu-id="4d8bb-114">0</span></span>
</dt> <dd>

<span data-ttu-id="4d8bb-115">Il server licenze Desktop remoto viene attivato.</span><span class="sxs-lookup"><span data-stu-id="4d8bb-115">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="4d8bb-116">1</span><span class="sxs-lookup"><span data-stu-id="4d8bb-116">1</span></span>
</dt> <dd>

<span data-ttu-id="4d8bb-117">Il server licenze Desktop remoto non è attivato.</span><span class="sxs-lookup"><span data-stu-id="4d8bb-117">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="4d8bb-118">2</span><span class="sxs-lookup"><span data-stu-id="4d8bb-118">2</span></span>
</dt> <dd>

<span data-ttu-id="4d8bb-119">Si è verificato un errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="4d8bb-119">An unknown error occurred.</span></span> <span data-ttu-id="4d8bb-120">Non è noto se il server licenze Desktop remoto è attivato.</span><span class="sxs-lookup"><span data-stu-id="4d8bb-120">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d8bb-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d8bb-121">Return value</span></span>

<span data-ttu-id="4d8bb-122">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="4d8bb-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4d8bb-123">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="4d8bb-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4d8bb-124">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4d8bb-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4d8bb-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d8bb-125">Remarks</span></span>

<span data-ttu-id="4d8bb-126">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="4d8bb-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4d8bb-127">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4d8bb-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4d8bb-128">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="4d8bb-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4d8bb-129">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="4d8bb-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4d8bb-130">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4d8bb-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d8bb-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d8bb-131">Requirements</span></span>



| <span data-ttu-id="4d8bb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d8bb-132">Requirement</span></span> | <span data-ttu-id="4d8bb-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4d8bb-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d8bb-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d8bb-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4d8bb-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4d8bb-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="4d8bb-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d8bb-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4d8bb-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d8bb-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="4d8bb-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4d8bb-138">Namespace</span></span><br/>                | <span data-ttu-id="4d8bb-139">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="4d8bb-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="4d8bb-140">MOF</span><span class="sxs-lookup"><span data-stu-id="4d8bb-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d8bb-141"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d8bb-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d8bb-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4d8bb-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d8bb-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d8bb-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d8bb-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d8bb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d8bb-145">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="4d8bb-145">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


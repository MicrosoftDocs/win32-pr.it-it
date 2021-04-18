---
title: Metodo IsLSinTSLSGroup della classe Win32_TSLicenseServer
description: Recupera un valore che indica se il server licenze Desktop remoto è un membro del gruppo server licenze Desktop remoto in un controller di dominio in un determinato dominio.
ms.assetid: a6ad7f09-8972-47d4-8b3b-cd129b400ea8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsLSinTSLSGroup
- Metodo IsLSinTSLSGroup Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo IsLSinTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSinTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de3577e4632167612b4d71841501a2a2845203a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301869"
---
# <a name="islsintslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="493ac-106">Metodo IsLSinTSLSGroup della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="493ac-106">IsLSinTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="493ac-107">Recupera un valore che indica se il server licenze Desktop remoto è un membro del gruppo server licenze Desktop remoto in un controller di dominio in un determinato dominio.</span><span class="sxs-lookup"><span data-stu-id="493ac-107">Retrieves whether the Remote Desktop license server is a member of the Remote Desktop license server group on a domain controller in a given domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="493ac-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="493ac-108">Syntax</span></span>


```mof
uint32 IsLSinTSLSGroup(
  [in]  string  Domain,
  [out] boolean IsMember
);
```



## <a name="parameters"></a><span data-ttu-id="493ac-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="493ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="493ac-110">*Dominio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="493ac-110">*Domain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="493ac-111">Nome del dominio.</span><span class="sxs-lookup"><span data-stu-id="493ac-111">The domain name.</span></span>

</dd> <dt>

<span data-ttu-id="493ac-112">*Membro* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="493ac-112">*IsMember* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="493ac-113">Valore booleano che indica se il server licenze è un membro del gruppo di server licenze Desktop remoto nel dominio.</span><span class="sxs-lookup"><span data-stu-id="493ac-113">Boolean value that indicates whether the license server is a member of the Remote Desktop license server group in the domain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="493ac-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="493ac-114">Return value</span></span>

<span data-ttu-id="493ac-115">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="493ac-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="493ac-116">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="493ac-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="493ac-117">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="493ac-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="493ac-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="493ac-118">Remarks</span></span>

<span data-ttu-id="493ac-119">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="493ac-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="493ac-120">Se non viene specificato alcun nome di dominio, viene eseguita una query su un controller di dominio nello stesso dominio del server licenze.</span><span class="sxs-lookup"><span data-stu-id="493ac-120">If no domain name is provided, a domain controller in the same domain as the license server is queried.</span></span>

<span data-ttu-id="493ac-121">Il server licenze deve essere membro del gruppo server licenze Desktop remoto se il server è configurato per l'utilizzo dell'ambito di individuazione dominio o foresta.</span><span class="sxs-lookup"><span data-stu-id="493ac-121">The license server should be a member of the Remote Desktop license server group if the server is configured to use the domain or forest discovery scope.</span></span> <span data-ttu-id="493ac-122">Se il server licenze non è un membro di questo gruppo, il monitoraggio e la creazione di report delle licenze per utente non funzioneranno.</span><span class="sxs-lookup"><span data-stu-id="493ac-122">If the license server is not a member of this group, per-user license tracking and reporting will not work.</span></span>

<span data-ttu-id="493ac-123">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="493ac-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="493ac-124">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="493ac-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="493ac-125">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="493ac-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="493ac-126">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="493ac-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="493ac-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="493ac-127">Requirements</span></span>



| <span data-ttu-id="493ac-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="493ac-128">Requirement</span></span> | <span data-ttu-id="493ac-129">Valore</span><span class="sxs-lookup"><span data-stu-id="493ac-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="493ac-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="493ac-130">Minimum supported client</span></span><br/> | <span data-ttu-id="493ac-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="493ac-131">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="493ac-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="493ac-132">Minimum supported server</span></span><br/> | <span data-ttu-id="493ac-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="493ac-133">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="493ac-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="493ac-134">Namespace</span></span><br/>                | <span data-ttu-id="493ac-135">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="493ac-135">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="493ac-136">MOF</span><span class="sxs-lookup"><span data-stu-id="493ac-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="493ac-137"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="493ac-137"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="493ac-138">DLL</span><span class="sxs-lookup"><span data-stu-id="493ac-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="493ac-139"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="493ac-139"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="493ac-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="493ac-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="493ac-141">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="493ac-141">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="493ac-142">**AddLStoTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="493ac-142">**AddLStoTSLSGroup**</span></span>](addlstotslsgroup-win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="493ac-143">**RemoveLSfromTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="493ac-143">**RemoveLSfromTSLSGroup**</span></span>](removelsfromtslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 


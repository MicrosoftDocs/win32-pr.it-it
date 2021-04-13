---
title: Metodo IsSecureAccessAllowed della classe Win32_TSLicenseServer
description: Recupera un valore che indica se host sessione Desktop remoto un server Host sessione Desktop remoto può richiedere Servizi Desktop remoto licenze di accesso client (RDS \ 160; Licenze CAL) dal server licenze Desktop remoto.
ms.assetid: b9124808-79be-4b94-b12b-f093d5e8195a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsSecureAccessAllowed
- Metodo IsSecureAccessAllowed Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo IsSecureAccessAllowed
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsSecureAccessAllowed
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf35fd8b38139027955fde51a209000435744f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517740"
---
# <a name="issecureaccessallowed-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="e82ff-106">Metodo IsSecureAccessAllowed della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="e82ff-106">IsSecureAccessAllowed method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="e82ff-107">Recupera un valore che indica se un server Host sessione Desktop remoto (host sessione Desktop remoto) può richiedere Servizi Desktop remoto licenze CAL (Client Access License) dal server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="e82ff-107">Retrieves whether a Remote Desktop Session Host (RD Session Host) server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e82ff-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e82ff-108">Syntax</span></span>


```mof
uint32 IsSecureAccessAllowed(
  [in]  string  tsname,
  [out] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="e82ff-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e82ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e82ff-110">*tsname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e82ff-110">*tsname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e82ff-111">Nome del server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="e82ff-111">Name of the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="e82ff-112">*Consentito* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e82ff-112">*Allowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e82ff-113">Valore booleano che indica se il server Host sessione Desktop remoto è autorizzato a richiedere licenze CAL Servizi Desktop remoto dal server licenze.</span><span class="sxs-lookup"><span data-stu-id="e82ff-113">Boolean value that indicates whether the RD Session Host server is allowed to request RDS CALs from the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e82ff-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e82ff-114">Return value</span></span>

<span data-ttu-id="e82ff-115">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="e82ff-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e82ff-116">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="e82ff-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e82ff-117">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e82ff-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e82ff-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="e82ff-118">Remarks</span></span>

<span data-ttu-id="e82ff-119">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="e82ff-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e82ff-120">Il valore restituito è basato sull'impostazione di criteri di gruppo "gruppo di sicurezza del server licenze" e sull'appartenenza al gruppo locale computer Terminal Server nel server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="e82ff-120">The returned value is based on the "license server security group" group policy setting, and membership in the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

<span data-ttu-id="e82ff-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e82ff-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e82ff-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="e82ff-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e82ff-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="e82ff-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e82ff-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e82ff-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e82ff-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e82ff-125">Requirements</span></span>



| <span data-ttu-id="e82ff-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e82ff-126">Requirement</span></span> | <span data-ttu-id="e82ff-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e82ff-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e82ff-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e82ff-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e82ff-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e82ff-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e82ff-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e82ff-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e82ff-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e82ff-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e82ff-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e82ff-132">Namespace</span></span><br/>                | <span data-ttu-id="e82ff-133">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e82ff-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e82ff-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e82ff-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e82ff-135"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e82ff-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e82ff-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e82ff-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e82ff-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e82ff-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e82ff-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e82ff-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e82ff-139">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="e82ff-139">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="e82ff-140">**IsLSSecGrpGPEnabled**</span><span class="sxs-lookup"><span data-stu-id="e82ff-140">**IsLSSecGrpGPEnabled**</span></span>](islssecgrpgpenabled-win32-tslicenseserver.md)
</dt> </dl>

 


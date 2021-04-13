---
title: Metodo ChangeRole della classe Win32_TSLicenseServer
description: Modifica l'ambito di individuazione del server licenze Desktop remoto. L'ambito di individuazione determina host sessione Desktop remoto quali server Host sessione Desktop remoto nella rete possono individuare automaticamente il server licenze.
ms.assetid: 3d98fd8a-4ade-489f-8edd-5df1227f15cd
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ChangeRole
- Metodo ChangeRole Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo ChangeRole
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ChangeRole
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9746b856c74e9603751fe85bb861e2b6869f03a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475796"
---
# <a name="changerole-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="af4ba-107">Metodo ChangeRole della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="af4ba-107">ChangeRole method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="af4ba-108">Modifica l'ambito di individuazione del server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="af4ba-108">Changes the discovery scope of the Remote Desktop license server.</span></span> <span data-ttu-id="af4ba-109">L'ambito di individuazione determina host sessione Desktop remoto quali server Host sessione Desktop remoto nella rete possono individuare automaticamente il server licenze.</span><span class="sxs-lookup"><span data-stu-id="af4ba-109">The discovery scope determines which Remote Desktop Session Host (RD Session Host) servers on the network can automatically discover the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="af4ba-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af4ba-110">Syntax</span></span>


```mof
uint32 ChangeRole(
  [in] uint32 ServerRole
);
```



## <a name="parameters"></a><span data-ttu-id="af4ba-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="af4ba-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af4ba-112">*ServerRole* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af4ba-112">*ServerRole* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af4ba-113">Ambito di individuazione per il server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="af4ba-113">Discovery scope for the Remote Desktop license server.</span></span> <span data-ttu-id="af4ba-114">È possibile impostare uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="af4ba-114">You can set one of the following values.</span></span>

<dt>

<span data-ttu-id="af4ba-115">0</span><span class="sxs-lookup"><span data-stu-id="af4ba-115">0</span></span>
</dt> <dd>

<span data-ttu-id="af4ba-116">I server Host sessione Desktop remoto nello stesso gruppo di lavoro possono individuare il server licenze.</span><span class="sxs-lookup"><span data-stu-id="af4ba-116">RD Session Host servers in the same workgroup can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="af4ba-117">1</span><span class="sxs-lookup"><span data-stu-id="af4ba-117">1</span></span>
</dt> <dd>

<span data-ttu-id="af4ba-118">I server Host sessione Desktop remoto nello stesso dominio possono individuare il server licenze.</span><span class="sxs-lookup"><span data-stu-id="af4ba-118">RD Session Host servers in the same domain can discover the license server.</span></span> <span data-ttu-id="af4ba-119">Per impostare questo valore, è necessario effettuare l'accesso come amministratore di dominio.</span><span class="sxs-lookup"><span data-stu-id="af4ba-119">You must be logged on as a domain administrator to set this value.</span></span>

</dd> <dt>

<span data-ttu-id="af4ba-120">2</span><span class="sxs-lookup"><span data-stu-id="af4ba-120">2</span></span>
</dt> <dd>

<span data-ttu-id="af4ba-121">I server Host sessione Desktop remoto da più domini nella stessa foresta possono individuare il server licenze.</span><span class="sxs-lookup"><span data-stu-id="af4ba-121">RD Session Host servers from multiple domains in the same forest can discover the license server.</span></span> <span data-ttu-id="af4ba-122">Per impostare questo valore, è necessario effettuare l'accesso come amministratore dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="af4ba-122">You must be logged on as an enterprise administrator to set this value.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af4ba-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af4ba-123">Return value</span></span>

<span data-ttu-id="af4ba-124">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="af4ba-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="af4ba-125">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="af4ba-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="af4ba-126">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="af4ba-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="af4ba-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="af4ba-127">Remarks</span></span>

<span data-ttu-id="af4ba-128">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="af4ba-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="af4ba-129">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="af4ba-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="af4ba-130">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="af4ba-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="af4ba-131">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="af4ba-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="af4ba-132">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="af4ba-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="af4ba-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af4ba-133">Requirements</span></span>



| <span data-ttu-id="af4ba-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="af4ba-134">Requirement</span></span> | <span data-ttu-id="af4ba-135">Valore</span><span class="sxs-lookup"><span data-stu-id="af4ba-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="af4ba-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af4ba-136">Minimum supported client</span></span><br/> | <span data-ttu-id="af4ba-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="af4ba-137">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="af4ba-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af4ba-138">Minimum supported server</span></span><br/> | <span data-ttu-id="af4ba-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af4ba-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="af4ba-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="af4ba-140">Namespace</span></span><br/>                | <span data-ttu-id="af4ba-141">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="af4ba-141">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="af4ba-142">MOF</span><span class="sxs-lookup"><span data-stu-id="af4ba-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af4ba-143"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af4ba-143"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="af4ba-144">DLL</span><span class="sxs-lookup"><span data-stu-id="af4ba-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af4ba-145"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af4ba-145"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af4ba-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af4ba-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af4ba-147">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="af4ba-147">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


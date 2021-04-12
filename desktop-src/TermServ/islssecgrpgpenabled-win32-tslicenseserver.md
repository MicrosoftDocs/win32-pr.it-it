---
title: Metodo IsLSSecGrpGPEnabled della classe Win32_TSLicenseServer
description: Recupera un valore che indica se il gruppo di protezione \ 0034; License Server \ 0034; l'impostazione di criteri di gruppo è abilitata nel server licenze Desktop remoto.
ms.assetid: 715b619b-f082-4fed-ac4c-70d5e286e37c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsLSSecGrpGPEnabled
- Metodo IsLSSecGrpGPEnabled Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo IsLSSecGrpGPEnabled
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSSecGrpGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f3d7ec9de3d98849f9680f1b2a87bf5b22922a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120186"
---
# <a name="islssecgrpgpenabled-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="dbb8d-106">Metodo IsLSSecGrpGPEnabled della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="dbb8d-106">IsLSSecGrpGPEnabled method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="dbb8d-107">Recupera un valore che indica se l'impostazione di criteri di gruppo "gruppo di sicurezza del server licenze" è abilitata nel server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="dbb8d-107">Retrieves whether the "license server security group" group policy setting is enabled on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbb8d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dbb8d-108">Syntax</span></span>


```mof
uint32 IsLSSecGrpGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="dbb8d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="dbb8d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbb8d-110">*Abilitato* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dbb8d-110">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbb8d-111">Valore booleano che indica se l'impostazione dei criteri "gruppo di sicurezza del server licenze" è abilitata.</span><span class="sxs-lookup"><span data-stu-id="dbb8d-111">Boolean value that indicates whether the "license server security group" policy setting is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbb8d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dbb8d-112">Return value</span></span>

<span data-ttu-id="dbb8d-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="dbb8d-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="dbb8d-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="dbb8d-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="dbb8d-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="dbb8d-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dbb8d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="dbb8d-116">Remarks</span></span>

<span data-ttu-id="dbb8d-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="dbb8d-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="dbb8d-118">L'impostazione dei criteri "gruppo di sicurezza del server licenze" consente di specificare i server di host sessione Desktop remoto (host sessione Desktop remoto) a cui è consentito contattare il server licenze per ottenere Servizi Desktop remoto licenze CAL (Client Access License).</span><span class="sxs-lookup"><span data-stu-id="dbb8d-118">The "license server security group" policy setting allows you to specify the Remote Desktop Session Host (RD Session Host) servers that are permitted to contact the license server to obtain Remote Desktop Services client access licenses (RDS CALs).</span></span> <span data-ttu-id="dbb8d-119">Se l'impostazione dei criteri è abilitata nel server licenze, il server risponderà solo alle richieste CAL Servizi Desktop remoto dei server Host sessione Desktop remoto i cui account computer sono membri del gruppo locale computer Terminal Server nel server licenze.</span><span class="sxs-lookup"><span data-stu-id="dbb8d-119">If the policy setting is enabled on the license server, the server will only respond to RDS CAL requests from RD Session Host servers whose computer accounts are members of the Terminal Server Computers local group on the license server.</span></span>

<span data-ttu-id="dbb8d-120">L'impostazione dei criteri si trova nel nodo seguente di Editor criteri di gruppo locali:</span><span class="sxs-lookup"><span data-stu-id="dbb8d-120">The policy setting is located in the following node of the local group policy editor:</span></span>

<span data-ttu-id="dbb8d-121">Configurazione computer \\ modelli amministrativi \\ componenti di \\ Servizi Terminal Servizi terminal di Windows \\</span><span class="sxs-lookup"><span data-stu-id="dbb8d-121">Computer Configuration\\Administrative Templates\\Windows Components\\Terminal Services\\TS Licensing</span></span>

<span data-ttu-id="dbb8d-122">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="dbb8d-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dbb8d-123">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="dbb8d-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="dbb8d-124">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="dbb8d-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dbb8d-125">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="dbb8d-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbb8d-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dbb8d-126">Requirements</span></span>



| <span data-ttu-id="dbb8d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbb8d-127">Requirement</span></span> | <span data-ttu-id="dbb8d-128">Valore</span><span class="sxs-lookup"><span data-stu-id="dbb8d-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbb8d-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbb8d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dbb8d-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="dbb8d-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="dbb8d-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbb8d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dbb8d-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbb8d-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="dbb8d-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dbb8d-133">Namespace</span></span><br/>                | <span data-ttu-id="dbb8d-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="dbb8d-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="dbb8d-135">MOF</span><span class="sxs-lookup"><span data-stu-id="dbb8d-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbb8d-136"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbb8d-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbb8d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="dbb8d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbb8d-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbb8d-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbb8d-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dbb8d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbb8d-140">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="dbb8d-140">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


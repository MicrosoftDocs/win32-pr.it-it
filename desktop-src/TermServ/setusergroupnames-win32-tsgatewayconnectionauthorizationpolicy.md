---
title: Metodo SetUserGroupNames della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà UserGroupNames per i criteri di autorizzazione della connessione Desktop remoto (RD \ 160; LIMITE).
ms.assetid: 03c9b2c5-8769-46f2-941f-302d798dd3a1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetUserGroupNames
- Metodo SetUserGroupNames Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo SetUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ca948b63cd106e7284b00c2c5f9e54c6dfa86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302443"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="235f0-106">Metodo SetUserGroupNames della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="235f0-106">SetUserGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="235f0-107">Imposta la proprietà **UserGroupNames** per questo criterio di autorizzazione connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="235f0-107">Sets the **UserGroupNames** property for this Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="235f0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="235f0-108">Syntax</span></span>


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="235f0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="235f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="235f0-110">*UserGroupNames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="235f0-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="235f0-111">Elenco di nomi di gruppi di utenti separati da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="235f0-111">List of semicolon-separated user group names.</span></span> <span data-ttu-id="235f0-112">I nomi sono nel formato *dominio \\ nomegruppoutenti*.</span><span class="sxs-lookup"><span data-stu-id="235f0-112">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="235f0-113">Se l'utente appartiene a uno di questi gruppi di utenti, l'utente sarà autorizzato ad accedere al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="235f0-113">If the user belongs to any of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="235f0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="235f0-114">Return value</span></span>

<span data-ttu-id="235f0-115">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="235f0-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="235f0-116">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="235f0-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="235f0-117">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="235f0-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="235f0-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="235f0-118">Remarks</span></span>

<span data-ttu-id="235f0-119">Se nel parametro *UserGroupNames* sono presenti più nomi di gruppi di utenti e uno dei nomi non può essere elaborato, nessuno dei nomi verrà elaborato.</span><span class="sxs-lookup"><span data-stu-id="235f0-119">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="235f0-120">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="235f0-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="235f0-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="235f0-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="235f0-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="235f0-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="235f0-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="235f0-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="235f0-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="235f0-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="235f0-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="235f0-125">Requirements</span></span>



| <span data-ttu-id="235f0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="235f0-126">Requirement</span></span> | <span data-ttu-id="235f0-127">Valore</span><span class="sxs-lookup"><span data-stu-id="235f0-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="235f0-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="235f0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="235f0-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="235f0-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="235f0-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="235f0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="235f0-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="235f0-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="235f0-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="235f0-132">Namespace</span></span><br/>                | <span data-ttu-id="235f0-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="235f0-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="235f0-134">MOF</span><span class="sxs-lookup"><span data-stu-id="235f0-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="235f0-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="235f0-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="235f0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="235f0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="235f0-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="235f0-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="235f0-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="235f0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="235f0-139">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="235f0-139">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


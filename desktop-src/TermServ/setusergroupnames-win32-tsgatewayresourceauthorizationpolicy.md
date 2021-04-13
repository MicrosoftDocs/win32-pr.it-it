---
title: Metodo SetUserGroupNames della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Imposta la proprietà UserGroupNames per i criteri di autorizzazione risorse di Desktop remoto (RD \ 160; RAP).
ms.assetid: 91b77cd6-779e-460a-88a3-eda7a6fe99e5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetUserGroupNames
- Metodo SetUserGroupNames Servizi Desktop remoto, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto, metodo SetUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708d3eb3a6cc08cd94ba56979fc482a92a530646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120178"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="16af7-106">Metodo SetUserGroupNames della \_ classe TSGatewayResourceAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="16af7-106">SetUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="16af7-107">Imposta la proprietà **UserGroupNames** per i criteri di autorizzazione delle risorse Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="16af7-107">Sets the **UserGroupNames** property for the Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="16af7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16af7-108">Syntax</span></span>


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="16af7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="16af7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16af7-110">*UserGroupNames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16af7-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16af7-111">Elenco delimitato da punti e virgola di nomi di gruppi di utenti.</span><span class="sxs-lookup"><span data-stu-id="16af7-111">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="16af7-112">I nomi sono nel formato *dominio \\ nomegruppoutenti*.</span><span class="sxs-lookup"><span data-stu-id="16af7-112">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="16af7-113">Se l'utente appartiene a uno di questi gruppi di utenti, sarà consentito l'accesso.</span><span class="sxs-lookup"><span data-stu-id="16af7-113">If the user belongs to any of these user groups, access will be permitted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16af7-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16af7-114">Return value</span></span>

<span data-ttu-id="16af7-115">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="16af7-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="16af7-116">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="16af7-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="16af7-117">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="16af7-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="16af7-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="16af7-118">Remarks</span></span>

<span data-ttu-id="16af7-119">Se nel parametro *UserGroupNames* sono presenti più nomi di gruppi di utenti e uno dei nomi non può essere elaborato, nessuno dei nomi verrà elaborato.</span><span class="sxs-lookup"><span data-stu-id="16af7-119">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="16af7-120">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="16af7-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="16af7-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="16af7-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="16af7-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="16af7-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="16af7-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="16af7-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="16af7-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="16af7-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="16af7-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16af7-125">Requirements</span></span>



| <span data-ttu-id="16af7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="16af7-126">Requirement</span></span> | <span data-ttu-id="16af7-127">Valore</span><span class="sxs-lookup"><span data-stu-id="16af7-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="16af7-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16af7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="16af7-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="16af7-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="16af7-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16af7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="16af7-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16af7-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="16af7-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="16af7-132">Namespace</span></span><br/>                | <span data-ttu-id="16af7-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="16af7-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="16af7-134">MOF</span><span class="sxs-lookup"><span data-stu-id="16af7-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16af7-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16af7-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="16af7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="16af7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16af7-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16af7-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="16af7-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16af7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16af7-139">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="16af7-139">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 


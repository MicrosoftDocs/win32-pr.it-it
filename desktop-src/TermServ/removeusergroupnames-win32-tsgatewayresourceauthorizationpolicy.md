---
title: Metodo RemoveUserGroupNames della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Rimuove i nomi dei gruppi di utenti specificati dai gruppi di utenti esistenti nella proprietà UserGroupNames.
ms.assetid: 8538e41a-b9ae-43ce-b19a-40a40f9a12f5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveUserGroupNames
- Metodo RemoveUserGroupNames Servizi Desktop remoto, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto, metodo RemoveUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.RemoveUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6746eaa9d6a7c3cfd82512a4b9f632c873bc9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301616"
---
# <a name="removeusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="bc646-106">Metodo RemoveUserGroupNames della \_ classe TSGatewayResourceAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="bc646-106">RemoveUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="bc646-107">Rimuove i nomi dei gruppi di utenti specificati dai gruppi di utenti esistenti nella proprietà **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="bc646-107">Removes the specified user group names from the existing user groups in the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc646-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc646-108">Syntax</span></span>


```mof
uint32 RemoveUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="bc646-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc646-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc646-110">*UserGroupNames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc646-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc646-111">Elenco delimitato da punti e virgola di nomi di gruppi di utenti.</span><span class="sxs-lookup"><span data-stu-id="bc646-111">Semicolon-separated list of user group names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc646-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc646-112">Return value</span></span>

<span data-ttu-id="bc646-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="bc646-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bc646-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="bc646-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bc646-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bc646-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bc646-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc646-116">Remarks</span></span>

<span data-ttu-id="bc646-117">Se nel parametro *UserGroupNames* sono presenti più nomi di gruppi di utenti e uno dei nomi non può essere elaborato, nessuno dei nomi verrà elaborato.</span><span class="sxs-lookup"><span data-stu-id="bc646-117">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="bc646-118">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="bc646-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="bc646-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bc646-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bc646-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="bc646-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bc646-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="bc646-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bc646-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bc646-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc646-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc646-123">Requirements</span></span>



| <span data-ttu-id="bc646-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc646-124">Requirement</span></span> | <span data-ttu-id="bc646-125">Valore</span><span class="sxs-lookup"><span data-stu-id="bc646-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc646-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc646-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bc646-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bc646-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bc646-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc646-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bc646-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc646-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bc646-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bc646-130">Namespace</span></span><br/>                | <span data-ttu-id="bc646-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="bc646-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bc646-132">MOF</span><span class="sxs-lookup"><span data-stu-id="bc646-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc646-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc646-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc646-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bc646-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc646-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc646-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bc646-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc646-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc646-137">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="bc646-137">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 


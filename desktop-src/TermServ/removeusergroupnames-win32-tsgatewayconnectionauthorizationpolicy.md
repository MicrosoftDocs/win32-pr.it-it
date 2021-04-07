---
title: Metodo RemoveUserGroupNames della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Rimuove i nomi dei gruppi di utenti specificati dai gruppi di utenti esistenti nella proprietà UserGroupNames.
ms.assetid: 4ddbac15-7054-482a-8b5c-49551561673e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveUserGroupNames
- Metodo RemoveUserGroupNames Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo RemoveUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.RemoveUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e4c3d9556243bcb28167378fea6018b4cd2ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963953"
---
# <a name="removeusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="0dcf8-106">Metodo RemoveUserGroupNames della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="0dcf8-106">RemoveUserGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="0dcf8-107">Rimuove i nomi dei gruppi di utenti specificati dai gruppi di utenti esistenti nella proprietà **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="0dcf8-107">Removes specified user group names from the existing user groups in the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dcf8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0dcf8-108">Syntax</span></span>


```mof
uint32 RemoveUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="0dcf8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0dcf8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dcf8-110">*UserGroupNames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0dcf8-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dcf8-111">Nomi dei gruppi di utenti da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0dcf8-111">User group names to remove.</span></span> <span data-ttu-id="0dcf8-112">I nomi dei gruppi di utenti devono essere nel formato *dominio \\ nomegruppoutenti*.</span><span class="sxs-lookup"><span data-stu-id="0dcf8-112">User group names should be of the format *Domain\\UserGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dcf8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0dcf8-113">Return value</span></span>

<span data-ttu-id="0dcf8-114">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="0dcf8-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0dcf8-115">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="0dcf8-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0dcf8-116">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0dcf8-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0dcf8-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="0dcf8-117">Remarks</span></span>

<span data-ttu-id="0dcf8-118">Se nel parametro *UserGroupNames* sono presenti più nomi di gruppi di utenti e uno dei nomi non può essere elaborato, nessuno dei nomi verrà elaborato.</span><span class="sxs-lookup"><span data-stu-id="0dcf8-118">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="0dcf8-119">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="0dcf8-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0dcf8-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0dcf8-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0dcf8-121">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="0dcf8-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0dcf8-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="0dcf8-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0dcf8-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0dcf8-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0dcf8-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0dcf8-124">Requirements</span></span>



| <span data-ttu-id="0dcf8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dcf8-125">Requirement</span></span> | <span data-ttu-id="0dcf8-126">Valore</span><span class="sxs-lookup"><span data-stu-id="0dcf8-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dcf8-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0dcf8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0dcf8-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0dcf8-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0dcf8-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0dcf8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0dcf8-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0dcf8-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0dcf8-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0dcf8-131">Namespace</span></span><br/>                | <span data-ttu-id="0dcf8-132">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0dcf8-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0dcf8-133">MOF</span><span class="sxs-lookup"><span data-stu-id="0dcf8-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0dcf8-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0dcf8-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0dcf8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0dcf8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0dcf8-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dcf8-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0dcf8-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0dcf8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dcf8-138">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="0dcf8-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


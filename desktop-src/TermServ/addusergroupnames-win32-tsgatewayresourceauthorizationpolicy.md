---
title: Metodo AddUserGroupNames della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Aggiunge l'elenco delimitato da punti e virgola di nomi di gruppi di utenti ai gruppi di utenti esistenti nella proprietà UserGroupNames.
ms.assetid: 9cd18ecd-ad56-49c7-954a-2d67bbd7b1db
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddUserGroupNames
- Metodo AddUserGroupNames Servizi Desktop remoto, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto, metodo AddUserGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.AddUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c5c3fcb57c60ff2ca4c14d2e42ff0acdc84f0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963911"
---
# <a name="addusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="fc58b-106">Metodo AddUserGroupNames della \_ classe TSGatewayResourceAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="fc58b-106">AddUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="fc58b-107">Aggiunge l'elenco delimitato da punti e virgola di nomi di gruppi di utenti ai gruppi di utenti esistenti nella proprietà **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="fc58b-107">Adds the specified semicolon-separated list of user group names to the existing user groups in the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc58b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc58b-108">Syntax</span></span>


```mof
uint32 AddUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="fc58b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc58b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc58b-110">*UserGroupNames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc58b-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc58b-111">Elenco delimitato da punti e virgola di nomi di gruppi di utenti da aggiungere alla proprietà **UserGroupNames** .</span><span class="sxs-lookup"><span data-stu-id="fc58b-111">Semicolon-separated list of user group names to add to the **UserGroupNames** property.</span></span> <span data-ttu-id="fc58b-112">I nomi dei gruppi di utenti devono essere nel formato *dominio \\ nomegruppoutenti*.</span><span class="sxs-lookup"><span data-stu-id="fc58b-112">User group names should be of the format *Domain\\UserGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc58b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc58b-113">Return value</span></span>

<span data-ttu-id="fc58b-114">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="fc58b-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fc58b-115">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="fc58b-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fc58b-116">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fc58b-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc58b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc58b-117">Remarks</span></span>

<span data-ttu-id="fc58b-118">Se nel parametro *UserGroupNames* sono presenti più nomi di gruppi di utenti e uno dei nomi non può essere elaborato, nessuno dei nomi verrà elaborato.</span><span class="sxs-lookup"><span data-stu-id="fc58b-118">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="fc58b-119">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="fc58b-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fc58b-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fc58b-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fc58b-121">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="fc58b-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fc58b-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="fc58b-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fc58b-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fc58b-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc58b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc58b-124">Requirements</span></span>



| <span data-ttu-id="fc58b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc58b-125">Requirement</span></span> | <span data-ttu-id="fc58b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="fc58b-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc58b-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc58b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fc58b-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fc58b-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="fc58b-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc58b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fc58b-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc58b-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fc58b-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fc58b-131">Namespace</span></span><br/>                | <span data-ttu-id="fc58b-132">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="fc58b-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="fc58b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="fc58b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc58b-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc58b-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc58b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="fc58b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc58b-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc58b-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fc58b-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc58b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc58b-138">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="fc58b-138">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 


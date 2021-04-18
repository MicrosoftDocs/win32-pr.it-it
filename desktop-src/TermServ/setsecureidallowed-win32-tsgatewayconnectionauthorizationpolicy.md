---
title: Metodo SetSecureIdAllowed della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Questo metodo è riservato per utilizzi futuri.
ms.assetid: 9f49e69a-c004-4e3e-b238-69865e3bf00b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSecureIdAllowed
- Metodo SetSecureIdAllowed Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo SetSecureIdAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSecureIdAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e61c158a7dfcafb6d1d5ac66833e42284b818d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301974"
---
# <a name="setsecureidallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="9cc1f-106">Metodo SetSecureIdAllowed della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="9cc1f-106">SetSecureIdAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="9cc1f-107">Questo metodo è riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="9cc1f-107">This method is reserved for future use.</span></span>

<span data-ttu-id="9cc1f-108">Imposta la proprietà **SecureIdAllowed** , riservata per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="9cc1f-108">Sets the **SecureIdAllowed** property, which is reserved for future use.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc1f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9cc1f-109">Syntax</span></span>


```mof
uint32 SetSecureIdAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="9cc1f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="9cc1f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cc1f-111">*Consentito* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9cc1f-111">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cc1f-112">Nuovo valore di **SecureIdAllowed** .</span><span class="sxs-lookup"><span data-stu-id="9cc1f-112">New **SecureIdAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cc1f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9cc1f-113">Return value</span></span>

<span data-ttu-id="9cc1f-114">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="9cc1f-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9cc1f-115">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="9cc1f-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9cc1f-116">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9cc1f-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9cc1f-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9cc1f-117">Remarks</span></span>

<span data-ttu-id="9cc1f-118">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="9cc1f-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9cc1f-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9cc1f-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9cc1f-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="9cc1f-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9cc1f-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="9cc1f-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9cc1f-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9cc1f-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9cc1f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9cc1f-123">Requirements</span></span>



| <span data-ttu-id="9cc1f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cc1f-124">Requirement</span></span> | <span data-ttu-id="9cc1f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="9cc1f-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc1f-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cc1f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9cc1f-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9cc1f-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9cc1f-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cc1f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9cc1f-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cc1f-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9cc1f-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9cc1f-130">Namespace</span></span><br/>                | <span data-ttu-id="9cc1f-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9cc1f-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9cc1f-132">MOF</span><span class="sxs-lookup"><span data-stu-id="9cc1f-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9cc1f-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9cc1f-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9cc1f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9cc1f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cc1f-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cc1f-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9cc1f-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9cc1f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cc1f-137">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="9cc1f-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


---
title: Metodo SetCookieAuthenticationAllowed della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà CookieAuthenticationAllowed.
ms.assetid: 481b89cb-d73b-4dae-941c-a629c2ae5ac4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetCookieAuthenticationAllowed
- Metodo SetCookieAuthenticationAllowed Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo SetCookieAuthenticationAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetCookieAuthenticationAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9293123ab6ce5b1ddcdb172f9258ba73b23fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119259"
---
# <a name="setcookieauthenticationallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="8d8d3-106">Metodo SetCookieAuthenticationAllowed della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="8d8d3-106">SetCookieAuthenticationAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="8d8d3-107">Imposta la proprietà **CookieAuthenticationAllowed** .</span><span class="sxs-lookup"><span data-stu-id="8d8d3-107">Sets the **CookieAuthenticationAllowed** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d8d3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d8d3-108">Syntax</span></span>


```mof
uint32 SetCookieAuthenticationAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="8d8d3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d8d3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d8d3-110">*Consentito* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d8d3-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d8d3-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8d8d3-111">Type: **boolean**</span></span>

<span data-ttu-id="8d8d3-112">Nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d8d3-112">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d8d3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d8d3-113">Return value</span></span>

<span data-ttu-id="8d8d3-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d8d3-114">Type: **uint32**</span></span>

<span data-ttu-id="8d8d3-115">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="8d8d3-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8d8d3-116">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="8d8d3-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8d8d3-117">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8d8d3-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8d8d3-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d8d3-118">Remarks</span></span>

<span data-ttu-id="8d8d3-119">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="8d8d3-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8d8d3-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8d8d3-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8d8d3-121">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="8d8d3-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8d8d3-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="8d8d3-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8d8d3-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8d8d3-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d8d3-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d8d3-124">Requirements</span></span>



| <span data-ttu-id="8d8d3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d8d3-125">Requirement</span></span> | <span data-ttu-id="8d8d3-126">Valore</span><span class="sxs-lookup"><span data-stu-id="8d8d3-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8d3-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d8d3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8d8d3-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8d8d3-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8d8d3-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d8d3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8d8d3-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8d8d3-130">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="8d8d3-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8d8d3-131">Namespace</span></span><br/>                | <span data-ttu-id="8d8d3-132">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8d8d3-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8d8d3-133">MOF</span><span class="sxs-lookup"><span data-stu-id="8d8d3-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d8d3-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d8d3-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d8d3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8d8d3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d8d3-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d8d3-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8d8d3-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d8d3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d8d3-138">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="8d8d3-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


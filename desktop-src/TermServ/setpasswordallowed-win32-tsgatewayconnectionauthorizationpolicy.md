---
title: Metodo SetPasswordAllowed della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà PasswordAllowed, che Abilita o Disabilita il supporto per l'utilizzo di una password per la connessione al server gateway di Desktop remoto (Gateway Desktop remoto).
ms.assetid: 2d2dfc45-ac2c-41dc-b2c1-4c8eab42c442
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetPasswordAllowed
- Metodo SetPasswordAllowed Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo SetPasswordAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetPasswordAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8bda5fde2fd79cc02697fd270fc307ef5f410f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400878"
---
# <a name="setpasswordallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="2e1a9-106">Metodo SetPasswordAllowed della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="2e1a9-106">SetPasswordAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="2e1a9-107">Imposta la proprietà **PasswordAllowed** , che Abilita o Disabilita il supporto per l'utilizzo di una password per la connessione al server gateway di desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="2e1a9-107">Sets the **PasswordAllowed** property, which enables or disables support for using a password to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e1a9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e1a9-108">Syntax</span></span>


```mof
uint32 SetPasswordAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="2e1a9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e1a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e1a9-110">*Consentito* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e1a9-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e1a9-111">Nuovo valore di **PasswordAllowed** .</span><span class="sxs-lookup"><span data-stu-id="2e1a9-111">New **PasswordAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e1a9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e1a9-112">Return value</span></span>

<span data-ttu-id="2e1a9-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="2e1a9-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2e1a9-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="2e1a9-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2e1a9-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2e1a9-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2e1a9-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e1a9-116">Remarks</span></span>

<span data-ttu-id="2e1a9-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="2e1a9-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2e1a9-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2e1a9-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2e1a9-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="2e1a9-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2e1a9-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="2e1a9-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2e1a9-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2e1a9-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e1a9-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e1a9-122">Requirements</span></span>



| <span data-ttu-id="2e1a9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e1a9-123">Requirement</span></span> | <span data-ttu-id="2e1a9-124">Valore</span><span class="sxs-lookup"><span data-stu-id="2e1a9-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e1a9-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e1a9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2e1a9-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2e1a9-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2e1a9-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e1a9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2e1a9-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e1a9-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2e1a9-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2e1a9-129">Namespace</span></span><br/>                | <span data-ttu-id="2e1a9-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2e1a9-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2e1a9-131">MOF</span><span class="sxs-lookup"><span data-stu-id="2e1a9-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e1a9-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e1a9-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e1a9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2e1a9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e1a9-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e1a9-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2e1a9-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e1a9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e1a9-136">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="2e1a9-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


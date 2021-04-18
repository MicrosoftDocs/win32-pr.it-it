---
title: Metodo SetIdleTimeout della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà IdleTimeout.
ms.assetid: 162224dd-e4d4-483f-9ec4-b87731bc5014
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetIdleTimeout
- Metodo SetIdleTimeout Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo SetIdleTimeout
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetIdleTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c166311477dc9de94ca6c9614e14ac98907b406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302571"
---
# <a name="setidletimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="02aca-106">Metodo SetIdleTimeout della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="02aca-106">SetIdleTimeout method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="02aca-107">Imposta la proprietà **IdleTimeout** .</span><span class="sxs-lookup"><span data-stu-id="02aca-107">Sets the **IdleTimeout** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="02aca-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02aca-108">Syntax</span></span>


```mof
uint32 SetIdleTimeout(
  [in] uint32 IdleTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="02aca-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="02aca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02aca-110">*IdleTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02aca-110">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02aca-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02aca-111">Type: **uint32**</span></span>

<span data-ttu-id="02aca-112">Nuovo valore di timeout, in minuti.</span><span class="sxs-lookup"><span data-stu-id="02aca-112">The new timeout value, in minutes.</span></span> <span data-ttu-id="02aca-113">Il valore 0 indica che non esiste alcun timeout.</span><span class="sxs-lookup"><span data-stu-id="02aca-113">A value of 0 means there is no timeout.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02aca-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02aca-114">Return value</span></span>

<span data-ttu-id="02aca-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02aca-115">Type: **uint32**</span></span>

<span data-ttu-id="02aca-116">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="02aca-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="02aca-117">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="02aca-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="02aca-118">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="02aca-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="02aca-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="02aca-119">Remarks</span></span>

<span data-ttu-id="02aca-120">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="02aca-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="02aca-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="02aca-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="02aca-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="02aca-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="02aca-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="02aca-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="02aca-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="02aca-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="02aca-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02aca-125">Requirements</span></span>



| <span data-ttu-id="02aca-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="02aca-126">Requirement</span></span> | <span data-ttu-id="02aca-127">Valore</span><span class="sxs-lookup"><span data-stu-id="02aca-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="02aca-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02aca-128">Minimum supported client</span></span><br/> | <span data-ttu-id="02aca-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="02aca-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="02aca-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02aca-130">Minimum supported server</span></span><br/> | <span data-ttu-id="02aca-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="02aca-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="02aca-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="02aca-132">Namespace</span></span><br/>                | <span data-ttu-id="02aca-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="02aca-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="02aca-134">MOF</span><span class="sxs-lookup"><span data-stu-id="02aca-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02aca-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02aca-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="02aca-136">DLL</span><span class="sxs-lookup"><span data-stu-id="02aca-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02aca-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02aca-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="02aca-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02aca-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02aca-139">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="02aca-139">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


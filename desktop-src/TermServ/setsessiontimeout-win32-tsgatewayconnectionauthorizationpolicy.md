---
title: Metodo SetSessionTimeout della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta le proprietà SessionTimeout e SessionTimeoutAction.
ms.assetid: 11491c97-3ef8-46c1-9504-696c613e374e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSessionTimeout
- Metodo SetSessionTimeout Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo SetSessionTimeout
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSessionTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e544b59ae4fe0b74d0c120e6884ab81743cac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518160"
---
# <a name="setsessiontimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="42035-106">Metodo SetSessionTimeout della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="42035-106">SetSessionTimeout method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="42035-107">Imposta le proprietà **SessionTimeout** e **SessionTimeoutAction** .</span><span class="sxs-lookup"><span data-stu-id="42035-107">Sets the **SessionTimeout** and **SessionTimeoutAction** properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="42035-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42035-108">Syntax</span></span>


```mof
uint32 SetSessionTimeout(
  [in] uint32 SessionTimeout,
  [in] uint32 SessionTimeoutAction
);
```



## <a name="parameters"></a><span data-ttu-id="42035-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="42035-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42035-110">*SessionTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42035-110">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42035-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42035-111">Type: **uint32**</span></span>

<span data-ttu-id="42035-112">Nuovo valore di timeout, in minuti.</span><span class="sxs-lookup"><span data-stu-id="42035-112">The new timeout value, in minutes.</span></span> <span data-ttu-id="42035-113">Il valore 0 indica che non esiste alcun timeout.</span><span class="sxs-lookup"><span data-stu-id="42035-113">A value of 0 means there is no timeout.</span></span>

</dd> <dt>

<span data-ttu-id="42035-114">*SessionTimeoutAction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42035-114">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42035-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42035-115">Type: **uint32**</span></span>

<span data-ttu-id="42035-116">Specifica l'azione da intraprendere in caso di timeout della sessione.</span><span class="sxs-lookup"><span data-stu-id="42035-116">Specifies the action to be taken in case of a session timeout.</span></span> <span data-ttu-id="42035-117">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="42035-117">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="42035-118">0</span><span class="sxs-lookup"><span data-stu-id="42035-118">0</span></span>
</dt> <dd>

<span data-ttu-id="42035-119">Disconnettere la sessione.</span><span class="sxs-lookup"><span data-stu-id="42035-119">Disconnect the session.</span></span>

</dd> <dt>

<span data-ttu-id="42035-120">1</span><span class="sxs-lookup"><span data-stu-id="42035-120">1</span></span>
</dt> <dd>

<span data-ttu-id="42035-121">Tentativo di autorizzare nuovamente la sessione.</span><span class="sxs-lookup"><span data-stu-id="42035-121">Attempt to re-authorize the session.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42035-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42035-122">Return value</span></span>

<span data-ttu-id="42035-123">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42035-123">Type: **uint32**</span></span>

<span data-ttu-id="42035-124">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="42035-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="42035-125">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="42035-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="42035-126">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="42035-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="42035-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="42035-127">Remarks</span></span>

<span data-ttu-id="42035-128">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="42035-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="42035-129">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="42035-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="42035-130">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="42035-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="42035-131">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="42035-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="42035-132">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="42035-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="42035-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42035-133">Requirements</span></span>



| <span data-ttu-id="42035-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="42035-134">Requirement</span></span> | <span data-ttu-id="42035-135">Valore</span><span class="sxs-lookup"><span data-stu-id="42035-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="42035-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42035-136">Minimum supported client</span></span><br/> | <span data-ttu-id="42035-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="42035-137">None supported</span></span><br/>                                                                |
| <span data-ttu-id="42035-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42035-138">Minimum supported server</span></span><br/> | <span data-ttu-id="42035-139">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="42035-139">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="42035-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="42035-140">Namespace</span></span><br/>                | <span data-ttu-id="42035-141">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="42035-141">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="42035-142">MOF</span><span class="sxs-lookup"><span data-stu-id="42035-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42035-143"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42035-143"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="42035-144">DLL</span><span class="sxs-lookup"><span data-stu-id="42035-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42035-145"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42035-145"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="42035-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42035-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42035-147">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="42035-147">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


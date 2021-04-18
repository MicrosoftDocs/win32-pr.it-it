---
title: Metodo DisablePrinters della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà PrintersDisabled. Se il valore della proprietà DeviceRedirectionType è \ 0034; 2 \ 0034;, la proprietà PrintersDisabled controlla il reindirizzamento delle stampanti per le sessioni stabilite tramite il server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: bf58d226-e3de-4c2b-aaa9-9e7ddbf49d31
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DisablePrinters
- Metodo DisablePrinters Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo DisablePrinters
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisablePrinters
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1625425170bd5e29b953db8299048261e9351bff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301120"
---
# <a name="disableprinters-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="0445d-107">Metodo DisablePrinters della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="0445d-107">DisablePrinters method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="0445d-108">Imposta la proprietà **PrintersDisabled** .</span><span class="sxs-lookup"><span data-stu-id="0445d-108">Sets the **PrintersDisabled** property.</span></span> <span data-ttu-id="0445d-109">Se il valore della proprietà **DeviceRedirectionType** è "2", la proprietà **PrintersDisabled** controlla il reindirizzamento delle stampanti per le sessioni stabilite tramite il server Gateway Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="0445d-109">If the **DeviceRedirectionType** property has a value of "2", the **PrintersDisabled** property controls redirection of the printers for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="0445d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0445d-110">Syntax</span></span>


```mof
uint32 DisablePrinters(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="0445d-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="0445d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0445d-112">*Disabilitato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0445d-112">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0445d-113">Nuovo valore per la proprietà **PrintersDisabled** .</span><span class="sxs-lookup"><span data-stu-id="0445d-113">New value for the **PrintersDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0445d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0445d-114">Return value</span></span>

<span data-ttu-id="0445d-115">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="0445d-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0445d-116">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="0445d-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0445d-117">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0445d-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0445d-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="0445d-118">Remarks</span></span>

<span data-ttu-id="0445d-119">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="0445d-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0445d-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0445d-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0445d-121">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="0445d-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0445d-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="0445d-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0445d-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0445d-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0445d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0445d-124">Requirements</span></span>



| <span data-ttu-id="0445d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0445d-125">Requirement</span></span> | <span data-ttu-id="0445d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="0445d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0445d-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0445d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0445d-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0445d-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0445d-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0445d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0445d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0445d-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0445d-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0445d-131">Namespace</span></span><br/>                | <span data-ttu-id="0445d-132">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0445d-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0445d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="0445d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0445d-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0445d-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0445d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0445d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0445d-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0445d-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0445d-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0445d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0445d-138">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="0445d-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


---
title: Metodo DisableClipboard della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà ClipboardDisabled. Se il valore della proprietà DeviceRedirectionType è \ 0034; 2 \ 0034;, la proprietà ClipboardDisabled controlla il reindirizzamento degli Appunti per le sessioni stabilite tramite il server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: c53fc802-958b-452d-9af9-0ce89ed46079
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DisableClipboard
- Metodo DisableClipboard Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo DisableClipboard
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableClipboard
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ae2070a35fa31f1c9d9ad31e9e632e31c0193f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301124"
---
# <a name="disableclipboard-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="8be89-107">Metodo DisableClipboard della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="8be89-107">DisableClipboard method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="8be89-108">Imposta la proprietà **ClipboardDisabled** .</span><span class="sxs-lookup"><span data-stu-id="8be89-108">Sets the **ClipboardDisabled** property.</span></span> <span data-ttu-id="8be89-109">Se il valore della proprietà **DeviceRedirectionType** è "2", la proprietà **ClipboardDisabled** controlla il reindirizzamento degli Appunti per le sessioni stabilite tramite il server Gateway Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="8be89-109">If the **DeviceRedirectionType** property has a value of "2", the **ClipboardDisabled** property controls redirection of the clipboard for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="8be89-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8be89-110">Syntax</span></span>


```mof
uint32 DisableClipboard(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="8be89-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="8be89-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8be89-112">*Disabilitato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8be89-112">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8be89-113">Nuovo valore per la proprietà **ClipboardDisabled** .</span><span class="sxs-lookup"><span data-stu-id="8be89-113">New value for the **ClipboardDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8be89-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8be89-114">Return value</span></span>

<span data-ttu-id="8be89-115">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="8be89-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8be89-116">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="8be89-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8be89-117">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8be89-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8be89-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="8be89-118">Remarks</span></span>

<span data-ttu-id="8be89-119">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="8be89-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8be89-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8be89-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8be89-121">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="8be89-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8be89-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="8be89-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8be89-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8be89-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8be89-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8be89-124">Requirements</span></span>



| <span data-ttu-id="8be89-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8be89-125">Requirement</span></span> | <span data-ttu-id="8be89-126">Valore</span><span class="sxs-lookup"><span data-stu-id="8be89-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8be89-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8be89-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8be89-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8be89-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8be89-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8be89-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8be89-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8be89-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8be89-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8be89-131">Namespace</span></span><br/>                | <span data-ttu-id="8be89-132">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8be89-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8be89-133">MOF</span><span class="sxs-lookup"><span data-stu-id="8be89-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8be89-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8be89-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8be89-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8be89-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8be89-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8be89-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8be89-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8be89-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8be89-138">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="8be89-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


---
title: Metodo DisableDiskDrives della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà DiskDrivesDisabled.
ms.assetid: bdc4a923-bda7-464a-95eb-95231374ac93
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DisableDiskDrives
- Metodo DisableDiskDrives Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo DisableDiskDrives
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableDiskDrives
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63938ccae6e93e23bd754c1d18ede0008fe92257
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400326"
---
# <a name="disablediskdrives-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="f3112-106">Metodo DisableDiskDrives della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="f3112-106">DisableDiskDrives method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="f3112-107">Imposta la proprietà **DiskDrivesDisabled** .</span><span class="sxs-lookup"><span data-stu-id="f3112-107">Sets the **DiskDrivesDisabled** property.</span></span> <span data-ttu-id="f3112-108">Se il valore della proprietà **DeviceRedirectionType** è "2", la proprietà **DiskDrivesDisabled** controlla il reindirizzamento delle unità disco client per le sessioni stabilite tramite il server Gateway Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="f3112-108">If the **DeviceRedirectionType** property has a value of "2", the **DiskDrivesDisabled** property controls redirection of the client disk drives for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3112-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3112-109">Syntax</span></span>


```mof
uint32 DisableDiskDrives(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="f3112-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3112-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3112-111">*Disabilitato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3112-111">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3112-112">Nuovo valore per la proprietà **DiskDrivesDisabled** .</span><span class="sxs-lookup"><span data-stu-id="f3112-112">New value for the **DiskDrivesDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3112-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3112-113">Return value</span></span>

<span data-ttu-id="f3112-114">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="f3112-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f3112-115">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="f3112-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f3112-116">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f3112-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f3112-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3112-117">Remarks</span></span>

<span data-ttu-id="f3112-118">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="f3112-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f3112-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f3112-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f3112-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="f3112-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f3112-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="f3112-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f3112-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f3112-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3112-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3112-123">Requirements</span></span>



| <span data-ttu-id="f3112-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3112-124">Requirement</span></span> | <span data-ttu-id="f3112-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f3112-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3112-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3112-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f3112-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f3112-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f3112-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3112-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f3112-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3112-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f3112-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f3112-130">Namespace</span></span><br/>                | <span data-ttu-id="f3112-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f3112-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f3112-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f3112-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3112-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3112-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3112-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f3112-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3112-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3112-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f3112-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3112-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3112-137">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="f3112-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


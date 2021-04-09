---
title: Metodo DisableSerialPorts della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà SerialPortsDisabled.
ms.assetid: 95c027e3-f76d-4335-84ac-93a1c3718e66
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DisableSerialPorts
- Metodo DisableSerialPorts Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo DisableSerialPorts
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableSerialPorts
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a4f6941f8bc98d7f8e424a984922ad1f6631c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740415"
---
# <a name="disableserialports-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="04852-106">Metodo DisableSerialPorts della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="04852-106">DisableSerialPorts method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="04852-107">Imposta la proprietà **SerialPortsDisabled** .</span><span class="sxs-lookup"><span data-stu-id="04852-107">Sets the **SerialPortsDisabled** property.</span></span> <span data-ttu-id="04852-108">Se il valore della proprietà **DeviceRedirectionType** è "2", la proprietà **SerialPortsDisabled** controlla il reindirizzamento delle porte seriali per le sessioni stabilite tramite il server Gateway Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="04852-108">If the **DeviceRedirectionType** property has a value of "2", the **SerialPortsDisabled** property controls redirection of the serial ports for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="04852-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04852-109">Syntax</span></span>


```mof
uint32 DisableSerialPorts(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="04852-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="04852-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04852-111">*Disabilitato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04852-111">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04852-112">Nuovo valore per la proprietà **SerialPortsDisabled** .</span><span class="sxs-lookup"><span data-stu-id="04852-112">New value for the **SerialPortsDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04852-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04852-113">Return value</span></span>

<span data-ttu-id="04852-114">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="04852-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="04852-115">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="04852-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="04852-116">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="04852-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="04852-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="04852-117">Remarks</span></span>

<span data-ttu-id="04852-118">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="04852-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="04852-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="04852-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="04852-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="04852-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="04852-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="04852-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="04852-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="04852-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="04852-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04852-123">Requirements</span></span>



| <span data-ttu-id="04852-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="04852-124">Requirement</span></span> | <span data-ttu-id="04852-125">Valore</span><span class="sxs-lookup"><span data-stu-id="04852-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="04852-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04852-126">Minimum supported client</span></span><br/> | <span data-ttu-id="04852-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="04852-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="04852-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04852-128">Minimum supported server</span></span><br/> | <span data-ttu-id="04852-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04852-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="04852-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="04852-130">Namespace</span></span><br/>                | <span data-ttu-id="04852-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="04852-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="04852-132">MOF</span><span class="sxs-lookup"><span data-stu-id="04852-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04852-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04852-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="04852-134">DLL</span><span class="sxs-lookup"><span data-stu-id="04852-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04852-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04852-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="04852-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04852-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04852-137">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="04852-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


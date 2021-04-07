---
title: Metodo SetDeviceRedirectionType della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà DeviceRedirectionType, che consente di controllare i dispositivi da reindirizzare.
ms.assetid: d97a0a7d-a08e-4703-b0f0-ba5d20688dc8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetDeviceRedirectionType
- Metodo SetDeviceRedirectionType Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo SetDeviceRedirectionType
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetDeviceRedirectionType
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98b369e0b6031aa503e2f7f55860d004f63b7f93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964137"
---
# <a name="setdeviceredirectiontype-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="b73a7-106">Metodo SetDeviceRedirectionType della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="b73a7-106">SetDeviceRedirectionType method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="b73a7-107">Imposta la proprietà **DeviceRedirectionType** , che consente di controllare i dispositivi da reindirizzare.</span><span class="sxs-lookup"><span data-stu-id="b73a7-107">Sets the **DeviceRedirectionType** property, which controls which devices will be redirected.</span></span>

## <a name="syntax"></a><span data-ttu-id="b73a7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b73a7-108">Syntax</span></span>


```mof
uint32 SetDeviceRedirectionType(
  [in] uint32 DeviceRedirectionType
);
```



## <a name="parameters"></a><span data-ttu-id="b73a7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b73a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b73a7-110">*DeviceRedirectionType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b73a7-110">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b73a7-111">Tipo di reindirizzamento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b73a7-111">The device redirection type.</span></span>

<dt>

<span data-ttu-id="b73a7-112">0</span><span class="sxs-lookup"><span data-stu-id="b73a7-112">0</span></span>
</dt> <dd>

<span data-ttu-id="b73a7-113">Verranno reindirizzati tutti i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b73a7-113">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="b73a7-114">1</span><span class="sxs-lookup"><span data-stu-id="b73a7-114">1</span></span>
</dt> <dd>

<span data-ttu-id="b73a7-115">Non verrà reindirizzato alcun dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b73a7-115">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="b73a7-116">2</span><span class="sxs-lookup"><span data-stu-id="b73a7-116">2</span></span>
</dt> <dd>

<span data-ttu-id="b73a7-117">I dispositivi specificati non verranno reindirizzati.</span><span class="sxs-lookup"><span data-stu-id="b73a7-117">Specified devices will not be redirected.</span></span> <span data-ttu-id="b73a7-118">Le proprietà **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled** e **PlugAndPlayDevicesDisabled** controllano i dispositivi che non verranno reindirizzati.</span><span class="sxs-lookup"><span data-stu-id="b73a7-118">The **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled**, and **PlugAndPlayDevicesDisabled** properties control which devices will not be redirected.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b73a7-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b73a7-119">Return value</span></span>

<span data-ttu-id="b73a7-120">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="b73a7-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b73a7-121">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="b73a7-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b73a7-122">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b73a7-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b73a7-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="b73a7-123">Remarks</span></span>

<span data-ttu-id="b73a7-124">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="b73a7-124">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b73a7-125">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b73a7-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b73a7-126">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="b73a7-126">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b73a7-127">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b73a7-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b73a7-128">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b73a7-128">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b73a7-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b73a7-129">Requirements</span></span>



| <span data-ttu-id="b73a7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b73a7-130">Requirement</span></span> | <span data-ttu-id="b73a7-131">Valore</span><span class="sxs-lookup"><span data-stu-id="b73a7-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b73a7-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b73a7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b73a7-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b73a7-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b73a7-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b73a7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b73a7-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b73a7-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b73a7-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b73a7-136">Namespace</span></span><br/>                | <span data-ttu-id="b73a7-137">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b73a7-137">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b73a7-138">MOF</span><span class="sxs-lookup"><span data-stu-id="b73a7-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b73a7-139"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b73a7-139"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b73a7-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b73a7-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b73a7-141"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b73a7-141"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b73a7-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b73a7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b73a7-143">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="b73a7-143">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


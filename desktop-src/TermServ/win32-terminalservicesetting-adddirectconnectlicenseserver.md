---
title: Metodo AddDirectConnectLicenseServer della classe Win32_TerminalServiceSetting
description: AddDirectConnectLicenseServer non è più disponibile.
ms.assetid: 7920fd28-0fa3-4f96-bec3-d9e37c97920c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddDirectConnectLicenseServer
- Metodo AddDirectConnectLicenseServer Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo AddDirectConnectLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.AddDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9bba23f5c0bfc69b4c8d7951ab38eac6690b84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400873"
---
# <a name="adddirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="34dd5-106">Metodo AddDirectConnectLicenseServer della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="34dd5-106">AddDirectConnectLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="34dd5-107">\[**AddDirectConnectLicenseServer** non è più disponibile per l'uso a partire da Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="34dd5-107">\[**AddDirectConnectLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="34dd5-108">**Windows Server 2008:** Configura un nuovo server licenze e aggiunge il server licenze al registro di sistema per l'individuazione da parte di host sessione Desktop remoto server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="34dd5-108">**Windows Server 2008:** Configures a new license server and adds the license server to the registry for discovery by Remote Desktop Session Host (RD Session Host) servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="34dd5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34dd5-109">Syntax</span></span>


```mof
uint32 AddDirectConnectLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="34dd5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="34dd5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34dd5-111">*LicenseServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34dd5-111">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34dd5-112">Nome del server licenze da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="34dd5-112">Name of the license server to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34dd5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34dd5-113">Return value</span></span>

<span data-ttu-id="34dd5-114">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="34dd5-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="34dd5-115">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="34dd5-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="34dd5-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="34dd5-116">Remarks</span></span>

<span data-ttu-id="34dd5-117">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="34dd5-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="34dd5-118">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="34dd5-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="34dd5-119">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="34dd5-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="34dd5-120">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="34dd5-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="34dd5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34dd5-121">Requirements</span></span>



| <span data-ttu-id="34dd5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="34dd5-122">Requirement</span></span> | <span data-ttu-id="34dd5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="34dd5-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34dd5-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34dd5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="34dd5-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="34dd5-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="34dd5-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34dd5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="34dd5-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34dd5-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="34dd5-128">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="34dd5-128">End of client support</span></span><br/>    | <span data-ttu-id="34dd5-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="34dd5-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="34dd5-130">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="34dd5-130">End of server support</span></span><br/>    | <span data-ttu-id="34dd5-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34dd5-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="34dd5-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="34dd5-132">Namespace</span></span><br/>                | <span data-ttu-id="34dd5-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="34dd5-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="34dd5-134">MOF</span><span class="sxs-lookup"><span data-stu-id="34dd5-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34dd5-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="34dd5-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="34dd5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="34dd5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34dd5-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34dd5-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34dd5-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34dd5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34dd5-139">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="34dd5-139">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 


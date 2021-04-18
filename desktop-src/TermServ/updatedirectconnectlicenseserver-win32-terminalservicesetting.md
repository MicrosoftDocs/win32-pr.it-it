---
title: Metodo UpdateDirectConnectLicenseServer della classe Win32_TerminalServiceSetting
description: UpdateDirectConnectLicenseServer non è più disponibile.
ms.assetid: 0b6e0dba-e23b-4c8d-8021-93d802501359
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo UpdateDirectConnectLicenseServer
- Metodo UpdateDirectConnectLicenseServer Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo UpdateDirectConnectLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.UpdateDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2249dd00b44955a4e2712b8b7bf746793e89d57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301744"
---
# <a name="updatedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="e711c-106">Metodo UpdateDirectConnectLicenseServer della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="e711c-106">UpdateDirectConnectLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="e711c-107">\[**UpdateDirectConnectLicenseServer** non è più disponibile per l'uso a partire da Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="e711c-107">\[**UpdateDirectConnectLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="e711c-108">**Windows Server 2008:** Aggiorna l'elenco dei server licenze di individuazione.</span><span class="sxs-lookup"><span data-stu-id="e711c-108">**Windows Server 2008:** Updates the list of discovery license servers.</span></span> <span data-ttu-id="e711c-109">L'elenco dei server è delimitato da punti e virgola (";").</span><span class="sxs-lookup"><span data-stu-id="e711c-109">The server list is delimited by semicolons (";").</span></span>

## <a name="syntax"></a><span data-ttu-id="e711c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e711c-110">Syntax</span></span>


```mof
uint32 UpdateDirectConnectLicenseServer(
  [in] string LicenseServerList
);
```



## <a name="parameters"></a><span data-ttu-id="e711c-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="e711c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e711c-112">*LicenseServerList* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e711c-112">*LicenseServerList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e711c-113">Elenco dei server licenze.</span><span class="sxs-lookup"><span data-stu-id="e711c-113">List of license servers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e711c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e711c-114">Return value</span></span>

<span data-ttu-id="e711c-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="e711c-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e711c-116">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="e711c-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="e711c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e711c-117">Remarks</span></span>

<span data-ttu-id="e711c-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e711c-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e711c-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="e711c-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e711c-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="e711c-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e711c-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e711c-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e711c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e711c-122">Requirements</span></span>



| <span data-ttu-id="e711c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e711c-123">Requirement</span></span> | <span data-ttu-id="e711c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e711c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e711c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e711c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e711c-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e711c-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e711c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e711c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e711c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e711c-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e711c-129">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e711c-129">End of client support</span></span><br/>    | <span data-ttu-id="e711c-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e711c-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e711c-131">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="e711c-131">End of server support</span></span><br/>    | <span data-ttu-id="e711c-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e711c-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e711c-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e711c-133">Namespace</span></span><br/>                | <span data-ttu-id="e711c-134">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e711c-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e711c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e711c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e711c-136"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e711c-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e711c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e711c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e711c-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e711c-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e711c-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e711c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e711c-140">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="e711c-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 


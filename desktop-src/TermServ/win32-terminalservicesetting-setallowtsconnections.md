---
title: Metodo SetAllowTSConnections della classe Win32_TerminalServiceSetting
description: Il metodo SetAllowTSConnections consente o nega nuove connessioni Desktop remoto. Questo metodo modificherà la proprietà AllowTSConnections per la classe di conseguenza.
ms.assetid: 6cbaea62-ced0-4788-99fb-5b36816b80a1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetAllowTSConnections
- Metodo SetAllowTSConnections Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetAllowTSConnections
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetAllowTSConnections
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e800f1a47567f16d916563d4d1e62c767016329a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478833"
---
# <a name="setallowtsconnections-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="41e1e-107">Metodo SetAllowTSConnections della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="41e1e-107">SetAllowTSConnections method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="41e1e-108">Il metodo **SetAllowTSConnections** consente o nega nuove connessioni Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="41e1e-108">The **SetAllowTSConnections** method allows or denies new remote desktop connections.</span></span> <span data-ttu-id="41e1e-109">Questo metodo modificherà la proprietà **AllowTSConnections** per la classe di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="41e1e-109">This method will modify the **AllowTSConnections** property for the class accordingly.</span></span>

## <a name="syntax"></a><span data-ttu-id="41e1e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41e1e-110">Syntax</span></span>


```mof
uint32 SetAllowTSConnections(
  [in] uint32 AllowTSConnections,
  [in] uint32 ModifyFirewallException
);
```



## <a name="parameters"></a><span data-ttu-id="41e1e-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="41e1e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41e1e-112">*AllowTSConnections* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41e1e-112">*AllowTSConnections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e1e-113">Specifica se sono consentite nuove connessioni Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="41e1e-113">Specifies whether new remote desktop connections are allowed.</span></span> <span data-ttu-id="41e1e-114">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="41e1e-114">This must be one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="41e1e-115"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="41e1e-115"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="41e1e-116">Non sono consentite nuove connessioni.</span><span class="sxs-lookup"><span data-stu-id="41e1e-116">New connections are not allowed.</span></span> <span data-ttu-id="41e1e-117">Se il parametro *ModifyFirewallException* è 1, l'eccezione desktop remoto firewall è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="41e1e-117">If the *ModifyFirewallException* parameter is 1, then the Remote Desktop firewall exception is disabled.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="41e1e-118"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="41e1e-118"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="41e1e-119">Sono consentite nuove connessioni.</span><span class="sxs-lookup"><span data-stu-id="41e1e-119">New connections are allowed.</span></span> <span data-ttu-id="41e1e-120">Se il parametro *ModifyFirewallException* è 1, l'eccezione desktop remoto firewall è abilitata.</span><span class="sxs-lookup"><span data-stu-id="41e1e-120">If the *ModifyFirewallException* parameter is 1, then the Remote Desktop firewall exception is enabled.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="41e1e-121">*ModifyFirewallException* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41e1e-121">*ModifyFirewallException* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e1e-122">Specifica se l'impostazione di eccezione del firewall per Desktop remoto verrà modificata nello stato specificato dal parametro *AllowTSConnections* .</span><span class="sxs-lookup"><span data-stu-id="41e1e-122">Specifies if the firewall exception setting for Remote Desktop will be modified to the state specified by the *AllowTSConnections* parameter.</span></span> <span data-ttu-id="41e1e-123">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="41e1e-123">This must be one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="41e1e-124"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="41e1e-124"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="41e1e-125">Non modificare l'impostazione delle eccezioni del firewall.</span><span class="sxs-lookup"><span data-stu-id="41e1e-125">Do not modify the firewall exception setting.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="41e1e-126"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="41e1e-126"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="41e1e-127">Modificare l'impostazione di eccezione del firewall.</span><span class="sxs-lookup"><span data-stu-id="41e1e-127">Modify the firewall exception setting.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41e1e-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41e1e-128">Return value</span></span>

<span data-ttu-id="41e1e-129">Restituisce esito positivo in caso di esito positivo; in caso contrario, restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="41e1e-129">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="41e1e-130">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="41e1e-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="41e1e-131">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="41e1e-131">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="41e1e-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="41e1e-132">Remarks</span></span>

<span data-ttu-id="41e1e-133">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="41e1e-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="41e1e-134">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="41e1e-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="41e1e-135">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="41e1e-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="41e1e-136">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="41e1e-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="41e1e-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41e1e-137">Requirements</span></span>



| <span data-ttu-id="41e1e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="41e1e-138">Requirement</span></span> | <span data-ttu-id="41e1e-139">Valore</span><span class="sxs-lookup"><span data-stu-id="41e1e-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41e1e-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41e1e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="41e1e-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41e1e-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41e1e-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41e1e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="41e1e-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41e1e-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41e1e-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="41e1e-144">Namespace</span></span><br/>                | <span data-ttu-id="41e1e-145">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="41e1e-145">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="41e1e-146">MOF</span><span class="sxs-lookup"><span data-stu-id="41e1e-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41e1e-147"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41e1e-147"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="41e1e-148">DLL</span><span class="sxs-lookup"><span data-stu-id="41e1e-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41e1e-149"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41e1e-149"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41e1e-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41e1e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e1e-151">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="41e1e-151">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 


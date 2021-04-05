---
title: Classe MDM_Policy_Result01_DeviceLock02
description: La \_ \_ classe Result01 DeviceLock02 dei criteri MDM \_ rappresenta i criteri di blocco del dispositivo disponibili.
ms.assetid: 9aac25a8-8502-468f-9478-1ac4ccccaf0b
keywords:
- Classe MDM_Policy_Result01_DeviceLock02
- Classe MDM_Policy_Result01_DeviceLock02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceLock02
- MDM_Policy_Result01_DeviceLock02.InstanceID
- MDM_Policy_Result01_DeviceLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa93236b99add5cb49e0b54aa10eab9e959ab01a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873862"
---
# <a name="mdm_policy_result01_devicelock02-class"></a><span data-ttu-id="921a1-105">\_ \_ Classe Result01 DeviceLock02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="921a1-105">MDM\_Policy\_Result01\_DeviceLock02 class</span></span>

<span data-ttu-id="921a1-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="921a1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="921a1-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="921a1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="921a1-108">La **classe \_ \_ Result01 \_ DeviceLock02 dei criteri MDM** rappresenta i criteri di blocco del dispositivo disponibili.</span><span class="sxs-lookup"><span data-stu-id="921a1-108">The **MDM\_Policy\_Result01\_DeviceLock02** class represents the device lock policies available.</span></span>

<span data-ttu-id="921a1-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="921a1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="921a1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="921a1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceLock02
{
  string InstanceID;
  string ParentID;
  sint32 AllowScreenTimeoutWhileLockedUserConfig;
  sint32 AllowSimpleDevicePassword;
  sint32 AlphanumericDevicePasswordRequired;
  sint32 DevicePasswordEnabled;
  sint32 DevicePasswordExpiration;
  sint32 DevicePasswordHistory;
  string EnforceLockScreenAndLogonImage;
  string EnforceLockScreenProvider;
  sint32 MinimumPasswordAge;
  sint32 MaxDevicePasswordFailedAttempts;
  sint32 MaxInactivityTimeDeviceLock;
  sint32 MinDevicePasswordComplexCharacters;
  sint32 MinDevicePasswordLength;
  sint32 ScreenTimeoutWhileLocked;
  string PreventLockScreenSlideShow;
};
```

## <a name="members"></a><span data-ttu-id="921a1-111">Members</span><span class="sxs-lookup"><span data-stu-id="921a1-111">Members</span></span>

<span data-ttu-id="921a1-112">La **classe \_ \_ Result01 \_ DeviceLock02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="921a1-112">The **MDM\_Policy\_Result01\_DeviceLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="921a1-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="921a1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="921a1-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="921a1-114">Properties</span></span>

<span data-ttu-id="921a1-115">La **classe \_ \_ \_ DeviceLock02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="921a1-115">The **MDM\_Policy\_Result01\_DeviceLock02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="921a1-116">AllowScreenTimeoutWhileLockedUserConfig</span><span class="sxs-lookup"><span data-stu-id="921a1-116">AllowScreenTimeoutWhileLockedUserConfig</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="921a1-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="921a1-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="921a1-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="921a1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="921a1-119">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="921a1-119">AllowSimpleDevicePassword</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-allowsimpledevicepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="921a1-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="921a1-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="921a1-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="921a1-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="921a1-122">AlphanumericDevicePasswordRequired</span><span class="sxs-lookup"><span data-stu-id="921a1-122">AlphanumericDevicePasswordRequired</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired)
</dt> <dd> <dl> <dt>

<span data-ttu-id="921a1-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="921a1-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="921a1-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="921a1-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="921a1-125">DevicePasswordEnabled</span><span class="sxs-lookup"><span data-stu-id="921a1-125">DevicePasswordEnabled</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="921a1-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="921a1-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="921a1-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="921a1-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="921a1-128">DevicePasswordExpiration</span><span class="sxs-lookup"><span data-stu-id="921a1-128">DevicePasswordExpiration</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordexpiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="921a1-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="921a1-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="921a1-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="921a1-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="921a1-131">DevicePasswordHistory</span><span class="sxs-lookup"><span data-stu-id="921a1-131">DevicePasswordHistory</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="921a1-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="921a1-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="921a1-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="921a1-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="921a1-134">EnforceLockScreenAndLogonImage</span><span class="sxs-lookup"><span data-stu-id="921a1-134">EnforceLockScreenAndLogonImage</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-enforcelockscreenandlogonimage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="921a1-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="921a1-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="921a1-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="921a1-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="921a1-137">EnforceLockScreenProvider</span><span class="sxs-lookup"><span data-stu-id="921a1-137">EnforceLockScreenProvider</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="921a1-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="921a1-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="921a1-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="921a1-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="921a1-140">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="921a1-140">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="921a1-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="921a1-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="921a1-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="921a1-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="921a1-143">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="921a1-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="921a1-144">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="921a1-144">Identifies the name of the parent node.</span></span> <span data-ttu-id="921a1-145">Per questa classe la stringa è "DeviceLock".</span><span class="sxs-lookup"><span data-stu-id="921a1-145">For this class, the string is "DeviceLock".</span></span>

</dd> <dt>

[<span data-ttu-id="921a1-146">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="921a1-146">MaxDevicePasswordFailedAttempts</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxdevicepasswordfailedattempts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="921a1-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="921a1-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="921a1-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="921a1-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="921a1-149">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="921a1-149">MaxInactivityTimeDeviceLock</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxinactivitytimedevicelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="921a1-150">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="921a1-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="921a1-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="921a1-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="921a1-152">MinDevicePasswordComplexCharacters consente</span><span class="sxs-lookup"><span data-stu-id="921a1-152">MinDevicePasswordComplexCharacters</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordcomplexcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="921a1-153">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="921a1-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="921a1-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="921a1-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="921a1-155">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="921a1-155">MinDevicePasswordLength</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="921a1-156">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="921a1-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="921a1-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="921a1-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="921a1-158">MinimumPasswordAge</span><span class="sxs-lookup"><span data-stu-id="921a1-158">MinimumPasswordAge</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-minimumpasswordage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="921a1-159">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="921a1-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="921a1-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="921a1-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="921a1-161">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="921a1-161">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="921a1-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="921a1-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="921a1-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="921a1-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="921a1-164">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="921a1-164">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="921a1-165">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="921a1-165">Describes the full path to the parent node.</span></span> <span data-ttu-id="921a1-166">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="921a1-166">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="921a1-167">PreventLockScreenSlideShow</span><span class="sxs-lookup"><span data-stu-id="921a1-167">PreventLockScreenSlideShow</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-preventlockscreenslideshow)
</dt> <dd> <dl> <dt>

<span data-ttu-id="921a1-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="921a1-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="921a1-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="921a1-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="921a1-170">ScreenTimeoutWhileLocked</span><span class="sxs-lookup"><span data-stu-id="921a1-170">ScreenTimeoutWhileLocked</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="921a1-171">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="921a1-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="921a1-172">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="921a1-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="921a1-173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="921a1-173">Requirements</span></span>



| <span data-ttu-id="921a1-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="921a1-174">Requirement</span></span> | <span data-ttu-id="921a1-175">Valore</span><span class="sxs-lookup"><span data-stu-id="921a1-175">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="921a1-176">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="921a1-176">Minimum supported client</span></span><br/> | <span data-ttu-id="921a1-177">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="921a1-177">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="921a1-178">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="921a1-178">Minimum supported server</span></span><br/> | <span data-ttu-id="921a1-179">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="921a1-179">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="921a1-180">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="921a1-180">Namespace</span></span><br/>                | <span data-ttu-id="921a1-181">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="921a1-181">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="921a1-182">MOF</span><span class="sxs-lookup"><span data-stu-id="921a1-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="921a1-183"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="921a1-183"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="921a1-184">DLL</span><span class="sxs-lookup"><span data-stu-id="921a1-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="921a1-185"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="921a1-185"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="921a1-186">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="921a1-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="921a1-187">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="921a1-187">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


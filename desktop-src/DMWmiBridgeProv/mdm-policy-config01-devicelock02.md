---
title: Classe MDM_Policy_Config01_DeviceLock02
description: La \_ \_ classe Config01 DeviceLock02 dei criteri MDM \_ rappresenta i criteri di blocco del dispositivo disponibili.
ms.assetid: 222081ec-c38f-481d-ae38-941fd1317197
keywords:
- Classe MDM_Policy_Config01_DeviceLock02
- Classe MDM_Policy_Config01_DeviceLock02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeviceLock02
- MDM_Policy_Config01_DeviceLock02.InstanceID
- MDM_Policy_Config01_DeviceLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c5926912d276fbe04f75c161196c47d0f0dd384
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121135"
---
# <a name="mdm_policy_config01_devicelock02-class"></a><span data-ttu-id="3b8c0-105">\_ \_ Classe Config01 DeviceLock02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="3b8c0-105">MDM\_Policy\_Config01\_DeviceLock02 class</span></span>

<span data-ttu-id="3b8c0-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3b8c0-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="3b8c0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3b8c0-108">La **classe \_ \_ Config01 \_ DeviceLock02 dei criteri MDM** rappresenta i criteri di blocco del dispositivo disponibili.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-108">The **MDM\_Policy\_Config01\_DeviceLock02** class represents the device lock policies available.</span></span>

<span data-ttu-id="3b8c0-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b8c0-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b8c0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeviceLock02
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

## <a name="members"></a><span data-ttu-id="3b8c0-111">Members</span><span class="sxs-lookup"><span data-stu-id="3b8c0-111">Members</span></span>

<span data-ttu-id="3b8c0-112">La **classe \_ \_ Config01 \_ DeviceLock02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3b8c0-112">The **MDM\_Policy\_Config01\_DeviceLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="3b8c0-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3b8c0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b8c0-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3b8c0-114">Properties</span></span>

<span data-ttu-id="3b8c0-115">La **classe \_ \_ \_ DeviceLock02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-115">The **MDM\_Policy\_Config01\_DeviceLock02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b8c0-116">AllowScreenTimeoutWhileLockedUserConfig</span><span class="sxs-lookup"><span data-stu-id="3b8c0-116">AllowScreenTimeoutWhileLockedUserConfig</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b8c0-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3b8c0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b8c0-119">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="3b8c0-119">AllowSimpleDevicePassword</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-allowsimpledevicepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b8c0-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3b8c0-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b8c0-122">AlphanumericDevicePasswordRequired</span><span class="sxs-lookup"><span data-stu-id="3b8c0-122">AlphanumericDevicePasswordRequired</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b8c0-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3b8c0-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b8c0-125">DevicePasswordEnabled</span><span class="sxs-lookup"><span data-stu-id="3b8c0-125">DevicePasswordEnabled</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b8c0-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3b8c0-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3b8c0-128">DevicePasswordEnabled non deve essere impostato su Enabled (0) quando WMI viene usato per impostare i criteri di DeviceLock EAS, dato che è abilitato per impostazione predefinita nei criteri CSP per back compat con Windows 8. x.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-128">DevicePasswordEnabled should not be set to Enabled (0) when WMI is used to set the EAS DeviceLock policies given that it is Enabled by default in Policy CSP for back compat with Windows 8.x.</span></span> <span data-ttu-id="3b8c0-129">Se DevicePasswordEnabled è impostato su Enabled (0), i criteri CSP restituiranno un errore che informa che DevicePasswordEnabled esiste già.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-129">If DevicePasswordEnabled is set to Enabled(0) then Policy CSP will return an error stating that DevicePasswordEnabled already exists.</span></span> <span data-ttu-id="3b8c0-130">Windows 8. x non supporta i criteri di DevicePassword.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-130">Windows 8.x did not support DevicePassword policy.</span></span> <span data-ttu-id="3b8c0-131">Quando si disabilita DevicePasswordEnabled (1), questo deve essere l'unico set di criteri del gruppo DeviceLock di criteri riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-131">When disabling DevicePasswordEnabled  (1) then this should be the only policy set from the DeviceLock group of policies below.</span></span> <span data-ttu-id="3b8c0-132">I criteri sono elencati di seguito: >-DevicePasswordEnabled è il criterio padre dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="3b8c0-132">The policies are listed below: > - DevicePasswordEnabled is the parent policy of the following:</span></span>

-   <span data-ttu-id="3b8c0-133">DevicePasswordEnabled è il criterio padre dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="3b8c0-133">DevicePasswordEnabled is the parent policy of the following:</span></span>
    -   <span data-ttu-id="3b8c0-134">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="3b8c0-134">AllowSimpleDevicePassword</span></span>
    -   <span data-ttu-id="3b8c0-135">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="3b8c0-135">MinDevicePasswordLength</span></span>
    -   <span data-ttu-id="3b8c0-136">AlphanumericDevicePasswordRequired è il criterio padre di:</span><span class="sxs-lookup"><span data-stu-id="3b8c0-136">AlphanumericDevicePasswordRequired is the parent policy of:</span></span>
        -   <span data-ttu-id="3b8c0-137">MinDevicePasswordComplexCharacters consente</span><span class="sxs-lookup"><span data-stu-id="3b8c0-137">MinDevicePasswordComplexCharacters</span></span> 
    -   <span data-ttu-id="3b8c0-138">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="3b8c0-138">MaxDevicePasswordFailedAttempts</span></span>
    -   <span data-ttu-id="3b8c0-139">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="3b8c0-139">MaxInactivityTimeDeviceLock</span></span>

</dd> <dt>

[<span data-ttu-id="3b8c0-140">DevicePasswordExpiration</span><span class="sxs-lookup"><span data-stu-id="3b8c0-140">DevicePasswordExpiration</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordexpiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b8c0-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3b8c0-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b8c0-143">DevicePasswordHistory</span><span class="sxs-lookup"><span data-stu-id="3b8c0-143">DevicePasswordHistory</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b8c0-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3b8c0-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b8c0-146">EnforceLockScreenAndLogonImage</span><span class="sxs-lookup"><span data-stu-id="3b8c0-146">EnforceLockScreenAndLogonImage</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-enforcelockscreenandlogonimage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b8c0-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3b8c0-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3b8c0-149">EnforceLockScreenProvider</span><span class="sxs-lookup"><span data-stu-id="3b8c0-149">EnforceLockScreenProvider</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b8c0-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3b8c0-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3b8c0-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b8c0-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b8c0-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-155">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3b8c0-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3b8c0-156">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="3b8c0-157">Per questa classe la stringa è "DeviceLock".</span><span class="sxs-lookup"><span data-stu-id="3b8c0-157">For this class, the string is "DeviceLock".</span></span>

</dd> <dt>

[<span data-ttu-id="3b8c0-158">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="3b8c0-158">MaxDevicePasswordFailedAttempts</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxdevicepasswordfailedattempts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b8c0-159">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3b8c0-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b8c0-161">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="3b8c0-161">MaxInactivityTimeDeviceLock</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxinactivitytimedevicelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b8c0-162">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-163">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3b8c0-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b8c0-164">MinDevicePasswordComplexCharacters consente</span><span class="sxs-lookup"><span data-stu-id="3b8c0-164">MinDevicePasswordComplexCharacters</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordcomplexcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b8c0-165">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3b8c0-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b8c0-167">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="3b8c0-167">MinDevicePasswordLength</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b8c0-168">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3b8c0-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b8c0-170">MinimumPasswordAge</span><span class="sxs-lookup"><span data-stu-id="3b8c0-170">MinimumPasswordAge</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-minimumpasswordage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b8c0-171">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-172">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3b8c0-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3b8c0-173">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-173">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b8c0-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b8c0-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-176">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3b8c0-176">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3b8c0-177">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="3b8c0-177">Describes the full path to the parent node.</span></span> <span data-ttu-id="3b8c0-178">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="3b8c0-178">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="3b8c0-179">PreventLockScreenSlideShow</span><span class="sxs-lookup"><span data-stu-id="3b8c0-179">PreventLockScreenSlideShow</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-preventlockscreenslideshow)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b8c0-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-181">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3b8c0-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3b8c0-182">ScreenTimeoutWhileLocked</span><span class="sxs-lookup"><span data-stu-id="3b8c0-182">ScreenTimeoutWhileLocked</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b8c0-183">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3b8c0-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b8c0-184">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3b8c0-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b8c0-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b8c0-185">Requirements</span></span>



| <span data-ttu-id="3b8c0-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b8c0-186">Requirement</span></span> | <span data-ttu-id="3b8c0-187">Valore</span><span class="sxs-lookup"><span data-stu-id="3b8c0-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b8c0-188">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b8c0-188">Minimum supported client</span></span><br/> | <span data-ttu-id="3b8c0-189">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3b8c0-189">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3b8c0-190">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b8c0-190">Minimum supported server</span></span><br/> | <span data-ttu-id="3b8c0-191">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3b8c0-191">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3b8c0-192">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3b8c0-192">Namespace</span></span><br/>                | <span data-ttu-id="3b8c0-193">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="3b8c0-193">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="3b8c0-194">MOF</span><span class="sxs-lookup"><span data-stu-id="3b8c0-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b8c0-195"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b8c0-195"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b8c0-196">DLL</span><span class="sxs-lookup"><span data-stu-id="3b8c0-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b8c0-197"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b8c0-197"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b8c0-198">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b8c0-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b8c0-199">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="3b8c0-199">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


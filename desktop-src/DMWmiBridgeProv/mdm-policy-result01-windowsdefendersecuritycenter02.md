---
title: Classe MDM_Policy_Result01_WindowsDefenderSecurityCenter02
description: La \_ \_ classe Result01 WindowsDefenderSecurityCenter02 dei criteri MDM \_ rappresenta i criteri di Windows Defender Security Center.
ms.assetid: 59047e16-a188-4ec9-9d1b-db2b15c1109b
keywords:
- Classe MDM_Policy_Result01_WindowsDefenderSecurityCenter02
- Classe MDM_Policy_Result01_WindowsDefenderSecurityCenter02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02.InstanceID
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7739410347169637ca5f27fef5627e26f8347c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475311"
---
# <a name="mdm_policy_result01_windowsdefendersecuritycenter02-class"></a><span data-ttu-id="92ad0-105">\_ \_ Classe Result01 WindowsDefenderSecurityCenter02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="92ad0-105">MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02 class</span></span>

<span data-ttu-id="92ad0-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="92ad0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="92ad0-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="92ad0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="92ad0-108">La \_ \_ classe Result01 WindowsDefenderSecurityCenter02 dei criteri MDM \_ rappresenta i criteri di Windows Defender Security Center.</span><span class="sxs-lookup"><span data-stu-id="92ad0-108">The MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02 class represents the Windows Defender Security Center policies.</span></span>

<span data-ttu-id="92ad0-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="92ad0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="92ad0-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92ad0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WindowsDefenderSecurityCenter02
{
  string InstanceID;
  string ParentID;
  string CompanyName;
  sint32 DisableAppBrowserUI;
  sint32 DisableEnhancedNotifications;
  sint32 DisableFamilyUI;
  sint32 DisableHealthUI;
  sint32 DisableNetworkUI;
  sint32 DisableNotifications;
  sint32 DisableVirusUI;
  sint32 DisallowExploitProtectionOverride;
  string Email;
  sint32 EnableCustomizedToasts;
  sint32 EnableInAppCustomization;
  string Phone;
  string URL;
};
```

## <a name="members"></a><span data-ttu-id="92ad0-111">Members</span><span class="sxs-lookup"><span data-stu-id="92ad0-111">Members</span></span>

<span data-ttu-id="92ad0-112">La **classe \_ \_ Result01 \_ WindowsDefenderSecurityCenter02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="92ad0-112">The **MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02** class has these types of members:</span></span>

-   [<span data-ttu-id="92ad0-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="92ad0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92ad0-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="92ad0-114">Properties</span></span>

<span data-ttu-id="92ad0-115">La **classe \_ \_ \_ WindowsDefenderSecurityCenter02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="92ad0-115">The **MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="92ad0-116">CompanyName</span><span class="sxs-lookup"><span data-stu-id="92ad0-116">CompanyName</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-companyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="92ad0-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="92ad0-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="92ad0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="92ad0-119">DisableAppBrowserUI</span><span class="sxs-lookup"><span data-stu-id="92ad0-119">DisableAppBrowserUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableappbrowserui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="92ad0-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="92ad0-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="92ad0-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="92ad0-122">DisableEnhancedNotifications</span><span class="sxs-lookup"><span data-stu-id="92ad0-122">DisableEnhancedNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableenhancednotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="92ad0-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="92ad0-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="92ad0-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="92ad0-125">DisableFamilyUI</span><span class="sxs-lookup"><span data-stu-id="92ad0-125">DisableFamilyUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablefamilyui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="92ad0-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="92ad0-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="92ad0-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="92ad0-128">DisableHealthUI</span><span class="sxs-lookup"><span data-stu-id="92ad0-128">DisableHealthUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablehealthui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="92ad0-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="92ad0-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="92ad0-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="92ad0-131">DisableNetworkUI</span><span class="sxs-lookup"><span data-stu-id="92ad0-131">DisableNetworkUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenetworkui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="92ad0-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="92ad0-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="92ad0-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="92ad0-134">DisableNotifications</span><span class="sxs-lookup"><span data-stu-id="92ad0-134">DisableNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="92ad0-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="92ad0-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="92ad0-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="92ad0-137">DisableVirusUI</span><span class="sxs-lookup"><span data-stu-id="92ad0-137">DisableVirusUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablevirusui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="92ad0-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="92ad0-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="92ad0-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="92ad0-140">DisallowExploitProtectionOverride</span><span class="sxs-lookup"><span data-stu-id="92ad0-140">DisallowExploitProtectionOverride</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disallowexploitprotectionoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="92ad0-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="92ad0-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="92ad0-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="92ad0-143">Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="92ad0-143">Email</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-email)
</dt> <dd> <dl> <dt>

<span data-ttu-id="92ad0-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="92ad0-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="92ad0-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="92ad0-146">EnableCustomizedToasts</span><span class="sxs-lookup"><span data-stu-id="92ad0-146">EnableCustomizedToasts</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enablecustomizedtoasts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="92ad0-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="92ad0-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="92ad0-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="92ad0-149">EnableInAppCustomization</span><span class="sxs-lookup"><span data-stu-id="92ad0-149">EnableInAppCustomization</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enableinappcustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="92ad0-150">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="92ad0-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="92ad0-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="92ad0-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="92ad0-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92ad0-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="92ad0-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="92ad0-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-155">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="92ad0-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="92ad0-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="92ad0-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92ad0-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="92ad0-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="92ad0-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-159">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="92ad0-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="92ad0-160">Telefono</span><span class="sxs-lookup"><span data-stu-id="92ad0-160">Phone</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-phone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="92ad0-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="92ad0-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-162">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="92ad0-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="92ad0-163">URL</span><span class="sxs-lookup"><span data-stu-id="92ad0-163">URL</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-url)
</dt> <dd> <dl> <dt>

<span data-ttu-id="92ad0-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="92ad0-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92ad0-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="92ad0-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92ad0-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92ad0-166">Requirements</span></span>



| <span data-ttu-id="92ad0-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="92ad0-167">Requirement</span></span> | <span data-ttu-id="92ad0-168">Valore</span><span class="sxs-lookup"><span data-stu-id="92ad0-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92ad0-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92ad0-169">Minimum supported client</span></span><br/> | <span data-ttu-id="92ad0-170">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="92ad0-170">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="92ad0-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92ad0-171">Minimum supported server</span></span><br/> | <span data-ttu-id="92ad0-172">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="92ad0-172">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="92ad0-173">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="92ad0-173">Namespace</span></span><br/>                | <span data-ttu-id="92ad0-174">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="92ad0-174">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="92ad0-175">MOF</span><span class="sxs-lookup"><span data-stu-id="92ad0-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92ad0-176"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92ad0-176"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="92ad0-177">DLL</span><span class="sxs-lookup"><span data-stu-id="92ad0-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92ad0-178"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92ad0-178"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

